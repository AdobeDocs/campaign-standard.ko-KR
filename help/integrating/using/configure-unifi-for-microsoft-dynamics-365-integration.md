---
title: Microsoft Dynamics 365용 Unifi 통합 구성
description: Microsoft Dynamics 365용 Unifi 통합 구성 방법 살펴보기
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a1bc9d23163d12517c4501a572fc92aac6aacbc6

---



# Microsoft Dynamics 365용 Unifi 통합 구성

Microsoft Dynamics 365 - Adobe Campaign 통합을 설정하고 활성화하도록 Unifi를 구성합니다.

## 사전 요구 사항

이 아티클에서 프로비저닝 후 단계를 수행하기 전에 Campaign 및 Dynamics 365에 대한 [사후](../../integrating/using/configure-adobe-io-for-ms-dynamic.md) 제공 단계를 이미 성공적으로 완료했다고 가정합니다 [](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).  이러한 문제가 발생하지 않은 경우 이러한 단계를 따라 Campaign Standard 및 Dynamics 365 사후 프로비저닝을 완료해야 합니다.

Unifi에 연결되었거나, 사용자를 위해 만든 Unifi 계정이 있으며, 성공적으로 로그인할 수 있다고 가정합니다.  이 문제가 발생하지 않은 경우 [이 문서에](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)설명된 단계를 따르십시오.

>[!CAUTION]
>
>Unifi 구성 시 Unifi 및/또는 Adobe 컨설팅(Adobe CSM 문의)을 사용하는 것이 좋습니다.

## 캠페인 통합 구성

첫 번째 연결에서 아이콘을 클릭하여 캠페인 자격 증명을 **[!UICONTROL Adobe Campaign Standard]** 입력합니다.

이러한 자격 증명의 대부분은 Campaign Standard 구성 단계 [](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)동안 Adobe I/O 콘솔에서 만든 통합에서 가져옵니다.

>[!NOTE]
>
>보안 및 개인 정보를 보장하기 위해 이러한 구성 화면을 수정할 때 중요한 자격 증명 필드는 공백으로 표시됩니다.

1. Adobe 인증 URL의 경우 `https://ims-na1.adobelogin.com/ims/exchange/jwt`

1. 사용자 **[!UICONTROL Adobe IO Organization ID]** 및 사용자 **[!UICONTROL Adobe IO Integration ID]**&#x200B;이름을 입력합니다.

Adobe IO 조직 및 통합 ID를 얻으려면 Adobe I/O 콘솔 통합을 화면으로 이동한 후 웹 URL을 확인하십시오.

다음과 같이 표시됩니다.여기서 조직 ID와 int ID는 숫자입니다. `https://console.adobe.io/integrations/<Org ID>/<Int ID>/overview`

1. Enter your **[!UICONTROL Tenant ID]**

테넌트 ID를 받으려면 아래 단계를 따르십시오.

