---
title: 고객 보기
seo-title: 고객 보기
description: 고객 보기
seo-description: 대상 활동을 읽으면 기존 고객을 검색하고 추가 필터링 조건을 적용하여 세부적으로 수정할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 58 c 54 e 71-f 4 a 7-4 ae 9-80 a 3-33 c 379 ab 1 db 9
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 타깃팅 활동
discoiquuid: 674684 e 5-8830-4 d 2 f-ba 97-59 ed 4 ba 7422 f
context-tags: Readaudience, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Read audience{#read-audience}

## Description {#description}

![](assets/prefill.png)

**[!UICONTROL Read audience]** 활동을 통해 기존 대상을 검색하고 추가 필터링 조건을 적용하여 이를 개선할 수 있습니다.

## Context of use {#context-of-use}

**[!UICONTROL Read audience]** 활동은 기존 대상자만 선택해야 **[!UICONTROL Query]** 하는 경우를 위해 디자인된 더 간단한 버전의 활동입니다.

## Configuration {#configuration}

1. **[!UICONTROL Read audience]** 워크플로우에 활동을 놓습니다.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the audience you want to retrieve from the **[!UICONTROL Properties]** tab.

   You can retrieve audiences of the following types: **[!UICONTROL List]**, **[!UICONTROL Query]**, **[!UICONTROL File]** and **[!UICONTROL Experience Cloud]**. For more information on audience types, refer to the [Audiences](../../audiences/using/about-audiences.md) documentation.

   **[!UICONTROL Use a dynamic audience]** 이 옵션을 사용하면 워크플로우의 이벤트 변수를 기반으로 타게팅할 대상의 이름을 정의할 수 있습니다. For more on this, refer to the [Customizing activities with events variables](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) section.

   ![](assets/readaudience_activity1.png)

1. If you want to apply additional filtering to the selected audience, add conditions via the **[!UICONTROL Source filtering]** tab of the activity.

   For more information about creating filtering conditions, refer to the [Creating queries](../../automating/using/editing-queries.md#creating-queries) documentation.

1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

## Example: Reconcile a File audience with the database {#example--reconcile-a-file-audience-with-the-database}

This example shows how to use the **[!UICONTROL Read audience]** activity to reconcile an audience directly created from a file import.

파일 가져오기를 수행할 때 대상의 컨텐츠를 직접 저장할 수 있습니다. 이 대상은 파일 대상자이며 해당 데이터는 모든 데이터베이스 리소스와 연결되어 있지 않습니다.

가져오기 워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example3.png)

* [로드 파일](../../automating/using/load-file.md) 활동은 외부 도구에서 추출한 프로필 데이터가 들어 있는 파일을 업로드합니다.

   예를 들면 다음과 같습니다.

   ```
   lastname;firstname;birthdate;email;crmID
   Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
   Mars;Daniel;17/11/1987;dannymars@example.com;123545
   Smith;Clara;08/02/1989;hayden.smith@example.com;124567
   Durance;Allison;15/12/1978;allison.durance@example.com;120987
   Lucassen;Jody;28/03/1988;jody.lucassen@example.com;127634
   Binder;Tom;19/01/1982;tombinder@example.com;128653
   Binder;Tommy;19/01/1915;tombinder@example.com;134576
   Connor;Jade;10/10/1979;connor.jade@example.com;132452
   Mack;Clarke;02/03/1985;clarke.mack@example.com;149876
   Ross;Timothy;04/07/1986;timross@example.com;157643
   ```

* [대상자](../../automating/using/save-audience.md) 활동 저장은 들어오는 데이터를 대상자로 저장합니다. 데이터가 아직 조정되지 않았으므로 대상이 파일 대상이고 해당 데이터가 아직 프로필 데이터로 인식되지 않습니다.

조정 워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example2.png)

* **[!UICONTROL Read audience]** 활동은 가져오기 워크플로우에서 만든 파일 대상자를 업로드합니다. 대상 데이터는 아직 Adobe Campaign 데이터베이스와 화해하지 않습니다.
* [조정](../../automating/using/reconciliation.md) 활동은 들어오는 데이터를 **[!UICONTROL Identification]** 탭을 통해 프로필로 식별합니다. For example by using the **email** field as reconciliation criteria.
* [데이터](../../automating/using/update-data.md) 업데이트 작업은 들어오는 데이터로 데이터베이스의 프로필 리소스를 삽입하고 업데이트합니다. As the data is already identified as profiles, you can select the **[!UICONTROL Directly using the targeting dimension]** option and select **[!UICONTROL Profiles]** in the **[!UICONTROL Identification]** tab of the activity. 그런 다음 탭 기준 탭에서 업데이트해야 하는 필드 목록을 추가하면 됩니다.

## Example: Union on two refined audiences {#example--union-on-two-refined-audiences}

The workflow defined in this example shows the union of two **[!UICONTROL Read audience]** activities. 이 워크플로우의 목표는 18 세에서 30 세 사이의 골드 또는 실버 멤버로 이메일을 보내는 것입니다.

Gold 및 Silver 멤버를 추적할 수 있도록 시스템에서 특정 대상이 이미 만들어져 있습니다.

워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example1.png)

* A first **[!UICONTROL Read audience]** activity that retrieves the Gold members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A second **[!UICONTROL Read audience]** activity that retrieves the Silver members audience and refines it by selecting only profiles that are between 18 and 30 years old.
* A **[!UICONTROL Union]** activity that unites populations from both **[!UICONTROL Read audiences]** activities into one final population.
* An **[!UICONTROL Email delivery]** activity that sends the email to the population coming from the **[!UICONTROL Union]** activity.

