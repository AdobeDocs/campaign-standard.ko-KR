---
solution: Campaign Standard
product: campaign
title: 제어 규칙
description: 제어 규칙을 사용하여 메시지의 품질 검사를 강화하는 방법을 알아봅니다.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 3%

---


# 제어 규칙 {#control-rules}

제어 규칙을 사용하면 메시지를 보내기 전에 문자 표시, SMS 메시지 크기, 주소 형식 등과 같은 메시지의 유효성 및 품질을 확인할 수 있습니다.

>[!NOTE]
>
>보안상의 이유로 제어 규칙은 읽기 전용이므로 수정할 수 없습니다.

## 기본 제어 규칙 {#default-control-rules}

기본 규칙 세트가 표준 컨트롤을 보장합니다. 아래 표는 관련 채널 및 [실행 단계뿐만 아니라 이러한 규칙에 대한 정보를 제공합니다](#control-rules-execution-phases).

| 레이블 | 채널 | 실행 단계 | 설명 |
---------|----------|---------|---------
| **[!UICONTROL A/B Test]** | 이메일 | 개인화 시작 | A/B 테스트를 사용하여 배달에 대한 테스트 모집단을 추출합니다. |
| **[!UICONTROL Check delivery size]** | 모두 | 타깃팅 후 | 메시지 크기를 확인합니다. |
| **[!UICONTROL Check email content is not empty]** | 이메일 | 타깃팅 후 | 메시지 내용이 비어 있는 경우 오류를 생성합니다. |
| **[!UICONTROL Check In-App content for broadcast template]** | 인앱 | 개인화 시작 | 브로드캐스트 템플릿에 대해 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check In-App content for profile template]** | 인앱 | 개인화 시작 | 프로필 템플릿에 대해 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check In-App content for subscriber template]** | 인앱 | 개인화 시작 | 구독자 템플릿에 대해 인앱 콘텐츠/트리거가 비어 있지 않은지 확인합니다. |
| **[!UICONTROL Check proof size]** | 모두 | 타깃팅 후 | 증명 대상 모집단에서 받는 사람이 100명을 초과하는 경우 오류 메시지를 생성합니다. |
| **[!UICONTROL Check social network sharing link]** | 이메일 | 개인화 시작 | 컨텐츠에 소셜 네트워크 공유 링크(ViralLinks)를 포함할 때 미러 페이지에 대한 링크가 있는지 확인합니다. |
| **[!UICONTROL Check subject]** | 이메일 | 개인화 시작 | 제목과 보낸 사람 주소에 특정 메일 전송 에이전트에 문제를 일으킬 수 있는 특수 문자가 포함되어 있지 않은지 확인하고 메시지 제목이 완료되었는지 확인합니다. |
| **[!UICONTROL Check unsubscription link]** | 이메일 | 개인화 시작 | 각 컨텐츠(HTML 및 텍스트)에 하나 이상의 구독 취소(옵트아웃) URL이 있는지 확인합니다. |
| **[!UICONTROL Check URL labels]** | 이메일 | 개인화 시작 | 각 추적 URL에 레이블이 있는지 확인합니다. |
| **[!UICONTROL Check URLs]** | 이메일 | 개인화 시작 | 추적 URL(&quot;&amp;&quot; 문자 존재)을 확인합니다. |

## 규칙 실행 단계 제어 {#control-rules-execution-phases}

제어 규칙은 전달 라이프사이클의 여러 단계에서 적용할 수 있습니다.

* **타깃팅을 시작할 때**:이 단계에서 제어 규칙을 적용하여 오류가 발생하는 경우 개인화 단계를 실행하지 않을 수 있습니다.

* **타깃팅 후**:타깃팅 후 실행에서는 제어 규칙을 적용하기 위해 대상 볼륨을 알 수 있습니다.

   예를 들어, **검사 증명 크기** 제어 규칙은 타깃팅 단계 다음에 적용됩니다.받는 사람이 너무 많을 경우 메시지 개인화 준비를 방지할 수 있습니다.

* **개인화**&#x200B;시작:검사가 메시지 개인화 승인에 관련된 경우에 적용됩니다. 분석 단계 동안 메시지 개인화가 수행됩니다.

* **분석**&#x200B;종료 시:메시지 개인화를 완료해야 하는 경우
