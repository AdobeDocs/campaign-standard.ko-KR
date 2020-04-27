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
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# 구독을 확장해 애플리케이션 리소스로 만들기{#extending-the-subscriptions-to-an-application-resource}

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications&#39; subscribers. 사용자 지정 리소스에 대한 자세한 내용은 [이 페이지를](../../developing/using/key-steps-to-add-a-resource.md)참조하십시오.

이 리소스를 확장하여 모바일 장치에서 Adobe Campaign으로 전송할 데이터를 수집할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Development]**&#x200B;을 선택한 다음 **[!UICONTROL Custom resources]**&#x200B;선택합니다.
1. 을 **[!UICONTROL Create]** 클릭하고 **[!UICONTROL Extend an existing resource]** 옵션을 선택합니다.
1. 리소스를 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 선택하고 을 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/in_app_personal_data_4.png)

1. 탭의 **[!UICONTROL Fields]** 카테고리에서 **[!UICONTROL Data structure]** **[!UICONTROL Add field]** 단추를 클릭하여 모바일 애플리케이션에서 검색할 고객 데이터를 정의합니다.

   >[!NOTE]
   >
   >여러 모바일 애플리케이션을 관리하는 경우 모든 애플리케이션에서 사용하는 모든 필드가 나열되어야 합니다. iOS 또는 Android 수집 PII 호출은 각 애플리케이션에서 캡처되는 필드를 정의합니다.

   ![](assets/in_app_personal_data.png)

1. 새 필드에 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 를 추가합니다. 필드를 **[!UICONTROL Type]**&#x200B;선택합니다.

   ![](assets/schema_extension_uc9.png)

1. 카테고리에서 Adobe Campaign 데이터베이스의 프로필을 이메일과 같은 애플리케이션의 구독자에게 연결하는 데 사용되는 조정 키를 구성합니다. **[!UICONTROL Link to profiles]**

   인앱 메시지의 경우 모든 모바일 애플리케이션에 대해 하나의 조정 키만 정의할 수 있습니다.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Save]** 사용자 지정 리소스를 게시할 수 있습니다. 사용자 지정 리소스 게시에 대한 자세한 내용은 이 [페이지를](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)참조하십시오.

