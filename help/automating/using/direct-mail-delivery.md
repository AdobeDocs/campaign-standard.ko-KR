---
title: DM 게재
description: DM 배달 활동을 사용하면 워크플로우에서 단일 DM 또는 반복 DM 전송을 구성할 수 있습니다.
page-status-flag: never-activated
uuid: bfa7b176-a17c-4079-a073-64b8ce4788ed
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: b9ddb2a0-54ff-4ada-be6f-8109fa06d461
context-tags: directMail,workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6f7f4f3d81f4e6a540b3317f283c1e2311ccc65a

---


# DM 게재{#direct-mail-delivery}

## 설명 {#description}

![](assets/paper.png)

![](assets/recurrentpaper.png)

이 **[!UICONTROL Direct mail delivery]**활동을 사용하면 DM 캠페인에 사용할 프로필 데이터가 포함된 파일을 구성하고 준비할 수 있습니다. 한 번만 사용되는 DM이거나**&#x200B;반복되는&#x200B;**DM일 수 있습니다.

표준 다이렉트 메일은 한 번 전송됩니다.

반복 메일을 사용하면 지정된 기간 동안 동일한 DM을 여러 번 다른 타겟으로 보낼 수 있습니다. 필요에 해당하는 보고서를 가져오려면 기간당 납품을 집계할 수 있습니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Direct mail delivery]**활동은 일반적으로 프로필 데이터가 포함된 파일 준비를 자동화하는 데 사용됩니다. 그러면 이 파일을 우편 발송 담당 파트너/제공자에게 보낼 수 있습니다.

스케줄러에 연결할 때 반복되는 다이렉트 메일을 정의할 수 있습니다.

DM 수신자는 쿼리, 교차로 등과 같은 타깃팅 활동을 통해 동일한 워크플로우에서 활동의 업스트림으로 정의됩니다. 우편 주소가 지정되지 않은 프로필은 직접 메일을 준비할 때 자동으로 제외됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 수동 확인을 요청할지 여부를 선택할 수 있습니다(기본적으로 필수). 워크플로우를 수동으로 시작하거나 워크플로우에 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

## 구성 {#configuration}

1. 워크플로우를 워크플로우로 드래그하여 **[!UICONTROL Direct mail delivery]**놓을 수 있습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.

   >[!NOTE]
   >
   >활동의 빠른 작업의 ![](assets/dlv_activity_params-24px.png) 단추를 통해 배달 자체가 아닌 활동의 일반 속성 및 고급 옵션에 액세스할 수 있습니다. 이 단추는 채널 활동에만 적용됩니다. 다이렉트 메일 대시보드의 작업 표시줄을 통해 다이렉트 메일 속성에 액세스할 수 있습니다.

1. DM 전송 모드를 선택합니다.

   * **[!UICONTROL Direct mail]**:DM은 한 번 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 이 절차의 7단계에서 다양한 전환 유형에 대해 자세히 설명합니다.
   * **[!UICONTROL Recurring direct mail]**:다이렉트 메일은 활동에 정의된 빈도에 따라 여러 번 전송됩니다.**[!UICONTROL Scheduler]** 전송의 집계 기간을 선택합니다. 이렇게 하면 정의된 기간 동안 발생한 모든 전송을 반복 실행이라고도 하며 **애플리케이션의 마케팅 활동 목록에서 액세스할 수 있는 단일 DM에서** 다시 그룹화할 수 있습니다.

      예를 들어 매일 처리되는 반복 생일 메일의 경우 월별 전송을 집계하도록 선택할 수 있습니다. 이렇게 하면 메일이 매일 처리되지만 매월 배달 보고서를 받을 수 있습니다.

      >[!NOTE]
      >
      >반복되는 다이렉트 메일의 경우 워크플로우의 각 실행 시 새 파일이 생성됩니다. 선택한 집계 기간은 이 동작에 영향을 주지 않습니다.

1. DM 유형을 선택합니다. DM 유형은 **[!UICONTROL Resources]**>**[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]**메뉴에 정의된 템플릿에서 가져옵니다.
1. DM의 일반 속성을 입력합니다. 기존 캠페인에 연결할 수도 있습니다. 워크플로우의 배달 활동의 레이블이 직접 메일 레이블로 업데이트됩니다.
1. DM 컨텐츠를 정의합니다. 컨텐츠 [편집에](../../designing/using/personalization.md)대한 섹션을 참조하십시오.
1. 기본적으로 이 **[!UICONTROL Direct mail delivery]**활동에는 아웃바운드 전환이 포함되지 않습니다. 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션(활동의 빠른 동작에 있는**[!UICONTROL Direct mail delivery]** 단추)의 **[!UICONTROL General]**![](assets/dlv_activity_params-24px.png)탭으로 이동한 다음 다음 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**:이를 통해 인바운드 전환과 정확히 동일한 인구를 포함하는 아웃바운드 전환을 생성할 수 있습니다. 이 변환에는 DM 활동으로 생성된 파일과 DM 활동으로 받은 원시 모집단 등이 포함됩니다.
   * **[!UICONTROL Add outbound transition with the population]**:이렇게 하면 다이렉트 메일을 보낼 인구를 포함하는 아웃바운드 전환을 생성할 수 있습니다. DM 준비 중 제외된 대상 구성원(격리, 잘못된 주소 등) 는 이 전환에서 제외됩니다. 이 변환에는 DM에서 생성된 파일도 포함됩니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 다이렉트 메일 대시보드로 바로 이동합니다. 컨텐트만 편집할 수 있습니다.

기본적으로 배달 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우가 시작된 후에도 워크플로우에서 만든 메시지 전송을 확인해야 합니다. 그러나 메시지 대시보드에서 메시지를 만든 경우에만 **[!UICONTROL Request confirmation before sending messages]**옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료되면 추가 통보 없이 메시지가 전송됩니다.

## 주의 사항 {#remarks}

워크플로우 내에서 생성된 게재는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. 다이렉트 메일 요약 창의 링크를 사용하면 연결된 요소(반복 DM의 경우 워크플로우, 캠페인, 상위 배달)에 직접 액세스할 수 있습니다.

![](assets/wkf_display_parent_elements_direct_mail.png)

반복 게재의 실행은 기본적으로 숨겨집니다. 이를 보려면 마케팅 활동의 검색 패널에서 **[!UICONTROL Show recurring executions]**옵션을 선택합니다.

![](assets/wkf_display_recurrent_executions_direct_mail.png)

마케팅 활동 목록에서 액세스하거나 관련 반복 실행을 통해 직접 액세스할 수 있는 상위 배달에서 처리된 총 메일 수를 볼 수 있습니다(활동이 구성되었을 때 지정된 집계 기간에 따라). **[!UICONTROL Direct mail delivery]**이렇게 하려면 단추를 선택하여 상위 배달**[!UICONTROL Deployment]** 블록의 세부 사항 보기를 ![](assets/wkf_dlv_detail_button.png) 엽니다.

![](assets/wkf_display_recurrent_executions_3_direct_mail.png)

## 예 {#example}

Direct Mail **[!UICONTROL Direct mail delivery]**장의 예는[다음과 같습니다](../../channels/using/example-of-direct-mail-in-a-workflow.md).