1. Adobe Admin [Console로](https://adminconsole.adobe.com/) 이동하여 오른쪽 상단 드롭다운 메뉴에서 IMS 조직을 선택합니다.
1. Adobe Campaign Standard 제품을 선택한 다음 Campaign Standard 인스턴스를 선택합니다(인스턴스가 두 개 이상인 경우).  그러면 제품 프로필 목록이 표시됩니다.

   제품 프로필 설명은 일반적으로 다음 형식 중 하나로 나타납니다. 여기서 `<tenantID>` 은 인스턴스의 임차인 ID입니다.

`Campaign Standard – https://<tenantID> - <ROLE>`

`Campaign Standard – <tenantID> - <ROLE>`

>[!NOTE]
>
>테넌트 ID를 식별하는 데 문제가 있는 경우 > Adobe 기술 담당자 또는 Adobe 고객 지원 센터에 문의하십시오.
>
>파트너 샌드박스 인스턴스 테넌트 ID는 일반적으로 패턴을 `https://<tenantId>`따르며, 여기서 `tenantId` 는 `tbd.campaign-sandbox.adobe.com`입니다.

1. 를 **[!UICONTROL Campaign Instance ID]**&#x200B;입력합니다.

인스턴스 ID를 받으려면 아래 단계를 따르십시오.

    1. 웹 브라우저에 &#39;https://&lt;acs-instance-url>/r/test&#39;를 입력하고 &#39;&lt;acs-instance-url>&#39;을 Campaign Standard 인스턴스의 URL로 바꿉니다.
    1. 응답에는 &#39;instance=&#39;가 포함되고 그 다음에 인스턴스 ID가 포함됩니다.

1. 캠페인 인스턴스의 영역을 선택합니다.

1. 빈 칸으로 **[!UICONTROL Base Directory]** 두시면 됩니다

1. 옵션을 **[!UICONTROL Allow as Output Destination]** 선택합니다.

매개 변수가 설정되면 클릭 **[!UICONTROL CONNECT]** 및 연결이 성공했는지 확인합니다.

그렇지 않은 경우 를 클릭하고 매개 변수를 **[!UICONTROL CLOSE]** 확인합니다.

>[!NOTE]
>
>이 단계를 완료할 수 없는 경우 Unifi [고객 서비스에](mailto:support@unifisoftware.atlassian.net)문의하십시오.

## Dynamics 365 통합 구성

Microsoft Dynamics CRM을 클릭하여 Dynamics 365 자격 증명을 구성합니다. 이러한 자격 증명의 대부분은 Microsoft Dynamics 365 구성 단계 동안 Microsoft Dynamics 365에서 만든 통합에서 제공됩니다.

>[!NOTE]
>
>보안 및 개인 정보를 보장하기 위해 이러한 구성 화면을 수정할 때 중요한 자격 증명 필드는 공백으로 표시됩니다.

1. 예를 **[!UICONTROL URL]**&#x200B;들어, &quot;.crm&quot; 앞에 &quot;.api&quot;를 삽입하도록 주의하여 Dynamics 365 인스턴스의 URL을 입력합니다(예: `https://mydynamicsinstance.api.crm.dynamics.com`).

1. 예를 **[!UICONTROL clientid]**&#x200B;들어, 앱 등록을 만들 때 생성된 응용 프로그램 ID를 Dynamics 365를 [구성할 때 사용합니다](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. 예를 **[!UICONTROL clientsecret]**&#x200B;들어 Dynamics 365를 [구성할 때 앱 등록에 클라이언트 암호를 추가할 때 생성된 클라이언트 암호를 사용하게 됩니다](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. 에 **[!UICONTROL callbackurl]**&#x200B;대해 추가를 `http://localhost:33333`참조하십시오.

1. 를 **[!UICONTROL refresh token]**&#x200B;비워 둡니다.

1. 테넌트 ID의 **[!UICONTROL경우 portal.azure.com에서 가져온 테넌트 ID를 Dynamics 365]**&#x200B;를 구성할 때 사용하십시오 [](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. 마지막으로, 에 대한 상자를 선택합니다 **[!UICONTROL Allow as Output Destination]**.

매개 변수가 입력되면 을 클릭하고 연결 상태를 **[!UICONTROL CONNECT]** 확인합니다.

그렇지 않은 경우 를 클릭하고 매개 변수를 **[!UICONTROL CLOSE]** 확인합니다.

>[!NOTE]
>
>이 단계를 완료할 수 없는 경우 Unifi [고객 서비스에](mailto:support@unifisoftware.atlassian.net)문의하십시오.

## Unifi 설정 완료

자격 증명이 설정되면 통합 설정을 완료하기 전에 몇 가지 추가 단계를 수행해야 하므로 Unifi에 알려야 합니다.  자격 증명을 설정했음을 나타내는 Unifi 연락처 정보를 제공합니다.

옵트아웃 옵션을 선택하고 완료 시 Unifi에 알려주어야 합니다(선택한 옵트아웃 옵션을 Unifi로 표시).  옵트아웃 옵션에 대한 설명은 Unifi 사용 안내서를 [참조하십시오](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn).

Unifi가 작업을 완료하면 알림 메시지를 수신하고 Unifi 인스턴스를 구성하고, 데이터 수집을 한 번 실행한 다음, 완료되면 예약을 활성화할 수 있습니다.

다양한 사용 사례에는 다음 빈도가 권장됩니다.

* 수신:15분마다
* 송신:15분마다
* 삭제:매일
* 옵트아웃:매일

>[!NOTE]
>
>기본적으로 SEND 마케팅 이벤트는 송신 작업에서 필터링됩니다.  Dynamics 365에서 SEND 마케팅 이벤트를 보려면 Unifi에서 송신 작업의 필터(5단계)를 수정해야 합니다.

Unifi에는 소유자 사용자 및 읽기 전용 애널리스트 사용자, 두 개의 별도의 역할이 있습니다. 소유자 사용자는 작업 및 일정을 수정할 수 있지만 읽기 전용 분석가는 수정할 수 없습니다.  지정된 고객 인스턴스에 대해 하나의 소유자 사용자만 있을 수 있습니다.  고객이 소유자 사용자로 지정된 개인을 변경해야 하는 경우 adobe-support@unifisoftware.com [(mailto]:(adobe-support@unifisoftware.com))를 참조하십시오.

통합 구성, 작업 세부 사항, 설정 및 모니터링이 아래 비디오에 나와 있습니다.

## Unifi Jobs

### Unifi 작업 개요

>[!VIDEO](https://video.tv.adobe.com/v/27392)

이 비디오에서는 Microsoft Dynamics 365와의 Adobe Campaign Standard 통합에 필요한 다양한 Unifi 작업에 대해 설명합니다(02:10분).

### Unifi 작업 세부 정보:수신 및 송신

>[!VIDEO](https://video.tv.adobe.com/v/27396)

이 비디오에서는 Unifi의 수신 및 송신 작업에 대해 설명합니다(04:27분).

### 운영 및 모니터링

>[!VIDEO](https://video.tv.adobe.com/v/27391)

이 비디오에서는 워크플로우 및 일정을 설명합니다(3:03분).

더 보기
* [Adobe Campaign Standard 작업 - Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Microsoft Dynamics 365 for Campaign 통합 구성](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)
* [Microsoft Dynamics 365용 Adobe IO 구성 - Campaign Standard 통합](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [Microsoft Dynamics 365 통합 기능 페이지](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html)