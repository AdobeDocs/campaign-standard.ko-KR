---
title: 모바일 애플리케이션 데이터를 기반으로 프로필 정보 만들고 업데이트하기
description: 모바일 애플리케이션 데이터를 기반으로 프로필 정보를 만들고 업데이트하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: delivery,mobileAppContent,back
feature: Push
role: User
level: Intermediate
exl-id: 1b48456e-9aae-485c-a7c4-7e3e2f53cbca
source-git-commit: b5e98c07ee55cab0b6a628a97162ccd64711501a
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 3%

---

# 모바일 애플리케이션 데이터를 기반으로 프로필 정보 만들고 업데이트하기

## 개요

이 페이지에서는 Mobile Application이 Collect PII 데이터를 예약된 대로 보낸 후 프로필 데이터를 생성/업데이트하는 워크플로우를 개발하는 단계에 대해 설명합니다.

* **** PII는 &quot;개인 식별 정보&quot;를 의미합니다. Campaign 데이터베이스의 프로필 테이블에 표시되지 않는 정보(예: 모바일용 Analytics [관심 영역](../../integrating/using/about-campaign-points-of-interest-data-integration.md))를 포함한 모든 데이터가 될 수 있습니다. PII는 일반적으로 마케터가 사용하는 모바일 앱 개발자가 정의합니다.
* **Collect** PII는 모바일 앱에서 Adobe Campaign Standard의 Rest API에 대한 HTTP POST 작업입니다.

이 사용 사례의 목표는 모바일 애플리케이션에서 반환한 PII 데이터에 프로필 관련 데이터가 포함된 경우 Campaign Standard 프로필을 만들거나 업데이트하는 것입니다.

## 필수 구성 요소

모바일 앱 구독 데이터를 기반으로 프로필을 만들거나 업데이트하기 전에 Campaign Standard에서 푸시 알림을 활성화하기 위해 따라야 할 구성 단계가 있습니다.

1. [모바일 애플리케이션 만들기](../../administration/using/configuring-a-mobile-application.md)
1. [모바일 애플리케이션과 Adobe Mobile SDK를 통합합니다](../../administration/using/supported-mobile-use-cases.md).
1. [푸시 알림을 전송하도록 Adobe Campaign을 구성합니다](../../administration/using/configuring-a-mobile-application.md).

## 1단계 - 푸시 알림/구독에 대한 프로필 리소스 확장

PII 데이터로 프로필 리소스를 만들거나 업데이트하려면 먼저 원하는 필드로 프로필 리소스를 확장해야 합니다. 방법은 다음과 같습니다.

* 모바일 애플리케이션에서 전송하는 PII 필드를 식별합니다.
* 조정을 위해 사용할 필드를 식별하여 PII 데이터를 프로필 데이터와 연결합니다.

![](assets/update_profile1.png)

이 예에서 **[!UICONTROL Fields]** 섹션은 모바일 애플리케이션에서 보낸 PII 데이터를 반영합니다. **[!UICONTROL Link to profiles]** 섹션은 PII를 프로필 데이터와 연결하는 데 사용되는 필드를 나타냅니다. 여기서 **cusEmail**&#x200B;은 **@email**&#x200B;에 매핑됩니다.

**[!UICONTROL Subscriptions to an Application]** 리소스를 확장하는 동안 프로필 데이터에 대한 매핑은 읽기 전용입니다. 조정에 사용됩니다. 프로필을 PII 데이터와 조정하기 위해 필요한 데이터로 시스템에 프로필을 입력해야 합니다. 이 경우 조정을 수행하려면 프로필의 이메일 주소가 수집 PII의 이메일과 일치해야 합니다.

* Collect PII는 모바일 앱에서 수신되며, 여기서 First Name은 &quot;Jane, Last Name is &quot;Doe&quot;, Email address는 janedoe@doe.com입니다.
* 별도로 프로필 데이터가 있어야 합니다(예: 데이터를 수동으로 입력하거나 다른 리소스에서 이미 입력해야 함). 여기서 프로필의 이메일 주소는 janedoe@doe.com입니다.

**관련 항목:**

* [구독을 확장해 애플리케이션 리소스로 만들기](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).
* [기존 리소스 만들기 또는 확장](../../developing/using/key-steps-to-add-a-resource.md).

## 2단계 - 워크플로우 만들기

관리자는 Campaign Standard의 워크플로우를 사용하여 AppSubscription(가입자) 데이터와 프로필 또는 수신자 데이터 간에 데이터를 고유하게 식별하고 동기화할 수 있습니다. 워크플로우 기반 업데이트는 프로필 데이터를 실시간으로 동기화하지 않지만, 이로 인해 과도한 데이터베이스 잠금 또는 오버헤드가 발생하지 않습니다.

워크플로우를 빌드하는 주요 단계는 다음과 같습니다.

1. **[!UICONTROL Query]** 또는 **[!UICONTROL Incremental query]** 활동을 사용하여 최신 구독 목록을 가져옵니다.
1. **[!UICONTROL Reconciliation]** 활동을 사용하여 PII 데이터를 프로필에 매핑합니다.
1. 확인 프로세스를 추가합니다.
1. **[!UICONTROL Update data]** 을 사용하여 PII 데이터로 프로필을 업데이트하거나 만듭니다.

이 워크플로우에서는 다음 요구 사항을 가정합니다.

