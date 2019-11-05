---
title: Analytics에서 Campaign 차원 및 지표 보기
description: Adobe Analytics에서 찾을 수 있는 다양한 차원을 학습하여 Adobe Campaign에서 이메일 게재 추적을 시작합니다.
page-status-flag: 활성화 안 함
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Analytics에서 Campaign 차원 및 지표 보기{#campaign-dimensions-and-metrics-in-analytics}

Adobe Campaign 및 Adobe Analytics와의 통합을 통해 Adobe Analytics에서 직접 이메일 전달의 성공을 추적할 수 있습니다.

Analytics에서 **[!UICONTROL dimensions]** 찾은 캠페인은 다음과 같습니다.

<table> 
 <thead> 
  <tr> 
   <th> 차원<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 캠페인 ID<br /> </td> 
   <td> 캠페인에서 본 캠페인의 내부 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 캠페인 레이블<br /> </td> 
   <td> 캠페인에 표시된 캠페인 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 ID<br /> </td> 
   <td> Campaign에 표시된 게재 내부 이름입니다.<br /> 예를 들어 DM1은 매주 하위 배달 전송을 보내도록 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 그런 다음 배달 ID 차원은 모든 배달(즉, DM1 - DM4)에 대한 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 레이블<br /> </td> 
   <td> 캠페인에 표시된 게재 레이블<br /> </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 ID<br /> </td> 
   <td> Campaign에 표시된 게재 내부 이름입니다. 이는 Campaign의 실행에 대한 전달에만 해당됩니다.<br /> 예를 들어 DM1은 매주 하위 배달 전송을 보내도록 예약된 반복 배달입니다. DM2, DM3 및 DM4는 처음 3주 동안 전송됩니다. 그런 다음 실행된 배달 ID 차원은 하위 배달 DM2, DM3 및 DM4 등의 실행 결과를 표시합니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 수행된 배달 레이블<br /> </td> 
   <td> 게재 레이블에 표시됩니다. 이는 Campaign의 실행에 대한 전달에만 해당됩니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Analytics에서 **[!UICONTROL metrics]** 찾은 캠페인은 다음과 같습니다.

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
   <td> 배달의 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 총 바운스 수<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 배달 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br /> </td> 
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

