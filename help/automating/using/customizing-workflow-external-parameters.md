---
title: 외부 파라미터로 워크플로우 호출
description: 이 섹션에서는 외부 매개 변수를 사용한 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
page-status-flag: never-activated
uuid: beccd1b6-8e6d-4504-9152-9ff537459c4a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 1676da91-55e3-414f-bcd3-bb0804b682bd
translation-type: tm+mt
source-git-commit: 121b36056317cc89909607220f988c02ae470f08
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 1%

---


# Customizing a workflow with external parameters {#customizing-a-workflow-with-external-parameters}

워크플로우가 트리거되면 매개 변수가 이벤트 변수에 수집되고 워크플로우의 활동을 사용자 지정하는 데 사용할 수 있습니다.

예를 들어 활동에서 읽을 대상, **[!UICONTROL Read audience]** 활동에서 전송할 파일의 이름 등을 정의하는 데 사용할 수 **[!UICONTROL Transfer file]** 있습니다. (see [this page](../../automating/using/customizing-workflow-external-parameters.md)).

## 이벤트 변수 사용 {#using-events-variables}

이벤트 변수는 [표준 구문을 따라야 하는 표현식 내에서 사용됩니다](../../automating/using/advanced-expression-editing.md#standard-syntax).

이벤트 변수를 사용하는 구문은 아래 형식을 따르고 활동에 정의된 매개 변수 이름을 사용해야 합니다(외부 신호 활동에서 매개 변수 선언 **[!UICONTROL External signal]** 참조 [](../../automating/using/declaring-parameters-external-signal.md)).

```
$(vars/@parameterName)
```

이 구문에서 **$** 함수는 **문자열** 데이터 유형을 반환합니다. 다른 데이터 유형을 지정하려면 다음 함수를 사용하십시오.

* **$long**:정수 숫자.
* **$float**:소수.
* **$부울**:true/false.
* **$datetime**:타임스탬프.

활동에서 변수를 사용하는 경우 이 인터페이스는 변수를 호출하는 데 도움이 됩니다.

![](assets/extsignal_callparameter.png)

* ![](assets/extsignal_picker.png):워크플로우에서 사용할 수 있는 모든 변수 중에서 events 변수를 선택합니다.

   ![](assets/wkf_test_activity_variables.png)

* ![](assets/extsignal_expression_editor.png):변수와 함수를 결합하는 표현식을 편집합니다( [이 페이지](../../automating/using/advanced-expression-editing.md)참조).

   ![](assets/wkf_test_activity_variables_expression.png)

   이 목록은 복잡한 필터링을 수행할 수 있는 기능을 제공합니다. 이러한 기능은 [이 섹션에 자세히 설명되어 있습니다](../../automating/using/list-of-functions.md).

   또한 아래 기능을 사용할 수 있습니다. 이 기능은 외부 매개 변수를 사용하여 워크플로우를 호출한 후 이벤트 변수를 사용할 수 있도록 하는 모든 활동에서 사용할 수 있습니다( [이 섹션 참조](../../automating/using/customizing-workflow-external-parameters.md#customizing-activities-with-events-variables)).

   | 이름 | 설명 | 구문 |
   ---------|----------|---------
   | EndWith | 문자열(1번째 매개 변수)이 특정 문자열(2번째 매개 변수)로 끝나는지 여부를 나타냅니다. | EndWith(&lt;String>,&lt;String>) |
   | startWith | 문자열(1번째 매개 변수)이 특정 문자열(2번째 매개 변수)로 시작하는지 여부를 나타냅니다. | startWith(&lt;String>,&lt;String>) |
   | Extract | 구분 기호를 사용하여 문자열의 첫 번째 문자를 반환합니다. | Extract(&lt;String>,&lt;Separator>) |
   | ExtractRight | 구분 기호를 사용하여 문자열의 마지막 문자를 반환합니다. | ExtractRight(&lt;문자열>,&lt;구분 문자>) |
   | DateFormat | 두 번째 매개 변수에 지정된 형식을 사용하여 날짜를 지정합니다(예: &#39;%4Y%2M%2D&#39;) | DateFormat(&lt;Date>,&lt;Format>) |
   | 파일 이름 | 파일 경로의 이름을 반환합니다. | FileName(&lt;String>) |
   | FileExt | 파일 경로 확장명을 반환합니다. | FileExt(&lt;String>) |
   | IsNull | 문자열 또는 날짜가 null인지 여부를 나타냅니다. | IsNull(&lt;String/date>) |
   | UrlUtf8Encode | URL을 UTF8로 인코딩합니다. | UrlUtf8Encode(&lt;String>) |

## 이벤트 변수를 사용하여 활동 사용자 정의 {#customizing-activities-with-events-variables}

이벤트 변수는 아래 섹션에 나열된 여러 활동을 사용자 지정하는 데 사용할 수 있습니다. 활동에서 변수를 호출하는 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/customizing-workflow-external-parameters.md#using-events-variables).

**[!UICONTROL Read audience]** 활동:이벤트 변수를 기반으로 타깃팅할 대상을 정의합니다. 활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/read-audience.md).

![](assets/extsignal_activities_audience.png)

**[!UICONTROL Test]** 활동:이벤트 변수를 기반으로 조건을 만듭니다. 활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/test.md).

![](assets/extsignal_activities_test.png)

**[!UICONTROL Transfer file]** 활동:이벤트 변수에 따라 전송할 파일을 사용자 정의합니다. 활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/transfer-file.md).

![](assets/extsignal_activities_transfer.png)

**[!UICONTROL Query]** 활동:매개 변수는 이벤트 변수와 함수를 결합하는 표현식을 사용하여 쿼리에서 참조할 수 있습니다. 이렇게 하려면 규칙을 추가한 다음 **[!UICONTROL Advanced mode]** 링크를 클릭하여 표현식 편집 창에 액세스합니다( [고급 표현식 편집](../../automating/using/advanced-expression-editing.md)참조).

활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/query.md).

