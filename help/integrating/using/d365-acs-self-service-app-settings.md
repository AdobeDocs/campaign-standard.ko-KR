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
source-git-commit: f75df49e7957437df72c814aa9055d34770f22d6
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 4%

---

# 통합 앱과 시스템 연결

## 통합 앱에 자격 증명 추가

다음 **[!UICONTROL Settings]** 화면에서 Microsoft Dynamics 365 및 Adobe API 자격 증명을 지정할 수 있습니다. Adobe Campaign SFTP 인스턴스와 관련된 설정을 구성할 수도 있습니다.

### Microsoft Dynamics 365 자격 증명

Microsoft Dynamics 365 자격 증명을 사용하면 통합 응용 프로그램에 Microsoft Dynamics 365에서 데이터를 가져올 수 있는 권한을 부여합니다.  먼저 화면의 단계를 따라야 합니다 [Campaign 통합을 위해 Microsoft Dynamics 365 구성](../../integrating/using/d365-acs-configure-d365.md) 를 입력하여 이 화면에 붙여넣을 값을 생성합니다. 아래 설명된 입력은 이 화면을 참조합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-d365.png)

* **[!UICONTROL Client ID]**: 에서 클라이언트 ID를 참조하는 방법 알아보기 [이 섹션](../../integrating/using/d365-acs-configure-d365.md#register-a-new-app)

* **[!UICONTROL Client Secret]**: 에서 클라이언트 암호를 생성하는 방법을 알아봅니다. [이 섹션](../../integrating/using/d365-acs-configure-d365.md#generate-a-client-secret)

* **[!UICONTROL Tenant]**: 에서 테넌트 ID를 찾는 방법을 알아봅니다. [이 섹션](../../integrating/using/d365-acs-configure-d365.md#get-the-tenant-id)

* **[!UICONTROL URL]**: URL은 형식을 갖습니다 `https://&lt;servername&gt;.api.crm.dynamics.com/`

### Adobe API 자격 증명

Adobe Campaign 자격 증명은 [Adobe I/O](https://www.adobe.io/). 화면을 방문해야 합니다 [Adobe I/O 구성](../../integrating/using/d365-acs-configure-adobe-io.md) 그리고 이 섹션의 입력을 입력하기 전에 여기 지침을 따르십시오.

다음 이미지는 Adobe I/O과 설정 화면 입력 간의 매핑에 대해 자세히 설명합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-adobeio.png)

* *개인 키*: 이 프로세스를 정의하는 프로세스는 &quot;공용/개인 키 쌍 생성&quot; 단추를 클릭하여 시작합니다. 다운로드해야 하는 zip 파일이 만들어집니다. 이 파일을 다운로드하면 파일의 압축을 해제하여 certificate_pub.crt 파일과 private.key 라는 두 파일이 생성됩니다. private.key를 안전한 위치에 두고 공유하지 마십시오. 텍스트 편집기에서 private.key 파일을 엽니다. 텍스트 편집기에서 전체 값을 복사합니다(PC에서는 ctrl-A, Mac에서는 Ctrl-C, Cmd-A 및 Cmd-C). 여기에는 &quot;개인 키 시작&quot; 및 &quot;개인 키 종료&quot;가 포함된 줄이 전체적으로 포함되어야 합니다. 전체 여러 줄 텍스트를 설정 화면의 &quot;개인 키&quot; 입력에 붙여넣습니다.

* *URL*: 이 값은 https\:///mc.adobe.io/ 패턴에 맞게 됩니다.&lt;campaign-instance-name>. 통합 앱의 헤더에 &quot;조직&quot;과 &quot;인스턴스&quot;가 모두 포함됩니다. url의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

## Adobe Campaign SFTP 설정 {#ac-smtp-settings}

이러한 설정은 선택 사항입니다. Adobe Campaign SFTP 인스턴스를 사용하여 커넥터에서 로그를 출력하려는 경우 커넥터를 정의해야 합니다. 이 기능은 통합이 실행될 때 문제가 발생하고 출력이 예상과 일치하지 않는 이유를 디버깅해야 하는 경우에 유용합니다.

SFTP 서버를 설정하는 다른 이유는 옵트인/아웃 워크플로우를 실행할 계획이고 Adobe Campaign에서 Microsoft Dynamics 365로의 데이터 흐름이 있는 경우입니다 **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]** 또는 **[!UICONTROL Bidirectional]**.

>[!IMPORTANT]
>
>SFTP 폴더에서 액세스 및 다운로드하는 정보는 사용자가 책임집니다. 정보에 개인 데이터가 포함되어 있는 경우 해당 개인 정보 보호 법 및 규정을 준수할 책임이 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy)

Microsoft Dynamics 365 통합에 대한 Campaign SFTP 설정을 정의하려면 다음 섹션에 액세스합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-sftp.png)

다음을 지정해야 합니다.

* **SFTP 호스트**: 이 필드에는 다음 내용이 포함됩니다 &lt;campaign-instance-name>.campaign.adobe.com 통합 앱의 헤더에 **조직** 및 **인스턴스**. url의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

* **SFTP 사용자**: SFTP 사용자가 있는 경우 여기에 추가합니다. 그렇지 않으면 [이 섹션](#ac-control-panel-settings). 프로세스의 일부로 사용자 이름이 표시됩니다.

* **SFTP 키**: SSH 키가 있는 경우 여기에 추가합니다. 그렇지 않으면 [이 섹션](#ac-control-panel-settings).

* 다음 **IP 범위** 은 Adobe Campaign SFTP 구성에 포함되어야 합니다. 통합에서 SFTP 종단점을 사용하려면 이러한 엔드포인트를 허용 목록에추가된으로 사용해야 합니다.

* 다음 **Adobe Campaign SFTP로 로그를 내보내시겠습니까?** 통합에서 SFTP 종단점에 로깅 정보를 출력할지 여부를 결정할 수 있습니다. Adobe Campaign 또는 Microsoft Dynamics 365에서 예상한 정보가 표시되지 않는 경우 디버깅에 도움이 될 수 있습니다.

## Adobe Campaign의 SFTP 설정 {#ac-control-panel-settings}

을 사용하여 SFTP 관리 살펴보기 [캠페인 Campaign 컨트롤 패널](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko) 다음 섹션에 있습니다.

* [SFTP 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/about-sftp-management.html?lang=ko#sftp-management)

* [SFTP 스토리지 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=en#installing-ssh-key)

* [IP 범위 추가](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/ip-range-allow-listing.html?lang=en#sftp-management)

* [키 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=en#sftp-management)

* [SFTP 서버에 로그온](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/logging-into-sftp-server.html?lang=en#sftp-management)

구성이 완료되면 개인 키를 사용하여 SFTP 서버에 로그인하고 &quot;d365_loads/exports&quot; 디렉토리를 만듭니다.

[이 페이지 방문](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html?lang=en#sftp-management) Adobe Campaign Standard SFTP 서버에 대한 정보입니다.
