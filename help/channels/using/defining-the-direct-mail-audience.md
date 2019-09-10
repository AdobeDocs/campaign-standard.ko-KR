---
title: 다이렉트 메일 대상 정의
seo-title: 다이렉트 메일 대상 정의
description: 다이렉트 메일 대상 정의
seo-description: 다이렉트 메일 게재의 대상을 정의하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: F 843 E 368-5 C 07-4 B 53-8943-46 F 7 BF 45 B 62 B
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: DM
discoiquuid: F 993 D 1 B 6-4 B 9 A -4 F 95-81 FC -60 C 126211 BD 2
context-tags: 전달, Directmailcontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 27447db9ee0dd387c39976c7bd4e157a4b7899b8

---


# 다이렉트 메일 대상 정의{#defining-the-direct-mail-audience}

만들기 마법사에서 대상을 정의하거나 배달 대시보드의 **대상** 섹션을 클릭하여 대상을 정의할 수 있습니다.

![](assets/direct_mail_15.png)

## 기본 타겟 정의 {#defining-the-main-target}

다이렉트 메일의 경우, 타깃팅된 프로필은 다이렉트 메일 공급자에게 전송할 추출 파일에 포함될 프로필입니다.

타깃팅된 각 프로필에 대해 추출 파일에 새 라인이 추가됩니다. 각 수신자에 대해 포함될 프로필 정보의 양은 [추출](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) 화면 정의에 정의됩니다.

>[!CAUTION]
>
>다이렉트 메일 제공업체에 반드시 필요한 정보가 프로필에 포함되어야 합니다. 프로필 정보에서 **[!UICONTROL Address specified]** 상자를 선택했는지 확인하십시오. [권장 사항을 참조하십시오](../../channels/using/about-direct-mail.md#recommendations).

## 테스트 및 트랩 프로필 추가 {#adding-test-and-trap-profiles}

적은 수의 프로필로 파일을 테스트할 수 있도록 테스트 프로필을 추가합니다. 이를 통해 파일 샘플을 신속하게 작성하여 실제 파일을 준비하기 전에 구조를 테스트하고 확인할 수 있습니다. 테스트 프로필 [관리 및 증명 전송을 참조하십시오](../../sending/using/managing-test-profiles-and-sending-proofs.md).

트랩의 사용은 메일 배달을 위해 필수적입니다. 이를 통해 다이렉트 메일 공급자가 통신을 실제로 보내고 있으며 클라이언트 목록을 다른 공급자에게 보내지 않는지 확인할 수 있습니다. 트랩 [사용을 참조하십시오](../../sending/using/managing-test-profiles-and-sending-proofs.md#using-traps).

다이렉트 메일 배달의 경우, 추출 동안 트랩이 추가되고 출력 문서에서 믹스가 혼합됩니다. 기본적으로 출력 파일의 정렬 순서에 삽입되지만, 파일의 끝 또는 끝 부분에 삽입하도록 선택할 수 있습니다. 대상자를 정의할 때 **[!UICONTROL Trap insertion mode]** 탭에서 원하는 옵션을 선택합니다.

![](assets/direct_mail_trap_insertion_mode.png)