![](assets/extsignal_activities_query.png)

**[!UICONTROL Channels]** 활동:이벤트 변수를 기반으로 전달 개인화

>[!NOTE]
>
>배달 매개 변수의 값은 배달을 준비할 때마다 검색됩니다.
>
>반복 납품 준비는 배달 **총괄 기간을 기반으로 합니다**. 예를 들어 집계 기간이 &quot;일별&quot;일 경우, 하루 한 번만 배달이 다시 준비됩니다. 배달 매개 변수의 값이 일 중에 수정되는 경우 이미 한 번 준비되었기 때문에 배달 시 업데이트되지 않습니다.
>
>워크플로우를 하루에 여러 번 호출할 계획인 경우 배달 매개 변수가 매번 업데이트되도록 [!UICONTROL No aggregation] 옵션을 사용하십시오. 반복 배달 구성에 대한 자세한 내용은 [이 섹션을 참조하십시오](/help/automating/using/email-delivery.md#configuration).

이벤트 변수를 기반으로 배달을 개인화하려면 먼저 사용할 변수를 전달 활동으로 선언해야 합니다.

1. 활동을 선택한 다음 ![](assets/dlv_activity_params-24px.png) 단추를 클릭하여 설정에 액세스합니다.
1. 탭을 **[!UICONTROL General]** 선택한 다음 게재에서 개인화 필드로 사용할 이벤트 변수를 추가합니다.

   ![](assets/extsignal_activities_delivery.png)

1. **[!UICONTROL Confirm]** 버튼을 클릭합니다.

선언된 이벤트 변수는 이제 개인화 필드 목록에서 사용할 수 있습니다. 게재에서 다음 작업을 수행할 수 있습니다.

* 게재에 사용할 템플릿의 이름을 정의합니다.

   >[!NOTE]
   >
   >이 작업은 **반복 배달에만** 사용할 수 있습니다.

   ![](assets/extsignal_activities_template.png)

* 전달 개인화:개인화 필드를 선택하여 배달을 구성할 때 이벤트 변수를 **[!UICONTROL Workflow parameters]** 요소에서 사용할 수 있습니다. 이러한 필드를 개인화 필드로 사용할 수 있습니다. 예를 들어 배달 주체, 발신자 등을 정의할 수 있습니다.

   전달 개인화는 [이 섹션에 자세히 설명되어 있습니다](../../designing/using/personalization.md).

   ![](assets/extsignal_activities_perso.png)

**세그먼트 코드**:이벤트 변수를 기반으로 세그먼트 코드를 정의합니다.

>[!NOTE]
>
>이 작업은 세그먼트 코드(예: **[!UICONTROL Query]** 또는 활동)를 정의할 수 있는 모든 활동에서 수행할 수 **[!UICONTROL Segmentation]** 있습니다.

![](assets/extsignal_activities_segment.png)

**배달 레이블**:이벤트 변수를 기반으로 배달 레이블을 정의합니다.

![](assets/extsignal_activities_label.png)
