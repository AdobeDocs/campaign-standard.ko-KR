---
title: SMS 배달
seo-title: SMS 배달
description: SMS 배달
seo-description: SMS 배달 활동을 통해 워크플로우에서 단일 SMS 또는 반복되는 SMS 전송을 구성할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 736078 C 6-AC 91-4440-825 B -4 A 6 AE 31894 EF
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 채널 활동
discoiquuid: 978592 B 8-989 A -446 A -8 A 84-12 B 7 FECFC 130
context-tags: sms, main; 전달, Smscontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: bb65cbf808a95e8b42b2a682b7c0a9cc6225d920

---


# SMS 배달{#sms-delivery}

## description {#description}

![](assets/sms.png)

![](assets/recurrentsms.png)

**[!UICONTROL SMS delivery]** 활동을 통해 워크플로우에서 SMS 전송을 구성할 수 있습니다. 단일 SMS **로** 전송할 수 있고 한 번만 전송할 수도 있고 **반복되는** SMS 일 수도 있습니다.

단일 SMS 메시지는 한 번 전송되는 표준 SMS 입니다.

반복되는 SMS 메시지를 사용하면 정의된 기간 동안 동일한 SMS를 다른 타겟으로 여러 번 보낼 수 있습니다. 필요에 따라 보고서를 받을 수 있도록 기간별로 배달을 집계할 수 있습니다.

## 사용 상황 {#context-of-use}

**[!UICONTROL SMS delivery]** 활동은 일반적으로 동일한 워크플로우에서 계산된 타겟에 SMS를 보내는 데 사용됩니다.

스케줄러에 연결된 경우 반복되는 SMS 메시지를 정의할 수 있습니다.

SMS 수신자는 쿼리, 교차로 등의 타깃팅 활동을 통해 동일한 워크플로우에서 활동 업스트림 정의됩니다.

메시지 준비는 워크플로우 실행 매개 변수에 따라 트리거됩니다. 메시지 대시보드에서 수동 확인을 요청할지 여부를 선택할 수 있습니다 (기본적으로 필수). 워크플로우를 수동으로 시작하거나 워크플로우에서 스케줄러 활동을 배치하여 실행을 자동화할 수 있습니다.

## 구성 {#configuration}

1. **[!UICONTROL SMS delivery]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.

   >[!NOTE]
   >
   >워크플로우의 작업 표시줄에 있는 ![](assets/dlv_activity_params-24px.png) 단추를 통해 (게재 자체가 아닌) 활동의 일반 속성과 고급 옵션에 액세스할 수 있습니다. 이 단추는 **[!UICONTROL SMS delivery]** 활동과 관련이 있습니다. SMS 속성은 SMS Dashboard의 작업 표시줄을 통해 액세스할 수 있습니다.

1. SMS 전송 모드를 선택합니다.

   * **[!UICONTROL SMS]**: SMS는 한 번만 전송됩니다. 활동에 아웃바운드 전환을 추가할지 여부를 여기에서 지정할 수 있습니다. 이 절차의 7 단계에서는 서로 다른 전환 유형을 자세히 설명합니다.
   * **[!UICONTROL Recurring SMS]**: 활동에서 정의된 빈도에 따라 SMS가 여러 번 **[!UICONTROL Scheduler]** 전송됩니다. 전송 집계 기간을 선택합니다. 이렇게 하면 정의된 기간 동안의 모든 전송을 **반복 실행이라고** 하는 하나의 단일 보기로 다시 그룹화할 수 있으며, 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다.

      예를 들어 매일 전송되는 반복되는 생일 SMS에 대해 매월 전송을 집계하도록 선택할 수 있습니다. SMS를 매일 전송하더라도 매월 전달에 대한 보고서를 받을 수 있습니다.

