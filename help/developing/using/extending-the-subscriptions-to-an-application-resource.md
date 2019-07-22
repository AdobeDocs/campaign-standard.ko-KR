---
title: 응용 프로그램 리소스에 대한 구독 확장
seo-title: 응용 프로그램 리소스에 대한 구독 확장
description: 응용 프로그램 리소스에 대한 구독 확장
seo-description: null
page-status-flag: 정품 인증 안 함
uuid: 8879 B 427-B 31 B -4311-BF 54-258 A 91 B 1 FB 78
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: 사용 사례—Extending-resources
discoiquuid: 59 FAA 74 E -86 FC -42 D 3-90 DA-F 48580 B 5 EC 13
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 20b4d5dfb297cac4cd69fe6f945b4399abd7f06a

---


# Extending the subscriptions to an application resource{#extending-the-subscriptions-to-an-application-resource}

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications' subscribers. For more information on custom resources, refer to this [page](../../developing/using/key-steps-to-add-a-resource.md).

모바일 장치에서 Adobe Campaign로 전송할 데이터를 수집하도록 이 리소스를 확장할 수 있습니다.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. Click **[!UICONTROL Create]** and choose the **[!UICONTROL Extend an existing resource]** option.
1. **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 리소스를 선택하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   ![](assets/in_app_personal_data_4.png)

1. In the **[!UICONTROL Fields]** category of the **[!UICONTROL Data structure]** tab, define the customer data that you want to retrieve from your mobile application by clicking the **[!UICONTROL Add field]** button.

   >[!NOTE]
   >
   >여러 모바일 애플리케이션을 관리하는 경우 모든 애플리케이션에서 사용하는 모든 필드를 나열해야 합니다. iOS 또는 Android 수집 수집은 각 응용 프로그램에서 캡처한 필드를 정의합니다.

   ![](assets/in_app_personal_data.png)

1. Add a **[!UICONTROL Label]** and an **[!UICONTROL ID]** to your new field. Select your field's **[!UICONTROL Type]**.

   ![](assets/schema_extension_uc9.png)

1. **[!UICONTROL Link to profiles]** 카테고리에서 Adobe Campaign 데이터베이스의 프로필을 이메일과 같은 응용 프로그램의 가입자에게 연결하는 데 사용되는 조정 키를 구성합니다.

   In-App 메시지는 모든 모바일 애플리케이션에 대해 하나의 조정 키만 정의할 수 있습니다.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Save]** 사용자 지정 리소스를 게시할 수 있습니다. For more information on custom resource publication, refer to this [page](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

