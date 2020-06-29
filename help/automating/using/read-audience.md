---
title: 대상자 읽기
description: 대상 읽기 활동을 사용하면 기존 대상을 검색하고 추가 필터링 조건을 적용하여 대상을 세분화할 수 있습니다.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 대상자 읽기{#read-audience}

## 설명 {#description}

![](assets/prefill.png)

이 **[!UICONTROL Read audience]** 활동을 통해 기존 대상을 검색하고 추가 필터링 조건을 적용하여 세분화할 수 있습니다.

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Read audience]** 활동은 기존 대상을 선택하기만 하면 되는 경우에 사용하기 위해 고안된 활동의 더 간단한 **[!UICONTROL Query]** 버전입니다.

**관련 항목**

* [사용 사례: 세련된 두 고객을 위한 결합](../../automating/using/union-on-two-refined-audiences.md)
* [사용 사례: 데이터베이스와 파일 대상 조정](../../automating/using/reconcile-file-audience-with-database.md)

## 구성 {#configuration}

1. 워크플로우에 **[!UICONTROL Read audience]** 활동 놓기
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 활동을 엽니다.
1. 탭에서 검색할 대상을 **[!UICONTROL Properties]** 선택합니다.

   다음 유형의 대상을 검색할 수 있습니다. **[!UICONTROL List]**, **[!UICONTROL Query]**, **[!UICONTROL File]** and **[!UICONTROL Experience Cloud]**. 대상 유형에 대한 자세한 내용은 대상 [설명서를](../../audiences/using/about-audiences.md) 참조하십시오.

   이 **[!UICONTROL Use a dynamic audience]** 옵션을 사용하면 워크플로우의 이벤트 변수를 기반으로 타게팅할 대상의 이름을 정의할 수 있습니다. 자세한 내용은 이벤트 변수를 사용하여 [활동 사용자 지정 섹션을 참조하십시오](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) .

   ![](assets/readaudience_activity1.png)

1. 선택한 대상에 추가적인 필터링을 적용하려면 활동의 **[!UICONTROL Source filtering]** 탭을 통해 조건을 추가하십시오.

   필터링 조건을 만드는 방법에 대한 자세한 내용은 쿼리 [만들기](../../automating/using/editing-queries.md#creating-queries) 설명서를 참조하십시오.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.
