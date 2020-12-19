---
solution: Campaign Standard
product: campaign
title: Campaign-Experience Manager 통합 기본 정보
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 컨텐츠를 제작하여 Adobe Campaign에서 나중에 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---


# Campaign-Experience Manager 통합 기본 정보{#integrating-with-experience-manager}

Adobe Campaign Standard과 Adobe Experience Manager 간의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 컨텐츠를 사용할 수 있습니다.

따라서 Adobe Campaign의 전달 및 데이터 관리 기능은 물론 Adobe Experience Manager 컨텐츠 편집 기능을 최대한 활용할 수 있습니다. Adobe Experience Manager에서 가져온 내용에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard은 Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 및 6.5와 호환됩니다. 다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 [configuration](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html)에 대한 전용 섹션 및 [통합의 ](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)사용 섹션을 참조하십시오.

>[!NOTE]
>
> Adobe Experience Manager 6.5에서는 Adobe Campaign Standard 템플릿을 더 이상 사용할 수 없습니다.

## 캠페인 Experience Manager 통합 사용 방법에 대한 팁 {#tips-aem}

* **통합에 사용할 템플릿 확인**

   이메일 템플릿은 Adobe Experience Manager 내에서 편집할 수 있으므로 Adobe Experience Manager에서 템플릿을 편집하기가 더 쉽습니다. 그러나 특정 템플릿이 쉽게 수용되지는 않습니다. 한 고객만 사용할 수 있는 개별 템플릿은 이 통합에 권장되지 않으며 Adobe Campaign Standard에서 직접 편집해야 합니다.

   템플릿에 대한 자세한 내용은 이 [페이지](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html)를 참조하십시오.

* **구현 중에 Externalizer가 구성되어 있는지 확인합니다.**

   Adobe Campaign Standard에 대한 Experience Manager을 구현하는 동안 Externalizer를 구성하면 리소스 경로를 URL로 변환할 수 있습니다. 이렇게 하면 페이지에 이미지를 볼 수 있습니다. Externalizer가 제대로 구성되지 않으면 이메일에 손상된 이미지가 포함됩니다.

   Externalizer 구성 방법에 대해 알려면 이 [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/externalizer.html)을 참조하십시오.

* **오용되지 않도록 이메일 템플릿을 구성할 수 있습니다.**

   템플릿을 체계적으로 유지하면 적절한 템플릿이 적절한 폴더에 있고 실수로 잘못된 템플릿을 선택하지 않을 수 있습니다. 구현 중에 적절한 위치에 템플릿을 저장하려면 경로를 만들어야 합니다.

   템플릿에 대한 자세한 내용은 이 [페이지](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html#template-availability)를 참조하십시오.

* **즉시 사용 가능한 구성 요소를 사용하여 빠르게 시작할 수 있습니다.**

   Adobe Campaign Standard용 Adobe Experience Manager의 기본 구성 요소를 사용하면 템플릿이 복잡하지 않은 경우 빠르게 시작할 수 있습니다.
Experience Manager에는 바로 사용할 수 있는 7개의 구성 요소가 있습니다.

   * 머리글
   * 이미지
   * 링크
   * Scene7 이미지 템플릿
   * 대상 참조
   * 텍스트 및 이미지
   * 텍스트 및 개인화

* **이메일용 HTML은 웹용 HTML과 다릅니다.**

   이메일 템플릿에 웹 컨텐츠에 사용된 것과 동일한 구성 요소를 사용할 수 없음을 이해하는 것이 중요합니다. 즉시 사용 가능한 구성 요소를 사용하면 구성 요소가 이메일 호환되도록 할 수 있습니다.

* **템플릿에서 컨텐츠 연결을 해제하고 다시 사용할 수 있습니다.**

   Campaign Standard에서 이메일을 설정하고 Experience Manager 템플릿을 선택할 때 다른 캠페인에 아직 연결되지 않은 이메일만 선택할 수 있습니다. 그렇지 않으면 한 캠페인의 Adobe Experience Manager 컨텐츠를 변경하고 새로 고치면 의도치 않게 다른 캠페인의 컨텐츠에 영향을 줄 수 있습니다.
이를 방지하려면 템플릿 사용을 완료하면 연결을 해제하여 다시 사용할 수 있습니다. 템플릿을 선택하고 **[!UICONTROL Delete the link with Adobe Experience Manager content]**&#x200B;만 클릭하면 됩니다.

* **Adobe Experience Manager을 사용하여 Adobe Campaign Standard용 다양한 이메일을 만들 수 있습니다.**

   이러한 통합을 통해 하나의 이메일을 여러 버전으로 손쉽게 전환할 수 있습니다.
Adobe Experience Manager에서 세그멘테이션을 설정하는 방법과 타깃팅된 컨텐츠로 이메일을 만드는 방법에 대해 알려면 이 [페이지](https://docs.adobe.com/help/en/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem)를 참조하십시오.

* **성공적으로 동기화하려면 Experience Manager의 세그먼트 이름이 캠페인의 세그먼트 이름과 정확히 일치해야 합니다.**