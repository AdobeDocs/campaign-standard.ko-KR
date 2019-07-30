---
title: 이중 옵트인 프로세스 설정
seo-title: 이중 옵트인 프로세스 설정
description: 이중 옵트인 프로세스 설정
seo-description: 다음 단계에 따라 Adobe Campaign의 랜딩 페이지를 사용하여 이중 옵트인 프로세스를 설정하십시오.
page-status-flag: 정품 인증 안 함
uuid: 23 E 6 C 4 C 2-E 2 C 7-472 F-B 616-36 A 95225 AC 1 D
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 랜딩 페이지
discoiquuid: 1 A 24504 E -7 F 9 D -4297-B 39 E-C 5 F 085 B 0 F 388
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6dd0c32259d942a0fb790f345cd13800a57e814a

---


# Setting up a double opt-in process{#setting-up-a-double-opt-in-process}

## About double opt-in {#about-double-opt-in}

이메일을 보낼 때 이중 옵트인 메커니즘은 우수 사례입니다. 플랫폼이 잘못되었거나 잘못된 이메일 주소, 스팸, 스팸 차단 등을 방지합니다.

이 원칙은 방문자의 계약서를 캠페인 데이터베이스에'프로필'으로 저장하기 전에 방문자의 계약서를 확인하기 위해 보내는 것입니다. 방문자가 온라인 랜딩 페이지를 채우고 이메일을 받고 확인 링크를 클릭해야 구독을 마무리할 수 있습니다.

![](assets/optin_mechanism.png)

이를 설정하려면 다음을 수행해야 합니다.

1. 방문자가 등록 및 가입할 수 있도록 랜딩 페이지를 만들고 게시합니다. 이 랜딩 페이지는 웹 사이트에서 사용할 수 있습니다. Visitors who fill in and submit this landing page will be stored in the database but ‘blacklisted', in order not to receive any communication before the final validation (see [Managing blacklisting in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)).
1. 확인 링크와 함께 옵트인 이메일을 만들어 자동으로 보냅니다. 이 이메일은 랜딩 페이지를 제출한 모집단을 타깃팅합니다. ' 옵트아웃'프로필을 타깃팅할 수 있는 이메일 템플릿을 기반으로 합니다.
1. 확인 랜딩 페이지로 리디렉션합니다. 이 최종 랜딩 페이지는 확인 단추를 제시하게 됩니다. 방문자가 클릭해야 합니다. 확인으로 전송할 환영 이메일을 디자인할 수 있으며, 예를 들어 새 받는 사람에 대한 이메일에 특별 오퍼를 추가할 수 있습니다.

이러한 단계는 모든 매개 변수를 제대로 사용하도록 하려면 Adobe Campaign에서 설정해야 합니다.

## Step 1: Create the confirmation landing page {#step-1--create-the-confirmation-landing-page}

이중 옵트인 메커니즘을 설정하는 프로세스는 확인 랜딩 페이지 생성으로 시작됩니다. 이 페이지는 방문자가 등록 확인을 위해 확인 이메일을 클릭하면 표시됩니다.

이 랜딩 페이지를 만들고 구성하려면 다음을 수행해야 합니다.

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Profile acquisition (acquisition)]** template. Enter the label '**CONFIRMATION**'.

   If you need to use [services](../../audiences/using/about-subscriptions.md), you can also use the **[!UICONTROL Subscription (sub)]** template.

1. Edit the landing page properties and under the **[!UICONTROL Access and loading]** section, unselect the option **[!UICONTROL Authorize unidentified visitors]**, select **[!UICONTROL Preload visitor data]** (this one is not mandatory).

   ![](assets/optin_confirmlp_param.png)

