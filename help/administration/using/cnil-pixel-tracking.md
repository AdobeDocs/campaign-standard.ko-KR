---
title: 이메일 추적 픽셀에 대한 CNIL 지침
description: 이메일 추적 픽셀 및 규정 준수 노력을 지원할 수 있는 Adobe Campaign Standard 컨트롤에 대한 CNIL의 업데이트된 지침에 대해 알아봅니다.
audience: administration
role: Admin
level: Experienced
hide: true
source-git-commit: 75f1f4ad8f7173f4601c9cff1ea93bf4092f274d
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---


# 이메일 추적 픽셀에 대한 CNIL의 업데이트된 지침 이해 {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**이 페이지에서:** 전자 메일 추적 픽셀에 대한 CNIL의 2026년 4월 권장 사항에 대해 알아보고, 추적 활성화, 링크 수준 추적, 동의 데이터 모델, 옵트아웃 메커니즘 및 보고 등 규정 준수를 지원할 수 있는 Adobe Campaign Standard 컨트롤을 알아봅니다.

>[!ENDSHADEBOX]

이 게시물은 정보 제공용으로만 제공됩니다. 이는 법률적인 조언이 아니며, 해당 법률의 준수를 보증하지 않습니다. 아래에 설명된 Adobe Campaign Standard 제품 기능은 적절하게 구성되고 작동되어 규정 준수 구현을 지원할 수 있는 기본 구성단위입니다. 각 고객은 해당 법률에 따라 의무를 결정하고 준수할 책임이 있습니다.

## 개요 {#overview}

2026년 4월 14일, 프랑스의 데이터 보호 당국인 *Commission national de l&#39;informatique et des libertés*(CNIL)에서 [이메일 내의 픽셀 추적 사용에 대한 권장 사항](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf)을 게시했습니다. 안내서에서는 동의가 필요한 시기를 명확히 설명하고 이메일 픽셀 추적에 대한 적절한 동의 사례의 중요성을 강조합니다. 이 정책은 프랑스에 기반을 둔 구독자에게 이메일을 게재하는 모든 엔터티의 전송 사례에 영향을 줄 수 있습니다.

