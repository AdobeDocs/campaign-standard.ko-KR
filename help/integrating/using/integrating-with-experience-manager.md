---
title: Experience Manager와 통합
seo-title: Experience Manager와 통합
description: Experience Manager와 통합
seo-description: Adobe Experience Manager 통합을 통해 AEM에서 직접 컨텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: ED 6 C 1 B 76-87 F 7-4 D 23-B 5 E 2-0765297 A 905 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6 C 0 C 3 C 5 B-B 596-459 E -87 DD-A 06 BB 7 D 633 D 2
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Integrating with Experience Manager{#integrating-with-experience-manager}

Adobe Campaign Standard와 Adobe Experience Manager 간의 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 컨텐츠를 사용할 수 있습니다.

따라서 Adobe Experience Manager 컨텐츠 편집 기능뿐만 아니라 Adobe Campaign의 전달 및 데이터 관리 기능도 활용할 수 있습니다.

>[!NOTE]
>
>Adobe Experience Manager에서 가져온 컨텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard는 Adobe Experience Manager 6.1, 6.2, 6.3 및 6.4와 호환됩니다. 다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. For more information, refer to the sections dedicated to [configuration](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) and the [use](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html) of the integration.

## Prerequisites {#prerequisites}

다음 요소를 미리 가지고 있어야 합니다.

* An Adobe Experience Manager **authoring** instance
* An Adobe Experience Manager **publishing** instance
* Adobe Campaign 인스턴스

## Use case {#use-case}

Adobe Experience Manager에서 이메일 콘텐츠를 만들려면:

1. Adobe Campaign 용으로 특별히 만든 템플릿을 사용하여 이메일 컨텐츠를 만듭니다.
1. In the content properties, select the **[!UICONTROL Cloud Service]** corresponding to your Adobe Campaign instance.
1. 텍스트, 이미지, 개인화 등을 삽입하여 컨텐츠를 편집합니다.
1. 내용의 유효성을 확인합니다.

For more information, refer to the [detailed documentation](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/campaign.html).

![](assets/aem_content.png)

Adobe Campaign에서 컨텐츠를 검색하려면:

1. Adobe Experience Manager 유형 컨텐츠 템플릿을 기반으로 이메일을 만듭니다.
1. Adobe Campaign 이메일 콘텐츠 정의 화면을 사용하여 Adobe Experience Manager로 만든 컨텐트를 링크합니다.

![](assets/aem_linked_content.png)

## Configuration {#configuration}

이러한 두 솔루션을 함께 사용하려면 서로 연결되도록 구성해야 합니다.

1. Adobe Campaign 구성을 참조하십시오. 이렇게 하려면:

   * Adobe Experience Manager Type External Account를 구성합니다.
   * Configure the **AEMResourceTypeFilter** option, which recognizes the content types created in Adobe Experience Manager for Adobe Campaign.
   * Adobe Experience Manager 컨텐츠임을 지정하는 이메일 템플릿을 만들고 이전에 만든 외부 계정을 이 템플릿에 연결합니다.

1. Adobe Experience Manager 구성을 참조하십시오. 이렇게 하려면:

   * Adobe Experience Manager 작성 및 게시 인스턴스 간 복제를 구성합니다.
   * Connect Adobe Experience Manager to Adobe Campaign by configuring a dedicated **[!UICONTROL Cloud Service]**.

