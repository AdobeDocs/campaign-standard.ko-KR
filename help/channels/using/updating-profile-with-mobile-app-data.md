---
solution: Campaign Standard
product: campaign
title: 모바일 애플리케이션 데이터를 기반으로 프로필 정보 만들고 업데이트하기
description: 모바일 애플리케이션 데이터를 기반으로 프로필 정보를 만들고 업데이트하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: delivery,mobileAppContent,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 4%

---


# 모바일 애플리케이션 데이터를 기반으로 프로필 정보 만들고 업데이트하기

## 개요

이 페이지에서는 Mobile Application이 PII 데이터 수집을 예약별로 보낸 후 프로필 데이터를 생성/업데이트하는 워크플로우를 개발하는 단계에 대해 설명합니다.

* **PII는** &quot;개인 식별 정보&quot;를 의미합니다. 모바일 [관심 영역용 분석과 같은 캠페인 데이터베이스의 프로필 테이블에 표시되지 않는 정보를 포함하여 모든 데이터가 될 수 있습니다](../../integrating/using/about-campaign-points-of-interest-data-integration.md). PII는 일반적으로 마케터와 함께 모바일 앱 개발자가 정의합니다.
* **PII** 수집은 모바일 앱에서 Adobe Campaign Standard의 Rest API에 대한 HTTP POST 작업입니다.

이 사용 사례의 목표는 모바일 응용 프로그램에서 반환되는 PII 데이터에 프로필 관련 데이터가 포함된 경우 Campaign Standard 프로필을 만들거나 업데이트하는 것입니다.

## 사전 요구 사항

모바일 앱 구독 데이터를 기반으로 프로파일을 생성하거나 업데이트하기 전에 Campaign Standard에서 푸시 알림을 활성화하는 데 따라야 하는 몇 가지 구성 단계가 있습니다.

