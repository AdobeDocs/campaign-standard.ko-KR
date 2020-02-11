---
title: DM 대상자 정의
description: DM 전달 대상을 정의하는 방법을 알아봅니다.
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
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# DM 대상자 정의{#defining-the-direct-mail-audience}

생성 마법사에서 또는 전달 대시보드의 대상자 **섹션을 클릭하여 대상을** 정의할 수 있습니다.

![](assets/direct_mail_15.png)

## 기본 대상 정의 {#defining-the-main-target}

DM의 경우 대상 프로필은 DM 공급자에게 보낼 추출 파일에 포함될 프로필입니다.

각 대상 프로필에 대해 추출 파일에 새 줄이 추가됩니다. 각 수신자에 대해 포함될 프로파일 정보의 양은 추출 정의 [화면에 정의됩니다](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) .

>[!CAUTION]
>
>이 정보는 다이렉트 메일 제공업체에 필수이므로 프로필에 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택했는지 확인하십시오. 권장 사항을 [참조하십시오](../../channels/using/about-direct-mail.md#recommendations).

## 테스트 및 트랩 프로파일 추가 {#adding-test-and-trap-profiles}

적은 수의 프로파일로 파일을 테스트할 수 있도록 테스트 프로필을 추가합니다. 이 플러그인을 사용하면 실제 파일을 준비하기 전에 구조를 테스트하고 확인할 수 있는 파일 샘플을 신속하게 만들 수 있습니다. 테스트 [프로필](../../audiences/using/managing-test-profiles.md)관리를 참조하십시오.

우편 배달은 덫을 사용하는 것이 필수적이다. 이러한 기능을 사용하면 다이렉트 메일 공급자가 실제로 통신을 보내고 있는지, 그리고 해당 공급자가 클라이언트 목록을 다른 공급자에게 보내지 않는지 확인할 수 있습니다. 트랩 [사용을](../../sending/using/using-traps.md)참조하십시오.

DM 전달의 경우 추출 중에 트랩이 추가되고 출력 문서에 혼합됩니다. 기본적으로 출력 파일의 정렬 순서에 삽입되지만 파일의 끝이나 시작 부분에 삽입하도록 선택할 수 있습니다. 대상을 정의할 때 **[!UICONTROL Trap insertion mode]** 탭에서 원하는 옵션을 선택합니다.

![](assets/direct_mail_trap_insertion_mode.png)
