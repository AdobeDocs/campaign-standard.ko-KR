---
title: 외부 매개 변수를 사용하여 워크플로우 사용자 정의
description: 이 섹션에서는 외부 매개 변수를 사용하는 워크플로우를 호출하는 방법에 대해 자세히 설명합니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 8c1a47ed-3467-4fcd-8747-86f0e8f15cec
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 1%

---

# 외부 매개 변수를 사용하여 워크플로우 사용자 정의 {#customizing-a-workflow-with-external-parameters}

워크플로우가 트리거되면 매개 변수가 이벤트 변수로 수집되어 워크플로우의 활동을 사용자 지정하는 데 사용할 수 있습니다.

예를 들어 에서 읽을 대상을 정의하는 데 사용할 수 있습니다. **[!UICONTROL Read audience]** 활동:에서 전송할 파일의 이름 **[!UICONTROL Transfer file]** 활동 등 (참조 [이 페이지](../../automating/using/customizing-workflow-external-parameters.md)).

## 이벤트 변수 사용 {#using-events-variables}

Events 변수는 [표준 구문](../../automating/using/advanced-expression-editing.md#standard-syntax).

이벤트 변수를 사용하는 구문은 아래 형식을 따라야 하며,에서 정의한 매개 변수의 이름을 사용해야 합니다. **[!UICONTROL External signal]** 활동(참조) [외부 신호 활동에서 매개 변수 선언](../../automating/using/declaring-parameters-external-signal.md)):

```
$(vars/@parameterName)
```

이 구문에서 **$** 함수 반환 **문자열** 데이터 유형. 다른 유형의 데이터를 지정하려면 다음 함수를 사용합니다.

* **US$long**: 정수입니다.
* **$float**: 십진수입니다.
* **$boolean**: true/false.
* **$datetime**: 타임스탬프.

활동에서 변수를 사용할 때 인터페이스는 변수를 호출하는 데 도움이 됩니다.

![](assets/extsignal_callparameter.png)

* ![](assets/extsignal_picker.png): 워크플로우에서 사용할 수 있는 모든 변수 중에서 이벤트 변수를 선택합니다.

  ![](assets/wkf_test_activity_variables.png)

