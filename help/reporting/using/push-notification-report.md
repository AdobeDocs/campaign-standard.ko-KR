---
title: 푸시 알림 보고서
seo-title: 푸시 알림 보고서
description: 푸시 알림 보고서
seo-description: 푸시 알림 즉시 사용 가능한 보고서를 통해 푸시 알림의 성공 여부를 확인할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 5 B 121 A 37-1 C 09-4749-A 409-6989978 DDC 4 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: list-of-reports
discoiquuid: A 425 CD 59-EDFD -42 C 5-A 6 BD -38773 C 353 FF 0
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 7102ed308f94985f8924a13aab2583e50b6c68e4

---


# Push notification report{#push-notification-report}

>[!CAUTION]
>
>Please note that you have to drag and drop the **[!UICONTROL Message type]** metrics to your tables to split your data depending on your delivery types, in this case push notification deliveries.

**푸시 알림** 보고서는 Adobe Campaign에서 푸시 알림의 마케팅 성과에 대한 세부 정보를 제공합니다. 이 즉시 사용 가능한 보고서에서는 사용자가 푸시 알림, 모바일 애플리케이션 및 전달을 어떻게 이용하고 있는지 이해하는 데 도움이 됩니다.

Some configuration is required in the mobile application to implement push tracking, refer to this [page](https://helpx.adobe.com/campaign/kb/push-tracking.html) for the detailed steps.

![](assets/dynamic_report_push.png)

각 표는 요약 번호와 차트로 표시됩니다. 각 시각화 설정에 세부 사항이 표시되는 방식을 변경할 수 있습니다.

The first table **Push notification Engagement Summary** is split into three categories: by day, by mobile app and by delivery. 여기에는 수신자 재활동에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Processed/sent]**: 전송된 총 푸시 알림 수입니다.
* **[!UICONTROL Delivered]**: 전송된 푸시 알림의 총 수와 관련하여 성공적으로 전송된 푸시 알림 수입니다.
* **[!UICONTROL Impressions]**: 푸시 알림이 장치로 배달되고 알림 센터에서 변경되지 않은 횟수입니다. 대부분의 경우 노출 수는 배달된 번호와 비슷해야 합니다. 이렇게 하면 장치가 메시지를 받아서 해당 정보를 서버로 다시 전송합니다.
* **[!UICONTROL Unique impressions]**: 수령인별 노출 횟수.
* **[!UICONTROL Click through rate]**: 푸시 알림과 상호 작용한 사용자의 비율입니다.
* **[!UICONTROL Open rate]**: 열린 푸시 알림의 비율.

![](assets/dynamic_report_push_2.png)

The second table **Push notification Clicks &amp; opens** is split into three categories: by day, by mobile app and by delivery. 여기에는 배달당 수신자 행동에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Impressions]**: 수신자가 볼 수 있는 푸시 알림의 합계입니다.
* **[!UICONTROL Unique impressions]**: 수령인별 노출 횟수.
* **[!UICONTROL Click]**: 푸시 알림이 장치에 전달되고 사용자가 클릭한 횟수입니다. 사용자는 알림을 보고, 이 알림을 통해 푸시 열기 추적을 푸시하거나, 페이지를 닫습니다.
* **[!UICONTROL Unique clicks]**: 고유 사용자가 푸시 알림과 상호 작용하는 횟수 (예: 알림이나 단추 클릭)
* **[!UICONTROL Open]**: 장치에 배달되고 사용자가 클릭해서 앱을 여는 총 푸시 알림 수입니다. 이것은 알림이 닫혔을 경우 푸시 열기 외에는 푸시 클릭이 트리거되지 않습니다.
* **[!UICONTROL Unique Opens]**: 배달을 연 수신자 수입니다.

