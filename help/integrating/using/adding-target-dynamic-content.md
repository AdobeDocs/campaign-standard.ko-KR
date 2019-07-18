---
title: Target 동적 컨텐츠 추가
seo-title: Target 동적 컨텐츠 추가
description: Target 동적 컨텐츠 추가
seo-description: Adobe Campaign 게재 중 하나에서 Adobe Target 동적 컨텐츠를 추가하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: B 3 CC 045 F -7924-480 E -8 C 61-8246510 F 3 ADB
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-target
discoiquuid: 45 DDF 7 B 7-98 F 7-4 FDD-BB 4 A -49 EC 8490 E 877
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Adding Target dynamic content{#adding-target-dynamic-content}

Adobe Target 통합을 통해 다이내믹한 이미지를 전달에 추가하여 경험에 따라 컨텐츠를 개인화할 수 있습니다.

이메일을 편집하는 동안 Adobe Target에서 받는 사람에 따라 변경되는 동적 이미지를 삽입할 수 있습니다.

Adobe Campaign에서 이미지에 액세스하려면 먼저 Adobe Target에서 다음 작업을 수행해야 합니다.

* Create one or several [redirect offers](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Creating_a_Redirect_Offer.html), in which you must specify the URL of the image you will be using.
* Create one or several [audiences](https://marketing.adobe.com/resources/help/en_US/target/ov/c_about_segments.html), to define the target of your activity.
* Create a [Form-based experience composer](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html) activity, in which you have to select a rawbox and specify several experiences, depending on the number of redirect offers created. 각 경험에 대해 만든 리디렉션 오퍼 중 하나를 선택해야 합니다.
* Adobe Campaign의 정보를 사용하여 세그먼트를 만들어 경험을 지정합니다. 오퍼의 선택 규칙에서 Adobe Campaign의 데이터를 사용하려면 Adobe Target의 rawbox에서 데이터를 지정해야 합니다.

1. 이메일 게재를 만듭니다.
1. When editing the content of an email or a landing page, go to an image block, then select **[!UICONTROL Dynamic image from Adobe Target]** via the contextual menu.

   ![](assets/tar_insert_dynamic_image.png)

1. 기본적으로 이메일에서 표시되는 이미지를 선택합니다. You can directly specify the image URL or select an image shared via [Assets](../../integrating/using/working-with-campaign-and-assets-core-service.md).

   통합은 정적 이미지만 지원합니다. 나머지 컨텐츠는 사용자 정의할 수 없습니다.

1. Adobe Target에 지정된 rawbox의 이름을 입력합니다.
1. Adobe Target의 설정에서 기업 권한을 사용하는 경우 이 필드에 해당 속성을 추가합니다. Learn more about Target Enterprise permissions in [this page](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html). Target에서 Enterprise 권한을 사용하지 않는 경우 이 필드는 선택 사항이며 필수가 아닙니다.
1. In **[!UICONTROL Additional decision parameters]**, specify the mapping between the fields defined in the Adobe Target segments and the Adobe Campaign fields.

   사용된 Adobe Campaign 필드가 rawbox에 지정되어 있어야 합니다. 여기서는 수신자의 성별에 따라 다른 경험을 정의할 것입니다.

   ![](assets/tar_additional_decisionning_parameters.png)

1. 이메일을 미리 보면 다른 프로필을 선택할 때 Adobe Target 활동 및 Adobe Campaign에 지정된 매개 변수에 따라 이미지가 삽입되는 방식이 달라집니다.

이제 동적 이미지가 포함된 게재를 보낼 수 있습니다. Adobe Target에서 해당 결과를 찾을 수 있습니다.

**관련 항목:**

* [Adobe Target 포털](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html)
* [이메일 컨텐츠 디자인 정보](../../designing/using/about-email-content-design.md)
* [실시간](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 비디오에서 이메일 이미지 개인화

