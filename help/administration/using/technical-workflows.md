---
title: 기술 워크플로우
description: 기술 워크플로우에 대해 자세히 알아보기
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: da3a3af5-207a-4289-bd07-00a8c5d1cf57
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 89%

---

# 기술 워크플로우{#technical-workflows}

기술 워크플로우는 Adobe Campaign과 함께 기본적으로 제공됩니다. 기술 워크플로우는 서버에서 정기적으로 실행하도록 예약된 작업 또는 작업입니다.

이를 통해 데이터베이스 유지 관리 작업을 수행하고, 게재 시 추적 정보를 활용하고, 게재의 임시 작업을 업데이트할 수 있습니다.

기능 관리자는 **[!UICONTROL Administration > Application settings > Workflows]** 메뉴를 통해 기술 워크플로우에 액세스할 수 있습니다.

>[!NOTE]
>
>기능 관리자는 기술 워크플로우를 다시 시작하거나 일시 중지하고, 속성 및 구조를 수정할 수 있습니다.

![](assets/technical_workflows.png)

## 기술 워크플로우 목록 {#list-of-technical-workflows}

기술 워크플로우는 Adobe Campaign에서 자동으로 트리거되는 백그라운드 및 기술 프로세스를 처리하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>레이블</strong><br /> </td> 
   <td> <strong>ID</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">A/B 테스트</span> <br /> </td> 
   <td> <span class="uicontrol">abTesting</span> <br /> </td> 
   <td> 이 워크플로우는 각 변형의 추적 로그를 분석합니다. A/B 테스트 기간이 끝나면 자동으로 가장 효과적인 변형을 계산합니다. 기본적으로 매일 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">과금</span> <br /> </td> 
   <td> <span class="uicontrol">billing</span> <br /> </td> 
   <td> 이 워크플로우는 '과금' 사용자에게 이메일로 시스템 활동 보고서를 보냅니다. 기본적으로 매일 오전 1시에 자동 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">데이터베이스 정리</span> <br /> </td> 
   <td> <span class="uicontrol">cleanup</span> <br /> </td> 
   <td> 이 워크플로우는 데이터베이스 유지 관리 워크플로우입니다. 다양한 통계 및 프로세스를 실행하고, 정의된 구성에 따라 데이터베이스에서 오래된 데이터를 삭제합니다. 기본적으로 매일 오전 4시에 자동 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">예측</span> <br /> </td> 
   <td> <span class="uicontrol">forecasting</span> <br /> </td> 
   <td> 이 워크플로우는 임시 예측(임시 로그 생성)에 저장된 게재의 분석을 실행합니다. 기본적으로 매일 오전 1시에 시작됩니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">공유 대상자 가져오기</span> <br /> </td> 
   <td> <span class="uicontrol">importSharedAudience</span> <br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign에 가져온 Adobe Experience Cloud 대상자 데이터를 동기화합니다. 기본적으로 매시간 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보고서 즉시 공유</span> <br /> </td> 
   <td> <span class="uicontrol">reportSendingNow</span> <br /> </td> 
   <td> 이 워크플로우는 보고서를 보내도록 예약하는 즉시 시작됩니다. 보고서를 pdf 파일로 변환한 다음 타겟팅된 수신자에게 이메일로 전송합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics와의 KPI 조정</span> <br /> </td> 
   <td> <span class="uicontrol">kpiReconciliation</span> <br /> </td> 
   <td> 이 워크플로우는 하루에 한 번 보고 서비스의 KPI를 가져와서 Adobe Analytics의 데이터와 조정합니다. 필요한 경우 차이를 적용합니다. 기본적으로 매일 오전 4시 20분에 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">메시지 센터 로컬 아카이빙</span> <br /> </td> 
   <td> <span class="uicontrol">mcSynch_local</span> <br /> </td> 
   <td> 이 워크플로우는 실시간 이벤트를 기록 표로 아카이빙합니다. 기본적으로 매시간 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">합계 보고</span> <br /> </td> 
   <td> <span class="uicontrol">reportingAggregates</span> <br /> </td> 
   <td> 이 워크플로우는 보고서에 사용되는 합계를 업데이트합니다. 기본적으로 오전 2시에 자동 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics와 KPI 공유</span> <br /> </td> 
   <td> <span class="uicontrol">kpiSharing</span> <br /> </td> 
   <td> 이 워크플로우는 15분마다 Adobe Campaign Standard에서 Adobe Analytics로 KPI 데이터를 푸시합니다.<br /> </td> 
  </tr> 
    </tr> 
   <tr> 
   <td> <span class="uicontrol">Launch와 동기화</span> <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span> <br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign Standard에 가져온 태그 모바일 속성을 동기화합니다. 15분마다 시작됩니다.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">추적 로그 복구</span> <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span> <br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign Standard에 가져온 태그 모바일 속성을 동기화합니다. 15분마다 시작됩니다.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">추적 로그 복구</span> <br /> </td> 
   <td> <span class="uicontrol">trackingLogRecovery</span> <br /> </td> 
   <td> 이 워크플로우는 손실된 추적 로그를 복원합니다. 이 기술 워크플로우는 특정 컨텍스트에서 사용되며 Adobe 내부용으로만 제한됩니다. <br> 기본적으로 10분마다 시작됩니다.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">게재 실행 업데이트</span> <br/> </td> 
   <td> <span class="uicontrol">updateDeliveryExecInfo</span> <br/> </td> 
   <td> 이 워크플로우는 로컬 데이터베이스의 브로드로그 및 추적 로그를 복사합니다. 기본적으로 10분마다 시작됩니다.<br/> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">게재 표시기 업데이트</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryIndicators</span> <br /> </td> 
   <td> 이 워크플로우는 게재의 KPI(주요 성과 지표)를 업데이트합니다. 기본적으로 매시간 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">이벤트 상태 업데이트</span> <br /> </td> 
   <td> <span class="uicontrol">updateEventsStatus</span> <br /> </td> 
   <td> 이 워크플로우를 통해 이벤트 상태를 지정할 수 있습니다. 다음 이벤트 상태를 사용할 수 있습니다.<br /> <strong>보류 중</strong>: 이벤트가 큐에 있습니다. 메시지 템플릿이 아직 할당되지 않았습니다.<br /> <span class="uicontrol">게재 보류 중</span> : 이벤트가 큐에 있고 메시지 템플릿이 할당되어 게재에 의해 처리되는 중입니다.<br /> <strong>전송됨</strong>: 이 상태는 게재 로그에서 복사됩니다. 게재가 보내졌다는 뜻입니다.<br /> <strong>게재에서 무시됨</strong>: 이 상태는 게재 로그에서 복사됩니다. 게재가 무시되었다는 뜻입니다.<br /> <strong>게재 실패</strong>: 이 상태는 게재 로그에서 복사됩니다. 게재에 실패했다는 뜻입니다.<br /> <span class="uicontrol">이벤트가 고려되지 않음</span> : 이벤트를 메시지 템플릿에 연결할 수 없습니다. 이벤트가 처리되지 않습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">게재 능력을 위한 업데이트</span> <br /> </td> 
   <td> <span class="uicontrol">게재능력업데이트</span> <br /> </td> 
   <td> 이 워크플로우를 통해 반송 규칙 자격 규칙 목록과 플랫폼에 있는 도메인 및 MX 목록을 만들 수 있습니다. 이 워크플로우는 HTTPS가 열려 있는 경우에만 작동합니다. 기본적으로 오전 2시에 자동 시작됩니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>
