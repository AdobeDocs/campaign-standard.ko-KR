---
title: 외부 계정
seo-title: 외부 계정
description: 외부 계정
seo-description: SFTP 서버와 같은 외부 시스템과 연결되도록 외부 계정을 구성합니다.
page-status-flag: 정품 인증 안 함
uuid: 5 D 2 E 2 E 3 D -5 D 1 F -4466-97 E 5-842 C 50390146
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: application-settings
discoiquuid: d 5 c 6 a 3 d 4-f 767-46 c 1-a 8 c 0-3 b 9 dc 52 dcea 8
internal: n
snippet: Y
context-tags: extaccount, main; Extaccount, 개요
translation-type: tm+mt
source-git-commit: 0fcedd464ae2074e7eda793bbf20cc53ce04f324

---


# External accounts{#external-accounts}

외부 계정은 Adobe Campaign 외부에 있는 서버에 대한 액세스를 구성하고 테스트할 수 있도록 해주는 구성입니다.

이러한 외부 계정은 캠페인 워크플로우에 사용하여 데이터에 액세스하고 관리할 수 있습니다.

다음과 같은 유형의 외부 계정을 설정할 수 있습니다.

* Sftp. For more on this, refer to [this section](../../administration/using/external-accounts.md#sftp-external-account).
* Amazon Storage Service (S 3). For more on this, refer to [this section](../../administration/using/external-accounts.md#amazon-s3-external-account).
* Adobe Experience Manager. For more on this, refer to [this section](../../administration/using/external-accounts.md#adobe-experience-manager-external-account).
* Adobe Analytics. For more on this, refer to [this section](../../integrating/using/configure-campaign-analytics-integration.md).
* Google recaptcha. For more on this, refer to [this section](../../administration/using/external-accounts.md#google-recaptcha-external-account).

>[!NOTE]
>
>제품 제공 과정에서 Adobe는 다른 유형의 외부 계정을 사용합니다. Campaign Standard 17.9 릴리스에서는 FTP 외부 계정을 여전히 정의할 수 있지만 새 워크플로우 활동에서는 더 이상 사용할 수 없습니다. 이미 연결이 설정된 경우 여전히 활성화됩니다.

External accounts can be configured by administrators under the **[!UICONTROL Administration > Application settings > External accounts]** menu.

## Creating an external account {#creating-an-external-account}

Adobe Campaign 에는 사전 정의된 외부 계정 세트가 포함되어 있습니다. 파일 전송에 사용되는 FTP 서버와 같은 외부 시스템과 연결을 설정하기 위해 고유한 외부 계정을 만들 수 있습니다.

외부 계정은 기술 워크플로우 또는 캠페인 워크플로우와 같은 기술 프로세스에서 사용됩니다. 워크플로우에서 파일 전송 또는 기타 애플리케이션 (Adobe Target, Experience Manager 등) 과의 데이터 교환을 설정할 때 외부 계정을 선택해야 합니다.

1. **[!UICONTROL Create]** 단추를 클릭합니다.
1. 레이블을 입력합니다. 워크플로우에서 외부 계정을 선택할 때 레이블과 ID가 사용됩니다.
1. 만들려는 계정 유형을 선택합니다.
1. 자격 증명, 서버 주소, 포트 번호 및 관련 키를 지정하여 계정에 대한 액세스 권한을 구성합니다.

   필요한 정보는 일반적으로 연결 중인 서버의 공급자가 제공합니다.

1. 계정을 저장합니다.

외부 계정이 만들어져 계정 목록에 추가됩니다. 이제 워크플로우 활동 및 전달 속성에서 데이터/파일 전송 또는 라우팅 구성에서 사용할 수 있습니다.

## SFTP external account {#sftp-external-account}

다른 외부 계정 유형은 정보를 지정해야 합니다.

Sftp 외부 계정의 경우 다음 세부 정보를 제공합니다.

* 서버 주소. For example, **ftp.domain.com**.
* 포트 번호. **예를 들면 22 입니다.**
* SFTP 서버 자격 증명: 서버에 연결하는 데 사용되는 계정 이름 및 암호입니다.

### Adobe hosted SFTP server recommendations {#adobe-hosted-sftp-server-recommendations}

ETL 용도의 파일 및 데이터를 관리할 때 이러한 파일은 Adobe가 제공하는 호스팅 SFTP 서버에 저장됩니다. 이 Sftp는 파일의 보유 및 삭제를 제어할 수 있는 임시 저장 공간으로 설계되었습니다.

올바르게 사용하거나 모니터링하지 않는 경우 이 공간은 서버에서 사용할 수 있는 물리적 공간을 빠르게 채우고 심각한 문제를 일으킬 수 있습니다. 이로 인해 플랫폼에서 데이터가 손실되거나 손상될 수 있습니다.

이러한 문제를 방지하려면 아래의 우수 사례를 따르는 것이 좋습니다.

* 가능한 최소 데이터를 유지합니다.
* 키 기반 인증을 사용하여 암호 만료일을 방지합니다. Supported formats are **OpenSSH** and **SSH2** only. 캠페인 서버에 업로드하려면 Adobe 지원 팀에 공개 키를 제공해야 합니다.
* 필요할 때만 데이터를 보관합니다. 15 일이 최대 시간 한계입니다.
* 워크플로우를 사용하여 데이터를 적절히 삭제합니다 (데이터를 소비한 워크플로우에서 유지 관리).
* 워크플로우에서는 SFTP 업로드와 워크플로우의 일괄 처리를 사용합니다.
* 오류/예외를 처리합니다.
* Sftp에 로그인하여 무엇이 있는지 직접 확인할 수 있습니다.
* Sftp 디스크 관리는 주로 사용자의 책임입니다.

또한 Sftp 연결을 시작하려는 공개 IPS는 캠페인 인스턴스에서 허용 목록에 포함되어야 합니다. Whitelisting of IP addresses can be requested via a [support ticket](https://support.neolane.net), along with providing the public key to use for authentication.

SFTP 서버는 제어판에서 관리할 수 있습니다. For more information, refer to the [Control Panel documentation](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html).

>[!NOTE]
>
>제어판에서 호스팅되는 고객 관리자만 제어판을 사용할 수 있습니다.
Check if your instance is hosted on AWS [here](https://helpx.adobe.com/campaign/kb/control-panel-faq.html#IMSOrgID).

## Amazon S3 external account {#amazon-s3-external-account}

Amazon S 3 Server 필드는 다음과 같이 채워야 합니다.

```
<S3 bucket name>.s3.amazonaws.com/<s3 object path>
```

To store your file in S3 encrypted mode, check the **[!UICONTROL Keep files in S3 encrypted]** box.

![](assets/external_accounts_2.png)

필요한 정보는 일반적으로 연결 중인 서버의 공급자가 제공합니다.

Specify the **[!UICONTROL AWS Region]** associated to your endpoint. You can check the supported regions and signature versions in the official [Amazon S3 documentation](https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region) .

### Amazon S3 account recommendations {#amazon-s3-account-recommendations}

Amazon S 3 계정을 설정하는 데 도움이 되도록 다음과 같은 권장 사항을 따를 것을 권장합니다.

* 엄격한 버킷 정책을 만들어 S 3 버킷에 대한 액세스를 제한합니다. 버킷을 만드는 동안 버킷 정책을 구성할 수 있습니다. For more information, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//example-bucket-policies.html).
* While creating an external account, enable the encryption to store sensitive data in the S3 bucket by checking the **[!UICONTROL Keep files in S3 encrypted]** box.
* 버킷에서 개체에 액세스할 수 있는 사용자를 지정하려면 버킷 권한을 부여합니다. For more information on bucket permission, refer to the [Amazon S3 documentation](http://docs.aws.amazon.com/AmazonS3/latest/dev//access-control-overview.html)

## Adobe Experience Manager external account {#adobe-experience-manager-external-account}

Adobe Experience Manager 외부 계정은 Adobe Experience Manager와 캠페인을 통합할 때 사용됩니다.

Process and requirements related to this integration are available in [this document](../../integrating/using/about-campaign-integrations.md).

이 새 외부 계정을 설정할 때 다음 세부 정보를 제공해야 합니다.

* 서버: Adobe Experience Manager 서버의 URL를 입력합니다. For example, **http://aem.domain.com:4502**.
* AEM 계정 자격 증명: Adobe Experience Manager 인스턴스에 액세스할 계정을 사용합니다. Experience Manager에서 캠페인 원격 그룹의 계정 부분에 속해야 합니다.

## Google reCAPTCHA external account {#google-recaptcha-external-account}

>[!NOTE]
>
>Google recaptcha 구성을 사용하려면 Google 계정이 필요합니다.

Google recaptcha 메커니즘을 사용하면 봇으로 인한 스팸 및 남용으로부터 랜딩 페이지를 보호할 수 있습니다. 이 기능은 고객과의 상호 작용이 필요 없고 사이트와의 상호 작용을 기반으로 하므로 고객에게 방해가 되지 않습니다. To register your site, refer to this [page](https://www.google.com/recaptcha/admin/create). v 3 recaptcha 유형을 선택해야 합니다.

랜딩 페이지에 Google recaptcha v 3를 추가하려면 먼저 외부 계정에서 이 계정을 구성해야 합니다. For more information on how to add it to your landing page, refer to this [section](../../channels/using/designing-a-landing-page.md#setting-google-recaptcha).

Google recaptcha v 3 외부 계정의 경우 다음 세부 정보를 제공합니다.

* A **[!UICONTROL Label]** and **[!UICONTROL ID]** of your external account
* **[!UICONTROL Type]**: Google recaptcha
* Your **[!UICONTROL Site key]** and **[!UICONTROL Site secret]**
* A **[!UICONTROL Threshold]** between 0 and 1

   The 0.0 **[!UICONTROL Threshold]** value means that it is likely a bot and 1.0 likely a good interaction. 기본적으로 임계값은 0.5를 사용할 수 있습니다.

![](assets/external_accounts_3.png)

