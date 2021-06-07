---
solution: Campaign Standard
product: campaign
title: 초기 릴리스 정보
description: 초기 릴리스 정보
feature: 개요
role: Business Practitioner
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 7eb12fbb89f677eb7184cb5ff200d3f8a466d3c8
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# 조기 릴리스 노트 {#new-release}

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 설명합니다.

>[!CAUTION]
>
> 이 컨텐츠는 단계 환경 업그레이드 날짜까지 사전 통지 없이 변경될 수 있습니다. 자세한 내용은 [릴리스 계획 페이지](../../rn/using/release-planning.md)를 참조하십시오.


## 릴리스 21.2 - 2021년 6월 {#release-21-2---june-2021}

**개선 사항**

* 이제 랜딩 페이지를 디자인할 때 양식을 제출하기 전에 프로필에 선택해야 하는 필수 확인란을 추가할 수 있습니다.

* 트리거 통합의 경우, 트리거 페이로드에서 들어오는 조정 데이터가 없을 때 표시되는 오류 메시지가 개선되었습니다.&quot;페이로드에서 별칭 데이터가 누락되었습니다.&quot;

* 큐에서 푸시 알림을 검색하는 성능이 개선되었습니다.

**기타 변경 사항**

* 타사 보안 도구에 의해 수정된 후 일부 유효한 서명된 추적 링크가 잘못 차단되는 문제를 방지하기 위해 링크 추적을 위한 URL 서명 메커니즘을 비활성화했습니다.

* 다중 변형 게재에서 기본 변형이 삭제된 경우 사용자가 더 이상 언어 사본을 만들 수 없습니다. 이제 언어 사본 작성 중에 메시지가 표시됩니다. (CAMP-48235)

* 2단계 프로필 삭제 프로세스(Campaign 19.4 릴리스부터 더 이상 사용되지 않음)는 이제 기본적으로 비활성화됩니다. 이전에는 개인 정보 보호 핵심 서비스를 사용하기 전에 Campaign 인터페이스에서 수동으로 비활성화해야 했습니다. 이렇게 하지 않으면 삭제 요청이 완료되지 않고 보류 중인 상태로 유지됩니다.

* 문자열 유형 열의 값을 연결하기 위해 새로운 &#39;StringAgg&#39; 집계 함수가 도입되었습니다. (CAMP-47077)

* 동적 보고서에서 **제외 증명** 세그먼트가 제거되었습니다. (CAMP-46161)

* Campaign 애플리케이션에서 platformPrincipal 값 없이 iOS 인증서를 업로드할 때 사용자에게 알리는 새 경고 메시지가 추가되었습니다.

* 전자 메일의 최대 크기는 기본적으로 100MB로 설정됩니다. 이 제한을 사용하면 이메일 크기를 무한정 늘릴 수 있는 오류를 방지하여 시스템 충돌을 야기할 수 있습니다. (CAMP-47445)

* 이제 표준 사용자가 이메일 디자이너와의 자산 핵심 서비스 통합을 사용할 수 있습니다.

* v4 푸시 애플리케이션에서 v5 푸시 애플리케이션으로의 성공적인 마이그레이션을 확인하기 위해 새로운 메시지가 추가되었습니다.

* JSONWeb 토큰을 만들어 Campaign Standard API를 인증하는 동안 제품 프로필이 이제 **고려됩니다**. 즉, 보안 그룹에 할당된 조직 단위 및 역할(AdobeIO의 제품 프로필과 일치함)은 Campaign Standard Rest API 호출에 필요한 IMS 기술 계정에 적용됩니다. (CAMP-47479)


**패치**

* 일괄 처리 프로세스 로그 테이블(**xtkjoblog**) 테이블에 대한 만료 옵션이 적용되지 않는 문제를 해결했습니다. 이로 인해 테이블이 올바르게 삭제되지 않았습니다.

* **세그먼테이션** 워크플로우 활동에서 필터 순서를 변경할 수 없는 문제를 수정했습니다. (CAMP-48357)

* null 값 오류로 인해 게재가 실패할 수 있는 20.4의 회귀 문제를 해결했습니다. (CAMP-48591)

* **공유** > **지금 보고서 보내기** 또는 **일정에 따라 보고서 보내기** 메뉴를 통해 보고서를 전송할 수 없는 문제를 해결했습니다. (CAMP-47798)

* Gmail 계정에서 받은 추적 이벤트를 필터링하여 Gmail에 대해 잘못된 열기 비율을 발생시킬 수 있는 회귀 문제를 해결했습니다. (CAMP-46504)