1. SMS 유형을 선택합니다. SMS 유형은 **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** 메뉴에 정의된 SMS 템플릿에서 가져옵니다.
1. SMS의 일반 속성을 입력합니다. 기존 캠페인에 첨부할 수도 있습니다. 워크플로우의 배달 활동 레이블이 SMS 레이블로 업데이트됩니다.
1. SMS 콘텐츠를 정의합니다. SMS 메시지 [작성에](../../channels/using/creating-an-sms-message.md)관한 섹션을 참조하십시오.
1. 기본적으로 활동에는 **[!UICONTROL SMS delivery]** 아웃바운드 전환이 포함되지 않습니다. **[!UICONTROL SMS delivery]** 활동에 아웃바운드 전환을 추가하려면 고급 활동 옵션 **[!UICONTROL General]** 탭 (활동의 빠른 작업에 있는 ![](assets/dlv_activity_params-24px.png) 단추) 로 이동한 후 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL Add outbound transition without the population]**: 이를 통해 인바운드 전환과 동일한 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다.
   * **[!UICONTROL Add outbound transition with the population]**: 이렇게 하면 SMS가 전송된 모집단을 포함하는 아웃바운드 전환을 생성할 수 있습니다. 게재 준비 동안 제외되는 타겟 구성원 (Quarantine, Invalid Number 등) 이 전환 값에서 제외됩니다.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

활동을 다시 열면 SMS 대시보드로 바로 이동됩니다. 해당 컨텐트만 편집할 수 있습니다.

기본적으로 배달 워크플로우를 시작하면 메시지 준비만 트리거됩니다. 워크플로우에서 만든 메시지 전송은 워크플로우가 시작된 후에도 여전히 확인해야 합니다. 하지만 메시지 대시보드에서는 워크플로우에서 메시지를 만든 경우에만 **[!UICONTROL Request confirmation before sending messages]** 옵션을 비활성화할 수 있습니다. 이 옵션을 선택 해제하면 준비가 완료되면 추가 통지 없이 메시지가 전송됩니다.

## comments {#remarks}

워크플로우 내에서 만들어진 게시는 애플리케이션의 마케팅 활동 목록에서 액세스할 수 있습니다. 대시보드를 사용하여 워크플로우의 실행 상태를 볼 수 있습니다. SMS 요약 창에서 링크를 사용하면 연결된 요소 (반복되는 SMS의 경우 워크플로우, 캠페인, 상위 게재) 에 직접 액세스할 수 있습니다.

하지만 반복 게재의 실행은 기본적으로 마스크됩니다. 이를 보려면 마케팅 활동의 검색 패널에서 **[!UICONTROL Show recurring executions]** 옵션을 선택하십시오.

마케팅 활동 목록이나 관련 반복 실행을 통해 직접 액세스할 수 있는 상위 배달에서 처리된 총 전송 수를 볼 수 있습니다 ( **[!UICONTROL SMS delivery]** 활동이 구성되었을 때 지정된 집계 기간에 따라). 이렇게 하려면 상위 게재 **[!UICONTROL Deployment]** 블록의 세부 사항 보기를 선택하여 ![](assets/wkf_dlv_detail_button.png)엽니다.

## example {#example}

![](assets/wkf_sms_example_1.png)

이 예는 생일 워크플로우입니다. 매일 SMS가 해당 일에 생년생인 프로필로 전송됩니다. 이렇게 하려면:

* 을 **[!UICONTROL Scheduler]** 사용하면 매일 오전 8 시에 워크플로우를 시작할 수 있습니다.

   ![](assets/wkf_delivery_example_2.png)

* **[!UICONTROL Query]** 활동을 통해 워크플로우를 실행할 때마다 휴대폰 번호를 제공하고 현재 날짜에 생일이 있는 프로필을 계산할 수 있습니다. 생일 계산은 쿼리 편집 도구의 팔레트에서 사용할 수 있는 사전 정의된 필터를 사용하여 수행됩니다.

   ![](assets/wkf_delivery_example_3.png)

* **[!UICONTROL SMS]** 가 반복되고 있습니다. 센드는 월별로 집계됩니다. 따라서 한 달에 전송된 SMS 메시지는 하나의 보기로 집계됩니다. 따라서 1 년 동안 365 개의 배달이 실행되지만 Adobe Campaign 인터페이스에서 12 개의 보기 ( **반복되는 실행**) 로 다시 그룹화됩니다. 내역과 보고서 세부 사항은 매달 표시되며 모든 전송 시에는 표시되지 않습니다.

   ![](assets/wkf_sms_example_4.png)

워크플로우에 있는 SMS 전달의 또 다른 예는 사용 사례를 [참조하십시오. 비공개로 새 배달을 전송하는 리타겟팅 워크플로우](../../automating/using/workflow-cross-channel-retargeting.md).
