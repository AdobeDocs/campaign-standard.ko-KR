---
title: Campaign-Experience Manager 통합 구성
description: Adobe Experience Manager 통합을 사용하면 AEM에서 직접 컨텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: f56f5a19-6283-4eef-8127-c69a16a42a37
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 3%

---

# Campaign-Experience Manager 통합 구성 {#configuration-aem}

Adobe Campaign Standard과 Adobe Experience Manager 간의 통합을 통해 Adobe Campaign 이메일에서 Adobe Experience Manager에서 만든 콘텐츠를 사용할 수 있습니다.

이 사용 사례에서는 Adobe Experience Manager에서 이메일 콘텐츠를 만들고 관리하는 방법을 배웁니다. 그런 다음 마케팅 캠페인에서 전자 메일의 해당 콘텐츠를 Adobe Campaign Standard으로 가져와서 사용하는 방법을 알아봅니다.

## 필수 구성 요소 {#prerequisites}

미리 다음 요소가 있는지 확인해야 합니다.

* Adobe Experience Manager **작성** 인스턴스
* Adobe Experience Manager **게시** 인스턴스
* Adobe Campaign 인스턴스

## Adobe Campaign Standard의 구성 {#config-acs}

이 두 솔루션을 함께 사용하려면 서로 연결하도록 구성해야 합니다.
Adobe Campaign을 구성하려면:

1. 먼저 을 구성해야 합니다 **[!UICONTROL Adobe Experience Manager instance]** 외부 계정 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL External accounts menu]**.

1. 다음 아이콘을 사용하여 Adobe Experience Manager 유형 외부 계정을 구성합니다 **[!UICONTROL Server]** URL, **[!UICONTROL Account]** 및 **[!UICONTROL Password]**.

   ![](assets/aem_1.png)

1. 다음을 확인하십시오. **[!UICONTROL AEMResourceTypeFilter]** 옵션이 올바르게 구성되었습니다. 액세스 권한 **[!UICONTROL Options]** 메뉴 아래의 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 에서 **[!UICONTROL Value (text)]** 필드에서 다음 구문이 올바른지 확인합니다.

   ```
   mcm/campaign/components/newsletter,mcm/campaign/components/campaign_newsletterpage,mcm/neolane/components/newsletter
   ```

   ![](assets/aem_2.png)

1. 그런 다음 아래의 고급 메뉴에서 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**&#x200B;기존 템플릿 중 하나를 복제하여 Adobe Experience Manager과 관련된 이메일 템플릿을 만듭니다.

   ![](assets/aem_3.png)

1. 을(를) 클릭합니다. **[!UICONTROL Edit properties]** 아이콘.

   ![](assets/aem_4.png)

1. 아래에 **[!UICONTROL Content]** 드롭다운에서 을 선택합니다. **[!UICONTROL Adobe Experience Manager]** 에서 **[!UICONTROL Content source]** 필드에서 이전에 만든 외부 계정을 **[!UICONTROL Adobe Experience Manager account]**.

이제 Adobe Experience Manager에서 통합을 구성해야 합니다.

## Adobe Experience Manager의 구성 {#config-aem}

Adobe Campaign Standard으로 Adobe Experience Manager을 구성하려면 다음 단계를 수행해야 합니다.

1. 먼저 Adobe Experience Manager 작성 및 게시 인스턴스 간에 복제를 구성해야 합니다. 다음을 참조하십시오 [섹션](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html#configuring-adobe-experience-manager).

1. 그런 다음 전용 구성 을 통해 Adobe Experience Manager을 Adobe Campaign에 연결합니다 **[!UICONTROL Cloud Service]**. 다음을 참조하십시오 [섹션](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html#connecting-aem-to-adobe-campaign).

1. 이제 작성 인스턴스에서 Adobe Experience Manager에서 외부 도우미를 구성해야 합니다. 다음을 참조하십시오 [섹션](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html#configuring-the-externalizer).