1. **[!UICONTROL Job]** &gt; **[!UICONTROL Additional data]** 섹션에서 다음 **[!UICONTROL Add an element]** 컨텍스트 경로를 클릭하여 입력합니다.

   /context/profile/blackList

   **값을 false** 로 설정하고 **[!UICONTROL Add]**&#x200B;를 클릭합니다.

   ![](assets/optin_confirmlp_newelement.png)

   이 컨텍스트는 이메일을 전송할 수 있도록 블랙리스트 필드를 제거합니다. We will see later that the first landing page was setting this field to **true** before confirmation, to prevent from sending emails to non-confirmed profiles. For more on this, see [Step 3: Create the acquisition landing page](../../channels/using/setting-up-a-double-opt-in-process.md#step-3--create-the-acquisition-landing-page).

1. 랜딩 페이지의 컨텐츠를 사용자 지정합니다. 개인화된 데이터를 표시하고 확인 단추의 레이블을'여기를 클릭하여 내 구독 확인'으로 변경할 수 있습니다.

   ![](assets/optin_confirmlp_design.png)

1. 이제 가입자에게 등록되었음을 알리는 확인 페이지의 내용을 변경합니다.

   ![](assets/optin_confimlp_page2.png)

1. [랜딩 페이지를 테스트하고 게시합니다](../../channels/using/sharing-a-landing-page.md) .

## Step 2: Create the confirmation email {#step-2--create-the-confirmation-email}

확인 랜딩 페이지가 만들어지면 확인 이메일을 디자인할 수 있습니다. 이 이메일은 획득 랜딩 페이지의 유효성을 검사하는 모든 방문자에게 자동으로 전송됩니다. 이 유효성 검사는 이벤트로 간주되며, 이메일은 옵트아웃 모집단을 타깃팅할 수 있는 특정 유형 지정 규칙에 연결된 트랜잭션 메시지입니다.

이러한 요소를 만드는 단계는 아래에 설명되어 있습니다. 이 이메일 템플릿이 참조되면 획득 랜딩 페이지 자체를 만들기 전에 이를 따라야 합니다.

### Create the event {#create-the-event}

The confirmation email is a [transactional message](../../channels/using/about-transactional-messaging.md) as it reacts to an event: the validation of the form. 먼저 이벤트를 만든 다음 트랜잭션 메시지의 템플릿을 만들어야 합니다.

1. Create an event, from the **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo, and enter the label '**CONFIRM**'.
1. **[!UICONTROL Profile]** 타깃팅 차원을 선택하고 **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   ![](assets/optin_eventcreate.png)

1. **[!UICONTROL Fields]** 섹션에서 데이터 **[!UICONTROL Create element]** 구조에서를 **[!UICONTROL email]** 클릭하고 추가하여 조정을 활성화합니다.
1. **[!UICONTROL Enrichment]** 섹션에서 대상 리소스를 클릭하여 **[!UICONTROL Create element]** 선택합니다 **[!UICONTROL Profile]**. You can then map on the **[!UICONTROL email]** in the **[!UICONTROL Join definition]** section, or any other composite reconciliation key, depending on your needs.

   ![](assets/optin_eventcreate_join.png)

   If you need to use services, you can also add the **[!UICONTROL serviceName]**.

1. Select **[!UICONTROL Profile]** as the **[!UICONTROL Targeting enrichment]** in the dropdown list.
1. Click **[!UICONTROL Publish]** to publish the event.

이벤트가 준비되었습니다. 이제 이메일 템플릿을 디자인할 수 있습니다. This template must include a link to the **CONFIRMATION** landing page created before. For more on this, see [Design the confirmation message](../../channels/using/setting-up-a-double-opt-in-process.md#design-the-confirmation-message).

### Create the typology rule {#create-the-typology-rule}

You need to create a specific [typology rule](../../administration/using/about-typology-rules.md), by duplicating an out-of-box one. 이 규칙은 아직 자신의 계약서를 확인하지 않았고 여전히 차단 상태인 프로필로 메시지를 보낼 수 있게 해 줍니다. 기본적으로 유형 지정 규칙은 옵트아웃 (즉, 블랙리스트에 추가된) 프로필을 제외합니다. 이러한 유형 규칙을 만들려면 다음 단계를 수행하십시오.

1. From the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Typologies]** and click **[!UICONTROL Typologies]**.
1. Duplicate the out-of-box typology **[!UICONTROL Transactional message on profile (mcTypologyProfile)]**.
1. Once duplication confirmed, edit the new typology and enter the label **TYPOLOGY_PROFILE**.
1. **블랙리스트에 추가된 주소** 규칙을 제거합니다.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

이제 이러한 유형을 확인 이메일에 연결할 수 있습니다.

### Design the confirmation message {#design-the-confirmation-message}

확인 이메일은 이전에 만든 이벤트를 기반으로 하는 트랜잭션 메시지입니다. 아래 절차에 따라 이 메시지를 작성하십시오.

1. From the Adobe Campaign logo, select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** and click **[!UICONTROL Transactional messages]**.
1. **확인** 이메일 템플릿을 편집하고 개인화합니다. 기존 컨텐츠를 업로드하거나 즉시 사용할 수 있는 템플릿을 사용할 수 있습니다.
1. **확인** 랜딩 페이지에 링크를 추가하고를 클릭하여 **[!UICONTROL Confirm]** 수정 사항을 저장합니다.

   ![](assets/optin_email_selectlp.png)

1. 이메일 템플릿 속성을 편집합니다. **[!UICONTROL Advanced parameters]** &gt; **[!UICONTROL Preparation]** 섹션에서 이전에 만든 **tyatype_ profile** 유형을 선택합니다.
1. 트랜잭션 메시지를 저장하고 게시합니다.

## Step 3: Create the acquisition landing page {#step-3--create-the-acquisition-landing-page}

초기 획득 랜딩 페이지를 만들어야 합니다. 이 OP-in 양식은 웹 사이트에 게시됩니다.

이 랜딩 페이지를 만들고 구성하려면 다음을 수행해야 합니다.

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Profile acquisition (acquisition)]** template. Enter the label '**ACQUISITION**'.
1. Edit the landing page properties: in the **[!UICONTROL Job]** &gt; **[!UICONTROL Additional data]** section, click **[!UICONTROL Add an element]** and enter the following context path:

   /context/profile/blackList

   and set the value to **true**.

   강제 블랙리스트를 강제 적용하고 해당 계약서를 확인하지 않은 방문자에게 메시지를 보내지 않는 것이 필수적입니다. The validation of the CONFIRMATION landing page will set this field to **false** after confirmation. For more on this, see [Step 1: Create the confirmation landing page](../../channels/using/setting-up-a-double-opt-in-process.md#step-1--create-the-confirmation-landing-page).

1. **[!UICONTROL Job]** &gt; **[!UICONTROL Specific actions]** 섹션에서 옵션을 **[!UICONTROL Start sending messages]**&#x200B;선택합니다.
1. In the associated drop-down list, choose the **CONFIRM** transactional message template you created.

   ![](assets/optin_acquisition_startoption.png)

1. 자사 브랜드와 구매해야 하는 데이터에 따라 랜딩 페이지의 컨텐츠를 사용자 정의합니다. You can display personalized data and change the label of the confirmation button to **Confirm my subscription** for example.

   ![](assets/optin_acquisition_page1.png)

1. 확인 페이지를 사용자 지정하여 새 구독자에게 자신의 구독 상태를 확인해야 함을 알립니다.

   ![](assets/optin_acquisition_page2.png)

1. [랜딩 페이지를 테스트하고 게시합니다](../../channels/using/sharing-a-landing-page.md) .

이제 이중 옵트인 메커니즘이 구성됩니다. You can run and test the procedure from end to end, starting from the public URL of this **[!UICONTROL ACQUISITION]** landing page. 이 URL는 랜딩 페이지 대시보드에 표시됩니다.
