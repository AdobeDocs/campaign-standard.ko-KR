---
title: 'Experience Manager에서 캠페인 양식 만들기 '
seo-title: 'Experience Manager에서 캠페인 양식 만들기 '
description: 'Experience Manager에서 캠페인 양식 만들기 '
seo-description: Adobe Experience Manager 통합을 통해 AEM에서 직접 양식을 만들어 프로필을 만들거나 업데이트하거나 구독을 관리할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 43057 F 81-D 47 D -4 B 96-B 150-217 C 289 CD 608
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 4 a 8 b 5807-87 dd -4 db 4-bd 67-890 f 0 adae 932
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: eed2e3597548c97345f51fe62dd2b56af5042e87

---


# Creating a Campaign form in Experience Manager {#creating-a-campaign-form-in-experience-manager}

AEM 사이트에서 "양식" 를 만들고 양식의 필드를 Adobe Campaign 데이터베이스의 필드에 매핑할 수 있습니다. 이를 통해 프로필을 생성 및 업데이트하거나 서비스에 대한 가입을 관리할 수 있습니다.

AEM 사이트에서 Adobe Campaign 양식을 만들려면:

1. In your AEM site, create a new page based on the **Adobe Campaign Profile** template.

   ![](assets/aem_content_forms.png)

1. In the page properties, select the **[!UICONTROL Cloud Service]** corresponding to your Adobe Campaign instance.

   ![](assets/aem_content_forms_2.png)

1. Select the form type from the **[!UICONTROL Form Start]** component:

   * **Adobe Campaign: 프로필 저장**
   * **Adobe Campaign: 서비스 구독**
   * **Adobe Campaign: 서비스 가입 해지**

1. Adobe Campaign 데이터베이스 필드에 매핑할 수 있는 서로 다른 필드 및 구성 요소를 추가하여 양식의 컨텐츠를 편집합니다.
1. AEM 사이트에서 액세스할 수 있도록 양식을 테스트하고 게시합니다.

For more information, refer to the [detailed documentation](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/adobe-campaign-forms.html).
