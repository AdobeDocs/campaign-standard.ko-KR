---
title: DM (Direct Mail Delivery)
seo-title: DM (Direct Mail Delivery)
description: DM (Direct Mail Delivery)
seo-description: 다이렉트 메일 배달 활동을 사용하면 워크플로우에서 단일 전송 DM 또는 반복되는 다이렉트 메일을 보낼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: BFA 7 B 176-A 17 C -4079-A 073-64 B 8 CE 4788 ED
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 채널 활동
discoiquuid: b 9 ddb 2 a 0-54 ff -4 ada-be 6 f -8109 fa 06 d 461
context-tags: Directmail, workflow, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Direct mail delivery{#direct-mail-delivery}

## Description {#description}

![](assets/paper.png)

![](assets/recurrentpaper.png)

**[!UICONTROL Direct mail delivery]** 이 활동을 사용하면 다이렉트 메일 캠페인에 사용할 프로필 데이터가 들어 있는 파일을 구성하고 준비할 수 있습니다. This can be a direct mail that is used just once, or it can be a **recurring** direct mail.

표준 다이렉트 메일은 한 번 전송됩니다.

반복 메일을 사용하면 정의된 기간 동안 동일한 직통 메일을 다른 대상에 여러 번 보낼 수 있습니다. 필요에 따라 보고서를 받을 수 있도록 기간별로 배달을 집계할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Direct mail delivery]** 활동은 일반적으로 프로필 데이터를 포함하는 파일 준비를 자동화하는 데 사용됩니다. 그런 다음 이 파일을 메일링 관련 파트너/공급자에게 전송할 수 있습니다.

스케줄러에 연결되면 반복되는 다이렉트 메일을 정의할 수 있습니다.

다이렉트 메일 수신자는 쿼리, 교차로 등의 타깃팅 활동을 통해 동일한 워크플로우에서 활동 업스트림 정의됩니다. 우편 주소가 지정되지 않은 프로필은 다이렉트 메일을 준비할 때 자동으로 제외됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 수동 확인을 요청할지 여부를 선택할 수 있습니다 (기본적으로 필수). 워크플로우를 수동으로 시작하거나 워크플로우에서 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

## Configuration {#configuration}

1. **[!UICONTROL Direct mail delivery]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.

   >[!NOTE]
   >
   >You can access the general properties and advanced options of the activity (and not of the delivery itself) via the ![](assets/dlv_activity_params-24px.png) button from the activity's quick actions. 이 단추는 채널 활동과 관련이 있습니다. 다이렉트 메일 속성은 DM 대시보드의 작업 표시줄을 통해 액세스할 수 있습니다.

1. DM (Direct Mail Send) 모드를 선택합니다.

   * **[!UICONTROL Direct mail]**: 다이렉트 메일은 한 번만 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 이 절차의 7 단계에서는 서로 다른 전환 유형을 자세히 설명합니다.
   * **[!UICONTROL Recurring direct mail]**: 활동에 정의된 빈도에 따라 다이렉트 메일이 여러 번 **[!UICONTROL Scheduler]** 전송됩니다. 전송 집계 기간을 선택합니다. This allows you to regroup all the sends that occur during the defined period in one single direct mail that is also called **Recurring execution** and can be accessed from the application's marketing activity list.

      예를 들어 매일 처리되는 반복되는 생일 메일의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 이렇게 하면 매일 메일을 처리하더라도 매월 배송 시 보고서를 받을 수 있습니다.

      >[!NOTE]
      >
      >반복되는 다이렉트 메일의 경우, 워크플로우의 각 실행 시 새 파일이 생성됩니다. 선택한 집계 기간은 이 비헤이비어에는 영향을 주지 않습니다.

1. 직접 메일 유형을 선택합니다. The direct mail types come from templates defined in the **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** menu.
1. 일반 우편물의 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 배달 활동 레이블이 DM 레이블로 업데이트됩니다.
1. 다이렉트 메일 컨텐츠를 정의합니다. Refer to the section concerning [content editing](../../designing/using/about-personalization.md).
1. By default, the **[!UICONTROL Direct mail delivery]** activity does not include any outbound transitions. **[!UICONTROL Direct mail delivery]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션 **[!UICONTROL General]** 탭 (활동의 빠른 작업에 있는 ![](assets/dlv_activity_params-24px.png) 단추) 로 이동한 후 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 이를 통해 인바운드 전환과 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 이 전환에는 다이렉트 메일 활동에 의해 생성된 파일과 다이렉트 메일 활동으로 받은 원시 모집단 수가 포함됩니다.
   * **[!UICONTROL Add outbound transition with the population]**: 이렇게 하면 다이렉트 메일을 보낼 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 다이렉트 메일 준비 동안 제외되는 타겟 구성원 (Quarantine, Invalid Address 등) 이 전환 값에서 제외됩니다. 전환 과정에는 다이렉트 메일로 생성된 파일도 포함되어 있습니다.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 다이렉트 메일 대시보드로 바로 이동됩니다. 해당 컨텐트만 편집할 수 있습니다.

기본적으로 배달 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우에서 만든 메시지 전송은 워크플로우가 시작된 후에도 여전히 확인해야 합니다. But from the message dashboard, and only if the message was created from a workflow, you can disable the **[!UICONTROL Request confirmation before sending messages]** option. 이 옵션을 선택 해제하면 준비가 완료되면 추가 통지 없이 메시지가 전송됩니다.

## Remarks {#remarks}

워크플로우 내에서 만들어진 게시는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 다이렉트 메일 요약 창의 링크를 사용하면 연결된 요소 (반복되는 직통 메일의 경우 워크플로우, 캠페인, 상위 배달) 에 직접 액세스할 수 있습니다.

![](assets/wkf_display_parent_elements_direct_mail.png)

반복 게재의 실행이 기본적으로 마스크됩니다. To view them, check the **[!UICONTROL Show recurring executions]** option in the marketing activities' search panel.

![](assets/wkf_display_recurrent_executions_direct_mail.png)

In the parent deliveries, which can be accessed from the marketing activity list or directly via the associated recurring executions, you can view the total number of mails that have been processed (according to the aggregation period specified when the **[!UICONTROL Direct mail delivery]** activity was configured). To do this, open the detail view of the parent delivery's **[!UICONTROL Deployment]** block by selecting ![](assets/wkf_dlv_detail_button.png).

![](assets/wkf_display_recurrent_executions_3_direct_mail.png)

## Example {#example}

An example of **[!UICONTROL Direct mail delivery]** is available in the [Direct Mail](../../channels/using/example-of-direct-mail-in-a-workflow.md) chapter.
