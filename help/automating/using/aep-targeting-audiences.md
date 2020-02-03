---
title: Adobe Experience Platform 고객 타깃팅
description: 워크플로우 내에서 Adobe Experience PLatform 고객을 타깃팅하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 528d9472-e447-47af-a6b2-3181aa5fb5ad
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 19796aca-6e9e-4d3a-8917-ba660ec7993c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4b18f3b93394101eb569799bcfe362b4daf8f250

---


# Adobe Experience Platform 고객 타깃팅 {#targeting-aep-audiences}

>[!IMPORTANT]
>
>대상 서비스는 현재 베타 버전으로, 예고 없이 빈번한 업데이트가 적용될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

통합 프로필 [세그먼트 빌더를 사용하여 Adobe Experience Platform 대상을](../../audiences/using/aep-about-audience-destinations-service.md) 만든 후에는 워크플로우 내의 캠페인 대상에서와 동일한 방식으로 메시지를 개인화하고 보낼 수 있습니다.

워크플로우에 Adobe Experience Platform 고객을 활성화하려면 다음 단계를 따르십시오.

1. 워크플로우에 **[!UICONTROL Read audience]**활동을 추가한 다음 엽니다.

1. 아래에서 **[!UICONTROL Adobe Experience Platform]**옵션을**[!UICONTROL Type of audience]**&#x200B;선택한 다음 원하는 대상을 추가합니다.

   ![](assets/aep_wkf_readaudience.png)

1. (선택 사항) 대상을 선택하면 눈 단추를 클릭하여 세그먼트 정의를 검토 및/또는 편집할 수 있습니다(변경 사항을 다시 저장했는지 확인).

   눈 모양 단추를 클릭하면 Campaign 내에서 선택한 대상과 연결된 통합 세그먼트 빌더(다른 탭)로 이동합니다.

1. 선택한 Adobe Experience Platform 대상에 대해 원하는 타깃팅 차원을 지정하려면 **[!UICONTROL Platform data mapping]**요소를 선택합니다.

   기본적으로 조정을 위해 사용되는 기본 키(예: 프로필 테이블의 iRecipientID, AppSubscription 테이블의 iAppSubscriptionID)는 드롭다운 목록에서 자동으로 사용할 수 있습니다. 기본 키 외부에서 타깃팅하려면 사용자 지정 네임스페이스를 만들어야 **합니다**.

   >[!NOTE]
   >
   >기본 키 외부의 대상의 경우 사용자 지정 네임스페이스에 해당하는 사용자 지정 대상 매핑을 만들어야 합니다. 타겟 매핑에 대한 자세한 내용은 [이 섹션을](../../administration/using/target-mappings-in-campaign.md)참조하십시오.

   ![](assets/aep_wkf_readaudience_namespace.png)

   이 목록에는 인스턴스에 구성된 모든 XDM(Experience Data Model) 매핑이 포함되어 있습니다. Adobe Experience Platform Data Connector에 대한 자세한 내용은 [이 전용 문서를](../../administration/using/aep-about-data-connector.md)참조하십시오.

   ![](assets/aep_wkf_readaudience_namespace2.png)

1. 대상 및 타깃팅 차원이 제대로 구성되면 **[!UICONTROL Confirm]**단추를 클릭하여 변경 내용을 저장합니다.

이제 다른 활동으로 워크플로우를 구성할 수 있습니다. 예를 들어, 활동을 연결하여 선택한 대상자에게 이메일을 보낼 수 있습니다. **[!UICONTROL Email delivery]**

![](assets/aep_wkf_email.png)

>[!NOTE]
>
>Campaign Standard를 사용하면 모든 전달 채널 내에서 Adobe Experience Platform 고객을 타깃팅할 수 있습니다.이메일, SMS 메시지, DM 메시지, 푸시 알림 및 인앱 메시지
>
>*참고:모든 푸시 및 인앱 메시지의 경우 Campaign Standard는 알려진 프로필에 대해서만 게재를 지원합니다.

워크플로우 및 전달 사용 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [워크플로우 살펴보기](../../automating/using/discovering-workflows.md)
* [워크플로우 구축](../../automating/using/building-a-workflow.md)
* [소통 채널 살펴보기](../../channels/using/discovering-communication-channels.md)
* [채널 활동 기본 정보](../../automating/using/about-channel-activities.md)
