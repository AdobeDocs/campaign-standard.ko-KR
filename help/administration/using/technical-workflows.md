---
title: 기술 워크플로우
seo-title: 기술 워크플로우
description: 기술 워크플로우
seo-description: 기술 워크플로우는 Adobe Campaign의 백그라운드 기술 프로세스를 처리하기 위해 고안된 기본 작업 과정으로, 플랫폼의 올바른 동작을 보장합니다.
page-status-flag: 정품 인증 안 함
uuid: 6 e 763 dc 1-e 1 d 3-4 d 94-bc 0 b-ef 5 b 1703 d 8 e 5
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: application-settings
discoiquuid: e 9 f 147 bd -6 a 5 b -4 b 82-b 9 bb -311 e 38 e 22 c 62
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 2541b6dadd005c74d6bb737a0e3692e63a5b85db

---


# Technical workflows{#technical-workflows}

기술 워크플로우는 Adobe Campaign를 통해 즉시 제공됩니다. 기술 워크플로우는 서버에서 정기적으로 실행되도록 예약된 운영 또는 작업입니다.

이 기능을 사용하면 데이터베이스에서 유지 관리 작업을 수행하고, 배달의 추적 정보를 활용하고, 배달 시 임시 작업을 업데이트할 수 있습니다.

Functional administrators can access technical workflows under the **[!UICONTROL Administration > Application settings > Workflows]** menu.

>[!NOTE]
>
>기능 관리자는 기술 워크플로우를 다시 시작하거나 일시 중지할 수 있고 해당 속성과 구조를 수정할 수 있습니다.

![](assets/technical_workflows.png)

## List of technical workflows {#list-of-technical-workflows}

기술 워크플로우는 Adobe Campaign에서 자체적으로 트리거된 백그라운드 및 기술 프로세스를 처리하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>label</strong><br /> </td> 
   <td> <strong>ID</strong><br /> </td> 
   <td> <strong>description</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">A/B 테스트</span><br /> </td> 
   <td> <span class="uicontrol">Abtesting</span><br /> </td> 
   <td> 이 워크플로우는 각 변형에 대한 추적 로그를 분석합니다. A/B 테스트 기간이 종료되면 우승한 변형을 자동으로 계산합니다. By default, it is started every day.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">과금</span><br /> </td> 
   <td> <span class="uicontrol">과금</span><br /> </td> 
   <td> 이 워크플로우는 시스템 활동 보고서를 이메일로'과금'사용자에게 보냅니다. By default, it is automatically started every day at 1am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">데이터베이스 정리</span><br /> </td> 
   <td> <span class="uicontrol">정리</span><br /> </td> 
   <td> 이 워크플로우는 데이터베이스 유지 관리 워크플로우입니다. 다른 통계 및 프로세스를 실행하고 정의된 구성에 따라 데이터베이스에서 오래된 데이터를 삭제합니다. By default, it is automatically started every day 4am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">예측</span><br /> </td> 
   <td> <span class="uicontrol">예측</span><br /> </td> 
   <td> 이 워크플로우는 임시 예측에 저장된 게재 (임시 로그 작성) 의 분석을 실행합니다. By default, it is started every day at 1am. <br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">공유 대상 가져오기</span><br /> </td> 
   <td> <span class="uicontrol">Importsharedaudience</span><br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign에서 가져온 Adobe Experience Cloud 대상 데이터를 동기화합니다. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">즉각적인 보고서 공유</span><br /> </td> 
   <td> <span class="uicontrol">Reportsendingnow</span><br /> </td> 
   <td> 이 워크플로우는 보고서가 전송되도록 예약되는 즉시 시작됩니다. It converts your report into a pdf file then sends it in an email to the targeted recipients.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics를 사용한 KPI 조정</span><br /> </td> 
   <td> <span class="uicontrol">Kpireconciliation</span><br /> </td> 
   <td> 이 워크플로우는 하루에 한 번 보고 서비스에서 KPI를 가져와 Adobe Analytics의 데이터와 통합합니다. 그런 다음 필요한 경우 그 차이를 푸시합니다. By default, it is started every day at 4.20am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">NMAC 옵트아웃 관리</span><br /> </td> 
   <td> <span class="uicontrol">mobileappoptoutmgt</span><br /> </td> 
   <td> 이 워크플로우는 모바일 장치에서 알림의 가입을 업데이트합니다. By default, it is started every 6 hours between 1am and midnight.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">메시지 센터 로컬 보관</span><br /> </td> 
   <td> <span class="uicontrol">mcsynch_ local</span><br /> </td> 
   <td> 이 워크플로우는 실시간 이벤트를 내역 테이블로 보관합니다. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">집계 보고</span><br /> </td> 
   <td> <span class="uicontrol">Reportingaggregate</span><br /> </td> 
   <td> 이 워크플로우는 보고서에 사용된 합계를 업데이트합니다. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics와 KPI 공유</span><br /> </td> 
   <td> <span class="uicontrol">Kpisharing</span><br /> </td> 
   <td> This workflow pushes KPI data every 15 minutes from Adobe Campaign Standard to Adobe Analytics.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">배달 실행 업데이트</span><br /> </td> 
   <td> <span class="uicontrol">Updatedeliveryexecinfo</span><br /> </td> 
   <td> 이 워크플로우는 게재 추적을 업데이트합니다. By default, it is started every 10 minutes.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">배달 표시기 업데이트</span><br /> </td> 
   <td> <span class="uicontrol">Updatedeliveryindicator</span><br /> </td> 
   <td> 이 워크플로우는 게재 KPI (Key Performance Indicator) 를 업데이트합니다. By default, it is started every hour.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">이벤트 상태 업데이트</span><br /> </td> 
   <td> <span class="uicontrol">Updateeventsstatus</span><br /> </td> 
   <td> 이 워크플로우에서는 이벤트에 상태를 지정할 수 있습니다. The following event statuses are available:<br /> <strong>Pending</strong>: The event is in a queue. 아직 지정된 메시지 템플릿이 없습니다.<br /><span class="uicontrol">배달</span> 보류 중: 이벤트가 대기열에 있는 경우 메시지 템플릿이 할당되었으며 배달에 의해 처리됩니다.<br /><strong>전송</strong>: 이 상태는 배달 로그에서 복사됩니다. 배달이 전송되었음을 의미합니다.<br /><strong>게시에 의해</strong>무시됨: 이 상태는 배달 로그에서 복사됩니다. 이것은 배달이 무시되었음을 의미합니다.<br /><strong>배달 실패</strong>: 이 상태는 배달 로그에서 복사됩니다. 배달이 실패했음을 의미합니다.<br /><span class="uicontrol">고려되지 않는 이벤트</span> : 이벤트를 메시지 템플릿에 연결할 수 없습니다. The event will not be processed.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">배달 기능 업데이트</span><br /> </td> 
   <td> <span class="uicontrol">Deliverabilityupdate</span><br /> </td> 
   <td> 이 워크플로우에서는 플랫폼에서 도메인 및 MX 목록과 바운스 규칙 검증 규칙 목록을 만들 수 있습니다. 이 워크플로우는 HTTPS가 열려 있는 경우에만 작동합니다. By default, it is automatically started at 2am.<br /> </td> 
  </tr> 
 </tbody> 
</table>

