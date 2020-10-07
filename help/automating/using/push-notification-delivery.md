---
title: 푸시 알림 게재
description: 푸시 알림 배달 활동을 통해 워크플로우에서 단일 푸시 알림 또는 반복 푸시 알림 전송을 구성할 수 있습니다.
page-status-flag: never-activated
uuid: 994d8fe3-29f0-4b5c-89ee-c6be7c60a31b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: e61bdaee-4b48-4845-a2a5-574b577ea796
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 47%

---


# 푸시 알림 게재{#push-notification-delivery}

## 설명 {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

The **[!UICONTROL Push notification]** activity allows you to configure sending a push notification in a workflow. 단일 전송 알림일 수 있으며 한 번만 전송되거나 반복적인 알림일 수 있습니다.

* **단일** 전송 알림은 표준 모바일 앱 푸시 알림 배달이며 한 번 전송됩니다.
* **반복적인** 알림을 사용하면 정의된 기간 동안 여러 대상에 동일한 모바일 앱 푸시 알림 전송을 여러 번 전송할 수 있습니다. 필요한 보고서를 얻기 위해 기간별 게재를 집계할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

The **[!UICONTROL Push notification]** activity is generally used to automate sending a notification to a target calculated in the same workflow.

스케줄러에 연결되면 반복되는 푸시 알림을 정의할 수 있습니다.

받는 사람은 쿼리, 교차점 등과 같은 타깃팅 활동을 통해 동일한 워크플로에서 활동의 업스트림으로 정의됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 메시지를 보낼 수동 확인을 요청할지 여부를 선택할 수 있습니다(기본적으로 필요). 워크플로우를 수동으로 시작하거나 워크플로우에 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

**관련 항목**

* [워크플로우로 반복 푸시 알림 전송](../../automating/using/recurring-push-notifications.md)

## 구성 {#configuration}

1. **[!UICONTROL Push notification]** 활동을 워크플로우로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.

   >[!NOTE]
   >
   >활동의 빠른 작업에서 ![](assets/dlv_activity_params-24px.png) 버튼을 통해 활동의 일반 속성 및 고급 옵션(게재 자체가 아님)에 액세스할 수 있습니다. 이 버튼은 **[!UICONTROL Push notification]** 활동에만 해당됩니다. 푸시 알림의 속성은 푸시 대시보드의 작업 표시줄을 통해 액세스할 수 있습니다.

1. 푸시 알림 전송 모드를 선택합니다.

   * **[!UICONTROL Single notification]**:푸시 알림이 한 번 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 다양한 전환 유형은 이 절차의 7단계에서 자세히 설명합니다.
   * **[!UICONTROL Recurring notification]**:푸시 알림은 활동에 정의된 빈도에 따라 여러 번 **[!UICONTROL Scheduler]** 전송됩니다. 전송 집계 기간을 선택합니다. This allows you to regroup all the sends that occur during the defined period in one single push notification that is also called **recurring execution** and can be accessed from the application&#39;s marketing activity list.

      예를 들어, 매일 전송되는 반복 생일 알림의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 알림을 매일 보내더라도 매월 배달 보고서를 받을 수 있습니다.

1. 알림 유형을 선택합니다. 이러한 유형은 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]** 메뉴에 정의된 푸시 알림 템플릿에서 가져옵니다.
1. 푸시 알림의 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 배달 활동의 레이블은 푸시 알림 레이블로 업데이트됩니다.
1. 푸시 알림 컨텐츠를 정의합니다. 푸시 [알림 만들기를 참조하십시오.](../../channels/using/preparing-and-sending-a-push-notification.md)
1. 기본적으로 **[!UICONTROL Push notification]** 활동에는 아웃바운드 전환이 포함되지 않습니다. **[!UICONTROL Push Notification]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션의 ![](assets/dlv_activity_params-24px.png) 탭(활동의 빠른 작업에 있는 **[!UICONTROL General]** 버튼)으로 이동한 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 인바운드 전환과 정확히 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**:이렇게 하면 알림을 보낸 모집단 포함 아웃바운드 전환을 생성할 수 있습니다. 배달 준비 중에 제외된 대상의 멤버는 이 전환에서 제외됩니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 푸시 알림 대시보드로 바로 이동합니다. 콘텐츠만 편집할 수 있습니다.

기본적으로 게재 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우가 시작된 후에도 워크플로우에서 만든 메시지 전송을 확인해야 합니다. 하지만 메시지가 워크플로우에서 생성된 경우에만 메시지 대시보드에서 **[!UICONTROL Request confirmation before sending messages]** 옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료된 후 추가 통보 없이 메시지가 전송됩니다.

## 비고 {#remarks}

워크플로우 내에서 생성된 게재는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 푸시 알림 요약 창의 링크를 통해 연결된 요소(워크플로우, 캠페인 등)에 직접 액세스할 수 있습니다.

In the parent deliveries, which can be accessed from the marketing activity list, you can view the total number of sends that have been processed (according to the aggregation period specified when the **[!UICONTROL Push notification]** activity was configured). 이렇게 하려면 ![](assets/wkf_dlv_detail_button.png)을(를) 선택하여 상위 게재 **[!UICONTROL Deployment]** 블록의 세부 사항 보기를 엽니다.
