---
title: Campaign Standard 관리 시작
description: 사용자 및 권한 관리, 모니터링 지침, 채널별 구성 및 애플리케이션 설정 지침 등을 살펴볼 수 있습니다.
audience: administration
content-type: reference
topic-tags: about-administrating-adobe-campaign
feature: Access Management
role: Admin
level: Experienced
exl-id: 9676b5e8-4c34-4848-8616-235e0bac5d6b
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 15%

---

# Campaign Standard 관리 시작 {#about-administrating-adobe-campaign}

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"><p><a href="#administration-menu">관리 메뉴</a></p></td>
<td><img src="assets/do-not-localize/icon_users.svg" width="60px"><p><a href="#users-security">사용자 및 보안</a></p></td>
<td><img src="assets/do-not-localize/icon_channels.svg" width="60px"><p><a href="#channels-configuration">채널 구성</a></p></td>
<td><img src="assets/do-not-localize/icon_settings.svg" width="60px"><p><a href="#application-settings">애플리케이션 설정</a></p></td></tr>
</table>

클라우드 기반 솔루션인 Adobe Campaign은 관리자에게 애플리케이션을 구성하는 다양한 방법을 제공합니다. 인프라 구성은 Adobe이 수행하지만 기능 관리자는 아래에 자세히 설명된 다양한 구성 작업을 수행할 수 있습니다.

>[!NOTE]
>
>구현 및 구성 문제에 대한 질문이나 요청이 있는 경우 Adobe 계정 담당자에게 문의하십시오.

관리 사용자는 Campaign Campaign 컨트롤 패널을 활용하여 각 인스턴스에 대한 설정을 관리하고 사용을 추적할 수도 있습니다. 자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko)를 참조하십시오.

## 관리 메뉴 {#administration-menu}

<img src="assets/do-not-localize/icon_menu.svg" width="60px">

왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭할 때 액세스 가능한 **[!UICONTROL Administration]** 메뉴를 통해 다양한 Adobe Campaign 관리 작업이 수행됩니다. 인터페이스의 이 부분은 플랫폼의 기능 관리자만이 액세스할 수 있습니다.

사용할 수 있는 다양한 메뉴는 다음과 같습니다.

* [사용자 및 보안](../../administration/using/about-access-management.md): 이 메뉴를 사용하면 플랫폼에 대한 액세스(사용자, 역할, 보안 그룹, 단위)를 관리할 수 있습니다.
* [채널](../../administration/using/about-channel-configuration.md): 이 메뉴는 유형화와 격리 관리 및 유형화와 다양한 플랫폼 채널(이메일, 모바일)에 연결된 기술 매개 변수를 다시 그룹화합니다.
* [애플리케이션 설정](../../administration/using/external-accounts.md): 이 메뉴를 사용하면 다양한 애플리케이션 요소(외부 계정, 옵션, 기술 워크플로우)를 구성할 수 있습니다.
* [개발](../../developing/using/data-model-concepts.md): 이 메뉴를 사용하면 사용자 정의 리소스를 관리하고 진단 도구에 액세스할 수 있습니다.
* [인스턴스 설정](../../administration/using/branding.md): 이 메뉴는 다양한 브랜드를 정의하고 설정(로고, 추적 관리, 랜딩 페이지에 액세스하기 위한 URL 도메인 등)을 구성하는 위치입니다.
* [배포](../../automating/using/managing-packages.md): 이 메뉴는 패키지 가져오기 및 내보내기 옵션을 다시 그룹화합니다.
* [고객 지표](../../audiences/using/active-profiles.md): Adobe Campaign에서는 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 오직 유익하며, 청구서에 직접적인 영향을 주지 않습니다.
* [개인 정보 보호 도구](../../start/using/privacy-management.md): 이 메뉴를 사용하면 GDPR 액세스 및 삭제 요청을 만들고 변경 사항을 추적할 수 있습니다.

## 사용자 및 보안 {#users-security}

<img src="assets/do-not-localize/icon_users.svg"  width="60px">

사용자에게 응용 프로그램에 액세스하고 조직 내에서 동일한 역할과 권한을 공유하는 사용자 집합인 **보안 그룹**&#x200B;을 관리하도록 초대합니다. 기본적으로 Adobe Campaign에서는 사용자 및 사용자 그룹에 할당된 단일 권한을 정의할 수 있는 **역할** 세트를 제공합니다. 역할은 **조직 단위**&#x200B;와 결합되어 사용자에게 필터링된 인터페이스 보기를 제공하고 다른 기능에 대한 액세스 권한을 정의합니다.

또한 Campaign Standard에서 보안 관련 정보를 모니터링할 수 있습니다. **[!UICONTROL Export audits]** 화면을 통해 사용자가 수행한 데이터 내보내기에 대한 정보를 검색하고, **[!UICONTROL Licenses]** 화면을 활용하여 조직 내에 설치된 모든 Campaign 라이센스와 빌드 번호, 릴리스 버전 및 계약 조건 등의 다양한 정보를 모니터링할 수 있습니다.

자세히 알아보기:

* [사용자 관리](../../administration/using/users-management.md)
* [조직 단위](../../administration/using/organizational-units.md)
* [역할 목록](../../administration/using/list-of-roles.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)
* [내보내기 로그 감사](../../administration/using/auditing-export-logs.md)
* [라이선스](../../administration/using/licenses.md)

## 채널 구성 {#channels-configuration}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

메시지를 효과적으로 보낼 수 있도록 Adobe Campaign의 모든 통신 채널을 올바르게 구성해야 합니다. **[!UICONTROL Channel]** 메뉴를 사용하면 다른 채널에 연결된 기술 매개 변수를 관리할 수 있습니다.

다양한 **email** 매개 변수를 구성합니다. 반송, 격리, 전자 메일 속성 및 라우팅 매개 변수에 대한 처리 규칙, 일반적인 규칙. **SMS** 채널에 대한 라우팅 구성 및 속성과 SMS 인코딩 및 형식을 정의합니다.

Adobe Experience Platform SDK를 사용하여 인앱 메시지 및 푸시 알림을 전송할 수 있도록 **모바일 애플리케이션**&#x200B;을 설정합니다.

자세히 알아보기:

* [채널 구성 기본 정보](../../administration/using/about-channel-configuration.md)
* [이메일 채널 구성](../../administration/using/configuring-email-channel.md)
* [SMS 채널 구성](../../administration/using/configuring-sms-channel.md)
* [모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md)

## 애플리케이션 설정 {#application-settings}

<img src="assets/do-not-localize/icon_settings.svg" width="60px">

Campaign Standard에는 요구 사항에 맞게 구성할 수 있는 다양한 애플리케이션 요소가 포함되어 있습니다.

Adobe Campaign을 외부 서버에 연결하는 데 사용되는 **외부 계정**&#x200B;을 설정합니다. Campaign Standard 대상 매핑에 액세스하고 **기술 워크플로우**&#x200B;를 사용하여 플랫폼을 모니터링합니다.

조직에 대해 하나 또는 여러 **브랜드**&#x200B;를 정의하고, 중요한 시스템 활동이 발생하는 경우 애플리케이션 내에서 **실시간 알림**&#x200B;을 보내도록 구성합니다.

자세히 알아보기:

* [Campaign Standard 설정 기본 정보](../../administration/using/about-campaign-standard-settings.md)
* [외부 계정](../../administration/using/external-accounts.md)
* [Campaign에서 타깃 매핑](../../administration/using/target-mappings-in-campaign.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [브랜딩](../../administration/using/branding.md)
* [내부 알림 보내기](../../administration/using/sending-internal-notifications.md)
