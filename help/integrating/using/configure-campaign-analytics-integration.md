---
title: Campaign-Analytics 통합 구성
description: 이메일 게재의 성공 측정을 시작하도록 Adobe Analytics 통합을 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: a6748b4b-36c5-4961-a599-ace73a8504cc
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 9%

---

# Campaign-Analytics 통합 구성{#configure-campaign-analytics-integration}

이 통합을 통해 주요 성능 지표 데이터를 Adobe Campaign에서 Adobe Analytics Standard 또는 Premium으로 직접 공유할 수 있습니다.

Adobe Campaign Standard과 Adobe Analytics 간의 통합을 시작하려면 먼저 Adobe Analytics에 연결된 외부 계정을 구성해야 합니다.

외부 계정 및 기술 워크플로우는 플랫폼의 기능 관리자만 관리할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration > Application settings > External accounts]** 을 선택합니다.
1. **[!UICONTROL Share KPIs with Adobe Analytics]** 외부 계정을 선택합니다.

   ![](assets/analytics_2.png)

1. **[!UICONTROL Connection]** 필드에 **[!UICONTROL Web services user name]** 및 **[!UICONTROL Web services share secret]**&#x200B;을 지정합니다.

   이러한 매개 변수는 **[!UICONTROL Admin > Company settings > Web services]** 을 선택하여 Analytics에서 찾을 수 있습니다.

   ![](assets/analytics_1.png)

1. **[!UICONTROL Refresh report suites]** 버튼을 클릭합니다.
1. Adobe Campaign 데이터로 보강할 Adobe Analytics 보고서 세트의 **[!UICONTROL Analytics default report suite]** 드롭다운에서 을 선택합니다.

   이제 외부 계정을 준비하여 Adobe Analytics에 연결합니다. **[!UICONTROL Enabled]** 상자를 선택하여 언제든지 비활성화할 수 있습니다.

   ![](assets/analytics.png)

이제 **[!UICONTROL Share KPIs with Adobe Analytics]** 기술 워크플로우가 자동으로 시작되며 **[!UICONTROL Administration > Application settings > Workflow]** 을 선택하여 고급 메뉴에서 볼 수 있습니다. 이 기술 워크플로우는 15분마다 자동으로 실행되며 Adobe Analytics의 최대 6개월 이전 데이터를 푸시합니다.

![](assets/analytics_3.png)

이제 Adobe Analytics에서 데이터를 사용할 수 있습니다.

**관련 항목:**

* [외부 계정](../../administration/using/external-accounts.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [통합 Campaign 보고를 위한 KPI ](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 공유 비디오
