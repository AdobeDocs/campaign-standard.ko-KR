---
title: Campaign Standard 관리 시작
description: 사용자 및 권한 관리, 모니터링 지침, 채널별 구성 및 애플리케이션 설정 지침에 대해 자세히 알아보십시오.
audience: administration
feature: Access Management
role: Admin
level: Experienced
exl-id: 9676b5e8-4c34-4848-8616-235e0bac5d6b
source-git-commit: bfba6b156d020e8d2656239e713d2d24625bda54
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 12%

---

# Campaign Standard 관리 시작 {#about-administrating-adobe-campaign}

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"><p><a href="#administration-menu">관리 메뉴</a></p></td>
<td><img src="assets/do-not-localize/icon_users.svg" width="60px"><p><a href="#users-security">사용자 및 보안</a></p></td>
<td><img src="assets/do-not-localize/icon_channels.svg" width="60px"><p><a href="#channels-configuration">채널 구성</a></p></td>
<td><img src="assets/do-not-localize/icon_settings.svg" width="60px"><p><a href="#application-settings">응용 프로그램 설정</a></p></td></tr>
</table>

Adobe Campaign은 클라우드 기반 솔루션으로서, 관리자에게 애플리케이션을 구성하는 다양한 방법을 제공합니다. 인프라 구성은 Adobe이 수행하지만 기능 관리자는 아래에 설명된 다양한 구성 작업을 수행할 수 있습니다.

>[!NOTE]
>
>구현 및 구성 문제에 대한 질문이나 요청이 있는 경우 Adobe 계정 담당자에게 문의하십시오.

관리 사용자는 Campaign Campaign 컨트롤 패널을 활용하여 각 인스턴스에 대한 설정을 관리하고 사용을 추적할 수도 있습니다. 자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko)를 참조하십시오.

## 관리 메뉴 {#administration-menu}

<img src="assets/do-not-localize/icon_menu.svg" width="60px">

다양한 Adobe Campaign 관리 작업은 **[!UICONTROL Administration]** 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭하면 메뉴에 액세스할 수 있습니다. 인터페이스의 이 부분은 플랫폼의 기능 관리자만 액세스할 수 있습니다.

사용할 수 있는 다양한 메뉴는 다음과 같습니다.

* [사용자 및 보안](../../administration/using/about-access-management.md): 이 메뉴를 사용하면 플랫폼에 대한 액세스(사용자, 역할, 보안 그룹, 단위)를 관리할 수 있습니다.
* [채널](../../administration/using/about-channel-configuration.md): 이 메뉴는 유형화와 격리 관리 및 다양한 플랫폼 채널(이메일, 모바일)에 연결된 기술 매개 변수를 다시 그룹화합니다.
* [응용 프로그램 설정](../../administration/using/external-accounts.md): 이 메뉴를 사용하면 다양한 애플리케이션 요소(외부 계정, 옵션, 기술 워크플로우)를 구성할 수 있습니다.
* [개발](../../developing/using/data-model-concepts.md): 이 메뉴를 사용하면 사용자 지정 리소스를 관리하고 진단 도구에 액세스할 수 있습니다.
* [인스턴스 설정](../../administration/using/branding.md): 이 메뉴를 통해 다양한 브랜드를 정의하고 설정(로고, 추적 관리, 랜딩 페이지에 액세스하기 위한 URL 도메인 등)을 구성할 수 있습니다.
* [배포](../../automating/using/managing-packages.md): 이 메뉴는 패키지 가져오기 및 내보내기 옵션을 다시 그룹화합니다.
* [고객 지표](../../audiences/using/active-profiles.md): Adobe Campaign은 활성 프로필의 수를 표시하는 보고서를 제공합니다. 이 보고서는 정보용일 뿐이며, 청구에 직접적인 영향을 주지 않습니다.
* [개인 정보 보호 도구](../../start/using/privacy-management.md): 이 메뉴를 사용하면 GDPR 액세스 및 삭제 요청을 만들고 진행 상황을 추적할 수 있습니다.

## 사용자 및 보안 {#users-security}

<img src="assets/do-not-localize/icon_users.svg"  width="60px">

애플리케이션에 액세스하고 관리하도록 사용자 초대 **보안 그룹**: 조직 내에서 동일한 역할과 권한을 공유하는 사용자의 집합입니다. 기본적으로 Adobe Campaign은 **역할** 사용자 및 사용자 그룹에 할당된 단일 권한을 정의할 수 있습니다. 결합 대상 **조직 단위**, 역할은 사용자에게 인터페이스의 필터링된 보기를 제공하고 다양한 기능에 대한 액세스를 정의합니다.

Campaign standard를 사용하면 보안 관련 정보를 모니터링할 수도 있습니다. 를 통해 사용자가 수행한 데이터 내보내기에 대한 정보를 검색할 수 있습니다. **[!UICONTROL Export audits]** 스크린 및 활용 **[!UICONTROL Licenses]** 조직 내에 설치된 모든 Campaign 라이선스와 빌드 번호, 릴리스 버전 및 계약 조건 등의 다양한 정보를 모니터링하는 화면입니다.

자세한 내용:

* [사용자 관리](../../administration/using/users-management.md)
* [조직 단위](../../administration/using/organizational-units.md)
* [역할 목록](../../administration/using/list-of-roles.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)
* [내보내기 로그 감사](../../administration/using/auditing-export-logs.md)
* [라이선스](../../administration/using/licenses.md)

## 채널 구성 {#channels-configuration}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

메시지를 효과적으로 보낼 수 있도록 Adobe Campaign의 모든 통신 채널을 올바르게 구성해야 합니다. **[!UICONTROL Channel]**  메뉴를 사용하면 다양한 채널에 연결된 기술 매개 변수를 관리할 수 있습니다.

다양한 구성 **이메일** 매개 변수: 바운스, 격리, 이메일 속성 및 라우팅 매개 변수에 대한 처리 규칙, typoly 규칙. 다음에 대한 라우팅 구성 및 속성 정의 **SMS** 채널, SMS 인코딩 및 형식을 지원합니다.

설정 **모바일 애플리케이션** Adobe Experience Platform SDK를 사용하여 인앱 메시지 및 푸시 알림을 전송할 수 있습니다.

자세한 내용:

* [채널 구성 기본 정보](../../administration/using/about-channel-configuration.md)
* [이메일 채널 구성](../../administration/using/configuring-email-channel.md)
* [SMS 채널 구성](../../administration/using/configuring-sms-channel.md)
* [모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md)

## 응용 프로그램 설정 {#application-settings}

<img src="assets/do-not-localize/icon_settings.svg" width="60px">

Campaign Standard은 요구 사항에 맞게 구성할 수 있는 다양한 애플리케이션 요소와 함께 제공됩니다.

설정 **외부 계정**: Adobe Campaign을 외부 서버에 연결하는 데 사용됩니다. Campaign Standard 대상 매핑에 액세스하고 다음을 사용하여 플랫폼 모니터링 **기술 워크플로우**.

하나 또는 여러 개 정의 **브랜드** (으)로 이메일을 보내십시오. **실시간 알림** 중요한 시스템 활동의 경우 애플리케이션 내에서.

자세한 내용:

* [Campaign Standard 설정 기본 정보](../../administration/using/about-campaign-standard-settings.md)
* [외부 계정](../../administration/using/external-accounts.md)
* [Campaign에서 타깃 매핑](../../administration/using/target-mappings-in-campaign.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [브랜딩](../../administration/using/branding.md)
* [내부 알림 보내기](../../administration/using/sending-internal-notifications.md)
