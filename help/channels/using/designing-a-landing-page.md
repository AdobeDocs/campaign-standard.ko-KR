---
title: 랜딩 페이지 디자인
seo-title: 랜딩 페이지 디자인
description: 랜딩 페이지 디자인
seo-description: 랜딩 페이지의 컨텐츠를 디자인하고 서비스에 연결하려면 다음 단계를 따르십시오.
page-status-flag: 활성화 안 함
uuid: de6fe190-835c-40fd-8101-a809b430b423
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 랜딩 페이지
discoiquuid: bd77d6f0-3143-4030-a91b-988a2bebc534
context-tags: landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: aeb0e7bc6765b23042fafd34fb360d4e3046adcd

---


# 랜딩 페이지 디자인{#designing-a-landing-page}

## 컨텐츠 디자인 정보 {#about-content-design}

랜딩 페이지는 [마케팅 활동으로](../../start/using/marketing-activities.md#about-marketing-activities)만들어집니다.

랜딩 페이지를 디자인할 때 다음 컨텐츠를 정의해야 합니다.

* 페이지 자체,
* 확인 페이지,
* 오류 페이지를 참조하십시오.

작업 표시줄 아래에 있는 전환기를 사용하여 이러한 각 페이지를 표시하고 구성합니다.

이러한 페이지의 컨텐츠는 캠페인 컨텐츠 편집기를 통해 디자인되었습니다. 디자인 [컨텐츠를](../../channels/using/about-landing-page-content-design.md)참조하십시오.

## 양식 필드 매핑 {#mapping-form-fields}

입력 필드는 Campaign 데이터베이스에 데이터를 저장하거나 업데이트하는 데 사용됩니다. 이렇게 하려면 데이터베이스 필드를 입력 영역, 라디오 단추 또는 확인란 유형 블록과 연결해야 합니다. 이렇게 하려면:

1. Select a block in the landing page.
1. 팔레트에서 **[!UICONTROL Form data]** 부품을 완료합니다.

   ![](assets/editing_lp_content_4.png)

1. Choose a database field to link with the form field in the **[!UICONTROL Field]** selection zone.

   When the **[!UICONTROL Mandatory]** option is checked, the page can only be submitted if the user has completed this field. If a mandatory field is not completed, an error message will appear when the user validates the page.

   >[!NOTE]
   >
   >Landing pages can only be mapped with **Profiles**.

1. Define the field type by choosing, for example , , or  in the  selection area.**[!UICONTROL Text]****[!UICONTROL Number]****[!UICONTROL Date]****[!UICONTROL HTML type of the field]**

>[!NOTE]
>
>The default fields of the built-in landing pages are preconfigured. You can modify them as needed.

## Submitting the form {#submitting-the-form}

You can select the action to perform when the visitor clicks the submit button. To do this:

1. Select the submit button of the landing page.
1. Select the action in the drop-down list in the left panel. Possible actions are:  (to refresh the page) and  (to display the confirmation page).**[!UICONTROL Refresh]****[!UICONTROL Next page]**

   ![](assets/editing_lp_content_5.png)

또한 단추의 레이블을 변경하거나 특정 링크를 구성할 수 있습니다. To do this:

1. 제출 단추를 선택합니다.
1. 왼쪽 패널에서 ![](assets/lp_link_properties.png) 버튼을 클릭합니다.
1. 단추의 레이블을 입력하고 링크 유형, 속성 및 대상을 선택합니다.

   ![](assets/lp_link_custom.png)

## 서비스에 양식 연결 {#linking-a-form-to-a-service}

랜딩 페이지의 유효성을 검사할 때 특정 서비스에 프로필을 가입할 수 있도록 양식을 서비스에 연결할 수 있습니다.

랜딩 페이지 연결에 대한 매개 변수를 사용하여 수행한 작업 유형과 랜딩 페이지가 특정 단일 서비스에 연결되어 있는지 또는 일반적인지를 지정할 수 있습니다.

연결할 서비스를 선택하려면 다음을 수행해야 합니다.

1. 랜딩 페이지 대시보드의 ![](assets/edit_darkgrey-24px.png) 아이콘을 통해 액세스한 랜딩 페이지 속성을 편집하고 **[!UICONTROL Job]** 매개 변수를 표시합니다.

   ![](assets/lp_edit_properties_button.png)

1. 드롭다운 **[!UICONTROL Subscription]** 목록에서 **[!UICONTROL Specific actions]** 선택합니다.

   ![](assets/lp_parameters_5.png)

1. 랜딩 페이지를 단일 서비스에 **[!UICONTROL Specific service]** 연결하려면 선택합니다. 랜딩 페이지에서 여러 서비스를 사용하려면 이 옵션을 선택하지 마십시오.

   여러 서비스에 랜딩 페이지를 사용할 수 있도록 하려면 이 **[!UICONTROL Specified service in the URL]** 옵션을 사용합니다. 따라서 서비스를 구성할 때 랜딩 페이지를 참조해야 합니다.

### 랜딩 페이지 제출 확인 {#confirm-a-landing-page-submission}

방문자가 랜딩 페이지를 제출하면 트리거된 작업을 구성할 수 있습니다. 이렇게 하려면:

1. 랜딩 페이지 대시보드의 ![](assets/edit_darkgrey-24px.png) 아이콘을 통해 액세스한 랜딩 페이지 속성을 편집하고 **[!UICONTROL Job]** 매개 변수를 표시합니다.

   ![](assets/lp_edit_properties_button.png)

1. 이 **[!UICONTROL Specific actions]** 섹션에서 자동 메시지 전송을 **[!UICONTROL Start sending message]** 결정하려면 선택합니다. 예를 들어 서비스에 대한 가입을 확인합니다. 그런 다음 이메일 배달 템플릿을 선택해야 합니다.

   확인 메시지가 이미 서비스 수준에서 구성된 경우 이 화면에서 확인 메시지를 여러 번 보내지 않도록 선택할 수 없습니다. 서비스 [구성을](../../audiences/using/creating-a-service.md)참조하십시오.

1. 랜딩 페이지를 제출할 때 추가 데이터를 저장할 **[!UICONTROL Additional data]** 수 있도록 만듭니다. 이 데이터는 페이지를 방문한 사람에게 표시되지 않습니다. 상수 값만 고려됩니다.

   ![](assets/lp_parameters_6.png)

## 권한 설정 및 사전 로드 데이터 {#setting-permissions-and-pre-loading-data}

랜딩 페이지에 대한 액세스는 Campaign에서 보낸 메시지의 링크에서 온 식별된 방문자로 제한됩니다. 이 경우 랜딩 페이지에서 데이터를 미리 로드할 수 있습니다. 이렇게 하려면:

1. Edit the landing page properties accessed via the  icon in the landing page dashboard, and display the  parameters.![](assets/edit_darkgrey-24px.png)**[!UICONTROL Access & loading]**

   ![](assets/lp_edit_properties_button.png)

1. 을 **[!UICONTROL Preload visitor data]**&#x200B;선택합니다.

   If a visitor to the page corresponds to a profile in the database, their data is displayed in the form's fields that are mapped with the database data and the landing page's personalization elements are taken into account.

   ![](assets/lp_parameters_3.png)

You can also:

* Use the URL parameters to identify the visitors, using the  option: then you must choose the loading key and map the filter parameters with the parameters of the corresponding URL.**[!UICONTROL Authorize visitor identification via URL parameters]**
* Authorize any visitor to access the landing page, using the  option.**[!UICONTROL Authorize unidentified visitors]**

## Setting Google reCAPTCHA {#setting-google-recaptcha}

You can set up Google reCAPTCHA V3 with your landing page to protect it from spam and abuse caused by bots. To be able to use it with your landing page, you first need to create an external account. For more information on how to configure it, refer to this section.[](../../administration/using/external-accounts.md#google-recaptcha-external-account)

Google reCAPTCHA V3 외부 계정이 설정되면 랜딩 페이지에 추가할 수 있습니다.

1. Before publishing your landing page, access the page properties accessed via the  icon from you landing page dashboard.![](assets/edit_darkgrey-24px.png)

   ![](assets/lp_parameters_google3.png)

1. Unfold the  menu.**[!UICONTROL Access & loading]**
1. Check the  option.**[!UICONTROL Use reCAPTCHA to protect your site from spam and abuse]**
1. Select your previously created Google reCAPTCHA external account.

   ![](assets/lp_parameters_google.png)

1. Click **[!UICONTROL Confirm]**.

Your landing page is now set up with Google reCAPTCHA which can be seen at the bottom of your page.

![](assets/lp_parameters_google2.png)

Google reCAPTCHA will then return a score based on users' interactions with your page. 점수를 확인하려면 Google 관리 콘솔에 [연결합니다](https://g.co/recaptcha/admin).
