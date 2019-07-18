---
title: 전송 날짜 계산
seo-title: 전송 날짜 계산
description: 전송 날짜 계산
seo-description: 특정 날짜와 시간에 메시지를 보내는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: fbbb 37 a 0-7257-4407-a 4 c 9-f 76 bf 04460 d 4
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: sheduling-messages
discoiquuid: 02 A 87 CC 6-C 40 C -44 FE-BB 4 E-B 68870 A 4859 B
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 28abc1e8aa31f3e0c7f09926f34a977d4c491fd8

---


# Computing the sending date{#computing-the-sending-date}

특정 날짜와 시간에 각 수신자에게 메시지를 보내는 공식을 정의할 수 있습니다.

## Customizing date formula {#customizing-date-formula}

예를 들어, 경사 등록 프로세스 중에 전송 시간 최적화를 사용할 수 있습니다.

새 플랫폼을 사용하여 이메일을 전송하는 경우 ISP (Internet Service Provider) 는 인식할 수 없는 IP 주소를 의심합니다. 대량의 이메일이 갑자기 전송되면 ISP는 이러한 이메일을 스팸으로 표시합니다.

스팸으로 표시되지 않도록 하려면 다양한 시간에 대량의 이메일을 배포하여 보낸 볼륨을 점진적으로 늘릴 수 있습니다. 이렇게 하면 초기 단계의 원활한 개발이 보장되고 잘못된 주소의 전체 속도를 줄일 수 있습니다.

예를 들어 타겟 대상을 무작위로 세그먼트화하여 배달을 5 개의 배치로 전송할 수 있습니다. 6 월 1 일 오전 10:00에 타겟 사용자의 10%를 나타내는 첫 번째 일괄 처리, 15%의 고객 중 15%를 포함하는 두 번째 일괄 처리 등을 전송합니다.

워크플로우를 사용하여 예약할 수 있습니다.

![](assets/send-time_opt_workflow1.png)

1. 마케팅 활동 목록에 액세스하고 새 워크플로우를 만듭니다. See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. **쿼리** 활동을 워크플로우로 드래그하여 놓고 엽니다. [쿼리](../../automating/using/query.md) 섹션을 참조하십시오.
1. Select an audience, for example all your Gold customers and click **[!UICONTROL Confirm]** to save the query.
1. **세그멘테이션** 활동을 워크플로우로 드래그하여 놓고 엽니다. [세그멘테이션](../../automating/using/segmentation.md) 섹션을 참조하십시오.
1. 5 개 세그먼트 정의 For each segment:

   * **[!UICONTROL Segment code]** 필드를 채웁니다. 메시지를 보낼 날짜와 시간을 수동으로 입력합니다.

      예를 들어 6 월 1 일 오전 10:00 GMT +1에 첫 번째 일괄 처리를 보낼 수 있습니다. Use the following format: **YYYY-MM-DD hh:mm:ss+tz**.

      ![](assets/send-time_opt_segment_configuration.png)

      To send the next batch the day after, enter **2017-06-02 10:00:00+01** for the second segment.

      나머지 세그먼트에 대해 다음과 같이 다음 배치를 정의합니다.

      * **2017-06-03 10:00:00+01**
      * **2017-06-04 10:00:00+01**
      * **2017-06-05 10:00:00+01**
   * Make sure you select the **[!UICONTROL Limit the population of this segment]** option.

      **[!UICONTROL Limitation]** 탭에서 각 **[!UICONTROL Random sampling]** 세그먼트에 대해 원하는 백분율을 선택하고 입력합니다. 첫 번째 묶음은 10 이고 두 번째 묶음은 15 입니다.

      ![](assets/send-time_opt_segment_limitation.png)


1. Once all segments are defined, select **[!UICONTROL Generate all segments in the same transition]** and click **[!UICONTROL Confirm]**.

   ![](assets/send-time_opt_segment_dates.png)

1. **이메일 전달** 활동을 워크플로우로 드래그하여 놓고 엽니다. [이메일 배달](../../automating/using/email-delivery.md) 섹션을 참조하십시오.
1. Click the **[!UICONTROL Schedule]** section in the email dashboard and select **[!UICONTROL Messages to be sent automatically on the date specified below]**.
1. **[!UICONTROL Start sending from]** 필드에서 연락처 날짜를 정의합니다.
1. From the send time optimization drop-down menu, choose **[!UICONTROL Send at a custom date defined by a formula]**.
1. Click the **[!UICONTROL Edit an expression]** button of the **[!UICONTROL Custom date formula]** field.

   ![](assets/send-time_opt_formula_define.png)

1. **[!UICONTROL ToDateTime]** 함수 및 **[!UICONTROL Segment code]** 필드를 사용하여 다음 표현식을 만듭니다. 표현식을 직접 입력할 수도 있지만 올바른 구문 및 철자를 사용해야 합니다.

   ```
   ToDateTime([targetData/@segmentCode])
   ```

   The **[!UICONTROL ToDateTime]** function transforms the segment code from a text string to a date and time value.

   이전 화면으로 돌아갈 표현식을 확인합니다.

   ![](assets/send-time_opt_formula_define_segment.png)

   **[!UICONTROL Schedule]** 창에서 사용자 지정 날짜 공식은 다음과 같이 표시됩니다.

   ```
   ToDateTime([targetData/@segmentCode])
   ```

   ![](assets/send-time_opt_custom_formula.png)

1. 일정을 확인하고 배달을 저장하고 워크플로우를 실행합니다.

배달이 5 일 이상 모든 타깃팅된 수신자에게 점진적으로 전송됩니다.

