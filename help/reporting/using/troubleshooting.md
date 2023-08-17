---
title: 동적 보고 문제 해결
description: 다이내믹 보고와 관련된 일반적인 질문을 여기에서 확인하십시오.
audience: reporting
content-type: reference
topic-tags: troubleshooting
feature: Reporting
role: Leader
level: Intermediate
exl-id: 0f99a109-2923-4e64-8131-80fcacf79c82
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 5%

---

# 문제 해결{#troubleshooting}

이 섹션에서는 동적 보고와 관련된 일반적인 질문을 확인할 수 있습니다.

## 고유 열람 수 및 고유 클릭 수의 경우 집계 행의 개수가 개별 행의 개수와 일치하지 않습니다 {#unique-open-clicks-no-match}

이는 예상되는 비헤이비어입니다.
다음 예를 들어 이 동작을 설명할 수 있습니다.

프로필 P1 및 P2로 이메일이 전송됩니다.

P1은 첫 번째 날에 이메일을 두 번 연 다음 두 번째 날에 세 번 엽니다.

반면 P2는 첫 번째 날에 이메일을 한 번 열고 다음 날 다시 열지 않습니다.
다음은 전송된 이메일에 대한 프로필의 상호 작용을 시각적으로 표현한 것입니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>Day</strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 오픈</strong> <br /> </th> 
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

고유 열람 수를 전체적으로 파악하려면 행 수를 합해야 합니다 **[!UICONTROL Unique Opens]** 3 값을 제공합니다. 그러나 이메일이 2개의 프로필로만 타겟팅되었으므로 공개 비율은 150%로 표시되어야 합니다.

100보다 큰 백분율을 구하지 않으려면 **[!UICONTROL Unique Opens]** 열려 있는 고유한 브로드로그 수로 유지됩니다. 이 경우 P1이 1일과 2일에 이메일을 열었더라도 고유한 열림은 여전히 1입니다.

이렇게 하면 다음 테이블이 표시됩니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong></strong> <br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 오픈</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong> Day </strong><br /> </td> 
   <td align="center"> <strong> 6 </strong><br /> </td> 
   <td align="center"> <strong> 2</strong><br /> </td>
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
>고유 개수는 HLL 기반 스케치를 기반으로 하며, 이는 큰 개수에서 약간의 부정확성을 야기할 수 있습니다.

## 열린 수가 데이터베이스 수와 일치하지 않습니다. {#open-counts-no-match-database}

이는 추론을 추적할 수 없는 경우에도 열림을 추적하기 위해 동적 보고에서 추론이 사용되기 때문일 수 있습니다. **[!UICONTROL Open]** 작업.

예를 들어 사용자가 클라이언트에서 이미지를 비활성화하고 이메일의 링크를 클릭하면 **[!UICONTROL Open]** 데이터베이스에서 추적할 수 없지만 **[!UICONTROL Click]** 윌.

따라서 **[!UICONTROL Open]** 추적 로그 수는 데이터베이스에서 동일한 수를 가질 수 없습니다.

이러한 발생 횟수는 다음과 같이 추가됩니다. **&quot;이메일 클릭은 이메일 열기를 의미합니다.&quot;**.

>[!NOTE]
>
>고유 카운트는 HLL 기반 스케치를 기반으로 하므로 카운트 간 사소한 불일치가 발생할 수 있습니다.

## 반복/트랜잭션 게재의 카운트는 어떻게 계산됩니까? {#counts-recurring-deliveries}

반복 및 트랜잭션 게재로 작업할 때 카운트는 상위 및 하위 게재 모두에 연결됩니다.
라는 이름의 반복 게재의 예를 사용할 수 있습니다. **R1** 1일(RC1), 2일(RC2) 및 3일(RC3)에 매일 실행되도록 설정합니다.
한 사람만 모든 하위 분만을 여러 번 열었다고 가정해 보겠습니다. 이 경우 개별 반복 하위 게재에 표시되는 항목은 다음과 같습니다. **[!UICONTROL Open]** 각각에 대해 1로 계산합니다.
그러나 동일한 사람이 모든 게재를 클릭했으므로 상위 반복 게재에도 다음이 적용됩니다. **[!UICONTROL Unique open]** as 1.

보고서는 다음과 같아야 합니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>게재</strong> <br /> </th> 
   <th align="center"> <strong>전송됨</strong> <br /> </th> 
   <th align="center"> <strong>전달됨</strong> <br /> </th>
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 오픈</strong> <br /> </th>
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td align="center"> <strong>R1</strong><br/> </td> 
   <td align="center"> <strong>100</strong><br/> </td> 
   <td align="center"> <strong>90</strong><br/> </td> 
   <td align="center"> <strong>10</strong><br/> </td> 
   <td align="center"> <strong>3</strong><br/> </td> 
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

## 내 보고서 테이블에 있는 색깔의 의미는 무엇입니까? {#reports-color-signification}

보고서에 표시된 색상은 임의화되어 개인화할 수 없습니다. 진행률 표시줄을 나타내며 보고서에 도달한 최대 값을 더 잘 강조 표시할 수 있도록 표시됩니다.

아래 예에서 셀의 값은 100%이므로 셀의 색상은 동일합니다.

![](assets/troubleshooting_1.png)

을(를) 변경하면 **[!UICONTROL Conditional formatting]** 사용자 지정의 경우 값이 상한에 도달하면 셀이 더 커집니다. 반면, 하한에 도달하면 더 붉어집니다.

예를 들어 여기서는 를 **[!UICONTROL Upper limit]** ~ 500 및 **[!UICONTROL Lower limit]** 을 0으로 설정합니다.

![](assets/troubleshooting_2.png)

## 보고서에 N/A 값이 표시되는 이유는 무엇입니까?

![](assets/troubleshooting_3.png)

값 **해당 사항 없음** 동적 보고서에 표시될 수 있습니다. 다음과 같은 세 가지 이유로 표시될 수 있습니다.

* 게재가 삭제되고 여기에 (으)로 표시됩니다. **해당 사항 없음** 결과에 불일치를 일으키지 않도록.
* 을(를) 끌어다 놓을 때 **[!UICONTROL Transactional Delivery]** 보고서에 차원, 값 **해당 사항 없음** 결과로 나타날 수 있습니다. 이 문제는 동적 보고서가 트랜잭션이 아닌 경우에도 모든 게재를 가져오기 때문에 발생합니다. 이 문제는 을(를) 끌어서 놓을 때도 발생할 수 있습니다 **[!UICONTROL Delivery]** 보고서에 대한 차원이지만 이 경우 **해당 사항 없음** 값은 트랜잭션 게재를 나타냅니다.
* 차원이 차원과 관련이 없는 지표와 함께 사용되는 경우. 아래 예에서는 분류가 **[!UICONTROL Tracking URL]** 차원이지만 **[!UICONTROL Click]** 이 게재에서 count는 0으로 설정됩니다.

  ![](assets/troubleshooting_4.png)

## 사용자 지정 대상 매핑을 사용할 때 게재 보고서에 불완전한 데이터가 표시됨

게재에서 가져온 사용자 지정 대상 매핑을 사용하고 다른 보고서에 데이터가 표시되지 않는 경우 해당 대상 매핑에 대한 보고 보강이 생성되지 않았을 수 있습니다.

이 문제를 해결하려면

* XML에서 Target 매핑을 가져온 후 보고 데이터 보강 또한 가져와야 합니다.

* Target 매핑을 가져오는 대신 Adobe Campaign Standard에서 직접 만들어 보고 데이터 보강 기능을 자동으로 만들 수 있습니다.
