---
title: 제어 규칙
description: 제어 규칙을 사용하여 메시지 품질 검사를 강화하는 방법을 알아봅니다.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
feature: Typology Rules
role: User
level: Intermediate
exl-id: 6461c128-1e42-4685-88f8-507244147e6f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 3%

---

# 제어 규칙 {#control-rules}

제어 규칙을 사용하면 메시지를 보내기 전에 문자 표시, SMS 메시지 크기, 주소 형식 등과 같은 메시지의 유효성 및 품질을 확인할 수 있습니다.

>[!NOTE]
>
>보안상의 이유로 제어 규칙은 읽기 전용이며 수정할 수 없습니다.

## 기본 제어 규칙 {#default-control-rules}

기본 규칙 세트를 사용하면 표준 컨트롤을 사용할 수 있습니다. 아래 표는 이러한 규칙과 관련 채널 및 [실행 단계](#control-rules-execution-phases).

| 레이블 | 채널 | 실행 단계 | 설명 |
|---------|----------|---------|---------|
| **[!UICONTROL A/B Test]** | 이메일 | 개인화 시작 시 | A/B 테스트를 사용하여 게재할 테스트 모집단을 추출합니다. |
| **[!UICONTROL Check delivery size]** | 모두 | 타겟팅 후 | 메시지 크기를 확인합니다. |
| **[!UICONTROL Check email content is not empty]** | 이메일 | 타겟팅 후 | 메시지 콘텐츠가 비어 있는 경우 오류를 생성합니다. |
| **[!UICONTROL Check In-App content for broadcast template]** | 인앱 | 개인화 시작 시 | 브로드캐스트 템플릿에 대한 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check In-App content for profile template]** | 인앱 | 개인화 시작 시 | 프로필 템플릿에 대한 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check In-App content for subscriber template]** | 인앱 | 개인화 시작 시 | 구독자 템플릿에 대해 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check proof size]** | 모두 | 타겟팅 후 | 증명 대상 모집단이 100명의 수신자를 초과하는 경우 오류 메시지를 생성합니다. |
| **[!UICONTROL Check social network sharing link]** | 이메일 | 개인화 시작 시 | 컨텐츠에 소셜 네트워크 공유 링크(ViralLinks)를 포함할 때 미러 페이지에 대한 링크가 있는지 확인합니다. |
| **[!UICONTROL Check subject]** | 이메일 | 개인화 시작 시 | 제목 및 보낸 사람 주소에 특정 메일 전송 에이전트에 문제를 일으킬 수 있는 특수 문자가 포함되어 있지 않은지 확인하고 메시지 주제가 완료되었는지 확인합니다. |
| **[!UICONTROL Check unsubscription link]** | 이메일 | 개인화 시작 시 | 각 컨텐츠(HTML 및 텍스트)에 하나 이상의 구독 취소(옵트아웃) URL이 있는지 확인합니다. |
| **[!UICONTROL Check URL labels]** | 이메일 | 개인화 시작 시 | 각 추적 URL에 레이블이 있는지 확인합니다. |
| **[!UICONTROL Check URLs]** | 이메일 | 개인화 시작 시 | 추적 URL(&quot;&amp;&quot; 문자 유무)을 확인합니다. |

## 규칙 실행 단계 제어 {#control-rules-execution-phases}

제어 규칙은 게재 라이프 사이클의 다른 단계에서 적용할 수 있습니다.

* **타겟팅 시작 시**: 이 단계에서 제어 규칙을 적용하여 오류가 발생하는 경우 개인화 단계가 실행되지 않도록 할 수 있습니다.

* **타겟팅 후**: 타깃팅 후 를 실행하면 제어 규칙을 적용하기 위해 대상의 볼륨을 알 수 있습니다.

   예: **증명 크기 확인** 제어 규칙은 타깃팅 단계 다음에 적용됩니다. 증명 수신자가 너무 많으면 이 규칙은 메시지 개인화를 준비할 수 없습니다.

* **개인화 시작 시**: 이 확인이 메시지 개인화 승인과 관련된 경우에 적용됩니다. 메시지 개인화는 분석 단계 동안 수행됩니다.

* **분석 종료 시**: 검사를 위해 메시지 개인화를 완료해야 하는 경우.
