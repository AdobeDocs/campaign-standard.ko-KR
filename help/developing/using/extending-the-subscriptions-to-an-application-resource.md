---
title: 구독을 확장해 애플리케이션 리소스로 만들기
description: null
page-status-flag: never-activated
uuid: 8879b427-b31b-4311-bf54-258a91b1fb78
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-cases--extending-resources
discoiquuid: 59faa74e-86fc-42d3-90da-f48580b5ec13
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 25%

---


# 구독을 확장해 애플리케이션 리소스로 만들기{#extending-the-subscriptions-to-an-application-resource}

모바일 디바이스에서 전송한 모바일 프로필 속성 데이터는 Adobe Campaign의 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스에 저장됩니다. 이를 통해 애플리케이션 구독자로부터 수집하려는 데이터를 정의할 수 있습니다. For more information on custom resources, refer to [this page](../../developing/using/key-steps-to-add-a-resource.md).

이 리소스를 확장하여 모바일 장치에서 Adobe Campaign으로 전송할 데이터를 수집할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Development]** 다음 **[!UICONTROL Custom resources]**&#x200B;을 선택합니다.
1. 을 **[!UICONTROL Create]** 클릭하고 **[!UICONTROL Extend an existing resource]** 옵션을 선택합니다.
1. Select the **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource and click **[!UICONTROL Create]**.

   ![](assets/in_app_personal_data_4.png)

1. 탭 **[!UICONTROL Fields]** 카테고리 **[!UICONTROL Data structure]** 에서 **[!UICONTROL Add field]** 단추를 클릭하여 모바일 애플리케이션에서 검색할 고객 데이터를 정의합니다.

   >[!NOTE]
   >
   >여러 모바일 애플리케이션을 관리하는 경우 모든 애플리케이션에서 사용하는 모든 필드가 나열되어야 합니다. iOS 또는 Android 수집 PII 호출은 각 응용 프로그램에서 캡처한 필드를 정의합니다.

   ![](assets/in_app_personal_data.png)

1. 새 필드 **[!UICONTROL Label]** 에 및 **[!UICONTROL ID]** 를 추가합니다. 필드를 선택합니다 **[!UICONTROL Type]**.

   ![](assets/schema_extension_uc9.png)

1. 카테고리에서 **[!UICONTROL Link to profiles]** Adobe Campaign 데이터베이스의 프로파일을 이메일과 같은 애플리케이션의 구독자에게 연결하는 데 사용되는 조정 키를 구성합니다.

   인앱 메시지의 경우 모든 모바일 애플리케이션에 대해 하나의 조정 키만 정의할 수 있습니다.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Save]** 사용자 지정 리소스를 게시합니다. 사용자 지정 리소스 게시에 대한 자세한 내용은 이 [페이지를 참조하십시오](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

