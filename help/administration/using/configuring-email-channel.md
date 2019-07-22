---
title: 이메일 채널 구성
seo-title: 이메일 채널 구성
description: 이메일 채널 구성
seo-description: 이메일 채널을 구성하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 9 FDDB 655-B 445-41 F 3-9 B 02-5 D 356 FC 88 AA 1
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 채널 구성
discoiquuid: 3752 d 41 f -8 c 59-4 fad-b 30 f-e 98 e 09 cd 74 a 8
context-tags: Extaccountemail, 개요; emailconfig, main; 규칙 세트, 개요; 전달, 속성, 열기
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 4d95fe00c1958399ff4d22d5f0e7762f895b4032

---


# Configuring email channel{#configuring-email-channel}

## Email channel parameters {#email-channel-parameters}

[이메일 구성] 화면에서는 이메일 채널에 대한 매개 변수를 정의할 수 있습니다.

![](assets/channels_1.png)

* **보낸 이메일의 머리글 매개 변수**

   In this section, you can specify the **[!UICONTROL masks]** authorized for the sender address and the error address. 필요한 경우 이러한 마스크를 쉼표로 분리할 수 있습니다. 이 구성은 선택 사항입니다. 이러한 필드를 입력할 때 메시지 준비 단계에서 Adobe Campaign는 입력한 주소가 올바른지 확인합니다. 이 작동 모드에서는 배달 가능성 문제를 유발할 수 있는 주소가 사용되지 않도록 합니다. 배달 주소는 배달 서버에 구성해야 합니다.

* **전달 능력**

   이 ID는 지원을 통해 제공됩니다. 배달 가능성 보고서가 올바르게 작동하려면 필요합니다.

* **배달 매개 변수**

   Adobe Campaign는 시작 날짜에 메시지를 보냅니다. **[!UICONTROL Message delivery duration]** 필드에서 메시지를 보낼 수 있는 기간을 지정할 수 있습니다.

   **[!UICONTROL Online resources validity duration]** 필드는 주로 미러 페이지 및 이미지에 대해 업로드된 리소스에 사용됩니다. 이 페이지의 리소스는 디스크 공간을 절약하기 위해 제한된 기간 동안 유효합니다.

* **재시도 횟수**

   일시적으로 배달되지 않은 메시지는 자동으로 재시도할 수 있습니다. This section indicates how many retries should be performed the day after the send is started (**Number of retries**) and the minimum delay between retries (**Retry period**).

   기본적으로 최소 한 시간의 간격이 있는 첫 번째 날에 대한 5 회 재시도 횟수는 하루 중 24 시간에 걸쳐 분산됩니다. One retry per day is programmed after that and until the delivery deadline, which is defined in the **[!UICONTROL Delivery parameters]** section.

* **이메일 격리 매개 변수**

   In the **[!UICONTROL Time between two significant errors]** field, enter a value to define the time the application waits before incrementing the error counter in case of failure. Defaut value: **"1d"**, for 1 day.

   **[!UICONTROL Maximum number of errors before quarantine]** 값에 도달하면 이메일 주소가 격리됩니다. Default value: **"5"**: the address will be quarantined on the sixth error. 이것은 연락처가 후속 배달에서 자동으로 제외됨을 의미합니다.

**관련 항목**:

[격리 관리 이해](../../sending/using/understanding-quarantine-management.md)

## Email routing accounts {#email-routing-accounts}

**[!UICONTROL Integrated email routing]** 외부 계정은 기본적으로 제공됩니다. 애플리케이션에 이메일을 전송할 수 있는 기술 매개 변수가 들어 있습니다.

![](assets/channels_2.png)

The account type must always be set to **[!UICONTROL Routing]**, the channel to **[!UICONTROL Email]** and the delivery mode set to **[!UICONTROL Bulk delivery]**.

**관련 항목**:

[외부 계정](../../administration/using/external-accounts.md)

## Email processing rules {#email-processing-rules}

These rules contain the list of character strings which can be returned by remote servers and which let you qualify the error (**Hard**, **Soft** or **Ignored**).

기본 규칙은 다음과 같습니다.

**바운스 메일**

이메일이 실패할 경우, 원격 메시지 서버는 응용 프로그램 설정에서 지정한 주소로 바운스 오류 메시지를 반환합니다. Adobe Campaign는 각 바운스 이메일의 컨텐츠를 규칙 목록의 문자열로 비교한 다음 세 가지 오류 유형 중 하나를 할당합니다.

사용자는 자신의 규칙을 만들 수 있습니다.

