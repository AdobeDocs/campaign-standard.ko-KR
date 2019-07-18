---
title: 사용자 유형
seo-title: 사용자 유형
description: 사용자 유형
seo-description: 'Adobe Campaign 사용자는 특정 역할을 보유합니다. 주요 사용자 유형 파악 '
page-status-flag: 정품 인증 안 함
uuid: 8 C 4 CC 74 A -815 F -4815-AF 66-A 7 C 21 BC 754 F 1
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 사용자 및 보안
discoiquuid: 08 C 8712 A -0066-4 B 8 B -8471-2656 B 8 FB 23 ED
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 866567d63dd2798eb56d42d4e163e5484c9b4d68

---


# Types of users{#types-of-users}

관리자는 Admin Console에서 사용자를 관리할 수 있습니다. 그러면 사용자가 Adobe Campaign와 자동으로 동기화됩니다.

For more on this, refer to the [Admin console](https://helpx.adobe.com/enterprise/using/users.html) documentation.

To view the users in Adobe Campaign, click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Administration > Users & Security > Users]**.

To access the user management interface from Adobe Campaign, click **[!UICONTROL User administration]**.

![](assets/user_management_5.png)

Adobe Campaign를 사용하면 사용자에게 일련의 역할을 할당하여 액세스할 수 있는 인터페이스의 부분을 정의할 수 있습니다.

