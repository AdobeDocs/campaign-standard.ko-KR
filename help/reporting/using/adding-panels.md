---
solution: Campaign Standard
product: campaign
title: 패널 추가
description: 동적 보고서를 사용하면 선택한 기간에 따라 패널을 추가하여 데이터를 보다 효과적으로 필터링할 수 있습니다.
audience: reporting
content-type: reference
topic-tags: customizing-reports
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 패널 추가{#adding-panels}

## 빈 패널 {#adding-a-blank-panel} 추가

보고서를 시작하려면 패널 세트를 즉시 사용하거나 사용자 지정 보고서에 추가할 수 있습니다. 각 패널은 서로 다른 데이터 세트를 포함하며 자유 형식 테이블 및 시각화로 구성됩니다.

이 패널에서는 필요에 따라 보고서를 작성할 수 있습니다. 기간이 다른 데이터를 필터링하기 위해 보고서에 원하는 만큼 패널을 추가할 수 있습니다.

1. **패널** 아이콘을 클릭합니다. **삽입 탭**&#x200B;을 클릭하고 **새 빈 패널**&#x200B;을 선택하여 패널을 추가할 수도 있습니다.

   ![](assets/dynamic_report_panel_1.png)

1. **빈 패널**&#x200B;을 대시보드로 드래그하여 놓습니다.

   ![](assets/dynamic_report_panel.png)

이제 패널에 자유 형식 테이블을 추가하여 데이터 타깃팅을 시작할 수 있습니다.

## 자유 형식 테이블 {#adding-a-freeform-table} 추가

자유 형식 테이블을 사용하면 **구성 요소** 테이블에서 사용할 수 있는 다른 지표와 차원을 사용하여 데이터를 분석할 테이블을 만들 수 있습니다.

각 테이블 및 시각화는 크기 조정이 가능하며, 보고서를 더 잘 사용자 정의하도록 이동할 수 있습니다.

1. **패널** 아이콘을 클릭합니다.

   ![](assets/dynamic_report_panel_1.png)

1. **자유 형식** 항목을 대시보드에 드래그하여 놓습니다.

   **삽입** 탭을 클릭하고 **새 자유 형식**&#x200B;을 선택하거나 빈 패널에서 **자유 형식 테이블 추가**&#x200B;를 클릭하여 표를 추가할 수도 있습니다.

   ![](assets/dynamic_report_panel_2.png)

1. 기본적으로 **[!UICONTROL Exclude proof]** 세그먼트가 이미 선택되어 있습니다. 필요한 경우 **[!UICONTROL Components]** 탭에서 **[!UICONTROL Segments]** 중 하나를 맨 위 막대로 드래그하여 놓아 변경할 수 있습니다.

   ![](assets/dynamic_report_panel_3.png)

1. **구성 요소** 탭의 항목을 열 및 행으로 드래그하여 테이블을 만듭니다.

   ![](assets/dynamic_report_freeform_3.png)

1. **설정** 아이콘을 클릭하여 데이터가 열에 표시되는 방식을 변경합니다.

   ![](assets/dynamic_report_freeform_4.png)

   **[!UICONTROL Column settings]**&#x200B;은(는) 다음 항목으로 구성됩니다.

   * **[!UICONTROL Number]**:열에 요약 번호를 표시하거나 숨길 수 있습니다.
   * **[!UICONTROL Percent]**:열에 백분율을 표시하거나 숨길 수 있습니다.
   * **[!UICONTROL Interpret zero as no value]**:값이 0인 경우를 표시하거나 숨길 수 있습니다.
   * **[!UICONTROL Background]**:셀에서 가로 진행률 표시줄을 표시하거나 숨길 수 있습니다.
   * **[!UICONTROL Include retries]**:결과에 재시도를 포함시킬 수 있습니다. 이 값은 **[!UICONTROL Sent]** 및 **[!UICONTROL Bounces + Errors]**&#x200B;에만 사용할 수 있습니다.

1. 하나 이상의 행을 선택하고 **Visualize** 아이콘을 클릭합니다. 선택한 행을 반영하도록 시각화가 추가됩니다.

   ![](assets/dynamic_report_freeform_5.png)

이제 필요한 만큼 구성 요소를 추가하고 시각화를 추가하여 데이터를 그래픽으로 나타낼 수 있습니다.
