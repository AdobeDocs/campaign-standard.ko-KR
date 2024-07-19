---
title: 수신 SMS 관리
description: Adobe Campaign에서 중지 SMS를 관리하고 수신 SMS를 저장하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: sms-messages
delivercontext-tags: delivery,smsContent,back
feature: SMS
role: User
level: Intermediate
exl-id: 86cb6f4c-a5a7-4d9d-bbfd-4a70af38cf3a
source-git-commit: 30d0c2552bea3a7cbd8500be4e8c0c74e5a40a99
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 2%

---

# 수신 SMS 관리{#managing-incoming-sms}

## STOP SMS 관리 {#managing-stop-sms}

Campaign을 통해 보낸 SMS 메시지에 프로필이 답장할 경우 수행할 작업과 자동으로 다시 보낼 메시지를 구성할 수 있습니다.

이 구성은 [SMS 라우팅 외부 계정](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)의 **[!UICONTROL Automatic reply sent to the MO]** 섹션에 정의되어 있습니다. MO는 &#39;Mobile Originated&#39;의 약자로, SMS를 보낸 모바일에 자동 회신을 구성할 수 있음을 의미합니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration > Application settings > External accounts]**&#x200B;을(를) 선택한 다음 **[!UICONTROL SMS routing via SMPP]** 외부 계정을 선택합니다.
1. **[!UICONTROL Automatic reply sent to the MO]** 범주 아래에서 **[!UICONTROL Create element]**&#x200B;을(를) 클릭하여 자동 회신 구성을 시작합니다.

   ![](assets/sms_mo_1.png)

1. 이 자동 회신을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어 수신자가 &quot;STOP&quot; 키워드를 전송하면 자동 회신을 받게 됩니다.

   키워드가 무엇이든 동일한 회신을 보내려면 이 열을 비워 둡니다.

   >[!IMPORTANT]
   >
   >영숫자만 허용됩니다.

   ![](assets/sms_mo_2.png)

1. **[!UICONTROL Short code]** 필드에서 게재를 보내는 데 일반적으로 사용되는 발신자 이름으로 사용할 숫자를 지정합니다. 짧은 코드에 관계없이 동일한 회신을 보내도록 **[!UICONTROL Short code]** 열을 비워 둘 수도 있습니다.

   ![](assets/sms_mo_4.png)

1. 받는 사람에게 보낼 대답을 필드 **[!UICONTROL Reply]**&#x200B;에 입력하십시오.

   회신을 보내지 않고 작업을 수행하려면 **[!UICONTROL Reply]** 열을 비워 둡니다. 예를 들어 &quot;STOP&quot; 이외의 다른 메시지로 답장하는 사용자의 전화 번호를 격리에서 제거할 수 있습니다.

   ![](assets/sms_mo_3.png)

1. **[!UICONTROL Additional action]** 필드에서 작업을 자동 회신에 연결합니다.

   * **[!UICONTROL Send to quarantine]** 작업은 프로필 전화 번호를 자동으로 격리합니다.
   * **[!UICONTROL Remove from quarantine]** 작업을 수행하면 프로필 전화 번호가 격리되지 않습니다.
   * **[!UICONTROL None]** 동작을 사용하면 동작을 수행하지 않고 받는 사람에게만 메시지를 보낼 수 있습니다.

   예를 들어 아래 구성에서 수신자가 &quot;STOP&quot; 키워드를 전송하면 구독 취소 확인이 자동으로 수신되며 해당 전화번호는 **[!UICONTROL On denylist]** 상태로 격리에 전송됩니다. 이 상태는 전화번호에만 해당되며, 프로필은 사용자가 이메일 메시지를 계속 받도록 되어 있습니다.

   ![](assets/sms_mo.png)

1. **[!UICONTROL Save]**&#x200B;를 클릭합니다.

1. SMS 게재 **[!UICONTROL Properties]**&#x200B;의 **[!UICONTROL Advanced parameters]**&#x200B;에서 특정 **[!UICONTROL Short code]**&#x200B;을(를) 설정하여 옵트아웃한 수신자를 자동으로 제외할 수 있습니다. 자세한 내용은 [이 섹션](../../administration/using/configuring-sms-channel.md#configuring-sms-properties)을 참조하세요.

이제 수신자가 메시지 구독을 자동으로 취소하고 이 자동 회신으로 격리될 수 있습니다. 격리된 받는 사람은 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** 메뉴를 통해 사용할 수 있는 **[!UICONTROL Addresses]** 테이블에 나열됩니다. 격리에 대한 자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md)을 참조하세요.

필요한 경우 이러한 수신 SMS를 저장할 수 있습니다. 자세한 내용은 이 [섹션](#storing-incoming-sms)을 참조하세요.

## 수신 SMS 저장 {#storing-incoming-sms}

**[!UICONTROL SMS routing via SMPP]** 외부 계정에서 받는 사람 목록에서 제거할 수 있도록 구독자가 SMS 메시지에 &quot;STOP&quot;이라고 답장하는 등의 경우 받는 메시지를 저장하도록 선택할 수 있습니다.

![](assets/sms_config_mo_1.png)

**[!UICONTROL SMPP channel settings]** 범주에서 **[!UICONTROL Store incoming MO in the database]**&#x200B;을(를) 선택하면 모든 SMS가 inSMS 테이블에 저장되고 워크플로우의 쿼리 활동을 통해 검색할 수 있습니다.

방법은 다음과 같습니다.

1. **[!UICONTROL SMPP channel settings]** 필드에서 **[!UICONTROL Store incoming MO in the database]**&#x200B;을(를) 확인합니다.

   ![](assets/sms_config_mo_2.png)

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Workflow]**&#x200B;을(를) 선택합니다.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. 워크플로우의 속성을 편집한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다. 워크플로우 만들기에 대한 자세한 정보는 이 [섹션](../../automating/using/building-a-workflow.md)을 참조하세요.
1. **[!UICONTROL Query]** 활동을 끌어다 놓고 활동을 두 번 클릭합니다.
1. 쿼리의 **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Resource]** 필드의 **[!UICONTROL Incoming SMS (inSMS)]**&#x200B;을(를) 선택합니다.

   ![](assets/sms_config_mo_4.png)

1. 그런 다음 **[!UICONTROL Target]** 탭에서 **[!UICONTROL Incoming SMS attributes]** 규칙을 끌어서 놓습니다.

   ![](assets/sms_config_mo_5.png)

1. 여기에서는 전날부터 들어오는 모든 메시지를 타겟팅하려고 합니다. **[!UICONTROL Field]** 범주에서 **[!UICONTROL Creation date (created)]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Filter type]**&#x200B;에서 **[!UICONTROL Relative]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Level of precision]**&#x200B;에서 **[!UICONTROL Day]**&#x200B;을(를) 선택하십시오.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘, 전날 또는 지난 며칠 중에 데이터를 검색하도록 선택할 수 있습니다. 쿼리가 구성되면 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

이 쿼리는 선택한 시간 범위에 따라 수신된 모든 STOP 메시지를 검색합니다.

예를 들어 활동을 통해 모집단을 만들고 게재를 더 잘 개인화할 수 있습니다.
