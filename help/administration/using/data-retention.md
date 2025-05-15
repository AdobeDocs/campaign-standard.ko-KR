---
title: 데이터 유지
description: 표준 표의 기본 보존 값에 대해 알아보기
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
source-git-commit: 2bc6ce04d2580b561bfdaafe29985353fd116a42
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 5%

---

# 데이터 유지{#data-retention}

>[!NOTE]
>
>데이터 보고는 지난 2년 동안만 사용할 수 있습니다. 데이터 보존 기간에 대한 자세한 내용은 Adobe 컨설턴트 또는 기술 관리자에게 문의하십시오.

Campaign의 표준 로그 테이블에는 사전 설정된 보존 기간이 있어 시스템 오버로드를 방지하기 위해 데이터 저장 기간을 제한합니다.

데이터 보존 구성은 구현 중에 Adobe 기술 관리자가 설정하며 고객 요구 사항에 따라 각 구현마다 값이 달라질 수 있습니다.

Adobe 컨설턴트 또는 기술 관리자에게 문의하여 환경에 적용되는 유지 기간에 대해 자세히 알아보거나 사용자 지정 유지 기간을 설정하십시오.

표준 워크플로우 기능을 사용하면 모든 사용자 정의 테이블에 대해 보존 기간을 설정할 수 있습니다.

다음은 표준 표의 기본 보존 기간입니다. 가능하면 데이터 사용에 따라 Adobe에서는 Campaign 인스턴스의 성능을 개선하기 위해 권장 유지 기간으로 이동하는 것을 권장합니다.

* **통합 추적**: 6개월(권장: 1개월)
* **게재 로그**: 6개월(권장: 1개월)
* **추적 로그**: 6개월(권장: 1개월)
* **이벤트**: 1개월
* **이벤트 처리 통계**: 6개월(권장: 1개월)
* **보관된 이벤트**: 6개월(권장: 1개월)
* **임시 엔터티**: 7일
* **무시된 파이프라인 이벤트**: 1개월
* **게재 경고**: 1개월
* **감사 내보내기**: 6개월(권장: 1개월)
* **게재**: 2년

## 게재 유지 기간 {#deliveries}

<!-- By default, the retention period for deliveries is unlimited.-->

2025년 6월 1일부터 지난 2년 동안의 게재만 시스템에서 계속 사용할 수 있습니다. 자세한 내용은 아래에서 확인할 수 있습니다.

* 2년 이상 된 모든 게재는 영구적으로 제거되며 더 이상 액세스할 수 없습니다.
* 이 정리에는 전송 및 실패한 게재만 포함됩니다. 반복 게재, 초안 게재 및 템플릿은 영향을 받지 않습니다.
* 게재가 제거되면 연결된 모든 추적 또는 전송 정보도 영구적으로 삭제됩니다.
* 마케팅 또는 트랜잭션 게재 템플릿은 삭제되지 않습니다.
* 반복 게재의 경우 합산 기간이 월 또는 년으로 설정된 하위 게재는 삭제되지 않습니다.

**[!UICONTROL Copy headers from delivery templates]** 워크플로와 같은 프로세스 속도를 높이려는 경우 게재 유지 기간을 줄일 수 있습니다. 이렇게 하려면 Adobe 담당자에게 문의하십시오.

<!--

However, if there is a high volume of deliveries on your instance, you can update the **NmsCleanup_DeliveryPurgeDelay** option available from the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** menu.

Each time the **[!UICONTROL Database cleanup]** workflow is run, the deliveries meeting the conditions set for this option will be deleted.

-->

<!--

When updating the **NmsCleanup_DeliveryPurgeDelay** option, it is recommended to proceed gradually with multiple iterations. For example, you can start by setting the value to 300 days, then 180 days, then 120 days, and so on - making sure iterations are at least 2 days apart. Otherwise, the **[!UICONTROL Database cleanup]** workflow may take much longer because of a large number of deliveries to delete.

This action can help speeding up processes such as the **[!UICONTROL Copy headers from delivery templates]** workflow. Learn more on technical workflows in [this section](technical-workflows.md).

The default value for the **NmsCleanup_DeliveryPurgeDelay** option is `-1`. In this case, no delivery is deleted.

For example, if you set it to `180`, any non-template deliveries that have not been updated in the last 180 days will be deleted when the **[!UICONTROL Database cleanup]** workflow is run.

-->


