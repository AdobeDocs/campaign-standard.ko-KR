---
title: 고급 표현식 편집
seo-title: 고급 표현식 편집
description: 고급 표현식 편집
seo-description: 쿼리 에디션 마법사를 사용하여 고급 표현식을 정의할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: A 635 F 999-27 CE -41 E 0-A 88 C -8 A 3882 E 31 EFE
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 필터링 데이터
discoiquuid: 4375153 C -0621-4 D 4 C-BFCC -66 D 157 F 04 F 6 C
context-tags: Queryfilter, overview; 대상, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Advanced expression editing{#advanced-expression-editing}

## About advanced expression editing {#about-advanced-expression-editing}

표현식을 편집하면 규칙을 양식에 수동으로 입력하는 조건이 포함됩니다.

이 모드에서는 고급 기능을 사용할 수 있습니다. 이러한 함수를 사용하면 날짜, 문자열, 숫자 필드, 정렬 등의 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있습니다.

표현식을 편집할 때 이벤트 변수를 사용할 수도 있습니다. For more on this, refer to the [Customizing activities with events variables](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) section.

다음 작업을 위해 표현식을 편집할 수 있습니다.

* Define a query, via the **[!UICONTROL Advanced mode]** option which is available when a rule is added.

   ![](assets/expression_editor_2.png)

* 워크플로우에서 표현식을 편집합니다. 예를 들어 활동에 데이터를 더 추가하려면
* 가시성 조건을 편집하여 HTML 컨텐츠 편집기의 블록이 표시되는 방식을 정의합니다. 이 경우 표현식은 JavaScript 형식으로 편집되며 Advanced Functions as standard를 제공하지 않습니다.

## Edit an expression {#edit-an-expression}

고급 표현식 에디션을 사용하면 요구 사항에 맞는 표현식을 수동으로 정의할 수 있습니다.

표현식 편집은 워크플로우를 만드는 동안 이메일 또는 쿼리 활동을 만드는 동안 대상 창에서 사용할 수 있습니다.

1. Access the expression editing window via one of the methods detailed in the [About advanced expression editing](../../automating/using/advanced-expression-editing.md#about-advanced-expression-editing) section. 여기에는 다음 요소가 포함됩니다.

   * 표현식이 정의된 입력 필드입니다.
   * The list of available fields that can be used in the expression and correspond to the targeting dimension of the query (see [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources)).
   * 카테고리별로 정렬된 사용 가능한 함수 목록입니다.
   ![](assets/expression_editor_1.png)

1. 표현식을 해당 필드에 직접 입력하거나 사용 가능한 필드 및 함수의 목록을 사용하여 표현식을 편집합니다.

   필드 또는 표현식을 두 번 클릭하면 커서가 배치된 표현식에 해당 필드나 표현식이 추가됩니다.

   워크플로우의 이벤트 변수를 사용하여 표현식을 만들 수 있습니다. For more on this, refer to the [Customizing activities with events variables](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) section.

1. 필요한 경우 규칙에 특정 이름을 지정합니다. 입력한 이름은 쿼리 편집기 작업 영역에서 규칙 이름으로 나타납니다.

표현식을 편집하면 필요에 따라 대상 표현식을 개인화하여 모집단을 타깃팅할 수 있습니다.

**관련 항목:**

* [표현식 구문](../../automating/using/advanced-expression-editing.md#expression-syntax)
* [함수 목록](../../automating/using/list-of-functions.md)

## Expression Syntax {#expression-syntax}

### Standard syntax {#standard-syntax}

표준 표현식은 다음 구문 요소를 참조하는 하나 또는 여러 개의 조건으로 구성됩니다.

* Each condition takes the form of **&lt;value1&gt; &lt;comparison operator&gt; &lt;value2&gt;** whereby:

   * **&lt; value 1 &gt;** 는 필드 또는 함수입니다. For example **@created** for the date a profile was created or **Year(@created)** for the year a profile was created.
   * **&lt; 비교 연산자 &gt;** 는 [비교 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 섹션에 나열된 연산자 중 하나입니다. This operator defines the comparison method between **&lt;value1&gt;** and **&lt;value2&gt;**.
   * **&lt; value 2 &gt;** 는 수동으로 입력된 필드, 함수 또는 값입니다.
   >[!NOTE]
   >
   >**&lt; value 1 &gt;** 및 **&lt; value 2 &gt;** 유형 데이터는 동일해야 합니다. For example, if **&lt;value1&gt;** is a date, then **&lt;value2&gt;** must also be a date.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL AND]**: 두 조건이 교차합니다.
   * **[!UICONTROL OR]**: 두 가지 조건이 결합됩니다.

예를 들면 다음과 같습니다.

```
Year(@created) = Year(GetDate()) AND Month(@created) = Month(GetDate())
```

이 예에서는 작성 날짜가 현재 월과 연도에 있는 프로필이 타깃팅됩니다.

### JavaScript syntax {#javascript-syntax}

HTML 컨텐츠 편집기의 텍스트 유형 블록에 대한 가시성 조건을 정의할 때는 JavaScript 유형 구문으로 표현식을 사용해야 합니다.

JavaScript 표현식은 하나 또는 여러 개의 조건으로 구성되며, 다음과 같은 구문 요소를 사용합니다.

* Each condition takes the form of **&lt;context&gt; &lt;comparison operator&gt; &lt;value2&gt;** whereby:

   * **&lt; context &gt;** 는 컨텍스트를 지정할 수 있는 필드 또는 함수입니다. **예: context. profile.@email** for a profile's email address or **context.profile.firstName.length()** for the number of characters of a profile's first name.
   * **&lt; 비교 연산자 &gt;** 는 [비교 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 섹션에 나열된 연산자 중 하나입니다. This operator defines the comparison method between **&lt;context&gt;** and **&lt;value2&gt;**.
   * **&lt; value 2 &gt;** 는 수동으로 입력된 필드, 함수 또는 값입니다.
   >[!NOTE]
   **&lt; context &gt;** 및 **&lt; value 2 &gt;** 유형 데이터는 동일해야 합니다. For example, if **&lt;context&gt;** is a date, then **&lt;value2&gt;** must also be a date.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL &&]**: 두 조건이 교차합니다.
   * **[!UICONTROL ||]**: 두 가지 조건이 결합됩니다.

예를 들면 다음과 같습니다.

```
context.profile.age > 21 && context.profile.firstName.length() > 0
```

In this example, profiles older than 21 years of age and whose first name has been provided (symbolized by the fact that the **firstName** field contains at least one character).

## Comparison operators {#comparison-operators}

일부 규칙의 경우 쿼리 편집기에서 조건을 정의할 값을 선택할 수 있습니다.

조건은 다음 연산자 중 하나를 사용하여 값에 연결해야 합니다.

<table> 
 <thead> 
  <tr> 
   <th> Operator<br /> </th> 
   <th> Standard syntax<br /> </th> 
   <th> JavaScript syntax<br /> </th> 
   <th> Description<br /> </th> 
   <th> Example<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <span class="uicontrol">같음</span><br /> </td> 
   <td> =<br /> </td> 
   <td> ==<br /> </td> 
   <td> The first value must be completely identical to the second value.<br /> </td> 
   <td> <strong>@ Lastname = Martin</strong> 는 성이'Martin'인 프로필을 검색하며 이러한 문자만 사용합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보다 큼</span><br /> </td> 
   <td> &gt;<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> The first value must categorically be more than the second value.<br /> </td> 
   <td> <strong>@ AGE &gt; 50</strong> 는 50 보다 오래된 프로필, so ' 51 ',' 52 ' 등을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보다 작음</span><br /> </td> 
   <td> &lt;<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> The first value must categorically be less than the second value.<br /> </td> 
   <td> <strong>@ created &lt; daysago (100)</strong> 100 일 전 데이터베이스에 생성된 모든 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">크거나 같음</span><br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> The first value must be more than or equal to the second value.<br /> </td> 
   <td> <strong>@ age &gt; = 30</strong> 는 30 세 이상의 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">작거나 같음</span><br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> The first value must be less than or equal to the second value.<br /> </td> 
   <td> <strong>@ age &lt; = 60</strong> 는 60 이하의 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">different </span><br /> </td> 
   <td> !=<br /> </td> 
   <td> !=<br /> </td> 
   <td> The first value must be different from the second value.<br /> </td> 
   <td> <strong>@ language!= English</strong> retrieves profiles that have not been defined as English speaking.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">contains</span><br /> </td> 
   <td> IN<br /> </td> 
   <td> N/A<br /> </td> 
   <td> The first value must contain the second value.<br /> </td> 
   <td> <strong>@ domain in mail</strong>. 여기에서, 결과에'mail'값이 있는 모든 도메인 이름이 반환됩니다. Consequently, the 'gmail.com' domain name will make up part of the returned results.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">like</span><br /> </td> 
   <td> LIKE<br /> </td> 
   <td> N/A<br /> </td> 
   <td> <span class="uicontrol">like</span> 연산자와 <span class="uicontrol">매우</span> 유사합니다. It lets you insert a <span class="uicontrol">%</span> wild card character in the value that is being searched.<br /> </td> 
   <td> <strong>@ Lastname (예: Mart % n</strong>). Here, the substitution character <strong>%</strong> serves as a "joker" to find the name "Martin" in the hypothetical case that the spelling is not correct.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">좋아요 아님</span><br /> </td> 
   <td> NOT<br /> </td> 
   <td> N/A<br /> </td> 
   <td> Is similar to <span class="uicontrol">Like</span>. 이렇게 하면 입력한 값을 복구할 수 없습니다. Here too, the entered value must contain the <span class="uicontrol">%</span> wild card character.<br /> </td> 
   <td> <strong>@ Lastname는 (는) SMI % H</strong>입니다. 여기에서 받는 사람은 이름'smi % h ' (so Smith 등) 에 해당합니다. are not returned as a result.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">비어 있음</span><br /> </td> 
   <td> IS NULL<br /> </td> 
   <td> N/A<br /> </td> 
   <td> The first value must correspond to an empty value.<br /> </td> 
   <td> <strong>@ Mobilephone는 휴대폰 번호가 제공되지 않은 모든 프로필을</strong> 검색합니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

