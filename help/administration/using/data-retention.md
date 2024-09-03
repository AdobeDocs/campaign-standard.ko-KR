---
title: 데이터 유지
description: 표준 표의 기본 보존 값에 대해 알아보기
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
source-git-commit: 99c092bc40c9176a25a6ec2a164ee1d3f85d5cbe
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 4%

---

# 데이터 유지{#data-retention}

>[!NOTE]
>
>데이터 보고는 지난 3년 동안만 사용할 수 있습니다. 데이터 보존 기간에 대한 자세한 내용은 Adobe 컨설턴트 또는 기술 관리자에게 문의하십시오.

Campaign의 표준 로그 테이블에는 사전 설정된 보존 기간이 있어 시스템 오버로드를 방지하기 위해 데이터 저장 기간을 제한합니다.

데이터 보존 구성은 구현 중에 Adobe 기술 관리자가 설정하며 고객 요구 사항에 따라 각 구현마다 값이 달라질 수 있습니다.

Adobe 컨설턴트 또는 기술 관리자에게 문의하여 환경에 적용되는 보존 기간에 대해 자세히 알아보거나 사용자 지정 보존 기간을 설정하십시오.

표준 워크플로우 기능을 사용하면 모든 사용자 정의 테이블에 대해 보존 기간을 설정할 수 있습니다.

다음은 표준 표의 기본 보존 기간입니다. 가능하면 데이터 사용에 따라 Adobe은 Campaign 인스턴스의 성능을 개선하기 위해 권장 유지 기간으로 이동하는 것을 권장합니다.

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

## 게재 유지 기간 {#deliveries}

기본적으로 게재의 보존 기간은 무제한입니다.

그러나 인스턴스에 게재 양이 많은 경우 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** 메뉴에서 사용할 수 있는 **NmsCleanup_DeliveryPurgeDelay** 옵션을 업데이트할 수 있습니다.

**[!UICONTROL Database cleanup]** 워크플로우를 실행할 때마다 이 옵션에 대해 설정된 조건을 충족하는 게재가 삭제됩니다.

이 작업은 **[!UICONTROL Copy headers from delivery templates]** 워크플로와 같은 프로세스 속도를 높이는 데 도움이 될 수 있습니다.

>[!NOTE]
>
>기술 워크플로우에 대한 자세한 내용은 [이 섹션](technical-workflows.md)을 참조하세요.


**NmsCleanup_DeliveryPurgeDelay** 옵션의 기본값은 `-1`입니다. 이 경우 게재가 삭제되지 않습니다.

예를 들어 `180`(으)로 설정하면 **[!UICONTROL Database cleanup]** 워크플로우를 실행할 때 지난 180일 동안 업데이트되지 않은 모든 비템플릿 게재가 삭제됩니다.

>[!NOTE]
>
>* 마케팅 또는 트랜잭션 게재 템플릿은 삭제되지 않습니다.
>
>* 반복 게재의 경우 합산 기간이 월 또는 년으로 설정된 하위 게재는 삭제되지 않습니다.

**NmsCleanup_DeliveryPurgeDelay** 옵션을 업데이트할 때 여러 번 반복하는 것이 좋습니다. 예를 들어 값을 300일, 180일, 120일 등으로 설정하여 반복이 최소 2일 간격으로 유지되도록 할 수 있습니다. 그렇지 않으면 삭제할 게재가 많기 때문에 **[!UICONTROL Database cleanup]** 워크플로가 훨씬 오래 걸릴 수 있습니다.

