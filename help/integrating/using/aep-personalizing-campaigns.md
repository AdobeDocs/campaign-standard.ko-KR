---
title: Adobe Experience Platform 특성을 사용한 캠페인 개인화
description: Experience Platform 속성을 사용하여 캠페인을 개인화하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: channel-activities
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 4d4e7e58-e161-4e5a-898a-b5c29ffb20e0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 8%

---

# Adobe Experience Platform 특성을 사용한 캠페인 개인화 {#personalizing-campaigns-using-aep-attributes}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타에 있으며, 예고 없이 자주 업데이트될 수 있습니다. 고객은 이러한 기능에 액세스하려면 Azure에서 호스팅(현재 북미 전용 베타 버전)해야 합니다. 액세스하려면 고객 지원 센터에 문의하십시오.
>
>**푸시** 및 **인앱** Adobe Experience Platform의 컨텍스트 데이터를 사용하여 개인화에 아직 채널을 사용할 수 없습니다.

워크플로우가 [Adobe Experience Platform 대상](../../integrating/using/aep-about-audience-destinations-service.md), XDM(Experience Data Model)에만 있는 프로필 속성을 사용하여 메시지를 개인화할 수 있습니다.

이를 수행하려면 다음 속성을 **[!UICONTROL Read audience]** 활동:

1. 를 엽니다. **[!UICONTROL Read audience]** 활동. 에서 **[!UICONTROL Additional data]** 탭에서 **[!UICONTROL Create element]** 버튼을 클릭합니다.

   다음 사항에 유의하십시오. **[!UICONTROL Additional data]** 탭은 Adobe Experience Platform 대상자를 선택한 후에만 사용할 수 있습니다.

   ![](assets/aep_wkf_readaudience_attributes.png)

   >[!NOTE]
   >
   >배열 및 맵 데이터 유형은 이 기능에서 지원되지 않습니다. 또한 결합 스키마의 데이터만 선택기에 표시됩니다.

1. 목록에서 원하는 XDM 필드를 선택한 다음 를 클릭합니다 **[!UICONTROL Confirm]**.

   ![](assets/aep_wkf_readaudience_perso1.png)

1. 을(를) 클릭합니다. **[!UICONTROL Add]** 추가 데이터 목록에 추가하는 단추.

   ![](assets/aep_wkf_readaudience_perso3.png)

1. 워크플로우에 추가할 모든 XDM 필드에 대해 이 단계를 반복합니다.

   >[!NOTE]
   >
   >에는 최대 20개의 XDM 필드를 추가할 수 있습니다 **[!UICONTROL Read audience]** 활동.

1. 모든 필드가 추가되면 **[!UICONTROL Confirm]** 단추를 클릭하여 변경 사항을 저장합니다. 이제 게재를 개인화할 수 있습니다.

게재를 만들고 개인화하는 방법에 대한 자세한 내용은 Campaign Standard 설명서를 참조하십시오.

* [통신 채널 살펴보기](../../channels/using/get-started-communication-channels.md)
* [채널 활동 기본 정보](../../automating/using/about-channel-activities.md)
* [게재 개인화](../../designing/using/personalization.md)
