---
title: 추적된 URL 정보
seo-title: 추적된 URL 정보
description: 추적된 URL 정보
seo-description: 추적할 컨텐츠의 모든 URL를 관리하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: DFE 5146 B -5256-431 C -87 B 3-3 C 54817 EBA 36
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 관리 링크
discoiquuid: D 9 B 0 B 3 C 2-874 B -4 CB 4-BCE 9-C 0194 A 19 F 25 F
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# About tracked URLs{#about-tracked-urls}

Adobe Campaign를 사용하면 이메일에 포함된 URL를 클릭하면 수신자의 행동을 추적할 수 있습니다. For more on tracking, see [this section](../../sending/using/tracking-messages.md#about-tracking).

The **[!UICONTROL Links]** icon in the action bar automatically displays the list of all the URLs of your content that will be tracked.

![](assets/des_links.png)

>[!NOTE]
>
>추적이 기본적으로 활성화됩니다. 이 기능은 Adobe Campaign에서 추적이 활성화된 경우 이메일에만 사용할 수 있습니다. For more on the tracking parameters, refer to [this section](../../administration/using/configuring-email-channel.md#tracking-parameters).

각 링크의 URL, 범주, 레이블 및 추적 유형은 이 목록에서 수정할 수 있습니다. 링크를 편집하려면 해당 연필 아이콘을 클릭합니다.

![](assets/des_links_tracking.png)

추적된 각 URL에 대해 추적 모드를 다음 값 중 하나로 설정할 수 있습니다.

* **추적됨: 이 URL에 대한 추적을 활성화합니다.**
* **미러 페이지**: 이 URL를 미러 페이지 URL로 간주합니다.
* ****&#x200B;절대 안 함: 이 URL에 대한 추적을 활성화하지 않습니다. 이 정보는 저장됩니다. URL 이 이후 메시지에서 다시 나타나면 해당 추적이 자동으로 비활성화됩니다.
* **옵트아웃: 이 URL를 옵트아웃 또는 구독 취소 URL로 간주합니다.**

![](assets/des_link_tracking_type.png)

각 URL에 대한 추적을 비활성화하거나 활성화할 수도 있습니다.

>[!NOTE]
>
>By default in Adobe Campaign, all content URLs are tracked except **Mirror page URL** and **Unsubscription** link.

You can regroup your URLs by editing the **[!UICONTROL Category]** field, depending on the URLs used in the message. These categories can be displayed reports, as for example in [URLs and click streams](../../reporting/using/urls-and-click-streams.md).

![](assets/des_link_tracking_category.png)

When building a report, from the **[!UICONTROL Components]** tab, select **[!UICONTROL Dimension]** and scroll down the list to access the tracking components. For example, drag and drop **[!UICONTROL Tracking URL Category]** into the workspace to display results according to the tracking category of each clicked URL.

![](assets/des_link_tracking_report.png)

For more on building customized reports, see [this section](../../reporting/using/about-dynamic-reports.md).
