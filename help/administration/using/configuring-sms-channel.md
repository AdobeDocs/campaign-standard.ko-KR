---
title: SMS 채널 구성
description: '"SMS 구성 단계를 살펴보십시오.라우팅, 인코딩, 형식 및 고급 속성을 설정할 수 있습니다. "'
page-status-flag: never-activated
uuid: 5f13dbd5-9522-4199-8d9a-44c397cb2458
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 356d4d4f-3d5a-468c-bff8-96767cd8fff6
context-tags: extAccountMobile,overview;extAccount,main;delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e31e8c63fa94d190211c7a51e7f1091657c9f479

---


# SMS 채널 구성{#configuring-sms-channel}

SMS 메시지를 전송하려면 관리자가 **[!UICONTROL Administration]**>**[!UICONTROL Channels]** > **[!UICONTROL SMS]**>**[!UICONTROL SMS accounts]** 메뉴 아래에 하나 이상의 외부 계정을 구성해야 합니다.

외부 계정을 만들고 수정하는 단계는 외부 계정 [섹션에서](../../administration/using/external-accounts.md) 자세히 설명합니다. SMS 메시지 전송을 위한 외부 계정 관련 매개 변수는 아래와 같습니다.

## SMS 라우팅 정의 {#defining-an-sms-routing}

외부 계정은 기본적으로 **[!UICONTROL SMS routing via SMPP]**제공되지만 다른 계정을 추가하는 것이 유용할 수 있습니다.

SMPP 프로토콜을 사용하려면 새 외부 계정을 만들 수도 있습니다. SMS 프로토콜 및 설정에 대한 자세한 내용은 이 [기술 문서를](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html)참조하십시오.

1. 새 외부 계정을 만듭니다 **[!UICONTROL Administration > Application settings > External accounts]**.
1. 계정 유형을 **[!UICONTROL Routing]**로, 채널은**[!UICONTROL Mobile (SMS)]** 로, 배달 모드는 으로 **[!UICONTROL Bulk delivery]**정의합니다.

   ![](assets/sms_routing.png)

1. 연결 설정을 정의합니다.

   SMS 메시지 전송과 관련된 연결 설정을 입력하려면 SMS 서비스 제공업체에 연락하여 다른 외부 계정 필드를 완료하는 방법을 알려주십시오.

   ![](assets/sms_connection.png)

   이 **[!UICONTROL Enable TLS over SMPP]**옵션을 사용하면 SMPP 트래픽을 암호화할 수 있습니다.

   **[!UICONTROL Enable verbose SMPP traces in the log file]**모든 SMPP 트래픽을 로그 파일에 덤프할 수 있습니다. 커넥터 문제를 해결하고 공급자가 보는 트래픽과 비교하려면 이 옵션을 활성화해야 합니다.

