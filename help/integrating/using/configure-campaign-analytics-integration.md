---
title: 캠페인 분석 통합 구성
seo-title: 캠페인 분석 통합 구성
description: 캠페인 분석 통합 구성
seo-description: 이메일 게재 성공 측정을 시작하도록 Adobe Analytics 통합을 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: BDAA 00 B 0-7445-469 C -8268-9 D 06 C 53 CE 2 B 0
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: Working-with-campaign-and-analytics
discoiquuid: 92 B 9004 C-CBA 0-41 FD-A 035-32 BEE 1 D 6 A 42 C
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Configure Campaign-Analytics integration{#configure-campaign-analytics-integration}

이러한 통합을 통해 주요 성능 지표 데이터를 Adobe Campaign에서 Adobe Analytics Standard 또는 Premium로 바로 공유할 수 있습니다.

Adobe Campaign Standard와 Adobe Analytics 간의 통합을 시작하려면 먼저 Adobe Analytics에 연결된 외부 계정을 구성해야 합니다.

외부 계정 및 기술 워크플로우는 플랫폼의 기능 관리자만 관리할 수 있습니다.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration > Application settings > External accounts]**.
1. Select the **[!UICONTROL Share KPIs with Adobe Analytics]** external account.

   ![](assets/analytics_2.png)

1. Specify your **[!UICONTROL Web services user name]** and **[!UICONTROL Web services share secret]** in the **[!UICONTROL Connection]** field.

   These parameters can be found in Analytics by selecting **[!UICONTROL Admin > Company settings > Web services]**.

   ![](assets/analytics_1.png)

1. **[!UICONTROL Refresh report suites]** 단추를 클릭합니다.
1. Select in the **[!UICONTROL Analytics default report suite]** drop-down the Adobe Analytics report suite you want to enrich with Adobe Campaign data.

   이제 외부 계정이 준비되고 Adobe Analytics와 연결됩니다. You can disable it at any time by checking the **[!UICONTROL Enabled]** box.

   ![](assets/analytics.png)

**[!UICONTROL Share KPIs with Adobe Analytics]** 기술 워크플로우는 이제 자동으로 실행되며, 선택하면 고급 메뉴에서 볼 **[!UICONTROL Administration > Application settings > Workflow]**&#x200B;수 있습니다. 이 기술 워크플로우는 15 분마다 자동으로 실행되며 Adobe Analytics에서 최대 6 개월 이전 데이터로 푸시됩니다.

![](assets/analytics_3.png)

이제 Adobe Analytics에서 데이터를 사용할 수 있습니다.

**관련 항목:**

* [외부 계정](../../administration/using/external-accounts.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [통합 캠페인 보고](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html) 비디오에 KPI 공유

