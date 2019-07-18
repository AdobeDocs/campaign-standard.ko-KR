---
title: SMS 채널 구성
seo-title: SMS 채널 구성
description: SMS 채널 구성
seo-description: '" SMS 구성 단계를 살펴보십시오. 라우팅, 인코딩, 형식 및 고급 속성. "'
page-status-flag: 정품 인증 안 함
uuid: 5 F 13 DBD 5-9522-4199-8 D 9 A -44 C 397 CB 2458
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 채널 구성
discoiquuid: 356 D 4 D 4 F -3 D 5 A -468 C-BFF 8-96767 CD 8 FFF 6
context-tags: Extaccountmobile, 개요; extaccount, main; 전달, Smscontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 866567d63dd2798eb56d42d4e163e5484c9b4d68

---


# Configuring SMS channel{#configuring-sms-channel}

To send SMS messages, one or several external accounts must be configured by an administrator under the **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL SMS]** &gt; **[!UICONTROL SMS accounts]** menu.

The steps for creating and modifying an external account are detailed in the [External accounts](../../administration/using/external-accounts.md) section. SMS 메시지 전송을 위해 외부 계정에 관련된 매개 변수 아래에서 찾을 수 있습니다.

## Defining an SMS Routing {#defining-an-sms-routing}

The external account **[!UICONTROL SMS routing via SMPP]** is provided by default, but it can be useful to add other accounts.

SMPP 프로토콜을 사용하려면 새 외부 계정을 만들 수도 있습니다. For more information on SMS protocol and settings, refer to this [technical note](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html).

1. Create a new external account from **[!UICONTROL Administration > Application settings > External accounts]**.
1. Define the account type as **[!UICONTROL Routing]**, the channel as **[!UICONTROL Mobile (SMS)]** and the delivery mode as **[!UICONTROL Bulk delivery]**.

   Once these routing parameters have been defined, the SMS connector ( **[!UICONTROL Generic SMPP]** ) is selected automatically. 이 커넥터를 사용하면 Adobe Campaign에서 SMPP 프로토콜을 통해 SMS-C (Short Message Service Center) 에 연결하여 SMS 메시지를 대상 프로파일에 직접 보낼 수 있습니다.

   ![](assets/sms_routing.png)

1. 연결 설정을 정의합니다.

   SMS 메시지 전송 관련 연결 설정을 입력하려면 다른 외부 계정 필드를 작성하는 방법을 설명하는 SMS 서비스 공급자에게 문의하십시오.

   ![](assets/sms_connection.png)

   **[!UICONTROL Enable TLS over SMPP]** 이 옵션을 사용하면 SMPP 트래픽을 암호화할 수 있습니다.

   **[!UICONTROL Enable verbose SMPP traces in the log file]** 로그 파일에서 모든 SMPP 트래픽을 덤프할 수 있습니다. 이 옵션을 사용하여 커넥터를 해결하고 공급자가 본 트래픽과 비교할 수 있습니다.

