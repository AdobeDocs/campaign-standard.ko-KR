---
title: 문제 해결
description: 다이내믹 보고와 관련된 일반적인 질문은 여기에서 찾을 수 있습니다.
audience: reporting
content-type: reference
topic-tags: troubleshooting
feature: Reporting
role: Leader
level: Intermediate
exl-id: 0f99a109-2923-4e64-8131-80fcacf79c82
source-git-commit: 8be43668d1a4610c3388ad27e493a689925dc88c
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 5%

---

# 문제 해결{#troubleshooting}

이 섹션에서는 동적 보고와 관련된 일반적인 질문을 확인할 수 있습니다.

## 고유 열기 및 고유 클릭 수의 경우 합계 행의 카운트가 개별 행의 카운트와 일치하지 않습니다 {#unique-open-clicks-no-match}

예상된 동작입니다.
다음 예를 들어 이 동작을 설명할 수 있습니다.

프로필 P1 및 P2에 이메일이 전송됩니다.

P1은 첫 번째 날에 두 번 이메일을 열고 두 번째 날에는 세 번 이메일을 엽니다.

반면 P2는 첫 날에 한 번 이메일을 열고 다음 날 다시 열지 않습니다.
다음은 보낸 이메일과 프로필의 상호 작용을 시각적으로 보여줍니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Day</strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기 수</strong> <br /> </th> 
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

고유한 전체 열기 수를 이해하려면 행 수를 합해야 합니다. **[!UICONTROL Unique Opens]** 3의 가치를 제공해줍니다. 그러나 이메일이 2개의 프로필만 타겟팅되었으므로 공개 비율은 150%를 표시해야 합니다.

100보다 높은 백분율을 얻지 않으려면 **[!UICONTROL Unique Opens]** 는 열려 있는 고유한 브로드로그 수로 유지됩니다. 이 경우 P1이 1일과 2일에 이메일을 열더라도 고유한 오픈은 1입니다.

이 경우 다음 테이블이 만들어집니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong></strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기 수</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong> Day </strong><br /> </td> 
   <td align="center"> <strong> 6 </strong><br /> </td> 
   <td align="center"> <strong> 2개</strong><br /> </td>
  </tr> 
  <tr> 
   <td align="center"> 1일<br /> </td> 
   <td align="center"> 3<br /> </td> 
   <td align="center"> 2<br /> </td>
  </tr> 
  <tr> 
   <td align="center"> 2일<br /> </td> 
   <td align="center"> 3<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하며, 이로 인해 큰 카운트에서 약간 정확하지 않을 수 있습니다.

## 열린 카운트가 데이터베이스 수와 일치하지 않습니다. {#open-counts-no-match-database}

이는 추론을 추적할 수 없는 경우에도 동적 보고에서 열기를 추적하기 위해 추론을 사용했기 때문일 수 있습니다 **[!UICONTROL Open]** 작업.

예를 들어, 사용자가 클라이언트의 이미지를 비활성화하고 이메일의 링크를 클릭한 경우, **[!UICONTROL Open]** 데이터베이스에 의해 추적되지 않지만 **[!UICONTROL Click]** 합니다.

따라서, **[!UICONTROL Open]** 추적 로그 카운트는 데이터베이스에서 동일한 수를 가질 수 없습니다.

이러한 항목은 다음과 같이 추가됩니다. **&quot;이메일 클릭은 이메일을 열었다는 것을 의미합니다.&quot;**.

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하므로 카운트 간의 작은 불일치를 경험할 수 있습니다.

## 반복/트랜잭션 게재에 대한 수는 어떻게 계산됩니까? {#counts-recurring-deliveries}

반복 및 트랜잭션 게재 작업 시 카운트는 상위 및 하위 게재 모두에 귀속됩니다.
라는 반복 게재의 예를 들어볼 수 있습니다 **R1** 근무일 1(RC1), 근무일 2(RC2) 및 근무일 3(RC3)에서 매일 실행되도록 설정합니다.
한 사람만 모든 하위 게재를 여러 번 열었다고 가정해 보겠습니다. 이 경우 개별 반복 하위 게재에 **[!UICONTROL Open]** 각각 1로 카운트합니다.
그러나 동일한 사람이 모든 게재를 클릭했으므로 상위 반복 게재도 이러한 결과를 초래할 수 있습니다 **[!UICONTROL Unique open]** 로서의 1.

보고서는 다음과 같습니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>게재</strong> <br /> </th> 
   <th align="center"> <strong>전송</strong> <br /> </th> 
   <th align="center"> <strong>배달됨</strong> <br /> </th>
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기 수</strong> <br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1</strong><br/> </td> 
   <td align="center"> <strong>100년</strong><br/> </td> 
   <td align="center"> <strong>90</strong><br/> </td> 
   <td align="center"> <strong>10</strong><br/> </td> 
   <td align="center"> <strong>3</strong><br/> </td> 
  </tr> 
  <tr> 
   <td align="center"> RC1<br/> </td> 
   <td align="center"> 20년<br /> </td> 
   <td align="center"> 20년<br /> </td> 
   <td align="center"> 6<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr>
    <tr> 
   <td align="center"> RC2<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 30<br /> </td> 
   <td align="center"> 2개<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
    <tr> 
   <td align="center"> RC3<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 40<br /> </td> 
   <td align="center"> 2개<br /> </td> 
   <td align="center"> 1<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 보고서 테이블에 있는 색상은 무엇입니까? {#reports-color-signification}

보고서에 표시되는 색상은 무작위화되므로 개인화할 수 없습니다. 진행률 표시줄을 표시되며 보고서에 도달하는 최대 값을 더 잘 강조 표시하는 데 도움이 됩니다.

아래 예제에서 셀은 값이 100%이므로 색상이 동일합니다.

![](assets/troubleshooting_1.png)

만약 **[!UICONTROL Conditional formatting]** 사용자 지정을 위해 값이 상한에 도달하면 셀이 더 푸르게 됩니다. 반면에, 그것이 더 낮은 제한에 도달한다면, 그것은 더 낮아질 것입니다.

예를 들어, 여기서는 **[!UICONTROL Upper limit]** 및 **[!UICONTROL Lower limit]** 0.

![](assets/troubleshooting_2.png)

## 내 보고서에 값 N/A가 표시되는 이유는 무엇입니까?

![](assets/troubleshooting_3.png)

값 **해당 없음** 은 때로 동적 보고서에 나타날 수 있습니다. 다음 세 가지 이유로 표시될 수 있습니다.

* 게재가 삭제되었으며 다음과 같이 표시됩니다. **해당 없음** 결과에 불일치가 발생하지 않도록 합니다.
* 을(를) 끌어다 놓을 때 **[!UICONTROL Transactional Delivery]** 차원 값을 보고서에 추가합니다. **해당 없음** 결과로 나타날 수 있습니다. 이 문제는 동적 보고서가 트랜잭션이 아닌 경우에도 모든 게재를 가져오기 때문에 발생합니다. 드래그 앤 드롭할 때도 이 문제가 발생할 수 있습니다 **[!UICONTROL Delivery]** 차원 을 보고서에 추가하지만 이 경우 **해당 없음** 값은 트랜잭션 게재를 나타냅니다.
* 차원과 관련이 없는 지표와 함께 차원을 사용하는 경우. 아래 예에서는 분류가 **[!UICONTROL Tracking URL]** 차원 **[!UICONTROL Click]** 이 게재에서 카운트가 0으로 설정됩니다.

   ![](assets/troubleshooting_4.png)

