---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard의 접근성
description: Adobe Campaign Standard Workspace의 접근성 지원에 대해 알아봅니다.
audience: designing
content-type: reference
topic-tags: accessibility
translation-type: tm+mt
source-git-commit: 6632216ce4697892ea08b32641c9c026482ca713
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 100%

---


# Adobe Campaign Standard의 접근성 {#accessibility-acs}

Adobe Campaign Standard Workspace의 접근성 지원에 대해 알아봅니다.

접근성이란 시각, 청각, 인지 또는 기타 장애가 있거나 거동이 불편한 사용자가 제품을 사용할 수 있게 하는 것을 의미합니다. 소프트웨어 제품에 사용되는 접근성 기능으로는 화면 판독기 지원, 그래픽을 대신할 텍스트, 키보드 단축키, 디스플레이 색상의 고대비 변경 등이 있습니다.

Adobe Campaign Standard에서는 대비, 키보드 탐색, 상황별 도움말 및 반응형 크기 조정과 같이 접근성을 지원하는 데 사용되는 일부 도구를 제공합니다.

## 접근성 기능 {#accessibility-features}

### 대비 {#contrast}

Adobe Campaign Standard 사용자 인터페이스에서는 저시력 또는 색각 이상이 있는 사용자가 편하게 볼 수 있도록 애플리케이션의 충분한 대비를 제공하려 노력하고 있습니다.

* 배경색과 전경색 간의 대비를 개선하기 위해 워크플로우의 일시 중지 및 취소 아이콘이 업데이트되었습니다.

   ![](assets/accessibility_1.png)

* 게재가 성공적일 때 표시되는 텍스트에는 배경색과 전경색 간의 대비가 적은 큰 녹색 텍스트가 포함되어 있습니다. 대비가 최소 3:1 비율로 업데이트되었습니다.

   ![](assets/accessibility_2.png)

* Adobe Campaign Standard에서는 색상, 모양 또는 위치뿐만 아니라 다른 방법으로도 정보나 계층 구조를 전달할 수 있도록 합니다.

### 사용자 인터페이스 {#user-interface}

Adobe Campaign Standard 사용자 인터페이스를 사용하면 사용자는 배경색과 전경색을 구분하고 사용 가능한 다양한 버튼에 대체 텍스트를 추가하는 등 콘텐츠를 손쉽게 보고 들을 수 있습니다.

* 사용자가 필수 ID 필드를 비워 두면 그래픽은 오류 메시지 텍스트로 오류가 있는 필드를 시각적으로 나타냅니다.

   ![](assets/accessibility_3.png)

* 마우스로 가리키거나 초점이 맞춰진 콘텐츠는 사용자가 해제할 수 있으며 다른 콘텐츠를 가리지 않습니다.

   ![](assets/accessibility_4.png)

* 이미지 버튼에 대한 대체 텍스트가 추가되었으며 일러스트레이션을 보는 대신 읽을 수 있습니다.

   ![](assets/accessibility_5.png)

* 목록 사용 시 데이터 테이블 헤더 셀이 테이블 모서리에 비어 있는 상태로 남아 있지 않습니다.

### 여러 디바이스에 대한 반응형 크기 조정 만들기 {#resize-devices}

여러 디바이스와 플랫폼에 배포할 콘텐츠를 디자인할 때는 모바일 및 데스크톱 해상도의 전반에 걸쳐 화면 크기에 맞는 원활한 경험을 만들어야 합니다.

Adobe Campaign Standard을 사용하면 iPhone, Android 디바이스, iPad, Android 태블릿 및 데스크톱과 같은 다양한 디바이스에서 이메일 및 푸시 알림을 디자인하고 테스트할 수 있습니다.

![](assets/accessibility_6.png)

## 상황별 도움말 {#contextual-help}

상황별 도움말은 사용할 수 있는 다양한 요청된 필드 및 기능을 이해하는 데 도움이 됩니다. 또한 선택된 기능의 자세한 내용을 알아보기 위한 제품 설명서로 안내합니다.

이메일을 디자인할 때 커서를 정보 단추 위에 올리면 됩니다. 기능 설명 및 제품 설명서에 대한 링크를 제공하는 도구 설명이 나타납니다.

![](assets/accessibility_7.png)

## 화면 돋보기 지원 {#screen-magnifiers}

화면 읽기 프로그램은 컴퓨터 화면에 나타나는 텍스트를 읽습니다. 또한 접근성 태그나 특성으로 제공되는 애플리케이션의 단추 레이블이나 이미지 설명과 같은 텍스트가 아닌 정보를 읽습니다.

Adobe Campaign Standard에서는 사용자가 텍스트 간격 속성을 무시해도 여전히 콘텐츠와 기능을 사용할 수 있습니다.

## 원하는 언어로 작업 {#languages}

Adobe Campaign Standard는 영어, 프랑스어 및 독일어의 다양한 언어로 제공됩니다.

설치 시 언어가 설정되고 나중에 변경할 수 없습니다.

## 단축키{#shortcuts}

### 홈페이지 {#homepage-shortcuts}

| 단축키 | 작업 |
|:-:|:-:|
| 탭 | 사용자 인터페이스의 개별 요소 탐색 |
| Enter 키 또는 스페이스바 | 선택한 항목 활성화 |

### 이메일 디자이너 {#email-designer-shortcuts}

| 단축키 | 작업 |
|:-:|:-:|
| CTRL + Z | 실행 취소 |
| CTRL + Y | 다시 실행 |

### 동적 보고서 {#report-shortcuts}

| 단축키 | 작업 |
|:-:|:-:|
| CTRL + O | 프로젝트 열기 |
| CTRL + S | 저장. |
| Shift + CTRL + S | 다른 이름으로 저장 |
| Alt + R | 프로젝트 새로 고침 |
| Shift + CTRL + V | CSV 다운로드 |
| Alt + P | 인쇄 |
| CTRL + Z | 실행 취소 |
| CTRL + Shift + Z | 다시 실행 |
| Alt + B | 새 빈 패널 |
| Alt + A | 새 자유형 |
| Alt + 1 | 새 자유형 테이블 |
| Alt + 2 | 새 줄 |
| Alt + 3 | 새 막대 |
| Alt + S | 지금 보고서 전송 |
| Shift + Alt + S | 일정에 따라 보고서 전송 |
| Shift = Alt + L | 예약된 보고서 |

## 추가 읽기{#further-reading}

Adobe Campaign Standard는 모든 사용자가 쉽게 사용할 수 있도록 항상 증가하는 접근성 수준을 제공하기 위해 노력하고 있습니다.

개선 사항 제안 및 사용 중인 접근성의 문제를 Adobe에 보내려면 [Adobe 접근성 피드백 양식](https://www.adobe.com/accessibility/feedback.html)을 사용하는 것이 좋습니다.

최신 개선 사항 및 기능을 따라가려면 [Adobe Campaign Standard 릴리스 노트](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/release-notes.html?lang=ko#release-notes)를 참조할 수도 있습니다.