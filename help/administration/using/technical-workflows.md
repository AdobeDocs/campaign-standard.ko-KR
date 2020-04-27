---
title: 기술 워크플로우
description: 기술 워크플로우는 Adobe Campaign의 백그라운드 기술 프로세스를 처리하기 위해 고안된 즉시 사용 가능한 워크플로우로서, 플랫폼의 올바른 동작을 보장합니다.
page-status-flag: never-activated
uuid: 6e763dc1-e1d3-4d94-bc0b-ef5b1703d8e5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: e9f147bd-6a5b-4b82-b9bb-311e38e22c62
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b4cbc56973a57cde8af6cefa9ff89c7d29ab7b79

---


# 기술 워크플로우{#technical-workflows}

기술 워크플로우는 Adobe Campaign과 함께 즉시 제공됩니다. 기술 워크플로는 서버에서 정기적으로 실행되도록 예약된 작업 또는 작업입니다.

이러한 기능을 통해 데이터베이스에서 유지 관리 작업을 수행하고, 게재의 추적 정보를 활용하고, 게재에서 임시 작업을 업데이트할 수 있습니다.

기능 관리자는 **[!UICONTROL Administration > Application settings > Workflows]** 메뉴에서 기술 워크플로우에 액세스할 수 있습니다.

>[!NOTE]
>
>기능 관리자는 기술 워크플로우를 다시 시작하거나 일시 중지하고 속성 및 구조를 수정할 수 있습니다.

![](assets/technical_workflows.png)

## 기술 워크플로우 목록 {#list-of-technical-workflows}

기술 워크플로우는 Adobe Campaign에서 자동으로 실행되는 백그라운드 및 기술 프로세스를 처리하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>레이블</strong><br /> </td> 
   <td> <strong>ID</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">A/B 테스트</span><br /> </td> 
   <td> <span class="uicontrol">abTesting</span><br /> </td> 
   <td> 이 워크플로우는 각 변형의 추적 로그를 분석합니다. A/B 테스트 기간이 끝나면 우승 변형을 자동으로 계산합니다. 기본적으로 매일 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">청구</span><br /> </td> 
   <td> <span class="uicontrol">청구</span><br /> </td> 
   <td> 이 워크플로우는 시스템 활동 보고서를 이메일로 '과금' 사용자에게 보냅니다. 기본적으로 매일 오전 1시에 자동으로 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">데이터베이스 정리</span><br /> </td> 
   <td> <span class="uicontrol">정리</span><br /> </td> 
   <td> 이 워크플로우는 데이터베이스 유지 관리 워크플로우입니다.다른 통계 및 프로세스를 실행하고 정의된 구성에 따라 데이터베이스에서 오래된 데이터를 삭제합니다. 기본적으로 매일 오전 4시에 자동으로 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">예측</span><br /> </td> 
   <td> <span class="uicontrol">예측</span><br /> </td> 
   <td> 이 워크플로우는 임시 예측에 저장된 게재의 분석을 실행합니다(임시 로그 작성). 기본적으로 매일 오전 1시에 시작됩니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">공유 대상자</span> 가져오기 <br /> </td> 
   <td> <span class="uicontrol">importSharedAudience</span><br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign에서 가져온 Adobe Experience Cloud 대상 데이터를 동기화합니다. 기본적으로 매 시간마다 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">즉각적인 보고서 공유</span><br /> </td> 
   <td> <span class="uicontrol">reportSendingNow</span><br /> </td> 
   <td> 이 워크플로우는 보고서가 전송되도록 예약되는 즉시 시작됩니다. 보고서를 pdf 파일로 변환한 다음 타깃팅된 수신자에게 이메일로 전송합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics를 사용한 KPI 조정</span><br /> </td> 
   <td> <span class="uicontrol">kpiAdjustment</span><br /> </td> 
   <td> 이 워크플로우는 하루에 한 번 보고 서비스의 KPI를 가져와서 Adobe Analytics의 데이터와 조정합니다. 그러면 필요할 때 차이를 밀어냅니다. 기본적으로 매일 오전 4.20시에 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">NMAC 옵트아웃</span> 관리 <br /> </td> 
   <td> <span class="uicontrol">mobileAppOptOutMgt</span><br /> </td> 
   <td> 이 워크플로우는 모바일 장치의 알림에 대한 구독 취소를 업데이트합니다. 기본적으로 오전 1시에서 자정 사이에 6시간마다 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">메시지 센터 로컬 보관</span><br /> </td> 
   <td> <span class="uicontrol">mcSynch_local</span><br /> </td> 
   <td> 이 워크플로우는 실시간 이벤트를 기록 테이블로 보관합니다. 기본적으로 매 시간마다 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보고 집계</span><br /> </td> 
   <td> <span class="uicontrol">reportingAggregate</span><br /> </td> 
   <td> 이 워크플로우는 보고서에 사용된 집계를 업데이트합니다. 기본적으로 오전 2시에 자동으로 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Adobe Analytics와 KPI 공유</span><br /> </td> 
   <td> <span class="uicontrol">kpiSharing</span><br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign Standard에서 Adobe Analytics로 15분마다 KPI 데이터를 전달합니다.<br /> </td> 
  </tr> 
    </tr> 
   <tr> 
   <td> <span class="uicontrol">Launch와</span> 동기화 <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span><br /> </td> 
   <td> 이 워크플로우는 Adobe Campaign Standard에서 가져온 Adobe Launch 모바일 속성을 동기화합니다. 15분마다 시작됩니다.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">배달 실행</span> 업데이트 <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryExecInfo</span><br /> </td> 
   <td> 이 워크플로우는 게재 추적을 업데이트합니다. 기본적으로 10분마다 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">전달 표시기</span> 업데이트 <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryIndicator</span><br /> </td> 
   <td> 이 워크플로우는 게시의 KPI(주요 성능 지표)를 업데이트합니다. 기본적으로 매 시간마다 시작됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">이벤트 상태</span> 업데이트 <br /> </td> 
   <td> <span class="uicontrol">updateEventsStatus</span><br /> </td> 
   <td> 이 워크플로우에서는 상태를 이벤트에 지정할 수 있습니다. 다음 이벤트 상태를 사용할 수 있습니다.<br /> 보류 <strong>중</strong>:이벤트가 대기열에 있습니다. 메시지 템플릿이 아직 지정되지 않았습니다.<br /> 배달 <span class="uicontrol">대기 중</span> :이벤트가 대기열에 있고 메시지 템플릿이 할당되어 전달에 의해 처리되는 중입니다.<br /> 전송 <strong></strong>:이 상태는 배달 로그에서 복사됩니다. 배달이 전송되었음을 의미합니다.<br /> 배달에서 <strong>무시됨</strong>:이 상태는 배달 로그에서 복사됩니다. 배달이 무시되었음을 의미합니다.<br /> 배달 <strong>실패</strong>:이 상태는 배달 로그에서 복사됩니다. 배달이 실패했다는 뜻입니다.<br /> <span class="uicontrol">이벤트가 고려되지</span> 않음:이벤트를 메시지 템플릿에 연결할 수 없습니다. 이벤트가 처리되지 않습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">전달</span> 업데이트 <br /> </td> 
   <td> <span class="uicontrol">deliverabilityUpdate</span><br /> </td> 
   <td> 이 워크플로우에서는 바운스 규칙 자격 규칙 목록과 플랫폼의 도메인 및 MX 목록을 만들 수 있습니다. 이 워크플로우는 HTTPS가 열려 있는 경우에만 작동합니다. 기본적으로 오전 2시에 자동으로 시작됩니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