* Adobe Campaign Standard의 보고서와 Adobe Analytics의 보고서 간에 데이터 불일치가 발생하는 다양한 문제를 수정했습니다. (CAMP-47671, CAMP-47296)

* 준비에 실패한 후 게재 로그에 액세스할 수 없는 문제를 수정했습니다. (CAMP-48296)

* 사용자 지정 보고서를 편집, 삭제 또는 전송하려고 할 때 오류 메시지가 표시되는 문제를 해결했습니다. (CAMP-47789, CAMP-47798)

* 새 사용자 지정 리소스를 만들고 **동기화 안 함** 옵션을 활성화하면 API 호출이 실패하는 문제를 해결했습니다. (CAMP-48014)

* **동기화 안 함** 옵션이 활성화된 사용자 지정 리소스가 재초안 또는 삭제된 스키마를 참조할 수 있는 문제가 해결되었습니다. 이 문제로 인해 사용자 지정 리소스를 게시할 때 오류가 발생했습니다.

* 동일한 외부 계정에서 여러 짧은 코드를 사용할 때 SMS 옵트아웃 문제가 해결되었습니다.

* 데이터베이스를 게시한 후 새 게재 경고 기준(&quot;액세스하려는 리소스에 연결할 수 없음&quot;)에 액세스할 수 없는 문제를 수정했습니다. (CAMP-48221)

* 일부 인스턴스에서 추적 로그가 누락되는 문제가 수정되었습니다. 이러한 손실된 추적 로그를 복원하기 위해 새로운 기술 워크플로우(**trackingLogRecovery**)가 추가되었으며 Adobe 내부에서만 사용해야 합니다.

* 게재 데이터가 동적 보고서에 표시되지 않던 문제를 수정했습니다. 보고서가 0으로 설정되었습니다. (CAMP-47480)

* 서버 JavaScript HTTP 클라이언트가 외부 URL에 연결할 수 없는 문제를 해결했습니다.

* 워크플로우의 내부 이름을 변경한 후 **증분 쿼리** 활동을 재설정하는 문제를 해결했습니다. 이 문제는 날짜 필드가 증분 모드로 사용되었을 때 발생했습니다. (CAMP-47674)

* Adobe Experience Manager 통합으로 다국어 이메일을 만들 때 게재 요약에 미리 보기 축소판이 표시되지 않는 문제를 해결했습니다. 이 문제는 **언어 사본 작성** 단추를 사용하여 이메일 변형을 만들 때 발생했습니다. (CAMP-47810)

* 사용자가 이메일 또는 SMS 하위 게재에서 상위 게재에 액세스할 수 없는 문제를 해결했습니다. (CAMP-47986)

* 사용자 지정 이벤트가 누락된 REST API를 통해 트랜잭션 메시지를 전송할 때 CPU 및 메모리 사용량이 초과되는 문제를 해결했습니다. (CAMP-47147)

* 경우에 따라 실시간 메시지가 전송되지 않는 트랜잭션 메시지 API 관련 오류를 수정했습니다.

* **일정에 따라 보고서 보내기** 옵션을 사용한 후에 보고서가 수신되지 않던 문제를 수정했습니다. (CAMP-48583)

* **지금 보고서 보내기 옵션**&#x200B;을 사용한 후에 받은 보고서가 불완전하고 데이터가 누락되는 문제를 수정했습니다. (CAMP-48583)

* 기본 제공 **인스턴트 보고서 공유**(reportSendingNow) 워크플로우가 보고서를 생성하지 못하는 Dynamics 보고서의 **일정에 따라 보고서 보내기** 옵션 문제를 해결했습니다. (CAMP-47786)

* 이미지를 업로드할 때 이미지 차원이 축소되는 이메일 디자이너 문제를 수정했습니다. (CAMP-47017)

* 게재를 만들 때 사용 가능한 모든 Experience Manager 템플릿이 표시되지 않는 문제를 해결했습니다. (CAMP-48132)

* 전송된 게재의 요약 페이지에 있는 캠페인 링크가 사용자를 관련 캠페인으로 리디렉션하지 못하는 오류를 수정했습니다. (CAMP-48012)

* 자산을 선택하려고 할 때 자산 핵심 서비스 통합이 계속 실패하는 이메일 디자이너의 문제를 해결했습니다. (CAMP-47446)

* Campaign으로 인해 일부 Journey Orchestration 게재이 Journey Orchestration에서 이벤트에 의해 전송된 정확한 값(즉, 00으로 끝나는)으로 타임스탬프를 지원하지 않는 문제를 해결했습니다.