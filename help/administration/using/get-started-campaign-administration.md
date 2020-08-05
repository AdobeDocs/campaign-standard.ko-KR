---
title: Campaign Standard 관리 시작
description: Adobe Campaign은 완벽한 관리 툴을 제공합니다. 사용자를 관리하고 채널을 구성하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 64c34729-5c98-4db0-9131-af6dd0e78fb4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: about-administrating-adobe-campaign
discoiquuid: 5587530a-2308-4be1-9f56-19eeb7a924d5
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ad110413fd325894405b421999baccda2c7cef4a
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 14%

---


# Campaign Standard 관리 시작 {#about-administrating-adobe-campaign}

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"><p><a href="#administration-menu">관리 메뉴</a></p></td>
<td><img src="assets/do-not-localize/icon_users.svg" width="60px"><p><a href="#users-security">사용자 및 보안</a></p></td>
<td><img src="assets/do-not-localize/icon_channels.svg" width="60px"><p><a href="#channels-configuration">채널 구성</a></p></td>
<td><img src="assets/do-not-localize/icon_settings.svg" width="60px"><p><a href="#application-settings">애플리케이션 설정</a></p></td></tr>
</table>

클라우드 기반의 솔루션으로, Adobe Experience Manager는 관리자에게 애플리케이션을 구성하는 다양한 방법을 제공합니다. 인프라 구성은 Adobe에서 수행되지만 기능 관리자는 아래 설명된 다양한 구성 작업을 수행할 수 있습니다.

>[!NOTE]
>
>구현 및 구성 문제에 대한 질문이나 요청이 있는 경우 Adobe 계정 관리자에게 문의하십시오.

## 관리 메뉴 {#administration-menu}

<img src="assets/do-not-localize/icon_menu.svg" width="60px">

왼쪽 상단의 Adobe Campaign 로고를 클릭하면 액세스할 수 있는 **[!UICONTROL Administration]** 메뉴를 통해 다양한 Adobe Campaign 관리 작업을 수행할 수 있습니다. 인터페이스의 이 부분은 플랫폼의 기능 관리자만 액세스할 수 있습니다.

사용할 수 있는 다양한 메뉴는 다음과 같습니다.

* [사용자 및 보안](../../administration/using/about-access-management.md): 이 메뉴를 사용하면 플랫폼(사용자, 역할, 보안 그룹, 단위)에 대한 액세스를 관리할 수 있습니다.
* [채널](../../administration/using/about-channel-configuration.md): 이 메뉴는 유형 및 격리 관리뿐만 아니라 다양한 플랫폼 채널(이메일, SMS)에 연결된 기술 매개 변수를 다시 그룹화합니다.
* [애플리케이션 설정](../../administration/using/external-accounts.md): 이 메뉴를 사용하면 다른 애플리케이션 요소(외부 계정, 옵션, 기술 워크플로우)를 구성할 수 있습니다.
* [개발](../../developing/using/data-model-concepts.md): 이 메뉴를 사용하면 사용자 지정 리소스를 관리하고 진단 도구에 액세스할 수 있습니다.
* [인스턴스 설정](../../administration/using/branding.md): 이 메뉴에서는 다른 브랜드를 정의하고 해당 설정(로고, 추적 관리, 랜딩 페이지에 액세스하기 위한 URL 도메인 등)을 구성합니다.
* [배포](../../automating/using/managing-packages.md): 이 메뉴는 패키지 가져오기 및 내보내기 옵션을 다시 그룹화합니다.
* [고객 지표](../../audiences/using/active-profiles.md): Adobe Campaign은 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 단지 유익할 뿐, 대금 청구에는 직접적인 영향을 주지 않습니다.
* [개인 정보 보호 도구](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html): 이 메뉴를 사용하면 GDPR 액세스를 만들고 요청을 삭제하고 진행 상황을 추적할 수 있습니다.

## 사용자 및 보안 {#users-security}

<img src="assets/do-not-localize/icon_users.svg"  width="60px">

