---
title: 푸시 알림 게재
description: 푸시 알림 게재 활동을 사용하면 워크플로우에서 단일 전송 푸시 알림 또는 반복되는 푸시 알림 전송을 구성할 수 있습니다.
audience: automating
content-type: reference
topic-tags: channel-activities
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: b6a43d51-32d4-4806-b4e4-33236f1e27f5
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 46%

---

# 푸시 알림 게재{#push-notification-delivery}

## 설명 {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

**[!UICONTROL Push notification]** 활동을 사용하면 워크플로우에서 푸시 알림 전송을 구성할 수 있습니다. 한 번만 보내는 단일 전송 알림일 수도 있고 반복 알림일 수도 있습니다.

* **단일** 전송 알림은 한 번 전송되는 표준 모바일 앱 푸시 알림 게재입니다.
* **반복** 알림을 사용하면 정의된 기간 동안 동일한 모바일 앱 푸시 알림 게재를 여러 대상에 여러 번 보낼 수 있습니다. 필요한 보고서를 얻기 위해 기간별 게재를 집계할 수 있습니다.

## 사용 컨텍스트 {#context-of-use}

**[!UICONTROL Push notification]** 활동은 일반적으로 동일한 워크플로우에서 계산된 타겟으로 알림 전송을 자동화하는 데 사용됩니다.

스케줄러에 연결하면 반복되는 푸시 알림을 정의할 수 있습니다.

수신자는 쿼리, 교집합 등과 같은 타겟팅 활동을 통해 동일한 워크플로우에서 활동의 업스트림으로 정의됩니다.

메시지 준비는 워크플로 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 메시지를 보낼 수동 확인을 요청할지 여부를 선택할 수 있습니다(기본적으로 필요). 워크플로를 수동으로 시작하거나 워크플로에 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

**관련 항목**

* [워크플로우로 반복 푸시 알림 보내기](../../automating/using/recurring-push-notifications.md)

## 구성 {#configuration}

1. **[!UICONTROL Push notification]** 활동을 워크플로로 끌어서 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.

   >[!NOTE]
   >
   >활동의 빠른 작업에서 ![](assets/dlv_activity_params-24px.png) 버튼을 통해 활동의 일반 속성 및 고급 옵션(게재 자체가 아님)에 액세스할 수 있습니다. 이 버튼은 **[!UICONTROL Push notification]** 활동에만 해당됩니다. 푸시 알림의 속성은 푸시 대시보드의 작업 표시줄을 통해 액세스할 수 있습니다.

1. 푸시 알림 전송 모드를 선택합니다.

   * **[!UICONTROL Single notification]**: 푸시 알림이 한 번만 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 다양한 전환 유형은 이 절차의 7단계에서 자세히 설명합니다.
   * **[!UICONTROL Recurring notification]**: **[!UICONTROL Scheduler]** 활동에 정의된 빈도에 따라 푸시 알림이 여러 번 전송됩니다. 전송 집계 기간을 선택합니다. 이를 통해 정의된 기간 동안 발생하는 모든 전송을 하나의 푸시 알림에서 다시 그룹화할 수 있습니다. 이 알림은 **반복 실행**&#x200B;이라고도 하며 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다.

     예를 들어 매일 전송되는 반복 생일 알림의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 이렇게 하면 매일 알림이 전송되지만 매월 게재 보고서를 받을 수 있습니다.

1. 알림 유형을 선택합니다. 이러한 유형은 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]** 메뉴에 정의된 푸시 알림 템플릿에서 가져옵니다.
1. 푸시 알림의 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 게재 활동의 레이블은 푸시 알림 레이블로 업데이트됩니다.
1. 푸시 알림 콘텐츠를 정의합니다. [푸시 알림 만들기](../../channels/using/preparing-and-sending-a-push-notification.md)를 참조하세요.
1. 기본적으로 **[!UICONTROL Push notification]** 활동에는 아웃바운드 전환이 포함되지 않습니다. **[!UICONTROL Push Notification]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션의 ![](assets/dlv_activity_params-24px.png) 탭(활동의 빠른 작업에 있는 **[!UICONTROL General]** 버튼)으로 이동한 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 인바운드 전환과 정확히 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**: 알림이 전송된 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 게재를 준비하는 동안 제외된 타겟 멤버는 이 전환에서 제외됩니다.

1. 활동 구성을 확인하고 워크플로를 저장합니다.

활동을 다시 열면 푸시 알림 대시보드로 바로 이동합니다. 콘텐츠만 편집할 수 있습니다.

기본적으로 게재 워크플로를 시작하면 메시지 준비만 트리거됩니다. 워크플로가 시작된 후에도 워크플로에서 만든 메시지 전송을 확인해야 합니다. 하지만 메시지가 워크플로에서 생성된 경우에만 메시지 대시보드에서 **[!UICONTROL Request confirmation before sending messages]** 옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료된 후 추가 통보 없이 메시지가 전송됩니다.

## 비고 {#remarks}

워크플로 내에서 생성된 게재는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로의 실행 상태를 볼 수 있습니다. 푸시 알림 요약 창의 링크를 사용하면 연결된 요소(워크플로우, 캠페인 등)에 직접 액세스할 수 있습니다.

마케팅 활동 목록에서 액세스할 수 있는 상위 게재에서 **[!UICONTROL Push notification]** 활동이 구성되었을 때 지정된 집계 기간에 따라 처리된 총 전송 수를 볼 수 있습니다. 이렇게 하려면 ![](assets/wkf_dlv_detail_button.png)을(를) 선택하여 상위 게재 **[!UICONTROL Deployment]** 블록의 세부 사항 보기를 엽니다.
