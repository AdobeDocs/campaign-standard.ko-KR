---
title: 이중 옵트인 프로세스 설정
description: 다음 단계에 따라 Adobe Campaign의 랜딩 페이지를 사용하여 이중 옵트인 프로세스를 설정합니다.
page-status-flag: never-activated
uuid: 23e6c4c2-e2c7-472f-b616-36a95225ac1d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 1a24504e-7f9d-4297-b39e-c5f085b0f388
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3b40a9bba79d04f1635b7522cfc99f9e7566c3c0

---


# 이중 옵트인 프로세스 설정{#setting-up-a-double-opt-in-process}

## 이중 옵트인 정보 {#about-double-opt-in}

이중 옵트인 메커니즘은 이메일을 보낼 때 가장 좋은 방법입니다. 플랫폼이 잘못되거나 유효하지 않은 이메일 주소, 스팸 메일 주소 등을 보호하고 스팸 불만 사항을 방지합니다.

기본 사항은 방문자의 계약을 &#39;프로필&#39;으로 저장하기 전에 확인 이메일을 Campaign 데이터베이스에 보내는 것입니다.방문자가 온라인 랜딩 페이지를 작성한 다음 이메일을 수신하고 확인 링크를 클릭하여 구독을 완료해야 합니다.

![](assets/optin_mechanism.png)

이를 설정하려면 다음을 수행해야 합니다.

1. 방문자가 등록하고 가입할 수 있도록 랜딩 페이지를 만들고 게시합니다. 이 랜딩 페이지는 웹 사이트에서 사용할 수 있습니다. 이 랜딩 페이지를 채우고 제출한 방문자는 최종 유효성 검사 전에 통신을 받지 않기 위해 데이터베이스에 저장되지만 &#39;블랙리스트에 [있는&#39; 방문자가 됩니다(Campaign에서 블랙 목록 관리 참조](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)).
1. 확인 링크가 포함된 옵트인 이메일을 자동으로 만들어 보냅니다. 이 이메일은 랜딩 페이지를 제출한 모집단을 대상으로 합니다. &#39;옵트아웃&#39; 프로파일을 타깃팅할 수 있는 이메일 템플릿을 기반으로 합니다.
1. 확인 랜딩 페이지로 리디렉션합니다. 이 최종 랜딩 페이지에는 확인 단추가 표시됩니다.방문자가 클릭해야 합니다. 확인 작업이 완료되면 보낼 환영 이메일을 디자인할 수 있습니다. 예를 들어 새 수신자를 위해 이메일에 특별 오퍼를 추가할 수 있습니다.

모든 매개 변수가 제대로 활성화되도록 하려면 Adobe Campaign에서 이 단계를 설정해야 합니다.

## 1단계:확인 랜딩 페이지 만들기 {#step-1--create-the-confirmation-landing-page}

이중 옵트인 메커니즘을 설정하는 프로세스는 확인 랜딩 페이지 만들기에서 시작됩니다.이 페이지는 방문자가 등록 목적으로 확인 이메일을 클릭하면 표시됩니다.

이 랜딩 페이지를 만들고 구성하려면 다음을 수행해야 합니다.

1. 템플릿을 기반으로 [새 랜딩 페이지를](../../channels/using/getting-started-with-landing-pages.md) 디자인합니다 **[!UICONTROL Profile acquisition (acquisition)]** . &#39;CONFIRMATION&#39; 레이블을&#x200B;**입력합니다**.

   서비스를 [사용해야 하는 경우](../../audiences/using/about-subscriptions.md)**[!UICONTROL Subscription (sub)]** 템플릿을 사용할 수도 있습니다.

1. 랜딩 페이지 속성을 편집하고 **[!UICONTROL Access and loading]** 섹션 아래에서 옵션을 선택 **[!UICONTROL Authorize unidentified visitors]**&#x200B;해제하고 **[!UICONTROL Preload visitor data]** (필수 아님)을 선택합니다.

   ![](assets/optin_confirmlp_param.png)

