---
title: 푸시 알림 보고서
description: 푸시 알림의 기본 보고서를 통해 푸시 알림의 성공에 대해 알아봅니다.
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
>을(를) 끌어다 놓아야 합니다. **[!UICONTROL Message type]** 테이블에 지표를 추가하여 게재 유형에 따라 데이터를 분할합니다(이 경우 푸시 알림 게재).

다음 **푸시 알림** 보고서는 Adobe Campaign에서 푸시 알림의 마케팅 성능에 대한 세부 정보를 제공합니다. 이 기본 보고서는 사용자가 푸시 알림, 모바일 애플리케이션 및 게재와 상호 작용하는 방법을 이해하는 데 도움이 됩니다.

푸시 추적을 구현하려면 모바일 애플리케이션에서 일부 구성이 필요합니다. 다음을 참조하십시오. [페이지](../../administration/using/push-tracking.md) 을 참조하십시오.

![](assets/dynamic_report_push.png)

각 테이블은 요약 번호와 차트로 표시됩니다. 세부 사항이 각각의 시각화 설정에 표시되는 방식을 변경할 수 있습니다.

첫 번째 테이블 **푸시 알림 참여 요약** 는 일별, 모바일 앱별 및 게재별 세 가지 카테고리로 나뉩니다. 여기에는 게재에 대한 수신자 반응성에 사용 가능한 데이터가 포함됩니다.

* **[!UICONTROL Processed/sent]**: 전송된 총 푸시 알림 수입니다.
* **[!UICONTROL Delivered]**: 전송된 총 푸시 알림 수와 관련하여 성공적으로 전송된 푸시 알림 수입니다.
* **[!UICONTROL Impressions]**: 푸시 알림이 장치에 전달되고 알림 센터에 그대로 남아 있는 횟수입니다. 대부분의 경우 노출 횟수는 게재된 횟수와 유사해야 합니다. 이렇게 하면 장치가 메시지를 받고 해당 정보를 서버에 다시 전달했는지 확인할 수 있습니다.
* **[!UICONTROL Unique impressions]**: 수신자별 노출 횟수.
* **[!UICONTROL Click through rate]**: 푸시 알림과 상호 작용한 사용자의 비율입니다.
* **[!UICONTROL Open rate]**: 열린 푸시 알림의 백분율입니다.

![](assets/dynamic_report_push_2.png)

두 번째 테이블 **푸시 알림 클릭 및 열기** 는 일별, 모바일 앱별 및 게재별 세 가지 카테고리로 나뉩니다. 여기에는 게재당 수신자 동작에 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL Impressions]**: 수신자가 본 총 푸시 알림 수입니다.
* **[!UICONTROL Unique impressions]**: 수신자별 노출 횟수.
* **[!UICONTROL Click]**: 푸시 알림이 디바이스에 전달되고 사용자가 클릭한 횟수 사용자는 푸시 오픈 추적으로 이동될 알림을 보거나 닫으려고 했습니다.
* **[!UICONTROL Unique clicks]**: 고유 사용자가 푸시 알림과 상호 작용하는 횟수(예: 알림 또는 버튼 클릭)
* **[!UICONTROL Open]**: 장치에 전달되고 사용자가 클릭하여 앱을 여는 총 푸시 알림 수입니다. 알림이 해제된 경우 푸시 열기 가 트리거되지 않는다는 점을 제외하면 푸시 클릭과 유사합니다.
* **[!UICONTROL Unique Opens]**: 게재를 연 수신자 수.
