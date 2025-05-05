---
title: Campaign-Dynamics 통합 앱 구성
description: Campaign-Dynamics 통합 앱을 구성하는 방법 알아보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 184bc656-2107-4380-9b35-148cb4380547
source-git-commit: c701043cbba22711de1ea7ddc5266e193d771e14
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 2%

---

# 통합 앱과 시스템 연결

## 통합 앱에 자격 증명 추가

**[!UICONTROL Settings]** 화면에서 Microsoft Dynamics 365 및 Adobe API 자격 증명을 지정할 수 있습니다. Adobe Campaign SFTP 인스턴스와 관련된 설정을 구성할 수도 있습니다.

### Microsoft Dynamics 365 자격 증명

Microsoft Dynamics 365 자격 증명은 통합 응용 프로그램에 Microsoft Dynamics 365에서 데이터를 가져올 수 있는 권한을 부여합니다.  이 화면에 붙여넣을 값을 생성하려면 먼저 [Campaign 통합을 위해 Microsoft Dynamics 365 구성](../../integrating/using/d365-acs-configure-d365.md) 화면의 단계를 따라야 합니다. 아래에 설명된 입력은 이 화면을 참조합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-d365.png)

* **[!UICONTROL Client ID]**: [이 섹션](../../integrating/using/d365-acs-configure-d365.md#register-a-new-app)에서 클라이언트 ID를 참조하는 방법을 알아봅니다.

* **[!UICONTROL Client Secret]**: [이 섹션](../../integrating/using/d365-acs-configure-d365.md#generate-a-client-secret)에서 클라이언트 암호를 생성하는 방법을 알아봅니다.

* **[!UICONTROL Tenant]**: [이 섹션](../../integrating/using/d365-acs-configure-d365.md#get-the-tenant-id)에서 테넌트 ID를 찾는 방법을 알아봅니다.

* **[!UICONTROL URL]**: URL의 형식은 `https://&lt;servername&gt;.api.crm.dynamics.com/`입니다.

### Adobe API 자격 증명

Adobe Campaign 자격 증명은 [Adobe I/O](https://www.adobe.io/)을 사용하여 생성됩니다. [Adobe I/O 구성](../../integrating/using/d365-acs-configure-adobe-io.md) 화면에 방문하여 지침을 따르면 이 섹션의 입력을 작성할 수 있습니다.

* JWT 기반 인증은 더 이상 사용되지 않으므로 인증 유형을 Oauth로 선택합니다.
* 다음 이미지는 Adobe I/O과 설정 화면 입력 간의 매핑에 대해 자세히 설명합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-adobeio.png)

* *URL*: 이 값은 https\://mc.adobe.io/&lt;campaign-instance-name> 패턴에 맞게 됩니다. 통합 앱의 헤더에는 &quot;조직&quot;과 &quot;인스턴스&quot;가 모두 포함됩니다. URL의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

## Adobe Campaign SFTP 설정 {#ac-smtp-settings}

이러한 설정은 선택 사항입니다. Adobe Campaign SFTP 인스턴스를 사용하여 커넥터에서 로그를 출력할 계획이라면 이를 정의해야 합니다. 이 기능은 통합이 실행 중일 때 출력이 예상과 맞지 않는 이유를 디버깅해야 하는 경우에 유용합니다.

SFTP 서버를 설정하는 또 다른 이유는 옵트인/아웃 워크플로우를 실행할 계획이며 Adobe Campaign에서 Microsoft Dynamics 365로 **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]** 또는 **[!UICONTROL Bidirectional]**&#x200B;의 데이터 흐름이 있는 경우 입니다.

>[!IMPORTANT]
>
>SFTP 폴더에서 액세스하고 다운로드하는 정보는 사용자가 담당합니다. 정보에 개인 데이터가 포함되어 있는 경우 귀하는 해당 개인 정보 보호 법률 및 규정을 준수할 책임이 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy).
>

Microsoft Dynamics 365 통합을 위해 Campaign SFTP 설정을 정의하려면 다음 섹션에 액세스합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-sftp.png)

다음을 지정해야 합니다.

* **SFTP 호스트**: 이 필드에는 &lt;campaign-instance-name>.campaign.adobe.com이 포함됩니다. 통합 앱의 헤더에 **조직**&#x200B;과(와) **인스턴스**&#x200B;이(가) 모두 포함됩니다. URL의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

* **SFTP 사용자**: SFTP 사용자가 있는 경우 여기에 추가하십시오. 그렇지 않으면 [이 섹션](#ac-control-panel-settings)을 참조하세요. 프로세스의 일부로 사용자 이름이 표시됩니다.

* **SFTP 키**: SSH 키가 있는 경우 여기에 추가하십시오. 그렇지 않으면 [이 섹션](#ac-control-panel-settings)을 참조하세요.

* Adobe Campaign SFTP 구성에 **IP 범위**&#x200B;을(를) 포함해야 합니다. 통합에서 SFTP 끝점을 사용하려면 허용 목록에추가된여야 합니다.

* **로그를 Adobe Campaign SFTP로 내보내시겠습니까?**&#x200B;을(를) 사용하면 통합에서 로깅 정보를 SFTP 끝점으로 출력할지 여부를 확인할 수 있습니다. Adobe Campaign 또는 Microsoft Dynamics 365에 예상 정보가 표시되지 않는 경우 디버깅을 지원하는 데 사용할 수 있습니다.

## Adobe Campaign의 SFTP 설정 {#ac-control-panel-settings}

다음 섹션에서 [캠페인 Campaign 컨트롤 패널](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko)을(를) 사용하여 SFTP 관리 살펴보기:

* [SFTP 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/about-sftp-management.html?lang=ko#sftp-management)

* [SFTP 스토리지 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=ko#installing-ssh-key)

* [IP 범위 추가](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/ip-range-allow-listing.html?lang=ko#sftp-management)

* [키 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=ko#sftp-management)

* [SFTP 서버에 로그온](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/logging-into-sftp-server.html?lang=ko#sftp-management)

구성이 완료되면 개인 키로 SFTP 서버에 로그인하고 &quot;d365_loads/exports&quot; 디렉토리를 만듭니다.

Adobe Campaign Standard SFTP 서버에 대한 정보를 보려면 [이 페이지를 방문하세요](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html?lang=ko).