1. > **[!UICONTROL Job]** 섹션에서 을 클릭하고 다음 컨텍스트 경로를 **[!UICONTROL Additional data]** **[!UICONTROL Add an element]** 입력합니다.

   /context/profile/blackList

   값을 **false로** 설정하고 **[!UICONTROL Add]**&#x200B;클릭합니다.

   ![](assets/optin_confirmlp_newelement.png)

   이 컨텍스트는 이메일을 보낼 수 있도록 블랙 리스트 필드를 제거합니다. 확인 전에 첫 번째 랜딩 페이지에서 이 필드를 **true** 로 설정하여 확인되지 않은 프로필로 이메일을 보내지 않도록 합니다. 자세한 내용은 3단계를 [참조하십시오.획득 랜딩 페이지를](#step-3--create-the-acquisition-landing-page)만듭니다.

1. 랜딩 페이지의 컨텐츠를 사용자 정의합니다.예를 들어 개인화된 데이터를 표시하고 확인 단추의 레이블을 &#39;여기를 클릭하여 구독을 확인할 수 있습니다&#39;로 변경할 수 있습니다.

   ![](assets/optin_confirmlp_design.png)

1. 가입자에게 이제 등록되었음을 알리기 위해 확인 페이지의 컨텐츠를 조정합니다.

   ![](assets/optin_confimlp_page2.png)

1. [랜딩 페이지를 테스트하고 게시합니다](../../channels/using/testing-publishing-landing-page.md) .

## 2단계:확인 이메일 만들기 {#step-2--create-the-confirmation-email}

확인 랜딩 페이지가 만들어지면 확인 이메일을 디자인할 수 있습니다.이 이메일은 획득 랜딩 페이지의 유효성을 검사하는 모든 방문자에게 자동으로 전송됩니다. 이 유효성 검사는 이벤트로 간주되며 이메일은 옵트아웃 모집단을 타깃팅할 수 있는 특정 유형 규칙에 연결된 트랜잭션 메시지입니다.

이러한 요소를 만드는 단계는 아래에 설명되어 있습니다. 이 이메일 템플릿이 참조되므로 획득 랜딩 페이지를 만들기 전에 이를 팔로우해야 합니다.

### 이벤트 만들기 {#create-the-event}

확인 이메일은 이벤트에 반응하는 [트랜잭션 메시지입니다](../../channels/using/about-transactional-messaging.md) .양식의 유효성 검사. 먼저 이벤트를 만든 다음 트랜잭션 메시지의 템플릿을 만들어야 합니다.

1. Adobe Campaign 로고에서 액세스할 수 있는 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]** 메뉴에서 이벤트를 만들고 레이블 &#39;CONFIRM&#39;**을 입력합니다**.
1. 타깃팅 **[!UICONTROL Profile]** 차원을 선택하고 을 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/optin_eventcreate.png)

1. 섹션에서 데이터 구조의 **[!UICONTROL Fields]** 을 클릭하고 **[!UICONTROL Create element]** **[!UICONTROL email]** 추가하여 조정을 활성화합니다.
1. 섹션에서 **[!UICONTROL Enrichment]** 타겟 리소스를 **[!UICONTROL Create element]** 클릭하고 **[!UICONTROL Profile]** 선택합니다. 그런 다음 필요에 따라 **[!UICONTROL email]** 섹션의 **[!UICONTROL Join definition]** 필드 또는 기타 합성 조정 키를 매핑할 수 있습니다.

   ![](assets/optin_eventcreate_join.png)

   서비스를 사용해야 하는 경우 **[!UICONTROL Service]** 대상 리소스를 추가하고 **[!UICONTROL serviceName]** 필드에 매핑합니다. 자세한 내용은 을 참조하십시오.

1. 드롭다운 **[!UICONTROL Profile]** 목록에서 **[!UICONTROL Targeting enrichment]** 을 선택합니다.
1. 이벤트를 **[!UICONTROL Publish]** 게시하려면 을 클릭합니다.

