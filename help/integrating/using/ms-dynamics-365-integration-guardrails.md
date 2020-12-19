---
solution: Campaign Standard
product: campaign
title: Microsoft Dynamics 365 통합 보장
description: Microsoft Dynamics 365(Campaign Standard 통합 보안 기능 포함)
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---


# 통합 보호 및 경계

## 통합 가드레일

이 통합을 사용할 계획이라면 다음 지침을 고려해야 합니다. 이러한 보증서를 초과한다고 생각되면 Adobe 기술 담당자에게 문의하십시오.

* 통합으로 생성된 ACS 엔진 호출 볼륨을 지원하기 위해 적절한 캠페인 패키지에 라이선스를 부여해야 합니다. 라이센스가 있는 엔진 호출 볼륨을 초과하면 캠페인 성능이 저하될 수 있습니다.

   통합에서 엔진 호출 볼륨을 예상하는 데 도움이 되도록 다음을 사용하십시오.

   * 레코드 삽입(새 레코드):엔진 호출 1회
   * 레코드 삭제:엔진 호출 1회
   * 업데이트 기록:2개의 엔진 호출(대상 레코드가 소스 레코드와 동일한 경우(즉, ACS 레코드에 대한 변경 사항이 없는 경우) 1개의 호출만)

   전체 ACS 엔진 호출 볼륨을 계산할 때 랜딩 페이지, WebApps, JSSP, API, 모바일 앱 등록 등을 비롯한 다른 엔진 호출 소스를 고려하는 것이 중요합니다.

   다음 사이트에서 캠페인 패키지 정보를 봅니다.https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html

* 통합은 최대 3천만 명의 연락처를 지원합니다.

* 표준 통합 서비스에는 최대 5개의 사용자 정의 엔티티에 대한 지원이 포함되어 있습니다.

* 500,000개 이상의 사용자 지정 개체는 캠페인 워크플로우를 통해(추가 비용이 발생하는 경우) 첫 번째 파일 기반 가져오기를 수행하려면 추가 컨설팅 시간이 필요합니다.

* 표준 통합 서비스에는 최대 50개의 열 크기의 사용자 정의 엔티티에 대한 지원이 포함되어 있습니다.

* 통합을 구현하기 전에 사용자 지정 리소스를 만들고 게시해야 합니다.

* 테이블을 연결할 때의 최대 테이블 깊이는 2개입니다(예: table1->table2->table3).

* 동적 365 데이터 유형에 대한 지원이 제한적입니다. 데이터 모델에 단순 데이터 유형(예: 문자열, 정수, 소수 등)이 아닌 데이터 유형이 포함되어 있는 경우 통합을 사용하기 전에 데이터 모델을 업데이트해야 할 수 있습니다.

* Campaign 사용자 지정 엔티티의 기존 데이터를 보존하면 통합을 위한 데이터를 준비하는 데 추가 컨설팅 비용이 발생할 수 있습니다.

* 초기 인제스트가 캠페인 지연을 유발할 수 있으므로 온보딩 유지 관리 윈도우를 Adobe과 고객 사이에 설정해야 할 수 있습니다.

* 이러한 경우 데이터 동기화 속도가 느려질 수 있으므로 통합 사용(예: 새 레코드나 업데이트된 레코드의 급격한 증가) 시 알려진 증가 또는 스파이크 인스턴스를 통신할 수 있습니다.

* 통합의 일부로 Microsoft Azure 및 Dynamics 365의 사전 통합 구성 단계를 완료해야 합니다. 이 페이지에서 [구성 단계를 참조하십시오](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)

* Dynamics 365 및 Campaign 데이터 모델을 통합으로 가져오고 유지 관리하게 됩니다.

## 통합 경계

이 통합은 Dynamics 365와 Campaign 간의 일반적인 데이터 이동 사례를 해결하기 위해 고안되었지만 각 고객에 맞는 모든 사용 사례를 처리하기 위한 것은 아닙니다.

* 통합은 개인 정보(예: GDPR)를 삭제하지 않습니다. 최종 사용자 개인 정보 보호 요청을 이행하는 책임은 고객에게 있습니다.이러한 요청은 Adobe Experience Platform Privacy Service을 통해 Campaign과 Dynamics 365의 모두에 독립적으로 해야 합니다. 원할 경우 데이터 동기화를 지원하기 위해 정기적으로 삭제를 실행할 수 있습니다.

* 옵트아웃 정보(고객이 구성한 경우)를 제외하고 Campaign에서 Dynamics 365로 프로필 또는 사용자 지정 엔티티 데이터가 동기화되지 않습니다.

* 캠페인 구독 관리(즉, 가입/가입 해지)는 기본적으로 지원되지 않습니다.

* Dynamics 365 내에서 캠페인 이메일 캠페인을 구성하고 트리거하는 것은 지원되지 않습니다.

* 통합은 Dynamics 365와 Campaign 데이터 모델 간의 데이터 리모델링을 지원하지 않습니다. 하나의 Dynamics 365 테이블을 하나의 캠페인 테이블에 동기화해야 합니다.

* 현재 통합 릴리스가 있는 셀프 서비스 UI가 없습니다.
