---
title: Adobe Experience Manager에서 이메일 콘텐츠 만들기.
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
source-git-commit: 5c1a540475b7d93c18c957243ee2a403b8154aa3

---


# Adobe Experience Manager에서 이메일 콘텐츠 만들기 {#creating-email-aem}

Adobe Campaign Standard와 Adobe Experience Manager의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 콘텐츠를 사용할 수 있습니다.

이 사용 사례는 Adobe Experience Manager에서 이메일 컨텐츠를 만드는 방법을 보여줍니다.

## 사전 요구 사항 {#prerequisites}

다음 요소가 미리 있는지 확인해야 합니다.

* Adobe Experience Manager **제작** 인스턴스
* Adobe Experience Manager **게시** 인스턴스
* Adobe Campaign 인스턴스

## 구성 {#configuration}

이 두 솔루션을 함께 사용하려면 서로 연결하도록 구성해야 합니다.

1. Adobe Campaign 구성을 참조하십시오. 이렇게 하려면:

   * Adobe Experience Manager 유형 외부 계정을 구성합니다.
   * Adobe Campaign용 Adobe Experience Manager에서 만든 콘텐츠 유형을 인식하는 옵션을 **[!UICONTROL AEMResourceTypeFilter]**구성합니다.
   * Adobe Experience Manager 콘텐츠임을 지정하는 이메일 템플릿을 만들고 이전에 만든 외부 계정을 이 템플릿에 연결합니다.

1. Adobe Experience Manager 구성 이렇게 하려면:

   * Adobe Experience Manager 작성 및 게시 인스턴스 간 복제를 구성합니다.
   * 전용 구성을 통해 Adobe Experience Manager를 Adobe Campaign에 연결할 수 **[!UICONTROL Cloud Service]**있습니다.

## Adobe Experience Manager에서 이메일 콘텐츠 만들기 {#use-case}

Adobe Experience Manager에서 이메일 컨텐츠를 만들려면

1. Adobe Campaign용으로 특별히 작성된 템플릿을 사용하여 이메일 컨텐츠를 만듭니다.
1. 컨텐츠 속성에서 Adobe Campaign 인스턴스에 **[!UICONTROL Cloud Service]**해당하는 항목을 선택합니다.
1. 텍스트, 이미지, 개인화 등을 삽입하여 컨텐츠를 편집합니다.
1. 컨텐츠의 유효성을 확인합니다.

자세한 내용은 [자세한 설명서를](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)참조하십시오.

![](assets/aem_content.png)

Adobe Campaign에서 컨텐츠를 검색하려면

1. Adobe Experience Manager 유형 콘텐츠 템플릿을 기반으로 이메일을 만듭니다.
1. Adobe Campaign 이메일 컨텐츠 정의 화면을 사용하여 Adobe Experience Manager로 제작한 컨텐츠를 연결합니다.

![](assets/aem_linked_content.png)