>[!NOTE]
>
>전송을 확인할 때 모든 날짜가 미래 상태인지 확인하십시오. 그렇지 않으면 전송이 확인되면 메시지가 전송됩니다.

## Using an expression {#using-an-expression}

전송 시간 최적화는 콜센터를 포함하는 캠페인에도 유용합니다. 모든 메시지가 동시에 수신되지 않도록 할 수 있습니다. 따라서 조직은 용량에 따라 호출 수를 처리할 수 있습니다.

예를 들어 프로모션 혜택을 받으려면 고객에게 콜센터에 문의하도록 초대하는 이메일을 보내주십시오. 콜 센터의 문제를 방지하려면 타겟 고객을 무작위로 세그먼트화하여 이메일을 4 개의 배치로 전송해야 합니다.

워크플로우를 사용하여 예약할 수 있습니다.

![](assets/send-time_opt_workflow2.png)

1. 마케팅 활동 목록에 액세스하고 새 워크플로우를 만듭니다. See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. **쿼리** 활동을 워크플로우로 드래그하여 놓고 엽니다. [쿼리](../../automating/using/query.md) 섹션을 참조하십시오.
1. Select an audience, for example over 35 profiles and click **[!UICONTROL Confirm]** to save the query.
1. **세그멘테이션** 활동을 워크플로우로 드래그하여 놓고 엽니다. [세그멘테이션](../../automating/using/segmentation.md) 섹션을 참조하십시오.
1. 네 개의 세그먼트를 정의합니다. For each segment:

   * 다음과 같이 세그먼트 코드를 정의합니다.

      * 8:00 AM - 10:00 AM: **0**. 메시지는 오전 8 시 (연락처 날짜) 에 대상 인구의 첫 번째 분기에 전송됩니다.
      * 10:00 AM - 12:00 PM: **2**. 메시지는 오전 10 시 (연락처 기준 + 2 시간) 에 Target 인구의 2 분기로 전송됩니다.
      * 2:00 PM - 4:00 PM: **6**. 콜 센터는 오후 12 시 ~ 오후 2:00 시 사이에 닫히고, 메시지가 오후 2:00 (연락처 날짜 + 6 시간) 에 타겟 인구의 3 분기로 전송됩니다.
      * 4:00 PM - 6:00 PM: **8**. 메시지는 오후 4:00 (연락처 날짜 + 8 시간) 에 대상 인구의 마지막 분기에 전송됩니다.
      >[!NOTE]
      >
      >연락처 날짜는 워크플로우에서 나중에 이메일 게재 활동에 정의됩니다.

   * Make sure you select the **[!UICONTROL Limit the population of this segment]** option.
   * **[!UICONTROL Limitation]** 탭에서 각 **[!UICONTROL Random sampling]** 세그먼트에 대해 원하는 백분율을 선택하고 입력합니다. **25.**


1. Once all segments are defined, select **[!UICONTROL Generate all segments in the same transition]** and click **[!UICONTROL Confirm]**.

   ![](assets/send-time_opt_segment.png)

1. **이메일 전달** 활동을 워크플로우로 드래그하여 놓고 엽니다. [이메일 배달](../../automating/using/email-delivery.md) 섹션을 참조하십시오.
1. Click the **[!UICONTROL Schedule]** section in the email dashboard.
1. **[!UICONTROL Messages to be sent automatically on the date specified below]** Select.
1. **[!UICONTROL Start sending from]** 필드에서 연락처 날짜를 정의합니다.

   이 예에서는 5 월 25 일을 오전 8 시에 선택합니다.

1. From the send time optimization drop-down menu, choose **[!UICONTROL Send at a custom date defined by a formula]** and click the **[!UICONTROL Edit an expression]** button.

   ![](assets/send-time_opt_formula_expression.png)

1. In the **[!UICONTROL Expression editor]**, set the date and the segment codes to compute the data for each customer.

   In the list of functions, select **[!UICONTROL AddHours]**.

   ![](assets/send-time_opt_formula_expression_addhours.png)

   In the available fields, select **[!UICONTROL Current delivery]** &gt; **[!UICONTROL Delivery scheduling]** &gt; **[!UICONTROL Contact date]**.

   ![](assets/send-time_opt_formula_expression_contact_date.png)

   This enables you to retrieve the date and time specified in the **[!UICONTROL Start sending from]** field.

   In the list of functions, select **[!UICONTROL ToInteger]**. In the available fields, select **[!UICONTROL Additional data]** &gt; **[!UICONTROL Segment code]**.

   ![](assets/send-time_opt_formula_expression_segment_code.png)

   세그먼트 코드에 지정된 숫자를 검색할 수 있습니다.

   다음 공식을 가져와야 합니다.

   ```
   AddHours([currentDelivery/scheduling/@contactDate], ToInteger([targetData/@segmentCode]))
   ```

1. 표현식을 저장했는지 확인합니다. 일정을 확인하고 배달을 저장하고 워크플로우를 실행합니다.

* 첫 번째 세그먼트는 연락처 날짜 (5 월 25 일 오전 8 시) 에 메시지를 받게 됩니다.
* 두 번째 세그먼트는 2 시간 후 (5 월 25 일 오전 10:00 시) 메시지를 받게 됩니다.
* 세 번째 세그먼트는 6 시간 후 (5 월 25 일 오후 2:00 시) 메시지를 받게 됩니다.
* 네 번째 세그먼트는 8 시간 후 (5 월 25 일 오후 4:00 시) 메시지를 받게 됩니다.