>[!CAUTION]
>
>When importing a package and when updating data via the **Update for deliverability** workflow, the user-created rules are overwritten.

**이메일 도메인 관리**

도메인 관리 규칙은 특정 도메인에 대한 발신 이메일의 흐름을 제어하는 데 사용됩니다. 바운스 메시지를 샘플링하고 해당되는 경우 전송을 차단합니다. Adobe Campaign 메시징 서버는 도메인과 관련된 규칙을 적용한 다음 규칙 목록에서 별표로 표시된 일반 사례에 대한 규칙을 적용합니다. Hotmail 및 MSN 도메인의 규칙은 기본적으로 Adobe Campaign에서 사용할 수 있습니다.

도메인 관리 규칙을 구성하려면 임계값을 설정하고 특정 SMTP 매개 변수를 선택하십시오. **임계값은** 특정 도메인에 대한 모든 메시지가 차단되는 오류 비율로 계산된 제한 값입니다.

예를 들어 일반적으로 300 개의 메시지의 경우, 오류 비율이 90%에 도달한 경우 3 시간 동안 이메일 전송이 차단됩니다.

**SMTP 매개 변수는** 차단 규칙에 적용되는 필터 역할을 합니다.

* **발신자 ID**, **도메인 키**, **DKIM**&#x200B;및 **s/MIME와 같이 도메인 이름을 확인하기 위해 특정 식별 표준 및 암호화 키를 활성화할지 여부를 선택할**&#x200B;수 있습니다.
* **SMTP 릴레이**: 특정 도메인에 대한 릴레이 서버의 IP 주소와 포트를 구성할 수 있습니다.

**MX 관리**

각 규칙은 MX에 대한 주소 마스크를 정의합니다. 이름이 이 마스크와 일치하는 모든 MX는 적용 가능합니다. 마스크는 " *" 및 " 일반 문자.

예를 들어 다음 주소는 다음과 같습니다.

* a.mx.ya hoo.com
* b.mx.ya hoo.com
* c.mx.ya hoo.com

는 다음 마스크와 호환됩니다.

* *.yahoo.com
* ? .mx.yahoo.com

이러한 규칙은 차례로 적용됩니다. MX 마스크가 타깃팅된 MX와 호환되는 첫 번째 규칙이 적용됩니다.

각 규칙에 대해 다음 매개 변수를 사용할 수 있습니다.

* **[!UICONTROL Range of IDs]**: 이 옵션을 사용하면 규칙이 적용되는 식별자 (Publicid) 범위를 표시할 수 있습니다. 다음을 지정할 수 있습니다.

   * 숫자: 규칙은 이 Publicid 에만 적용됩니다.
   * 숫자 범위 (number 1-number 2): 규칙은 이 두 숫자 사이의 모든 이메일에 적용됩니다.
   필드가 비어 있으면 규칙은 모든 ID에 적용됩니다.

* **[!UICONTROL Shared]**: 이 옵션은 시간당 최대 메시지 수가 이 규칙에 연결된 모든 Mxs에 적용됨을 나타냅니다.
* **[!UICONTROL Maximum number of connections]**: 지정된 주소에서 MX에 대한 최대 동시 연결 수입니다.
* **최대 메시지 수**: 한 연결에서 전송할 수 있는 최대 메시지 수입니다. 이 금액 이후에는 연결이 닫히고 새 연결이 다시 열립니다.
* **[!UICONTROL Messages per hour]**: 지정된 주소를 통해 MX에 대해 한 시간 동안 전송할 수 있는 최대 메시지 수입니다.

>[!CAUTION]
>
>* 매개 변수가 변경되면 배달 서버 (MTA) 를 다시 시작해야 합니다.
>* 관리 규칙의 수정 또는 작성은 전문가 사용자만 수행할 수 있습니다.
>



## List of email properties {#list-of-email-properties}

This section details the list of parameters available in the properties screen of an email or [email template](../../start/using/about-templates.md).

>[!NOTE]
>
>일부 매개 변수는 템플릿에서만 사용할 수 있습니다. Parameters you can access [depend on your permissions](../../administration/using/users-management.md).

To edit the properties of an email or an email template, use the **[!UICONTROL Edit properties]** button.

![](assets/delivery_options_1.png)

### General parameters {#general-parameters}

On the top of the email parameter screen, identify the email using the **[!UICONTROL Label]** and **[!UICONTROL ID]** fields. 이 정보는 인터페이스에 표시되지만 메시지 받는 사람에게는 표시되지 않습니다.

![](assets/delivery_options_2.png)

>[!CAUTION]
>
>ID는 고유해야 합니다.