1. Contact Adobe who will give you the value to enter into the **[!UICONTROL SMS-C implementation name]** field, depending on the provider chosen.
1. SMPP 채널 설정을 정의합니다. You can learn more in the [SMS encoding and formats](../../administration/using/configuring-sms-channel.md#sms-encoding-and-formats) section.

   Enable the **[!UICONTROL Store incoming MO in the database]** if you want all incoming SMS to be stored in the inSMS table. For more information on how to retrieve your incoming SMS, refer to this [section](../../channels/using/managing-incoming-sms.md#storing-incoming-sms).

   **[!UICONTROL Enable Real-time KPI updates during SR processing]** 이 옵션을 사용하면 배달을 전송한 후 **[!UICONTROL Delivered]** 실시간으로 또는 **[!UICONTROL Bounces + Errors]** KPI를 업데이트할 수 있습니다. These KPIs can be found in the **[!UICONTROL Deployment]** window and are directly recalculated from the SR (Status Report) received from the provider.

   ![](assets/sms_connection_1.png)

1. **[!UICONTROL Throughput and timeouts]** 매개 변수를 정의합니다.

   아웃바운드 메시지 ("mt", 모바일 종료됨) 의 최대 처리량을 초당 MT로 지정할 수 있습니다. 해당 필드에 "0" 를 입력하면 처리량이 무제한입니다.

   기간에 해당하는 모든 필드의 값은 초 단위로 완료해야 합니다.

1. 특정 인코딩 매핑을 정의해야 하는 경우 SMS-C 특정 매개 변수를 정의할 수 있습니다. For more information, refer to the [SMSC specifics](../../administration/using/configuring-sms-channel.md#smsc-specifics) section.

   Enable the **[!UICONTROL Send full phone number (send characters other than digits)]** option if you don't want to respect the SMPP protocol and transfer the **[!UICONTROL +]** prefix to the server of the SMS provider (SMS-C).

   However, given that certain providers require the use of the **[!UICONTROL +]** prefix, it is advised that you check with your provider and they will suggest that you enable this option if necessary.

1. 필요한 경우 자동 답글을 정의하여 응답 내용을 기반으로 작업을 트리거합니다. For more on this, refer to [this section](../../channels/using/managing-incoming-sms.md#managing-stop-sms).
1. SMS 라우팅의 외부 계정 구성을 저장합니다.

이제 새 라우팅을 사용하여 Adobe Campaign로 SMS 메시지를 보낼 수 있습니다.

## SMS encoding and formats {#sms-encoding-and-formats}

### SMS encoding, length and transliteration {#sms-encoding--length-and-transliteration}

기본적으로 SMS의 문자 수는 GSM (Global System for Mobile Communications) 표준을 준수합니다.

GSM 인코딩을 사용하는 SMS 메시지는 여러 부분으로 전송되는 메시지의 경우 160 자 또는 SMS 당 153 자로 제한됩니다.

>[!NOTE]
>
>특정 문자가 2 개 (중괄호, 대괄호, 유로 기호 등) 로 계산됩니다. The list of available GSM characters is presented in the [Table of characters - GSM Standard](../../administration/using/configuring-sms-channel.md#table-of-characters---gsm-standard) section.

원하는 경우 해당 상자를 선택하여 문자 음영을 승인할 수 있습니다.

![](assets/sms_transliteration.png)

음영은 GSM 표준에서 해당 문자가 고려되지 않을 때 SMS의 한 문자를 다른 문자로 바꾸는 것으로 구성됩니다.

* If transliteration is **authorized**, each character that is not taken into account is replaced by a GSM character when the message is sent. 예를 들어 "ë" 라는 문자는 "e" 로 대체됩니다. 따라서 메시지가 약간 변경되지만 문자 제한이 동일하게 유지됩니다.
* When transliteration is **not authorized**, each message that contains characters that are not taken into account is sent in binary format (Unicode): all of the characters are therefore sent as they are. 유니코드를 사용하는 SMS 메시지는 70 자로 제한됩니다 (여러 부분으로 전송된 메시지의 경우 SMS 당 67 자). 최대 문자 수를 초과하면 몇 개의 메시지가 전송되어 추가 비용이 발생할 수 있습니다.

>[!CAUTION]
>
>개인화 필드를 SMS 메시지의 내용에 삽입하면 GSM 인코딩으로 고려되지 않는 문자가 소개될 수 있습니다. A content example is offered in the [Personalizing SMS messages](../../channels/using/personalizing-sms-messages.md) section.

기본적으로 문자 변환이 비활성화됩니다. SMS 메시지의 모든 문자를 그대로 유지하려면 적절한 이름을 변경하지 않도록 이 옵션을 활성화하지 않는 것이 좋습니다.

그러나 SMS 메시지에 유니코드 메시지를 생성하는 많은 문자가 포함된 경우 이 옵션을 활성화하여 메시지 전송 비용을 제한할 수 있습니다.

### Table of characters - GSM Standard {#table-of-characters---gsm-standard}

이 섹션에서는 GSM 표준에서 고려된 문자를 제공합니다. 아래에 언급된 문자 이외의 문자 본문에 삽입된 모든 문자가 이진 형식 (유니코드) 로 변환되므로 70 자로 제한됩니다. For more on this, refer to the [SMS encoding, length and transliteration](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) section.

**기본 문자**

<table> 
 <tbody> 
  <tr> 
   <td> @<br /> </td> 
   <td> <img height="21px" src="assets/delta.png" /> <br /> </td> 
   <td> SP<br /> </td> 
   <td> 0<br /> </td> 
   <td> ¡<br /> </td> 
   <td> P<br /> </td> 
   <td> ¿<br /> </td> 
   <td> P<br /> </td> 
  </tr> 
  <tr> 
   <td> £<br /> </td> 
   <td> _<br /> </td> 
   <td> !<br /> </td> 
   <td> 1<br /> </td> 
   <td> A<br /> </td> 
   <td> Q<br /> </td> 
   <td> a<br /> </td> 
   <td> q<br /> </td> 
  </tr> 
  <tr> 
   <td> $<br /> </td> 
   <td> <img height="21px" src="assets/phi.png" /> <br /> </td> 
   <td> "<br /> </td> 
   <td> 2<br /> </td> 
   <td> B<br /> </td> 
   <td> R<br /> </td> 
   <td> b<br /> </td> 
   <td> r<br /> </td> 
  </tr> 
  <tr> 
   <td> ¥<br /> </td> 
   <td> <img height="21px" src="assets/gamma.png" /> <br /> </td> 
   <td> #<br /> </td> 
   <td> 3<br /> </td> 
   <td> C<br /> </td> 
   <td> S<br /> </td> 
   <td> c<br /> </td> 
   <td> s<br /> </td> 
  </tr> 
  <tr> 
   <td> è<br /> </td> 
   <td> <img height="21px" src="assets/delta.png" /> <br /> </td> 
   <td> ¤<br /> </td> 
   <td> 4<br /> </td> 
   <td> D<br /> </td> 
   <td> T<br /> </td> 
   <td> d<br /> </td> 
   <td> t<br /> </td> 
  </tr> 
  <tr> 
   <td> é<br /> </td> 
   <td> <img height="21px" src="assets/omega.png" /> <br /> </td> 
   <td> %<br /> </td> 
   <td> 5<br /> </td> 
   <td> E<br /> </td> 
   <td> U<br /> </td> 
   <td> e<br /> </td> 
   <td> u<br /> </td> 
  </tr> 
  <tr> 
   <td> ù<br /> </td> 
   <td> <img height="21px" src="assets/pi.png" /> <br /> </td> 
   <td> &amp;<br /> </td> 
   <td> 6<br /> </td> 
   <td> F<br /> </td> 
   <td> V<br /> </td> 
   <td> f<br /> </td> 
   <td> v<br /> </td> 
  </tr> 
  <tr> 
   <td> ì<br /> </td> 
   <td> <img height="21px" src="assets/psi.png" /> <br /> </td> 
   <td> '<br /> </td> 
   <td> 7<br /> </td> 
   <td> G<br /> </td> 
   <td> W<br /> </td> 
   <td> g<br /> </td> 
   <td> w<br /> </td> 
  </tr> 
  <tr> 
   <td> ò<br /> </td> 
   <td> <img height="21px" src="assets/sigma.png" /> <br /> </td> 
   <td> (<br /> </td> 
   <td> 8<br /> </td> 
   <td> H<br /> </td> 
   <td> X<br /> </td> 
   <td> h<br /> </td> 
   <td> x<br /> </td> 
  </tr> 
  <tr> 
   <td> Ç<br /> </td> 
   <td> <img height="21px" src="assets/theta.png" /> <br /> </td> 
   <td> )<br /> </td> 
   <td> 9 </td> 
   <td> I<br /> </td> 
   <td> Y<br /> </td> 
   <td> i<br /> </td> 
   <td> y<br /> </td> 
  </tr> 
  <tr> 
   <td> LF<br /> </td> 
   <td> <img height="21px" src="assets/xi.png" /> <br /> </td> 
   <td> *<br /> </td> 
   <td> :<br /> </td> 
   <td> J<br /> </td> 
   <td> Z<br /> </td> 
   <td> j<br /> </td> 
   <td> z<br /> </td> 
  </tr> 
  <tr> 
   <td> Ø<br /> </td> 
   <td> ESC<br /> </td> 
   <td> +<br /> </td> 
   <td> ;<br /> </td> 
   <td> K<br /> </td> 
   <td> Ä<br /> </td> 
   <td> k<br /> </td> 
   <td> ä<br /> </td> 
  </tr> 
  <tr> 
   <td> ø<br /> </td> 
   <td> Æ<br /> </td> 
   <td> ,<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> L<br /> </td> 
   <td> Ö<br /> </td> 
   <td> l<br /> </td> 
   <td> ö<br /> </td> 
  </tr> 
  <tr> 
   <td> CR<br /> </td> 
   <td> æ<br /> </td> 
   <td> -<br /> </td> 
   <td> = </td> 
   <td> M<br /> </td> 
   <td> Ñ<br /> </td> 
   <td> m<br /> </td> 
   <td> ñ<br /> </td> 
  </tr> 
  <tr> 
   <td> Å<br /> </td> 
   <td> ß<br /> </td> 
   <td> .<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> N<br /> </td> 
   <td> Ü<br /> </td> 
   <td> n<br /> </td> 
   <td> ü<br /> </td> 
  </tr> 
  <tr> 
   <td> å<br /> </td> 
   <td> É<br /> </td> 
   <td> /<br /> </td> 
   <td> ?<br /> </td> 
   <td> O<br /> </td> 
   <td> §<br /> </td> 
   <td> o<br /> </td> 
   <td> à<br /> </td> 
  </tr> 
 </tbody> 
</table>

SP: space

ESC: escape

lf: 라인 피드

CR: 캐리지 리턴

**고급 문자 (두 번 계산)**

^ { } [ ~ ] | €

### SMSC specifics {#smsc-specifics}

>[!NOTE]
>
>이러한 옵션을 사용하여 비표준 SMSC (즉, SMPP 3.4 사양과 정확히 일치하지 않는 경우) 또는 특정 인코딩 요구 사항과 함께 작동하도록 커넥터를 조정할 수 있으며 고급 사용자만 구성해야 합니다.

Adobe Campaign에서 SMS 메시지를 보낼 때 하나 또는 여러 개의 텍스트 인코딩을 사용할 수 있습니다. 각 인코딩에는 고유한 문자 집합이 있으며 SMS 메시지에 맞는 문자 수를 결정합니다.

**[!UICONTROL DATA_CODING]** 이 필드를 사용하면 Adobe Campaign에서 인코딩이 사용되는 SMS-C와 통신할 수 있습니다.

>[!NOTE]
>
>**data_ coding** 값과 실제로 사용된 인코딩의 매핑이 표준화되어 있습니다. Nevertheless, certain SMS-C have their own specific mapping: in this case, your **Adobe Campaign** administrator needs to declare this mapping. 자세한 내용은 해당 제공업체에 문의하십시오.

**[!UICONTROL Define a specific mapping of encodings]** 이 기능을 사용하면 **data_ codings** 를 선언하고 필요한 경우 인코딩을 강제 적용할 수 있습니다. 이렇게 하려면 테이블에서 단일 인코딩을 지정합니다.

**구성**

* **[!UICONTROL Define a specific mapping of encodings]** 이 기능을 선택하지 않으면 커넥터는 일반적인 비헤이비어를 수행합니다.

   * It will try to use GSM encoding to which it assigns the value **data_coding = 0**.
   * If GSM encoding fails, it will use **UCS2** encoding to which it assigns the value **data_coding = 8**.
   ![](assets/sms_data_coding.png)

* **[!UICONTROL Define a specific mapping of encodings]** 이 기능을 선택하면 연결된 **[!UICONTROL data_coding]** 필드 값과 함께 사용할 인코딩을 정의할 수 있습니다. 첫 번째 인코딩이 불가능한 경우 Adobe Campaign 에서는 목록의 첫 번째 인코딩을 사용하려고 합니다. 그런 다음 다음을 수행합니다.

   The order of declaration is important: it is recommended that you put the list in ascending order **of cost** in order to favor the encodings allowing you to fit as many characters as possible in each SMS message.

   사용하려는 인코딩을 선언하기만 하면 됩니다. SMS-C가 제공한 인코딩이 사용 목적과 일치하지 않는 경우 목록에 선언하지 마십시오.

   ![](assets/sms_data_coding1.png)

### Automatic reply sent to the MO {#automatic-reply-sent-to-the-mo}

캠페인을 통해 전송된 SMS 메시지에 대한 프로필이 답글을 달 때 자동으로 다시 자신에게 보내는 메시지와 수행 작업을 구성할 수 있습니다.

For more information, refer to [this section](../../channels/using/managing-incoming-sms.md).

## Configuring SMS properties {#configuring-sms-properties}

이 섹션에서는 SMS 게재 또는 SMS 템플릿의 속성 화면에서 SMS에 고유한 매개 변수 목록을 자세히 설명합니다.

The specific parameters for sending SMS messages are regrouped in the **[!UICONTROL Send]** and in the **[!UICONTROL Advanced parameters]** sections.

![](assets/sms_options.png)

* **[!UICONTROL From]** 이 옵션을 사용하면 문자열을 사용하여 SMS 메시지 보낸 사람의 이름을 개인화할 수 있습니다. 수신자의 모바일 전화에 SMS 메시지의 발신자 이름으로 표시되는 이름입니다.

   이 필드가 비어 있으면 사용할 외부 계정에 제공된 소스 번호가 됩니다. 소스 번호가 제공되지 않으면 사용되는 짧은 코드가 사용됩니다. The external account specific to SMS delivery is presented in the [External SMS account](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing) section.

   ![](assets/sms_smpp.png)

   >[!CAUTION]
   >
   >발신자 주소 수정과 관련하여 국가의 법률을 확인하십시오. 또한 SMS 서비스 제공업체에 연락하여 이 기능을 제공하는지 확인해야 합니다.

* **[!UICONTROL Maximum number of SMS per message]** 이 옵션을 사용하면 메시지를 보내는 데 사용할 SMS 메시지의 수를 정의할 수 있습니다. 이 수가 초과하면 메시지가 전송되지 않습니다.

   >[!CAUTION]
   >
   >개인화 필드 또는 조건부 텍스트를 SMS 메시지의 컨텐츠에 삽입한 경우 메시지 길이 및 보낼 SMS 메시지의 수가 받는 사람마다 다를 수 있습니다. For more on this, refer to the [Personalizing SMS messages](../../channels/using/personalizing-sms-messages.md) section.

* **[!UICONTROL Transmission mode]** 이 필드에서 SMS 메시지의 배달 방법을 결정할 수 있습니다.

   * **[!UICONTROL Saved on SIM card]**: 메시지는 수신자의 전화 SIM 카드에 저장됩니다.
   * **[!UICONTROL Saved on mobile]**: 메시지는 전화기의 내부 메모리에 저장됩니다.
   * **[!UICONTROL Flash]**: 메시지가 수신자의 모바일 전화에 알림으로 표시되면 저장되지 않고 사라집니다.

