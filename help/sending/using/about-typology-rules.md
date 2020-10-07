---
title: 유형화 및 유형화 규칙 기본 정보
description: Adobe Campaign에서 유형화 및 유형화 규칙이 작동하는 방식을 살펴봅니다.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 100%

---


# 유형화 및 유형화 규칙 기본 정보{#about-typology-rules}

Campaign Standard를 사용하면 메시지가 유효하고 품질 기준을 충족하는지 확인하기 위해 메시지를 **유형화**&#x200B;에 연결할 수 있습니다.

유형화는 메시지 분석 단계 동안 실행되는 **유형화 규칙** 세트입니다. 이메일에 항상 특정 요소(예: 구독 취소 링크 또는 제목 줄)가 포함되어 있는지 확인하거나 그룹을 의도한 타겟(구독 취소자, 경쟁 업체 또는 비충성 고객)에서 제외하는 필터링 규칙이 있는지 확인할 수 있습니다.

![](assets/typology_messagelink.png)

Campaign Standard에서는 즉시 사용할 수 있는 유형화 및 유형화 규칙을 사용할 수 있습니다. 필요에 따라 새 규칙을 만들어 기존 또는 새로운 유형화에 추가하여 메시지에 연결할 수도 있습니다.

메시지에 유형화를 만들고 적용하는 단계는 다음과 같습니다.

1. 유형화 규칙을 만듭니다([이 섹션](../../sending/using/managing-typology-rules.md#creating-a-typology-rule) 참조).
1. 유형화를 만들고 유형화로 만든 규칙을 참조합니다([이 섹션](../../sending/using/managing-typologies.md#creating-a-typology) 참조).
1. 생성한 유형화를 사용하도록 게재를 구성합니다([이 섹션](../../sending/using/managing-typologies.md#applying-typologies-to-messages) 참조).
1. 메시지 준비 중에 기준이 충족되면 프로필이 제외됩니다. 로그를 확인하여 제외 사항을 모니터링할 수 있습니다.