**[!UICONTROL Brand]** 이 필드에서 게재에 연결된 브랜드를 선택할 수 있습니다. For more information on using and configuring brands, refer to the [Branding](../../administration/using/branding.md) section.

**[!UICONTROL Campaign]** 필드에서 이메일에 연결된 캠페인을 입력할 수 있습니다.

You can also add a **[!UICONTROL Description]** in the corresponding field and edit the image displayed on the email thumbnail in the lists.

### Sending parameters {#sending-parameters}

**[!UICONTROL Send]** 이 섹션은 이메일 템플릿에만 사용할 수 있습니다. 여기에는 다음 매개 변수가 포함됩니다.

#### Retries parameters {#retries-parameters}

일시적으로 배달되지 않은 메시지는 자동으로 재시도할 수 있습니다. This section indicates how many retries should be performed the day after the send is started ( **[!UICONTROL Max. number of retries]** ) and the minimum delay between retries ( **[!UICONTROL Retry period]** ).

기본적으로 최소 한 시간의 간격이 있는 첫 번째 날에 대한 5 회 재시도 횟수는 하루 중 24 시간에 걸쳐 분산됩니다. One retry per day is programmed after that and until the delivery deadline, which is defined in the [Validity period parameters](../../administration/using/configuring-email-channel.md#validity-period-parameters) section.

재시도 횟수는 전 세계 (Adobe 기술 관리자에게 문의) 또는 각 배달 또는 전달 템플릿에 대해 전체적으로 변경할 수 있습니다.

**[!UICONTROL Test SMTP delivery]** 이 옵션을 사용하면 SMTP를 통해 메시지 전송을 테스트할 수 있습니다. SMTP 서버와 연결할 때까지 메시지가 처리되지만 전송되지 않습니다. For more information on configuring SMTP, refer to the [List of email SMTP parameters](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters) section.

#### Email format parameters {#email-format-parameters}

전송할 이메일의 형식을 구성할 수 있습니다. 다음 세 가지 옵션을 사용할 수 있습니다.

* **수신자 환경 설정 사용** (기본 모드): 메시지 형식은 수신자 프로필에 저장된 데이터에 따라 정의되며 **기본적으로 이메일 형식** 필드 (@ Emailformat) 에 저장됩니다. 받는 사람이 특정 형식의 메시지를 수신하려는 경우 이 형식은 발송된 형식입니다. 필드가 완료되지 않으면 여러 부분 대체 메시지가 전송됩니다 (아래 참조).
* **수신자 메일 클라이언트가 가장 적절한 형식을 선택하도록 허용 (다중 부분 대체**): 이 메시지에는 두 가지 형식이 포함되어 있습니다. 텍스트 및 HTML. 수신 시 표시되는 형식은 수신자의 메일 소프트웨어 구성에 따라 달라집니다 (다제 대안).

   >[!CAUTION]
   >
   >이 옵션은 두 버전의 메시지를 포함합니다. 메시지 크기가 더 크므로 배달 처리량에 영향을 줍니다.

* **모든 메시지를 텍스트 형식으로 보내기**: 메시지는 텍스트 형식으로 전송됩니다. HTML 형식은 전송되지 않지만 받는 사람이 메시지의 링크를 클릭할 때에만 미러 페이지에 사용됩니다.

### Validity period parameters {#validity-period-parameters}

The **[!UICONTROL Validity]** section contains the following parameters:

* **[!UICONTROL Explicitly set validity dates]**: 이 상자를 선택 취소하면 **[!UICONTROL Delivery duration]** 및 **[!UICONTROL Resource validity limit]** 필드에 지속 기간을 입력해야 합니다. 특정 시간 및 날짜를 정의하려면 이 확인란을 선택합니다.
* **[!UICONTROL Delivery duration]**: Adobe Campaign는 시작 날짜에 메시지를 보냅니다. 이 필드에서 메시지를 보낼 수 있는 기간을 지정할 수 있습니다.
* **[!UICONTROL Resource validity duration]**: 이 필드는 주로 미러 페이지 및 이미지에 대해 업로드된 리소스에 사용됩니다. 이 페이지의 리소스는 디스크 공간을 절약하기 위해 제한된 기간 동안 유효합니다.
* **[!UICONTROL Mirror page management]**: 미러 페이지는 웹 브라우저를 통해 온라인에서 액세스할 수 있는 HTML 페이지입니다. 해당 컨텐츠는 이메일 콘텐츠와 동일합니다. 기본적으로 링크 페이지에 링크가 삽입되어 있으면 미러 페이지가 생성됩니다. 이 필드에서 이 페이지를 생성하는 방법을 수정할 수 있습니다.

   >[!CAUTION]
   >
   >미러 페이지에 대한 전자 메일에 대해 HTML 콘텐츠가 정의되어 있어야 합니다.

   * **[!UICONTROL Generate the mirror page if a mirror link appears in the email content]** (기본 모드): 링크 페이지에 링크가 삽입되어 있으면 미러 페이지가 생성됩니다.
   * **미러 페이지 생성 강제**&#x200B;적용: 미러 페이지에 대한 링크가 메시지에 삽입되지 않더라도 미러 페이지가 생성됩니다.
   * **미러 페이지는 생성하지 마십시오**. 링크가 메시지에 있어도 미러 페이지가 생성되지 않습니다.
   * **메시지 ID만 사용하여 액세스할 수 있는 미러 페이지를 생성합니다**. 이 옵션을 사용하면 배달 로그 창에서 개인화 정보와 함께 미러 페이지의 컨텐츠에 액세스할 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Explicitly set validity dates]** AND **[!UICONTROL Delivery duration]** 매개 변수는 트랜잭션 메시지에 적용되지 않습니다. For more on transactional messaging, see [this section](../../channels/using/about-transactional-messaging.md).

