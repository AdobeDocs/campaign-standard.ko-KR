---
title: 최신 릴리스
description: 이 페이지에서는 최신 Campaign Standard 릴리스의 콘텐츠를 자세히 설명합니다
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 93f1a6cb0727859f3c3f645366a9d2dc25795a79
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 20%

---


# 최신 릴리스{#latest-release}

![컨트롤 패널](assets/do-not-localize/cp-icon.png) **새로운 컨트롤 패널 릴리스**. [자세히 알아보기](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=ko){target=&quot;_blank&quot;}.


## 릴리스 22.3 - 2022년 가을/겨울 {#sept-22}

### 개선 사항{#rn-improvements}

**접근성**

Campaign Standard 22.3에는 사용자가 Adobe Campaign을 탐색하고 최대한 활용할 수 있는 액세스 가능성 수정 사항과 개선 사항이 포함되어 있습니다.

이러한 기능은 Limited Availability에서 출시되며 고객 집합에만 출시됩니다. Campaign 환경에서 이러한 개선 사항을 활성화하려면 Adobe 담당자에게 문의하십시오.

<!--
* **Data retention**

    Data retention periods have been reduced to avoid overloading Campaign server. However, you can still modify these values and define a custom period of time based on your needs and data retention policies. To change retention periods, contact Adobe.
-->

### 보안 업데이트{#rn-security}

이 릴리스는 다음과 같은 보안 업그레이드와 함께 제공됩니다. Apache Tomcat이 v7.0에서 v8.0으로 업그레이드되었습니다.

### 수정 사항{#e-rn-fixes}

* 예약된 시간보다 1시간 전에 트리거된 예약된 보고서 문제를 수정했습니다. (CAMP-51502)
* 전송 로그(nms:broadLogRcp)와 일치하지 않는 게재 대시보드의 게재 표시기에 대한 문제를 해결했습니다. (CAMP-51127)
* ACS 커넥터(Prime Offer)에서 사용자 지정 리소스 확장을 할 수 없는 문제를 해결했습니다. (CAMP-51033)
* 지연을 방지하기 위해 개인 정보 보호 요청 응답에 대한 게시 프로세스를 개선했습니다. (CAMP-50613)

