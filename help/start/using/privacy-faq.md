---
title: 개인 정보 FAQ
description: Adobe Campaign Standard의 개인 정보, 가상 사용자 및 동의 관리에 대해 알아보기
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3
translation-type: tm+mt
source-git-commit: 500a9575157a0652eac2504d2360f7a1cbd6189e
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 100%

---


# 개인 정보 FAQ {#privacy-faq}

다음은 Adobe Campaign 사용 시 개인 정보 및 동의에 관한 FAQ입니다.

## 주요 용어 {#key-terms}

**개인 정보에 관한 주요 용어는 무엇입니까?**

아래 나열된 항목은 Adobe Campaign의 개인 정보 및 동의와 관련된 주요 용어 및 개념의 링크입니다.

* [개인 정보 관리에 관한 규정](../../start/using/privacy-management.md#privacy-management-regulations)
* [개인 데이터 및 가상 사용자](../../start/using/privacy.md#personal-data)
* [액세스 권한 및 잊혀질 권리](../../start/using/privacy-management.md#right-access-forgotten)
* [동의, 보존 및 역할](../../start/using/privacy-management.md#consent-retention-roles)

## 개인 정보 보호 규정 준비 {#privacy-regulations-readiness}

**최신 개인 정보 보호 규정을 준수하기 위한 Adobe Campaign의 제안은 무엇입니까?**

Adobe는 법률적 조언을 제공하지 않습니다. 따라서 사용자가 직접 법률 자문과 협력하여 GDPR, CPA, PDPA, LGPD 또는 기타 관련 규정 준수를 준비하는 데 필요한 모든 조치를 취하도록 해야 합니다.

**데이터 액세스 및 삭제 요청 준비**

* 개인 정보 보호 담당자 지정 등 데이터 주체의 요청을 수신/응답하는 프로세스를 확인합니다.

* Adobe Campaign에 저장된 다양한 고객 데이터를 검토하고 고유한 식별자를 결정합니다(둘 이상이 있을 수 있음).

* 데이터 주체 ID 확인을 위한 유효성 검사/인증 정책 및 프로세스를 결정합니다.

* 데이터 주체의 응답은 쉽게 이해할 수 있도록 합니다.

**동의 고려**

* GDPR의 데이터 캡처(즉, 언어, 동의 메커니즘 및 동의 로그를 고려)에 필요한 모든 터치 포인트를 나열하고 업데이트합니다.

* 모든 마케팅 이메일에 구독 취소 링크가 포함되어 있는지 확인합니다.

* 이메일 마케팅을 위한 글로벌 전략을 평가하여 지역별 구현을 결정합니다.

**데이터 이해**

* 데이터가 Adobe Campaign으로 유입되는 모든 데이터 가져오기 및 캡처 소스를 검토하여 위치와 마케팅 활동에 사용되는 필드를 문서화합니다.

* Adobe Campaign 데이터베이스에서 사용되지 않은 데이터 속성을 제거합니다.

* 캡처한 목적에 맞게 Adobe Campaign에서 이용 가능한 데이터를 사용하여 수신자에게 더 나은 개인화된 경험을 제공합니다.

* 데이터 액세스 권한을 검토 및 업데이트하여 Adobe Campaign 사용자가 캠페인을 실행하는 데 필요한 데이터만 완전히 활용하되 그 이상의 데이터에는 액세스할 수 없게 합니다.

* Adobe Campaign의 각 사용자가 필요한 작업을 수행할 수 있는 적절한 액세스 권한을 가지고 있지만 추가 작업을 수행할 다른 권한은 없는지 확인합니다.

## 사용자 참여 유지 {#preserve-user-engagement}

**데이터 컨트롤러가 사용자 참여에 미치는 영향을 최소화하면서 동의를 얻는 방법은 무엇입니까?**

특정 마케팅 활동에 대한 동의가 필요한 경우, 소비자 동의는 활성화(즉, 동의 또는 사전 체크 박스로 침묵이 아님) 및 언번들링 되어야 하고 서비스를 제공할 때 조건부 상태가 아니어야 합니다.

계속 데이터를 사용할 수 있도록 특정 동의를 새로 고쳐야 하는 인스턴스가 있을 수 있습니다.

마케터는 이러한 강화된 동의 요구 사항을 마케팅 환경에 미치는 위험으로 생각하기보다는 브랜드 참여 및 충성도의 지표와 고객 만족도 및 신뢰의 지표로 활용할 수 있습니다.

## 동의 관리 {#manage-consent}

**데이터 컨트롤러는 Adobe Campaign에서 동의를 어떻게 관리합니까?**

Adobe Campaign은 이미 사용자 지정된 데이터 필드나 서비스 한 두개를 통해 이용하는 것보다 더 많은 수준에서 동의를 관리할 수 있는 기능을 제공하고 있습니다.

마케터는 진행 방법에 대한 지침을 얻기 위해 법률 자문을 구하고 Adobe Campaign에 내장된 기능을 이용해야 합니다.

예를 들어 Adobe Campaign에서 데이터 모델을 확장하여 사용자가 옵트인을 선택한 경우뿐만 아니라 옵트인의 타임스탬프 및 정확한 동의 범위를 캡처하는 일부 유형의 지표를 추적합니다.

## 데이터 삭제 {#data-deletion}

**데이터 주체의 고객 요청에 응답하여 데이터 컨트롤러가 Adobe Campaign에서 삭제할 수 있는 데이터는 무엇입니까?**

기본 제공 및 사용자 지정 테이블을 포함한 데이터 주체와 연관된 모든 데이터가 삭제됩니다.

기본적으로 `integrity="own"`이(가) 있는 데이터 주체와 연결된 데이터는 모두 삭제됩니다.

데이터 컨트롤러는 데이터 스키마에 정의된 링크의 무결성을 변경하여 이를 사용자 지정할 수 있는 옵션이 있습니다(예: 특정 데이터를 삭제하지 않는 비즈니스 타당성이 있는 경우).

**게재 및 추적 로그가 삭제되면 보고서는 어떤 영향을 받습니까?**

Adobe Campaign의 보고서는 게재 및 추적 로그에서 집계된 데이터에 대해 계산된 지표를 기반으로 합니다. 따라서 개별 로그를 제거해도 보고서에 표시된 지표에 영향을 주지 않습니다.

## 데이터 다시 가져오기 {#re-import-data}

**Adobe Campaign에서 기록은 외부 데이터 소스에서 업로드되는 경우가 많습니다. 나중에 데이터를 다시 가져올 수 있다는 점에 유의해야 합니까?**

데이터 컨트롤러는 삭제 요청을 받을 때 모든 시스템에서 데이터 주체의 필요한 데이터를 모두 삭제해야 합니다.

## 다시 옵트인 {#opt-in-again}

**Adobe Campaign에서 데이터가 지워진 데이터 주체가 나중에 다시 옵트인할 수 있습니까?**

데이터 주체는 데이터가 Adobe Campaign에서 삭제된 후 다시 옵트인하거나 새 수신자로 추가될 수 있습니다.

이전 삭제를 수행한 시점과 새 수신자가 만들어진 시기를 자세히 설명하는 감사 추적을 사용할 수 있습니다.