---
title: Campaign-Experience Manager 통합 기본 정보
description: Adobe Experience Manager 통합을 사용하면 AEM에서 직접 컨텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ff94f69b-3036-4103-a841-6b85feb0eb7e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 1%

---

# Campaign-Experience Manager 통합 기본 정보{#integrating-with-experience-manager}

Adobe Campaign Standard과 Adobe Experience Manager 간의 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 콘텐츠를 사용할 수 있습니다.

따라서 Adobe Campaign의 게재 및 데이터 관리 기능은 물론 Adobe Experience Manager 콘텐츠 편집 기능을 최대한 활용할 수 있습니다. Adobe Experience Manager에서 가져온 콘텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard은 Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 및 6.5와 호환됩니다. 다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 [구성](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html) 그리고 [사용](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html) 섹션에 있는 마지막 항목이 될 필요가 없습니다.

>[!NOTE]
>
> Adobe Experience Manager 6.5에서는 Adobe Campaign Standard 템플릿을 더 이상 사용할 수 없습니다.

## Campaign-Experience Manager 통합 사용 팁 {#tips-aem}

* **통합에 사용할 템플릿 확인**

   이메일 템플릿은 Adobe Experience Manager 내에서 편집할 수 있으므로 Adobe Experience Manager에서 모든 템플릿을 편집하는 것이 더 쉽습니다. 그러나 특정 템플릿은 쉽게 수용되지 않습니다. 한 고객별 개인화된 템플릿은 이 통합에 권장되지 않으며 Adobe Campaign Standard에서 직접 편집해야 합니다.

   템플릿에 대한 자세한 내용은 다음을 참조하십시오 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).

* **구현 중에 Externalizer가 구성되어 있는지 확인합니다.**

   Adobe Campaign Standard에 대한 Experience Manager을 구현하는 동안 Externalizer를 구성하면 리소스 경로를 URL로 변환할 수 있습니다. 이렇게 하면 페이지에서 이미지를 볼 수 있습니다. Externalizer가 제대로 구성되지 않으면 전자 메일에 손상된 이미지가 포함됩니다.

   Externalizer를 구성하는 방법에 대해 알아보려면 다음을 참조하십시오 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/externalizer.html).

* **오용을 방지하기 위해 이메일 템플릿을 구성합니다.**

   템플릿을 구성하면 적절한 템플릿이 적절한 폴더에 있고 실수로 잘못된 템플릿을 선택하지 않을 수 있습니다. 구현 중에 올바른 위치에 템플릿을 저장하도록 경로를 만들어야 합니다.

   템플릿에 대한 자세한 내용은 다음을 참조하십시오 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html#template-availability).

* **기본 구성 요소를 사용하여 빠르게 시작하십시오.**

   Adobe Experience Manager for Adobe Campaign Standard의 기본 구성 요소를 사용하면 템플릿이 복잡하지 않은 경우 빠르게 시작할 수 있습니다.
Experience Manager에는 사용을 시작할 수 있는 7개의 기본 구성 요소가 있습니다.

   * 제목
   * 이미지
   * 링크
   * Scene7 이미지 템플릿
   * 타깃팅된 참조
   * 텍스트 및 이미지
   * 텍스트 및 개인화

* **전자 메일 HTML은 웹 HTML과 다릅니다**

   이메일 템플릿에 웹 컨텐츠에 사용되는 것과 동일한 구성 요소를 사용할 수 없음을 이해하는 것이 중요합니다. 기본 구성 요소를 사용하면 구성 요소가 이메일 호환이 되도록 합니다.

* **템플릿에서 컨텐츠 연결을 해제하고 다시 사용합니다.**

   Campaign Standard에서 이메일을 설정하고 Experience Manager 템플릿을 선택할 때 다른 캠페인에 아직 연결되어 있지 않은 이메일만 선택할 수 있습니다. 그렇지 않으면 한 캠페인과 새로 고침에 대해 Adobe Experience Manager의 콘텐츠를 변경하는 경우 실수로 다른 캠페인의 콘텐츠에 영향을 줄 수 있습니다.
이를 방지하려면 템플릿 사용을 마치면 연결을 해제하여 다시 사용할 수 있습니다. 템플릿을 선택하고 **[!UICONTROL Delete the link with Adobe Experience Manager content]**.

* **Adobe Experience Manager을 사용하여 Adobe Campaign Standard용 이메일의 변형을 만듭니다.**

   이 통합을 사용하면 하나의 이메일을 세그멘테이션을 사용하여 여러 버전으로 쉽게 변환할 수 있습니다.
Adobe Experience Manager에서 세그멘테이션을 설정하는 방법과 타깃팅된 컨텐츠로 이메일을 만드는 방법을 알아보려면 이 문서를 참조하십시오 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem).

* **성공적으로 동기화되려면 Experience Manager의 세그먼트 이름이 Campaign의 세그먼트 이름과 정확히 일치해야 합니다.**
