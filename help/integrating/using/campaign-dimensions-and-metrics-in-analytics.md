---
title: Analytics에서 Campaign 차원 및 지표 보기
description: Adobe Analytics에서 Adobe Campaign에서 이메일 게재 추적을 시작할 수 있는 다양한 차원을 알아봅니다.
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

Adobe Campaign과 Adobe Analytics 통합을 사용하면 Adobe Analytics에서 직접 이메일 게재의 성공을 추적할 수 있습니다.

Analytics에 있는 **[!UICONTROL dimensions]** 캠페인은 아래에 나와 있습니다.

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
   <td> Campaign<br />에 표시된 Campaign의 내부 이름 </td> 
  </tr> 
  <tr> 
   <td> Campaign 레이블<br /> </td> 
   <td> Campaign<br />에 표시된 캠페인 레이블 </td> 
  </tr> 
  <tr> 
   <td> 배달 ID<br /> </td> 
   <td> 게재의 내부 이름이 Campaign에 표시된 것처럼 표시됩니다.<br /> 예를 들어 DM1은 매주 하위 게재를 보내도록 예약된 반복 게재입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 그런 다음 배달 ID 차원은 모든 게재에 대한 결과(즉, DM1 - DM4)를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 레이블<br /> </td> 
   <td> Campaign<br />에 표시된 게재 레이블입니다. </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 ID<br /> </td> 
   <td> 게재의 내부 이름이 Campaign에 표시된 것처럼 표시됩니다. 이는 Campaign의 실행 시 전달에만 해당됩니다.<br /> 예를 들어 DM1은 매주 하위 게재를 보내도록 예약된 반복 게재입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 그런 다음 실행된 배달 ID 차원은 실행된 게재, 즉 하위 게재 DM2, DM3 및 DM4에 대한 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 레이블<br /> </td> 
   <td> Campaign에 표시된 게재 레이블입니다. 이는 Campaign의 실행 시 전달에만 해당됩니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Analytics에 있는 **[!UICONTROL metrics]** 캠페인은 아래에 나와 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <br /> 클릭 </td> 
   <td> 게재에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열림<br /> </td> 
   <td> 게재에서 메시지를 연 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전송<br /> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 총 바운스 수<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유한 열기<br /> </td> 
   <td> 게재를 연 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 가입 해지됨<br /> </td> 
   <td> 구독 취소 링크에 대한 클릭 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>