조직 내에서 동일한 역할과 권한을 공유하는 사용자 집합인 응용 프로그램에 액세스하고 **보안 그룹을**&#x200B;관리하도록 사용자를 초대합니다. By default, Adobe Campaign offers a set of **roles** which allows you to define unitary authorizations assigned to users and user groups. Combined with **organizational units**, roles give users a filtered view of the interface and define their access to the different features.

또한 캠페인 표준을 사용하여 보안 관련 정보를 모니터링할 수 있습니다. 화면을 통해 사용자가 수행하는 데이터 내보내기 관련 정보를 검색하고, 화면 **[!UICONTROL Export audits]** **[!UICONTROL Licenses]** 을 활용하여 조직 내에 설치된 모든 Campaign 라이선스와 빌드 번호, 릴리스 버전 및 계약 조건 등의 다양한 정보를 모니터링할 수 있습니다.

자세한 내용:

* [사용자 관리](../../administration/using/users-management.md)
* [조직 단위](../../administration/using/organizational-units.md)
* [역할 목록](../../administration/using/list-of-roles.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)
* [내보내기 로그 감사](../../administration/using/auditing-export-logs.md)
* [라이선스](../../administration/using/licenses.md)

## 채널 구성 {#channels-configuration}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

메시지를 효과적으로 보낼 수 있도록 Adobe Campaign의 모든 통신 채널을 올바르게 구성해야 합니다. 메뉴를 사용하면 여러 채널에 연결된 기술 매개 변수를 관리할 수 있습니다. **[!UICONTROL Channel]**

다양한 **이메일** 매개 변수 구성: 바운스, 검역소, 이메일 속성 및 라우팅 매개 변수에 대한 처리 규칙, typoly 규칙. SMS **채널과 SMS** 인코딩 및 포맷에 대한 라우팅 구성 및 속성을 정의합니다.

Adobe Experience Platform SDK를 사용하여 인앱 메시지 및 푸시 알림을 전송할 수 있도록 **모바일 애플리케이션을** 설정하고 이벤트를 만들고 설정하여 **트랜잭션 메시지를** 구성할 수 있습니다.

자세한 내용:

* [채널 구성 기본 정보](../../administration/using/about-channel-configuration.md)
* [이메일 채널 구성](../../administration/using/configuring-email-channel.md)
* [SMS 채널 구성](../../administration/using/configuring-sms-channel.md)
* [모바일 애플리케이션 구성](../../administration/using/configuring-a-mobile-application.md)
* [트랜잭션 메시지 구성](../../administration/using/configuring-transactional-messaging.md)

## 애플리케이션 설정 {#application-settings}

<img src="assets/do-not-localize/icon_settings.svg" width="60px">

Campaign Standard에는 요구 사항에 맞게 구성할 수 있는 다양한 애플리케이션 요소가 포함되어 있습니다.

외부 서버에 Adobe Campaign을 연결하는 데 사용되는 **외부 계정을**&#x200B;설정합니다. Campaign Standard 대상 매핑에 액세스하고 **기술 워크플로우를 통해 플랫폼을 모니터링합니다**.

조직에서 사용할 하나 또는 여러 **브랜드** 를 정의하고, 중요한 시스템 활동 시 애플리케이션 내에서 **실시간 알림** 전송을 구성할 수 있습니다.

자세한 내용:

* [Campaign Standard 설정 기본 정보](../../administration/using/about-campaign-standard-settings.md)
* [외부 계정](../../administration/using/external-accounts.md)
* [Campaign에서 Target 매핑](../../administration/using/target-mappings-in-campaign.md)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [브랜딩](../../administration/using/branding.md)
* [내부 알림 보내기](../../administration/using/sending-internal-notifications.md)

## 추가 자료

* [사용자 액세스 권한 관리(비디오)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/managing-user-access-rights.html)
* [Campaign 컨트롤 패널 설명서](https://docs.adobe.com/content/help/ko-KR/control-panel/using/control-panel-home.html)
