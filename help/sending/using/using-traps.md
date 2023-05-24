---
title: 트랩 사용
description: 메시지에 트랩을 사용하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
context-tags: seedMember,overview
feature: Seed Address
role: User
level: Intermediate
exl-id: 0482a946-35b1-426f-8505-42adcd1c3bbb
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 2%

---

# 트랩 사용 {#using-traps}

트랩을 사용할 때 메시지가 [테스트 프로필](../../audiences/using/managing-test-profiles.md) 이는 클라이언트 파일이 부정하게 사용되는지 여부를 식별하기 위한 수단으로 기본 타겟으로 전송됩니다.

트랩은 원래 DM 게재를 위해 디자인되었습니다. 이를 통해 다음을 수행할 수 있습니다.

* DM 공급자가 실제로 통신을 보내고 있는지 확인합니다.
* 고객과 동일한 시간 및 조건으로 메일을 받습니다.
* 보낸 우편물의 정확한 사본을 보관하세요.
* DM 공급자가 클라이언트 목록을 잘못 사용하고 있지 않은지 확인하십시오. 실제로 테스트 프로필의 주소로 다른 커뮤니케이션이 전송되는 경우 클라이언트 파일이 사용자 모르게 사용되었을 수 있습니다. 테스트 프로필의 주소를 이 목적으로만 사용해야 하는 이유입니다.

DM 대상자에 트랩을 추가하는 방법에 대한 자세한 내용은 [테스트 및 트랩 프로필 추가](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles).

다른 통신 채널의 경우 다음과 같은 작업을 수행하기 위해 주 대상에 트랩 테스트 프로필을 추가할 수 있습니다.

* 메시지가 성공적으로 전송되었는지 확인합니다.
* 메시지의 정확한 복사본을 가져와서 보관합니다.
* 보내고 받은 시간을 추적합니다.

테스트 프로필을 트랩으로 사용하려면 테스트 프로필을 메시지 대상자에 포함해야 합니다.

>[!NOTE]
>
>에 사용되는 테스트 프로필과 반대 [증명](../../sending/using/sending-proofs.md) 또는 [전자 메일 렌더링](../../sending/using/email-rendering.md)에서 메시지는 기본 대상과 트랩으로 사용되는 테스트 프로필에 동시에 전송됩니다.

메시지 대상자를 정의할 때:

1. 다음에서 **[!UICONTROL Test profiles]** 탭에서 테스트 프로필을 선택합니다. 이(가) 있는지 확인합니다. **[!UICONTROL Trap]** as the intended의도한 use용도 .

   ![](assets/trap_select.png)

1. 메시지 콘텐츠가 준비되면 **[!UICONTROL Prepare]** 단추를 클릭합니다. 다음을 참조하십시오 [보내기 준비](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >주 대상을 선택했는지 확인하십시오. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. **[!UICONTROL Confirm]** 버튼을 클릭합니다. [전송 확인](../../sending/using/confirming-the-send.md)을 참조하십시오.

   ![](assets/trap_confirm.png)

메시지가 기본 대상과 테스트 프로필에 전송됩니다.

트랜잭션 메시지를 보낼 때 트랩을 사용할 수 있습니다. 이 경우 테스트 프로필은 이벤트 구성당 하나의 메시지를 수신하게 됩니다. 트랜잭션 메시지에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../../channels/using/getting-started-with-transactional-msg.md).

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때 메시지의 보강된 필드에 대해 해당 추가 데이터가 실제 타겟팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 데이터 보강에 대한 자세한 내용은 [이 예](../../automating/using/enriching-profile-data-file.md).