* ![](assets/extsignal_expression_editor.png): 변수와 함수를 결합한 표현식 편집(참조) [이 페이지](../../automating/using/advanced-expression-editing.md)).

  ![](assets/wkf_test_activity_variables_expression.png)

  이 목록에서는 복잡한 필터링을 수행할 수 있는 함수를 제공합니다. 이러한 기능은에 자세히 설명되어 있습니다. [이 섹션](../../automating/using/list-of-functions.md).

  또한 외부 매개 변수를 사용한 워크플로우를 호출한 후 이벤트 변수를 사용할 수 있는 모든 활동에서 사용할 수 있는 아래 함수를 사용할 수 있습니다(참조) [이 섹션](../../automating/using/customizing-workflow-external-parameters.md#customizing-activities-with-events-variables)):

  | 이름 | 설명 | 구문 |
  | ---------|----------|---------|
  | 끝 문자 | 문자열(1번째 매개 변수)이 특정 문자열(2번째 매개 변수)로 끝나는지 여부를 나타냅니다. | EndWith(&lt;string>,&lt;string>) |
  | startWith | 문자열(1번째 매개 변수)이 특정 문자열(2번째 매개 변수)로 시작하는지 여부를 나타냅니다. | startWith(&lt;string>,&lt;string>) |
  | Extract | 구분 기호를 사용하여 문자열의 첫 번째 문자를 반환합니다. | Extract(&lt;string>,&lt;separator>) |
  | 오른쪽 추출 | 구분 기호를 사용하여 문자열의 마지막 문자를 반환합니다. | ExtractRight(&lt;string>,&lt;separator>) |
  | 날짜 형식 | 두 번째 매개 변수에 지정된 형식을 사용하여 날짜 형식을 지정합니다(예: &#39;%4Y%2M%2D&#39;). | DateFormat(&lt;date>,&lt;format>) |
  | 파일 이름 | 파일 경로의 이름을 반환합니다. | 파일 이름(&lt;string>) |
  | 파일 텍스트 | 파일 경로의 확장명을 반환합니다. | FileExt(&lt;string>) |
  | GetOption | 지정된 함수의 값을 반환합니다. | GetOption(&lt;optionname>) |
  | IsNull | 문자열 또는 날짜가 null인지 보여 줍니다. | IsNull(&lt;string date=&quot;&quot;>) |
  | UrlUtf8Encode | URL을 UTF8로 인코딩합니다. | UrlUtf8Encode(&lt;string>) |

## 이벤트 변수를 사용하여 활동 사용자 지정 {#customizing-activities-with-events-variables}

이벤트 변수는 아래 섹션에 나열된 여러 활동을 사용자 지정하는 데 사용할 수 있습니다. 활동에서 변수를 호출하는 방법에 대한 자세한 내용은 [이 섹션](../../automating/using/customizing-workflow-external-parameters.md#using-events-variables).

**[!UICONTROL Read audience]** 활동: 이벤트 변수를 기반으로 타깃팅할 대상을 정의합니다. 활동 사용 방법에 대한 자세한 내용은 을 참조하십시오. [이 섹션](../../automating/using/read-audience.md).

![](assets/extsignal_activities_audience.png)

**[!UICONTROL Test]** 활동: 이벤트 변수를 기반으로 조건을 작성합니다. 활동 사용 방법에 대한 자세한 내용은 을 참조하십시오. [이 섹션](../../automating/using/test.md).

![](assets/extsignal_activities_test.png)

**[!UICONTROL Transfer file]** 활동: 이벤트 변수를 기반으로 전송할 파일을 사용자 지정합니다. 활동 사용 방법에 대한 자세한 내용은 을 참조하십시오. [이 섹션](../../automating/using/transfer-file.md).

![](assets/extsignal_activities_transfer.png)

**[!UICONTROL Query]** 활동: 이벤트 변수와 함수를 결합한 표현식을 사용하여 쿼리에서 매개 변수를 참조할 수 있습니다. 이렇게 하려면 규칙을 추가한 다음 **[!UICONTROL Advanced mode]** 표현식 편집 창에 액세스하기 위한 링크( 참조) [고급 표현식 편집](../../automating/using/advanced-expression-editing.md)).

활동 사용 방법에 대한 자세한 내용은 을 참조하십시오. [이 섹션](../../automating/using/query.md).

![](assets/extsignal_activities_query.png)

**[!UICONTROL Channels]** 활동: 이벤트 변수를 기반으로 게재를 개인화합니다.

>[!NOTE]
>
>게재가 준비될 때마다 게재 매개 변수의 값이 검색됩니다.
>
>반복 게재 준비는 게재를 기반으로 합니다 **집계 기간**. 예를 들어 집계 기간이 &quot;일별&quot;인 경우 게재는 하루에 한 번만 다시 준비됩니다. 게재 매개 변수의 값이 하루 동안 수정되면 이미 한 번 준비되었으므로 게재에서 업데이트되지 않습니다.
>
>하루에 여러 번 워크플로우를 호출할 계획이라면 [!UICONTROL No aggregation] 옵션을 활성화하면 게재 매개 변수가 매번 업데이트됩니다. 반복 게재 구성에 대한 자세한 내용은 [이 섹션](/help/automating/using/email-delivery.md#configuration).

이벤트 변수를 기반으로 게재를 개인화하려면 먼저 사용할 변수를 게재 활동에 선언해야 합니다.

1. 활동을 선택한 다음 ![](assets/dlv_activity_params-24px.png) 단추를 클릭하여 설정에 액세스합니다.
1. 다음 항목 선택 **[!UICONTROL General]** 탭을 클릭한 다음 게재에서 개인화 필드로 사용할 수 있는 이벤트 변수를 추가합니다.

   ![](assets/extsignal_activities_delivery.png)

1. **[!UICONTROL Confirm]** 버튼을 클릭합니다.

선언된 이벤트 변수는 이제 개인화 필드 목록에서 사용할 수 있습니다. 게재에서 이를 사용하여 아래 작업을 수행할 수 있습니다.

* 게재에 사용할 템플릿의 이름을 정의합니다.

  >[!NOTE]
  >
  >이 작업은 다음에 대해 사용할 수 있습니다. **자동연장** 게재만 해당.

  ![](assets/extsignal_activities_template.png)

* 게재 개인화: 게재를 구성할 개인화 필드를 선택할 때에서 이벤트 변수를 사용할 수 있습니다. **[!UICONTROL Workflow parameters]** 요소를 생성하지 않습니다. 모든 개인화 필드로 사용할 수 있습니다. 예를 들어 게재 제목, 발신자 등을 정의할 수 있습니다.

  게재 개인화는에 자세히 설명되어 있습니다. [이 섹션](../../designing/using/personalization.md).

  ![](assets/extsignal_activities_perso.png)

**세그먼트 코드**: 이벤트 변수를 기반으로 세그먼트 코드를 정의합니다.

>[!NOTE]
>
>이 작업은 다음과 같은 세그먼트 코드를 정의할 수 있는 활동에서 수행할 수 있습니다. **[!UICONTROL Query]** 또는 **[!UICONTROL Segmentation]** 활동.

![](assets/extsignal_activities_segment.png)

**게재 레이블**: 이벤트 변수를 기반으로 게재 레이블을 정의합니다.

![](assets/extsignal_activities_label.png)
