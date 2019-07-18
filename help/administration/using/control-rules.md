---
title: 제어 규칙
seo-title: 제어 규칙
description: 제어 규칙
seo-description: 제어 규칙으로 메시지의 품질을 강화하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 33 A 1 C 90 C -534 E -4 FE 1-982 C-F 4 E 1858 D 4 D 2 D
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: working-with-tyatype-rules
discoiquuid: 305 CADDE -6424-4 C 6 F-B 11 B -1 E 8 BDBAD 6 EF 1
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Control rules{#control-rules}

제어 규칙을 사용하여 문자 표시, SMS 메시지 크기, 주소 형식 등과 같은 메시지 전송 전에 사용자가 메시지의 유효성을 확인하고 품질을 확인할 수 있습니다.

Adobe Campaign에서 사용할 수 있는 기본 규칙 세트는 표준 제어를 보장합니다.

* **[!UICONTROL Check subject]** (이메일): 제목 및 보낸 사람 주소에 특정 메일 전송 에이전트에서 문제를 일으킬 수 있는 특수 문자가 포함되어 있지 않은지 확인하고 메시지 제목이 작성되었는지 확인합니다.
* **[!UICONTROL Check URL labels]** (이메일): 각 추적 URL에 레이블이 있는지 확인합니다.
* **[!UICONTROL Check URLs]** (이메일): 추적 URL (" &amp;" 문자) 를 추적합니다.
* **[!UICONTROL Check proof size]** (모든 채널): 교정 대상 모집단이 100 명의 수신자를 초과하는 경우 오류 메시지를 생성합니다.
* **구독 취소 링크** (이메일) 확인: 각 컨텐츠 (HTML 및 텍스트) 에 구독 취소 (옵트아웃) URL 이 하나 이상 있는지 확인합니다.
* **[!UICONTROL Check delivery size]** (모든 채널): 메시지의 크기를 확인합니다.
* **[!UICONTROL Check social network sharing link]** (이메일): 컨텐츠에 소셜 네트워크 공유 링크 (virallinks) 를 포함할 때 미러 페이지에 대한 링크가 있는지 확인합니다.
* **[!UICONTROL A/B Test]**: A/B 테스트를 포함한 게시에 대한 테스트 모집단을 추출합니다.

규칙의 라이프사이클 중 하나에서 규칙이 적용되는 시점을 선택할 수 있습니다. Select the value to apply in the drop-down list from the **[!UICONTROL Phase]** field of the typology rule.

![](assets/typology_phase.png)

가능한 값은 다음과 같습니다.

* **타겟팅 시작 시**

   오류가 발생하면 개인화 단계가 실행되지 않도록 이 단계에서 제어 규칙을 적용할 수 있습니다.

* **타깃팅 후**

   제어 규칙을 적용하려면 대상의 볼륨을 알아야 할 경우 이 단계를 선택합니다.

   For example, the **Check proof size** control rule applies after the targeting stage: this rule prevents the preparation of message personalization if there are too many proof recipients.

* **개인화를 시작할 때**

   이 단계는 메시지 개인화를 승인하는 데 문제가 있는 경우 선택해야 합니다. 메시지 개인화는 분석 단계에서 수행됩니다.

* **The End of the Analysis**

   메시지 개인화가 완료되도록 하려면 이 단계를 선택합니다.

