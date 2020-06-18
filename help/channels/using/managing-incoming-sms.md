---
title: 수신 SMS 관리
description: STOP SMS를 관리하고 수신 SMS를 Adobe Campaign에 저장하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: f063052b-96ef-41b6-bf1b-4006de73f0b9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
discoiquuid: ee1970e6-1ced-46e0-94e6-8337768300ee
delivercontext-tags: delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 012546e109b085b7ed968bcefa8f76482656ae0d
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---


# 수신 SMS 관리{#managing-incoming-sms}

## STOP SMS 관리 {#managing-stop-sms}

Campaign을 통해 전송된 SMS 메시지에 프로필 응답이 있으면 수행할 작업은 물론 자동으로 다시 보내지는 메시지를 구성할 수 있습니다.

이 구성은 **[!UICONTROL Automatic reply sent to the MO]** SMS 라우팅 외부 계정 [](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)섹션에 정의되어 있습니다. MO는 모바일 어피티드(Mobile Incorporated)의 개념으로, SMS를 보낸 모바일 사용자에 대한 자동 답글을 구성할 수 있음을 의미합니다.

이렇게 하려면:

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 외부 계정 **[!UICONTROL Administration > Application settings > External accounts]** 을 선택한 다음 **[!UICONTROL SMS routing via SMPP]** 외부 계정을 선택합니다.
1. 카테고리 아래에서 을 **[!UICONTROL Automatic reply sent to the MO]** 클릭하여 자동 회신 **[!UICONTROL Create element]** 구성을 시작합니다.

   ![](assets/sms_mo_1.png)

1. 이 자동 응답을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어 여기에서 수신자가 키워드 &quot;STOP&quot;을 보내면 자동 답글이 전송됩니다.

   키워드가 무엇이든지 동일한 답글을 보내려면 이 열을 비워 두십시오.

   ![](assets/sms_mo_2.png)

1. 필드에서 **[!UICONTROL Short code]** 배달 전송에 주로 사용되는 번호를 지정하고 보낸 사람 이름으로 사용할 번호를 지정합니다. 또한 짧은 코드에 관계없이 동일한 응답을 보내기 위해 **[!UICONTROL Short code]** 열을 비워 둘 수도 있습니다.

   ![](assets/sms_mo_4.png)

1. 필드에 수신자에게 보낼 답변을 입력합니다 **[!UICONTROL Reply]**.

   응답을 보내지 않고 작업을 수행하려면 열을 **[!UICONTROL Reply]** 비워 두십시오. 예를 들어 &quot;STOP&quot; 이외의 메시지로 답글을 쓴 사용자의 전화 번호를 격리하지 않아도 됩니다.

   ![](assets/sms_mo_3.png)

1. 필드에서 작업을 자동 답글에 **[!UICONTROL Additional action]** 연결합니다.

   * 그 **[!UICONTROL Send to quarantine]** 조치는 자동으로 프로필 전화 번호를 격리한다.
   * 이 **[!UICONTROL Remove from quarantine]** 작업을 수행하면 프로필 전화 번호가 격리되지 않습니다.
   * 이 **[!UICONTROL None]** 작업을 수행하면 수신자에게 작업을 전달하지 않고도 메시지를 보낼 수 있습니다.
   예를 들어, 아래 구성에서 수신자가 &quot;STOP&quot; 키워드를 전송하는 경우 구독 취소 확인 메시지가 자동으로 수신되고 전화 번호가 **[!UICONTROL On block list]** 상태가 포함된 검역으로 전송됩니다. 이 상태는 전화 번호만 가리키므로, 프로필이 차단 목록에 추가되지 않으므로 사용자가 계속 이메일 메시지를 수신하게 됩니다.

   ![](assets/sms_mo.png)

이제 수신자는 자동으로 메시지 구독 취소 및 이 자동 회신을 통해 격리 조치를 취할 수 있습니다. 격리된 받는 사람은 **[!UICONTROL Addresses]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** **[!UICONTROL Quarantines]** 메뉴를 통해 사용할 수 있는 표에 나열되어 있습니다. 검역에 대한 자세한 내용은 이 [섹션을 참조하십시오](../../sending/using/understanding-quarantine-management.md).

필요한 경우 이러한 수신 SMS를 저장할 수 있습니다. For more information on this, refer to this [section](#storing-incoming-sms).

## 수신 SMS 저장 {#storing-incoming-sms}

받는 사람 목록에서 제거하기 위해 구독자가 SMS 메시지에 &quot;STOP&quot;을 회신할 때와 같이 **[!UICONTROL SMS routing via SMPP]** 외부 계정에서 수신 메시지를 저장하도록 선택할 수 있습니다.

![](assets/sms_config_mo_1.png)

카테고리 **[!UICONTROL Store incoming MO in the database]** 를 **[!UICONTROL SMPP channel settings]** 체크 인하면 모든 SMS가 inSMS 테이블에 저장되고 워크플로우의 쿼리 활동을 통해 검색할 수 있습니다.

이렇게 하려면:

1. 필드에서 **[!UICONTROL SMPP channel settings]** 확인하십시오 **[!UICONTROL Store incoming MO in the database]**.

   ![](assets/sms_config_mo_2.png)

1. 탭에서 을 **[!UICONTROL Marketing activities]** 클릭한 **[!UICONTROL Create]** 다음 선택합니다 **[!UICONTROL Workflow]**.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. 워크플로우의 속성을 편집한 다음 을 클릭합니다 **[!UICONTROL Create]**. 워크플로우 만들기에 대한 자세한 내용은 이 [섹션을 참조하십시오](../../automating/using/building-a-workflow.md).
1. 활동을 드래그 앤 드롭하고 **[!UICONTROL Query]** 활동을 두 번 클릭합니다.
1. 쿼리의 **[!UICONTROL Properties]** 탭에서 필드 **[!UICONTROL Incoming SMS (inSMS)]** 에서 선택합니다 **[!UICONTROL Resource]** .

   ![](assets/sms_config_mo_4.png)

1. 그런 다음 **[!UICONTROL Target]** 탭에서 규칙을 드래그하여 **[!UICONTROL Incoming SMS attributes]** 놓습니다.

   ![](assets/sms_config_mo_5.png)

1. 여기에서, 우리는 전날의 모든 수신 메시지를 타깃팅하고 싶습니다. 카테고리에서 **[!UICONTROL Field]** 을 선택합니다 **[!UICONTROL Creation date (created)]**.
1. 에서 **[!UICONTROL Filter type]**&#x200B;을 선택한 **[!UICONTROL Relative]** 다음 **[!UICONTROL Level of precision]**&#x200B;에서 을 선택합니다 **[!UICONTROL Day]**.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘, 전일 또는 마지막 며칠 전부터 데이터를 검색할 수 있습니다. 쿼리가 구성되면 **[!UICONTROL Confirm]** 을 클릭합니다.

이 쿼리는 선택한 시간 범위에 따라 수신된 모든 STOP 메시지를 검색합니다.

활동을 통해 예를 들어 모집단 생성 및 게재 개인화를 개선할 수 있습니다.
