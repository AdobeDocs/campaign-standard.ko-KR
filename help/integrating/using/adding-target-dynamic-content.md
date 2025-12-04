---
title: Target 다이내믹 콘텐츠 추가
description: Adobe Campaign 게재 중 하나에서 Adobe Target 다이내믹 콘텐츠를 추가하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 7dfbd89f-877e-4598-bfe3-d743bb31ae9e
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 3%

---

# Target 다이내믹 콘텐츠 추가{#adding-target-dynamic-content}

Adobe Target 통합을 통해 다이내믹 이미지를 게재에 추가하여 경험에 따라 콘텐츠를 개인화할 수 있습니다.

이메일을 편집하는 동안 수신자에 따라 변경될 Adobe Target의 동적 이미지를 삽입할 수 있습니다.

Adobe Campaign에서 이미지에 액세스하려면 먼저 Adobe Target에서 다음 작업을 수행해야 합니다.

* 사용할 이미지의 URL을 지정해야 하는 [리디렉션 오퍼](https://experienceleague.adobe.com/docs/target/using/experiences/offers/offer-redirect.html?lang=ko)를 하나 이상 만듭니다.
* 하나 또는 여러 개의 [대상](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=ko)을 만들어 활동 대상을 정의합니다.
* [양식 기반 경험 작성기](https://experienceleague.adobe.com/docs/target/using/experiences/form-experience-composer.html?lang=ko) 활동을 만듭니다. 이 활동에서는 만든 리디렉션 오퍼의 수에 따라 rawbox를 선택하고 여러 경험을 지정해야 합니다. 각 경험에 대해 만들어진 리디렉션 오퍼 중 하나를 선택해야 합니다.
* Adobe Campaign의 정보를 사용하여 세그먼트를 만들고 경험을 지정합니다. 오퍼의 선택 규칙에 Adobe Campaign의 데이터를 사용하려면 Adobe Target의 rawbox에 데이터를 지정해야 합니다.

1. 이메일 게재를 만듭니다.
1. 전자 메일 또는 랜딩 페이지의 콘텐츠를 편집할 때 이미지 블록으로 이동한 다음 상황별 메뉴를 통해 **[!UICONTROL Dynamic image from Adobe Target]**&#x200B;을(를) 선택합니다.

   ![](assets/tar_insert_dynamic_image.png)

1. 이메일에 기본적으로 표시될 이미지를 선택합니다. 이미지 URL을 직접 지정하거나 [Assets](../../integrating/using/working-with-campaign-and-assets-core-service.md)을 통해 공유되는 이미지를 선택할 수 있습니다.

   통합은 정적 이미지만 지원합니다. 나머지 콘텐츠는 사용자 지정할 수 없습니다.

1. Adobe Target에 지정된 rawbox 이름을 입력합니다.
1. Adobe Target의 설정에서 Enterprise 권한을 사용하는 경우 이 필드에 해당 속성을 추가합니다. [이 페이지](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/properties-overview.html?lang=ko)에서 Target Enterprise 권한에 대해 자세히 알아보세요. 이 필드는 선택 사항이며 Target에서 Enterprise 권한을 사용하지 않는 경우에는 필수가 아닙니다.
1. **[!UICONTROL Additional decision parameters]**&#x200B;에서 Adobe Target 세그먼트에 정의된 필드와 Adobe Campaign 필드 간의 매핑을 지정합니다.

   사용된 Adobe Campaign 필드는 rawbox에 지정했어야 합니다. 이 예에서는 수신자의 성별에 따라 다른 경험을 정의합니다.

   ![](assets/tar_additional_decisionning_parameters.png)

1. 다른 프로필을 선택할 때 삽입된 이미지가 Adobe Target 활동 및 Adobe Campaign에 지정된 매개 변수에 따라 변경되는지 보려면 전자 메일을 미리 봅니다.

이제 동적 이미지가 포함된 게재를 보낼 수 있습니다. 그 결과는 Adobe Target에서 찾을 수 있습니다.

**관련 항목:**

* [Adobe Target 포털](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=ko)
* [이메일 콘텐츠 디자인 정보](../../designing/using/designing-content-in-adobe-campaign.md)
* [실시간으로 이메일 이미지 개인화](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 비디오
