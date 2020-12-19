---
solution: Campaign Standard
product: campaign
title: 수신 SMS 관리
description: Adobe Campaign에서 STOP SMS를 관리하고 수신 SMS를 저장하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: sms-messages
delivercontext-tags: delivery,smsContent,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 7%

---


# 수신 SMS 관리{#managing-incoming-sms}

## STOP SMS {#managing-stop-sms} 관리

Campaign을 통해 보낸 SMS 메시지에 프로필이 답장할 경우 수행할 작업과 자동으로 다시 보낼 메시지를 구성할 수 있습니다.

이 구성은 [SMS 라우팅 외부 계정](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)의 **[!UICONTROL Automatic reply sent to the MO]** 섹션에 정의됩니다. MO는 &#39;모바일 출처&#39;를 의미하며, 이는 SMS를 보낸 모바일 사용자에 대한 자동 응답을 구성할 수 있음을 의미합니다.

방법은 다음과 같습니다.

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration > Application settings > External accounts]**&#x200B;을 선택한 다음 **[!UICONTROL SMS routing via SMPP]** 외부 계정을 선택합니다.
1. **[!UICONTROL Automatic reply sent to the MO]** 범주에서 **[!UICONTROL Create element]**&#x200B;을 클릭하여 자동 응답 구성을 시작합니다.

   ![](assets/sms_mo_1.png)

1. 이 자동 응답을 트리거할 키워드를 선택합니다. 키워드는 대/소문자를 구분하지 않습니다. 예를 들어 여기에서 수신자가 &quot;STOP&quot; 키워드를 보낼 경우 자동 답글을 받게 됩니다.

   키워드가 무엇인지에 관계없이 동일한 응답을 보내려면 이 열을 비워 두십시오.

   ![](assets/sms_mo_2.png)

1. **[!UICONTROL Short code]** 필드에서 일반적으로 납품을 보내는 데 사용하며 발신자 이름으로 사용할 번호를 지정합니다. 또한 **[!UICONTROL Short code]** 열을 비워 두면 짧은 코드에 상관없이 동일한 응답을 보낼 수 있습니다.

   ![](assets/sms_mo_4.png)

1. **[!UICONTROL Reply]** 필드에 수신자에게 보낼 답변을 입력합니다.

   응답을 보내지 않고 작업을 수행하려면 **[!UICONTROL Reply]** 열을 비워 두십시오. 예를 들어 &quot;STOP&quot; 이외의 메시지로 답글을 쓴 사용자의 전화 번호를 격리하지 않아도 됩니다.

   ![](assets/sms_mo_3.png)

1. **[!UICONTROL Additional action]** 필드에서 작업을 자동 회신에 연결합니다.

   * **[!UICONTROL Send to quarantine]** 동작은 프로필 전화 번호를 자동으로 격리합니다.
   * **[!UICONTROL Remove from quarantine]** 작업은 격리되지 않은 프로필 전화 번호를 제거합니다.
   * **[!UICONTROL None]** 액션을 사용하면 액션을 전달하지 않고도 수신자에게 메시지를 보낼 수 있습니다.

   예를 들어 아래 구성에서 수신자가 &quot;STOP&quot; 키워드를 전송하는 경우 구독 취소 확인 메시지를 자동으로 수신하게 되고 해당 전화 번호가 **[!UICONTROL On denylist]** 상태로 격리되도록 전송됩니다. 이 상태는 전화 번호만 참조하며, 프로필은 사용자가 이메일 메시지를 계속 수신하도록 합니다.

   ![](assets/sms_mo.png)

이제 수신자는 자동으로 메시지를 구독 취소할 수 있으며 이 자동 회신을 통해 격리 조치를 취할 수 있습니다. 격리된 받는 사람은 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** 메뉴를 통해 사용할 수 있는 **[!UICONTROL Addresses]** 테이블에 나열됩니다. 검역소에 대한 자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md)을 참조하십시오.

필요한 경우 이러한 수신 SMS를 저장할 수 있습니다. 이에 대한 자세한 내용은 이 [섹션](#storing-incoming-sms)을 참조하십시오.

## 들어오는 SMS {#storing-incoming-sms} 저장 중

**[!UICONTROL SMS routing via SMPP]** 외부 계정에서 수신자 목록에서 제거하기 위해 구독자가 SMS 메시지에 &quot;STOP&quot;을 회신할 때와 같이 수신 메시지를 저장하도록 선택할 수 있습니다.

![](assets/sms_config_mo_1.png)

**[!UICONTROL SMPP channel settings]** 범주에서 **[!UICONTROL Store incoming MO in the database]**&#x200B;을 선택하면 모든 SMS가 inSMS 테이블에 저장되고 워크플로의 쿼리 활동을 통해 검색할 수 있습니다.

방법은 다음과 같습니다.

1. **[!UICONTROL SMPP channel settings]** 필드에서 **[!UICONTROL Store incoming MO in the database]**&#x200B;을 선택합니다.

   ![](assets/sms_config_mo_2.png)

1. **[!UICONTROL Marketing activities]** 탭에서 **[!UICONTROL Create]**&#x200B;을 클릭한 다음 **[!UICONTROL Workflow]**&#x200B;를 선택합니다.

   ![](assets/sms_config_mo_3.png)

1. 워크플로우 유형을 선택합니다.
1. 워크플로우의 속성을 편집한 다음 **[!UICONTROL Create]**&#x200B;을 클릭합니다. 워크플로우 생성에 대한 자세한 내용은 이 [섹션](../../automating/using/building-a-workflow.md)을 참조하십시오.
1. **[!UICONTROL Query]** 활동을 드래그하여 놓고 활동을 두 번 클릭합니다.
1. 쿼리의 **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Resource]** 필드에서 **[!UICONTROL Incoming SMS (inSMS)]**&#x200B;을 선택합니다.

   ![](assets/sms_config_mo_4.png)

1. 그런 다음 **[!UICONTROL Target]** 탭에서 **[!UICONTROL Incoming SMS attributes]** 규칙을 드래그하여 놓습니다.

   ![](assets/sms_config_mo_5.png)

1. 여기에서는 전날의 모든 수신 메시지를 타깃팅하고자 합니다. **[!UICONTROL Field]** 범주에서 **[!UICONTROL Creation date (created)]**&#x200B;을 선택합니다.
1. **[!UICONTROL Filter type]**&#x200B;에서 **[!UICONTROL Relative]**&#x200B;을 선택하고 **[!UICONTROL Level of precision]**&#x200B;에서 **[!UICONTROL Day]**&#x200B;을 선택합니다.

   ![](assets/sms_config_mo_6.png)

1. 그런 다음 오늘, 전일 또는 최근 며칠 간의 데이터를 검색할 수 있습니다. 쿼리가 구성되면 **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

이 쿼리는 선택한 시간 범위에 따라 수신된 모든 STOP 메시지를 검색합니다.

활동을 통해 모집단 생성 및 게재 개인화 개선을 예로 들 수 있습니다.
