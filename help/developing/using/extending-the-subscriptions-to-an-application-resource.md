---
title: 구독을 확장해 애플리케이션 리소스로 만들기
description: 애플리케이션 리소스로 구독을 확장하는 방법을 알아봅니다
audience: developing
content-type: reference
topic-tags: use-cases--extending-resources
feature: Data Model
role: Developer
level: Experienced
exl-id: ac9c556d-c0f6-4b33-8855-1f5f669c148f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 24%

---

# 구독을 확장해 애플리케이션 리소스로 만들기{#extending-the-subscriptions-to-an-application-resource}

모바일 디바이스에서 전송한 모바일 프로필 속성 데이터는 Adobe Campaign의 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스에 저장됩니다. 이를 통해 애플리케이션 구독자로부터 수집하려는 데이터를 정의할 수 있습니다. 사용자 지정 리소스에 대한 자세한 내용은 [이 페이지](../../developing/using/key-steps-to-add-a-resource.md).

이 리소스는 모바일 장치에서 Adobe Campaign으로 전송하려는 데이터를 수집하도록 확장할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** > **[!UICONTROL Development]** 다음 **[!UICONTROL Custom resources]**&#x200B;을 선택합니다.
1. 클릭 **[!UICONTROL Create]** 그리고 **[!UICONTROL Extend an existing resource]** 선택 사항입니다.
1. 을(를) 선택합니다 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 를 클릭하고 **[!UICONTROL Create]**.

   ![](assets/in_app_personal_data_4.png)

1. 에서 **[!UICONTROL Fields]** 카테고리 **[!UICONTROL Data structure]** 탭에서 을 클릭하여 모바일 애플리케이션에서 검색할 고객 데이터를 정의합니다 **[!UICONTROL Add field]** 버튼을 클릭합니다.

   >[!NOTE]
   >
   >여러 모바일 애플리케이션을 관리하는 경우 모든 애플리케이션에서 사용하는 모든 필드가 나열되어야 합니다. iOS 또는 Android 수집 PII 호출은 각 애플리케이션에서 캡처하는 필드를 정의합니다.

   ![](assets/in_app_personal_data.png)

1. 추가 **[!UICONTROL Label]** 그리고 **[!UICONTROL ID]** 새 필드에 추가합니다. 필드 선택 **[!UICONTROL Type]**.

   ![](assets/schema_extension_uc9.png)

1. 에서 **[!UICONTROL Link to profiles]** 카테고리에서는 Adobe Campaign 데이터베이스의 프로필을 이메일 등의 애플리케이션 구독자에게 연결하는 데 사용되는 조정 키를 구성합니다.

   인앱 메시지의 경우 모든 모바일 애플리케이션에 대해 하나의 조정 키만 정의할 수 있습니다.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Save]** 사용자 지정 리소스를 게시합니다. 사용자 지정 리소스 게시에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
