---
title: 교정본 보내기
description: 교정본을 보내는 방법을 살펴보십시오.
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
source-git-commit: f7f90991ed4c7323e3a2f8ac7d38da9ff165ef76

---


# 교정본 보내기 {#sending-proofs}

## 교정본 정보 {#about-proofs}

증표는 메시지를 기본 타겟으로 보내기 전에 테스트할 수 있도록 하는 특정 메시지입니다. 입증 받는 사람은 메시지(내용 및 양식)를 승인해야 합니다.

두 가지 유형의 증명 수신자가 있습니다.

* **테스트 프로필을** 사용하면 정의된 타깃팅 기준과 일치하지 않는 추가 수신자를 타깃팅할 수 있습니다.

   수신자 데이터베이스의 부정 사용을 감지하거나 이메일이 받은 편지함에 도착하도록 메시지 대상에 추가할 수 있습니다. 자세한 내용은 테스트 프로필 [관리를](../../audiences/using/managing-test-profiles.md)참조하십시오.

   >[!NOTE]
   >
   >증명을 전송하려면 테스트 프로필을 메시지 대상에 포함해야 합니다.

* **대체 프로필을** 사용하면 자신을 타깃팅된 프로필 중 하나의 위치에 배치하고 프로필에서 받게 될 메시지를 정확하게 표현할 수 있습니다. 자세한 내용은 타깃팅된 프로필을 [사용하여 이메일 메시지 테스트를 참조하십시오](../../sending/using/testing-messages-using-target.md).

   >[!NOTE]
   >
   >이 기능은 이메일 채널에서만 사용할 수 있습니다.

## 증명 보내기 {#sending-a-proof}

교정본을 보내려면 다음 단계를 따르십시오.

1. 받는 사람이 교정본을 구성했는지 확인합니다.
   * **테스트 프로필은** 메시지 대상에 포함되어야 합니다.
   * **메시지 준비가 성공적으로 완료되면 대체 프로필을** 추가해야 합니다( [이 섹션](../../sending/using/testing-messages-using-target.md)참조).

1. 단추를 **[!UICONTROL Send a test]** 클릭합니다.

   ![](assets/bat_select.png)

1. 사용할 증명 유형 선택:

   * **[!UICONTROL Email rendering]**:타깃팅된 받은 편지함에 따라 메시지가 수신되는 방식을 테스트하려면 이 옵션을 선택합니다. 자세한 내용은 이메일 [렌더링을](../../sending/using/email-rendering.md)참조하십시오.
   * **[!UICONTROL Proof]**:메시지를 기본 타겟으로 보내기 전에 테스트하려면 이 옵션을 선택합니다. 입증 받는 사람은 컨텐츠와 형식을 모두 확인하여 배달을 승인해야 합니다.
   * **[!UICONTROL Proof + Email rendering]**:이 옵션은 두 가지 이전 옵션을 결합합니다.
   ![](assets/bat_select1.png)

   >[!NOTE]
   >
   >이메일 렌더링은 테스트 프로필에서만 사용할 수 있습니다. 메시지에 테스트 프로필이 추가되지 않은 경우 **[!UICONTROL Proof]** 옵션만 선택할 수 있습니다.

1. 선택 사항을 확인합니다.

   교정본은 구성된 수신자에게 전송됩니다.

   ![](assets/bat_select2.png)

1. 드롭다운 목록을 사용하여 **[!UICONTROL Proofs]** 교정본을 볼 수 있습니다.

   ![](assets/bat_view.png)

1. 요약에 액세스할 증거를 선택합니다. 이메일의 경우 증명 유형으로 [ **이메일 렌더링** ] 옵션을 선택한 경우 **[!UICONTROL Access email rendering]** 증명 레이블 오른쪽에 아이콘이 표시됩니다. 이메일 [렌더링을](../../sending/using/email-rendering.md)참조하십시오.

   ![](assets/bat_view2.png)

증명을 받은 사람의 주석에 따라 전달 내용을 수정해야 할 수 있습니다. 수정 사항이 실행되면 이메일 준비를 다시 시작한 다음 증거를 다시 보내야 합니다. 이 **[!UICONTROL Show proofs]** 단추를 사용하여 새로운 증표에 액세스할 수 있습니다.

필요한 만큼 교정본을 보내야 합니다. 이 작업이 완료되면 배달을 기본 타겟으로 보내고 승인 주기를 닫을 수 있습니다.

## 교정본 제목 라인 구성 {#configuring-proofs-subject-line}

증빙 자료가 전송되면 해당 제목 줄은 기본적으로 **&quot;증명&quot;** 접두사와 증명 번호를 나타내는 카운터로 구성됩니다.

![](assets/proof-prefix.png)

사용할 기본 제목 라인을 변경하려면 다음 단계를 따르십시오.

1. 메시지 대시보드에서 **[!UICONTROL Open properties]** 단추를 클릭합니다.
1. 섹션에서 **[!UICONTROL Advanced parameters]** 제목 라인에서 기본적으로 사용할 접두사를 정의합니다.

제목 줄에서 증명 번호를 숨기려면 **[!UICONTROL Hide proof prefix counter]** 옵션을 활성화합니다.

>[!NOTE]
>
>전체 증명 접두사를 숨기려면 **[!UICONTROL Subject line prefix]** 필드를 비워 두십시오.

![](assets/proof-prefix-configuration.png)

1. 클릭 **[!UICONTROL Confirm]**. 선택한 메시지에 대해 전송된 모든 교정쇄에 기본적으로 설정이 적용됩니다.

**관련 항목:**

* [테스트 보내기, 이메일](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html) 비디오 준비 및 보내기
* [타깃팅된 프로파일을](../../sending/using/testing-messages-using-target.md)사용하여 이메일 메시지 테스트
* [테스트 프로필](../../audiences/using/managing-test-profiles.md)관리
* [메시지 미리 보기](../../sending/using/previewing-messages.md)
* [이메일 채널 구성](../../administration/using/configuring-email-channel.md)
