---
title: 문제 해결
description: 다이내믹 보고 관련 일반적인 질문을 살펴보십시오.
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
source-git-commit: 001fc2df11e32bdcc31dfe917884460b4d3de541

---


# 문제 해결{#troubleshooting}

이 섹션에서는 동적 보고 관련 일반적인 질문을 찾을 수 있습니다.

## 고유 열기 및 고유 클릭 수의 경우 집계 행의 카운트가 개별 행의 카운트와 일치하지 않습니다 {#unique-open-clicks-no-match}

이는 예상 동작입니다.
다음 예를 통해 이러한 행동을 설명할 수 있습니다.

프로필 P1 및 P2로 이메일이 전송됩니다.

P1은 첫 번째 날에 두 번 이메일을 열고 두 번째 날에 세 번 이메일을 엽니다.

반면에 P2는 첫 날에 이메일을 한 번 열고 다음 날 다시 열지 않습니다.
전송된 이메일과 프로필의 상호 작용을 시각적으로 보여줍니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>일</strong><br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th> 
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

전체 고유 열기 수를 이해하려면 값 3을 **[!UICONTROL Unique Opens]** 제공하는 행 카운트를 합산해야 합니다. 그러나 이메일이 2개의 프로필만 대상으로 작성되었으므로 공개 비율은 150%로 표시되어야 합니다.

100보다 높은 백분율을 획득하지 **[!UICONTROL Unique Opens]** 않도록 의 정의는 열린 고유 브로드로그 수로 유지됩니다. 이 경우, P1이 1일과 2일에 이메일을 열더라도, 그의 고유 열기는 여전히 1입니다.

그러면 다음 표가 나타납니다.

<table> 
 <thead> 
  <tr> 
   <th align="center"> <strong>일</strong><br /> </th> 
   <th align="center"> <strong>열어 본 기록</strong> <br /> </th> 
   <th align="center"> <strong>고유 열기</strong><br /> </th> 
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
>고유 카운트는 HLL 기반 스케치를 기반으로 하므로 큰 스케치에서 약간 부정확할 수 있습니다.

## 열린 카운트가 데이터베이스 수와 일치하지 않습니다. {#open-counts-no-match-database}

이는 동작을 추적할 수 없을 때에도 열림 추적을 추적하기 위해 동적 보고에 추론이 사용되기 때문일 수 **[!UICONTROL Open]** 있습니다.

예를 들어, 사용자가 클라이언트에서 이미지를 비활성화하고 이메일의 링크를 클릭하는 경우, 데이터베이스가 **[!UICONTROL Open]** 아니라 **[!UICONTROL Click]** 의도할 것입니다.

따라서 **[!UICONTROL Open]** 추적 로그 카운트는 데이터베이스에 동일한 카운트가 없을 수 있습니다.

이러한 항목은 **&quot;이메일 클릭은 이메일 열기를 의미합니다&quot;**.

>[!NOTE]
>
>고유 수는 HLL 기반 스케치를 기반으로 하므로 카운트 간의 사소한 불일치를 경험할 수 있습니다.

## 보고서 테이블의 색상 표시는 무엇입니까? {#reports-color-signification}

보고서에 표시되는 색상은 무작위 지정되므로 개인화할 수 없습니다. 진행률 표시줄을 나타내며 보고서에서 도달한 최대값을 더 잘 강조 표시할 수 있도록 표시됩니다.

아래 예에서 셀의 값은 100%이기 때문에 셀은 같은 색입니다.

![](assets/troubleshooting_1.png)

사용자 **[!UICONTROL Conditional formatting]** 지정으로 변경하면 값이 상한에 도달하면 셀이 더 푸르게 됩니다. 반면에, 그것이 더 낮은 제한에 도달하면, 더 붉어질 것입니다.

예를 들어 여기에서 500과 0 **[!UICONTROL Upper limit]** 으로 **[!UICONTROL Lower limit]** 설정합니다.

![](assets/troubleshooting_2.png)

## 내 보고서에 N/A 값이 표시되는 이유는 무엇입니까?

![](assets/troubleshooting_3.png)

값 N/ **A** 값이 동적 보고서에 나타나는 경우가 있습니다. 다음 두 가지 이유로 표시할 수 있습니다.

* 게재가 삭제되었으며 결과에 불일치가 발생하지 않도록 **N/A로** 여기에 표시됩니다.
* 차원을 **[!UICONTROL Transactional Delivery]** 보고서에 끌어다 놓으면 값 N/ **A** 가 결과로 나타날 수 있습니다. 이 문제는 다이내믹 보고서가 트랜잭션 대상이 아닌 경우에도 모든 전달을 가져오기 때문에 발생합니다.
이 문제는 **[!UICONTROL Delivery]** 차원을 보고서에 끌어다 놓을 때에도 발생할 수 있지만 이 경우 N/A **값이 트랜잭션 배달을** 나타냅니다.
