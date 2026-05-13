---
title: Campaign-Analytics 통합 구성
description: 이메일 게재의 성공 측정을 시작하도록 Adobe Analytics 통합을 구성하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a6748b4b-36c5-4961-a599-ace73a8504cc
TQID: https://experienceleague.adobe.com/bt1FQbafwhEuRao-YFhynO-ecg5EaiUDskSFvxuFv-k
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
subfeature_v2: id: ca3c1dd6-bdd2-41a9-bc5a-e35f5cca9e63
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 228
ht-degree: 10%

---

# Campaign-Analytics 통합 구성{#configure-campaign-analytics-integration}

이 통합을 통해 주요 성능 지표 데이터를 Adobe Campaign에서 Adobe Analytics Standard 또는 Premium으로 직접 공유할 수 있습니다.

Adobe Campaign Standard과 Adobe Analytics 간의 통합을 시작하려면 먼저 Adobe Analytics에 연결된 외부 계정을 구성해야 합니다.

외부 계정 및 기술 워크플로우는 플랫폼의 기능 관리자만 관리할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration > Application settings > External accounts]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Share KPIs with Adobe Analytics]** 외부 계정을 선택하십시오.

   ![](assets/analytics_2.png)

1. **[!UICONTROL Connection]** 필드에 **[!UICONTROL Web services user name]** 및 **[!UICONTROL Web services share secret]**&#x200B;을(를) 지정합니다.

   이러한 매개 변수는 **[!UICONTROL Admin > Company settings > Web services]**&#x200B;을(를) 선택하여 Analytics에서 찾을 수 있습니다.

   ![](assets/analytics_1.png)

1. **[!UICONTROL Refresh report suites]** 버튼을 클릭합니다.
1. **[!UICONTROL Analytics default report suite]** 드롭다운에서 Adobe Campaign 데이터로 보강할 Adobe Analytics 보고서 세트를 선택합니다.

   이제 외부 계정이 준비되었으며 Adobe Analytics에 연결됩니다. 언제든지 **[!UICONTROL Enabled]** 상자를 선택하여 비활성화할 수 있습니다.

   ![](assets/analytics.png)

이제 **[!UICONTROL Share KPIs with Adobe Analytics]** 기술 워크플로우가 자동으로 시작되며 **[!UICONTROL Administration > Application settings > Workflow]**&#x200B;을(를) 선택하여 고급 메뉴에서 볼 수 있습니다. 이 기술 워크플로우는 최대 6개월 된 브로드로그를 유지할 수 있습니다. 이 워크플로우는 증분 워크플로우이며 전날의 데이터를 푸시합니다.

![](assets/analytics_3.png)

이제 Adobe Analytics에서 데이터를 사용할 수 있습니다.

**관련 항목:**

* [외부 계정](../../administration/using/external-accounts.md)
* [기술 워크플로](../../administration/using/technical-workflows.md)
* [통합 Campaign 보고를 위한 KPI 공유](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 비디오
