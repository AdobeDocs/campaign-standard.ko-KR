---
title: DM 대상자 정의
description: DM 게재 대상을 정의하는 방법을 배웁니다.
page-status-flag: never-activated
uuid: f843e368-5c07-4b53-8943-46f7bf45b62b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: f993d1b6-4b9a-4f95-81fc-60c126211bd2
context-tags: delivery,directMailContent,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705
workflow-type: ht
source-wordcount: '278'
ht-degree: 100%

---


# DM 대상자 정의{#defining-the-direct-mail-audience}

만들기 마법사에서나 게재 대시보드의 **대상자** 섹션을 클릭하여 대상을 정의할 수 있습니다.

![](assets/direct_mail_15.png)

## 기본 대상 정의 {#defining-the-main-target}

DM의 경우 대상 지정된 프로필은 DM 공급자에게 보낼 추출 파일에 포함될 프로필입니다.

대상 지정된 프로필마다 추출 파일에 새 줄이 추가됩니다. 각 수신자에 대해 포함될 프로필 정보의 양은 [추출 정의](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) 화면에서 정의됩니다.

>[!CAUTION]
>
>우편 주소 정보는 DM 공급자에게 필수이므로 프로필에 포함했는지 확인하십시오. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택했는지 확인하십시오. [권장 사항](../../channels/using/about-direct-mail.md#recommendations)을 참조하십시오.

## 테스트 및 트랩 프로필 추가 {#adding-test-and-trap-profiles}

적은 수의 프로필로 파일을 테스트할 수 있도록 테스트 프로필을 추가합니다. 실제 파일을 준비하기 전에 구조를 테스트하고 유효성 검사를 할 수 있는 파일 샘플을 신속하게 만들 수 있습니다. [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

DM 게재에는 트랩을 사용하는 것이 필수입니다. 트랩을 사용하면 DM 공급자가 실제로 통신을 보내고 있으며 클라이언트 목록을 다른 공급자에게 보내지 않는지 확인할 수 있습니다. [트랩 사용](../../sending/using/using-traps.md)을 참조하십시오.

DM 게재의 경우 추출 중에 트랩이 추가되고 출력 문서에 혼합됩니다. 기본적으로 출력 파일의 정렬 순서에 삽입되지만 파일의 끝이나 시작 부분에 삽입하도록 선택할 수 있습니다. 대상자를 정의할 때 **[!UICONTROL Trap insertion mode]**&#x200B;탭에서 원하는 옵션을 선택합니다.

![](assets/direct_mail_trap_insertion_mode.png)
