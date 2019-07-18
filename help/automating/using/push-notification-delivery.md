---
title: 푸시 알림 전달
seo-title: 푸시 알림 전달
description: 푸시 알림 전달
seo-description: 푸시 알림 전송 활동을 통해 워크플로우에서 단일 전송 푸시 알림 또는 반복되는 푸시 알림을 구성할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 994 D 8 FE 3-29 F 0-4 B 5 C -89 EE-C 6 BE 7 C 60 A 31 B
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 채널 활동
discoiquuid: E 61 BDAEE -4 B 48-4845-A 2 A 5-574 B 577 EA 796
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 36727e82d3aa73add6116fa2916752ff0e407d9d

---


# Push notification delivery{#push-notification-delivery}

## Description {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

**[!UICONTROL Push notification]** 활동을 통해 워크플로우에서 푸시 알림 전송을 구성할 수 있습니다. This can be a **single send** notification and sent just once, or it can be a **recurring** notification.

단일 전송 알림은 한 번 전송되는 표준 모바일 앱 푸시 알림 배달입니다.

반복 알림을 사용하면 정의된 기간 동안 동일한 모바일 앱 푸시 알림 배달을 다른 대상에 여러 번 보낼 수 있습니다. 필요에 따라 보고서를 받을 수 있도록 기간별로 배달을 집계할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Push notification]** 활동은 일반적으로 동일한 워크플로우에서 계산된 타겟에 대한 알림을 자동화하는 데 사용됩니다.

스케줄러에 연결된 경우 반복되는 푸시 알림을 정의할 수 있습니다.

받는 사람은 쿼리, 교차로 등의 타깃팅 활동을 통해 동일한 워크플로우에서 활동 업스트림 정의됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 수동 확인을 요청할지 여부를 선택할 수 있습니다 (기본적으로 필수). 워크플로우를 수동으로 시작하거나 워크플로우에서 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

## Configuration {#configuration}

1. **[!UICONTROL Push notification]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.

   >[!NOTE]
   >
   >You can access the general properties and advanced options of the activity (and not of the delivery itself) via the ![](assets/dlv_activity_params-24px.png) button from the activity's quick actions. This button is specific to the **[!UICONTROL Push notification]** activity. 푸시 알림의 속성은 푸시 대시보드의 작업 표시줄을 통해 액세스할 수 있습니다.

1. 푸시 알림 전송 모드를 선택합니다.

   * **[!UICONTROL Single notification]**: 푸시 알림은 한 번만 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 이 절차의 7 단계에서는 서로 다른 전환 유형을 자세히 설명합니다.
   * **[!UICONTROL Recurring notification]**: 활동에 정의된 빈도에 따라 푸시 알림이 여러 번 **[!UICONTROL Scheduler]** 전송됩니다. 전송 집계 기간을 선택합니다. This allows you to regroup all the sends that occur during the defined period in one single push notification that is also called **recurring execution** and can be accessed from the application's marketing activity list.

      예를 들어 매일 전송되는 반복 생일 알림의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 따라서 매일 알림이 전송되더라도 월별 배송 시 보고서를 받을 수 있습니다.

1. 알림 유형을 선택합니다. These types come from push notifications templates defined in the **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** menu.
1. 푸시 알림에 대한 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 배달 활동 레이블이 푸시 알림 레이블로 업데이트됩니다.
1. 푸시 알림 내용을 정의합니다. See [Creating a push notification](../../channels/using/preparing-and-sending-a-push-notification.md)
1. By default, the **[!UICONTROL Push notification]** activity does not include any outbound transitions. **[!UICONTROL Push Notification]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션 **[!UICONTROL General]** 탭 (활동의 빠른 작업에 있는 ![](assets/dlv_activity_params-24px.png) 단추) 로 이동한 후 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 이를 통해 인바운드 전환과 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**: 이렇게 하면 알림이 전송된 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 게재 준비 중에 제외된 대상의 구성원은 이 전환 작업에서 제외됩니다.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 푸시 알림 대시보드로 바로 이동됩니다. 해당 컨텐트만 편집할 수 있습니다.

기본적으로 배달 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우에서 만든 메시지 전송은 워크플로우가 시작된 후에도 여전히 확인해야 합니다. But from the message dashboard, and only if the message was created from a workflow, you can disable the **[!UICONTROL Request confirmation before sending messages]** option. 이 옵션을 선택 해제하면 준비가 완료되면 추가 통지 없이 메시지가 전송됩니다.

