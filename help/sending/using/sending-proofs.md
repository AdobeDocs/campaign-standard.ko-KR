---
title: 증명 보내기
description: 증명을 보내는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a07ccaf864c3aef881cb02042b5e00a43c48f0a9
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 100%

---


# 증명 보내기 {#sending-proofs}

## 증명 정보 {#about-proofs}

증명은 메시지를 주요 타겟에게 보내기 전에 테스트하기 위해 사용할 수 있는 메시지입니다. 증명의 수신자는 메시지(콘텐츠 및 양식)를 승인해야 합니다.

증명 수신자에는 두 유형이 있습니다.

* **테스트 프로필**&#x200B;을 사용하면 정의한 타겟팅 기준과 일치하지 않는 추가 수신자를 타겟팅할 수 있습니다.

   이들을 메시지의 대상자에 추가하여 수신자 데이터베이스의 부정 사용을 찾아내거나 이메일이 받은 편지함에 잘 도착하는지 확인할 수 있습니다. 자세한 내용은 [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

   >[!NOTE]
   >
   >증명을 보내려면 테스트 프로필을 메시지 대상자에 포함해야 합니다.

* **대체 프로필**&#x200B;을 사용하면 자신을 타겟팅 프로필 중 하나의 위치에 배치하여 프로필에서 받게 될 메시지의 정확한 모습을 확인할 수 있습니다. 자세한 내용은 [타겟팅된 프로필을 사용하여 이메일 메시지 테스트](../../sending/using/testing-messages-using-target.md)를 참조하십시오.

   >[!NOTE]
   >
   >이 기능은 이메일 채널에서만 사용할 수 있습니다.

## 증명 보내기 {#sending-a-proof}

증명을 보내려면 다음 단계를 따르십시오.

1. 증명 수신자를 구성했는지 확인합니다.
   * **테스트 프로필**&#x200B;은 메시지 대상자에 포함되어야 합니다.
   * **대체 프로필**&#x200B;은 메시지를 성공적으로 준비한 이후에 추가해야 합니다([이 섹션](../../sending/using/testing-messages-using-target.md) 참조).

1. **[!UICONTROL Send a test]** 버튼을 클릭합니다.

   ![](assets/bat_select.png)

1. 사용할 증명 유형을 선택합니다.

   * **[!UICONTROL Email rendering]**: 이 옵션을 선택하면 타겟팅한 받은 편지함에 따른 메시지 수신 방식을 테스트할 수 있습니다. 자세한 내용은 [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.
   * **[!UICONTROL Proof]**: 이 옵션을 선택하면 메시지를 주요 타겟에게 보내기 전에 테스트할 수 있습니다. 증명 수신자는 게재의 콘텐츠와 포맷을 모두 확인하여 승인해야 합니다. 
   * **[!UICONTROL Proof + Email rendering]**: 이 옵션은 앞의 두 옵션을 결합합니다.

   ![](assets/bat_select1.png)

   >[!NOTE]
   >
   >이메일 렌더링은 테스트 프로필에서만 사용할 수 있습니다. 메시지에 테스트 프로필이 추가되지 않은 경우 **[!UICONTROL Proof]** 옵션만 선택할 수 있습니다.

1. 선택을 확인합니다.

   구성한 수신자에게 증명이 보내집니다.

   ![](assets/bat_select2.png)

1. **[!UICONTROL Proofs]** 드롭다운 목록을 사용하여 증명을 볼 수 있습니다.

   ![](assets/bat_view.png)

1. 증명을 선택하여 요약에 액세스합니다. 이메일의 경우, 증명 유형으로 **이메일 렌더링** 옵션을 선택했다면 증명의 레이블 오른쪽에 **[!UICONTROL Access email rendering]** 아이콘이 표시됩니다. [이메일 렌더링](../../sending/using/email-rendering.md)을 참조하십시오.

   ![](assets/bat_view2.png)

증명을 받은 사람의 의견에 따라 게재 콘텐츠를 수정해야 할 수도 있습니다. 수정을 완료하면 이메일 준비를 다시 시작한 다음 증명을 다시 보내야 합니다. 새로 만든 증명 각각에는 **[!UICONTROL Show proofs]** 버튼을 사용하여 액세스할 수 있습니다.

게재 콘텐츠를 완성할 때까지 필요한 만큼 증명을 보내야 합니다. 이를 마치고 나면 주요 타겟에게 게재를 보내고 승인 절차를 마무리할 수 있습니다.

## 증명 제목란 구성 {#configuring-proofs-subject-line}

증명을 보낼 때 제목란은 기본적으로 **“증명”** 접두사와 증명 번호를 나타내는 숫자로 구성됩니다.

![](assets/proof-prefix.png)

사용할 기본 제목을 변경하려면 다음 단계를 수행하십시오.

1. 메시지 대시보드에서 **[!UICONTROL Open properties]** 버튼을 클릭합니다.
1. **[!UICONTROL Advanced parameters]** 섹션에서 제목란에 기본적으로 사용할 접두사를 정의합니다.

제목란에서 증명 번호를 숨기려면 **[!UICONTROL Hide proof prefix counter]** 옵션을 활성화합니다.

>[!NOTE]
>
>전체 증명 접두사를 숨기려면 **[!UICONTROL Subject line prefix]** 필드를 비워 둡니다.

![](assets/proof-prefix-configuration.png)

1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다. 이 설정은 선택 메시지에 대해 보내는 모든 증명에 기본적으로 적용됩니다.

**관련 항목:**

* [테스트 보내기, 이메일 준비 및 보내기](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html) 비디오
* [타겟팅된 프로필을 사용하여 이메일 메시지 테스트](../../sending/using/testing-messages-using-target.md)
* [테스트 프로필 관리](../../audiences/using/managing-test-profiles.md)
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [이메일 채널 구성](../../administration/using/configuring-email-channel.md)