* 확장된 모든/모든 필드는 프로필 테이블을 만들거나 업데이트하는 데 사용할 수 있어야 합니다.
* 프로필 테이블은 기본적으로 지원되지 않는 필드(예: 티셔츠 크기)를 지원하도록 확장할 수 있습니다.
* AppSubscription 테이블의 필드가 비어 있으면 프로필 테이블에서 업데이트할 수 없습니다.
* AppSubscription 테이블에서 업데이트된 모든 레코드는 워크플로우의 다음 실행에 포함되어야 합니다.

워크플로우를 빌드하려면 다음 활동을 작업 공간에 끌어다 놓고 함께 연결합니다. **[!UICONTROL Start]**, **[!UICONTROL Scheduler]**, **[!UICONTROL Incremental query]**, **[!UICONTROL Update data]**.

![](assets/update_profile0.png)

그런 다음 아래 절차에 따라 각 활동을 구성하십시오.

### **[!UICONTROL Scheduler]** 활동 구성

**[!UICONTROL General]** 탭에서 **[!UICONTROL Execution frequency]**(예: &quot;Daily&quot;), **[!UICONTROL Time]**(예: &quot;1:00:00 AM&quot;) 및 **[!UICONTROL Start]**(예: 오늘 날짜)를 설정합니다.

![](assets/update_profile2.png)

### **[!UICONTROL Incremental query]** 활동을 구성합니다.

1. **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Resource]** 필드의 **[!UICONTROL Select an element]** 아이콘을 클릭한 다음 **[!UICONTROL Subscriptions to an application (nms:appSubscriptionRcp:appSubscriptionRcpDetail)]** 요소를 선택합니다.

   ![](assets/update_profile3.png)

1. **[!UICONTROL Target]** 탭에서 **[!UICONTROL Mobile application]** 필터를 드래그한 다음 모바일 애플리케이션 이름을 선택합니다.

   ![](assets/update_profile4.png)

1. **[!UICONTROL Processed data]** 탭에서 **[!UICONTROL Use a date field]** 을 선택한 다음 **[!UICONTROL Last modified (lastModified)]** 필드를 **[!UICONTROL Path to the date field]** (으)로 추가합니다.

   ![](assets/update_profile5.png)

### **[!UICONTROL Update data]** 활동을 구성합니다.

1. **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Dimension to update]** 필드가 &quot;프로필(프로필)&quot;로 설정되어 있는지 확인한 다음 **[!UICONTROL Create element]** 단추를 클릭하여 필드를 조정 기준으로 추가합니다.

   ![](assets/update_profile_createelement.png)

1. **[!UICONTROL Source]** 필드에서 appSubscriptionRcp 테이블의 필드를 조정 필드로 선택합니다. 프로필의 이메일, crmId, marketingCloudId 등이 될 수 있습니다. 이 예제에서는 &quot;Email (cusEmail)&quot; 필드를 사용합니다.

1. **[!UICONTROL Destination]** 필드의 프로필 테이블에서 필드를 선택하여 appSubscriptionRcp 테이블에서 데이터를 조정합니다. 프로필의 이메일 또는 crmId, marketingCloudId 등의 확장 필드일 수 있습니다. 이 예제에서는 &quot;이메일(이메일)&quot; 필드를 선택하여 appSubscriptionRcp 테이블의 &quot;Email (cusEmail)&quot; 필드에 매핑해야 합니다.

   ![](assets/update_profile7.png)

1. **[!UICONTROL Fields to update]** 탭에서 **[!UICONTROL Create element]** 단추를 클릭한 다음 appSubscriptionRcp 테이블(**[!UICONTROL Source]** 필드)에서 나오는 필드를 프로필 테이블(**[!UICONTROL Destination]** 필드)에서 업데이트할 필드에 매핑합니다.

1. **[!UICONTROL Enabled if]** 필드에서 표현식을 추가하여 소스 필드에 값이 있는 경우에만 프로필 테이블의 해당 필드가 업데이트되도록 합니다. 이렇게 하려면 목록에서 필드를 선택한 다음 &quot;!=&quot;&quot; 표현식(표현식 편집기의 소스 필드가 `[target/@cusEmail]`인 경우 `[target/@cusEmail] != ''"` 을 입력해야 합니다.)

   ![](assets/update_profile8.png)

>[!NOTE]
>
>이 경우 Workflow는 UPSERT를 수행하지만 **[!UICONTROL Incremental query]** 데이터를 기반으로 하므로 삽입만 됩니다. 쿼리를 변경하면 삽입되거나 업데이트되는 데이터에 영향을 줄 수 있습니다.
>또한 업데이트할 필드 탭의 설정에 따라 특정 조건에서 삽입되거나 업데이트되는 필드가 결정됩니다. 이러한 설정은 각 애플리케이션 또는 고객에 대해 고유해야 합니다.
>appSubscriptionRcp 데이터를 기반으로 프로필에서 레코드를 업데이트하면 유효성 검사 없이 개인 정보가 변경될 수 있으므로, 의도하지 않은 결과가 발생할 수 있으므로, 이러한 설정을 구성할 때 주의하십시오.

프로필에 삽입/업데이트할 모든 필드가 추가되면 **[!UICONTROL Confirm]** 을 클릭합니다.

![](assets/update_profile9.png)

워크플로우를 저장한 다음 **[!UICONTROL Start]** 을 클릭하여 워크플로우를 실행합니다.

![](assets/update_profile10.png)
