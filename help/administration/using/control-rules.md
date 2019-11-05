---
title: 제어 규칙
description: 제어 규칙을 사용하여 메시지의 품질 검사를 강화하는 방법을 살펴봅니다.
page-status-flag: 활성화 안 함
uuid: 33a1c90c-534e-4fe1-982c-f4e1858d4d2d
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 관리
content-type: reference
topic-tags: working-with-typical-rules
discoiquuid: 305cadde-6424-4c6f-b11b-1e8bdbad6ef1
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 제어 규칙{#control-rules}

제어 규칙을 사용하면 메시지를 보내기 전에 문자 표시, SMS 메시지 크기, 주소 형식 등과 같은 메시지의 유효성 및 품질을 확인할 수 있습니다.

Adobe Campaign에서 사용할 수 있는 기본 규칙 세트를 통해 표준 컨트롤을 사용할 수 있습니다.

* **[!UICONTROL Check subject]** (이메일):제목과 보낸 사람 주소에 특정 메일 전송 에이전트에 문제를 일으킬 수 있는 특수 문자가 포함되어 있지 않은지 확인하고 메시지 제목이 완료되었는지 확인합니다.
* **[!UICONTROL Check URL labels]** (이메일):각 추적 URL에 레이블이 있는지 확인합니다.
* **[!UICONTROL Check URLs]** (이메일):추적 URL을 확인합니다("&amp;" 문자 존재).
* **[!UICONTROL Check proof size]** (모든 채널):proof target 모집단이 100명을 초과하는 경우 오류 메시지를 생성합니다.
* **구독 취소 링크** 확인(이메일):각 컨텐츠(HTML 및 텍스트)에 하나 이상의 구독 취소(옵트아웃) URL이 있는지 확인합니다.
* **[!UICONTROL Check delivery size]** (모든 채널):메시지의 크기를 확인합니다.
* **[!UICONTROL Check social network sharing link]** (이메일):컨텐트에 소셜 네트워크 공유 링크(ViralLinks)를 포함할 때 미러 페이지에 대한 링크가 있는지 확인합니다.
* **[!UICONTROL A/B Test]**:a/B 테스트를 사용하여 배달에 대한 테스트 모집단을 추출합니다.

전달 라이프 사이클의 단계 중 하나에서 규칙이 적용되는 시점을 선택할 수 있습니다. 유형 규칙 필드의 드롭다운 목록에서 적용할 값을 **[!UICONTROL Phase]** 선택합니다.

![](assets/typology_phase.png)

가능한 값은 다음과 같습니다.

* **타깃팅 시작 시**

   이 단계에서 제어 규칙을 적용하여 오류가 발생하는 경우 개인화 단계를 실행하지 않을 수 있습니다.

* **타깃팅 후**

   제어 규칙을 적용하려면 대상 볼륨을 알아야 하는 경우 이 단계를 선택합니다.

   예를 들어, **검사 증명 크기** 제어 규칙은 타깃팅 단계 다음에 적용됩니다.이 규칙은 입증 받는 사람이 너무 많을 경우 메시지 개인화를 준비할 수 없습니다.

* **개인화 시작**

   확인 시 메시지 개인화를 승인하는 경우 이 단계를 선택해야 합니다. 메시지 개인화는 분석 단계 동안 수행됩니다.

* **분석 종료 시**

   확인 시 메시지 개인화를 완료해야 하는 경우 이 단계를 선택하십시오.

>[!NOTE]
>
>보안상의 이유로 제어 규칙 내용은 수정할 수 없습니다. 이 **[!UICONTROL Code]** 필드는 읽기 전용입니다.
