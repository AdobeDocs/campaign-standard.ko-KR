---
title: 테스트 프로필 관리 및 증명 보내기
description: 테스트 프로파일 및 교정본을 관리하는 방법을 알아봅니다.
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
source-git-commit: 2d8a46a53f2abd453aaf0ff8322b7f9b942ec1c6

---


# 테스트 프로필 관리 및 증명 보내기{#managing-test-profiles-and-sending-proofs}

## 테스트 프로필 정보 {#about-test-profiles}

테스트 프로필을 사용하면 정의된 타깃팅 기준과 일치하지 않는 추가 수신자를 타깃팅할 수 있습니다. 받는 사람 데이터베이스의 부정 사용을 감지하거나 받은 이메일이 받은 편지함에 도착하도록 하기 위해 메시지 대상자에 추가됩니다.

고급 메뉴에서 테스트 프로필을 관리할 수 **[!UICONTROL Profiles & audiences > Test profiles]**있습니다.

테스트 프로필에는 가상 연락처 정보 또는 발신자가 제어하는 연락처 정보가 포함되어 있으며, 이러한 정보는 다음 컨텍스트의 메시지에 사용할 수 있습니다.

* 교정본을 보내는 **경우**:입증은 완료된 전달을 수신자에게 보내기 전에 메시지를 확인하는 데 사용되는 특정 메시지입니다. 증명 테스트 프로필은 해당 컨텐츠 및 형식과 관련하여 배달을 확인하는 역할을 합니다. 교정본 [전송을 참조하십시오](#sending-proofs).
* 이메일 **렌더링의**&#x200B;경우:이메일 렌더링 테스트 프로필은 메시지를 받은 받은 편지함에 따라 메시지가 표시되는 방식을 확인하는 데 사용됩니다. 예: 웹 메일, 메시지 서비스, 모바일 등 이메일 [렌더링을](../../sending/using/email-rendering.md)참조하십시오.

   이메일 **렌더링** 사용은 읽기 전용입니다. 이 기능을 사용하는 테스트 프로필은 Adobe Campaign에서 바로 사용할 수 있습니다.

* 트랩( **As a Trap**):메시지는 기본 타겟으로 전송되는 것처럼 테스트 프로필로 전송됩니다. 트랩 [사용을](#using-traps)참조하십시오.
* 메시지를 **미리** 보려면:개인화 요소를 테스트하기 위한 메시지를 미리 볼 때 테스트 프로필을 선택할 수 있습니다. 메시지 [미리 보기를](/help/sending/using/previewing-messages.md)참조하십시오.

![](assets/test_profile.png)

## 테스트 프로필 관리 {#managing-test-profiles}

### 테스트 프로필 만들기 {#creating-test-profiles}

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 프로필 및 대상 **> 테스트 프로필을** 선택하여 테스트 프로필 목록에 액세스합니다.

   ![](assets/test_profile_creation_1.png)

1. 대시보드에서 **[!UICONTROL Test profiles]**만들기를**&#x200B;클릭합니다&#x200B;**.

   ![](assets/test_profile_creation_2.png)

1. 이 프로필에 대한 데이터를 입력합니다.

   ![](assets/test_profile_creation_3.png)

1. 테스트 프로필에 사용할 용도를 선택합니다.

   ![](assets/test_profile_creation_4.png)

1. 필요한 경우 연락처 채널과 테스트 프로필 주소를 **[!UICONTROL Email, Telephone, Mobile, Mobile app]**입력합니다.

   >[!NOTE]
   >
   >선호하는 이메일 형식을 정의할 수 있습니다. **[!UICONTROL Text]**또는**[!UICONTROL HTML]**.

1. 트랜잭션 메시지의 개인화를 테스트하기 위해 이 테스트 프로필을 사용하려면 이벤트 유형과 이 이벤트에 대한 데이터를 지정하십시오.
1. 을 **[!UICONTROL Create]**클릭하여 테스트 프로필을 저장합니다.

그러면 테스트 프로필이 프로필 목록에 추가됩니다.

**관련 항목:**

[테스트 프로필](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/test-profiles.html) 비디오 만들기

### 테스트 프로필 편집 {#editing-test-profiles}

테스트 프로필을 편집하고 연결된 데이터를 참조하거나 수정하려면:

1. 이미지를 클릭하여 편집할 테스트 프로필을 선택합니다.
1. 필드를 참조하거나 수정합니다.

   ![](assets/test_profile_edit.png)

1. 변경 내용을 **[!UICONTROL Save]**입력한 경우 을 클릭하고 테스트 프로필의 이름을 선택한 다음 화면 상단의**[!UICONTROL Test profiles]** 섹션에서 테스트 프로필 대시보드로 돌아갑니다.

## 교정본 보내기 {#sending-proofs}

증표는 메시지를 기본 타겟으로 보내기 전에 테스트할 수 있도록 하는 특정 메시지입니다.

입증 받는 사람은 메시지(내용 및 양식)를 승인해야 합니다. 테스트 프로필에 **정의됩니다**. 자세한 내용은 테스트 프로필 [관리를](#managing-test-profiles)참조하십시오.

증명을 전송하려면 테스트 프로필을 메시지 대상에 포함해야 합니다.

메시지:

1. 단추를 **[!UICONTROL Send a test]**클릭합니다.

   ![](assets/bat_select.png)

1. 사용할 증명 유형 선택:

   * **[!UICONTROL Email rendering]**:타깃팅된 받은 편지함에 따라 메시지가 수신되는 방식을 테스트하려면 이 옵션을 선택합니다. 자세한 내용은 이메일[렌더링을](../../sending/using/email-rendering.md)참조하십시오.
   * **[!UICONTROL Proof]**:메시지를 기본 타겟으로 보내기 전에 테스트하려면 이 옵션을 선택합니다. 입증 받는 사람은 컨텐츠와 형식을 모두 확인하여 배달을 승인해야 합니다.
   * **[!UICONTROL Proof + Email rendering]**:이 옵션은 두 가지 이전 옵션을 결합합니다.
   ![](assets/bat_select1.png)

1. 선택 사항을 확인합니다.

   교정본을 테스트 프로파일로 보냅니다.

   ![](assets/bat_select2.png)

1. 드롭다운 목록을 사용하여 **[!UICONTROL Proofs]**교정본을 볼 수 있습니다.

   ![](assets/bat_view.png)

1. 요약에 액세스할 증거를 선택합니다. 이메일의 경우 증명 유형으로 [ **이메일 렌더링** ] 옵션을 선택한 경우 **[!UICONTROL Access email rendering]**증명 레이블 오른쪽에 아이콘이 표시됩니다. 이메일[렌더링을](../../sending/using/email-rendering.md)참조하십시오.

   ![](assets/bat_view2.png)

증명을 받은 사람의 주석에 따라 전달 내용을 수정해야 할 수 있습니다. 수정 사항이 실행되면 이메일 준비를 다시 시작한 다음 증거를 다시 보내야 합니다. 이 **[!UICONTROL Show proofs]**단추를 사용하여 새로운 증표에 액세스할 수 있습니다.

필요한 만큼 교정본을 보내야 합니다. 이 작업이 완료되면 배달을 기본 타겟으로 보내고 승인 주기를 닫을 수 있습니다.

**관련 항목:**

[테스트 보내기, 이메일](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html) 비디오 준비 및 보내기

## 트랩 사용 {#using-traps}

트랩을 사용할 때 클라이언트 파일이 부정하게 사용되고 있는지 여부를 식별할 수 있도록 메시지가 기본 타겟으로 전송되는 것처럼 테스트 프로필로 전송됩니다.

트랩은 원래 직접 우편 배달을 위해 고안되었습니다. 이러한 기능을 통해 다음과 같은 이점을 얻을 수 있습니다.
* 다이렉트 메일 공급자가 실제로 통신을 전송하는지 확인합니다.
* 고객과 동일한 조건으로 동시에 이메일을 받을 수 있습니다.
* 보낸 우편물을 정확히 보관한다.
* 클라이언트 목록이 DM 공급자가 잘못 사용되지 않았는지 확인합니다. 실제로 다른 통신이 테스트 프로필의 주소로 전송되면 클라이언트 파일이 사용자 모르게 사용되었을 수 있습니다. 이 때문에 테스트 프로필의 주소를 이 용도로만 사용해야 합니다.

DM 대상에 트랩을 추가하는 방법에 대한 자세한 내용은 테스트 및 [트랩 프로필](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)추가를 참조하십시오.

다른 통신 채널의 경우 다음 작업을 수행하기 위해 기본 대상에 트랩 테스트 프로필을 추가할 수 있습니다.
* 메시지가 성공적으로 전송되었는지 확인합니다.
* 정확한 메시지 사본을 확인하고 보관하십시오.
* 전송 및 수신한 시간을 추적합니다.

테스트 프로필을 트랩으로 사용하려면 메시지 대상에 포함되어야 합니다.

>[!NOTE]
>
>증명 [또는](#sending-proofs) 이메일 렌더링에 [](../../sending/using/email-rendering.md)사용되는 테스트 프로필과 달리 메시지는 기본 타겟과 트랩으로 사용되는 테스트 프로필로 동시에 전송됩니다.

메시지 대상을 정의할 때:

1. 탭에서 테스트 프로필을 **[!UICONTROL Test profiles]**선택합니다. 의도한**[!UICONTROL Trap]** 용도로만 사용해야 합니다.

   ![](assets/trap_select.png)

1. 메시지 내용이 준비되면 **[!UICONTROL Prepare]**단추를 클릭합니다. See[Preparing the send](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >기본 대상을 선택했는지 확인합니다. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. 단추를 **[!UICONTROL Confirm]**클릭합니다. See[Confirming the send](../../sending/using/confirming-the-send.md).

   ![](assets/trap_confirm.png)

메시지는 기본 타겟과 테스트 프로필로 전송됩니다.

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때 메시지의 풍부해진 필드에 대해 해당 추가 데이터가 실제 타깃팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 농축에 대한 자세한 내용은 [이 예를](../../automating/using/enrichment.md#example--enriching-profile-data-with-data-contained-in-a-file)참조하십시오.
