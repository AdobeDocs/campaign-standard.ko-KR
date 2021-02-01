---
solution: Campaign Standard
product: campaign
title: Campaign-Experience Manager 통합 구성
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 컨텐츠를 제작하여 Adobe Campaign에서 나중에 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
translation-type: tm+mt
source-git-commit: 3672f0bc4ebc551c4eb34660a3a55d44fa726f1a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 3%

---


# Campaign-Experience Manager 통합 구성 {#configuration-aem}

Adobe Campaign Standard과 Adobe Experience Manager 간의 이러한 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 컨텐츠를 사용할 수 있습니다.

이 사용 사례에서는 Adobe Experience Manager에서 이메일 컨텐츠를 만들고 관리하는 방법을 알아보고, 마케팅 캠페인에 사용할 수 있도록 이메일을 Adobe Campaign Standard으로 가져옵니다.

## 사전 요구 사항 {#prerequisites}

다음 요소가 미리 있는지 확인해야 합니다.

* Adobe Experience Manager **authoring** 인스턴스
* Adobe Experience Manager **게시** 인스턴스
* Adobe Campaign 인스턴스

## Adobe Campaign Standard {#config-acs}의 구성

이 두 솔루션을 함께 사용하려면 두 솔루션을 서로 연결하도록 구성해야 합니다.
Adobe Campaign을 구성하려면:

1. 먼저 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL External accounts menu]**&#x200B;에서 **[!UICONTROL Adobe Experience Manager instance]** 외부 계정을 구성해야 합니다.

1. **[!UICONTROL Server]** URL, **[!UICONTROL Account]** 및 **[!UICONTROL Password]**&#x200B;을(를) 사용하여 Adobe Experience Manager 유형 외부 계정을 구성합니다.

   ![](assets/aem_1.png)

1. **[!UICONTROL AEMResourceTypeFilter]** 옵션이 올바르게 구성되었는지 확인하십시오. **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** 메뉴 아래의 **[!UICONTROL Options]** 메뉴에 액세스합니다.

1. **[!UICONTROL Value (text)]** 필드에서 다음 구문이 올바른지 확인하십시오.

   ```
   mcm/campaign/components/newsletter,mcm/campaign/components/campaign_newsletterpage,mcm/neolane/components/newsletter
   ```

   ![](assets/aem_2.png)

1. 그런 다음 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]** 아래의 고급 메뉴에서 기존 템플릿 중 하나를 복제하여 Adobe Experience Manager 전용 이메일 템플릿을 만듭니다.

   ![](assets/aem_3.png)

1. **[!UICONTROL Edit properties]** 아이콘을 클릭합니다.

   ![](assets/aem_4.png)

1. **[!UICONTROL Content]** 드롭다운 아래의 **[!UICONTROL Content source]** 필드에서 **[!UICONTROL Adobe Experience Manager]**&#x200B;을 선택한 다음 **[!UICONTROL Adobe Experience Manager account]**&#x200B;에서 이전에 만든 외부 계정을 선택합니다.

이제 Adobe Experience Manager에서 통합을 구성해야 합니다.

## Adobe Experience Manager {#config-aem}의 구성

Adobe Campaign Standard을 사용하여 Adobe Experience Manager을 구성하려면 다음 단계를 따라야 합니다.

1. 먼저 Adobe Experience Manager 작성 및 게시 인스턴스 간 복제를 구성해야 합니다. 이 [섹션](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#configuring-adobe-experience-manager)을 참조하십시오.

1. 그런 다음 전용 **[!UICONTROL Cloud Service]**&#x200B;을 구성하여 Adobe Experience Manager을 Adobe Campaign에 연결합니다. 이 [섹션](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#connecting-aem-to-adobe-campaign)을 참조하십시오.

1. 이제 작성 인스턴스에서 Adobe Experience Manager의 externalizer를 구성해야 합니다. 이 [섹션](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#configuring-the-externalizer)을 참조하십시오.

