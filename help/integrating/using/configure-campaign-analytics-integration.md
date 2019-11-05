---
title: Campaign-Analytics 통합 구성
description: Adobe Analytics 통합을 구성하여 이메일 전달의 성공 측정을 시작하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: bdaa00b0-7445-469c-8268-9d06c53ce2b0
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: 92b9004c-cba0-41fd-a035-32bee1d6a42c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Campaign-Analytics 통합 구성{#configure-campaign-analytics-integration}

이 통합을 통해 주요 성능 지표 데이터를 Adobe Campaign에서 Adobe Analytics Standard 또는 Premium으로 직접 공유할 수 있습니다.

Adobe Campaign Standard와 Adobe Analytics 간의 통합을 시작하려면 먼저 Adobe Analytics에 연결된 외부 계정을 구성해야 합니다.

외부 계정 및 기술 워크플로우는 플랫폼의 기능 관리자만 관리할 수 있습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 선택합니다 **[!UICONTROL Administration > Application settings > External accounts]**.
1. 외부 계정을 **[!UICONTROL Share KPIs with Adobe Analytics]** 선택합니다.

   ![](assets/analytics_2.png)

1. 및 를 **[!UICONTROL Web services user name]** **[!UICONTROL Web services share secret]** **[!UICONTROL Connection]** 필드에 지정합니다.

   이러한 매개 변수는 Analytics에서 선택하여 찾을 수 **[!UICONTROL Admin > Company settings > Web services]**&#x200B;있습니다.

   ![](assets/analytics_1.png)

1. 단추를 **[!UICONTROL Refresh report suites]** 클릭합니다.
1. Adobe Campaign 데이터로 보완할 Adobe Analytics 보고서 세트 **[!UICONTROL Analytics default report suite]** 드롭다운에서 선택합니다.

   이제 외부 계정이 준비되고 Adobe Analytics와 연결됩니다. 이 **[!UICONTROL Enabled]** 상자를 선택하면 언제든지 비활성화할 수 있습니다.

   ![](assets/analytics.png)

이제 **[!UICONTROL Share KPIs with Adobe Analytics]** 기술 워크플로우가 자동으로 실행되고 고급 메뉴에서 선택하여 볼 수 **[!UICONTROL Administration > Application settings > Workflow]**&#x200B;있습니다. 이 기술 워크플로우는 15분마다 자동으로 실행되며 Adobe Analytics에서 최대 6개월 이전 데이터를 푸시합니다.

![](assets/analytics_3.png)

이제 Adobe Analytics에서 데이터를 사용할 수 있습니다.

**관련 항목:**

* [외부 계정](../../administration/using/external-accounts.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [통합 캠페인 보고를](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 위한 KPI 공유 비디오

