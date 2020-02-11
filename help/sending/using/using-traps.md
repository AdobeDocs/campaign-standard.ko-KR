---
title: 트랩 사용
description: 메시지에 트랩을 사용하는 방법을 알아봅니다.
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
source-git-commit: ff9d0c3ca42606f097a34b1835d285541061e57b

---


# 트랩 사용 {#using-traps}

트랩을 사용할 때 메시지는 클라이언트 파일이 부정하게 사용되고 있는지 여부를 식별할 수 있는 수단으로 기본 타겟으로 전송되는 것처럼 [테스트 프로필로](../../audiences/using/managing-test-profiles.md) 전송됩니다.

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
>증명 [또는](../../sending/using/sending-proofs.md) 이메일 렌더링에 [](../../sending/using/email-rendering.md)사용되는 테스트 프로필과 달리 메시지는 기본 타겟과 트랩으로 사용되는 테스트 프로필로 동시에 전송됩니다.

메시지 대상을 정의할 때:

1. 탭에서 테스트 프로필을 **[!UICONTROL Test profiles]** 선택합니다. 의도한 **[!UICONTROL Trap]** 용도로만 사용해야 합니다.

   ![](assets/trap_select.png)

1. 메시지 내용이 준비되면 **[!UICONTROL Prepare]** 단추를 클릭합니다. See [Preparing the send](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >기본 대상을 선택했는지 확인합니다. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. 단추를 **[!UICONTROL Confirm]** 클릭합니다. See [Confirming the send](../../sending/using/confirming-the-send.md).

   ![](assets/trap_confirm.png)

메시지는 기본 타겟과 테스트 프로필로 전송됩니다.

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때 메시지의 풍부해진 필드에 대해 해당 추가 데이터가 실제 타깃팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 농축에 대한 자세한 내용은 [이 예를](../../automating/using/enrichment.md#example--enriching-profile-data-with-data-contained-in-a-file)참조하십시오.
