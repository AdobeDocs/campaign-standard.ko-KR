---
title: 푸시 알림 보고서
description: 푸시 알림 기본 제공 보고서를 사용하여 푸시 알림의 성공에 대해 알아봅니다.
audience: reporting
content-type: reference
topic-tags: list-of-reports
feature: Reporting
role: Leader
level: Intermediate
exl-id: acfe0b9c-77a4-46ad-8151-7bf9c21fa4b0
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# 푸시 알림 보고서{#push-notification-report}

>[!CAUTION]
>
>배달 유형에 따라 데이터를 분할하려면(이 경우 푸시 알림 게재) **[!UICONTROL Message type]** 지표를 테이블에 끌어다 놓아야 합니다.

**푸시 알림** 보고서는 Adobe Campaign에서 푸시 알림의 마케팅 성과에 대한 세부 정보를 제공합니다. 이 기본 보고서는 사용자가 푸시 알림, 모바일 애플리케이션 및 게재와 상호 작용하는 방법을 이해하는 데 도움이 됩니다.

푸시 추적을 구현하려면 모바일 애플리케이션에서 일부 구성이 필요합니다. 자세한 단계는 이 [page](../../administration/using/push-tracking.md) 를 참조하십시오.

![](assets/dynamic_report_push.png)

각 표는 요약 번호와 차트로 표시됩니다. 각 시각화 설정에 세부 정보가 표시되는 방식을 변경할 수 있습니다.

첫 번째 테이블 **푸시 알림 참여 요약**&#x200B;은(는) 다음 세 가지 카테고리로 분할됩니다. 일별, 모바일 앱 및 게재별. 여기에는 게재에 대한 수신자 재활동을 위해 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Processed/sent]**: 전송된 총 푸시 알림 수.
* **[!UICONTROL Delivered]**: 전송된 총 푸시 알림 수와 관련하여 성공적으로 전송된 푸시 알림 수입니다.
* **[!UICONTROL Impressions]**: 푸시 알림이 장치에 전달되고 알림 센터에 그대로 남아 있는 횟수입니다. 대부분의 경우 노출 횟수 번호는 전달된 번호와 유사해야 합니다. 이렇게 하면 장치가 메시지를 수신하여 해당 정보를 서버로 다시 전달할 수 있습니다.
* **[!UICONTROL Unique impressions]**: 수신자별 노출 횟수.
* **[!UICONTROL Click through rate]**: 푸시 알림과 상호 작용한 사용자의 비율입니다.
* **[!UICONTROL Open rate]**: 열린 푸시 알림의 비율입니다.

![](assets/dynamic_report_push_2.png)

두 번째 테이블 **푸시 알림 클릭 및 열기**&#x200B;는 다음 세 가지 카테고리로 분할됩니다. 일별, 모바일 앱 및 게재별. 여기에는 게재당 수신자 동작에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Impressions]**: 수신자가 본 푸시 알림의 총수입니다.
* **[!UICONTROL Unique impressions]**: 수신자별 노출 횟수.
* **[!UICONTROL Click]**: 푸시 알림이 장치에 전달되고 사용자가 클릭한 횟수입니다. 사용자가 알림을 보려 했습니다. 이 알림이 푸시 열기 추적으로 이동되거나 해지됩니다.
* **[!UICONTROL Unique clicks]**: 고유 사용자가 푸시 알림과 상호 작용하는 횟수(예: 알림 또는 단추 클릭).
* **[!UICONTROL Open]**: 장치에 배달되고 사용자가 클릭했던 총 푸시 알림 수로 인해 앱이 열립니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하고 푸시 클릭과 유사합니다.
* **[!UICONTROL Unique Opens]**: 게재를 연 수신자 수입니다.
