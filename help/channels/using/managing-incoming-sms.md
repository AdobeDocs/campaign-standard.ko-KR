---
title: 수신 SMS 관리
description: Adobe Campaign에서 STOP SMS를 관리하고 수신 SMS를 저장하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: f063052b-96ef-41b6-bf1b-4006de73f0b9
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: sms 메시지
discoiquuid: ee1970e6-1advanced-46e0-94e6-8337768300ee
delivercontext-tags: 전달,smsContent,뒤로
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 수신 SMS 관리{#managing-incoming-sms}

## STOP SMS 관리 {#managing-stop-sms}

Adobe Campaign을 통해 전송된 SMS 메시지에 프로필로 회신할 때 수행할 작업은 물론 본인에게 자동으로 전송되는 메시지를 구성할 수 있습니다.

이 구성은 SMS 라우팅 **[!UICONTROL Automatic reply sent to the MO]** 외부 계정의 [](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)섹션에 정의됩니다. MO는 '모바일 출처'를 의미하며, 이는 SMS를 보낸 모바일에 자동 회신을 구성할 수 있음을 의미합니다.

이렇게 하려면 다음을 수행하십시오.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration > Application settings > External accounts]** 외부 계정을 **[!UICONTROL SMS routing via SMPP]** 차례로 선택합니다.
1. 카테고리 아래에서 을 클릭하여 자동 회신 구성을 **[!UICONTROL Automatic reply sent to the MO]** **[!UICONTROL Create element]** 시작합니다.

   ![](assets/sms_mo_1.png)

1. 이 자동 회신을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어 여기에서 받는 사람이 "STOP" 키워드를 전송하는 경우 자동 답글을 받게 됩니다.

   키워드가 무엇인지에 관계없이 동일한 답글을 보내려면 이 열을 비워 두십시오.

   ![](assets/sms_mo_2.png)

1. 필드에서 일반적으로 납품을 보내는 데 사용되는 번호를 지정하고 발신자 이름으로 사용할 번호를 지정합니다. **[!UICONTROL Short code]** 또한 짧은 코드에 관계없이 동일한 답글을 보내도록 **[!UICONTROL Short code]** 열을 비워 둘 수도 있습니다.

   ![](assets/sms_mo_4.png)

1. 필드에 수신자에게 보낼 답변을 입력합니다 **[!UICONTROL Reply]**.

   응답을 보내지 않고 작업을 수행하려면 **[!UICONTROL Reply]** 열을 비워 두십시오. 예를 들어 "STOP" 이외의 메시지로 답글을 보낸 사용자의 전화 번호를 격리 조치에서 제거할 수 있습니다.

   ![](assets/sms_mo_3.png)

1. 필드에서 작업을 자동 답글에 **[!UICONTROL Additional action]** 연결합니다.

   * 그 **[!UICONTROL Send to quarantine]** 조치는 자동으로 프로필 전화 번호를 격리한다.
   * 이렇게 **[!UICONTROL Remove from quarantine]** 하면 프로필 전화 번호가 격리되지 않습니다.
   * 이 **[!UICONTROL None]** 작업을 통해 수신자에게 작업을 전달하지 않고도 메시지를 보낼 수 있습니다.
   예를 들어 아래 구성에서 수신자가 "STOP" 키워드를 전송하는 경우 구독 취소 확인 메시지를 자동으로 받게 되고 전화 번호가 **[!UICONTROL Blacklisted]** 상태가 포함된 검역으로 전송됩니다. 이 상태는 전화 번호만 참조하며, 프로필이 블랙리스트에 추가되지 않아 사용자가 이메일 메시지를 계속 수신하게 됩니다.

   ![](assets/sms_mo.png)

이제 수신자는 자동으로 메시지 구독 취소 및 이 자동 회신을 통해 격리 조치를 취할 수 있습니다. 격리된 수신자는 **[!UICONTROL Addresses]** &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** 메뉴를 통해 사용할 수 있는 **[!UICONTROL Quarantines]** 표에 나열됩니다. 검역에 대한 자세한 내용은 이 [절을](../../sending/using/understanding-quarantine-management.md)참조하십시오.

이러한 수신 SMS는 필요한 경우 저장할 수 있습니다. 자세한 내용은 이 [섹션을](#storing-incoming-sms)참조하십시오.

## 수신 SMS 저장 {#storing-incoming-sms}

외부 계정에서 수신자 목록에서 제거하기 위해 구독자가 SMS 메시지에 "STOP"을 회신(를) 보낼 때와 같이 수신 메시지를 저장하도록 선택할 수 있습니다. **[!UICONTROL SMS routing via SMPP]**

![](assets/sms_config_mo_1.png)

카테고리를 **[!UICONTROL Store incoming MO in the database]** **[!UICONTROL SMPP channel settings]** 체크 인하면 모든 SMS가 inSMS 테이블에 저장되고 워크플로우의 쿼리 활동을 통해 검색할 수 있습니다.

이렇게 하려면 다음을 수행하십시오.

1. 필드에서 **[!UICONTROL SMPP channel settings]** 확인하십시오 **[!UICONTROL Store incoming MO in the database]**.

   ![](assets/sms_config_mo_2.png)

1. 탭에서 을 **[!UICONTROL Marketing activities]** 클릭한 다음 **[!UICONTROL Create]** **[!UICONTROL Workflow]**&#x200B;선택합니다.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. 워크플로우의 속성을 편집한 다음 을 클릭합니다 **[!UICONTROL Create]**. 워크플로우 생성에 대한 자세한 내용은 이 [섹션을](../../automating/using/building-a-workflow.md)참조하십시오.
1. 활동을 드래그 앤 드롭하고 활동을 두 번 클릭합니다. **[!UICONTROL Query]**
1. 쿼리의 **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Incoming SMS (inSMS)]** **[!UICONTROL Resource]** 필드를 선택합니다.

   ![](assets/sms_config_mo_4.png)

1. 그런 다음 **[!UICONTROL Target]** 탭에서 규칙을 드래그하여 **[!UICONTROL Incoming SMS attributes]** 놓습니다.

   ![](assets/sms_config_mo_5.png)

1. 여기에서는 전날의 모든 수신 메시지를 타깃팅하고 싶습니다. 범주에서 **[!UICONTROL Field]** 을 선택합니다 **[!UICONTROL Creation date (created)]**.
1. 에서 **[!UICONTROL Filter type]**&#x200B;을 **[!UICONTROL Relative]** 선택한 다음 에서 **[!UICONTROL Level of precision]**&#x200B;을 선택합니다 **[!UICONTROL Day]**.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘, 전날이나 지난 며칠 간의 데이터를 검색할 수 있습니다. 쿼리가 **[!UICONTROL Confirm]** 구성되면 을 클릭합니다.

이 쿼리는 선택한 시간 범위에 따라 수신된 모든 STOP 메시지를 검색합니다.

활동을 통해 예를 들어 모집단 생성 및 게재 개인화를 개선할 수 있습니다.
