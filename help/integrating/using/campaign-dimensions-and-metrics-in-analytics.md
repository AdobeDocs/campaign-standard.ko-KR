---
title: Analytics에서 Campaign 차원 및 지표 보기
description: Adobe Campaign에서 이메일 게재 추적을 시작하기 위해 Adobe Analytics에서 찾을 수 있는 다양한 차원을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 6516c71a-efa8-4778-82bb-10615378f985
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 3%

---

# Analytics에서 Campaign 차원 및 지표 보기{#campaign-dimensions-and-metrics-in-analytics}

Adobe Campaign 및 Adobe Analytics 통합을 통해 Adobe Analytics에서 직접 이메일 게재 성공 여부를 추적할 수 있습니다.

캠페인 **[!UICONTROL dimensions]** analytics의 목록은 다음과 같습니다.

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 캠페인 ID<br /> </td> 
   <td> Campaign에 표시되는 Campaign의 내부 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 캠페인 레이블<br /> </td> 
   <td> Campaign에 표시된 캠페인 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 게재 ID<br /> </td> 
   <td> Campaign에 표시되는 게재 내부 이름.<br /> 예를 들어 DM1은 매주 하위 게재를 보내도록 예약된 반복 게재입니다. DM2, DM3 및 DM4는 처음 3주에 전송됩니다. 그러면 게재 ID 차원에 모든 게재, 즉 DM1~DM4의 결과가 표시됩니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 게재 레이블<br /> </td> 
   <td> Campaign에 표시되는 게재 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 ID<br /> </td> 
   <td> Campaign에 표시되는 게재 내부 이름. 이는 Campaign에서 실행 중인 게재에만 관련됩니다.<br /> 예를 들어 DM1은 매주 하위 게재를 보내도록 예약된 반복 게재입니다. DM2, DM3 및 DM4는 처음 3주에 전송됩니다. 그러면 수행된 배달 ID 차원에 수행된 배달, 즉 하위 배달 DM2, DM3 및 DM4의 결과가 표시됩니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 실행된 게재 레이블<br /> </td> 
   <td> Campaign에 표시되는 게재 레이블. 이는 Campaign에서 실행 중인 게재에만 관련됩니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

캠페인 **[!UICONTROL metrics]** analytics의 목록은 다음과 같습니다.

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 클릭됨<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열림<br /> </td> 
   <td> 게재 중 메시지가 열린 횟수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전송됨<br /> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 총 바운스 수<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 오픈<br /> </td> 
   <td> 게재를 연 수신자 수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소됨<br /> </td> 
   <td> 구독 취소 링크의 클릭 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>
