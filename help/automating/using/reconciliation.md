---
title: 조정
description: 조정 활동을 사용하면 미식별 데이터를 기존 리소스에 연결할 수 있습니다.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 87e0611fae0560aca276caa3c4cf793e9c095d72
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 95%

---


# 조정{#reconciliation}

## 설명 {#description}

![](assets/reconciliation.png)

**[!UICONTROL Reconciliation]** 활동을 사용하면 미식별 데이터를 기존 리소스에 연결할 수 있습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Reconciliation]** 활동은 기본적으로 데이터 관리 용도로 사용되며 두 가지 다른 사용 사례에서 쓰일 수 있습니다.

* 관계 추가: **[!UICONTROL Links]** 탭에서 인바운드 데이터와 다른 여러 Adobe Campaign 데이터베이스 차원 사이에 연결을 추가할 수 있습니다.

   예를 들어 구매 데이터가 들어 있는 파일에는 구매자와 구매한 제품을 식별하기 위한 정보도 들어 있을 수 있습니다. 따라서 파일 데이터에는 (**구매** 차원 외에도) **제품** 및 **프로필**&#x200B;의 두 차원에 대한 데이터가 더 있습니다. 이 두 차원과 **구매** 차원 사이에 관계를 만들어야 합니다(다음 예제 참조).

   관계를 정의할 때 연결된 차원의 외래 키를 참조할 수 있도록 인바운드 데이터에 열이 추가됩니다.

   >[!NOTE]
   >
   >이 작업은 연결된 차원의 데이터가 이미 데이터베이스에 있음을 의미합니다. 예를 들어 어떤 제품을, 어떤 시간에, 어떤 고객이 구매했는지 등을 표시하는 구매 파일을 가져올 경우, 데이터베이스에는 이미 고객과 제품이 존재할 것입니다.

* 데이터 식별: **[!UICONTROL Identification]** 탭에서 인바운드 데이터를 Adobe Campaign 데이터베이스의 기존 차원에 있는 열에 간단히 연결할 수 있습니다. 활동 후에 데이터는 정의된 차원에 속하는 것으로 식별됩니다.

   예를 들어 대상자 저장, 데이터베이스 업데이트 등의 활동을 수행할 수 있습니다.

예를 들어 데이터 로드 활동 뒤에 **[!UICONTROL Reconciliation]** 활동을 배치하여 비표준 데이터를 데이터베이스로 가져올 수 있습니다.

**관련 항목:**

* [사용 사례: 관계를 사용한 데이터 조정](../../automating/using/reconciliation-using-relations.md)
* [사용 사례: 조정을 사용한 데이터 업데이트](../../automating/using/data-update-reconciliation.md)
* [사용 사례: 데이터베이스와 파일 대상 조정](../../automating/using/reconcile-file-audience-with-database.md)

## 구성 {#configuration}

1. 타겟팅 차원이 Adobe Campaign에서 바로 제공되지 않는 모집단이 포함된 전환 이후, **[!UICONTROL Reconciliation]** 활동을 워크플로우에 끌어다 놓습니다. 자세한 내용은 [차원 및 리소스 타겟팅](../../automating/using/query.md#targeting-dimensions-and-resources)을 참조하십시오.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 인바운드 데이터와 다른 데이터베이스 차원 사이의 연결을 정의하려면 **[!UICONTROL Links]** 탭으로 이동합니다.

   필요한 만큼 관계를 추가합니다. 먼저 각 관계에 대하여 연결된 차원을 선택한 다음, 연결 세부 정보에서 해당 필드를 지정합니다.

1. 인바운드 데이터를 간단히 식별하려면 **[!UICONTROL Identification]** 탭으로 이동하여 **[!UICONTROL Identify the document from the working data]** 상자를 선택합니다.

   인바운드 데이터를 조정할 타겟팅 차원을 선택합니다.

   조정 기준을 추가하여 인바운드 전환 레코드에 선택한 타겟팅 차원 레코드를 연결합니다. 기준을 여러 개 지정한 경우, 모든 기준의 유효성을 검사해야 모든 데이터 간의 연결이 작동합니다.

   **[!UICONTROL Processing unidentified source lines]** 모드를 선택합니다.

   * **[!UICONTROL Ignore them]**: 식별 가능한 데이터만 활동의 아웃바운드 전환에 남습니다.
   * **[!UICONTROL Keep in the outbound population]**: 인바운드 전환의 모든 데이터가 활동의 아웃바운드 전환에 남습니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.