The specific roles and the corresponding authorizations are detailed in the following sections: [understanding roles](../../administration/using/list-of-roles.md) and [authorizations](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

이 사용자 세그멘테이션은 필수가 아니며, Adobe Campaign의 가장 일반적인 사용을 나타냅니다.

이 섹션은 Adobe Campaign 사용자의 주요 유형을 이해하는 데 도움이 됩니다. 여기에서는 사용자가 보유할 수 있는 모든 역할 (배달 시작, 내보내기, 배달 준비 등) 이 적용되지 않습니다. For more information on roles, refer to [List of roles](../../administration/using/list-of-roles.md) and [Managing groups and users](../../administration/using/managing-groups-and-users.md) pages.

Adobe Campaign의 다양한 작업이 세 가지 주요 사용자 유형 간에 어떻게 분할되는지에 중점을 둡니다.

* [기능 관리자](../../administration/using/types-of-users.md#functional-administrators): 모든 조직의 사용자 중에서 가장 전문적인 기술
* [고급 사용자](../../administration/using/types-of-users.md#advanced-users): 마케터가 배달을 전송하고 모니터링해야 하는 모든 요소를 설정합니다.
* [기본 사용자](../../administration/using/types-of-users.md#basic-users): 캠페인을 개인화, 전달 및 모니터링하는 마케터입니다.

>[!NOTE]
>
>기능 관리자는 Adobe 기술 관리자와 다릅니다. Adobe 기술 관리자는 고객이 사용할 수 없는 Adobe 내부 역할을 담당합니다. 이들은 인스턴스 프로비저닝, 호스팅, 인프라 모니터링 및 감독, 기술 문제 해결 등을 관리합니다.

**관련 항목:**

* [사용자 권한](https://helpx.adobe.com/campaign/kt/acs/using/acs-user-access-rights-feature-video-use.html) 관리 비디오
* [역할 목록](../../administration/using/list-of-roles.md)
* [승인 목록](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf)

## Functional administrators {#functional-administrators}

기능 관리자는 인터페이스의 기술 부분에 액세스할 수 있는 사용자입니다. They hold the **[!UICONTROL Administration]** role and make sure that the platform is all set up so that marketers only have to focus on delivering their campaigns.

Functional administrators are the only users who can access the **[!UICONTROL Administration]** menu, in the Adobe Campaign interface. Since these users need to access technical resources, more advanced roles should be assigned to them, such as the **[!UICONTROL Administration]** and **[!UICONTROL Datamodel]** out-of-the-box roles. These roles are combined in the **[!UICONTROL Administrators]** out-of-the-box security group. For more on this, refer to this [section](../../administration/using/list-of-roles.md).

다음은 수행할 수 있는 주요 작업입니다.

* [사용자 및 권한 관리](../../administration/using/about-access-management.md): 플랫폼 액세스 권한 관리 (사용자, 역할, 보안 그룹, 판매량)
* [다양한 채널을 구성합니다](../../administration/using/about-channel-configuration.md). 유형 및 격리 관리뿐만 아니라 다양한 플랫폼 채널을 설정할 수 있습니다.
* [일반 애플리케이션 설정을 구성합니다](../../administration/using/external-accounts.md). 다른 애플리케이션 요소 (외부 계정, 옵션, 기술 워크플로우) 를 구성합니다.
* [새로운 기능을 개발하여 즉시 사용 가능한 기능](../../developing/using/data-model-concepts.md)향상: 맞춤형 리소스를 관리하고 진단 툴을 이용할 수 있습니다.
* [인스턴스 매개 변수를 설정합니다](../../administration/using/branding.md). 다른 브랜드를 정의하고 설정 (로고, 추적 관리, 랜딩 페이지 액세스에 대한 URL 도메인 등) 를 구성합니다.
* [데이터 패키지 내보내기 및 가져오기](../../automating/using/managing-packages.md): 구조화된 XML 파일을 통해 다른 Adobe Campaign 인스턴스 간의 리소스를 교환합니다.
* [로그를](../../automating/using/exporting-logs.md) 내보내고 가져오기 템플릿을 [정의할](../../automating/using/defining-import-templates.md)수 있습니다.

## Advanced users {#advanced-users}

고급 사용자는 Adobe Campaign에서 기술 사용 사례를 수행하는 마케팅 사용자입니다. 마케터는 마케터가 전달을 전송하고 모니터링하는 데 사용하는 모든 요소를 미리 구성합니다.

이 유형의 사용자는 기능적인 관리자보다 더 일반적인 역할을 필요로 하지만 여전히 일부 기술 작업을 수행할 수 있어야 합니다. To do so, they should be assigned, for example, the **[!UICONTROL Export]**, **[!UICONTROL Generic import]** or **[!UICONTROL Workflow]** out-of-the-box roles. For more on this, refer to this [section](../../administration/using/list-of-roles.md).

다음은 수행할 수 있는 주요 작업입니다.

* [복잡한 데이터 관리 워크플로우 구축 및 실행](../../automating/using/about-data-management-activities.md): 데이터를 가져오거나 꾸미거나 변형하여 데이터베이스를 피드에 제공하거나 외부 파일에서 필요한 데이터를 내보내 고유한 툴로 처리할 수 있습니다.
* [템플릿 관리](../../start/using/about-templates.md): 템플릿을 관리하여 필요에 따라 마케팅 활동의 특정 매개 변수를 미리 구성할 수 있습니다.
* [쿼리](../../automating/using/editing-queries.md#about-query-editor) 작성 및 고객 [관리](../../audiences/using/about-audiences.md): 쿼리를 사용하거나 전용 워크플로우를 사용하여 자동으로 대상을 만듭니다.
* [고급 표현식 편집 수행](../../automating/using/editing-queries.md#about-query-editor): 고급 함수를 사용하여 날짜, 문자열, 숫자 필드, 정렬 등과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작합니다.
* [목록을](../../automating/using/exporting-lists.md) 내보내고 기존 가져오기 템플릿을 사용하여 데이터를 [가져올](../../automating/using/importing-data-with-import-templates.md)수 있습니다.

## Basic users {#basic-users}

기능 관리자 및 고급 사용자 덕분에 마케터는 기술 구성에 대해 걱정할 필요 없이 캠페인을 개인화, 전달 및 모니터링할 수 있습니다. To do so, they should be assigned, for example, the **[!UICONTROL Prepare deliveries]**, **[!UICONTROL Workflow]** and **[!UICONTROL Start deliveries]** out-of-the-box roles. These roles are combined in the **[!UICONTROL Standard Users]** out-of-the-box security group. For more on this, refer to this [section](../../administration/using/list-of-roles.md).

다음은 수행할 수 있는 주요 작업입니다.

* [프로그램 및 캠페인 관리](../../start/using/programs-and-campaigns.md): 다양한 유형의 활동 (이메일, SMS 메시지, 푸시 알림, 워크플로우, 랜딩 페이지) 를 포함하는 마케팅 캠페인을 만듭니다.
* [프로필 관리](../../audiences/using/about-profiles.md) 및 [프로필 테스트](../../sending/using/managing-test-profiles-and-sending-proofs.md): 배달에 의해 타깃팅될 식별된 테스트 받는 사람을 관리합니다. 이름, 성, 연락처 정보, 구독, 이메일 등과 같은 정보를 추가합니다.
* [메시지 작성 및 보내기](../../sending/using/confirming-the-send.md): 메시지를 만들고, 대상자를 선택하고, 메시지 컨텐츠와 개인화 요소를 정의하고, 증거 자료를 보내고, 최종 메시지를 사용자에게 보냅니다.
* [랜딩 페이지 만들기 및 게시](../../channels/using/about-landing-pages.md): 가입 또는 가입 해지 양식에 대한 클라이언트 제공하려는 서비스 세트를 만들고 관리합니다.
* [캠페인 워크플로우 만들기 및 실행](../../automating/using/building-a-workflow.md): 워크플로우를 사용하여 캠페인 프로세스를 자동화합니다.
* Monitor your marketing activities through the [available reports](../../reporting/using/defining-the-report-period.md).