### Tracking parameters {#tracking-parameters}

The **[!UICONTROL Tracking]** section contains the following parameters:

* **[!UICONTROL Activate tracking]**: 메시지 URL 추적을 활성화/비활성화할 수 있습니다. To manage tracking for each message URL, use the **[!UICONTROL Links]** icon in the Email Designer action bar. See [About tracked URLs](../../designing/using/about-tracked-urls.md).
* **[!UICONTROL Tracking validity limit]**: URL에서 추적이 활성화되는 기간을 정의할 수 있습니다.
* **[!UICONTROL Substitution URL for expired URLs]**: 추적이 만료된 후 표시되는 웹 페이지의 URL를 입력할 수 있습니다.

### Advanced parameters {#advanced-parameters}

**[!UICONTROL Advanced parameters]** 섹션에는 여러 매개 변수가 포함되어 있습니다.

처음 두 필드를 사용하여 이메일 메시지 헤더 (답글 주소 및 회신 주소 텍스트) 에 필요한 정보를 입력할 수 있습니다. 이러한 정보는 개인화할 수 있습니다. 이렇게 하려면 변경할 필드의 오른쪽에 있는 단추를 클릭한 다음 개인화 필드를 추가합니다. Inserting and using the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

#### Target context {#target-context}

타깃팅 컨텍스트를 사용하면 이메일 타깃팅 (대상 정의 화면에서) 및 개인화 (HTML 컨텐츠 편집기에서 개인화 필드 정의) 에 사용할 테이블 세트를 정의할 수 있습니다.

#### Routing {#routing}

이 필드는 사용된 라우팅 모드를 나타냅니다. 외부 계정을 참조합니다. 예를 들어, 특정 브랜딩 구성을 포함하는 외부 계정을 사용하려는 경우 사용할 수 있습니다.

>[!NOTE]
>
>External accounts are accessible via the **Administration** &gt; **Application settings** &gt; **External accounts** menu.

#### Preparation {#preparation}

Preparing messages is detailed in the [Approving messages](../../sending/using/preparing-the-send.md) section.

* **[!UICONTROL Typology]**: 보내기 전에 콘텐트와 구성을 확인하려면 메시지를 준비해야 합니다. The verification rules applied during the preparation phase are defined in a **typology**. 예를 들어 이메일에는 제목, URL 및 이미지 확인이 포함됩니다. 이 필드에 적용할 유형을 선택합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]****[!UICONTROL Typologies]** &gt; 메뉴를 통해 액세스할 수 있는 유형화는 [유형 지정](../../administration/using/about-typology-rules.md) 섹션에 표시됩니다.

* **[!UICONTROL Compute the label during delivery preparation]**: 개인화 필드, 컨텐츠 블록 및 동적 텍스트를 사용하여 메시지 준비 단계 동안 이메일의 레이블 값을 계산할 수 있습니다.

   또한 워크플로우의 외부 신호 활동으로 선언된 이벤트 변수를 사용하여 배달 레이블을 개인화할 수도 있습니다. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md).

* **[!UICONTROL Save SQL queries in the log]**: 이 옵션을 사용하면 준비 단계 동안 저널에서 SQL 쿼리 로그를 추가할 수 있습니다.

### List of email SMTP parameters {#list-of-email-smtp-parameters}

The **[!UICONTROL SMTP]** section contains the following parameters:

