---
title: Campaign-Experience Manager 통합 정보
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 컨텐츠를 제작하고 나중에 Adobe Campaign에서 사용할 수 있습니다.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 85f4d6d7ea4bdf63505bb2c8b586de3a10073345

---


# Campaign-Experience Manager 통합 정보{#integrating-with-experience-manager}

Adobe Campaign Standard와 Adobe Experience Manager의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 콘텐츠를 사용할 수 있습니다.

따라서 Adobe Experience Manager 컨텐츠 편집 기능은 물론 Adobe Campaign의 전달 및 데이터 관리 기능을 활용할 수 있습니다.

>[!NOTE]
>
>Adobe Experience Manager에서 가져온 콘텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard는 Adobe Experience Manager 6.1, 6.2, 6.3 및 6.4와 호환됩니다.다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 [구성](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) 전용 섹션 및 통합 [사용을](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html) 참조하십시오.

## Campaign-Experience Manager 통합 사용 방법에 대한 팁 {#tips-aem}

* **통합에 사용할 템플릿 파악**

   이메일 템플릿은 Adobe Experience Manager에서 편집할 수 있으므로 Adobe Experience Manager에서 템플릿을 보다 손쉽게 편집할 수 있습니다. 그러나 특정 템플릿은 쉽게 수용되지 않습니다. 한 고객에게만 제공되는 개별 템플릿은 이 통합에 권장되지 않으며 Adobe Campaign Standard에서 직접 편집해야 합니다.

   템플릿에 대한 자세한 내용은 이 [페이지를](https://docs.adobe.com/content/help/en/experience-manager-64/developing/platform/templates/templates.html)참조하십시오.

* **구현 중에 Externalizer가 구성되어 있는지 확인합니다.**

   Adobe Campaign Standard용 Experience Manager를 구현하는 동안 Externalizer를 구성하면 리소스 경로를 URL로 변환할 수 있습니다. 이렇게 하면 페이지에서 이미지를 볼 수 있습니다. Externalizer가 제대로 구성되지 않으면 이메일에 손상된 이미지가 포함됩니다.

   Externalizer 구성 방법에 대한 자세한 내용은 이 [페이지를 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-64/developing/platform/externalizer.html)

* **오용되지 않도록 이메일 템플릿을 구성할 수 있습니다.**

   템플릿을 체계적으로 유지하면 해당 템플릿이 적절한 폴더에 있고 실수로 잘못된 템플릿을 선택하지 않을 수 있습니다. 구현 중에 올바른 위치에 템플릿을 저장하려면 경로를 만들어야 합니다.

   템플릿에 대한 자세한 내용은 이 [페이지를 참조하십시오.](https://docs.adobe.com/content/help/en/experience-manager-64/developing/platform/templates/templates.html#template-availability)

* **즉시 사용 가능한 구성 요소를 사용하여 빠르게 시작할 수 있습니다.**

   Adobe Campaign Standard용 Adobe Experience Manager의 기본 구성 요소를 사용하면 템플릿이 복잡하지 않은 경우 신속하게 시작할 수 있습니다.
Adobe Experience Manager에는 즉시 사용할 수 있는 7개의 구성 요소가 포함되어 있습니다.
   1. 제목
   1. 이미지
   1. 링크
   1. Scene7 이미지 템플릿
   1. 타깃팅된 참조
   1. 텍스트 및 이미지
   1. 텍스트 및 개인화

* **이메일용 HTML은 웹용 HTML과 다릅니다.**

   이메일 템플릿에 웹 컨텐츠에 사용된 것과 동일한 구성 요소를 사용할 수 없다는 것을 이해하는 것이 중요합니다. 즉시 사용 가능한 구성 요소를 사용하면 구성 요소가 이메일과 호환됩니다.

* **템플릿에서 컨텐츠 연결을 해제하고 다시 사용할 수 있습니다.**

   Campaign Standard에서 이메일을 설정하고 Experience Manager 템플릿을 선택할 때 아직 다른 캠페인에 연결되어 있지 않은 이메일만 선택할 수 있습니다. 그렇지 않으면 Adobe Experience Manager에서 한 캠페인의 콘텐츠를 변경하고 새로 고치면 의도치 않게 다른 캠페인의 콘텐츠에 영향을 줄 수 있습니다.
이를 방지하려면 템플릿 사용을 완료하면 연결을 해제하여 다시 사용할 수 있습니다. 템플릿을 선택하고 클릭하면 **[!UICONTROL Delete the link with Adobe Experience Manager content]**됩니다.

* **Adobe Experience Manager를 사용하여 Adobe Campaign Standard에 대한 다양한 이메일 만들기**

   이러한 통합을 통해 하나의 이메일을 여러 버전으로 손쉽게 전환할 수 있습니다.
Adobe Experience Manager에서 세그멘테이션을 설정하는 방법과 타깃팅된 컨텐츠로 이메일을 만드는 방법에 대해 알아보려면 이 [페이지를](https://docs.adobe.com/help/en/experience-manager-64/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem)참조하십시오.

* **성공적으로 동기화하려면 Experience Manager의 세그먼트 이름이 Campaign의 세그먼트 이름과 정확히 일치해야 합니다.**