---
solution: Campaign Standard
product: campaign
title: 외부 파라미터로 워크플로우 호출
description: 이 섹션에서는 외부 매개 변수를 사용한 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---


# 사용 사례 {#use-case}

아래의 사용 사례는 워크플로우 내의 매개 변수를 사용하여 워크플로우를 호출하는 방법을 보여줍니다.

목표는 외부 매개 변수를 사용하여 API 호출에서 워크플로우를 트리거하는 것입니다. 이 워크플로우는 파일의 데이터를 데이터베이스에 로드하고 관련 대상을 만듭니다. 대상이 만들어지면 API 호출에 정의된 외부 매개 변수를 사용하여 개인화된 메시지를 전송하도록 두 번째 워크플로우가 트리거됩니다.

이 사용 사례를 수행하려면 아래 작업을 수행해야 합니다.

1. **외부 매개 변수를 사용하여** Workflow 1을 트리거하는 API 호출을 만듭니다. [1단계 참조:API 호출](../../automating/using/use-case-calling-workflow.md#step-1--configuring-the-api-call)을 구성하는 중입니다.
1. **빌드 워크플로 1**:워크플로우가 파일을 전송하여 데이터베이스로 로드합니다. 그런 다음 데이터가 비어 있는지 여부를 테스트하고 해당 프로필을 대상에 저장합니다. 마지막으로 워크플로우 2가 트리거됩니다. [단계 2:워크플로우 1](../../automating/using/use-case-calling-workflow.md#step-2--configuring-workflow-1) 구성
1. **빌드 워크플로 2**:워크플로우는 워크플로우 1에서 만든 고객을 읽은 다음, 매개 변수에 맞게 맞춤화된 세그먼트 코드와 함께 개인화된 메시지를 프로필에 보냅니다. [단계 3:워크플로 2](../../automating/using/use-case-calling-workflow.md#step-3--configuring-workflow-2) 구성.

![](assets/extsignal_uc_process.png)

## 사전 요구 사항 {#prerequisites}

워크플로우를 구성하기 전에 각 워크플로우에서 **[!UICONTROL External signal]** 활동을 사용하여 워크플로우 1 및 2를 만들어야 합니다. 이렇게 하면 워크플로우를 호출할 때 이러한 신호 활동을 타깃팅할 수 있습니다.

## 1단계:API 호출 {#step-1--configuring-the-api-call} 구성

매개 변수를 사용하여 워크플로우 1을 트리거하는 API 호출을 만듭니다. API 호출 구문에 대한 자세한 내용은 [Campaign Standard REST API 설명서](../../api/using/triggering-a-signal-activity.md)를 참조하십시오.

이 경우 아래 매개 변수를 사용하여 Workflow를 호출하려고 합니다.

* **fileToTarget**:데이터베이스로 가져올 파일의 이름입니다.
* **discountDesc**:할인 혜택을 위해 납품에 표시할 설명입니다.

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

## 2단계:워크플로 구성 1 {#step-2--configuring-workflow-1}

워크플로우 1은 아래와 같이 빌드됩니다.

* **[!UICONTROL External signal]** 활동:워크플로우 내에서 사용하기 위해 외부 매개 변수를 선언해야 하는 경우입니다.
* **[!UICONTROL Transfer file]** 활동:매개 변수에 정의된 이름으로 파일을 가져옵니다.
* **[!UICONTROL Load file]** 활동:가져온 파일의 데이터를 데이터베이스에 로드합니다.
* **[!UICONTROL Update data]** 활동:가져온 파일의 데이터로 데이터베이스를 삽입하거나 업데이트합니다.
* **[!UICONTROL Test]** 활동:가져온 데이터가 있는지 확인합니다.
* **[!UICONTROL Save audience]** 활동:파일에 데이터가 들어 있으면 해당 프로파일을 대상에 저장합니다.
* **[!UICONTROL End activity]** 활동:워크플로 2를 호출하고 그 안에 사용할 매개 변수를 사용합니다.

![](assets/extsignal_uc_wkf1.png)

아래 절차에 따라 워크플로우를 구성합니다.

1. API 호출에 정의된 매개 변수를 선언합니다. 이렇게 하려면 **[!UICONTROL External signal]** 활동을 연 다음 매개 변수의 이름과 유형을 추가합니다.

   ![](assets/extsignal_uc1.png)

1. 데이터를 데이터베이스에 가져올 **[!UICONTROL Transfer file]** 활동을 추가합니다. 이렇게 하려면 작업을 드래그 앤 드롭한 다음 열고 **[!UICONTROL Protocol]** 탭을 선택합니다.
1. **[!UICONTROL Use a dynamic file path]** 옵션을 선택한 다음 전송할 파일로 **fileToTarget** 매개 변수를 사용합니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc2.png)

1. 파일의 데이터를 데이터베이스에 로드합니다.

   이렇게 하려면 **[!UICONTROL Load file]** 활동을 워크플로우로 드래그하여 놓은 다음 필요에 따라 구성합니다.

1. 가져온 파일의 데이터로 데이터베이스를 삽입하고 업데이트합니다.

   이렇게 하려면 **[!UICONTROL Update data]** 활동을 드래그하여 놓은 다음 **[!UICONTROL Identification]** 탭을 선택하여 조정 기준을 추가합니다(이 경우 **email** 필드).

   ![](assets/extsignal_uc3.png)

1. **[!UICONTROL Fields to update]** 탭을 선택한 다음 데이터베이스에서 업데이트할 필드를 지정합니다(이 경우 **firstname** 및 **email** 필드).

   ![](assets/extsignal_uc4.png)

1. 파일에서 데이터를 검색하는지 확인합니다. 이렇게 하려면 **[!UICONTROL Test]** 활동을 워크플로우로 드래그 앤 드롭한 다음 **[!UICONTROL Add an element]** 단추를 클릭하여 조건을 추가합니다.
1. 조건의 이름을 지정하고 정의합니다. 이 경우 아웃바운드 전환에 아래 구문을 포함한 데이터가 포함되어 있는지 테스트하려고 합니다.

   ```
   $long(vars/@recCount)>0
   ```

   ![](assets/extsignal_uc5.png)

1. 데이터가 검색되면 대상에 저장합니다. 이렇게 하려면 **[!UICONTROL Save audience]** 활동이 비어 있지 않은 **Target에** 전환을 추가한 다음 엽니다.
1. **[!UICONTROL Use a dynamic label]** 옵션을 선택한 다음 **fileToTarget** 매개 변수를 대상 레이블로 사용합니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc6.png)

1. 매개 변수를 사용하여 워크플로 2를 호출할 **[!UICONTROL End]** 활동을 드래그 앤 드롭한 다음 엽니다.
1. **[!UICONTROL External signal]** 탭을 선택한 다음 트리거할 워크플로우와 연관된 신호 활동을 지정합니다.
1. 워크플로우 2 내에서 사용할 매개 변수와 관련 값을 정의합니다.

   이 경우, API 호출에 원래 정의된 매개 변수(**fileToTarget** 및 **discountDesc**)와 상수 값(&quot;20% 할인&quot;)을 포함한 추가 **segmentCode** 매개 변수를 전달하려고 합니다.

   ![](assets/extsignal_uc7.png)

워크플로우 1이 구성되었으므로 이제 워크플로우 2를 작성할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../automating/using/use-case-calling-workflow.md#step-3--configuring-workflow-2)을 참조하십시오.

## 3단계:워크플로 구성 2 {#step-3--configuring-workflow-2}

워크플로 2는 아래와 같이 빌드됩니다.

* **[!UICONTROL External signal]** 활동:워크플로우 내에서 사용하기 위해 매개 변수를 선언해야 하는 경우입니다.
* **[!UICONTROL Read audience]** 활동:워크플로우 1에 저장된 대상자를 읽습니다.
* **[!UICONTROL Email delivery]** 활동:매개 변수를 사용하여 개인화된 타깃팅된 대상자에게 반복 메시지를 전송합니다.

![](assets/extsignal_uc_wkf2.png)

아래 절차에 따라 워크플로우를 구성합니다.

1. 워크플로우 1에서 정의된 매개 변수를 선언합니다.

   이렇게 하려면 **[!UICONTROL External signal]** 활동을 연 다음 Workflow 1의 **[!UICONTROL End]** 활동에 정의된 각 매개 변수의 이름과 유형을 추가합니다.

   ![](assets/extsignal_uc8.png)

1. 워크플로우 1에 저장된 대상을 사용합니다. 이렇게 하려면 **[!UICONTROL Read audience]** 활동을 워크플로우로 드래그하여 놓은 다음 엽니다.
1. **[!UICONTROL Use a dynamic audience]** 옵션을 선택한 다음 읽을 대상의 이름으로 **fileToTarget** 매개 변수를 사용합니다.

   ```
   $(vars/@fileToTarget)
   ```

   ![](assets/extsignal_uc9.png)

1. **segmentCode** 매개 변수에 따라 아웃바운드 전환 이름을 지정합니다.

   이렇게 하려면 **[!UICONTROL Transition]** 탭을 선택하고 **[!UICONTROL Use a dynamic segment code]** 옵션을 선택합니다.

1. 아웃바운드 전환 이름으로 **segmentCode** 매개 변수를 사용합니다.

   ```
   $(vars/@segmentCode)
   ```

   ![](assets/extsignal_uc10.png)

1. **[!UICONTROL Email delivery]** 활동을 드래그 앤 드롭하여 잠재고객에게 메시지를 보냅니다.
1. 메시지에 사용할 매개 변수를 식별하여 **discountDesc** 매개 변수로 개인화합니다. 이렇게 하려면 활동의 고급 옵션을 연 다음 매개 변수 이름과 값을 추가합니다.

   ![](assets/extsignal_uc10b.png)

1. 이제 메시지를 구성할 수 있습니다. 활동을 연 다음 **[!UICONTROL Recurring email]**&#x200B;을 선택합니다.

   ![](assets/extsignal_uc11.png)

1. 사용할 템플릿을 선택한 다음 필요에 따라 이메일 속성을 정의합니다.
1. **discountDesc** 매개 변수를 개인화 필드로 사용합니다. 이렇게 하려면 개인화 필드 목록에서 선택합니다.

   ![](assets/extsignal_uc13.png)

1. 이제 메시지 구성을 완료한 다음 평소대로 보낼 수 있습니다.

   ![](assets/extsignal_uc14.png)

## 워크플로 {#executing-the-workflows} 실행

워크플로우가 만들어지면 실행할 수 있습니다. API 호출을 수행하기 전에 두 개의 워크플로우가 시작되었는지 확인합니다.
