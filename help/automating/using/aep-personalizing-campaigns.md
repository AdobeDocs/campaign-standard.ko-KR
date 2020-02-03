---
title: Adobe Experience Platform 속성을 사용하여 캠페인 개인화
description: Adobe Experience Platform 속성을 사용하여 캠페인을 개인화하는 방법을 살펴볼 수 있습니다.
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
source-git-commit: 2086bbb6fa87106692b3f3744c40ecf40e66caf3

---


# Adobe Experience Platform 속성을 사용하여 캠페인 개인화 {#personalizing-campaigns-using-aep-attributes}

>[!IMPORTANT]
>
>대상 서비스는 현재 베타 버전으로, 예고 없이 빈번한 업데이트가 적용될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.
>
>**푸시** 및 **인앱** 채널은 Adobe Experience Platform의 컨텍스트 데이터를 사용하여 개인화할 수 없습니다.

워크플로우가 Adobe Experience [Platform 대상으로](../../audiences/using/aep-about-audience-destinations-service.md)구성되면 XDM(Experience Data Model)에만 존재하는 프로필 속성을 사용하여 메시지를 개인화할 수 있습니다.

이렇게 하려면 다음 속성을 **[!UICONTROL Read audience]**활동에 추가해야 합니다.

1. 활동을 **[!UICONTROL Read audience]**엽니다. 탭에서**[!UICONTROL Additional data]** **[!UICONTROL Create element]**단추를 클릭합니다.

   >[!NOTE]
   >
   >이 **[!UICONTROL Additional data]**탭은 Adobe Experience Platform 대상을 선택한 후에만 사용할 수 있습니다.

   ![](assets/aep_wkf_readaudience_attributes.png)

1. 목록에서 원하는 XDM 필드를 선택한 다음 을 **[!UICONTROL Confirm]**클릭합니다.

   ![](assets/aep_wkf_readaudience_perso1.png)

1. 단추를 클릭하여 추가 데이터 목록에 추가합니다. **[!UICONTROL Add]**

   ![](assets/aep_wkf_readaudience_perso3.png)

1. 워크플로우에 추가할 모든 XDM 필드에 대해 이 단계를 반복합니다.

   >[!NOTE]
   >
   >한 **[!UICONTROL Read audience]**활동에 최대 20개의 XDM 필드를 추가할 수 있습니다.

1. 모든 필드가 추가되면 **[!UICONTROL Confirm]**단추를 클릭하여 변경 내용을 저장합니다. 이제 배송을 개인화할 수 있습니다.

게재를 만들고 개인화하는 방법에 대한 자세한 내용은 Campaign Standard 설명서를 참조하십시오.

* [소통 채널 살펴보기](../../channels/using/discovering-communication-channels.md)
* [채널 활동 기본 정보](../../automating/using/about-channel-activities.md)
* [배달 개인화](../../designing/using/personalization.md)
