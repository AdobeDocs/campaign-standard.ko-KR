---
solution: Campaign Standard
product: campaign
title: 외부 계정
description: SFTP 서버와 같은 외부 시스템과의 연결을 설정하도록 외부 계정을 구성합니다.
audience: administration
content-type: reference
topic-tags: application-settings
context-tags: extAccount,main;extAccount,overview
translation-type: tm+mt
source-git-commit: 6dda990d046cceae2a0c0da87764d4b6a16d9ae8
workflow-type: tm+mt
source-wordcount: '1773'
ht-degree: 85%

---


# 외부 계정{#external-accounts}

외부 계정은 Adobe Campaign 외부에 있는 서버에 대한 액세스를 구성하고 테스트할 수 있는 구성입니다.

이러한 외부 계정은 Campaign 워크플로우에서 데이터 액세스 및 관리에 사용할 수 있습니다.

다음 유형의 외부 계정을 설정할 수 있습니다.

* SFTP. 자세한 정보는 [이 섹션](#sftp-external-account)을 참조하십시오.
* Amazon Storage Service(S3). 자세한 정보는 [이 섹션](#amazon-s3-external-account)을 참조하십시오.
* Adobe Experience Manager. 자세한 정보는 [이 섹션](#adobe-experience-manager-external-account)을 참조하십시오.
* Adobe Analytics. 자세한 정보는 [이 섹션](../../integrating/using/configure-campaign-analytics-integration.md)을 참조하십시오.
* Google reCAPTCHA. 자세한 정보는 [이 섹션](#google-recaptcha-external-account)을 참조하십시오.
* Microsoft Azure Blob 저장 공간. 자세한 정보는 [이 섹션](#microsoft-azure-external-account)을 참조하십시오.
* OAuth 2.0. 자세한 내용은 [이 섹션](#oauth-account)을 참조하십시오.

>[!NOTE]
>
>기타 유형의 외부 계정은 제품 프로비전 프로세스 동안 Adobe에서 사용됩니다. Campaign Standard 17.9 릴리스부터는 FTP 외부 계정을 정의할 수 있지만 새로운 워크플로우 활동에서는 더 이상 사용할 수 없습니다. 이미 연결을 설정한 경우 여전히 활성화되어 있습니다.

외부 계정은 **[!UICONTROL Administration > Application settings > External accounts]** 메뉴 아래에서 관리자가 구성할 수 있습니다.

## 외부 계정 만들기 {#creating-an-external-account}

Adobe Campaign에는 미리 정의된 외부 계정 집합이 포함되어 있습니다. 파일 전송에 사용되는 FTP 서버와 같은 외부 시스템과의 연결을 설정하기 위해 자체적인 외부 계정을 만들 수 있습니다.

외부 계정은 기술 워크플로우 또는 캠페인 워크플로우와 같은 기술 프로세스에서 사용됩니다. 워크플로우 또는 다른 애플리케이션(Adobe Target, Experience Manager 등)과의 데이터 교환에서 파일 전송을 설정할 때는 외부 계정을 선택해야 합니다.

1. **[!UICONTROL Create]** 버튼을 클릭합니다.
1. 레이블을 입력합니다. 워크플로우에서 외부 계정을 선택할 때 레이블과 ID가 사용됩니다.
1. 만들 계정 유형을 선택합니다.
1. 자격 증명, 서버 주소, 포트 번호 및 관련 키를 지정하여 계정에 대한 액세스를 구성합니다.

   필요한 정보는 일반적으로 연결 중인 서버 공급자가 제공합니다.

1. 계정을 저장합니다.

외부 계정이 만들어지고 계정 목록에 추가됩니다. 이제 워크플로우 활동 및 게재 속성에서 데이터/파일 전송 또는 라우팅 구성에 사용할 수 있습니다.

## SFTP 외부 계정 {#sftp-external-account}

외부 계정 유형에 따라 서로 다른 정보를 지정해야 합니다.

SFTP 외부 계정의 경우 다음 세부 사항을 제공합니다.

* 서버 주소. 예를 들어 **ftp.domain.com**&#x200B;입니다.
* 포트 번호. 예를 들어 **22**&#x200B;입니다.
* SFTP 서버 자격 증명: 서버에 연결하는 데 사용되는 계정 이름 및 암호입니다.

### Adobe 호스팅 SFTP 서버 권장 사항 {#adobe-hosted-sftp-server-recommendations}

ETL 목적으로 파일 및 데이터를 관리할 때 이러한 파일은 Adobe에서 제공하는 호스팅 SFTP 서버에 저장됩니다. 이 SFTP는 파일의 보관 및 삭제를 제어할 수 있는 임시 저장 공간으로 설계되었습니다.

올바르게 사용하거나 모니터링하지 않으면 이 공간은 서버에서 사용 가능한 물리적 공간을 빠르게 채워 심각한 문제를 일으킬 수 있습니다. 따라서 플랫폼에서 데이터가 손실되거나 손상될 수 있습니다.

이러한 문제를 방지하기 위해 아래 모범 사례를 따를 것을 권장합니다.

* 가능한 최소 데이터를 유지합니다.
* 암호 만료를 방지하려면 키 기반 인증을 사용합니다. 지원되는 형식은 **OpenSSH** 및 **SSH2**&#x200B;입니다. Adobe 지원 팀이 Campaign 서버에 업로드하도록 하려면 공개 키를 제공해야 합니다.
* 필요한 기간 동안에만 데이터를 유지합니다. 최대 시간 제한은 15일입니다.
* 워크플로우를 사용하여 데이터를 올바르게 삭제합니다(데이터를 사용하는 워크플로우에서 보존을 관리합니다).
* 워크플로우뿐만 아니라 SFTP 업로드에서도 일괄 처리를 사용합니다.
* 오류/예외를 처리합니다.
* 때때로 SFTP에 로그인하여 무엇이 있는지 직접 확인합니다.
* SFTP 디스크 관리는 주로 사용자의 책임입니다.

또한 SFTP 연결을 시작하려는 공개 IP는 캠페인 인스턴스의허용 목록에 추가하다에 추가해야 합니다. 인증에 사용할 공개 키허용 목록에 추가하다를 제공하는 것과 함께 [지원 티켓](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)을 통해 IP 주소를에 추가할 것을 요청할 수 있습니다.

SFTP 서버는 Campaign 컨트롤 패널에서 관리할 수 있습니다. 자세한 내용은 [Campaign 컨트롤 패널 설명서](https://docs.adobe.com/content/help/ko-KR/control-panel/using/sftp-management/about-sftp-management.html)를 참조하십시오.

>[!NOTE]
>
>Campaign 컨트롤 패널은 AWS에서 호스팅된 고객의 관리자만 사용할 수 있습니다. 

>
>[여기](https://docs.adobe.com/content/help/ko-KR/control-panel/using/faq.html#ims-org-id)에서 인스턴스가 AWS에서 호스팅되는지 확인하십시오.

## OAuth 2.0 계정 {#oauth-account}

OAuth 2.0 외부 계정의 경우 다음 세부 정보를 제공합니다.

* **Grant 유형**:**클라이언트 자격 증명**&#x200B;만 지원됩니다.
* **보안 API URL**:인증 끝점을 입력합니다.
* **OAuth 2.0 중요 자격 증명**:이 섹션은 본질적으로 민감한 자격 증명을 위한 것입니다. 자격 증명 값은 추가된 후 화면에 마스크 처리됩니다.이때 읽을 수도 편집할 수도 없습니다. 인증 끝점에 POST 본문 매개 변수 대신 HTTP 인증 헤더에 특정 자격 증명을 삽입해야 하는 경우 해당 자격 증명을 위해 헤더에 포함 옵션을 선택할 수 있습니다.
* **OAuth 2.0 비중요 자격 증명**:이 섹션은 본질적으로 중요하지 않은 자격 증명을 위한 것입니다. 자격 증명 값은 추가된 후 화면에 표시됩니다.편집할 수도 있습니다.  인증 끝점에 POST 본문 매개 변수 대신 HTTP 인증 헤더에 특정 자격 증명을 삽입해야 하는 경우 해당 자격 증명을 위해 헤더에 포함 옵션을 선택할 수 있습니다.

계정 정보를 입력한 후 **연결 테스트**&#x200B;를 클릭하여 외부 계정이 올바르게 구성되었는지 확인합니다.

![](assets/external_accounts_OAuth.png)

>[!NOTE]
>
>자격 증명 &quot;Content-Type:application/x-www-form-urlencoded&quot; 및 &quot;grant_type=client_credentials&quot;가 API 호출에 자동으로 추가됩니다.따라서 자격 증명 섹션에 추가할 필요가 없습니다.

## Amazon S3 외부 계정 {#amazon-s3-external-account}

Amazon S3 서버 필드는 다음과 같이 채워야 합니다.

```
<S3 bucket name>.s3.amazonaws.com/<s3 object path>
```

파일을 S3 암호화 모드로 저장하려면 **[!UICONTROL Keep files in S3 encrypted]** 상자를 선택합니다.

![](assets/external_accounts_2.png)

필요한 정보는 일반적으로 연결 중인 서버 공급자가 제공합니다.

엔드포인트에 연결된 **[!UICONTROL AWS Region]**&#x200B;을(를) 지정합니다. 공식 [Amazon S3 설명서](https://docs.aws.amazon.com/ko_kr/general/latest/gr/rande.html#s3_region)에서 지원되는 지역 및 서명 버전을 확인할 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Receiver server]**&#x200B;은(는) AWS 지역 없이 입력해야 하며 나중에 자동으로 URL에 추가됩니다.

### Amazon S3 계정 권장 사항 {#amazon-s3-account-recommendations}

Amazon S3 계정을 설정하는 데 도움이 되도록 다음 권장 사항을 따르는 것이 좋습니다.

* 엄격한 버킷 정책을 만들어 S3 버킷에 대한 액세스를 제한합니다. 버킷을 만드는 동안 버킷 정책을 구성할 수 있습니다. 자세한 내용은 [Amazon S3 설명서](https://docs.aws.amazon.com/ko_kr/AmazonS3/latest/dev/example-bucket-policies.html)를 참조하십시오.
* 외부 계정을 만드는 동안 **[!UICONTROL Keep files in S3 encrypted]** 상자를 선택하여 암호화가 S3 버킷에 중요한 데이터를 저장하도록 설정합니다.
* 버킷 권한을 부여하여 버킷의 개체에 액세스할 수 있는 사용자를 지정합니다. 버킷 권한에 대한 자세한 내용은 [Amazon S3 설명서](https://docs.aws.amazon.com/ko_kr/AmazonS3/latest/dev/access-control-overview.html)를 참조하십시오.

## Adobe Experience Manager 외부 계정 {#adobe-experience-manager-external-account}

Adobe Experience Manager 외부 계정은 Campaign과 Experience Manager를 통합할 때 사용됩니다.

이 통합과 관련된 프로세스 및 요구 사항은 [이 문서](../../integrating/using/get-started-campaign-integrations.md)에서 사용할 수 있습니다.

이 새 외부 계정을 설정할 때 다음 세부 사항을 제공해야 합니다.

* 서버: Adobe Experience Manager 서버의 URL을 입력합니다. 예제:

   ```
   http://aem.domain.com:4502
   ```

* AEM 계정 자격 증명: Adobe Experience Manager 인스턴스에 액세스할 계정을 사용합니다. Experience Manager에서 캠페인-원격 그룹의 계정이어야 합니다.

## Google reCAPTCHA 외부 계정 {#google-recaptcha-external-account}

>[!NOTE]
>
>Google reCAPTCHA 구성을 사용하려면 Google 계정이 필요합니다.

Google reCAPTCHA 메커니즘을 사용하면 봇으로 인한 스팸 및 악용으로부터 랜딩 페이지를 보호할 수 있습니다. 이는 고객과의 상호 작용이 필요하지 않고 사이트와의 상호 작용을 기반으로 하기 때문에 고객을 방해하지 않습니다. 사이트를 등록하려면 이 [페이지](https://www.google.com/recaptcha/admin/create)를 참조하십시오. V3 reCAPTCHA 유형을 선택해야 합니다.

Google reCAPTCHA V3을 랜딩 페이지에 추가하려면 먼저 외부 계정에서 구성해야 합니다. 랜딩 페이지에 추가하는 방법에 대한 자세한 내용은 이 [섹션](../../channels/using/configuring-landing-page.md#setting-google-recaptcha)을 참조하십시오.

Google reCAPTCHA V3 외부 계정의 경우 다음 세부 정보를 제공합니다.

* 외부 계정의 **[!UICONTROL Label]** 및 **[!UICONTROL ID]**
* **[!UICONTROL Type]**: Google reCAPTCHA
* 사용자 **[!UICONTROL Site key]** 및 **[!UICONTROL Site secret]**
* 0~1 사이의 **[!UICONTROL Threshold]**

   0.0 **[!UICONTROL Threshold]** 값은 봇일 가능성이 높고 1.0은 양호한 상호 작용일 가능성이 높습니다. 기본적으로 0.5의 임계값을 사용할 수 있습니다.

![](assets/external_accounts_3.png)

## Microsoft Azure Blob 저장 공간 외부 계정 {#microsoft-azure-external-account}

>[!NOTE]
>
>Adobe Campaign Standard에서 외부 계정을 구성하는 데 필요한 정보는 **[!UICONTROL Settings]** > **[!UICONTROL Access keys]**&#x200B;을(를) 선택하여 Azure 포털에서 확인할 수 있습니다.

Azure Blob 저장 공간 커넥터를 사용하여 **[!UICONTROL Transfer file]** 워크플로우 활동을 통해 데이터를 Adobe Campaign으로 가져오거나 내보낼 수 있습니다. 자세한 정보는 이 [섹션](../../automating/using/transfer-file.md#azure-blob-configuration-wf)을 참조하십시오.

Microsoft Azure Blob 저장 공간 외부 계정의 경우 다음 세부 정보를 제공합니다.

* 외부 계정의 **[!UICONTROL Label]** 및 **[!UICONTROL ID]**
* **[!UICONTROL Type]**: Microsoft Azure Blob 저장 공간
* 사용자 **[!UICONTROL Account name]** 및 **[!UICONTROL Account key]**. 계정 이름과 키를 찾을 수 있는 위치를 파악하려면 이 [페이지](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-account-keys-manage?tabs=azure-portal)를 참조하십시오.
* 사용자 **[!UICONTROL Endpoint suffix]**. Azure 포털 **[!UICONTROL Access keys]** 메뉴의 **[!UICONTROL Connection string]**&#x200B;에서 찾을 수 있습니다. 자세한 정보는 이 [페이지](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-keys-manage)를 참조하십시오.
* 사용자 **[!UICONTROL Container]** 이름. 두 개 이상의 컨테이너를 사용하려는 경우 외부 계정을 컨테이너만큼 만들어야 합니다.
* **[!UICONTROL Concurrency]** 옵션을 사용하면 파일 전송 속도를 세밀하게 조정할 수 있습니다.

![](assets/external_accounts_4.png)

구성이 완료되면 **[!UICONTROL Test connection]**&#x200B;을(를) 클릭하여 Adobe Campaign을 Microsoft Azure Blob 저장 공간에 연결합니다.

### Microsoft Azure Blob 저장 공간 권장 사항 {#azure-blob-recommendations}

**암호화**

Adobe Campaign은 보안 연결(HTTPS)을 사용하여 Microsoft Azure Blob 저장 공간 계정에 액세스합니다.

**계정 키**

외부 계정을 구성할 때는 Azure 포털에서 사용할 수 있는 **[!UICONTROL Account key]** 중 하나를 사용해야 합니다. 계정 키를 찾을 수 있는 위치에 대한 자세한 내용은 이 [페이지](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-account-keys-manage?tabs=azure-portal#view-access-keys-and-connection-string)를 참조하십시오.

**파일 전송 속도 최적화**

**[!UICONTROL Concurrency]** 옵션을 사용하면 파일 전송 속도를 세밀하게 조정할 수 있습니다.
파일 전송을 수행하는 데 사용할 스레드 수를 나타냅니다. 이러한 각 스레드는 Blob에서 약 1MB의 일부를 다운로드합니다. 그런 다음 디스크에 쓸 수 있도록 대기합니다. 스레드 수가 증가하면 파일 전송 중에 애플리케이션에서 사용하는 리소스에 대한 부하도 증가합니다.

파일 전송 완료 후 워크플로우 로그에서 성능 지표를 찾을 수 있습니다.

**다시 시도**

기본적으로 Azure Blob의 파일 전송은 최대 4회의 다시 시도 횟수를 갖습니다.  Azure 저장 공간 서비스가 503(서버 사용 중) 또는 500(작업 시간 초과)과 같은 오류 코드를 반환하는 경우, 저장 공간 계정의 확장성에 근접하거나 초과했음을 나타낼 수 있습니다. 이 문제는 새 계정을 사용하거나 테스트를 수행할 때 발생할 수 있습니다.

오류가 지속되면 고급 메뉴 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]** 아래에 옵션을 만들어 다시 시도 횟수를 늘릴 수 있습니다.

구현된 경우 다음과 같이 옵션을 만들어야 합니다.

```
ID:        AzureBlob_Max_Retries
Date type: Integer
Default:   <the number of retries needed>
```
