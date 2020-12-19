---
solution: Campaign Standard
product: campaign
title: Analytics에서 Campaign 차원 및 지표 보기
description: Adobe Analytics에서 찾을 수 있는 다양한 차원을 살펴보고 Adobe Campaign에서 이메일 배달 추적을 시작합니다.
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

Adobe Campaign 및 Adobe Analytics 통합을 통해 Adobe Analytics에서 바로 이메일 전달의 성공을 추적할 수 있습니다.

Analytics에 있는 캠페인 **[!UICONTROL dimensions]**&#x200B;은(는) 아래에 나열되어 있습니다.

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
   <td> 캠페인<br />에 표시된 캠페인 내부 이름 </td> 
  </tr> 
  <tr> 
   <td> 캠페인 레이블<br /> </td> 
   <td> 캠페인<br />에 표시된 캠페인 레이블 </td> 
  </tr> 
  <tr> 
   <td> 배달 ID<br /> </td> 
   <td> 게재 내부 이름이 캠페인에 표시됩니다.<br /> 예를 들어 DM1은 매주 하위 제공을 보내도록 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 후에 전송됩니다. 그런 다음 배달 ID 차원이 모든 배달(DM1 - DM4)에 대한 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 레이블<br /> </td> 
   <td> 캠페인<br />에 표시된 게재 레이블 </td> 
  </tr> 
  <tr> 
   <td> 실행된 배달 ID<br /> </td> 
   <td> 게재 내부 이름이 캠페인에 표시됩니다. 이는 Campaign의 실행 시 전달과 관련된 것입니다.<br /> 예를 들어 DM1은 매주 하위 제공을 보내도록 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 후에 전송됩니다. 그런 다음 실행된 배달 ID 차원은 하위 배달 DM2, DM3 및 DM4와 같이 실행된 게재에 대한 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 실행 배달 레이블<br /> </td> 
   <td> 게재 레이블이 캠페인에 표시됩니다. 이는 캠페인의 실행 시 전달에 대한 문제일 뿐입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Analytics에 있는 캠페인 **[!UICONTROL metrics]**&#x200B;은(는) 아래에 나열되어 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 클릭한 항목<br /> </td> 
   <td> 배달에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
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
   <td> 보낸 날짜<br /> </td> 
   <td> 배달에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 총 바운스 수<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류 수<br /> </td> 
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
   <td> 구독 취소 링크에 대한 클릭 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

