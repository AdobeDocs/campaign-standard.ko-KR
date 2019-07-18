---
title: 랜딩 페이지 디자인
seo-title: 랜딩 페이지 디자인
description: 랜딩 페이지 디자인
seo-description: 다음 단계에 따라 랜딩 페이지의 컨텐츠를 디자인하고 서비스에 연결하십시오.
page-status-flag: 정품 인증 안 함
uuid: DE 6 FE 190-835 C -40 FD -8101-A 809 B 430 B 423
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 랜딩 페이지
discoiquuid: BD 77 D 6 F 0-3143-4030-A 91 B -988 A 2 BEBC 534
context-tags: landingpage, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Designing a landing page{#designing-a-landing-page}

## About content design {#about-content-design}

Landing pages are created as any [marketing activity](../../start/using/marketing-activities.md#about-marketing-activities).

랜딩 페이지를 디자인할 때에는 다음 컨텐츠의 컨텐츠를 정의해야 합니다.

* 페이지 자체,
* 확인 페이지,
* 오류 페이지.

작업 표시줄에서 전환기를 사용하여 이러한 각 페이지를 표시하고 구성합니다.

이러한 페이지의 내용은 캠페인 컨텐츠 편집기를 통해 디자인됩니다. Refer to [Design content](../../designing/using/about-landing-page-content-design.md).

## Mapping form fields {#mapping-form-fields}

입력 필드는 캠페인 데이터베이스에서 데이터를 저장하거나 업데이트하는 데 사용됩니다. 따라서 데이터베이스 필드를 입력 영역, 라디오 단추 또는 확인란 유형 블록과 연결해야 합니다. 이렇게 하려면:

1. 랜딩 페이지에서 블록을 선택합니다.
1. Complete the **[!UICONTROL Form data]** part in the palette.

   ![](assets/editing_lp_content_4.png)

1. Choose a database field to link with the form field in the **[!UICONTROL Field]** selection zone.

   **[!UICONTROL Mandatory]** 이 옵션을 선택하면 사용자가 이 필드를 완료한 경우에만 페이지를 제출할 수 있습니다. 필수 필드가 완료되지 않으면 사용자가 페이지의 유효성을 검사할 때 오류 메시지가 표시됩니다.

   >[!NOTE]
   >
   >Landing pages can only be mapped with **Profiles**.

1. Define the field type by choosing, for example **[!UICONTROL Text]**, **[!UICONTROL Number]**,or **[!UICONTROL Date]** in the **[!UICONTROL HTML type of the field]** selection area.

>[!NOTE]
>
>기본 제공 랜딩 페이지의 기본 필드가 미리 구성되어 있습니다. 필요에 따라 수정할 수 있습니다.

## Submitting the form {#submitting-the-form}

방문자가 제출 단추를 클릭할 때 수행할 작업을 선택할 수 있습니다. 이렇게 하려면:

1. 랜딩 페이지의 제출 단추를 선택합니다.
1. 왼쪽 패널의 드롭다운 목록에서 동작을 선택합니다. Possible actions are: **[!UICONTROL Refresh]** (to refresh the page) and **[!UICONTROL Next page]** (to display the confirmation page).

   ![](assets/editing_lp_content_5.png)

또한 단추의 레이블을 변경하거나 특정 링크를 구성할 수 있습니다. 이렇게 하려면:

1. 제출 단추를 선택합니다.
1. Click on the ![](assets/lp_link_properties.png) button in the left panel.
1. 단추 레이블을 입력하고 링크 유형, 속성 및 대상을 선택합니다.

   ![](assets/lp_link_custom.png)

## Linking a form to a service {#linking-a-form-to-a-service}

랜딩 페이지의 유효성을 검사할 때 프로필에서 특정 서비스에 가입할 수 있도록 양식을 서비스에 연결할 수 있습니다.

랜딩 페이지를 연결하기 위한 매개 변수를 사용하여 수행된 작업 유형과 랜딩 페이지가 단일 서비스에 구체적으로 연결되었는지 아니면 일반적인지를 지정할 수 있습니다.

연결할 서비스를 선택하려면 다음을 수행해야 합니다.

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_edit_properties_button.png)

1. Choose **[!UICONTROL Subscription]** in the **[!UICONTROL Specific actions]** drop-down list.

   ![](assets/lp_parameters_5.png)

1. Select **[!UICONTROL Specific service]** to link the landing page to a single service. 랜딩 페이지와 함께 여러 서비스를 사용하려는 경우 이 옵션을 선택하지 마십시오.

   Use the **[!UICONTROL Specified service in the URL]** option to allow the landing page to be used for several services. 따라서 서비스를 구성할 때 랜딩 페이지를 참조해야 합니다.

### Confirm a landing page submission {#confirm-a-landing-page-submission}

방문자가 랜딩 페이지를 제출하면 트리거된 작업을 구성할 수 있습니다. 이렇게 하려면:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Job]** parameters.

   ![](assets/lp_edit_properties_button.png)

