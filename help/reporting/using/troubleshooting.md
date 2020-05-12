---
title: 문제 해결
description: 동적 보고 관련 일반적인 질문을 찾습니다.
page-status-flag: never-activated
uuid: a84a18bd-4e33-466e-a6ce-d7008fe12746
contentOwner: beneat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: troubleshooting
discoiquuid: bbb41c38-12c1-4625-85d5-69627e2f4b39
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a894e72bb02fbecb86d43c6d2a13adf7ab10f73e
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 5%

---


# 문제 해결{#troubleshooting}

이 섹션에서는 동적 보고 관련 일반적인 질문을 찾을 수 있습니다.

## 고유 열기 및 고유 클릭 수의 경우 집계 행의 개수가 개별 행의 개수와 일치하지 않습니다 {#unique-open-clicks-no-match}

이는 예상 행동입니다.
다음 예를 들어 이 동작을 설명할 수 있습니다.

프로필 P1 및 P2로 이메일이 전송됩니다.

P1은 첫 번째 날에 두 번 이메일을 열고 두 번째 날에 세 번 이메일을 엽니다.

반면 P2는 첫 날에 이메일을 한 번 열고 다음 날 다시 열지 않습니다.
전송된 이메일과 프로필의 상호 작용을 시각적으로 보여줍니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>일</strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> 1일<br /> </td> 
   <td align="center"> 2 + 1 = 3<br /> </td> 
   <td align="center"> 1 + 1 = 2<br /> </td> 
  </tr> 
  <tr> 
   <td align="center"> 2일<br /> </td> 
   <td align="center"> 3 + 0 = 3<br /> </td> 
   <td align="center"> 1 + 0 = 1<br /> </td> 
  </tr>
 </tbody> 
</table>

전체 고유 열기 수를 이해하려면 값 3을 제공하는 행 카운트를 **[!UICONTROL Unique Opens]** 합산해야 합니다. 그러나 이메일이 2개의 프로필만 대상으로 작성되었으므로 공개 비율은 150%로 표시되어야 합니다.

100보다 높은 백분율을 획득하지 않기 위해 의 정의 **[!UICONTROL Unique Opens]** 는 열린 고유한 브로드로그 수로 유지됩니다. 이 경우, P1이 1일과 2일에 이메일을 열더라도, 그의 고유한 열기는 여전히 1이 됩니다.

그러면 다음 표가 나타납니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>일</strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> 1일<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 2<br /> </td>
  </tr> 
  <tr> 
   <td align="center"> 2일<br /> </td> 
   <td align="center"> 3<br /> </td> 
   <td align="center"> 2<br /> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하므로 큰 수에 약간 오류가 발생할 수 있습니다.

## 열린 카운트가 데이터베이스 수와 일치하지 않습니다. {#open-counts-no-match-database}

이는 동작을 추적할 수 없을 때도 열림 추적을 추적하기 위해 동적 보고에 휴리스틱이 사용되기 때문일 수 **[!UICONTROL Open]** 있습니다.

예를 들어, 사용자가 클라이언트에서 이미지를 비활성화하고 이메일에 있는 링크를 클릭하는 경우, 해당 이미지를 데이터베이스에 의해 추적되지 **[!UICONTROL Open]** 않지만 **[!UICONTROL Click]** 추적하게 됩니다.

따라서 **[!UICONTROL Open]** 추적 로그 카운트는 데이터베이스에서 동일한 카운트가 아닐 수 있습니다.

이러한 항목은 **&quot;이메일 클릭은 이메일 열기를 의미함&quot;으로 추가됩니다**.

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하므로 카운트 간의 사소한 불일치를 경험할 수 있습니다.

## 반복/트랜잭션 배달의 카운트는 어떻게 계산됩니까? {#counts-recurring-deliveries}

반복 및 트랜잭션 배달로 작업할 때 카운트는 상위 및 하위 배달 모두에 적용됩니다.
1일(RC1), 2일(RC2) 및 3일(RC3)에 매일 실행되도록 **R1** 세트라는 반복 배달의 예를 들 수 있습니다.
한 사람만 모든 하위 배달물을 여러 번 열었다고 가정해 봅시다. 이 경우, 개별 반복 하위 배달은 각각에 대해 **[!UICONTROL Open]** 카운트를 1로 표시합니다.
하지만 동일한 사용자가 모든 배달을 클릭했기 때문에 상위 반복 배달도 **[!UICONTROL Unique open]** 1입니다.

보고서는 다음과 같아야 합니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>게재</strong> <br /> </th> 
   <th align="center"> <strong>전송</strong> <br /> </th> 
   <th align="center"> <strong>배달됨</strong> <br /> </th>
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기</strong> <br /> </th>
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

## 보고서 테이블의 색상은 무엇입니까? {#reports-color-signification}

보고서에 표시되는 색상은 임의로 표시되며 개인화할 수 없습니다. 진행률 표시줄을 나타내며 보고서에서 도달한 최대값을 더 잘 강조하도록 표시됩니다.

아래 예에서 셀은 값이 100%이므로 색상이 동일합니다.

![](assets/troubleshooting_1.png)

사용자 지정 값 **[!UICONTROL Conditional formatting]** 으로 변경하면 값이 상한에 도달하면 셀이 더 푸르게 됩니다. 반면에, 그것이 더 낮은 한도에 도달한다면, 그것은 더 붉어질 것입니다.

예를 들어, 여기에서 을 500 **[!UICONTROL Upper limit]** 과 0 **[!UICONTROL Lower limit]** 으로 설정합니다.

![](assets/troubleshooting_2.png)

## 보고서에 N/A 값이 표시되는 이유는 무엇입니까?

![](assets/troubleshooting_3.png)

값 N/ **A** 가 동적 보고서에 나타나는 경우가 있습니다. 다음 두 가지 이유로 표시할 수 있습니다.

* 게재가 삭제되었으며 결과의 불일치를 초래하지 **않도록** 여기에 N/A로 표시됩니다.
* 차원을 **[!UICONTROL Transactional Delivery]** 보고서에 끌어다 놓으면 값 N/ **A** 가 결과로 나타날 수 있습니다. 이 문제는 동적 보고서가 트랜잭션 대상이 아닌 경우에도 모든 전달을 가져오기 때문에 발생합니다.
이 문제는 차원을 보고서에 끌어다 놓을 때에도 발생할 수 있지만 이 경우 **[!UICONTROL Delivery]** N/A **** 값이 거래 배달을 나타냅니다.
