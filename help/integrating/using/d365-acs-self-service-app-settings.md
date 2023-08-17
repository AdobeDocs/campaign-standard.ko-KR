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
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 4%

---

# 통합 앱과 시스템 연결

## 통합 앱에 자격 증명 추가

다음 **[!UICONTROL Settings]** 화면에서 Microsoft Dynamics 365 및 Adobe API 자격 증명을 지정할 수 있습니다. Adobe Campaign SFTP 인스턴스와 관련된 설정을 구성할 수도 있습니다.

### Microsoft Dynamics 365 자격 증명

Microsoft Dynamics 365 자격 증명은 통합 응용 프로그램에 Microsoft Dynamics 365에서 데이터를 가져올 수 있는 권한을 부여합니다.  먼저 화면의 단계를 따라야 합니다 [Campaign 통합을 위해 Microsoft Dynamics 365 구성](../../integrating/using/d365-acs-configure-d365.md) 이 화면에 붙여넣을 값을 생성하기 위해 아래에 설명된 입력은 이 화면을 참조합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-d365.png)

* **[!UICONTROL Client ID]**: 에서 클라이언트 ID를 참조하는 방법 알아보기 [이 섹션](../../integrating/using/d365-acs-configure-d365.md#register-a-new-app)

* **[!UICONTROL Client Secret]**: 클라이언트 암호를 생성하는 방법 알아보기 [이 섹션](../../integrating/using/d365-acs-configure-d365.md#generate-a-client-secret)

* **[!UICONTROL Tenant]**: 테넌트 ID를 찾는 방법 알아보기 [이 섹션](../../integrating/using/d365-acs-configure-d365.md#get-the-tenant-id)

* **[!UICONTROL URL]**: URL의 형식은 다음과 같습니다 `https://&lt;servername&gt;.api.crm.dynamics.com/`

### Adobe API 자격 증명

Adobe Campaign 자격 증명은 다음을 사용하여 생성됩니다 [Adobe I/O](https://www.adobe.io/). 화면을 방문해야 합니다. [구성 Adobe I/O](../../integrating/using/d365-acs-configure-adobe-io.md) 이 섹션의 입력을 작성하기 전에 지침을 따르십시오.

다음 이미지는 Adobe I/O과 설정 화면 입력 간의 매핑에 대해 자세히 설명합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-adobeio.png)

* *개인 키*: &quot;공개/비공개 키 쌍 생성&quot; 버튼을 클릭하여 이를 정의하는 프로세스가 시작됩니다. 이렇게 하면 다운로드해야 하는 zip 파일이 생성됩니다. 다운로드하고 나면 파일의 압축을 해제하면 certificate_pub.crt 및 private.key라는 두 개의 파일이 생성됩니다. private.key를 안전한 곳에 보관하고 공유하지 마십시오. 텍스트 편집기에서 private.key 파일을 엽니다. 텍스트 편집기에서 전체 값을 복사합니다(PC에서는 ctrl-A를 누른 다음 ctrl-C를 누르거나 Mac에서는 cmd-A를 누른 다음 cmd-C). 여기에는 전체가 &quot;BEGIN PRIVATE KEY&quot; 및 &quot;END PRIVATE KEY&quot;로 된 줄이 포함되어야 합니다. 여러 줄로 된 이 전체 텍스트를 설정 화면의 &quot;개인 키&quot; 입력에 붙여넣습니다.

* *URL*: 이 값은 https\://mc.adobe.io/ 패턴에 맞습니다.&lt;campaign-instance-name>. 통합 앱의 헤더에는 &quot;조직&quot;과 &quot;인스턴스&quot;가 모두 포함됩니다. URL의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

## Adobe Campaign SFTP 설정 {#ac-smtp-settings}

이러한 설정은 선택 사항입니다. Adobe Campaign SFTP 인스턴스를 사용하여 커넥터에서 로그를 출력할 계획이라면 이를 정의해야 합니다. 이 기능은 통합이 실행 중일 때 출력이 예상과 맞지 않는 이유를 디버깅해야 하는 경우에 유용합니다.

SFTP 서버를 설정하는 다른 이유는 옵트인/아웃 워크플로우를 실행할 계획이고 Adobe Campaign에서 Microsoft Dynamics 365로 데이터 흐름이 있는 경우 중 하나일 수 있습니다 **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]** 또는 **[!UICONTROL Bidirectional]**.

>[!IMPORTANT]
>
>SFTP 폴더에서 액세스하고 다운로드하는 정보는 사용자가 담당합니다. 정보에 개인 데이터가 포함되어 있는 경우 귀하는 해당 개인 정보 보호 법률 및 규정을 준수할 책임이 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy)
>

Microsoft Dynamics 365 통합을 위해 Campaign SFTP 설정을 정의하려면 다음 섹션에 액세스합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-sftp.png)

다음을 지정해야 합니다.

* **SFTP 호스트**: 이 필드에는 &lt;campaign-instance-name>.campaign.adobe.com입니다. 통합 앱의 헤더에는 **조직** 및 **인스턴스**. URL의 &quot;campaign-instance-name&quot; 부분은 이 인스턴스 값에 있는 이름일 뿐입니다.

* **SFTP 사용자**: SFTP 사용자가 있는 경우 여기에 추가하십시오. Else는 다음을 참조하십시오. [이 섹션](#ac-control-panel-settings). 프로세스의 일부로 사용자 이름이 표시됩니다.

* **SFTP 키**: SSH 키가 있는 경우 여기에 추가합니다. Else는 다음을 참조하십시오. [이 섹션](#ac-control-panel-settings).

* 다음 **IP 범위** Adobe Campaign SFTP 구성에 포함되어야 합니다. 통합에서 SFTP 끝점을 사용하려면 허용 목록에추가된여야 합니다.

* 다음 **로그를 Adobe Campaign SFTP로 내보내시겠습니까?** 통합에서 로깅 정보를 SFTP 끝점으로 출력할지 결정할 수 있습니다. Adobe Campaign 또는 Microsoft Dynamics 365에 예상 정보가 표시되지 않는 경우 디버깅을 지원하는 데 사용할 수 있습니다.

## Adobe Campaign의 SFTP 설정 {#ac-control-panel-settings}

다음을 통해 SFTP 관리 살펴보기 [캠페인 Campaign 컨트롤 패널](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko) 다음 섹션에서:

* [SFTP 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/about-sftp-management.html?lang=ko#sftp-management)

* [SFTP 스토리지 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html#installing-ssh-key)

* [IP 범위 추가](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/ip-range-allow-listing.html#sftp-management)

* [키 관리](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html#sftp-management)

* [SFTP 서버에 로그온](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/logging-into-sftp-server.html#sftp-management)

구성이 완료되면 개인 키로 SFTP 서버에 로그인하고 &quot;d365_loads/exports&quot; 디렉토리를 만듭니다.

[이 페이지 방문](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html?lang=ko) Adobe Campaign Standard SFTP 서버에 대한 정보입니다.
