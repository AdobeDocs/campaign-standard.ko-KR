---
title: 모니터링 지침
description: 이 섹션에서는 Campaign Standard 모니터링에 대한 일반적인 지침을 제공합니다.
page-status-flag: never-activated
uuid: cf0d782d-47bf-40ae-ab6f-d1d47fa15792
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
audience: production
content-type: reference
topic-tags: introduction
discoiquuid: 8b33e6af-15c3-4b30-8ad6-d76a1f33be21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b4bac585ec25340d1f1d047f9a1f8dcd8e243821
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 6%

---


# 모니터링 지침 {#monitoring-guidelines}

<table>
<tr><td><img src="assets/do-not-localize/icon_system.svg" width="60px"><p><a href="#monitoring-system">시스템 모니터링</a></p></td>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#moniroting-workflows">워크플로우 모니터링</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#monitoring-deliveries">배달 모니터링</a></p></td></tr>
</table>

Campaign Standard은 여러 가지 방법으로 인스턴스를 모니터링하여 시스템이 건강한지 확인하고 워크플로우 설정, 배달 전송 등에서 발생할 수 있는 문제를 최종적으로 해결할 수 있습니다.

## 시스템 모니터링 {#monitoring-system}

<img src="assets/do-not-localize/icon_system.svg" width="60px">

**시스템 알림** Campaign Standard 인터페이스는 시스템 상황에 대해 계속 알릴 수 있는 알림 창을 제공합니다. 이벤트 상태, 시스템 업데이트, 작업 필요 등 [자세한 내용](../../start/using/interface-description.md#top-bar)


**기술 워크플로우**&#x200B;기술 워크플로는 서버에 정기적으로 실행되도록 예약된 작업 또는 작업입니다. 인스턴스가 건강하고 제대로 기능하는지 확인하려면 항상 실행되고 있어야 합니다. [자세한 내용](../../administration/using/technical-workflows.md)

**Campaign 컨트롤 패널**&#x200B;을 사용하면 인스턴스의 여러 설정을 관리할 수 있습니다. URL 권한, 서버의 빌드 버전과 같은 인스턴스 세부 사항을 확인하고, 활성 프로필 사용 모니터링 등을 수행합니다. 또한 인스턴스에 연결된 SFTP 서버의 사용 가능한 공간을 모니터링할 수 있습니다. [자세한 내용](https://docs.adobe.com/content/help/ko-KR/control-panel/using/control-panel-home.html)

>[!NOTE]
>
>Campaign 컨트롤 패널은 관리 사용자에게만 액세스할 수 있으며 Adobe Managed Services을 사용하는 모든 고객도 사용할 수 있습니다.

**기술 개체****[!UICONTROL Diagnosis]** 메뉴는 응용 프로그램에서 생성한 여러 기술 개체를 모니터링하고 분석하는 주요 도구입니다. 데이터 스키마, 웹 페이지, 일괄 처리 작업 등 [자세한 내용](../../developing/using/monitoring-data-model-changes.md)

**내보내기 감사**내보내기 감사를 사용하여 인스턴스에 대해 수행된 내보내기를 모니터링할 수 있습니다. 워크플로우에서 업로드된 파일, 목록 내보내기 및 쪽지를 통해 다운로드한 파일.
[자세한 내용](../../administration/using/auditing-export-logs.md)

**라이선스**&#x200B;메뉴를 **[!UICONTROL Licenses]** 통해 인스턴스에 대한 정보를 모니터링합니다. 설치된 라이선스, 빌드 버전 및 약관 동의
[자세한 내용](../../administration/using/licenses.md)

## 워크플로우 모니터링 {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**우수 사례 및 문제 해결**워크플로우 사용 시 모범 사례 및 문제 해결 지침에 따라 성능을 개선할 수 있습니다.
[자세한 내용](../../automating/using/best-practices-workflows.md)

**로그 및 작업**워크플로우 로그 모니터링은 워크플로우를 분석하고 제대로 실행되고 있는지 확인하는 핵심 단계입니다.
[자세한 내용](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**알림**Campaign Standard을 사용하면 관리자의 작업 진행 상황을 모니터링하고 사용자의 주의를 요하는 오류가 있는지 확인하기 위해 감독자에게 알림을 보낼 수 있습니다.
[자세한 내용](../../automating/using/monitoring-workflow-execution.md#error-management)

## 배달 모니터링 {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**전달 능력**Campaign Standard은 배달된 메시지의 수를 향상시키는 데 도움이 되는 몇 가지 전달 기능 도구를 제공합니다. 전달 시간 보고서, 전송 시간 최적화, 메시지 미리 보기, 이메일 렌더링, 격리 관리 등
[자세한 내용](../../sending/using/about-deliverability.md)

**배달**메시지를 전송하면 세부 로그를 사용하여 메시지를 모니터링하고 캠페인의 성공을 측정할 수 있을 뿐만 아니라 메시지 수신자의 행동을 추적할 수 있습니다.
[자세한 내용](../../sending/using/monitoring-a-delivery.md)

**전달 경고**배달 경고 기능을 사용하면 배달 수행과 관련하여 사용자 그룹에 자동으로 전송되는 경고를 설정할 수 있습니다. 전송 또는 준비 실패, 잘못된 바운스 비율, 낮은 처리량 등.
[자세한 내용](../../sending/using/receiving-alerts-when-failures-happen.md)

**동적 보고**동적 보고는 배달이 수행되는 방식에 대해 지속적으로 알려주는 다양한 보고서를 제공합니다. 바운스 수, 수신자별 가장 많이 본 배달, 배달 처리량 등
[자세한 내용](../../reporting/using/about-dynamic-reports.md)
