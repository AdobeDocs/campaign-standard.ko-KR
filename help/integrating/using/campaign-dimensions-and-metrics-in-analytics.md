---
title: Analytics의 캠페인 차원 및 지표
seo-title: Analytics의 캠페인 차원 및 지표
description: Analytics의 캠페인 차원 및 지표
seo-description: Adobe Analytics에서 제공되는 다양한 차원을 살펴보고 Adobe Campaign에서 이메일 배달을 추적할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: Effa 1028-66 B 2-4 BEF-B 5 E 4-7319 DBB 23 D 5 D
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: Working-with-campaign-and-analytics
discoiquuid: EB 3639 F 5-7246-46 c 4-8 DDB-DA 9413 B 40 C 32
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Campaign dimensions and metrics in Analytics{#campaign-dimensions-and-metrics-in-analytics}

Adobe Campaign와 Adobe Analytics 통합을 통해 Adobe Analytics에서 이메일 게재 성과를 추적할 수 있습니다.

Campaign **[!UICONTROL dimensions]** found in Analytics are listed below:

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Campaign ID<br /> </td> 
   <td> Campaign's internal name as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign label<br /> </td> 
   <td> Campaign's label as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery ID<br /> </td> 
   <td> 캠페인에서 볼 때의 내부 이름.<br /> 예를 들어 DM 1는 매주 하위 배달을 전송하도록 예약된 반복 배달입니다. DM 2, DM 3 및 DM 4는 처음 3 주 동안 전송됩니다. The Delivery ID dimension will then display the results for every delivery, namely DM1 to DM4. <br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery label<br /> </td> 
   <td> Delivery's label as seen in Campaign<br /> </td> 
  </tr> 
  <tr> 
   <td> Executed delivery ID<br /> </td> 
   <td> 캠페인에서 볼 때의 내부 이름. 이는 캠페인에서 실행 중인 전달에만 적용됩니다.<br /> 예를 들어 DM 1는 매주 하위 배달을 전송하도록 예약된 반복 배달입니다. DM 2, DM 3 및 DM 4는 처음 3 주 동안 전송됩니다. The Executed delivery ID dimension will then display the results for the executed deliveries, namely the child deliveries DM2, DM3 and DM4. <br /> </td> 
  </tr> 
  <tr> 
   <td> Executed delivery label<br /> </td> 
   <td> 캠페인에서 본 게재 레이블입니다. This only concerns delivery in execution in Campaign.<br /> </td> 
  </tr> 
 </tbody> 
</table>

Campaign **[!UICONTROL metrics]** found in Analytics are listed below:

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Clicked<br /> </td> 
   <td> Number of times a content was clicked in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Opened<br /> </td> 
   <td> Number of times a message was opened in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sent<br /> </td> 
   <td> Total number of sends for the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Total Bounces<br /> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Open<br /> </td> 
   <td> Number of recipients who opened the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Click<br /> </td> 
   <td> Number of recipients who clicked on a content in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribed<br /> </td> 
   <td> Number of clicks on the unsubscription link.<br /> </td> 
  </tr> 
 </tbody> 
</table>

