---
title: 유형 및 유형 규칙 정보
description: Adobe Campaign에서 유형 및 유형 분류 규칙이 작동하는 방식을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a9c0e3cc4609e747bbfebeb90049862f29c9d8d9

---


# 유형 및 유형 규칙 정보{#about-typology-rules}

Campaign Standard를 사용하면 메시지가 **유효하고 품질 기준을 충족하는지**&#x200B;확인하기 위해 메시지를 유형에 연결할 수 있습니다.

유형 분류는 메시지 분석 단계 동안 실행되는 **유형 규칙**&#x200B;세트입니다. 이러한 기능을 사용하면 이메일에 항상 특정 요소(예: 가입 해지 링크 또는 제목 줄)를 포함하거나 필터링 규칙을 적용하여 의도한 타겟(비가입자, 경쟁업체 또는 비충성도 고객)에서 그룹을 제외할 수 있습니다.

![](assets/typology_messagelink.png)

바로 사용할 수 있는 유형 및 유형 분류 규칙을 Campaign Standard에서 사용할 수 있습니다. 필요에 따라 새 규칙을 만들어 기존 유형 또는 새 유형에 추가하여 메시지에 연결할 수도 있습니다.

메시지에 유형을 생성하고 적용하는 단계는 다음과 같습니다.

1. 유형 규칙을 만듭니다( [이 섹션](../../sending/using/managing-typology-rules.md#creating-a-typology-rule)참조).
1. 유형을 만들고 여기에 만든 규칙을 참조합니다( [이 섹션](../../sending/using/managing-typologies.md#creating-a-typology)참조).
1. 만든 유형을 사용하도록 배달 구성( [이 섹션](../../sending/using/managing-typologies.md#applying-typologies-to-messages)참조).
1. 메시지 준비 중에, 기준이 충족될 때 프로필이 제외됩니다. 로그를 확인하여 제외를 모니터링할 수 있습니다.
