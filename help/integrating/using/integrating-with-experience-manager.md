---
title: Experience Manager와 통합 사용
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 컨텐츠를 제작하고 나중에 Adobe Campaign에서 사용할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Experience Manager와 통합 사용{#integrating-with-experience-manager}

Adobe Campaign Standard와 Adobe Experience Manager의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 콘텐츠를 사용할 수 있습니다.

따라서 Adobe Experience Manager 컨텐츠 편집 기능은 물론 Adobe Campaign의 전달 및 데이터 관리 기능을 활용할 수 있습니다.

>[!NOTE]
>
>Adobe Experience Manager에서 가져온 콘텐츠에 대해서는 A/B 테스트를 수행할 수 없습니다.

Adobe Campaign Standard는 Adobe Experience Manager 6.1, 6.2, 6.3 및 6.4와 호환됩니다.다음 섹션에서는 실행할 수 있는 작업에 대한 개요를 제공합니다. 자세한 내용은 [구성](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) 전용 섹션 및 통합 [사용을](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html) 참조하십시오.

## 사전 요구 사항 {#prerequisites}

다음 요소가 미리 있는지 확인해야 합니다.

* Adobe Experience Manager **제작** 인스턴스
* Adobe Experience Manager **게시** 인스턴스
* Adobe Campaign 인스턴스

## 사용 사례 {#use-case}

Adobe Experience Manager에서 이메일 컨텐츠를 만들려면

1. Adobe Campaign용으로 특별히 작성된 템플릿을 사용하여 이메일 컨텐츠를 만듭니다.
1. 컨텐츠 속성에서 Adobe Campaign 인스턴스에 **[!UICONTROL Cloud Service]** 해당하는 항목을 선택합니다.
1. 텍스트, 이미지, 개인화 등을 삽입하여 컨텐츠를 편집합니다.
1. 컨텐츠의 유효성을 확인합니다.

자세한 내용은 [자세한 설명서를](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/campaign.html)참조하십시오.

![](assets/aem_content.png)

Adobe Campaign에서 컨텐츠를 검색하려면

1. Adobe Experience Manager 유형 콘텐츠 템플릿을 기반으로 이메일을 만듭니다.
1. Adobe Campaign 이메일 컨텐츠 정의 화면을 사용하여 Adobe Experience Manager로 제작한 컨텐츠를 연결합니다.

![](assets/aem_linked_content.png)

## 구성 {#configuration}

이 두 솔루션을 함께 사용하려면 서로 연결하도록 구성해야 합니다.

1. Adobe Campaign 구성을 참조하십시오. 이렇게 하려면:

   * Adobe Experience Manager 유형 외부 계정을 구성합니다.
   * Adobe Campaign **용 Adobe Experience** Manager에서 만든 콘텐츠 유형을 인식하는 AEMResourceTypeFilter 옵션을 구성합니다.
   * Adobe Experience Manager 콘텐츠임을 지정하는 이메일 템플릿을 만들고 이전에 만든 외부 계정을 이 템플릿에 연결합니다.

1. Adobe Experience Manager 구성 이렇게 하려면:

   * Adobe Experience Manager 작성 및 게시 인스턴스 간 복제를 구성합니다.
   * 전용 구성을 통해 Adobe Experience Manager를 Adobe Campaign에 연결할 수 **[!UICONTROL Cloud Service]**&#x200B;있습니다.

