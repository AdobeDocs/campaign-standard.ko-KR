---
title: Campaign-Experience Manager 통합 기본 정보
description: Adobe Experience Manager 통합을 통해 AEM에서 직접 콘텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: ff94f69b-3036-4103-a841-6b85feb0eb7e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---

# Campaign-Experience Manager 통합 기본 정보{#integrating-with-experience-manager}

Adobe Campaign Standard과 Adobe Experience Manager 간의 이러한 통합을 통해 Adobe Experience Manager에서 만든 콘텐츠를 Adobe Campaign 이메일에 사용할 수 있습니다.

따라서 Adobe Campaign의 게재 및 데이터 관리 기능과 Adobe Experience Manager 콘텐츠 편집 기능을 최대한 활용할 수 있습니다. Adobe Experience Manager에서 가져온 콘텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard은 Adobe Experience Manager 6.1, 6.2, 6.3, 6.4 및 6.5와 호환됩니다. 다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 통합의 [구성](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html) 및 [사용](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)에 대한 섹션을 참조하십시오.

>[!NOTE]
>
> Adobe Campaign Standard 템플릿은 Adobe Experience Manager 6.5에서 더 이상 사용할 수 없습니다.

## 캠페인-Experience Manager 통합 사용 방법에 대한 팁 {#tips-aem}

* **통합에 사용할 템플릿 파악**

  이메일 템플릿은 Adobe Experience Manager 내에서 편집할 수 있으므로 Adobe Experience Manager에서 모든 템플릿을 편집하는 것이 더 쉬워 보일 수 있습니다. 그러나 특정 템플릿은 쉽게 수용되지 않습니다. 한 고객에게만 해당하는 개별화된 템플릿은 이 통합에 권장되지 않으며 Adobe Campaign Standard에서 직접 편집해야 합니다.

  템플릿에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html)를 참조하세요.

* **구현 중에 외부화가 구성되었는지 확인**

  Adobe Campaign Standard에 대한 Experience Manager을 구현하는 동안 외부화를 구성하면 리소스 경로를 URL로 변환할 수 있습니다. 이미지를 페이지에 표시할 수 있습니다. 외부화가 제대로 구성되지 않은 경우 이메일에 손상된 이미지가 포함됩니다.

  외부화를 구성하는 방법에 대해 알아보려면 이 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/externalizer.html)를 참조하세요.

* **오용을 방지하려면 전자 메일 템플릿을 구성하세요.**

  템플릿을 체계적으로 관리하면 해당 템플릿이 해당 폴더에 저장되어 실수로 잘못된 템플릿을 선택하지 않을 수 있습니다. 구현 중에 템플릿을 올바른 위치에 저장하도록 경로를 만들어야 합니다.

  템플릿에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html#template-availability)를 참조하세요.

* **기본 구성 요소를 빠르게 시작하십시오.**

  템플릿이 복잡하지 않은 경우 Adobe Experience Manager for Adobe Campaign Standard의 기본 구성 요소를 사용하여 빠르게 시작할 수 있습니다.
Experience Manager에는 사용을 시작할 수 있는 7가지 기본 구성 요소가 있습니다.

   * 제목
   * 이미지
   * 링크
   * Scene7 이미지 템플릿
   * 타깃팅된 참조
   * 텍스트 및 이미지
   * 텍스트 및 Personalization

* **전자 메일 HTML이 웹용 HTML과 다릅니다**

  이메일 템플릿에 웹 컨텐츠에 사용된 것과 동일한 구성 요소를 사용할 수 없다는 것을 이해하는 것이 중요합니다. 기본 구성 요소를 사용하면 구성 요소가 이메일 호환성이 보장됩니다.

* **템플릿에서 콘텐츠를 연결 해제하고 다시 사용합니다.**

  Campaign Standard에서 이메일을 설정하고 Experience Manager 템플릿을 선택할 때는 아직 다른 캠페인에 연결되지 않은 캠페인만 선택할 수 있습니다. 그렇지 않으면 한 캠페인에 대해 Adobe Experience Manager의 콘텐츠를 변경하고 새로 고치는 경우 다른 캠페인의 콘텐츠에 의도하지 않게 영향을 줄 수 있습니다.
이를 방지하기 위해 템플릿 사용이 완료되면 연결을 해제하여 다시 사용할 수 있습니다. 템플릿을 선택하고 **[!UICONTROL Delete the link with Adobe Experience Manager content]**&#x200B;을(를) 클릭하면 됩니다.

* **Adobe Experience Manager을 사용하여 Adobe Campaign Standard에 대한 다양한 전자 메일을 만듭니다.**

  이 통합을 사용하면 세분화를 통해 하나의 이메일을 여러 버전으로 쉽게 전환할 수 있습니다.
Adobe Experience Manager에서 세그먼테이션을 설정하는 방법과 타겟팅된 콘텐츠로 이메일을 만드는 방법에 대해 알아보려면 이 [페이지](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/target-adobe-campaign.html#setting-up-segmentation-in-aem)를 참조하세요.

* **동기화하려면 Experience Manager의 세그먼트 이름이 Campaign 정확한 세그먼트 이름과 일치해야 합니다.**
