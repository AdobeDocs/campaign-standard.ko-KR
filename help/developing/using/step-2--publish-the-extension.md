---
solution: Campaign Standard
product: campaign
title: '"2단계: 확장 게시"'
description: Campaign Standard에서 확장을 게시하는 방법을 알아봅니다. 시리즈의 2부.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
feature: 데이터 모델
role: Developer
level: Experienced
exl-id: e3bebded-764c-4d2e-9580-c413f1576a2c
source-git-commit: d3482dfad245807aedee6deb36fd67e43c7a66b9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 23%

---

# 2단계: 확장 게시{#step-publish-the-extension}

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Development]** 다음 **[!UICONTROL Publication]**&#x200B;을 선택합니다.
1. **[!UICONTROL Prepare Publication]** 버튼을 클릭합니다.
1. **[!UICONTROL Create the Profiles & Services Ext API]** 옵션을 선택합니다.

   ![](assets/create-profile-and-services-api.png)

   >[!NOTE]
   >
   >API가 이미 게시되어 있는 경우(이 리소스 또는 다른 리소스에 대해 이 옵션을 이미 한 번 선택한 경우) API 업데이트가 강제로 수행됩니다.

1. **[!UICONTROL Profiles & Services API Preview]** 탭을 클릭합니다.

   그러면 API 게시가 현재 버전의 profilesAndServicesExt API에 적용되는 변경 사항이 표시됩니다.

   여기서는 프로모션 코드 필드(ID: cusBrand)가 API에 삽입됩니다.

   ![](assets/extendpandsapi_diff.png)

1. **[!UICONTROL Publish]** 버튼을 클릭합니다.
