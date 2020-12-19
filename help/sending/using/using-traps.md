---
solution: Campaign Standard
product: campaign
title: 트랩 사용
description: 메시지에 트랩 사용 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
context-tags: seedMember,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 2%

---


# 트랩 사용 {#using-traps}

트랩을 사용할 때 메시지는 클라이언트 파일이 잘못 사용되고 있는지 여부를 식별할 수 있는 수단으로 기본 타겟으로 보내지는 것처럼 [테스트 프로필](../../audiences/using/managing-test-profiles.md)에 전송됩니다.

원래 함정은 다이렉트 메일 배달을 위해 고안되었다. 이러한 기능을 통해 다음과 같은 이점을 얻을 수 있습니다.

* 다이렉트 메일 공급자가 실제로 통신을 전송하는지 확인합니다.
* 동시에 고객과 동일한 조건으로 이메일을 받습니다.
* 보낸 우편물의 정확한 사본을 보관하십시오.
* 클라이언트 목록이 DM 공급자가 잘못 사용되지 않았는지 확인합니다. 실제로 다른 통신이 테스트 프로필의 주소로 전송되면 클라이언트 파일이 사용자 모르게 사용되었을 수 있습니다. 테스트 프로필의 주소를 이 용도로만 사용해야 하는 이유입니다.

DM 대상에 트랩 추가에 대한 자세한 내용은 [테스트 및 트랩 프로필 추가](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)를 참조하십시오.

다른 통신 채널의 경우 다음 작업을 수행하기 위해 기본 대상에 트랩 테스트 프로필을 추가할 수 있습니다.

* 메시지가 성공적으로 전송되었는지 확인합니다.
* 메시지의 정확한 사본을 가져와 보관할 수 있습니다.
* 전송 및 수신한 시간을 추적합니다.

테스트 프로필을 트랩으로 사용하려면 메시지 대상에 포함되어야 합니다.

>[!NOTE]
>
>[propots](../../sending/using/sending-proofs.md) 또는 [이메일 렌더링](../../sending/using/email-rendering.md)에 사용되는 테스트 프로필과는 달리, 메시지는 동시에 주 타겟과 트랩으로 사용되는 테스트 프로필로 전송됩니다.

메시지 대상을 정의할 때:

1. **[!UICONTROL Test profiles]** 탭에서 테스트 프로필을 선택합니다. 의도한 대로 **[!UICONTROL Trap]**&#x200B;이(가) 있는지 확인합니다.

   ![](assets/trap_select.png)

1. 메시지 내용이 준비되면 **[!UICONTROL Prepare]** 단추를 클릭합니다. [보내기](../../sending/using/preparing-the-send.md) 준비를 참조하십시오.
   >[!NOTE]
   >
   >기본 대상을 선택했는지 확인합니다. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. **[!UICONTROL Confirm]** 버튼을 클릭합니다. [전송 확인](../../sending/using/confirming-the-send.md)을 참조하십시오.

   ![](assets/trap_confirm.png)

메시지는 주 타겟과 테스트 프로필로 전송됩니다.

트랜잭션 메시지를 보낼 때 트랩을 사용할 수 있습니다. 이 경우 테스트 프로필은 이벤트 구성당 하나의 메시지를 수신합니다. 트랜잭션 메시지에 대한 자세한 내용은 이 [섹션](../../channels/using/getting-started-with-transactional-msg.md)을 참조하십시오.

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때 메시지의 모든 농축 필드에 대해 해당 추가 데이터가 실제 타깃팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 농축에 대한 자세한 내용은 [이 예제](../../automating/using/enriching-profile-data-file.md)를 참조하십시오.
