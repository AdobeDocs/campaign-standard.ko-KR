---
title: Campaign-Experience Manager 통합 기본 정보
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 콘텐츠를 제작하고 나중에 Adobe Campaign에서 사용할 수 있습니다.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---


# Campaign-Experience Manager 통합 기본 정보{#integrating-with-experience-manager}

Adobe Campaign Standard과 Adobe Experience Manager 간의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 컨텐츠를 사용할 수 있습니다.

따라서 Adobe Campaign의 전달 및 데이터 관리 기능은 물론 Adobe Experience Manager 컨텐츠 편집 기능을 최대한 활용할 수 있습니다. Adobe Experience Manager에서 가져온 컨텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard은 Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 및 6.5와 호환됩니다. 다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 [구성](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html) 및 통합 [사용](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html) 전용 섹션을 참조하십시오.

>[!NOTE]
>
> Adobe Experience Manager 6.5에서는 더 이상 Adobe Campaign Standard 템플릿을 사용할 수 없습니다.

## 캠페인 Experience Manager 통합 사용 방법에 대한 팁 {#tips-aem}

* **통합에 사용할 템플릿 확인**

   이메일 템플릿은 Adobe Experience Manager에서 편집할 수 있으므로 Adobe Experience Manager에서 모든 템플릿을 보다 손쉽게 편집할 수 있습니다. 그러나 특정 템플릿은 쉽게 수용되지 않습니다. 이 통합에는 한 고객에게만 제공되는 개별 템플릿이 권장되지 않으며 Adobe Campaign Standard에서 직접 편집해야 합니다.

   For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html).

* **구현 중에 Externalizer가 구성되어 있는지 확인합니다.**

   Adobe Campaign Standard에 대한 Experience Manager을 구현하는 동안 Externalizer를 구성하면 리소스 경로를 URL로 변환할 수 있습니다. 이를 통해 페이지에 이미지를 표시할 수 있습니다. Externalizer가 제대로 구성되지 않은 경우 이메일에 손상된 이미지가 포함됩니다.

   Externalizer 구성 방법을 알려면 이 [페이지를 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/externalizer.html).

* **오용을 방지하기 위해 이메일 템플릿을 구성합니다.**

   템플릿을 체계적으로 유지하면 해당 템플릿이 적절한 폴더에 있으며 실수로 잘못된 템플릿을 선택하지 않을 수 있습니다. 구현 중에 올바른 위치에 템플릿을 저장하려면 경로를 만들어야 합니다.

   For more information on templates, refer to this [page](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/templates.html#template-availability).

* **즉시 사용 가능한 구성 요소를 사용하여 빠르게 시작할 수 있습니다.**

   Adobe Campaign Standard용 Adobe Experience Manager의 기본 구성 요소를 사용하면 템플릿이 복잡하지 않은 경우 빠르게 시작할 수 있습니다.
Experience Manager에 사용할 수 있는 7개의 기본 구성 요소가 있습니다.

   * 제목
   * 이미지
   * 링크
   * Scene7 이미지 템플릿
   * 타깃팅된 참조
   * 텍스트 및 이미지
   * 텍스트 및 개인화

* **이메일의 HTML은 웹용 HTML과 다릅니다.**

   이메일 템플릿에 웹 컨텐츠와 동일한 구성 요소를 사용할 수 없음을 이해하는 것이 중요합니다. 즉시 사용 가능한 구성 요소를 사용하면 구성 요소가 이메일과 호환됩니다.

* **템플릿에서 컨텐츠 연결 해제 및 재사용**

   Campaign Standard에서 이메일을 설정하고 Experience Manager 템플릿을 선택할 때 다른 캠페인에 아직 연결되어 있지 않은 이메일 하나만 선택할 수 있습니다. 그렇지 않으면 한 캠페인의 Adobe Experience Manager 컨텐츠를 변경하고 새로 고치면 의도치 않게 다른 캠페인의 컨텐츠에 영향을 줄 수 있습니다.
이를 방지하려면 템플릿 사용을 마치면 연결을 해제하여 다시 사용할 수 있습니다. 템플릿을 선택하고 클릭하면 됩니다 **[!UICONTROL Delete the link with Adobe Experience Manager content]**.

* **Adobe Experience Manager을 사용하여 Adobe Campaign Standard의 다양한 이메일을 만들 수 있습니다.**

   이러한 통합을 통해 하나의 이메일을 여러 버전으로 손쉽게 전환할 수 있습니다.
Adobe Experience Manager에서 세그멘테이션을 설정하는 방법과 타깃팅된 컨텐츠로 이메일을 만드는 방법에 대해 알아보려면 이 [페이지를 참조하십시오](https://docs.adobe.com/help/en/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem).

* **성공적으로 동기화하려면 Experience Manager의 세그먼트 이름이 캠페인의 세그먼트 이름과 정확히 일치해야 합니다.**