1. 선택한 공급자에 따라 필드에 입력할 값을 제공하는 Adobe에 문의하십시오. **[!UICONTROL SMS-C implementation name]**
1. SMPP 채널 설정을 정의합니다. SMS 인코딩 및 [포맷](#sms-encoding-and-formats) 섹션에서 자세한 내용을 살펴볼 수 있습니다.

   들어오는 모든 SMS를 inSMS 테이블에 저장하려면 를 **[!UICONTROL Store incoming MO in the database]**활성화합니다. 수신 SMS를 검색하는 방법에 대한 자세한 내용은 이[섹션을](../../channels/using/managing-incoming-sms.md#storing-incoming-sms)참조하십시오.

   이 **[!UICONTROL Enable Real-time KPI updates during SR processing]**옵션을 사용하면**[!UICONTROL Delivered]** 또는 **[!UICONTROL Bounces + Errors]**KPI를 게재한 후 실시간으로 업데이트할 수 있습니다. 이러한 KPI는**[!UICONTROL Deployment]** 창에서 찾을 수 있으며 공급자로부터 받은 SR(상태 보고서)에서 직접 재계산됩니다.

   ![](assets/sms_connection_1.png)

1. 매개 변수를 **[!UICONTROL Throughput and timeouts]**정의합니다.

   초당 MT로 아웃바운드 메시지의 최대 처리량(&quot;MT&quot;, Mobile Terminated)을 지정할 수 있습니다. 해당 필드에 &quot;0&quot;을 입력하면 처리량은 무제한이 됩니다.

   기간에 해당하는 모든 필드의 값을 초 단위로 완료해야 합니다.

1. 특정 인코딩 매핑을 정의해야 하는 경우에 대비해 SMS-C 특정 매개 변수를 정의합니다. 자세한 내용은 SMSC 세부 [사항](#smsc-specifics) 섹션을 참조하십시오.

   SMPP 프로토콜을 준수하지 않을 경우 **[!UICONTROL Send full phone number (send characters other than digits)]**옵션을 활성화하고 SMS-C(SMS 공급자)의 서버에**[!UICONTROL +]** 접두사를 전송합니다.

   그러나 특정 제공업체에서 **[!UICONTROL +]**접두사를 사용해야 하는 경우 공급자에게 확인하면 필요한 경우 이 옵션을 활성화하라는 메시지가 나타납니다.

1. 필요한 경우 자동 답글을 정의하여 회신 내용에 따라 작업을 트리거합니다. For more on this, refer to [this section](../../channels/using/managing-incoming-sms.md#managing-stop-sms).
1. SMS 라우팅 외부 계정의 구성을 저장합니다.

이제 새 라우팅을 사용하여 Adobe Campaign과 함께 SMS 메시지를 보낼 수 있습니다.

## SMS 인코딩 및 포맷 {#sms-encoding-and-formats}

### SMS 인코딩, 길이 및 번역 {#sms-encoding--length-and-transliteration}

기본적으로 SMS의 문자 수는 GSM(Global System for Mobile Communications) 표준을 충족합니다.

GSM 인코딩을 사용하는 SMS 메시지는 SMS당 160자, SMS당 153자로 제한됩니다.

>[!NOTE]
>
>특정 문자는 두 개(중괄호, 대괄호, 유로 기호 등)로 계산됩니다. 사용 가능한 GSM 문자 목록은 문자 표 [- GSM 표준 섹션에](#table-of-characters---gsm-standard) 있습니다.

원하는 경우 해당 상자를 선택하여 문자 변환을 승인할 수 있습니다.

![](assets/sms_transliteration.png)

교역은 GSM 표준으로 간주되지 않을 때 SMS의 한 문자를 다른 문자로 바꾸는 것으로 이루어집니다.

* 음역 **인증이**&#x200B;되면 메시지가 전송될 때 고려되지 않은 각 문자가 GSM 문자로 대체됩니다. 예를 들어 &quot;레크&quot;는 &quot;e&quot;로 대체됩니다. 따라서 메시지는 약간 변경되지만 문자 제한은 그대로 유지됩니다.
* 음역 지정이 인증되지 **않은**&#x200B;경우, 고려되지 않은 문자가 포함된 각 메시지는 바이너리 형식(유니코드)으로 전송됩니다.따라서 모든 문자가 그대로 전송됩니다. 그러나 유니코드를 사용하는 SMS 메시지는 70자(여러 부분으로 전송된 메시지의 경우 SMS당 67자)로 제한됩니다. 최대 문자 수가 초과되면 몇 개의 메시지가 전송되어 추가 비용이 발생할 수 있습니다.

>[!IMPORTANT]
>
>SMS 메시지의 컨텐츠에 개인화 필드를 삽입하면 GSM 인코딩에 의해 고려되지 않는 문자가 삽입될 수 있습니다. 컨텐츠 예는 SMS 메시지 개인화 [섹션에서 제공됩니다](../../channels/using/personalizing-sms-messages.md) .

기본적으로 문자 음역은 비활성화됩니다. SMS 메시지의 모든 문자를 그대로 유지하려면 적절한 이름을 변경하지 않는 것이 좋습니다. 이 옵션을 활성화하지 않는 것이 좋습니다.

그러나 SMS 메시지에 유니코드 메시지를 생성하는 문자가 많이 포함된 경우 이 옵션을 활성화하여 메시지 전송 비용을 제한할 수 있습니다.

### 문자 표 - GSM Standard {#table-of-characters---gsm-standard}

이 섹션에서는 GSM 표준에서 고려하는 문자를 제공합니다. 아래에 언급된 문자 외에 메시지 본문에 삽입된 모든 문자는 전체 메시지를 바이너리 형식(유니코드)으로 변환하여 70자로 제한합니다. 자세한 내용은 SMS 인코딩, [길이 및 음역 섹션을 참조하십시오](#sms-encoding--length-and-transliteration) .

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
   <td> 승<br /> </td> 
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
   <td> 우<br /> </td> 
   <td> <img height="21px" src="assets/pi.png" /> <br /> </td> 
   <td> &amp;<br /> </td> 
   <td> 6<br /> </td> 
   <td> F<br /> </td> 
   <td> V<br /> </td> 
   <td> f<br /> </td> 
   <td> v<br /> </td> 
  </tr> 
  <tr> 
   <td> 2차<br /> </td> 
   <td> <img height="21px" src="assets/psi.png" /> <br /> </td> 
   <td> '<br /> </td> 
   <td> 7<br /> </td> 
   <td> G<br /> </td> 
   <td> W<br /> </td> 
   <td> g<br /> </td> 
   <td> w<br /> </td> 
  </tr> 
  <tr> 
   <td> 보<br /> </td> 
   <td> <img height="21px" src="assets/sigma.png" /> <br /> </td> 
   <td> (<br /> </td> 
   <td> 8<br /> </td> 
   <td> H<br /> </td> 
   <td> X<br /> </td> 
   <td> h<br /> </td> 
   <td> x<br /> </td> 
  </tr> 
  <tr> 
   <td> 비치<br /> </td> 
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
   <td> 쇠<br /> </td> 
   <td> ESC<br /> </td> 
   <td> +<br /> </td> 
   <td> ;<br /> </td> 
   <td> K<br /> </td> 
   <td> Ae<br /> </td> 
   <td> k<br /> </td> 
   <td> a<br /> </td> 
  </tr> 
  <tr> 
   <td> 쇠<br /> </td> 
   <td> AE<br /> </td> 
   <td> ,<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> L<br /> </td> 
   <td> 5시<br /> </td> 
   <td> l<br /> </td> 
   <td> 5<br /> </td> 
  </tr> 
  <tr> 
   <td> CR<br /> </td> 
   <td> æ<br /> </td> 
   <td> -<br /> </td> 
   <td> = </td> 
   <td> M<br /> </td> 
   <td> Clncage<br /> </td> 
   <td> m<br /> </td> 
   <td> 팽년생<br /> </td> 
  </tr> 
  <tr> 
   <td> 오<br /> </td> 
   <td> 섬<br /> </td> 
   <td> .<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> N<br /> </td> 
   <td> 여우<br /> </td> 
   <td> n<br /> </td> 
   <td> 여우<br /> </td> 
  </tr> 
  <tr> 
   <td> o<br /> </td> 
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

SP:공간

ESC:Escape

LF:라인 피드

CR:캐리지 리턴

**고급 문자(두 번 카운트됨)**

^ { } [ ~ ] | €

### SMSC 세부 사항 {#smsc-specifics}

>[!NOTE]
>
>이러한 옵션을 사용하면 커넥터를 비표준 SMPP 3.4 사양 또는 특정 인코딩 요구 사항에 맞게 조정할 수 있으며 고급 사용자만 구성할 수 있습니다.

SMS 메시지를 보낼 때 Adobe Campaign은 하나 또는 여러 개의 텍스트 인코딩을 사용할 수 있습니다. 각 인코딩에는 고유한 문자 집합이 있으며 SMS 메시지에 맞는 문자 수를 결정합니다.

이 **[!UICONTROL DATA_CODING]**필드를 사용하면 Adobe Campaign이 인코딩이 사용되는 SMS-C와 통신할 수 있습니다.

>[!NOTE]
>
>data_coding **** 값과 실제로 사용된 인코딩 간의 매핑이 표준화되어 있습니다. 그러나 특정 SMS-C에는 고유한 매핑이 있습니다.이 경우 Adobe Campaign **관리자가** 이 매핑을 선언해야 합니다. 자세한 내용은 제공업체에 문의하십시오.

이 **[!UICONTROL Define a specific mapping of encodings]**기능을 사용하면** data_code를&#x200B;**선언하고 필요한 경우 인코딩을 강제 적용할 수 있습니다.이렇게 하려면 표에 단일 인코딩을 지정합니다.

**구성**

* 이 **[!UICONTROL Define a specific mapping of encodings]**기능이 선택되지 않으면 커넥터는 일반 동작을 수행합니다.

   * GSM 인코딩을 사용하여 **data_coding = 0을**&#x200B;지정합니다.
   * GSM 인코딩이 실패할 경우 **UCS2** 인코딩을 사용하여 값을 **data_coding = 8**&#x200B;지정합니다.
   ![](assets/sms_data_coding.png)

* 이 **[!UICONTROL Define a specific mapping of encodings]**기능을 선택하면 사용할 인코딩과 연결된**[!UICONTROL data_coding]** 필드 값을 정의할 수 있습니다. Adobe Campaign은 목록에서 첫 번째 인코딩을 사용하려고 시도하지만 첫 번째 인코딩이 불가능할 경우 다음을 수행합니다.

   선언의 순서는 중요합니다.각 SMS 메시지에서 가능한 한 많은 문자를 입력할 수 있도록 인코딩을 **위해 목록을 오름차순으로** 입력하는 것이 좋습니다.

   사용할 인코딩만 선언합니다. SMS-C에서 제공하는 인코딩 중 일부가 사용자의 사용 목적에 부합되지 않을 경우 목록에 선언하지 마십시오.

   ![](assets/sms_data_coding1.png)

### MO로 자동 회신 전송 {#automatic-reply-sent-to-the-mo}

Adobe Campaign을 통해 전송된 SMS 메시지에 프로필로 회신할 때 수행할 작업은 물론 본인에게 자동으로 전송되는 메시지를 구성할 수 있습니다.

For more information, refer to [this section](../../channels/using/managing-incoming-sms.md).

## SMS 속성 구성 {#configuring-sms-properties}

이 섹션에서는 SMS 배달 또는 SMS 템플릿의 속성 화면에서 SMS에 고유한 매개 변수 목록을 자세히 설명합니다.

SMS 메시지 전송을 위한 특정 매개 변수는 **[!UICONTROL Send]**및**[!UICONTROL Advanced parameters]** 섹션에서 다시 그룹화됩니다.

![](assets/sms_options.png)

* 이 **[!UICONTROL From]**옵션을 사용하면 문자열을 사용하여 SMS 메시지 발신자의 이름을 개인화할 수 있습니다. 받는 사람의 휴대폰 전화에서 SMS 메시지의 발신자 이름으로 표시되는 이름입니다.

   이 필드가 비어 있으면, 이 필드는 사용될 외부 계정에 제공된 소스 번호가 됩니다. 소스 번호가 제공되지 않으면 사용할 짧은 코드가 됩니다. SMS 전달과 관련된 외부 계정은 SMS 라우팅 [정의](#defining-an-sms-routing) 섹션에 표시됩니다.

   ![](assets/sms_smpp.png)

   >[!IMPORTANT]
   >
   >발신자 주소 수정과 관련하여 귀하의 국가에서 해당 법률을 확인하십시오. 또한 SMS 서비스 제공업체에 문의하여 이 기능을 제공하는지 확인해야 합니다.

* 이 **[!UICONTROL Maximum number of SMS per message]**옵션을 사용하면 메시지를 보내는 데 사용할 SMS 메시지 수를 정의할 수 있습니다. 이 수를 초과하면 메시지가 전송되지 않습니다.

   >[!IMPORTANT]
   >
   >개인화 필드 또는 조건부 텍스트를 SMS 메시지 컨텐츠에 삽입한 경우 메시지의 길이에 따라 보낼 SMS 메시지 수가 받는 사람마다 다를 수 있습니다. 자세한 내용은 SMS 메시지 [개인화](../../channels/using/personalizing-sms-messages.md) 섹션을 참조하십시오.

* 이 **[!UICONTROL Transmission mode]**필드를 통해 SMS 메시지의 전달 방법을 결정할 수 있습니다.

   * **[!UICONTROL Saved on SIM card]**:메시지는 수신자의 전화 SIM 카드에 저장됩니다.
   * **[!UICONTROL Saved on mobile]**:메시지는 전화의 내부 메모리에 저장됩니다.
   * **[!UICONTROL Flash]**:메시지가 수신자의 모바일 전화에 알림으로 표시되면 메시지를 저장하지 않고 사라집니다.
