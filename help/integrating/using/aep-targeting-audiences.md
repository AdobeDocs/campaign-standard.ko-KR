---
title: Adobe Experience Platform 대상자 타기팅
description: 워크플로우 내에서 Adobe Experience Platform 대상자를 타깃팅하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: channel-activities
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 11e2cd7e-99b7-45cc-a0c2-41049128fe49
hide: true
hidefromtoc: true
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 3%

---

# Adobe Experience Platform 대상자 타기팅 {#targeting-aep-audiences}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타 버전이며, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

세그먼트 빌더를 사용하여 [Adobe Experience Platform 대상자](../../integrating/using/aep-about-audience-destinations-service.md)를 만든 후에는 워크플로우 내의 Campaign 대상자가 메시지를 개인화하고 전송하는 것과 동일한 방법으로 사용할 수 있습니다.

워크플로우에 Adobe Experience Platform 대상자를 활성화하려면 다음 단계를 수행합니다.

1. 워크플로우에 **[!UICONTROL Read audience]** 활동을 추가한 다음 엽니다.

1. **[!UICONTROL Adobe Experience Platform]**&#x200B;에서 **[!UICONTROL Type of audience]** 옵션을 선택한 다음 원하는 대상을 추가합니다.

   ![](assets/aep_wkf_readaudience.png)

1. (선택 사항) 대상자를 선택하면 눈 모양 단추를 클릭하여 세그먼트 정의를 검토 및/또는 편집할 수 있습니다(변경 사항을 다시 저장해야 함).

   눈 모양 버튼을 클릭하면 Campaign 내에서 선택한 대상자와 연결된 세그먼트 빌더(다른 탭에서)로 바로 이동합니다.

1. 선택한 Adobe Experience Platform 대상에 대해 원하는 타겟팅 차원을 지정하려면 **[!UICONTROL Platform data mapping]** 요소를 선택하십시오.

   기본적으로 조정에 사용되는 기본 키(예: 프로필 테이블의 iRecipientID, AppSubscription 테이블의 iAppSubscriptionID)는 드롭다운 목록에서 자동으로 사용할 수 있습니다. 기본 키 외부를 대상으로 지정하려면 사용자 지정 **네임스페이스**&#x200B;를 만들어야 합니다.

   >[!NOTE]
   >
   >기본 키 외부의 대상에 대해서는 사용자 지정 네임스페이스에 해당하는 사용자 지정 대상 매핑도 만들어야 합니다. 대상 매핑에 대한 자세한 내용은 [이 섹션](../../administration/using/target-mappings-in-campaign.md)을 참조하세요.

   ![](assets/aep_wkf_readaudience_namespace.png)

   이 목록에는 인스턴스에 구성된 모든 XDM(경험 데이터 모델) 매핑이 포함되어 있습니다. Adobe Experience Platform 데이터 커넥터에 대한 자세한 내용은 [이 전용 문서](../../integrating/using/aep-about-data-connector.md)를 참조하세요.

   ![](assets/aep_wkf_readaudience_namespace2.png)

1. 대상 및 타깃팅 차원이 올바르게 구성되면 **[!UICONTROL Confirm]** 단추를 클릭하여 변경 내용을 저장합니다.

이제 다른 활동으로 워크플로우를 구성할 수 있습니다. 예를 들어 **[!UICONTROL Email delivery]** 활동을 연결하여 선택한 대상자에게 이메일을 보낼 수 있습니다.

![](assets/aep_wkf_email.png)

>[!NOTE]
>
>Campaign Standard을 사용하면 이메일, SMS 메시지, DM 메시지, 푸시 알림 및 인앱 메시지와 같은 모든 전달 채널 내에서 Adobe Experience Platform 대상을 타깃팅할 수 있습니다.
>
>*참고: 모든 푸시 및 인앱 메시지에 대해 Campaign Standard은 알려진 프로필에 대한 게재만 지원합니다.

워크플로우 및 게재 사용 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [워크플로우 살펴보기](../../automating/using/get-started-workflows.md)
* [워크플로 작성](../../automating/using/building-a-workflow.md)
* [통신 채널 살펴보기](../../channels/using/get-started-communication-channels.md)
* [채널 활동 기본 정보](../../automating/using/about-channel-activities.md)
