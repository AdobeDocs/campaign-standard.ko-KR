---
solution: Campaign Standard
product: campaign
title: 테스트 프로필 관리
description: 테스트 프로필을 관리하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
context-tags: seedMember,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 100%

---


# 테스트 프로필 관리 {#managing-test-profiles}

## 테스트 프로필 기본 정보 {#about-test-profiles}

테스트 프로필을 사용하면 정의된 타겟팅 기준과 일치하지 않는 추가 수신자를 타겟팅할 수 있습니다. 수신자 데이터베이스의 부정 사용을 감지하거나 이메일이 받은 편지함에 도착하는지 확인하기 위해 메시지 대상자에 추가됩니다.

고급 메뉴 **[!UICONTROL Profiles & audiences > Test profiles]**&#x200B;에서 테스트 프로필을 관리할 수 있습니다.

테스트 프로필에는 가상 연락처 정보 또는 발신자가 제어하는 연락처 정보가 포함되어 있으므로 다음 컨텍스트의 메시지에 사용할 수 있습니다.

* **증명**&#x200B;을 보내는 경우: 증명은 최종 게재를 수신자에게 보내기 전에 메시지를 확인하는 데 사용되는 특정 메시지입니다. 증명 테스트 프로필은 콘텐츠 및 포맷과 관련한 게재 확인을 담당합니다. [증명 보내기](../../sending/using/sending-proofs.md)를 참조하십시오.
* **이메일 렌더링**&#x200B;의 경우: 이메일 렌더링 테스트 프로필은 메시지를 수신한 받은 편지함에 따라 메시지가 표시되는 방식을 확인하는 데 사용됩니다. 예를 들어 웹 메일, 메시지 서비스, 모바일 등이 있습니다. [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.

   **이메일 렌더링** 사용은 읽기 전용입니다. 이러한 용도의 테스트 프로필은 Adobe Campaign에서 바로 사용할 수 있습니다.

* **트랩**&#x200B;인 경우: 메시지가 기본 타겟으로 전송되는 것처럼 테스트 프로필로 전송됩니다. [트랩 사용](../../sending/using/using-traps.md)을 참조하십시오.
* 메시지 **미리 보기**: 메시지를 미리 보고 개인화 요소를 테스트할 때 테스트 프로필을 선택할 수 있습니다. [메시지 미리 보기](/help/sending/using/previewing-messages.md)를 참조하십시오.

![](assets/test_profile.png)

## 테스트 프로필 만들기 {#creating-test-profiles}

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **프로필 및 대상자 > 테스트 프로필**&#x200B;을 선택하여 테스트 프로필 목록에 액세스합니다.

   ![](assets/test_profile_creation_1.png)

1. **[!UICONTROL Test profiles]** 대시보드에서 **만들기**&#x200B;를 클릭합니다.

   ![](assets/test_profile_creation_2.png)

1. 이 프로필에 대한 데이터를 입력합니다.

   ![](assets/test_profile_creation_3.png)

1. 테스트 프로필의 용도를 선택합니다.

   ![](assets/test_profile_creation_4.png)

1. 필요한 경우 연락처 채널 **[!UICONTROL Email, Telephone, Mobile, Mobile app]** 및 테스트 프로필 주소를 입력합니다.

   >[!NOTE]
   >
   >선호하는 이메일 형식(**[!UICONTROL Text]** 또는 **[!UICONTROL HTML]**)을 정의할 수 있습니다.

1. 트랜잭션 메시지의 개인화를 테스트하는 데 이 테스트 프로필을 사용하려면 이벤트 유형 및 이 이벤트에 대한 데이터를 지정합니다.
1. **[!UICONTROL Create]**&#x200B;를 클릭하여 테스트 프로필을 저장합니다.

그러면 테스트 프로필이 프로필 목록에 추가됩니다.

**관련 항목:**

[테스트 프로필 만들기](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/test-profiles.html) 비디오

## 테스트 프로필 편집 {#editing-test-profiles}

테스트 프로필을 편집하고 연결된 데이터를 참조하거나 수정하려면 다음을 수행합니다.

1. 이미지를 클릭하여 편집할 테스트 프로필을 선택합니다.
1. 필드를 참조하거나 수정합니다.

   ![](assets/test_profile_edit.png)

1. 변경 사항을 입력한 경우 **[!UICONTROL Save]**&#x200B;을(를) 클릭하고 테스트 프로필 이름을 선택한 다음 화면 상단의 섹션에서 **[!UICONTROL Test profiles]**&#x200B;을(를) 클릭하여 테스트 프로필 대시보드로 돌아갑니다.
