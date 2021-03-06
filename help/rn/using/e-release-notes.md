---
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 66aed3668dc0eb2041312dcbaebe7c36f54b13a5
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 100%

---

# 초기 릴리스 정보 {#new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 문제 해결에 대해 설명합니다.

>[!CAUTION]
>
> 이 콘텐츠는 단계 환경 업그레이드일까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하세요.

## 릴리스 22.2 - 2022년 6월 {#rn-2022}

**개선 사항**

* **Adobe 알림 서비스** - Campaign에는 Adobe 알림 서비스가 포함되어 있습니다. 이 서비스는 Experience Cloud 전반에 걸쳐 사용자가 알아야 할 중요한 활동에 대해 Experience Cloud 솔루션이 경고합니다. 22.2 버전부터 사용자 경험을 개선했습니다. 알림의 우선 순위가 지정되고 제품에서 생성한 알림이 Adobe 상태 알림과 분리됩니다. 또한 알림이 특정 워크플로우를 참조하는 경우 이제 이메일이나 제품 내 알림을 통해 직접 해당 워크플로우에 액세스할 수 있습니다.  Adobe Campaign 알림에 대한 자세한 내용은 [Adobe Campaign 알림](../../administration/using/sending-internal-notifications.md)을 참조하세요.

* **워크플로우 시작의 최적화** - Adobe는 동시에 시작되는 워크플로우 수를 세부 조정할 수 있는 새로운 기능을 추가했습니다. 이렇게 하면 서비스 중단이나 다운타임으로 이어질 수 있는 CPU 스파이크를 방지할 수 있습니다. Adobe은 22.2 릴리스 후에 이를 활성화합니다. 이와 관련하여 고객이 해야 할 조치 사항은 없습니다.

* **접근성** - Adobe는 애플리케이션의 전반적인 사용 편의성을 개선하기 위해 많은 접근성을 수정했습니다. 이러한 기능은 현재 얼리어답터 세트에만 활성화되어 있으며 ACS 22.3 릴리스에서 모든 고객에게 롤아웃될 예정입니다. 접근성 개선의 예는 다음과 같습니다.

   * 각 화면에 집중 가능한 요소에 대해 눈에 보이는 포커스 표시기가 있는지 확인합니다.
   * 보다 쉬운 탐색을 위해 페이지 랜드마크 만들기
   * 여러 컨트롤에 대한 이름, 역할, 값, 상태 추가
   * 기본 화면에서 동적 포커스 순서에서 발생하는 문제 해결


**패치**

* 중복 키 오류로 인해 청구 기술 워크플로우의 문제를 수정했습니다. (CAMP-51029)
* 추적 보고서에서 누락된 Microsoft Edge 브라우저 카테고리를 추가했습니다. 이 분류는 이전에 Microsoft Edge가 열릴 때 분류되었습니다. (CAMP-51165)
* 하위 테이블에서 데이터가 삭제되지 않는 GDPR 요청 문제를 수정했습니다. (CAMP-48276)
* 트랜잭션 메시지 템플릿에서 조각의 가시성 조건이 저장되지 않는 이메일 디자이너 문제를 해결했습니다. (CAMP-50338)
* 날짜 범위를 고려하지 않는 캠페인 보고서의 문제를 수정했습니다. (CAMP-50991)
* 예약된 이메일이 실패하는 오류를 수정했습니다. 게재가 여전히 &#39;다시 시도 보류 중&#39; 상태에 있으므로 게재 분석을 시작할 수 없었습니다. (CAMP-50302)
* 프로필 대체를 사용하여 이메일을 미리 볼 때 이메일 디자이너의 문제를 수정했습니다. (CAMP-49312)
* 사용자 지정 열거형의 값이 비는 문제가 해결되었습니다. 텍스트 열거형이며 하나의 값만 포함하는 필드로 사용자 지정 리소스를 만들 때 이 값이 기본적으로 설정되므로 이 필드에 간단한 요청으로 쿼리를 만들 수 있습니다. (CAMP-50606)
