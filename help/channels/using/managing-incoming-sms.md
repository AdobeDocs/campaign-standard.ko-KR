---
title: 수신 SMS 관리
description: Adobe Campaign에서 STOP SMS를 관리하고 수신 SMS를 저장하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: sms-messages
delivercontext-tags: delivery,smsContent,back
feature: SMS
role: User
level: Intermediate
exl-id: 86cb6f4c-a5a7-4d9d-bbfd-4a70af38cf3a
source-git-commit: 8be43668d1a4610c3388ad27e493a689925dc88c
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 2%

---

# 수신 SMS 관리{#managing-incoming-sms}

## STOP SMS 관리 {#managing-stop-sms}

Campaign을 통해 보낸 SMS 메시지에 프로필이 답장할 경우 수행할 작업과 자동으로 다시 보낼 메시지를 구성할 수 있습니다.

이 구성은 **[!UICONTROL Automatic reply sent to the MO]** 섹션 [SMS 라우팅 외부 계정](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing). MO는 &#39;모바일 Originated&#39;를 의미하며, 즉 SMS를 보낸 모바일에 자동 답장을 구성할 수 있습니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 을(를) 선택합니다 **[!UICONTROL Administration > Application settings > External accounts]** 그러면 **[!UICONTROL SMS routing via SMPP]** 외부 계정.
1. 아래에 **[!UICONTROL Automatic reply sent to the MO]** 카테고리 **[!UICONTROL Create element]** 자동 회신 구성을 시작하려면 다음을 수행하십시오.

   ![](assets/sms_mo_1.png)

1. 이 자동 답장을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어 여기에서 수신자가 키워드 &quot;STOP&quot;을 보낼 경우 자동 답장이 수신됩니다.

   키워드가 무엇이든 동일한 답글을 보내려면 이 열을 비워 둡니다.

   ![](assets/sms_mo_2.png)

1. 에서 **[!UICONTROL Short code]** 필드에서 게재를 전송하는 데 일반적으로 사용되는 번호를 지정하고 발신자 이름으로 사용됩니다. 또한 **[!UICONTROL Short code]** 열이 비어 있으면, 짧은 코드가 어떻든 동일한 답글을 보낼 수 있습니다.

   ![](assets/sms_mo_4.png)

1. 필드에서 수신자에게 보낼 답변을 입력합니다 **[!UICONTROL Reply]**.

   응답을 보내지 않고 작업을 수행하려면 다음을 그대로 둡니다 **[!UICONTROL Reply]** 열이 비어 있습니다. 예를 들어 &quot;STOP&quot; 이외의 메시지로 답장하는 사용자의 전화 번호를 격리하지 않을 수 있습니다.

   ![](assets/sms_mo_3.png)

1. 에서 **[!UICONTROL Additional action]** 필드에서 작업을 자동 응답에 연결합니다.

   * 다음 **[!UICONTROL Send to quarantine]** 자동으로 프로필 전화 번호를 격리합니다.
   * 다음 **[!UICONTROL Remove from quarantine]** 격리 작업에서 프로필 전화 번호가 제거됩니다.
   * 다음 **[!UICONTROL None]** 작업을 사용하면 작업을 수행하지 않고 수신자에게 메시지만 보낼 수 있습니다.

   예를 들어 아래 구성에서 수신자가 &quot;STOP&quot; 키워드를 전송하는 경우 자동으로 구독 취소 확인을 받게 되고 해당 전화 번호는 와 함께 격리로 전송됩니다 **[!UICONTROL On denylist]** 상태. 이 상태는 전화번호에만 해당되며, 프로필은 사용자가 이메일 메시지를 계속 수신하도록 합니다.

   ![](assets/sms_mo.png)

1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

1. 에서 **[!UICONTROL Advanced parameters]** SMS 게재 **[!UICONTROL Properties]**&#x200B;를 설정하는 경우 **[!UICONTROL Short code]** 옵트아웃한 수신자를 자동으로 제외합니다. 자세한 내용은 [이 섹션](../../administration/using/configuring-sms-channel.md#configuring-sms-properties).

이제 수신자는 자동으로 메시지 구독을 취소하고 이 자동 답글을 통해 격리에 보낼 수 있습니다. 격리된 수신자는 **[!UICONTROL Addresses]** 테이블 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** 메뉴 아래의 제품에서 사용할 수 있습니다. 격리에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../../sending/using/understanding-quarantine-management.md).

필요한 경우 이러한 수신 SMS를 저장할 수 있습니다. 자세한 내용은 다음을 참조하십시오 [섹션](#storing-incoming-sms).

## 수신 SMS 저장 {#storing-incoming-sms}

에서 **[!UICONTROL SMS routing via SMPP]** 외부 계정에서는 받는 사람 목록에서 제거하기 위해 구독자가 SMS 메시지에 &quot;STOP&quot;을 회신하는 경우와 같이 수신 메시지를 저장하도록 선택할 수 있습니다.

![](assets/sms_config_mo_1.png)

확인 **[!UICONTROL Store incoming MO in the database]** 에서 **[!UICONTROL SMPP channel settings]** 카테고리에서는 모든 SMS가 inSMS 표에 저장되고 워크플로우의 쿼리 활동을 통해 검색할 수 있습니다.

방법은 다음과 같습니다.

1. 에서 **[!UICONTROL SMPP channel settings]** 필드, 확인 **[!UICONTROL Store incoming MO in the database]**.

   ![](assets/sms_config_mo_2.png)

1. 에서 **[!UICONTROL Marketing activities]** 탭, **[!UICONTROL Create]** 을(를) 선택합니다. **[!UICONTROL Workflow]**.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. 워크플로우의 속성을 편집한 다음 **[!UICONTROL Create]**. 워크플로우 만들기에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../../automating/using/building-a-workflow.md).
1. 끌어서 놓기 **[!UICONTROL Query]** 활동을 만들고 활동을 두 번 클릭합니다.
1. 에서 **[!UICONTROL Properties]** 쿼리의 탭에서 **[!UICONTROL Incoming SMS (inSMS)]** 에서 **[!UICONTROL Resource]** 필드.

   ![](assets/sms_config_mo_4.png)

1. 그런 다음 **[!UICONTROL Target]** 탭에서 을(를) 끌어서 놓습니다. **[!UICONTROL Incoming SMS attributes]** 규칙.

   ![](assets/sms_config_mo_5.png)

1. 여기에서는 전날의 모든 수신 메시지를 타겟팅하려고 합니다. 에서 **[!UICONTROL Field]** 카테고리, 선택 **[!UICONTROL Creation date (created)]**.
1. in **[!UICONTROL Filter type]**, 선택 **[!UICONTROL Relative]** 다음에 **[!UICONTROL Level of precision]**, 선택 **[!UICONTROL Day]**.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘, 전일 또는 최근 며칠 간의 데이터를 검색하도록 선택할 수 있습니다. 클릭 **[!UICONTROL Confirm]** 쿼리가 구성된 경우

이 쿼리는 선택한 시간 범위에 따라 받은 모든 STOP 메시지를 검색합니다.

활동을 통해 모집단을 만들고 게재를 보다 잘 개인화할 수 있습니다.
