---
solution: Campaign Standard
product: campaign
title: 'Experience Manager에서 Campaign 양식 만들기 '
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 양식을 작성하여 프로파일을 생성 및 업데이트하거나 구독을 관리할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: 트리거
role: 데이터 아키텍트
level: 중간
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# Experience Manager에서 Campaign 양식 만들기 {#creating-a-campaign-form-in-experience-manager}

AEM 사이트에서 &quot;양식&quot;을 만들고 양식의 필드를 Adobe Campaign 데이터베이스의 필드에 매핑할 수 있습니다. 이를 통해 프로파일을 생성 및 업데이트하거나 서비스 가입을 관리할 수 있습니다.

AEM 사이트에서 Adobe Campaign 양식을 만들려면:

1. AEM 사이트에서 **Adobe Campaign Profile** 템플릿을 기반으로 새 페이지를 만듭니다.

   ![](assets/aem_content_forms.png)

1. 페이지 속성에서 Adobe Campaign 인스턴스에 해당하는 **[!UICONTROL Cloud Service]**&#x200B;을 선택합니다.

   ![](assets/aem_content_forms_2.png)

1. **[!UICONTROL Form Start]** 구성 요소에서 양식 유형을 선택합니다.

   * **Adobe Campaign:프로필 저장**
   * **Adobe Campaign:서비스 가입**
   * **Adobe Campaign:서비스 가입 해지**

1. Adobe Campaign 데이터베이스 필드에 매핑할 수 있는 서로 다른 필드 및 구성 요소를 추가하여 양식의 내용을 편집합니다.
1. AEM 사이트에서 액세스할 수 있도록 양식을 테스트하고 게시합니다.

자세한 내용은 [세부 설명서](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/adobe-campaign-forms.html)를 참조하십시오.
