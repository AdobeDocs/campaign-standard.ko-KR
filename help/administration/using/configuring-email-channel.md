---
title: Adobe Campaign Standard에서 이메일 채널 구성
description: Adobe Campaign Standard에서 이메일 채널을 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 9fddb655-b445-41f3-9b02-5d356fc88aa1
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3752d41f-8c59-4fad-b30f-e98e09cd74a8
context-tags: extAccountEmail,overview;emailConfig,main;ruleSet,overview;delivery,properties,open
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e2303055b3370efab204adbdb1b9f567a555a23f
workflow-type: tm+mt
source-wordcount: '2331'
ht-degree: 0%

---


# 이메일 채널 구성{#configuring-email-channel}

캠페인 [관리자는](../../administration/using/users-management.md#functional-administrators)이메일 채널 설정을 구성할 수 있습니다. 이러한 고급 설정에는 일반 이메일 채널 매개 변수, 이메일 라우팅 계정, 이메일 처리 규칙 및 이메일 속성이 포함됩니다. 이 페이지에서는 일반 이메일 및 전송 매개 변수의 기본값을 편집하는 방법을 알아봅니다.

일부 이메일 설정은 이제 Adobe Campaign 고급 MTA에서 관리됩니다. 따라서:
* 캠페인 사용자 인터페이스의 일부 구성이 더 이상 적용되지 않습니다.
   * [ **[!UICONTROL Retries]** 구성] 메뉴 [및 이메일 속성](#email-channel-parameters) 의 매개 변수 [전송](#retries-parameters) 의설정.
   * [ **[!UICONTROL MX management]** 이메일 처리 규칙] 메뉴의 **[!UICONTROL Domain management]** 및 규칙 [](#email-processing-rules).

* 다른 매개 변수는 이제 향상된 MTA에서 부분적으로 관리되지만 일부 구성은 Campaign 내에서 계속 수행할 수 있습니다. 영향을 받는 설정은 다음과 같습니다.
   * 메뉴의 **[!UICONTROL Message delivery duration]** 매개 **[!UICONTROL Configuration]** 변수입니다. 자세한 내용은 [이 섹션을 참조하십시오](#email-channel-parameters).
   * 섹션의 **[!UICONTROL Delivery duration]** 또는 **[!UICONTROL Validity limit for sending messages]** 매개 **[!UICONTROL Validity period]** 변수입니다. 자세한 내용은 [이 섹션을 참조하십시오](#validity-period-parameters).
   * The **[!UICONTROL Bounce mails]** rules in **[!UICONTROL Email processing rules]**. 자세한 내용은 [이 섹션을 참조하십시오](#email-processing-rules).

## 이메일 채널 매개 변수 {#email-channel-parameters}

이메일 구성 화면에서는 이메일 채널의 매개 변수를 정의할 수 있습니다. 관리자는 **[!UICONTROL Administration]>[!UICONTROL Channels]>[!UICONTROL Email]>[!UICONTROL Configuration]**메뉴에서 이러한 구성에 액세스할 수 있습니다.

![](assets/channels_1.png)

* **공인 마스크 필드**

   이 **[!UICONTROL Header parameters of sent emails]** 섹션에는 이메일을 받는 사람(보낸 사람 주소)에게 보내고 비동기 바운스, 사무실 밖 회신 등과 같은 자동 답글을 다시 보낼 수 있도록 사용할 수 있는 권한이 있는 이메일 주소가 나열됩니다. (오류 주소).  Adobe Campaign은 메시지 준비 단계 동안 입력한 주소가 유효한지 확인합니다. 이 운영 모드에서는 전달 가능성 문제를 유발할 수 있는 주소가 사용되지 않습니다.
   * 발신자와 오류 주소는 모두 Adobe에서 설정합니다. 이러한 필드는 비워 둘 수 없습니다.
   * 이러한 필드는 편집할 수 없습니다. 주소를 업데이트하려면 Adobe 고객 지원 센터에 문의하십시오.
   * 다른 주소를 추가하려면 [제어판](https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html) 을 사용하여 새 하위 도메인을 설정하거나 Adobe 고객 지원 센터에 문의하십시오. 여러 개의 마스크를 사용하는 경우 쉼표로 구분됩니다.
   * *@yourdomain.com과 같은 별을 사용하여 주소를 설정하는 것이 좋습니다. 이렇게 하면 하위 도메인 이름으로 끝나는 주소를 사용할 수 있습니다.

* **전달 능력**

   이 **[!UICONTROL Delivery reports ID]** 는 Adobe 고객 지원 센터에서 제공합니다. 이 ID는 기술 제공 가능 보고서에서 사용되는 배달 가능성 ID로 각 인스턴스를 식별합니다.
   <!--The Technical Deliverability report is not accessible through the UI in ACS. It will be replaced with 250ok in the future (project starting).-->

* **전달 매개 변수**

   Adobe Campaign은 시작 날짜에 시작되는 메시지를 전송합니다. 이 **[!UICONTROL Message delivery duration]** 필드를 사용하면 배달 중에 일시적인 오류나 소프트 바운스가 발생하는 메시지가 다시 시도될 시간대를 지정할 수 있습니다.

   >[!IMPORTANT]
   >
   >**이제 캠페인의 이 매개 변수는 3.5일 이내로 설정된 경우에만 사용됩니다.** 3.5일이 넘는 값을 정의하는 경우 Adobe Campaign 향상된 MTA에서 관리되므로 이 값을 고려하지 않습니다.

   이 **[!UICONTROL Online resources validity duration]** 필드는 주로 미러 페이지와 이미지에 대해 업로드된 리소스에 사용됩니다. 이 페이지의 리소스는 제한된 시간 동안 유효합니다(디스크 공간을 절약하려면).

* **재시도**

   일시적으로 배달되지 않은 메시지는 자동 재시도가 적용됩니다. 이 방법에 대한 자세한 내용은 배달 임시 실패 후 [재시도를 참조하십시오](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

   >[!NOTE]
   >
   >수행할 최대 재시도 횟수와 재시도 사이의 최소 지연 시간은 Adobe Campaign 향상된 MTA에 의해 관리됩니다. 이는 IP가 과거 및 현재 지정된 도메인에서 모두 수행하는 빈도를 기준으로 합니다. 캠페인의 **재시도** 설정은 무시됩니다.

   <!--This section indicates how many retries should be performed the day after the send is started (**Number of retries**) and the minimum delay between retries (**Retry period**). By default, five retries are scheduled for the first day with a minimum interval of one hour, spread out over the 24 hours of the day. One retry per day is programmed after that and until the delivery deadline, which is defined in the **[!UICONTROL Delivery parameters]** section.-->

* **이메일 격리 매개 변수**

   소프트 **[!UICONTROL Time between two significant errors]** 바운스 실패 시 응용 프로그램이 오류 카운터를 증가시키기 전에 기다리는 시간을 정의하는 값을 필드에 입력합니다. 1일 동안 기본값은 **&quot;1d&quot;**&#x200B;입니다.

   값이 **[!UICONTROL Maximum number of errors before quarantine]** 도달하면 이메일 주소가 격리됩니다. 기본값은 **&quot;5&quot;입니다**. 5번째 오류 때문에 주소가 격리될 것이다. 즉, 연락처는 후속 배달에서 자동으로 제외됩니다.
   <!--Actually the way ACS works is that the address is already on the quarantine list on the first bounce, but with a different status meaning that the error count has started.-->

   검역에 대한 자세한 내용은 [검역 관리 이해를 참조하십시오](../../sending/using/understanding-quarantine-management.md).

## 이메일 라우팅 계정 {#email-routing-accounts}

기본적으로 **[!UICONTROL Integrated email routing]** 외부 계정이 제공됩니다. 여기에는 애플리케이션이 이메일을 보낼 수 있는 기술 매개 변수가 포함되어 있습니다.

![](assets/channels_2.png)

계정 유형은 항상 로 설정되어야 **[!UICONTROL Routing]**&#x200B;하며, 채널 **[!UICONTROL Email]** 과 배달 모드를 다음으로 설정해야 합니다 **[!UICONTROL Bulk delivery]**.

**관련 항목**:

[외부 계정](../../administration/using/external-accounts.md)

## 이메일 처리 규칙 {#email-processing-rules}

관리자가 메뉴를 통해 액세스할 **[!UICONTROL Email processing rules]** 수 **[!UICONTROL Administration > Channels > Email]** 있습니다.

이메일 도메인과 MX 규칙은 이제 Adobe Campaign 향상된 MTA에서 관리됩니다.
* **DKIM(DomainKeys Identified Mail)** 이메일 인증 서명은 모든 도메인이 있는 모든 메시지에 대해 향상된 MTA를 통해 수행됩니다. 향상된 MTA 수준에서 별도로 명시되지 않는 한 **보낸 사람 ID**, **도메인 키**&#x200B;또는 **S/MIME** 으로 서명하지않습니다.
* Enhanced MTA는 자체 MX 규칙을 사용하여 고유한 내역 이메일 명성을 기반으로, 이메일을 전송하는 도메인에서 오는 실시간 피드백에 따라 도메인별로 처리량을 사용자 정의할 수 있습니다.

### 바운스 메일 {#bounce-mails}

비동기 바운스는 여전히 규칙을 통해 Campaign inMail 프로세스에서 자격을 **[!UICONTROL Bounce mails]** 갖습니다.

이러한 규칙에는 원격 서버에서 반환할 수 있는 문자 문자열 목록이 포함되어 있어 오류를 평가할 수 있습니다(**하드**, 소프트 **** 또는 **무시됨**).

>[!NOTE]
>
>동기 배달 실패 오류 메시지의 경우 Adobe Campaign 향상된 MTA가 바운스 유형 및 자격을 결정하고 해당 정보를 Campaign에 다시 전송합니다.

바운스 메일 자격에 대한 자세한 내용은 이 [섹션을 참조하십시오](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification).

<!--Because they are now managed by the Enhanced MTA, the bounce qualifications in the Campaign **[!UICONTROL Message qualification]** table are no longer used. For more on bounce mail qualification, see this [section](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification).

### Management of email domains {#managing-email-domains}

The email domains are now managed by the Adobe Campaign Enhanced MTA. The Adobe Campaign **[!UICONTROL Domain management]** rules are no longer used.

**DKIM (DomainKeys Identified Mail)** email authentication signing is done by the Enhanced MTA for all messages with all domains. It does not sign with **Sender ID**, **DomainKeys**, or **S/MIME** unless otherwise specified at the Enhanced MTA level.

### MX management {#mx-management}

The MX rules are now managed by the Adobe Campaign Enhanced MTA. The Adobe Campaign **[!UICONTROL MX management]** delivery throughput rules are no longer used.

The Enhanced MTA uses its own MX rules that allow it to customize your throughput by domain based on your own historical email reputation, and on the real-time feedback coming from the domains where you are sending emails.-->

## 이메일 속성 목록 {#list-of-email-properties}

이 섹션에서는 이메일 또는 이메일 템플릿의 속성 화면에서 사용할 수 있는 매개 변수 목록에 대해 자세히 설명합니다.

>[!NOTE]
>
>일부 매개 변수는 템플릿에서만 사용할 수 있습니다. 액세스할 수 있는 매개 변수 [는 사용 권한에 따라 다릅니다](../../administration/using/users-management.md).

이메일 또는 이메일 템플릿의 속성을 편집하려면 **[!UICONTROL Edit properties]** 단추를 사용합니다.

![](assets/delivery_options_1.png)

### 일반 매개 변수 {#general-parameters}

이메일 매개 변수 화면의 맨 위에서 **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 필드를 사용하여 이메일을 식별합니다. 이 정보는 인터페이스에 표시되지만 메시지 수신자는 볼 수 없습니다.

![](assets/delivery_options_2.png)

>[!IMPORTANT]
>
>ID는 고유해야 합니다.

이 **[!UICONTROL Brand]** 필드에서 게재에 연결된 브랜드를 선택할 수 있습니다. 브랜드 사용 및 구성에 대한 자세한 내용은 [브랜딩](../../administration/using/branding.md) 섹션을 참조하십시오.

이 **[!UICONTROL Campaign]** 필드에서는 이메일에 연결된 캠페인을 입력할 수 있습니다.

해당 필드 **[!UICONTROL Description]** 에 이미지를 추가하고 목록의 이메일 축소판에 표시되는 이미지를 편집할 수도 있습니다.

### 매개 변수 전송 {#sending-parameters}

이 **[!UICONTROL Send]** 섹션은 이메일 템플릿에만 사용할 수 있습니다. 여기에는 다음 매개 변수가 포함되어 있습니다.

#### 재시도 매개 변수 {#retries-parameters}

일시적으로 배달되지 않은 메시지는 자동 재시도가 적용됩니다. 이 방법에 대한 자세한 내용은 배달 임시 실패 후 [재시도를 참조하십시오](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>이제 IP가 이전 및 현재 지정된 도메인에서 얼마나 성과가 있는지 기준으로 하여 재시도 간격 및 최대 재시도 횟수를 Adobe Campaign 고급 MTA가 관리합니다. 캠페인 **재시도** 설정은 무시됩니다.

<!--This section indicates how many retries should be performed the day after the send is started ( **[!UICONTROL Max. number of retries]** ) and the minimum delay between retries ( **[!UICONTROL Retry period]** ).

By default, five retries are scheduled for the first day with a minimum interval of one hour, spread out over the 24 hours of the day. One retry per day is programmed after that and until the delivery deadline, which is defined in the [Validity period parameters](#validity-period-parameters) section.

The number of retries can be changed globally (contact your Adobe technical administrator) or for each delivery or delivery template.-->

Campaign에 **설정된** [배달 기간 설정](#validity-period-parameters) ( **유효 기간 매개 변수**&#x200B;섹션에 정의됨)은 그대로 유지되지만 최대 3.5일만유지됩니다. 이 시점에서 재시도 큐의 모든 메시지는 대기열에서 제거되고 바운스로 다시 전송됩니다. 배달 실패에 대한 자세한 내용은 이 [섹션을 참조하십시오](../../sending/using/understanding-delivery-failures.md#about-delivery-failures).

#### 이메일 형식 매개 변수 {#email-format-parameters}

보낼 이메일의 형식을 구성할 수 있습니다. 다음 세 가지 옵션을 사용할 수 있습니다.

* **수신자 환경 설정** 사용(기본 모드): 메시지 형식은 수신자 프로필에 저장된 데이터에 따라 정의되며 기본적으로 **이메일 형식** 필드(@emailFormat)에 저장됩니다. 받는 사람이 특정 형식으로 메시지를 수신하려는 경우 보낸 형식입니다. 필드가 완료되지 않으면 다중 부분 대체 메시지가 전송됩니다(아래 참조).
* **받는 사람 메일 클라이언트가 가장 적절한 형식(다중 부분 대체)을 선택할 수 있도록 합니다**. 메시지에는 두 형식 모두 포함되어 있습니다. 텍스트 및 HTML을 참조하십시오. 수신에 따라 표시되는 형식은 받는 사람의 메일 소프트웨어(다중 부분 대체)의 구성에 따라 달라집니다.

   >[!IMPORTANT]
   >
   >이 옵션에는 메시지의 두 버전이 모두 포함됩니다. 따라서 메시지 크기가 더 크기 때문에 배달 처리량에 영향을 줍니다.

* **모든 메시지를 텍스트 형식으로 보내기**: 메시지는 텍스트 형식으로 전송됩니다. HTML 형식은 전송되지 않지만 수신자가 메시지의 링크를 클릭할 때만 미러 페이지에 사용됩니다.

#### SMTP 테스트 모드 {#smtp-test-mode}

이 **[!UICONTROL Enable SMTP test mode]** 옵션을 사용하면 실제로 메시지를 보내지 않고 SMTP 연결을 통해 이메일 전송을 테스트할 수 있습니다.
메시지는 SMTP 서버와의 연결이 완료될 때까지 처리되지만 전송되지 않습니다.

![](assets/smtp-test-mode.png)

이 옵션은 이메일 및 이메일 템플릿에 사용할 수 있습니다.

이메일 템플릿에 대해 SMTP 테스트 모드 옵션을 활성화하면 이 템플릿에서 만든 모든 이메일 메시지에 이 옵션이 활성화됩니다.

>[!IMPORTANT]
>
>이메일에 대해 이 옵션을 활성화하면 선택 취소될 때까지 메시지가 전송되지 않습니다.
>이메일 또는 이메일 템플릿 대시보드에 경고가 표시됩니다.

SMTP 구성에 대한 자세한 내용은 이메일 SMTP 매개 변수 [목록 섹션을 참조하십시오](#list-of-email-smtp-parameters) .

### 유효 기간 매개변수 {#validity-period-parameters}

섹션에는 다음 매개 변수가 **[!UICONTROL Validity period]** 포함되어 있습니다.

![](assets/delivery-validity-period.png)

* **[!UICONTROL Explicitly set validity dates]**: 이 상자를 선택 취소하면 **[!UICONTROL Delivery duration]** 및 **[!UICONTROL Resource validity limit]** 필드에 기간을 입력해야 합니다.

   특정 시간과 날짜를 정의하려면 이 상자를 선택합니다.

   ![](assets/delivery-set-explicit-dates.png)

* **[!UICONTROL Delivery duration]** / **[!UICONTROL Validity limit for sending messages]**: Adobe Campaign은 시작 날짜에 시작되는 메시지를 전송합니다. 이 필드에서는 메시지를 보낼 수 있는 기간을 지정할 수 있습니다.

   >[!IMPORTANT]
   >
   >이 매개 변수는 이제 Adobe Campaign 향상된 MTA에서 관리합니다. **최대 3.5일 값을 정의해야 합니다.** 3.5일 이상의 값을 정의하면 고려되지 않습니다.

* **[!UICONTROL Resource validity duration]** / **[!UICONTROL Validity limit date for resources]**: 이 필드는 주로 미러 페이지 및 이미지에 대해 업로드된 리소스에 사용됩니다. 이 페이지의 리소스는 제한된 시간 동안 유효합니다(디스크 공간을 절약하려면).
* **[!UICONTROL Mirror page management]**: 미러 페이지는 웹 브라우저를 통해 온라인으로 액세스할 수 있는 HTML 페이지입니다. 컨텐츠는 이메일 컨텐츠와 동일합니다. 기본적으로 링크가 메일 컨텐츠에 삽입된 경우 미러 페이지가 생성됩니다. 이 필드에서는 이 페이지가 생성되는 방식을 수정할 수 있습니다.

   >[!IMPORTANT]
   >
   >미러 페이지를 만들 이메일에 대해 HTML 컨텐츠를 정의해야 합니다.

   * **[!UICONTROL Generate the mirror page if a mirror link appears in the email content]** (기본 모드): 링크가 메일 컨텐츠에 삽입되면 미러 페이지가 생성됩니다.
   * **미러 페이지를 강제로 생성합니다**. 미러 페이지에 대한 링크가 메시지에 삽입되지 않더라도 미러 페이지가 생성됩니다.
   * **미러 페이지를 생성하지 마십시오**. 링크가 메시지에 포함되어 있어도 미러 페이지가 생성되지 않습니다.
   * **메시지 ID만 사용하여 액세스할 수 있는 미러 페이지를 생성합니다**. 이 옵션을 사용하면 배달 로그 창에서 개인화 정보를 사용하여 미러 페이지의 컨텐츠에 액세스할 수 있습니다.

>[!NOTE]
>
>이 **[!UICONTROL Delivery duration]** 매개 변수는 트랜잭션 메시지에 적용되지 않습니다. 트랜잭션 메시지에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../channels/using/about-transactional-messaging.md).

### 추적 매개 변수 {#tracking-parameters}

섹션에는 다음 매개 변수가 **[!UICONTROL Tracking]** 포함되어 있습니다.

* **[!UICONTROL Activate tracking]**: 메시지 URL 추적을 활성화/비활성화할 수 있습니다. 각 메시지 URL에 대한 추적을 관리하려면 이메일 디자이너 작업 표시줄의 **[!UICONTROL Links]** 아이콘을 사용합니다. 추적된 [URL 정보를 참조하십시오](../../designing/using/links.md#about-tracked-urls).
* **[!UICONTROL Tracking validity limit]**: URL에서 추적이 활성화되는 기간을 정의할 수 있습니다.
* **[!UICONTROL Substitution URL for expired URLs]**: 추적이 만료되면 표시될 웹 페이지의 URL을 입력할 수 있습니다.

### 고급 매개 변수 {#advanced-parameters}

섹션에는 여러 매개 변수가 **[!UICONTROL Advanced parameters]** 포함되어 있습니다.

첫 번째 필드를 사용하면 이메일 메시지 헤더를 정교하게 작성하는 데 필요한 정보를 입력할 수 있습니다. 여기에서 회신 주소 및 텍스트와 발신자 주소(&quot;보낸 사람:&quot; 필드)를 관리할 수 있습니다. 이러한 정보는 개인화할 수 있습니다.

변경할 필드 오른쪽의 단추를 클릭한 다음 개인화 필드, 콘텐츠 블록 또는 동적 텍스트를 추가합니다.

![](assets/advancedparameters.png)

개인화 컨텐츠 삽입 및 사용은 [이메일 컨텐츠 개인화](../../designing/using/personalization.md) 문서에 자세히 설명되어 있습니다.

#### 타겟 컨텍스트 {#target-context}

타깃팅 컨텍스트를 사용하면 이메일 타깃팅(대상 정의 화면)과 개인화에 사용할 테이블 세트를 정의할 수 있습니다(HTML 컨텐츠 편집기에서 개인화 필드 정의).

#### 라우팅 {#routing}

이 필드는 사용되는 라우팅 모드를 나타냅니다. 외부 계정을 참조합니다. 예를 들어 특정 브랜딩 구성이 들어 있는 외부 계정을 사용하려는 경우 사용할 수 있습니다.

>[!NOTE]
>
>외부 계정은 **관리** > 응용 프로그램 설정 **>** 외부 계정 **** 메뉴를 통해 액세스할 수있습니다.

#### 준비 {#preparation}

메시지 준비에 대해서는 메시지 [승인](../../sending/using/preparing-the-send.md) 섹션에 자세히 설명되어 있습니다.

* **[!UICONTROL Typology]**: 보내기 전에 컨텐츠와 구성을 확인하기 위해 메시지를 준비해야 합니다. 준비 단계 동안 적용된 확인 규칙은 유형 **에서 정의됩니다**. 예를 들어 이메일의 경우 준비 과정에는 제목, URL 및 이미지 등이 포함됩니다. 이 필드에 적용할 유형을 선택합니다.

   >[!NOTE]
   >
   >> **[!UICONTROL Administration]** > 메뉴를 통해 액세스할 수 있는 Typolections는 **[!UICONTROL Channels]** 이 섹션에 **[!UICONTROL Typologies]** 설명되어 있습니다 [](../../sending/using/about-typology-rules.md).

* **[!UICONTROL Compute the label during delivery preparation]**: 개인화 필드, 컨텐츠 블록 및 동적 텍스트를 사용하여 메시지 준비 단계 동안 이메일의 레이블 값을 계산할 수 있습니다.

   또한 워크플로우의 외부 신호 활동으로 선언된 이벤트 변수를 사용하여 배달 레이블을 개인화할 수도 있습니다. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md).

* **[!UICONTROL Save SQL queries in the log]**: 이 옵션을 사용하면 준비 단계 동안 저널에 SQL 쿼리 로그를 추가할 수 있습니다.

#### 증명 설정 {#proof-settings}

이 섹션에서는 입체(proof)의 제목 줄에 사용할 기본 접두사를 구성할 수 있습니다. For more in this, refer to [this section](../../sending/using/sending-proofs.md).

### 이메일 SMTP 매개 변수 목록 {#list-of-email-smtp-parameters}

섹션에는 다음 매개 변수가 **[!UICONTROL SMTP]** 포함되어 있습니다.

* **[!UICONTROL Character encoding]**: 메시지 인코딩을 강제 **[!UICONTROL Force encoding]** 수행하려면 상자를 선택한 다음 사용할 인코딩을 선택합니다.
* **[!UICONTROL Bounce mails]**: 기본적으로 바운스 메일은 플랫폼의 오류 받은 편지함에서 수신됩니다( **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > **[!UICONTROL Configuration]** 화면에 정의됨). 이메일의 특정 오류 주소를 정의하려면 **[!UICONTROL Error address]** 필드에 주소를 입력합니다.
* **[!UICONTROL Additional SMTP headers]**: 이 옵션을 사용하면 메시지에 추가 SMTP 헤더를 추가할 수 있습니다. 필드에 입력한 스크립트는 **[!UICONTROL Headers]** 줄당 이름: **value**&#x200B;형식으로 한 개의 헤더를 참조해야 합니다. 필요한 경우 값이 자동으로 인코딩됩니다.

   >[!IMPORTANT]
   >
   >추가 SMTP 헤더 삽입용 스크립트 추가는 고급 사용자를 위해 예약되어 있습니다. 이 스크립트의 구문은 이 콘텐츠 형식의 요구 사항을 준수해야 합니다. 사용하지 않은 공간, 빈 줄 등이 없습니다.

### 액세스 권한 부여 매개 변수 목록 {#list-of-access-authorization-parameters}

섹션에는 다음 매개 변수가 **[!UICONTROL Access authorization]** 포함되어 있습니다.

* 이 **[!UICONTROL Organizational unit]** 필드에서는 특정 사용자에 대한 이 이메일에 대한 액세스를 제한할 수 있습니다. 지정한 장치 또는 상위 장치와 연결된 사용자는 이 이메일에 대한 읽기 및 쓰기 액세스 권한을 가집니다. 하위 단위와 연결된 사용자는 이 이메일에 대한 읽기 권한만 갖게 됩니다.

   >[!NOTE]
   >
   >[관리] > [ **사용자 및 보안** ] **메뉴를 통해 조직 단위를 구성할 수** 있습니다.

* 필드 **[!UICONTROL Created by]**, **[!UICONTROL Created]****[!UICONTROL Modified by]** 와 **[!UICONTROL Last modified]** 필드는 자동으로 완료됩니다.