## Remarks {#remarks}

워크플로우 내에서 만들어진 게시는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 푸시 알림 요약 창의 링크를 사용하여 연결된 요소 (워크플로우, 캠페인 등) 에 직접 액세스할 수 있습니다.

In the parent deliveries, which can be accessed from the marketing activity list, you can view the total number of sends that have been processed (according to the aggregation period specified when the **[!UICONTROL Push notification]** activity was configured). To do this, open the detail view of the parent delivery's **[!UICONTROL Deployment]** block by selecting ![](assets/wkf_dlv_detail_button.png).

## Sending a recurring push notification with a workflow {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

이 경우, 개인화된 푸시 알림은 오후 8 시 마다 해당 시간대에 따라 모바일 애플리케이션의 가입자에게 발송됩니다. 이렇게 하려면:

1. **[!UICONTROL Scheduler]** 활동을 사용하면 배달이 시작되기 전에 워크플로우 일수를 시작하여 지정된 시간대의 오후 8 시에 모든 구독자에게 알림을 보낼 수 있습니다.

   * **[!UICONTROL Execution frequency]** 필드에서 [월별] 를 선택합니다.
   * **[!UICONTROL Time]** 필드에서 오후 8 시를 선택합니다.
   * 배달이 매월 전송될 날짜를 선택합니다.
   * 배달을 시작하기 최소 1 일 전에 워크플로우의 시작 날짜를 선택합니다. 그렇지 않으면 선택한 시간이 이미 해당 시간대에서 전달된 경우 일부 수신자에게 다음날 메시지를 받을 수 있습니다.
   * **[!UICONTROL Execution options]** 탭에서 워크플로우가 **[!UICONTROL Time zone]** 시작되는 시간대를 선택합니다. 예를 들어, 워크플로우는 태평양 표준시 오후 8 시 (태평양 표준시 기준) 에 시작하여 해당 시간대가 모든 해당 시간대에 대해 생성되기까지 어느 정도 시간이 소요됩니다.
   ![](assets/wkf_push_example_5.png)

1. **쿼리** 활동을 통해 모바일 애플리케이션을 구독하고 사용자가 보낸 이메일을 열지 않은 20-30 세 사이의 VIP 고객을 타깃팅할 수 있습니다.

   * 대상 (VIP 고객) 를 선택하고 해당 연령대에서 필터링합니다.
   * Drag and drop the **Subscriptions to an application** element into the workspace. **존재함을** 선택하고 사용할 모바일 애플리케이션을 선택합니다.
   * 고객에게 보낸 이메일을 선택합니다.
   * **배달 로그 (로그)** 요소를 작업 공간으로 드래그하여 놓고 **이메일을** 받은 모든 고객을 타깃팅하려면 [존재함] 를 선택합니다.
   * **추적 로그 (추적)** 요소를 작업 공간으로 드래그하여 놓고 [존재하지 **않음] 를 선택하여** 이메일을 열지 않은 모든 고객을 타깃팅합니다.

      ![](assets/wkf_push_example_2.png)

1. **푸시 알림** 활동에서는 메시지 컨텐트를 입력하고 사용할 개인화 필드를 선택할 수 있습니다.

   * **[!UICONTROL Recurring notification]** 옵션을 선택합니다.
   * 푸시 알림 내용을 정의합니다. For more information on push notification content, refer to this [section](../../channels/using/preparing-and-sending-a-push-notification.md).
   * **[!UICONTROL Schedule]** 블록에서 **[!UICONTROL Messages to be sent automatically on the time zone specified below]**&#x200B;를 선택합니다. Here, we chose the **[!UICONTROL Time zone of the contact date]** Pacific as in the workflow **[!UICONTROL Scheduler]**.
   * **[!UICONTROL Optimize the sending time per recipient]** 필드에서 **[!UICONTROL Send at the recipient's time zone]**&#x200B;를 선택합니다.

      ![](assets/wkf_push_example_4.png)

1. **[!UICONTROL Start]** 단추를 클릭하여 반복되는 워크플로우를 시작합니다.

   ![](assets/wkf_push_example_3.png)

워크플로우가 실행 중입니다. It will start at the chosen start date of the **[!UICONTROL Scheduler]** at 8 pm Pacific time, the recurring push will then be sent every first day of the month at 8 pm depending on the customers time zone.