이벤트가 준비되었습니다. 이제 이메일 템플릿을 디자인할 수 있습니다. 이 템플릿에는 이전에 만든 CONFIRMATION **랜딩** 페이지에 대한 링크가 포함되어야 합니다. 자세한 내용은 확인 [메시지](#design-the-confirmation-message)디자인을 참조하십시오.

### 유형 만들기 {#create-the-typology-rule}

즉시 사용 가능한 [유형을](../../sending/using/about-typology-rules.md)복제하여 특정 유형을 만들어야 합니다. The typical will allow to send messages to profiles who did not confirm and still they stayed. 기본적으로 유형 분류는 옵트아웃(즉, 블랙리스트에 추가된) 프로필을 제외합니다. 이 유형을 만들려면 다음 단계를 수행하십시오.

1. Adobe Campaign 로고에서 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** 을 선택하고 **[!UICONTROL Typologies]**&#x200B;클릭합니다.
1. 즉시 사용 가능한 유형을 **[!UICONTROL Transactional message on profile (mcTypologyProfile)]**&#x200B;복제합니다.
1. 중복을 확인한 후 새 유형을 편집하고 TYPELICS_PROFILE 레이블을 **입력합니다**.
1. 차단된 **주소** 규칙을 제거합니다.
1. 클릭 **[!UICONTROL Save]**.

이제 이 유형을 확인 이메일에 연결할 수 있습니다.

### 확인 메시지 디자인 {#design-the-confirmation-message}

확인 이메일은 이전에 만든 이벤트를 기반으로 하는 트랜잭션 메시지입니다. 아래 단계에 따라 이 메시지를 만드십시오.

1. Adobe Campaign 로고에서 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** 을 선택하고 **[!UICONTROL Transactional messages]**&#x200B;클릭합니다.
1. CONFIRM **이메일** 템플릿을 편집하고 개인화합니다. 기존 컨텐츠를 업로드하거나 기본 템플릿을 사용할 수 있습니다.
1. 확인 랜딩 페이지에 대한 링크를 **추가하고** 을 클릭하여 수정 내용을 **[!UICONTROL Confirm]** 저장합니다.

   ![](assets/optin_email_selectlp.png)

1. 이메일 템플릿 속성을 편집합니다. > **[!UICONTROL Advanced parameters]** 섹션에서 이전에 만든 TYPELICS_PROFILE **[!UICONTROL Preparation]** 유형을 **** 선택합니다.
1. 트랜잭션 메시지를 저장하고 게시합니다.

## 3단계:획득 랜딩 페이지 만들기 {#step-3--create-the-acquisition-landing-page}

초기 획득 랜딩 페이지를 만들어야 합니다.이 옵트인 양식이 웹 사이트에 게시됩니다.

이 랜딩 페이지를 만들고 구성하려면 다음을 수행해야 합니다.

1. 템플릿을 기반으로 [새 랜딩 페이지를](../../channels/using/getting-started-with-landing-pages.md) 디자인합니다 **[!UICONTROL Profile acquisition (acquisition)]** . &#39;ACQUISITION&#39; 레이블을&#x200B;**입력합니다**.
1. 랜딩 페이지 속성을 편집합니다.> **[!UICONTROL Job]** 섹션에서 을 클릭하고 다음 컨텍스트 경로를 **[!UICONTROL Additional data]** **[!UICONTROL Add an element]** 입력합니다.

   /context/profile/blackList

   값을 **true로**&#x200B;설정합니다.

   이것은 블랙리스트를 강제하고 계약을 확인하지 않은 방문자에게 메시지를 보내는 것을 피하기 위해 의무적이다. 확인 랜딩 페이지의 유효성 검사에서는 확인 후 이 필드를 **false로** 설정합니다. 자세한 내용은 1단계를 [참조하십시오.확인 랜딩 페이지를](#step-1--create-the-confirmation-landing-page)만듭니다.

1. > **[!UICONTROL Job]** 섹션에서 옵션을 **[!UICONTROL Specific actions]** 선택합니다 **[!UICONTROL Start sending messages]**.
1. 연결된 드롭다운 목록에서 만든 CONFIRM **트랜잭션** 메시지 템플릿을 선택합니다.

   ![](assets/optin_acquisition_startoption.png)

1. 브랜드 및 확보해야 하는 데이터에 따라 랜딩 페이지의 컨텐츠를 사용자 정의합니다. 개인화된 데이터를 표시하고 확인 단추의 레이블을 [내 구독 **확인** ]으로 변경할 수 있습니다.

   ![](assets/optin_acquisition_page1.png)

1. 확인 페이지를 사용자 지정하여 새 구독자에게 자신의 구독의 유효성을 확인해야 한다는 것을 알립니다.

   ![](assets/optin_acquisition_page2.png)

1. [랜딩 페이지를 테스트하고 게시합니다](../../channels/using/testing-publishing-landing-page.md) .

이제 이중 옵트인 메커니즘이 구성됩니다. 이 **[!UICONTROL ACQUISITION]** 랜딩 페이지의 공개 URL부터 시작하여 이 절차를 처음부터 끝까지 실행하고 테스트할 수 있습니다. 이 URL은 랜딩 페이지 대시보드에 표시됩니다.