CNIL은 기업이 이메일 수신자(&#39;사용자&#39;)에게 추적 픽셀의 존재 여부, 목적, 사용자의 옵트아웃 권리 등을 알리도록 권고일로부터 3개월의 기간을 제공했다. 이 전환 기간 동안 고객은 픽셀 추적에 대해 사용자에게 알리고 필요한 경우 옵트아웃을 제공할 것으로 예상됩니다. CNIL은 2026년 7월 14일 이후 집행 활동을 시작할 것으로 예상된다.

CNIL 및 기타 규제 기관이 픽셀 추적 및 관련 문제에 대한 지침을 명확히 함에 따라 Adobe은 업데이트를 계속 모니터링하고 Adobe Campaign Standard을 비롯한 이메일 마케팅을 지원하는 Adobe 제품의 기술 기능을 고객에게 알릴 예정입니다.

Adobe Journey Optimizer, Journey Optimizer B2B, Adobe Campaign 및 Marketo Engage을 포함한 Adobe 이메일 마케팅 실행 애플리케이션은 고객이 게재 또는 이메일 수준에서 열린 추적을 관리하는 데 도움이 되는 컨트롤을 제공합니다. 고객은 해당 CNIL 지침 및 기타 법률에 따라 자신의 규정 준수 의무를 결정할 책임이 있지만 이러한 기능은 고객 규정 준수 노력을 지원할 수 있습니다.

### 이메일 추적 픽셀이란 무엇입니까? {#tracking-pixel}

이메일 추적 픽셀은 이메일의 HTML에 임베드된 1x1 투명 이미지입니다. 수신자의 이메일 클라이언트가 해당 이미지를 로드할 때 픽셀은 타임스탬프, 디바이스 유형, 이메일 클라이언트 및 경우에 따라 대략적인 위치에 대한 IP 주소와 같은 데이터를 기록하는 서버를 ping합니다. 그러면 해당 로그가 수신자의 레코드에 연결되어 마케터는 이메일이 열렸는지 여부를 확인할 수 있습니다.

### 고객 지원 {#support}

위에서 설명한 변경 사항을 구현하는 데 도움을 원하는 고객은 기존 Adobe 에코시스템과 연계될 수 있습니다. 참조된 Adobe 기능에 대한 기술적인 질문이 있는 경우 고객 성공 관리자 또는 기술 계정 관리자에게 문의하십시오.

## 이메일 추적과 관련된 Adobe Campaign Standard 기능 {#acs-functionality}

고객은 아키텍처를 구성할 때 Adobe Campaign Standard의 기본 추적, 스키마 및 개인화 메커니즘을 사용하여 특정 요소를 처리할 수 있습니다.

### 이메일 분류 {#email-classification}

이메일 유형(인증, 게재 가능성 전용, 트랜잭션, 동의 마케팅, B2B 전망)을 나타내는 사용자 지정 필드로 게재 템플릿을 확장합니다. Campaign Standard에서 게재 템플릿은 보고 및 워크플로우 논리로 이동하는 사용자 지정 필드를 전달할 수 있습니다. 이 분류는 각 전송에 적합한 추적을 구동합니다.

[게재 템플릿을 만들고 사용하는 방법을 알아봅니다](../../channels/using/creating-an-email.md)

### 동의 데이터 모델 {#consent-data-model}

Campaign Standard 사용자 지정 리소스 메커니즘(**관리 > 개발 > 사용자 지정 리소스**)을 통해 프로필 리소스를 확장하여 용도별 동의 플래그, 동의 타임스탬프 및 가장 최근에 열어 본 날짜(날짜만 - 시간 구성 요소 없음)를 전달합니다. 프로필에 연결된 별도의 사용자 지정 리소스는 개별 동의 증명을 지원하는 추가 전용 동의 이벤트 로그를 캡처합니다. Campaign Standard 랜딩 페이지는 프로필 필드에 직접 쓸 수 있으므로, 현재 동의 상태는 기본적으로 관리할 수 있습니다. 환경 설정이 제출되면 Adobe Campaign Standard REST API(`/profileAndServicesExt`)를 통해 동의 로그가 작성됩니다.

[리소스를 만들거나 확장하는 방법 알아보기](../../developing/using/creating-or-extending-the-resource.md)

[API를 통해 사용자 지정 리소스와 상호 작용하는 방법을 알아봅니다](../../api/using/interacting-with-custom-resources.md)

### 픽셀 방출 {#pixel-emission}

Adobe Campaign Standard은 게재 또는 템플릿 속성의 **[!UICONTROL Activate tracking]** 토글을 통해 게재 수준에서 추적을 제어합니다. 열기 추적이 합법적이지 않은 게재(인증 전용, 재요청 이메일)의 경우 이 토글이 비활성화됩니다. 용도별 픽셀 방출이 적합한 게재의 경우, 한 가지 접근 방법은 자동으로 삽입된 표준 픽셀을 비활성화하고 조건부 1×1 추적된 이미지 요소를 포함하는 콘텐츠 블록을 사용하는 것입니다(용도별 하나). 여기서 각 이미지에는 URL 범주(`PIX_DELIV`, `PIX_PERF`, `PIX_PROFILE`, `PIX_FRAUD`)가 할당되고 수신자의 해당 동의 플래그가 true인 경우에만 표시됩니다.

[이메일 추적 매개 변수를 구성하는 방법 알아보기](configuring-email-channel.md#tracking-parameters)

[이메일 Designer에서 추적된 URL을 관리하는 방법 알아보기](../../designing/using/links.md#about-tracked-urls)

[콘텐츠 블록을 추가하는 방법 알아보기](../../designing/using/personalization.md#adding-a-content-block)

### 철회 {#withdrawal}

구독 취소 링크와 별도로 모든 이메일 바닥글에 **추적기 환경 설정 관리** 링크를 추가합니다. 링크는 `recipientId` 또는 `urlSubscription` 메커니즘을 통해 인증된 Campaign Standard 랜딩 페이지를 가리킵니다. 수신자는 목적별 동의 플래그를 전환하여 제출합니다. 확인 시 Campaign Standard REST API에 대한 작은 호출은 동의 로그에 탈퇴 이벤트를 기록합니다. 권장 사항은 이 링크 자체가 추적 요구 사항에서 보안 제외됨을 나타냅니다.

[옵트인 및 옵트아웃 랜딩 페이지를 설정하는 방법을 알아봅니다](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages)

[랜딩 페이지를 시작하는 방법 알아보기](../../channels/using/getting-started-with-landing-pages.md)

### 동의 증명 {#consent-proof}

각 동의 변경 — 등록 시 캡처, 환경 설정 페이지에서 업데이트, 만료 — 동의 로그 사용자 지정 리소스에 단어 버전 코드, 캡처 타임스탬프, 캡처 소스 및 범위를 포함하는 행을 만듭니다. 이 로그는 Campaign Standard 탐색기를 통해 쿼리할 수 있고 REST API를 통해 내보낼 수 있으며 예약된 워크플로우를 통해 DPO 검토에 내보낼 수 있습니다.

[API를 통해 사용자 지정 리소스와 상호 작용하는 방법을 알아봅니다](../../api/using/interacting-with-custom-resources.md)

### 재요청 거버넌스 {#re-solicitation}

선택한 기간 내에 해당 필드가 있는 프로필을 제외하는 유형화 필터링 규칙과 함께 프로필의 사용자 지정 `cusLastPixelRefusalDate` 필드를 사용하면 해당 기간에 거부된 수신자의 재요청을 방지할 수 있습니다. 예약된 워크플로우는 오래된 레코드에 플래그를 지정하고 만료 이벤트를 동의 로그에 기록하여 고객의 동의 만료 기간을 관리합니다.

[유형화 규칙을 사용한 작업 방법 알아보기](../../sending/using/about-typology-rules.md)

[유형화 규칙을 관리하는 방법 알아보기](../../sending/using/managing-typology-rules.md)

### 보고 {#reporting}

Campaign Standard 동적 보고서는 URL 범주 및 프로필 차원을 기반으로 구축됩니다. 동적 보고서에서 새로운 차원으로 표시되는 용도별 URL 카테고리입니다. 이를 통해 운영자는 용도별로 데이터를 열고 클릭할 수 있습니다. URL 범주가 갖추어지면 기본적으로 동의 추적과 비동의 추적 간의 구분이 표시됩니다.

[동적 보고서를 시작하는 방법 알아보기](../../reporting/using/about-dynamic-reports.md)

[지표 추적에 대해 알아보기](../../reporting/using/tracking-indicators.md)
