---
title: 모니터링 지침
description: 이 페이지에서는 Campaign Standard 모니터링을 위한 일반 지침을 제공합니다
audience: production
feature: Access Management
role: Admin
level: Experienced
exl-id: 5f25f2b2-ca41-4baf-ade2-42bbafb4790d
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 12%

---

# 모니터링 지침 {#monitoring-guidelines}

<table>
<tr><td><img src="assets/do-not-localize/icon_system.svg" width="60px"><p><a href="#monitoring-system">시스템 모니터링</a></p></td>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#moniroting-workflows">워크플로우 모니터링</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#monitoring-deliveries">게재 모니터링</a></p></td></tr>
</table>

Campaign Standard은 인스턴스가 정상인지 확인하고 워크플로우를 설정하고 게재를 전송할 때 발생할 수 있는 문제를 해결하기 위해 몇 가지 방법으로 인스턴스를 모니터링합니다.

## 시스템 모니터링 {#monitoring-system}

<img src="assets/do-not-localize/icon_system.svg" width="60px">

**시스템 알림**

Campaign Standard 인터페이스는 이벤트 상태, 시스템 업데이트, 필요한 작업 등 시스템에서 발생하는 상황을 지속적으로 알려줄 수 있는 알림 창을 제공합니다. [자세히 보기](../../start/using/interface-description.md#top-bar)


**기술 워크플로우**

기술 워크플로우는 서버에서 정기적으로 실행하도록 예약된 작업 또는 작업입니다. 인스턴스가 정상이고 제대로 작동하는지 확인하려면 인스턴스가 항상 작동 중인지 확인해야 합니다. [자세히 보기](../../administration/using/technical-workflows.md)

**컨트롤 패널**

이 Campaign 컨트롤 패널을 사용하면 인스턴스의 URL 권한, 서버의 빌드 버전과 같은 인스턴스 세부 정보 확인, 활성 프로필 사용 모니터링 등 여러 설정을 관리할 수 있습니다. 또한 인스턴스에 연결된 SFTP 서버의 사용 가능한 공간을 모니터링할 수 있습니다. [자세히 보기](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=ko).

>[!NOTE]
>
>컨트롤 패널은 모든 관리 사용자가 액세스할 수 있습니다. 사용자에게 관리자 권한을 부여하는 단계는 [이 페이지](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=ko#discover-control-panel)에 자세히 설명되어 있습니다.

**기술 개체**

**[!UICONTROL Diagnosis]** 메뉴는 응용 프로그램에서 생성된 다양한 기술 개체(데이터 스키마, 웹 페이지, 일괄 처리 작업 등)를 모니터링하고 분석하는 주요 도구입니다. [자세히 보기](../../developing/using/monitoring-data-model-changes.md)

**감사 내보내기**

내보내기 감사를 사용하면 워크플로우에서 업로드한 파일, 목록 내보내기, DM 메시지에서 다운로드한 파일 등 인스턴스에서 수행된 내보내기를 모니터링할 수 있습니다.
[자세히 보기](../../administration/using/auditing-export-logs.md)

**라이선스**

**[!UICONTROL Licenses]** 메뉴를 사용하여 설치된 라이선스, 빌드 버전 및 약관 동의 등 인스턴스에 대한 정보를 모니터링합니다.
[자세히 보기](../../administration/using/licenses.md)

## 워크플로우 모니터링 {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**모범 사례 및 문제 해결**

워크플로우를 사용할 때 모범 사례 및 문제 해결 지침을 따르면 성능을 개선하는 데 도움이 될 수 있습니다.
[자세히 보기](../../automating/using/best-practices-workflows.md)

**로그 및 작업**

워크플로우 로그 모니터링은 워크플로우를 분석하고 제대로 실행되고 있는지 확인하는 주요 단계입니다.
[자세히 보기](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**알림**

Campaign Standard을 사용하면 감독자에게 알림을 전송하여 워크플로우의 실행을 모니터링하고 주의가 필요한 오류가 있는지 확인할 수 있습니다.
[자세히 보기](../../automating/using/monitoring-workflow-execution.md#error-management)

## 게재 모니터링 {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**게재 가능성**

Campaign Standard은 성공적으로 배달된 메시지 수를 개선하는 데 도움이 되는 게재 기능 도구인 게재 처리량 보고서, 전송 시간 최적화, 메시지 미리 보기, 이메일 렌더링, 격리 관리 등을 제공합니다.
[자세히 보기](../../sending/using/about-deliverability.md)

**게재**

메시지가 전송되면 세부 로그를 사용하여 게재를 모니터링하고 캠페인의 성공을 측정하고 메시지 수신자의 동작을 추적할 수 있습니다.
[자세히 보기](../../sending/using/monitoring-a-delivery.md)

**게재 경고**

게재 경고 기능을 사용하면 게재 실행과 관련하여 사용자 그룹에 자동으로 전송되는 경고(전송 또는 준비 실패, 잘못된 바운스 비율, 낮은 처리량 등)를 설정할 수 있습니다.
[자세히 보기](../../sending/using/receiving-alerts-when-failures-happen.md)

**동적 보고**

동적 보고는 바운스, 수신자별로 가장 많이 본 게재, 게재 처리량 등 게재 수행 방법을 안내하는 데 도움이 되는 다양한 보고서를 제공합니다.
[자세히 보기](../../reporting/using/about-dynamic-reports.md)
