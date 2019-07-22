---
title: 컨텐츠 블록 추가
seo-title: 컨텐츠 블록 추가
description: 컨텐츠 블록 추가
seo-description: 메시지를 개인화하고 맞춤형 콘텐츠 블록을 만드는 방법을 배울 수 있는 다양한 기본 다이내믹한 콘텐츠 블록을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 08153 EA 0-42 FB -4 C 0 B -8 D 4 B -9407540748 D 6
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 맞춤형 컨텐츠
discoiquuid: 3 ffda 143-f 42 a -4 cf 9-b 43 c-e 53 d 24549025
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 84bc011b079c9f620ea672bf081e54adc023aa07

---


# Adding a content block{#adding-a-content-block}

Adobe Campaign 에서는 미리 구성된 컨텐츠 블록의 목록을 제공합니다. 이러한 컨텐츠 블록은 다이내믹하고 개인적이며 특정 렌더링을 갖습니다. 예를 들어 미러 페이지에 인사말 또는 링크를 추가할 수 있습니다.

>[!NOTE]
>
>The images below show how to insert a content block using the [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) for an email.

컨텐츠 블록을 추가하려면:

1. Click inside a text block, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert content block]**. For more on the Email Designer interface, see [this section](../../designing/using/about-email-content-design.md#email-designer-interface).

   ![](assets/email_content_block_1.png)

1. 삽입할 컨텐츠 블록을 선택합니다. 사용 가능한 블록은 컨텍스트 (이메일 또는 랜딩 페이지) 에 따라 다릅니다.

   ![](assets/email_content_block_2.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

컨텐츠 블록의 이름이 편집기에 표시되고 노란색으로 강조 표시됩니다. 개인화가 생성되면 자동으로 프로필에 맞게 조정됩니다.

![](assets/email_content_block_3.png)

기본 컨텐츠 블록은 다음과 같습니다.

* **[!UICONTROL Database URL in emails (EmailUrlBase)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Mirror page URL (MirrorPageUrl)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Link to mirror page (MirrorPage)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Greetings (Greetings)]**
* **[!UICONTROL Unsubscription link (UnsubscriptionLink)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Social network sharing links (LandingPageViralLinks)]**: 이 컨텐츠 블록은 **랜딩 페이지에서만 사용할**&#x200B;수 있습니다.
* **[!UICONTROL Default sender name (DefaultSenderName)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Name of default reply-to email address (DefaultReplyName)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Email address of default sender (DefaultSenderAddress)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Default error email address (DefaultErrorAddress)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Default reply-to email address (DefaultReplyAddress)]**: 이 컨텐츠 블록은 배달에서만 사용할 **수 있습니다.**
* **[!UICONTROL Brand name (BrandingUsualName)]**
* **[!UICONTROL Link to the brand website (BrandingWebSiteLink)]**
* **[!UICONTROL Brand logo (BrandingLogo)]**
* **[!UICONTROL Notification style (notificationStyle)]**

## Creating custom content blocks {#creating-custom-content-blocks}

메시지 또는 랜딩 페이지에 삽입되는 새 컨텐츠 블록을 정의할 수 있습니다.

컨텐츠 블록을 만들려면 다음 단계를 수행합니다.

1. Click **[!UICONTROL Resources > Content blocks]** from the advanced menu to access the list of content blocks.
1. **[!UICONTROL Create]** 단추를 클릭하거나 기존 컨텐츠 블록을 복제합니다.

   ![](assets/content_bloc_01.png)

1. 레이블을 입력합니다.
1. Select the block's **[!UICONTROL Content type]**. 다음 세 가지 옵션을 사용할 수 있습니다.

   * **[!UICONTROL Shared]**: 컨텐츠 블록은 게재 또는 랜딩 페이지에서 사용할 수 있습니다.
   * **[!UICONTROL Delivery]**: 컨텐츠 블록은 게재에서만 사용할 수 있습니다.
   * **[!UICONTROL Landing page]**: 컨텐츠 블록은 랜딩 페이지에서만 사용할 수 있습니다.
   ![](assets/content_bloc_02.png)

1. You can select a **[!UICONTROL Targeting dimension]**. For more on this, see [About targeting dimension](../../designing/using/adding-a-content-block.md#about-targeting-dimension).

   ![](assets/content_bloc_04.png)

1. You can select the **[!UICONTROL Depends on format]** option to define two different blocks: one for HTML emails, and one for emails in text format. 그러면 해당 컨텐츠를 정의하기 위해 편집기에 두 개의 탭이 표시됩니다 (HTML 및 텍스트).

   ![](assets/content_bloc_03.png)

1. Enter the content of the content block(s), and click the **[!UICONTROL Create]** button.

이제 컨텐츠 블록을 메시지 또는 랜딩 페이지의 컨텐츠 편집기에서 사용할 수 있습니다.

>[!CAUTION]
>
>When editing the content of a block, make sure there are no extra white spaces between the beginning and the end of your *if* statements. HTML에서 공백이 화면에 표시되면 컨텐츠 레이아웃에 영향을 줍니다.

## About targeting dimension {#about-targeting-dimension}

타깃팅 차원을 사용하면 컨텐츠 블록을 사용할 수 있는 메시지 유형을 정의할 수 있습니다. 오류로 인해 오류로 인해 오류가 발생할 수 있습니다.

실제로 메시지를 편집할 때 해당 메시지의 타깃팅 차원과 호환되는 타깃팅 차원이 있는 컨텐츠 블록만 선택할 수 있습니다.

For example, the **[!UICONTROL Unsubscription link]** block's targeting dimension is **[!UICONTROL Profiles]** because it contains personalization fields specific to the **[!UICONTROL Profiles]** resource. Therefore, you cannot use an **[!UICONTROL Unsubscription link]** block in an [event transactional message](../../channels/using/event-transactional-messages.md), because the targeting dimension of that type of message is **[!UICONTROL Real-time events]**. However, you can use the **Unsubscription link** block in a [profile transactional message](../../channels/using/profile-transactional-messages.md), because the targeting dimension of that type of message is **Profiles**. Finally, the **[!UICONTROL Link to mirror page]** block does not have a targeting dimension, so you can use it in any message.

이 필드를 비워 두면 타깃팅 차원이 무엇이든 상관없이 컨텐츠 블록이 모든 메시지와 호환됩니다. 타깃팅 차원을 설정하는 경우 해당 블록은 타깃팅 차원이 동일한 메시지와만 호환됩니다.

For more on this, refer to [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
