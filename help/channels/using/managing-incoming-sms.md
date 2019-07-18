---
title: 들어오는 SMS 관리
seo-title: 들어오는 SMS 관리
description: 들어오는 SMS 관리
seo-description: Adobe Campaign에서 SMS 중지 및 수신 SMS 저장을 관리하는 방법에 대해 알아보십시오.
page-status-flag: 정품 인증 안 함
uuid: F 063052 B -96 EF -41 B 6-BF 1 B -4006 DE 73 F 0 B 9
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: sms-messages
discoiquuid: EE 1970 E 6-1 CED -46 E 0-94 E 0-94 E 6-83378300
delivercontext-tags: 전달, Smscontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Managing incoming SMS{#managing-incoming-sms}

## Managing STOP SMS {#managing-stop-sms}

캠페인을 통해 전송된 SMS 메시지에 대한 프로필이 답글을 달 때 자동으로 다시 자신에게 보내는 메시지와 수행 작업을 구성할 수 있습니다.

This configuration is defined in the **[!UICONTROL Automatic reply sent to the MO]** section of the [SMS Routing external account](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing). MO 는'모바일됨'을 의미하며 SMS를 보낸 모바일에 자동 답글을 구성할 수 있음을 의미합니다.

이렇게 하려면:

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration > Application settings > External accounts]** then the **[!UICONTROL SMS routing via SMPP]** external account.
1. **[!UICONTROL Automatic reply sent to the MO]** 카테고리 아래에서를 클릭하여 **[!UICONTROL Create element]** 자동 답글을 구성합니다.

   ![](assets/sms_mo_1.png)

1. 이 자동 답글을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어, 받는 사람이 "stop" 키워드를 전송하는 경우 자동 답글을 받게 됩니다.

   키워드와 관계없이 동일한 응답을 전송하려면 이 열을 비워 두십시오.

   ![](assets/sms_mo_2.png)

1. **[!UICONTROL Short code]** 이 필드에서 일반적으로 배달을 전송하는 데 사용되는 번호를 지정하고 발신자 이름으로 사용됩니다. You can also decide to leave the **[!UICONTROL Short code]** column empty, to send the same reply no matter what the short code.

   ![](assets/sms_mo_4.png)

1. Type in the answer you want to send to your recipients in the field **[!UICONTROL Reply]**.

   To carry out an action without sending a reply, leave the **[!UICONTROL Reply]** column empty. 예를 들어, "중지" 이외의 메시지로 응답한 사용자의 전화 번호를 격리할 수 있습니다.

   ![](assets/sms_mo_3.png)

1. **[!UICONTROL Additional action]** 필드에서 동작을 자동 답글에 연결합니다.

   * **[!UICONTROL Send to quarantine]** 이 작업은 프로필 전화 번호를 자동으로 격리합니다.
   * **[!UICONTROL Remove from quarantine]** 이 작업은 프로필 전화 번호를 격리에서 제거합니다.
   * The **[!UICONTROL None]** action allows you to only send the message to your recipients without carrying an action.
   For example, in the configuration below, if recipients send the keyword "STOP", they will automatically receive an unsubscription confirmation and their phone number will be sent to quarantine with the **[!UICONTROL Blacklisted]** status. 이 상태는 전화 번호에만 해당되며, 사용자가 이메일 메시지를 계속 수신할 수 있도록 프로필은 차단되지 않습니다.

   ![](assets/sms_mo.png)

이제 받는 사람은 자동으로 메시지를 구독 취소하고 이 자동 답글을 통해 격리 상태로 보낼 수 있습니다. The quarantined recipients are listed in the **[!UICONTROL Addresses]** table available through the **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Quarantines]** menu. For more information on quarantines, refer to this [section](../../sending/using/understanding-quarantine-management.md).

필요한 경우 이러한 SMS를 저장할 수 있습니다. For more information on this, refer to this [section](../../channels/using/managing-incoming-sms.md#storing-incoming-sms).

## Storing incoming SMS {#storing-incoming-sms}

**[!UICONTROL SMS routing via SMPP]** 외부 계정에서 받는 사람이 받는 사람 목록에서 제거되기 위해 SMS 메시지에 "중지" 할 때 예를 들어 들어오는 메시지를 저장하도록 선택할 수 있습니다.

![](assets/sms_config_mo_1.png)

By checking **[!UICONTROL Store incoming MO in the database]** in the **[!UICONTROL SMPP channel settings]** category, all SMS will be stored in the inSMS table and can be retrieved via a query activity in a workflow.

이렇게 하려면:

1. **[!UICONTROL SMPP channel settings]** 필드에서 **[!UICONTROL Store incoming MO in the database]**&#x200B;확인합니다.

   ![](assets/sms_config_mo_2.png)

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]****[!UICONTROL Workflow]**&#x200B;를 클릭하고 선택합니다.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. Edit the properties of your workflow, then click **[!UICONTROL Create]**. For more on workflows creation, refer to this [section](../../automating/using/building-a-workflow.md).
1. **[!UICONTROL Query]** 활동을 드래그하여 놓고 활동을 두 번 클릭합니다.
1. In the **[!UICONTROL Properties]** tab of the query, choose **[!UICONTROL Incoming SMS (inSMS)]** in the **[!UICONTROL Resource]** field.

   ![](assets/sms_config_mo_4.png)

1. Then, in the **[!UICONTROL Target]** tab, drag and drop the **[!UICONTROL Incoming SMS attributes]** rule.

   ![](assets/sms_config_mo_5.png)

1. Adobe는 전 날부터 모든 메시지를 타깃팅하고 있습니다. **[!UICONTROL Field]** 카테고리에서 **[!UICONTROL Creation date (created)]**&#x200B;를 선택합니다.
1. In **[!UICONTROL Filter type]**, select **[!UICONTROL Relative]** then in **[!UICONTROL Level of precision]**, choose **[!UICONTROL Day]**.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘 또는 지난 며칠 동안의 데이터를 검색할 수 있습니다. Click **[!UICONTROL Confirm]** when your query is configured.

이 쿼리는 선택한 시간 범위에 따라 수신된 모든 중지 메시지를 검색합니다.

예를 들어, 활동을 통해 모집단을 만들고 전달을 더 효과적으로 개인화할 수 있습니다.
