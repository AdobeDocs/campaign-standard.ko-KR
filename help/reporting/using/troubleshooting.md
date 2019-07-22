---
title: 문제 해결
seo-title: 문제 해결
description: 문제 해결
seo-description: 동적 보고와 관련된 일반적인 질문을 살펴보십시오.
page-status-flag: 정품 인증 안 함
uuid: A 84 A 18 BD -4 E 33-466 E-A 6 CE-D 7008 FE 12746
contentOwner: Beneat
products: sg_ campaign/standard
audience: 보고
content-type: 참조
topic-tags: 문제 해결
discoiquuid: BBB 41 C 38-12 C 1-4625-85 D 5-69627 E 2 F 4 B 39
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: e0cbdfecde495d7c9f8bfa33dd5ee8598cdfe60a

---


# Troubleshooting{#troubleshooting}

이 섹션에서는 동적 보고와 관련된 일반적인 질문을 찾을 수 있습니다.

## For Unique opens and Unique clicks, the count in the aggregate row is not matching the ones in individual rows {#unique-open-clicks-no-match}

예상되는 동작입니다.
다음 예제를 통해 이러한 행동을 설명할 수 있습니다.

이메일이 프로필 P 1 및 P 2로 전송됩니다.

P 1는 첫 날에는 이메일을 두 번, 두 번째 날에는 트리 시간을 엽니다.

반면에 P 2는 첫 날에 이메일을 한 번 열고 다음 날 다시 열지 않습니다.
다음은 보낸 이메일과 프로필의 상호 작용을 시각적으로 나타낸 것입니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>day</strong><br /> </th> 
   <th align="center"> <strong>opens</strong><br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> Day 1<br /> </td> 
   <td align="center"> 2 + 1 = 3<br /> </td> 
   <td align="center"> 1 + 1 = 2<br /> </td> 
  </tr> 
  <tr> 
   <td align="center"> Day 2<br /> </td> 
   <td align="center"> 3 + 0 = 3<br /> </td> 
   <td align="center"> 1 + 0 = 1<br /> </td> 
  </tr>
 </tbody> 
</table>

To understand the overall number of unique opens, we need to sum up the row counts of **[!UICONTROL Unique Opens]** which gives us the value 3. 그러나 이메일이 2 개의 프로필만 대상으로 지정되었으므로 공개율은 150%가 되어야 합니다.

To not obtain percentage higher than 100, the definition of **[!UICONTROL Unique Opens]** is maintained to be the number of unique broadlogs that were opened. 이 경우 P 1 이 1 일과 2 일에 이메일을 열어도 자신의 고유 열기는 여전히 1 입니다.

이렇게 하면 다음 표가 만들어집니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>day</strong><br /> </th> 
   <th align="center"> <strong>opens</strong><br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> Day 1<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 2<br /> </td>
  </tr> 
  <tr> 
   <td align="center"> Day 2<br /> </td> 
   <td align="center"> 3<br /> </td> 
   <td align="center"> 2<br /> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하며, 이로 인해 매우 부정확할 수 있습니다.

## Open counts do not match the Database count {#open-counts-no-match-database}

This may be due to the fact that, heuristics are used in Dynamic reporting to track opens even when we can't track the **[!UICONTROL Open]** action.

For example, if a user has disabled images on their client and click on a link in the email, the **[!UICONTROL Open]** may not be tracked by the database but the **[!UICONTROL Click]** will.

Therefore, the **[!UICONTROL Open]** tracking logs counts may not have the same count in the database.

Such occurrences are added as **"an email click implies an email open"**.

>[!NOTE]
>
>고유한 카운트는 HLL 기반 스케치를 기반으로 하므로, 카운트 간의 사소한 불일치를 경험할 수 있습니다.

## 반복/거래 게재 횟수는 어떻게 계산됩니까?

반복 및 거래 배달을 사용하여 작업할 때 카운트는 상위 및 하위 배달 모두에 귀속됩니다.

We can take the example of a recurring delivery named **R1** set to run every day on day 1 (RC1), day 2 (RC2) and day 3 (RC3).

한 사람만 모든 하위 배달을 여러 번 열었다고 가정합니다. In this case, the individual recurring child deliveries will show the **[!UICONTROL Open]** count as 1 for each.

However, since the same person clicked on all the deliveries, the parent recurring delivery will also have **[!UICONTROL Unique open]** as 1.

After the Adobe Campaign Standard 19.2.1 release, the definition of **Unique counts** is changed from **Number of unique persons interacting with the delivery** to **Number of unique messages interacted**.

Adobe Campaign Standard 19.2.1 릴리스 전에 보고서는 다음과 같이 표시되었습니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>배달</strong><br /> </th> 
   <th align="center"> <strong>sent</strong><br /> </th> 
   <th align="center"> <strong>배달됨</strong><br /> </th>
   <th align="center"> <strong>opens</strong><br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1<br/> </td> 
   <td align="center"> <strong>100<br/> </td> 
   <td align="center"> <strong>90<br/> </td> 
   <td align="center"> <strong>10<br/> </td> 
   <td align="center"> <strong>1<br/> </td> 
  </tr> 
  <tr> 
   <td align="center"> RC1<br/> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
    <tr> 
   <td align="center"> RC2<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 30<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
    <tr> 
   <td align="center"> RC3<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
 </tbody> 
</table>

Adobe Campaign Standard 19.2.1 릴리스 이후 보고서는 다음과 같이 표시됩니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>배달</strong><br /> </th> 
   <th align="center"> <strong>sent</strong><br /> </th> 
   <th align="center"> <strong>배달됨</strong><br /> </th>
   <th align="center"> <strong>opens</strong><br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1<br/> </td> 
   <td align="center"> <strong>100<br/> </td> 
   <td align="center"> <strong>90<br/> </td> 
   <td align="center"> <strong>10<br/> </td> 
   <td align="center"> <strong>3<br/> </td> 
  </tr> 
  <tr> 
   <td align="center"> RC1<br/> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 20<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
    <tr> 
   <td align="center"> RC2<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 30<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
    <tr> 
   <td align="center"> RC3<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 2<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
 </tbody> 
</table>

## What is the colors' signification in my reports' table? {#reports-color-signification}

보고서에 표시된 색상은 임의로 처리되며 개인화할 수 없습니다. 진행률 표시줄을 나타내며 보고서에서 도달한 최대 값을 더 잘 강조 표시하는 데 도움이 됩니다.

아래 예에서 셀은 값이 100% 이기 때문에 동일한 색상을 갖습니다.

![](assets/troubleshooting_1.png)

**조건부 서식을** 사용자 정의로 변경하면 값이 상한에 도달하면 더 흐리게 표시됩니다. 반면에 더 낮은 한도에 도달하면 Redder가 생성됩니다.

For example, here, we set the **Upper limit** to 500 and **Lower limit** to 0.

![](assets/troubleshooting_2.png)