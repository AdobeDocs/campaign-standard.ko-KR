---
solution: Campaign Standard
product: campaign
title: 트랩 사용
description: 메시지에 트랩을 사용하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
context-tags: seedMember,overview
feature: 시드 주소
role: User
level: Intermediate
exl-id: 0482a946-35b1-426f-8505-42adcd1c3bbb
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# 트랩 사용 {#using-traps}

트랩을 사용할 때 클라이언트 파일이 사기성으로 사용되는지 여부를 식별하는 방법으로 메시지가 기본 타겟으로 전송되는 것처럼 [테스트 프로필](../../audiences/using/managing-test-profiles.md)에 전송됩니다.

트랩은 원래 DM 게재용으로 설계되었습니다. 이를 통해 다음을 수행할 수 있습니다.

* DM 공급자가 실제로 통신을 보내고 있는지 확인합니다.
* 고객과 동일한 조건으로 동시에 메일을 받습니다.
* 보낸 메일의 정확한 사본을 보관하십시오.
* DM 공급자가 클라이언트 목록을 잘못 사용하지 않는지 확인합니다. 실제로 테스트 프로필의 주소로 다른 통신이 전송되면 클라이언트 파일이 사용자 모르게 사용되었을 수 있습니다. 테스트 프로필의 주소만 이 용도로만 사용해야 하는 이유입니다.

DM 대상에 트랩 추가에 대한 자세한 내용은 [테스트 및 트랩 프로필 추가](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)를 참조하십시오.

다른 통신 채널의 경우 트랩 테스트 프로필을 기본 타겟에 추가하여 다음을 수행할 수 있습니다.

* 메시지를 성공적으로 보냈는지 확인합니다.
* 메시지의 정확한 사본을 가져와 유지합니다.
* 전송 및 수신한 시기를 추적합니다.

테스트 프로필을 트랩으로 사용하려면 메시지 대상자에 포함되어야 합니다.

>[!NOTE]
>
>[증명](../../sending/using/sending-proofs.md) 또는 [이메일 렌더링](../../sending/using/email-rendering.md)에 사용되는 테스트 프로필과 달리, 메시지는 동시에 기본 타겟과 트랩으로 사용되는 테스트 프로필로 전송됩니다.

메시지 대상자를 정의할 때:

1. **[!UICONTROL Test profiles]** 탭에서 테스트 프로필을 선택합니다. 의도한 대로 **[!UICONTROL Trap]** 가 있는지 확인하십시오.

   ![](assets/trap_select.png)

1. 메시지 콘텐츠가 준비되면 **[!UICONTROL Prepare]** 버튼을 클릭합니다. [전송](../../sending/using/preparing-the-send.md) 준비를 참조하십시오.
   >[!NOTE]
   >
   >기본 타겟을 선택했는지 확인합니다. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. **[!UICONTROL Confirm]** 버튼을 클릭합니다. [전송 확인](../../sending/using/confirming-the-send.md)을 참조하십시오.

   ![](assets/trap_confirm.png)

메시지가 기본 타겟 및 테스트 프로필에 전송됩니다.

트랜잭션 메시지를 보낼 때 트랩을 사용할 수 있습니다. 이 경우 테스트 프로필은 이벤트 구성당 하나의 메시지를 수신하게 됩니다. 트랜잭션 메시지에 대한 자세한 내용은 이 [섹션](../../channels/using/getting-started-with-transactional-msg.md)을 참조하십시오.

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때 메시지의 보강된 필드에 대해 해당 추가 데이터는 실제 타겟팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 데이터 보조에 대한 자세한 내용은 [이 예제](../../automating/using/enriching-profile-data-file.md)를 참조하십시오.
