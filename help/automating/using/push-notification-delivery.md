---
title: 푸시 알림 게재
description: 푸시 알림 배달 활동을 사용하면 워크플로우에서 단일 푸시 알림 또는 반복 푸시 알림을 전송하도록 구성할 수 있습니다.
page-status-flag: never-activated
uuid: 994d8fe3-29f0-4b5c-89ee-c6be7c60a31b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: e61bdaee-4b48-4845-a2a5-574b577ea796
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: accc382ca1543d648e60d53cab338537fd9ea3ef

---


# 푸시 알림 게재{#push-notification-delivery}

## 설명 {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

이 **[!UICONTROL Push notification]**활동을 통해 워크플로우에서 푸시 알림 전송을 구성할 수 있습니다. 이는**&#x200B;단일 전송&#x200B;**알림일 수 있으며 한 번만 전송되거나**&#x200B;반복되는&#x200B;**알림일 수 있습니다.

단일 전송 알림은 표준 모바일 앱 푸시 알림 배달이며 한 번 전송됩니다.

반복 알림을 사용하면 지정된 기간 동안 동일한 모바일 앱 푸시 알림 전송을 여러 번 다른 타겟으로 전송할 수 있습니다. 필요에 해당하는 보고서를 가져오려면 기간당 납품을 집계할 수 있습니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Push notification]**활동은 일반적으로 동일한 워크플로우에서 계산된 타겟으로 알림 전송을 자동화하는 데 사용됩니다.

스케줄러에 연결할 때 반복되는 푸시 알림을 정의할 수 있습니다.

수신자는 쿼리, 교차로 등과 같은 타깃팅 활동을 통해 동일한 워크플로에서 활동의 업스트림으로 정의됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 수동 확인을 요청할지 여부를 선택할 수 있습니다(기본적으로 필수). 워크플로우를 수동으로 시작하거나 워크플로우에 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Push notification]**놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.

   >[!NOTE]
   >
   >활동의 빠른 작업의 ![](assets/dlv_activity_params-24px.png) 단추를 통해 배달 자체가 아닌 활동의 일반 속성 및 고급 옵션에 액세스할 수 있습니다. 이 단추는 **[!UICONTROL Push notification]**활동에 따라 다릅니다. 푸시 알림의 속성은 푸시 대시보드의 작업 표시줄을 통해 액세스할 수 있습니다.

1. 푸시 알림 전송 모드를 선택합니다.

   * **[!UICONTROL Single notification]**:푸시 알림이 한 번 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 이 절차의 7단계에서 다양한 전환 유형에 대해 자세히 설명합니다.
   * **[!UICONTROL Recurring notification]**:푸시 알림은**[!UICONTROL Scheduler]** 활동에 정의된 빈도에 따라 여러 번 전송됩니다. 전송의 집계 기간을 선택합니다. 이를 통해 **반복 실행이라고 하며 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있는 단일 푸시 알림에서 정의된 기간 동안 발생하는 모든 전송을** 다시 그룹화할 수 있습니다.

      예를 들어 매일 전송되는 반복 생일 알림의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 이렇게 하면 알림을 매일 보내더라도 매월 배달 보고서를 받을 수 있습니다.

