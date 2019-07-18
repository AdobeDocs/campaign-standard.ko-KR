---
title: 외부 매개 변수를 사용하여 워크플로우 호출
seo-title: 외부 매개 변수를 사용하여 워크플로우 호출
description: 외부 매개 변수를 사용하여 워크플로우 호출
seo-description: 이 섹션 상세 정보는 외부 매개 변수를 사용하여 워크플로우를 호출하는 데 사용됩니다.
page-status-flag: 정품 인증 안 함
uuid: BECCD 1 B 6-8 E 6 D -4504-9152-9 FF 537459 C 4 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: workflow-general-operation
discoiquuid: 1676 DA 91-55 E 3-414 F-BCD 3-BB 0804 B 682 BD
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 7c3b44a97af080ea7a1c28c7b7573d690d4df308

---


# Calling a workflow with external parameters{#calling-a-workflow-with-external-parameters}

Campaign Standard 에서는 매개 변수 (대상 이름, 가져올 파일 이름, 메시지 컨텐츠 일부 등) 를 포함하는 워크플로우를 호출할 수 있습니다. 이렇게 하면 캠페인을 외부 시스템과 쉽게 통합할 수 있습니다.

다음 예제를 통해 CMS에서 바로 이메일을 발송할 수 있습니다. 이 경우 대상 및 이메일 컨텐트를 CMS로 선택하도록 시스템을 구성할 수 있습니다. 그런 다음 전송을 클릭하면 이러한 매개 변수를 사용하여 캠페인 워크플로우가 호출됩니다. 이러한 매개 변수를 워크플로우로 사용하여 게시에 사용할 대상자 및 URL 컨텐트를 정의할 수 있습니다.

매개 변수를 사용하여 워크플로우를 호출하는 프로세스는 다음과 같습니다.

1. Declare the parameters in the **[!UICONTROL External signal]** activity. See [Declaring the parameters in the External signal activity](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity).
1. Configure the **[!UICONTROL End]** activity or the API call to define the parameters and trigger the workflow **[!UICONTROL External signal]** activity.

워크플로우가 트리거되면 매개 변수가 워크플로우의 이벤트 변수에 인제스트되며 워크플로우 내에서 사용할 수 있습니다. See [Customizing a workflow with external parameters](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters).

![](assets/extsignal_process.png)

## Declaring the parameters in the External signal activity {#declaring-the-parameters-in-the-external-signal-activity}

The first step to call a workflow with parameters is to declare them in an **[!UICONTROL External signal]** activity.

1. **[!UICONTROL External signal]** 활동을 열고 **[!UICONTROL Parameters]** 탭을 선택합니다.
1. **[!UICONTROL Create element]** 단추를 클릭한 다음 각 매개 변수의 이름과 유형을 지정합니다.

   >[!CAUTION]
   >
   >Make sure that the name and number of parameters are identical to what is defined when calling the workflow (see [Defining the parameters when calling the workflow](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow)). 또한 매개 변수 유형은 예상된 값과 일치해야 합니다.

   ![](assets/extsignal_declaringparameters_1.png)

1. 매개 변수가 선언되면 워크플로우 구성을 완료한 다음 실행합니다.

## Defining the parameters when calling the workflow {#defining-the-parameters-when-calling-the-workflow}

