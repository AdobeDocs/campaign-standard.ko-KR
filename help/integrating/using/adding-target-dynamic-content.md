---
title: Target 다이내믹 콘텐츠 추가
description: Adobe Campaign 게재 중 하나에서 Adobe Target 동적 컨텐츠를 추가하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: b3cc045f-7924-480e-8c61-8246510f3adb
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-target
discoiquuid: 45ddf7b7-98f7-4fdd-bb4a-49ec8490e877
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Target 다이내믹 콘텐츠 추가{#adding-target-dynamic-content}

Adobe Target과의 통합을 통해 동적 이미지를 전달에 추가하여 경험에 따라 콘텐츠를 개인화할 수 있습니다.

이메일을 편집하는 동안 수신자에 따라 변경되는 Adobe Target의 동적 이미지를 삽입할 수 있습니다.

Adobe Campaign에서 이미지에 액세스하려면 먼저 Adobe Target에서 다음 작업을 수행해야 합니다.

* 사용할 이미지의 URL을 지정해야 하는 하나 이상의 [리디렉션 오퍼를](https://docs.adobe.com/content/help/en/target/using/experiences/offers/offer-redirect.html)만듭니다.
* 하나 또는 여러 [대상을](https://marketing.adobe.com/resources/help/en_US/target/ov/c_about_segments.html)만들어 활동 대상을 정의합니다.
* 양식 [기반 경험 작성기](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html) 활동을 만듭니다. 이 활동을 만들려면 rawbox를 선택하고 생성된 리디렉션 오퍼 수에 따라 여러 경험을 지정해야 합니다. 각 경험에 대해 생성된 리디렉션 오퍼 중 하나를 선택해야 합니다.
* Adobe Campaign의 정보를 사용하여 세그먼트를 만들어 경험을 지정합니다. 오퍼의 선택 규칙에서 Adobe Campaign의 데이터를 사용하려면 Adobe Target의 rawbox에 데이터를 지정해야 합니다.

1. 이메일 배달 만들기
1. 이메일 또는 랜딩 페이지의 컨텐츠를 편집할 때 이미지 블록으로 이동한 다음 컨텍스트 메뉴를 **[!UICONTROL Dynamic image from Adobe Target]** 통해 선택합니다.

   ![](assets/tar_insert_dynamic_image.png)

1. 이메일에 기본적으로 표시되는 이미지를 선택합니다. 이미지 URL을 직접 지정하거나 자산을 통해 공유된 이미지를 선택할 수 [있습니다](../../integrating/using/working-with-campaign-and-assets-core-service.md).

   통합은 정적 이미지만 지원합니다. 나머지 컨텐츠는 사용자 정의할 수 없습니다.

1. Adobe Target에 지정된 rawbox의 이름을 입력합니다.
1. Adobe Target의 설정에서 Enterprise 권한을 사용하는 경우 이 필드에 해당 속성을 추가합니다. 이 [페이지에서](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html)Target Enterprise 권한에 대해 자세히 알아보십시오. 이 필드는 선택 사항이며 Target에서 엔터프라이즈 권한을 사용하지 않는 경우 필수가 아닙니다.
1. 에서 **[!UICONTROL Additional decision parameters]** Adobe Target 세그먼트에 정의된 필드와 Adobe Campaign 필드 간의 매핑을 지정합니다.

   사용된 Adobe Campaign 필드는 rawbox에 지정되어 있어야 합니다. 여기에서 우리는 받는 사람의 성별에 따라 다른 경험을 정의할 것입니다.

   ![](assets/tar_additional_decisionning_parameters.png)

1. 다른 프로필을 선택할 때 삽입된 이미지가 Adobe Target 활동 및 Adobe Campaign에 지정된 매개 변수에 따라 변경되었는지 확인하기 위해 이메일을 미리 봅니다.

이제 동적 이미지가 포함된 배달을 보낼 수 있습니다. 결과는 Adobe Target에서 찾을 수 있습니다.

**관련 항목:**

* [Adobe Target 포털](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html)
* [이메일 컨텐츠 디자인 정보](../../designing/using/overview.md)
* [실시간 비디오로 이메일 이미지](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 개인화

