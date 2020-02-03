---
title: 'Experience Manager에서 Campaign 양식 만들기 '
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 양식을 작성하여 프로파일을 만들고 업데이트하거나 구독을 관리할 수 있습니다.
page-status-flag: never-activated
uuid: 43057f81-d47d-4b96-b150-217c289cd608
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 4a8b5807-87dd-4db4-bd67-890f0adae932
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5c1a540475b7d93c18c957243ee2a403b8154aa3

---


# Experience Manager에서 Campaign 양식 만들기 {#creating-a-campaign-form-in-experience-manager}

AEM 사이트에서 &quot;양식&quot;을 만들고 양식의 필드를 Adobe Campaign 데이터베이스의 필드에 매핑할 수 있습니다. 따라서 프로파일을 생성 및 업데이트하거나 서비스에 대한 가입을 관리할 수 있습니다.

AEM 사이트에서 Adobe Campaign 양식을 만들려면:

1. AEM 사이트에서 Adobe Campaign 프로필 템플릿을 기반으로 새 **페이지를 만듭니다** .

   ![](assets/aem_content_forms.png)

1. 페이지 속성에서 Adobe Campaign 인스턴스에 **[!UICONTROL Cloud Service]**해당하는 항목을 선택합니다.

   ![](assets/aem_content_forms_2.png)

1. 구성 요소에서 양식 유형을 **[!UICONTROL Form Start]**선택합니다.

   * **Adobe Campaign:프로필 저장**
   * **Adobe Campaign:서비스 가입**
   * **Adobe Campaign:서비스 가입 해지**

1. Adobe Campaign 데이터베이스 필드에 매핑할 수 있는 서로 다른 필드 및 구성 요소를 추가하여 양식의 컨텐츠를 편집합니다.
1. 양식을 테스트하고 게시하여 AEM 사이트에서 액세스할 수 있도록 합니다.

자세한 내용은 [자세한 설명서를](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/adobe-campaign-forms.html)참조하십시오.