* **[!UICONTROL Character encoding]**: 메시지 인코딩을 강제 적용하려면 **[!UICONTROL Force encoding]** 상자를 선택한 다음 사용할 인코딩을 선택합니다.
* **[!UICONTROL Bounce mails]**: 기본적으로 바운스 이메일은 플랫폼의 오류 받은 편지함에서 수신됩니다 ( **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Email]** &gt; **[!UICONTROL Configuration]** 화면에 정의됨). To define a specific error address for an email, enter the address in the **[!UICONTROL Error address]** field.
* **[!UICONTROL Additional SMTP headers]**: 이 옵션을 사용하면 추가 SMTP 헤더를 메시지에 추가할 수 있습니다. **[!UICONTROL Headers]** 필드에 입력된 스크립트는 이름별로 한 줄의 헤더를 참조해야 **합니다.**&#x200B;값. 필요한 경우 값이 자동으로 인코딩됩니다.

   >[!CAUTION]
   >
   >추가 SMTP 헤더를 삽입하는 스크립트를 추가하는 것은 고급 사용자를 위해 예약됩니다. 이 스크립트의 구문은 이 컨텐츠 유형의 요구 사항을 준수해야 합니다. 사용하지 않은 공간, 빈 선 없음 등은

### List of access authorization parameters {#list-of-access-authorization-parameters}

The **[!UICONTROL Access authorization]** section contains the following parameters:

* **[!UICONTROL Organizational unit]** 이 필드에서는 이 이메일의 액세스를 특정 사용자에게 제한할 수 있습니다. 지정된 단위 또는 상위 단위와 연결된 사용자는 이 이메일에 대한 읽기 및 쓰기 권한을 갖게 됩니다. 하위 단위와 연결된 사용자는 이 이메일에 대한 읽기 권한만 갖게 됩니다.

   >[!NOTE]
   >
   >**관리** &gt; **사용자 및 보안** 메뉴를 통해 조직 단위를 구성할 수 있습니다.

* **[!UICONTROL Created by]**, **[!UICONTROL Created]****[!UICONTROL Modified by]** 및 **[!UICONTROL Last modified]** 필드는 자동으로 완성됩니다.

## Archiving emails {#archiving-emails}

플랫폼에서 보낸 이메일의 사본을 유지하도록 Adobe Campaign를 구성할 수 있습니다.

그러나 Adobe Campaign 자체에서는 보관된 파일을 관리하지 않습니다. 원하는 메시지를 외부 시스템을 사용하여 처리 및 보관할 수 있는 전용 주소로 보낼 수 있습니다.

배달 템플릿에서 활성화하면 이 기능을 사용하면 해당 보낸 메시지의 정확한 사본을 지정해야 하는 숨은 참조 이메일 주소 (배달 받는 사람에게 보이지 않음) 로 보낼 수 있습니다.

### Recommendations and limitations {#recommendations-and-limitations}

* 이 기능은 선택 사항입니다. 사용권 계약을 확인하고 계정 관리자에게 문의하여 정품 인증을 받으십시오.
* 하나의 숨은 참조 이메일 주소만 사용할 수 있습니다.
* 성공적으로 전송된 이메일만 계정에서 받습니다. 바운스는 그렇지 않습니다.
* 개인 정보 보호 상의 이유로 BCC 이메일은 PII (개인 식별 정보) 를 안전하게 저장할 수 있는 보관 시스템에서 처리해야 합니다.
* 새 배달 템플릿을 만들 때, 옵션을 구입한 경우에도 기본적으로 이메일 BCC가 활성화되지 않습니다. 사용할 각 배달 템플릿에서 수동으로 활성화해야 합니다.

### Activating email archiving {#activating-email-archiving}

Email BCC is activated in the [email template](../../start/using/about-templates.md), through a dedicated option:

1. **리소스** &gt; **템플릿** &gt; **배달 템플릿으로 이동합니다**.
1. Duplicate the out-of-the-box **[!UICONTROL Send via email]** template.
1. 복제된 템플릿을 선택합니다.
1. Click the **[!UICONTROL Edit properties]** button to edit the template's properties.
1. **[!UICONTROL Send]** 섹션을 확장합니다.
1. **[!UICONTROL Archive emails]** 이 템플릿을 기반으로 배달된 모든 메시지의 사본을 보관하려면 상자를 선택합니다.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>If the emails sent to the BCC address are opened and clicked through, this will be taken into account in the **[!UICONTROL Total opens]** and **[!UICONTROL Clicks]** from the send analysis, which could cause some miscalculations.

