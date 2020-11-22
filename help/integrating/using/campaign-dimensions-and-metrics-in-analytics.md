---
solution: Campaign Standard
product: campaign
title: Analytics에서 Campaign 차원 및 지표 보기
description: Adobe Campaign에서 이메일 배달 추적을 시작하려면 Adobe Analytics에서 찾을 수 있는 다양한 차원을 학습합니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 3%

---


# Analytics에서 Campaign 차원 및 지표 보기{#campaign-dimensions-and-metrics-in-analytics}

Adobe Campaign과 Adobe Analytics 통합을 통해 Adobe Analytics에서 바로 이메일 전달의 성공 여부를 추적할 수 있습니다.

Analytics **[!UICONTROL dimensions]** 에 있는 캠페인은 아래에 나열되어 있습니다.

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
   <td> 캠페인에 표시된 캠페인 내부 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 캠페인 레이블<br /> </td> 
   <td> 캠페인에 표시된 캠페인 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 ID<br /> </td> 
   <td> 게재 내부 이름이 캠페인에 표시됩니다.<br /> 예를 들어 DM1은 매주 하위 배달 전송을 위해 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 배달 ID 차원은 모든 배달(DM1 - DM4)에 대한 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 레이블<br /> </td> 
   <td> 캠페인에 표시된 게재 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 실행된 배달 ID<br /> </td> 
   <td> 게재 내부 이름이 캠페인에 표시됩니다. 이는 Campaign의 실행 시 전달과 관련된 것입니다.<br /> 예를 들어 DM1은 매주 하위 배달 전송을 위해 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 그런 다음 실행된 배달 ID 차원은 하위 배달 DM2, DM3 및 DM4 등의 실행 전달 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 레이블<br /> </td> 
   <td> 게재 레이블에 표시됩니다. 이는 Campaign의 실행 시 전달과 관련된 것입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Analytics **[!UICONTROL metrics]** 에 있는 캠페인은 아래에 나열되어 있습니다.

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
   <td> 게재에서 컨텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열림<br /> </td> 
   <td> 배달에서 메시지를 연 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전송<br /> </td> 
   <td> 배달에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 총 바운스 수<br /> </td> 
   <td> 전송 및 자동 반환 처리 중에 누적된 총 오류 수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> 배달을 연 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> 배달에서 콘텐츠를 클릭한 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소<br /> </td> 
   <td> 구독 취소 링크에 대한 클릭 수.<br /> </td> 
  </tr> 
 </tbody> 
</table>