이 섹션에서는 워크플로우를 호출할 때 매개 변수를 정의하는 방법을 자세히 설명합니다. For more on how to perform this operation from an API call, refer to the [REST APIs documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

매개 변수를 정의하기 전에 다음을 확인하십시오.

* The parameters have been declared in the **[!UICONTROL External Signal]** activity. See [Declaring the parameters in the External signal activity](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity).
* 신호 활동이 포함된 워크플로우가 실행 중입니다.

**[!UICONTROL End]** 활동을 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL End]** 활동을 열고 **[!UICONTROL External signal]** 탭을 선택합니다.
1. 호출하려는 워크플로우와 외부 신호 활동을 선택합니다.
1. **[!UICONTROL Create element]** 단추를 클릭하여 매개 변수를 추가한 다음 이름 및 값을 입력합니다.

   * **[!UICONTROL Name]**: **[!UICONTROL External signal]** 활동에서 선언한 이름입니다 (외부 신호 활동에서 매개 변수 [선언 참조](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity)).
   * **[!UICONTROL Value]**: 매개 변수에 할당할 값입니다. The value should follow the **Standard syntax**, described in [this section](../../automating/using/advanced-expression-editing.md#standard-syntax).
   ![](assets/extsignal_definingparameters_2.png)

   >[!CAUTION]
   >
   >Make sure that all the parameters have been declared in the **[!UICONTROL External signal]** activity. 그렇지 않으면 활동을 실행할 때 오류가 발생합니다.

1. 매개 변수가 정의된 후에는 활동을 확인하고 워크플로우를 저장합니다.

## Monitoring the events variables {#monitoring-the-events-variables}

선언된 외부 매개 변수를 포함하여 워크플로우에서 사용할 수 있는 이벤트 변수를 모니터링할 수 있습니다. 이렇게 하려면 아래 단계를 따르십시오.

1. **[!UICONTROL External signal]** 활동을 팔로우하는 활동을 선택한 다음 **[!UICONTROL Log and tasks]** 단추를 클릭합니다.
1. **[!UICONTROL Tasks]** 탭에서 ![](assets/edit_darkgrey-24px.png) 단추를 클릭합니다.

   ![](assets/extsignal_monitoring_2.png)

1. 이제 워크플로우에서 사용할 수 있는 모든 이벤트 변수를 포함하여 작업에 대한 실행 컨텍스트 (ID, 상태, 기간 등) 가 표시됩니다.

   ![](assets/extsignal_monitoring_3.png)

## Customizing a workflow with external parameters {#customizing-a-workflow-with-external-parameters}

워크플로우가 트리거되면 매개 변수가 이벤트 변수에 인제스트되고 워크플로우 활동을 사용자 지정하는 데 사용할 수 있습니다.

They can, for example, be used to define which audience to read in the **[!UICONTROL Read audience]** activity, the name of the file to transfer in the **[!UICONTROL Transfer file]** activity, etc.

Activities that can be customized with events variables are detailed in [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables).

### Using events variables {#using-events-variables}

Events variables are used within an expression that must respect the **[Standard syntax](../../automating/using/advanced-expression-editing.md#standard-syntax)**.

The syntax to use events variables must follow the format below, and use the parameter's name that has been defined in the **[!UICONTROL External signal]** activity (see [Declaring the parameters in the External signal activity](../../automating/using/calling-a-workflow-with-external-parameters.md#declaring-the-parameters-in-the-external-signal-activity)):

```
$(vars/@parameterName)
```

In this syntax, the **$** function returns **string** data type. 다른 유형의 데이터를 지정하려면 다음 함수를 사용하십시오.

* **$ long**: 정수.
* **$ float**: 십진수.
* **$ BOOLEAN**: true/false.
* **$ datetime**: 타임스탬프.

활동에서 변수를 사용할 때 인터페이스는 이를 호출하는 데 도움이 됩니다.

![](assets/extsignal_callparameter.png)

* ![](assets/extsignal_picker.png): 워크플로우에서 사용할 수 있는 모든 변수 간에 이벤트 변수를 선택합니다 (참조).

   ![](assets/wkf_test_activity_variables.png)

* ![](assets/extsignal_expression_editor.png): 변수와 함수를 결합하는 표현식을 편집합니다. For more on the Expression editor, refer to [this section](../../automating/using/advanced-expression-editing.md).

   ![](assets/wkf_test_activity_variables_expression.png)

**관련 항목:**

* [표현식 편집](../../automating/using/advanced-expression-editing.md#edit-an-expression)
* [표준 구문](../../automating/using/advanced-expression-editing.md#standard-syntax)
* [함수 목록](../../automating/using/list-of-functions.md)

### Customizing activities with events variables {#customizing-activities-with-events-variables}

이벤트 변수를 사용하여 아래 섹션에 나열된 여러 활동을 사용자 정의할 수 있습니다. For more on how to call a variable from an activity, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#using-events-variables).

**[!UICONTROL Read audience]** 활동: 이벤트 변수를 기반으로 타게팅할 대상을 정의합니다.

For more on how to use the activity, refer to the [dedicated section](../../automating/using/read-audience.md).

![](assets/extsignal_activities_audience.png)

**[!UICONTROL Test]** 활동: 이벤트 변수를 기반으로 조건을 만듭니다.

For more on how to use the activity, refer to the [dedicated section](../../automating/using/test.md).

![](assets/extsignal_activities_test.png)

**[!UICONTROL Transfer file]** 활동: 이벤트 변수를 기반으로 전송할 파일을 사용자 지정합니다.

For more on how to use the activity, refer to the [dedicated section](../../automating/using/transfer-file.md).

![](assets/extsignal_activities_transfer.png)

**[!UICONTROL Query]** 활동: 이벤트 변수와 함수를 결합하는 표현식을 사용하여 쿼리에서 매개 변수를 참조할 수 있습니다. To do this, add a rule then click the **[!UICONTROL Advanced mode]** link to access the expression editing window (see [Advanced expression editing](../../automating/using/advanced-expression-editing.md)).

For more on how to use the activity, refer to the [dedicated section](../../automating/using/query.md).

![](assets/extsignal_activities_query.png)

**[!UICONTROL Channels]** 활동: 이벤트 변수를 기반으로 배달을 개인화합니다.

>[!NOTE]
>
>배달 매개 변수의 값은 배달이 준비될 때마다 검색됩니다.
>
>Recurring deliveries preparation is based on the delivery **aggregation period**. 예를 들어 집계 기간이 "일별" 인 경우 배달이 하루에 한 번만 다시 준비됩니다. 배달 매개 변수의 값이 하루 동안 수정되면 이미 한 번 준비되었기 때문에 게시에 업데이트되지 않습니다.
>
>If you plan on calling the workflow multiple times a day, use the [!UICONTROL No aggregation] option, so that the delivery parameters are updated each time. For more on recurring deliveries configuration, refer to [this section](/help/automating/using/email-delivery.md#configuration).

이벤트 변수를 기반으로 배달을 개인화하려면, 먼저 사용할 변수를 배달 활동에 선언해야 합니다.

1. Select the activity, then click the ![](assets/dlv_activity_params-24px.png) button to access the settings.
1. **[!UICONTROL General]** 탭을 선택한 다음, 게시에 개인화 필드로 사용할 수 있는 이벤트 변수를 추가합니다.

   ![](assets/extsignal_activities_delivery.png)

1. **[!UICONTROL Confirm]** 단추를 클릭합니다.

이제 선언된 이벤트 변수를 개인화 필드 목록에서 사용할 수 있습니다. 배달에서 사용하여 아래 작업을 수행할 수 있습니다.

* 게시에 사용할 템플릿의 이름을 정의합니다.

   >[!NOTE]
   >
   >This action is available for **recurring** deliveries only.

   ![](assets/extsignal_activities_template.png)

* Personalize the delivery: when selecting a personalization field to configure a delivery, events variables are available in the **[!UICONTROL Workflow parameters]** element. 예를 들어 배달 주체, 보낸 사람 등을 정의하는 등의 개인화 필드로 사용할 수 있습니다.

   Delivery personalization is detailed in [this section](../../designing/using/about-personalization.md).

   ![](assets/extsignal_activities_perso.png)

**세그먼트 코드**: 이벤트 변수를 기반으로 세그먼트 코드를 정의합니다.

>[!NOTE]
>
>This action can be performed from any activity that lets you define a segment code like, for example, **[!UICONTROL Query]** or **[!UICONTROL Segmentation]** activities.

![](assets/extsignal_activities_segment.png)

## Use case {#use-case}

아래의 사용 사례는 워크플로우 내에서 매개 변수를 사용하여 워크플로우를 호출하는 방법을 보여줍니다.

목표는 외부 매개 변수를 사용하여 API 호출에서 워크플로우를 트리거하는 것입니다. 이 워크플로우는 파일에서 데이터베이스로 데이터를 로드하고 연결된 대상을 만듭니다. 대상이 만들어지면 API 호출에 정의된 외부 매개 변수로 페르소네이화된 메시지를 전송하기 위해 두 번째 워크플로우가 트리거됩니다.

이 사례를 수행하려면 아래 작업을 수행해야 합니다.

1. **외부 매개 변수를 사용하여 Workflow 1** 를 트리거하도록 API 호출을 만듭니다. [1 단계 참조: API 호출 구성을](../../automating/using/calling-a-workflow-with-external-parameters.md#step-1--configuring-the-api-call)참조하십시오.
1. **워크플로우 1 빌드**: 워크플로우는 파일을 전송한 후 데이터베이스로 로드합니다. 그런 다음 데이터가 비어 있는지 여부를 테스트하고 결국 대상을 대상에 저장합니다. 마지막으로, Workflow 2가 트리거됩니다. [2 단계 참조: Workflow 1 구성을](../../automating/using/calling-a-workflow-with-external-parameters.md#step-2--configuring-workflow-1)참조하십시오.
1. **워크플로우 2 빌드**: 워크플로우는 Workflow 1에서 만들어진 대상을 읽은 다음, 매개 변수로 사용자 지정된 세그먼트 코드를 사용하여 프로필로 개인화된 메시지를 보냅니다. [3 단계 참조: Workflow 2 구성을](../../automating/using/calling-a-workflow-with-external-parameters.md#step-3--configuring-workflow-2)참조하십시오.

![](assets/extsignal_uc_process.png)

### Prerequisites {#prerequisites}

Before configuring the workflows, you need to create Workflow 1 and 2 with an **[!UICONTROL External signal]** activity in each of them. 이렇게 하면 워크플로우를 호출할 때 이러한 신호 활동을 타깃팅할 수 있습니다.

### Step 1: Configuring the API call {#step-1--configuring-the-api-call}

매개 변수를 사용하여 Workflow 1를 트리거하도록 API 호출을 만듭니다. For more on the API call syntax, refer to the [Campaign Standard REST APIs documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

이 경우 다음 매개 변수를 사용하여 워크플로우에 전화를 걸려고 합니다.

* **Filetotarget**: 데이터베이스로 가져올 파일의 이름.
* **할인점: 할인 가격에 배송에 표시할 설명입니다.**

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/<TRIGGER_URL>
-H 'Authorization: Bearer <ACCESS_TOKEN>' 
-H 'Cache-Control: no-cache' 
-H 'X-Api-Key: <API_KEY>' 
-H 'Content-Type: application/json;charset=utf-8' 
-H 'Content-Length:79' 
-i
-d {
-d "source:":"API",
-d "parameters":{
-d "fileToTarget":"profile.txt",
-d "discountDesc":"Running shoes"
-d } 
```

### Step 2: Configuring Workflow 1 {#step-2--configuring-workflow-1}

Workflow 1는 다음과 같이 작성됩니다.

* **[!UICONTROL External signal]** 활동: 워크플로우 내에서 사용하기 위해 외부 매개 변수를 선언해야 하는 위치.
* **[!UICONTROL Transfer file]** 활동: 매개 변수에 정의된 이름으로 파일을 가져옵니다.
* **[!UICONTROL Load file]** 활동: 가져온 파일의 데이터를 데이터베이스로 로드합니다.
* **[!UICONTROL Update data]** 활동: 가져온 파일의 데이터로 데이터베이스를 삽입하거나 업데이트합니다.
* **[!UICONTROL Test]** 활동: 가져온 데이터가 있는지 확인합니다.
* **[!UICONTROL Save audience]** 활동: 파일에 데이터가 포함되어 있으면 해당 프로필이 대상에 저장됩니다.
* **[!UICONTROL End activity]** 활동: 워크플로우 2에 사용할 매개 변수와 함께 workflow 2를 호출합니다.

![](assets/extsignal_uc_wkf1.png)

아래 절차에 따라 워크플로우를 구성합니다.

1. API 호출에 정의된 매개 변수를 선언합니다. To do this, open the **[!UICONTROL External signal]** activity, then add the parameters' names and types.

   ![](assets/extsignal_uc1.png)

1. Add a **[!UICONTROL Transfer file]** activity to import data into the database.To do this, drag and drop the activity, open it, then select the **[!UICONTROL Protocol]** tab.
1. **[!UICONTROL Use a dynamic file path]** 옵션을 선택한 다음 **Filetotarget** 매개 변수를 전송할 파일로 사용합니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc2.png)

1. 파일의 데이터를 데이터베이스에 로드합니다.

   To do this, drag and drop a **[!UICONTROL Load file]** activity into the workflow, then configure it according to your needs.

1. 가져온 파일의 데이터로 데이터베이스를 삽입하고 업데이트합니다.

   To do this, drag and drop an **[!UICONTROL Update data]** activity, then select the **[!UICONTROL Identification]** tab to add a reconciliation criteria (in our case the **email** field).

   ![](assets/extsignal_uc3.png)

1. **[!UICONTROL Fields to update]** 탭을 선택한 다음 데이터베이스에서 업데이트할 필드를 지정합니다 ( **예제에서는 Firstname** 및 **이메일** 필드).

   ![](assets/extsignal_uc4.png)

1. 파일에서 데이터가 검색되는지 확인합니다. To do this, drag and drop a **[!UICONTROL Test]** activity into the workflow, then click the **[!UICONTROL Add an element]** button to add a condition.
1. 조건을 지정하고 정의합니다. In our case, we want to test if the outbound transition contains data with the syntax below:

   ```
   $long(vars/@recCount)>0
   ```

   ![](assets/extsignal_uc5.png)

1. 데이터가 검색되면 대상에 저장합니다. To do this, add a **[!UICONTROL Save audience]** activity to the **Target not empty** transition, then open it.
1. **[!UICONTROL Use a dynamic label]** 옵션을 선택한 다음 **Filetotarget** 매개 변수를 대상 레이블로 사용합니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc6.png)

1. Drag and drop an **[!UICONTROL End]** activity that will call Workflow 2 with parameters, then open it.
1. **[!UICONTROL External signal]** 탭을 선택한 다음 트리거할 워크플로우 및 관련 신호 활동을 지정합니다.
1. 워크플로우 2 내에서 사용할 매개 변수와 관련 값을 정의합니다.

   In our case, we want to pass the parameters originally defined in the API call (**fileToTarget** and **discountDesc**), and an additional **segmentCode** parameter with a constant value ("20% discount").

   ![](assets/extsignal_uc7.png)

Workflow 1 이 구성되었으며 이제 Workflow 2를 빌드할 수 있습니다. For more on this, refer to [this section](../../automating/using/calling-a-workflow-with-external-parameters.md#step-3--configuring-workflow-2).

### Step 3: Configuring Workflow 2 {#step-3--configuring-workflow-2}

Workflow 2는 다음과 같이 작성됩니다.

* **[!UICONTROL External signal]** 활동: 워크플로우 내에서 사용하기 위해 매개 변수를 선언해야 하는 위치.
* **[!UICONTROL Read audience]** 활동: Workflow 1에 저장된 대상을 읽습니다.
* **[!UICONTROL Email delivery]** 활동: 매개 변수를 사용하여 개인화된 타깃팅된 고객에게 반복되는 메시지를 전송합니다.

![](assets/extsignal_uc_wkf2.png)

아래 절차에 따라 워크플로우를 구성합니다.

1. workflow 1에 정의된 매개 변수를 선언합니다.

   To do this, open the **[!UICONTROL External signal]** activity, then add the name and type of each parameter defined in the **[!UICONTROL End]** activity of Workflow 1.

   ![](assets/extsignal_uc8.png)

1. Workflow 1에 저장된 대상을 사용합니다. To do this, drag and drop a **[!UICONTROL Read audience]** activity into the workflow, then open it.
1. **[!UICONTROL Use a dynamic audience]** 옵션을 선택한 다음 **Filetotarget** 매개 변수를 대상 이름으로 사용하여 읽습니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc9.png)

1. **Segmentcode** 매개 변수에 따라 아웃바운드 전환 이름을 지정합니다.

   To do this, select the **[!UICONTROL Transition]** tab, then the **[!UICONTROL Use a dynamic segment code]** option.

1. **Segmentcode** 매개 변수를 아웃바운드 전환 이름으로 사용합니다.

   ```
   $(vars/@segmentCode)
   ```

   ![](assets/extsignal_uc10.png)

1. **[!UICONTROL Email delivery]** 활동을 끌어다 놓아 사용자에게 메시지를 보냅니다.
1. Identify the parameters to use in the message to personalize it with the **discountDesc** parameter. 이렇게 하려면 활동의 고급 옵션을 연 다음 매개 변수 이름과 값을 추가합니다.

   ![](assets/extsignal_uc10b.png)

1. 이제 메시지를 구성할 수 있습니다. Open the activity, then select **[!UICONTROL Recurring email]**.

   ![](assets/extsignal_uc11.png)

1. 사용할 템플릿을 선택한 다음 필요에 따라 이메일 속성을 정의합니다.
1. Use the **discountDesc** parameter as a personalization field. 이렇게 하려면 개인화 필드 목록에서 해당 항목을 선택합니다.

   ![](assets/extsignal_uc13.png)

1. 이제 메시지 구성을 완료한 다음 평소대로 보낼 수 있습니다.

   ![](assets/extsignal_uc14.png)

### Executing the workflows {#executing-the-workflows}

워크플로우가 구축되면 이를 실행할 수 있습니다. API 호출을 수행하기 전에 두 개의 워크플로우가 시작되었는지 확인합니다.