1. 알림 유형을 선택합니다. 이러한 유형은 **[!UICONTROL Resources]**>**[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**메뉴에 정의된 푸시 알림 템플릿에서 가져옵니다.
1. 푸시 알림의 일반 속성을 입력합니다. 기존 캠페인에 연결할 수도 있습니다. 워크플로우의 배달 활동의 레이블은 푸시 알림 레이블로 업데이트됩니다.
1. 푸시 알림 컨텐츠를 정의합니다. 푸시 [알림 만들기를 참조하십시오.](../../channels/using/preparing-and-sending-a-push-notification.md)
1. 기본적으로 이 **[!UICONTROL Push notification]**활동에는 아웃바운드 전환이 포함되지 않습니다. 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션(활동의 빠른 동작에 있는**[!UICONTROL Push Notification]** 단추)의 **[!UICONTROL General]**![](assets/dlv_activity_params-24px.png)탭으로 이동한 다음 다음 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**:이를 통해 인바운드 전환과 정확히 동일한 인구를 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**:이렇게 하면 알림을 받은 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 배달 준비 중에 제외된 대상의 멤버는 이 전환에서 제외됩니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 푸시 알림 대시보드로 바로 이동합니다. 컨텐트만 편집할 수 있습니다.

기본적으로 배달 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우가 시작된 후에도 워크플로우에서 만든 메시지 전송을 확인해야 합니다. 그러나 메시지 대시보드에서 메시지를 만든 경우에만 **[!UICONTROL Request confirmation before sending messages]**옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료되면 추가 통보 없이 메시지가 전송됩니다.

## 주의 사항 {#remarks}

워크플로우 내에서 생성된 게재는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 푸시 알림 요약 창의 링크를 사용하면 연결된 요소(워크플로우, 캠페인 등)에 직접 액세스할 수 있습니다.

마케팅 활동 목록에서 액세스할 수 있는 상위 배달에서 처리된 총 전송 수를 볼 수 있습니다(활동이 구성될 때 지정된 집계 기간에 따라). **[!UICONTROL Push notification]**이렇게 하려면 상위 배달**[!UICONTROL Deployment]** 블록의 세부 사항 보기를 선택하여 엽니다 ![](assets/wkf_dlv_detail_button.png).

## 워크플로우로 반복 푸시 알림 보내기 {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

이 예에서, 개인화된 푸시 알림은 시간대에 따라 매월 1일 오후 8시에 모바일 애플리케이션 가입자에게 전송됩니다. 이렇게 하려면:

1. 이 **[!UICONTROL Scheduler]**활동을 사용하면 배달을 시작하기 전 워크플로우 일수를 시작하여 지정된 시간대의 오후 8시에 모든 가입자에게 알림을 전송할 수 있습니다.

   * 필드에서 **[!UICONTROL Execution frequency]**[월별]을 선택합니다.
   * 필드에서 오후 8시를 **[!UICONTROL Time]**선택합니다.
   * 매달 배달되는 날짜를 선택합니다.
   * 워크플로우의 시작 날짜를 하나 이상 먼저 선택합니다. 그렇지 않으면 선택한 시간이 이미 시간대에서 경과된 경우 일부 받는 사람이 하루 후에 메시지를 받을 수 있습니다.
   * 탭에서 **[!UICONTROL Execution options]**필드에서 워크플로우가 시작될 시간대를 선택합니다**[!UICONTROL Time zone]** . 예를 들어, 워크플로우는 해당하는 모든 시간대에 대해 배달을 만들 수 있도록 하기 위해 해당 월의 첫째 날 1주일 전에 태평양 표준시 오후 8시에 시작됩니다.
   >[!NOTE]
   >
   >기본적으로 선택한 시간대는 워크플로우 속성에 정의된 시간대입니다(워크플로우 [구축](../../automating/using/building-a-workflow.md)참조).

   ![](assets/wkf_push_example_5.png)

1. 쿼리 **활동을** 통해 20-30세 사이의 VIP 고객을 타깃팅할 수 있습니다. 20-30세 고객은 모바일 애플리케이션을 구독했고 보낸 이메일을 열지 않았습니다.

   * 고객(VIP 고객)을 선택하고 나이를 필터링합니다.
   * 구독을 **애플리케이션** 요소로 드래그하여 작업 영역에 놓습니다. [ **존재함** ]을 선택하고 사용할 모바일 응용 프로그램을 선택합니다.
   * 고객에게 보낸 이메일을 선택합니다.
   * 배달 로그( **로그)** 요소를 작업 공간으로 드래그하여 놓고 [존재함] **을 선택하여** 이메일을 받은 모든 고객을 타깃팅합니다.
   * 추적 로그( **추적)** 요소를 작업 영역으로 끌어다 놓고 [존재하지 않음]을 선택하여 **이메일을 열지** 않은 모든 고객을 타깃팅합니다.

      ![](assets/wkf_push_example_2.png)

1. 푸시 **알림** 활동을 통해 메시지 내용을 입력하고 사용할 개인화 필드를 선택할 수 있습니다.

   * 옵션을 **[!UICONTROL Recurring notification]**선택합니다.
   * 푸시 알림 컨텐츠를 정의합니다. 푸시 알림 컨텐츠에 대한 자세한 내용은 이 [섹션을](../../channels/using/preparing-and-sending-a-push-notification.md)참조하십시오.
   * 블록에서 **[!UICONTROL Schedule]**을 선택합니다**[!UICONTROL Messages to be sent automatically on the time zone specified below]**. 워크플로우에서와 마찬가지로 **[!UICONTROL Time zone of the contact date]**태평양 지역을 선택했습니다**[!UICONTROL Scheduler]**.
   * 필드에서 **[!UICONTROL Optimize the sending time per recipient]**을 선택합니다**[!UICONTROL Send at the recipient's time zone]**.

      ![](assets/wkf_push_example_4.png)

1. 단추를 클릭하여 반복되는 워크플로우를 시작합니다. **[!UICONTROL Start]**

   ![](assets/wkf_push_example_3.png)

이제 워크플로우가 실행 중입니다. 태평양 표준시 오후 8시에 선택한 시작 **[!UICONTROL Scheduler]**날짜에 시작하여 반복 푸시가 고객의 표준 시간대에 따라 해당 월의 첫 날 오후 8시에 전송됩니다.
