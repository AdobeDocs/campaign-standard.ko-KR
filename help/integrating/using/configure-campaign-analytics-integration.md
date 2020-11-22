---
solution: Campaign Standard
product: campaign
title: Campaign-Analytics 통합 구성
description: 이메일 배달의 성공 측정을 시작하도록 Adobe Analytics 통합을 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 9%

---


# Campaign-Analytics 통합 구성{#configure-campaign-analytics-integration}

이 통합을 통해 주요 성능 지표 데이터를 Adobe Campaign에서 Adobe Analytics Standard 또는 Premium으로 직접 공유할 수 있습니다.

Adobe Campaign Standard과 Adobe Analytics 간의 통합을 시작하려면 먼저 Adobe Analytics에 연결된 외부 계정을 구성해야 합니다.

외부 계정 및 기술 워크플로우는 플랫폼의 기능 관리자만 관리할 수 있습니다.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration > Application settings > External accounts]**.
1. Select the **[!UICONTROL Share KPIs with Adobe Analytics]** external account.

   ![](assets/analytics_2.png)

1. 필드 **[!UICONTROL Web services user name]** 에서 및 **[!UICONTROL Web services share secret]** 을 **[!UICONTROL Connection]** 지정합니다.

   이러한 매개 변수는 Analytics를 선택하여 찾을 수 있습니다 **[!UICONTROL Admin > Company settings > Web services]**.

   ![](assets/analytics_1.png)

1. **[!UICONTROL Refresh report suites]** 버튼을 클릭합니다.
1. Adobe Analytics 보고서 세트 **[!UICONTROL Analytics default report suite]** 드롭다운에서 Adobe Campaign 데이터로 보완할 요소를 선택합니다.

   이제 외부 계정이 준비가 되어 Adobe Analytics에 연결되어 있습니다. 이 **[!UICONTROL Enabled]** 상자를 선택하면 언제든지 비활성화할 수 있습니다.

   ![](assets/analytics.png)

이제 **[!UICONTROL Share KPIs with Adobe Analytics]** 기술 워크플로우가 자동으로 실행되고 고급 메뉴에서 선택하여 볼 수 있습니다 **[!UICONTROL Administration > Application settings > Workflow]**. 이 기술 워크플로우는 15분마다 자동으로 실행되며 Adobe Analytics에서 최대 6개월 이전의 데이터를 전송할 것입니다.

![](assets/analytics_3.png)

이제 Adobe Analytics에서 데이터를 이용할 수 있습니다.

**관련 항목:**

* [외부 계정](../../administration/using/external-accounts.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [통합 캠페인 보고](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 비디오를 위한 KPI 공유

