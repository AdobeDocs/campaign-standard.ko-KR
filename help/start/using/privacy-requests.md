---
title: 개인 정보 보호 요청
description: Adobe Campaign Standard의 개인 정보 보호 요청을 관리하는 방법 알아보기
audience: start
content-type: reference
topic-tags: discovering-the-interface
feature: Privacy
role: User
level: Intermediate
exl-id: b30f1395-965b-4709-ba4b-8cf6b010ef0b
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 98%

---

# 개인 정보 보호 요청 관리 {#privacy-requests}

개인 정보 관리에 대한 일반 프레젠테이션은 [이 섹션](../../start/using/privacy-management.md)을 참조하십시오.

이 정보는 GDPR, CPA, PDPA 및 LGPD에 적용됩니다. 이러한 규정에 대한 자세한 내용은 [이 섹션](../../start/using/privacy-management.md#privacy-management-regulations)을 참조하십시오.

CPA에만 해당되는 개인 정보 판매 옵트아웃은 [이 섹션](#sale-of-personal-information-ccpa)에 설명되어 있습니다.

<!--Starting 19.4, the use of the Campaign API and interface for Access and Delete requests is deprecated. For any GDPR, CCPA, PDPA, or LGPD Access and Delete requests, you need to use the [Privacy Core Service](#create-privacy-request) integration method.-->

## 개인 정보 보호 요청 정보 {#about-privacy-requests}

Adobe Campaign을 사용하면 개인 정보 보호 준비를 용이하게 하기 위해 액세스 및 삭제 요청을 처리할 수 있습니다. **액세스 권한** 및 **잊혀질 권리(삭제 요청)**&#x200B;는 [이 섹션](../../start/using/privacy-management.md#right-access-forgotten)에 설명되어 있습니다.

이러한 요청을 수행하려면 **개인 정보 보호 핵심 서비스** 통합을 사용해야 합니다. 개인 정보 보호 핵심 서비스에서 모든 Experience Cloud 솔루션으로 푸시된 개인 정보 보호 요청은 전용 워크플로를 통해 Campaign에서 자동으로 처리됩니다.

### 기본 사항 {#prerequesites}

Adobe Campaign은 저장된 데이터에 대한 개인 정보 요청을 만들고 처리할 수 있는 데이터 컨트롤러 도구를 제공합니다. 하지만 데이터 주체(이메일, 고객 지원 센터 또는 웹 포털)와의 관계를 처리하는 것은 데이터 컨트롤러의 책임입니다.

따라서 요청을 하는 데이터 주체의 ID를 확인하고 요청자에게 반환되는 데이터가 데이터 주체의 정보임을 확인하는 것은 데이터 컨트롤러로서의 책임입니다.

>[!NOTE]
>
>개인 데이터 및 데이터를 관리하는 다른 엔터티(데이터 컨트롤러, 데이터 프로세서 및 데이터 주체)에 대한 자세한 내용은 [개인 데이터 및 가상 사용자를 참조하십시오](../../start/using/privacy.md#personal-data).

### 네임스페이스 {#namesspaces}

개인 정보 요청을 만들기 전에 사용할 네임스페이스를 정의해야 합니다. 네임스페이스는 Adobe Campaign 데이터베이스에서 데이터 주체를 식별하는 데 사용되는 키입니다. 기본 제공되는 두개의 네임스페이스는 이메일 및 모바일 폰입니다. 다른 네임스페이스(예: 프로필 사용자 지정 필드)가 필요한 경우 다음 단계를 따르십시오.

또한 네임스페이스를 만드는 방법을 다루는 이 [튜토리얼](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/namespaces-for-privacy-requests.html?lang=ko#privacy)을 참조하십시오.

>[!NOTE]
>
>여러 네임스페이스를 사용하는 경우 네임스페이스당 개인 정보 요청을 하나씩 만듭니다.

1. 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭한 다음 **[!UICONTROL Administration]** > **[!UICONTROL Namespaces]**&#x200B;를 선택합니다.

   ![](assets/privacy-namespaces.png)

1. 네임스페이스 목록에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   ![](assets/privacy-namespace-create.png)

1. **[!UICONTROL Label]**&#x200B;을(를) 입력합니다.

   ![](assets/privacy-namespace-label.png)

1. 기존 ID 서비스 네임스페이스를 사용하려면 **[!UICONTROL Identity Service Namespaces]** 목록에서 **[!UICONTROL Map from Identity Namespace Service]**&#x200B;을(를) 선택하고 네임스페이스를 선택합니다.

   ![](assets/privacy-map-from-namespace.png)

   **[!UICONTROL Identity Service]**&#x200B;에서 새 네임스페이스를 만들어 Campaign에 매핑하려면 **[!UICONTROL Create new]**&#x200B;을(를) 선택하고 **[!UICONTROL Identity namespace name]** 필드에 이름을 입력합니다.

   ![](assets/privacy-create-new-namespace.png)

   ID 네임스페이스에 대한 자세한 내용은 [Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=ko) 설명서를 참조하십시오.

1. 하나의 ID 서비스 네임스페이스가 Campaign의 한 네임스페이스에 매핑됩니다. Campaign에서 네임스페이스를 조정할 방식을 지정해야 합니다.

   대상 매핑(**[!UICONTROL Recipients]** **[!UICONTROL Real-time event]** 또는 **[!UICONTROL Subscriptions to an application]**)을 선택합니다. 여러 대상 매핑을 사용하려면 대상 매핑당 네임스페이스를 하나씩 만듭니다.

   ![](assets/privacy-namespace-target-mapping.png)

1. **[!UICONTROL Reconciliation key]**&#x200B;을(를) 선택합니다. 이 필드는 Adobe Campaign 데이터베이스의 데이터 주체를 식별하는 데 사용됩니다.

   ![](assets/privacy-namespace-reconciliation-key.png)

1. **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다. 이제 새 네임스페이스에 따라 개인 정보 보호 요청을 만들 수 있습니다. 여러 네임스페이스를 사용하는 경우 네임스페이스당 개인 정보 요청을 하나씩 만듭니다.

### 개인 정보 보호 요청 만들기 {#create-privacy-request}

<!--Starting 19.4, the use of the Campaign API and interface for Access and Delete requests is deprecated. Use the **Privacy Core Service** for any GDPR, CCPA, PDPA, or LGPD Access and Delete requests.-->

개인 정보 보호 핵심 서비스 통합을 사용하면 단일 JSON API 호출을 통해 다중 솔루션 컨텍스트에서 개인 정보 보호 요청을 자동화할 수 있습니다. 개인 정보 보호 핵심 서비스에서 모든 Experience Cloud 솔루션으로 푸시된 개인 정보 보호 요청은 전용 워크플로를 통해 Campaign에서 자동으로 처리됩니다.

개인 정보 보호 핵심 서비스에서 개인 정보 보호 요청을 만드는 방법에 대해 알아보려면 [Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko) 설명서를 참조하십시오.

>[!IMPORTANT]
>
>사용자 지정 네임스페이스 유형을 사용하여 요청을 제출하려면 [JSON 메서드](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko#json){target="_blank"}를 활용하고 요청에 namespaceId를 추가하거나 [API 호출](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=ko#access-delete){target="_blank"}을(를) 사용하여 요청하십시오.
>
>표준 네임스페이스 유형을 사용하여 요청을 제출할 때는 [개인 정보 사용자 인터페이스](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko#request-builder){target="_blank"}만 사용할 수 있습니다.

각 개인 정보 보호 핵심 서비스 작업은 사용 중인 네임스페이스의 수를 기준으로 Campaign에서 여러 개인 정보 보호 요청으로 분할되며, 하나의 요청은 하나의 네임스페이스에 해당합니다. 또한 하나의 작업은 여러 인스턴스에 대해 실행할 수 있습니다. 따라서 하나의 작업에 대해 여러 파일이 만들어집니다. 예를 들어, 요청에 두 개의 네임스페이스가 있고 세 개의 인스턴스에서 실행 중인 경우 총 6개의 파일이 전송됩니다. 네임스페이스 및 인스턴스당 하나의 파일입니다.

파일 이름의 패턴은 `<InstanceName>-<NamespaceId>-<ReconciliationKey>.xml` 입니다.

* **InstanceName**: 캠페인 인스턴스 이름
* **NamespaceId**: 사용된 네임스페이스의 ID 서비스 네임스페이스 ID
* **조정 키**: 인코딩 조정 키

### 리소스 목록 {#list-of-resources}

Adobe Campaign은 개인 정보 보호 요청의 삭제 또는 액세스를 수행할 때 프로필 리소스(고유 유형)에 대한 링크가 있는 모든 리소스의 **조정** 값을 기준으로 모든 데이터 주체의 데이터를 검색합니다.

다음은 개인 정보 요청을 수행할 때 고려할 수 있는 기본 제공 리소스 목록입니다.

* 프로필(수신자)
* 프로필 게재 로그(broadLogRcp)
* 프로필 추적 로그(trackingLogRcp)
* 게재 로그(애플리케이션에 대한 구독)(broadLogAppSubRcp)
* 추적 로그(애플리케이션에 대한 구독)(trackingLogAppSubRcp)
* 애플리케이션에 대한 구독(appSubscriptionRcp)
* 프로필 구독 내역(subHistoRcp)
* 프로필 구독(subscriptionRcp)
* 방문자(방문자)

프로필 리소스(고유 유형)에 대한 링크가 있는 사용자 지정 리소스를 만든 경우 이러한 리소스도 고려됩니다. 예를 들어 프로필 리소스와 연결된 트랜잭션 리소스와 트랜잭션 리소스에 연결된 트랜잭션 세부 정보가 있는 경우 이 두 가지 모두 고려됩니다.

사용자 지정 리소스를 수정하는 방법에 대한 [이 튜토리얼](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/custom-resources-for-privacy-requests.html?lang=ko#privacy)을 참조하십시오.

이를 위해서는 사용자 지정 리소스에서 **[!UICONTROL Deleting the target record implies deleting records referenced by the link]** 옵션을 선택해야 합니다.

1. 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭한 다음 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom resources]**&#x200B;를 선택합니다.

1. 프로필 리소스(고유 유형)에 대한 링크가 있는 사용자 지정 리소스를 선택합니다.

1. **[!UICONTROL Links]** 섹션을 클릭합니다.

1. 각 링크에 대해 연필 아이콘(**[!UICONTROL Edit properties]**)을 클릭합니다.

1. **[!UICONTROL Behavior if deleted/duplicated]** 섹션에서 **[!UICONTROL Deleting the target record implies deleting records referenced by the link]** 옵션을 선택합니다.

   ![](assets/privacy-cus-resource-option.png)

### 개인 정보 보호 요청 상태 {#privacy-request-statuses}

개인정보 보호 요청에 대한 다양한 상태는 다음과 같습니다.

* **[!UICONTROL New]** / **[!UICONTROL Retry pending]**: 진행 중이며 워크플로는 아직 요청을 처리하지 않았습니다.
* **[!UICONTROL Processing]** / **[!UICONTROL Retry in progress]**: 워크플로가 요청을 처리하고 있습니다.
* **[!UICONTROL Delete pending]**: 워크플로는 삭제하려는 모든 수신자 데이터를 식별했습니다.
* **[!UICONTROL Delete in progress]**: 워크플로가 삭제를 처리하고 있습니다.
  <!--**[!UICONTROL Delete Confirmation Pending]** (Delete request in 2-steps process mode): the workflow has processed the Access request. Manual confirmation is requested to perform the deletion. The button is available for 15 days.-->
* **[!UICONTROL Complete]**: 요청 처리가 오류 없이 끝났습니다.
* **[!UICONTROL Error]**: 워크플로에서 오류가 발생했습니다. 이유는 **[!UICONTROL Request status]** 열의 개인 정보 보호 요청 목록에 표시됩니다. 예를 들어 **[!UICONTROL Error data not found]**&#x200B;은(는) 데이터 주체의 **[!UICONTROL Reconciliation value]**&#x200B;와(과) 일치하는 수신자 데이터가 데이터베이스에 없음을 의미합니다.

<!--### Disabling the 2-step process {#disabling-two-step-process}

The Core Privacy Service does not support the 2-step process.

>[!IMPORTANT]
>
>Before using the Core Privacy Service integration to manage your Privacy requests, you must disable the 2-step process for Delete requests from the Campaign Standard interface.

If this option is not disabled, all Delete requests managed with the Privacy Core Service will remain in pending state and will not complete.

By default, the 2-step process is activated.

To change this mode, click **[!UICONTROL Edit properties]**, in the top right corner of the **[!UICONTROL Privacy Requests]** screen, then uncheck the **[!UICONTROL Activate the 2-step process]** option.

![](assets/privacy-disable-2-step-process.png)-->

## 개인 정보 판매 옵트아웃(CCPA) {#sale-of-personal-information-ccpa}

**CCPA**(California Consumer Privacy Act)는 캘리포니아 거주자들에게 개인 정보에 대한 새로운 권리를 제공하고 캘리포니아에서 비즈니스를 수행하는 특정 엔터티에 데이터 보호 책임을 부과합니다.

액세스 및 삭제 요청의 구성 및 사용은 GDPR과 CCPA와 공통됩니다. 이 섹션에서는 CCPA에만 해당되는 개인 데이터 판매에 대한 옵트아웃을 제공합니다.

Adobe Campaign이 제공하는 [동의 관리](../../start/using/privacy-management.md#consent-management) 도구 외에도 소비자가 개인 정보 판매를 옵트아웃했는지 여부를 추적할 수 있습니다.

사용자가 시스템을 통해 자신의 개인 정보를 서드파티에 판매하는 것을 허용하지 않기로 결정하면 이 정보를 저장하고 추적할 수 있습니다.

>[!NOTE]
>
>Campaign 인터페이스와 API를 통해 개인 정보 판매에 대한 옵트아웃을 활용할 수 있습니다. 개인 정보 보호 핵심 서비스를 통해 사용할 수 없습니다.

>[!IMPORTANT]
>
>데이터 주체의 요청을 받고 CCPA에 대한 요청 날짜를 추적하는 것은 데이터 컨트롤러로서의 책임입니다. 기술 제공업체에서는 수신 거부 방법만 제공합니다. 데이터 컨트롤러로서의 역할에 대한 자세한 내용은 [개인 데이터 및 가상 사용자를 참조하십시오](../../start/using/privacy.md#personal-data).

### 사용자 지정 테이블에 대한 사전 요구 사항 {#ccpa-prerequisite}

**[!UICONTROL CCPA Opt-Out]** 필드는 Campaign 인터페이스 및 API에서 기본적으로 제공됩니다. 기본적으로 이 필드는 표준 **[!UICONTROL Profile]** 리소스에 대해 사용할 수 있습니다.

사용자 지정 프로필 리소스를 사용하는 경우 리소스를 확장하고 필드를 추가해야 합니다. **[!UICONTROL Opt-Out for CCPA]** Optopcpa와 같이 기본적으로 제공되는 필드가 아닌 다른 이름을 사용하는 것이 좋습니다. 새 필드를 만들면 Campaign API에서 자동으로 지원됩니다.

프로필 리소스 확장 방법에 대한 자세한 내용은 [이 섹션](../../developing/using/extending-the-profile-resource-with-a-new-field.md)을 참조하십시오.

>[!NOTE]
>
>리소스 수정은 전문가 사용자만 수행해야 하는 중요한 작업입니다.

1. **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]**(으)로 이동합니다. 사용자 지정 프로필 리소스를 클릭합니다. 리소스 확장에 대한 자세한 내용은 [이 섹션](../../developing/using/creating-or-extending-the-resource.md)을 참조하십시오.

   ![](assets/privacy-ccpa-extend-cus.png)

1. **[!UICONTROL Add field]** 또는 **[!UICONTROL Create Element]**&#x200B;을(를) 클릭하거나 레이블, ID를 추가하고 **[!UICONTROL Boolean]** 유형을 선택합니다. 이름은 **CCPA용 옵트아웃**&#x200B;을 사용합니다. ID는 **optOutCcpa**&#x200B;를 사용합니다. 

   ![](assets/privacy-ccpa-extend-field.png)

1. **[!UICONTROL Screen definition]** 탭의 **[!UICONTROL Detail screen configuration]** 아래에서 필드를 추가하고 **[!UICONTROL Input field]**&#x200B;을(를) 선택합니다 . 그러면 프로필 목록 및 세부 정보에 있는 필드를 사용할 수 있습니다.  화면 정의 구성에 대한 자세한 내용은 [이 섹션](../../developing/using/configuring-the-screen-definition.md)을 참조하십시오.

   ![](assets/privacy-ccpa-extend-screen.png)

1. **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publishing]**(으)로 이동하여 게시를 준비하고 수정 내용을 게시합니다. 리소스 게시에 대한 자세한 내용은 [이 섹션](../../developing/using/updating-the-database-structure.md)을 참조하십시오.

   ![](assets/privacy-ccpa-extend-pub.png)

1. 프로필 세부 정보에 필드를 사용할 수 있는지 확인합니다. 자세한 내용은 [이 섹션](#usage)을 참조하십시오.

### 사용 {#usage}

필드의 값을 채우고 데이터 판매에 관한 CCPA 지침 및 규칙을 따르는 것은 데이터 컨트롤러의 책임입니다.

값을 채우려면 다음과 같은 몇 가지 방법을 사용할 수 있습니다.

* 수신자의 세부 사항을 편집하여 Campaign 인터페이스 사용(아래 참조)
* Campaign 개인 정보 API 사용( [API 설명서](../../api/using/managing-ccpa-opt-out.md) 참조)
* 데이터 가져오기 워크플로를 통해

그런 다음 옵트아웃한 프로필의 개인 정보를 제3자에게 판매해서는 안 됩니다.

1. Campaign 인터페이스에서 옵트아웃 상태를 변경하려면 프로필을 편집합니다.

   ![](assets/privacy-ccpa-profile-opt-out.png)

1. 필드의 값이 **[!UICONTROL True]**(이)면 프로필 세부 사항에 정보가 표시됩니다.

   ![](assets/privacy-ccpa-profile-opt-out-true.png)

1. 프로필 목록이 옵트아웃 열을 표시하도록 구성할 수 있습니다. 목록 구성 방법을 알려면 [이 섹션](../../start/using/customizing-lists.md)을 참조하십시오.

   ![](assets/privacy-ccpa-profile-configure-list.png)

1. 이 열을 클릭하여 옵트아웃 정보에 따라 수신자를 정렬할 수 있습니다.

   ![](assets/privacy-ccpa-profile-sorting.png)
