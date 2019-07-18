---
title: 메시지에서 대상 선택
seo-title: 메시지에서 대상 선택
description: 메시지에서 대상 선택
seo-description: '" 이메일 대상을 선택하는 단계별 절차: 기본 타겟 모집단과 테스트 프로필. "'
page-status-flag: 정품 인증 안 함
uuid: 7 D 8 F 8446-F 2 E 0-49 C 1-83 F 1-83 F 6-9667 B 29
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: 관리 대상
discoiquuid: 158 DA 6 FF -8899-4 E 7 B-B 925-8 A 42 C 3 DE 46 A 1
context-tags: Deliverycreation, Wizard; 전달, 고객, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: c9e33f51ab497b8bd111dfc307670f2fde5d804f

---


# Selecting an audience in a message{#selecting-an-audience-in-a-message}

Adobe Campaign 에서는 메시지 대상 내에서 여러 프로필 유형을 구성할 수 있습니다.

대상자는 작성 마법사나 메시지 대시보드에서 메시지를 만들 때 메시지를 만들 때 정의할 수 있습니다.

>[!NOTE]
>
>대상이 워크플로우 내에 구축되어 추가 데이터로 보강된 경우 이러한 데이터를 사용하여 독립형 제공을 개인화할 수 없습니다. 워크플로우에서 실행된 배달에서만 사용할 수 있습니다.

1. 대시보드에서 대상 블록으로 이동하여 시작합니다.

   ![](assets/delivery_audience_definition_1.png)

   그러면 대상을 정의하는 화면이 열립니다. 여기에는 메시지를 받을 각 유형의 대상을 별도로 정의할 수 있는 두 개의 탭이 있습니다.

   * Target
   * 프로파일 테스트
   ![](assets/delivery_audience_definition_2.png)

1. Define the main **[!UICONTROL Target]** of the email. 이메일의 일반 대상 대상입니다.

   The target is defined in the **[!UICONTROL Target]** tab and is made up of identified profiles from your database.

   [쿼리 편집기](../../automating/using/editing-queries.md#creating-queries) 기능을 사용하여 기본 Target를 설정할 수 있습니다.

   In this tab, the **[!UICONTROL Shortcuts]** palette only contains predefined filters and the audiences that have been defined in the identified profiles. **[!UICONTROL Explorer]** 탭에서는 추가 구성에 액세스할 수 있습니다.

   따라서 기존 대상을 다시 사용하고 결합하고 추가 필터를 적용할 수 있습니다.

1. Define the **[!UICONTROL Test profiles]** you want to use for the email. 테스트 프로필은 기본 Target로 보내기 전에 이메일을 테스트하기 전에 전송할 수 있는 증명서를 받게 됩니다.

   For more information on configuring test profiles, refer to the [Test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md) section.

그런 다음 대상 블록이 업데이트되고 해당 이메일에 대해 Target 및 테스트 프로필이 선택되었음을 보여줍니다.

![](assets/delivery_audience_definition_3.png)