1. **[!UICONTROL Specific actions]** 섹션에서, 예를 들어 **[!UICONTROL Start sending message]** 서비스에 대한 가입을 확인하는 등의 자동 메시지 전송을 결정합니다. 이메일 배달 템플릿을 선택해야 합니다.

   확인 메시지가 이미 서비스 수준에서 구성되어 있는 경우, 여러 확인 메시지를 보내지 않도록 이 화면에서 하나를 선택하지 말아야 합니다. Refer to [Configure a service](../../audiences/using/creating-a-service.md).

1. Create **[!UICONTROL Additional data]** to enable storing additional data when the landing page is being submitted. 이 데이터는 페이지를 방문한 사람들이 볼 수 없습니다. 상수 값만 고려됩니다.

   ![](assets/lp_parameters_6.png)

## Setting permissions and pre-loading data {#setting-permissions-and-pre-loading-data}

랜딩 페이지에 대한 액세스는 예를 들어 캠페인으로 전송된 메시지의 링크에서 오는 식별된 방문자로 제한될 수 있습니다. 이 경우 랜딩 페이지에서 해당 데이터를 미리 로드할 수 있습니다. 이렇게 하려면:

1. Edit the landing page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon in the landing page dashboard, and display the **[!UICONTROL Access & loading]** parameters.

   ![](assets/lp_edit_properties_button.png)

1. **[!UICONTROL Preload visitor data]** Select.

   페이지의 방문자가 데이터베이스의 프로필에 해당하는 경우 해당 데이터가 데이터베이스 데이터와 매핑된 양식 필드에 표시되고 랜딩 페이지의 개인화 요소가 고려됩니다.

   ![](assets/lp_parameters_3.png)

다음을 수행할 수도 있습니다.

* Use the URL parameters to identify the visitors, using the **[!UICONTROL Authorize visitor identification via URL parameters]** option: then you must choose the loading key and map the filter parameters with the parameters of the corresponding URL.
* Authorize any visitor to access the landing page, using the **[!UICONTROL Authorize unidentified visitors]** option.

## Setting Google reCAPTCHA {#setting-google-recaptcha}

랜딩 페이지와 함께 Google recaptcha v 3를 설정하여 봇으로 인한 스팸 및 남용으로부터 보호할 수 있습니다. 랜딩 페이지에서 사용하려면 먼저 외부 계정을 만들어야 합니다. For more information on how to configure it, refer to this [section](../../administration/using/external-accounts.md#google-recaptcha-external-account).

Google recaptcha v 3 외부 계정이 설정되면 랜딩 페이지에 해당 계정을 추가할 수 있습니다.

1. Before publishing your landing page, access the page properties accessed via the ![](assets/edit_darkgrey-24px.png) icon from you landing page dashboard.

   ![](assets/lp_parameters_google3.png)

1. **[!UICONTROL Access & loading]** 메뉴를 펼칩니다.
1. Check the **[!UICONTROL Use reCAPTCHA to protect your site from spam and abuse]** option.
1. 이전에 만든 Google recaptcha 외부 계정을 선택합니다.

   ![](assets/lp_parameters_google.png)

1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

랜딩 페이지가 이제 페이지 하단에 표시될 수 있는 Google recaptcha로 설정되었습니다.

![](assets/lp_parameters_google2.png)

Google recaptcha는 사용자의 페이지와의 상호 작용에 따라 점수를 반환합니다. To check your score, connect to your [Google admin console](https://g.co/recaptcha/admin).