1. [모바일 애플리케이션 만들기](../../administration/using/configuring-a-mobile-application.md)
1. [Adobe Mobile SDK를 모바일 애플리케이션과 통합합니다](https://helpx.adobe.com/kr/campaign/kb/integrate-mobile-sdk.html).
1. [푸시 알림을 전송하도록 Adobe Campaign을 구성합니다](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html).

## 1단계 - 푸시 알림/구독에 대한 프로필 리소스 확장

PII 데이터로 프로필 리소스를 만들거나 업데이트하려면 먼저 원하는 필드로 프로필 리소스를 확장해야 합니다. 방법은 다음과 같습니다.

* 모바일 응용 프로그램에서 보낸 PII 필드를 식별합니다.
* PII 데이터를 프로필 데이터와 연결하기 위해 조정에 사용할 필드를 식별합니다.

![](assets/update_profile1.png)

이 예제에서 **[!UICONTROL Fields]** 섹션은 모바일 응용 프로그램에서 보낸 PII 데이터를 반영합니다. 이 **[!UICONTROL Link to profiles]** 섹션은 PII를 프로필 데이터와 연결하는 데 사용되는 필드를 나타냅니다. 여기서 cusEmail은 **@email** 로 **매핑됩니다**.

리소스를 확장하는 동안 프로필 데이터에 대한 **[!UICONTROL Subscriptions to an Application]** 매핑은 읽기 전용입니다. 그것은 화해를 위해 사용된다. 프로파일을 PII 데이터와 조정하기 위해 필요한 데이터와 함께 프로파일을 시스템에 입력해야 합니다. Adobe의 경우, 조정을 수행하려면 프로필의 이메일 주소가 수집 PII의 이메일과 일치해야 합니다.

* Collect PII는 자신의 이름이 &quot;Jane, Last Name is &quot;Doe&quot;, 이메일 주소가 janedoe@doe.com인 사용자의 모바일 앱에서 수신됩니다.
* 별도로 프로필 데이터가 있어야 합니다(예를 들어, 데이터는 수동으로 입력하거나 다른 리소스에서 이미 입력되어야 함). 여기서 프로필의 이메일 주소는 janedoe@doe.com입니다.

**관련 항목:**

* [구독을 확장해 애플리케이션 리소스로 만들기](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).
* [기존 리소스](../../developing/using/key-steps-to-add-a-resource.md)만들기 또는 확장

## 2단계 - 워크플로우 만들기

관리자는 Campaign Standard의 워크플로우를 사용하여 AppSubscription(가입자) 데이터와 프로필 또는 수신자 데이터 간에 데이터를 고유하게 식별하고 동기화할 수 있습니다. 워크플로우 기반 업데이트는 실시간으로 프로필 데이터를 동기화하지 않지만, 과도한 데이터베이스 잠장이나 오버헤드를 발생시키지 않아야 합니다.

워크플로우를 구축하는 주요 단계는 다음과 같습니다.

1. 최신 구독 목록을 얻으려면 **[!UICONTROL Query]** 또는 **[!UICONTROL Incremental query]** 활동을 사용하십시오.
1. 활동을 사용하여 PII 데이터를 프로필에 매핑합니다. **[!UICONTROL Reconciliation]**
1. 확인 프로세스를 추가합니다.
1. PII 데이터 **[!UICONTROL Update data]** 를 사용하여 프로파일을 업데이트하거나 만듭니다.

이 워크플로우에서는 다음 요구 사항을 가정합니다.

* 확장된 모든/모든 필드는 프로필 테이블을 만들거나 업데이트하는 데 사용할 수 있어야 합니다.
* 프로필 테이블은 기본적으로 지원되지 않는 필드(예: 티셔츠 크기)를 지원하도록 확장될 수 있습니다.
* AppSubscription 테이블의 비어 있는 필드는 프로필 테이블에서 업데이트할 수 없습니다.
* AppSubscription 테이블에서 업데이트된 모든 레코드는 Workflow의 다음 실행에 포함되어야 합니다.

워크플로우를 빌드하려면 다음 활동을 작업 공간으로 드래그하여 놓고 함께 연결합니다. **[!UICONTROL Start]**,, **[!UICONTROL Scheduler]**, **[!UICONTROL Incremental query]**, **[!UICONTROL Update data]**.

![](assets/update_profile0.png)

그런 다음 아래 단계에 따라 각 활동을 구성합니다.

### 활동 **[!UICONTROL Scheduler]** 구성

탭에서 **[!UICONTROL General]** (예: &quot;일별&quot;), **[!UICONTROL Execution frequency]** (예: &quot;1:00:00 AM&quot;) 및 **[!UICONTROL Time]** **[!UICONTROL Start]** (예: 오늘 날짜)를 설정합니다.

![](assets/update_profile2.png)

### 활동을 **[!UICONTROL Incremental query]** 구성합니다.

1. 탭에서 **[!UICONTROL Properties]** 필드의 **[!UICONTROL Select an element]** 아이콘 **[!UICONTROL Resource]** 을 클릭한 다음 **[!UICONTROL Subscriptions to an application (nms:appSubscriptionRcp:appSubscriptionRcpDetail)]** 요소를 선택합니다.

   ![](assets/update_profile3.png)

1. 탭에서 **[!UICONTROL Target]** **[!UICONTROL Mobile application]** 필터를 드래그한 다음 모바일 응용 프로그램 이름을 선택합니다.

   ![](assets/update_profile4.png)

1. 탭에서 **[!UICONTROL Processed data]** 선택한 **[!UICONTROL Use a date field]**&#x200B;다음 **[!UICONTROL Last modified (lastModified)]** 필드를 다른 이름으로 추가합니다 **[!UICONTROL Path to the date field]**.

   ![](assets/update_profile5.png)

### 활동을 **[!UICONTROL Update data]** 구성합니다.

1. 탭 **[!UICONTROL Identification]** 에서 **[!UICONTROL Dimension to update]** 필드가 &quot;프로필(프로필)&quot;으로 설정되어 있는지 확인하고 **[!UICONTROL Create element]** 단추를 클릭하여 필드를 조정 기준으로 추가합니다.

   ![](assets/update_profile_createelement.png)

1. 필드 **[!UICONTROL Source]** 에서 appSubscriptionRcp 테이블의 필드를 조정 필드로 선택합니다. 프로필의 이메일, crmId, marketingCloudId 등이 될 수 있습니다. 이 경우 &quot;이메일(cusEmail)&quot; 필드를 사용합니다.

1. 필드 **[!UICONTROL Destination]** 의 프로필 테이블에서 필드를 선택하여 appSubscriptionRcp 테이블에서 데이터를 조정합니다. 프로필의 이메일이나 crmId, marketingCloudId 등의 확장 필드일 수 있습니다. 이 예에서는 appSubscriptionRcp 테이블의 &quot;이메일(cusEmail)&quot; 필드에 매핑하려면 &quot;이메일(이메일)&quot; 필드를 선택해야 합니다.

   ![](assets/update_profile7.png)

1. 탭에서 **[!UICONTROL Fields to update]** 단추를 **[!UICONTROL Create element]** 클릭한 다음 appSubscriptionRcp 표(**[!UICONTROL Source]** 필드)에서 오는 필드를 프로필 표(**[!UICONTROL Destination]** 필드)에서 업데이트할 필드와 매핑합니다.

1. 필드에 **[!UICONTROL Enabled if]** 표현식을 추가하여 소스 필드에 값이 들어 있는 경우에만 프로필 테이블의 해당 필드가 업데이트되도록 합니다. 이렇게 하려면 목록에서 필드를 선택한 다음 &quot;!=&quot;&quot; 표현식(소스 필드 `[target/@cusEmail]` 가 표현식 편집기에 있는 경우 반드시 입력하십시오 `[target/@cusEmail] != ''"`).

   ![](assets/update_profile8.png)

>[!NOTE]
>
>이 경우 워크플로우는 UPSERT를 수행하지만 데이터를 기반으로 하기 때문에 삽입만 **[!UICONTROL Incremental query]** 수행합니다. 쿼리를 변경하면 삽입되거나 업데이트되는 데이터에 영향을 줄 수 있습니다.
>또한 업데이트할 필드 탭의 설정에 따라 특정 조건에서 삽입되거나 업데이트되는 필드가 결정됩니다. 이러한 설정은 각 응용 프로그램 또는 고객에 대해 고유할 수 있습니다.
>의도하지 않은 결과가 발생할 수 있으므로 이러한 설정을 구성할 때 주의하십시오. appSubscriptionRcp 데이터를 기반으로 프로필의 레코드를 업데이트할 때 유효성 검사 없이 사용자의 개인 정보가 변경될 수 있습니다.

프로필에 삽입/업데이트할 모든 필드가 추가되면 을 클릭합니다 **[!UICONTROL Confirm]**.

![](assets/update_profile9.png)

워크플로우를 저장한 다음 을 클릭하여 워크플로우 **[!UICONTROL Start]** 를 실행합니다.

![](assets/update_profile10.png)
