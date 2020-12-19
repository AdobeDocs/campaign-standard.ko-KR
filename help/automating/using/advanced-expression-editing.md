---
solution: Campaign Standard
product: campaign
title: 고급 표현식 편집
description: 쿼리 편집 마법사를 사용하여 고급 표현식을 정의할 수 있습니다.
audience: automating
content-type: reference
topic-tags: filtering-data
context-tags: queryFilter,overview;audience,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 98%

---


# 고급 표현식 편집{#advanced-expression-editing}

## 고급 표현식 편집 기본 정보 {#about-advanced-expression-editing}

표현식을 편집하려면 수동으로 조건을 입력하여 규칙을 형성해야 합니다.

이 모드에서는 고급 기능을 사용할 수 있습니다. 이러한 함수를 사용하면 날짜, 문자열, 숫자 필드, 정렬 등과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있습니다.

표현식을 편집할 때 워크플로우의 이벤트 변수를 사용할 수도 있습니다. 자세한 내용은 [이벤트 변수를 사용하여 활동 사용자 지정](../../automating/using/customizing-workflow-external-parameters.md) 섹션을 참조하십시오.

다음 절차를 수행하여 표현식을 편집할 수 있습니다.

* 규칙을 추가할 때 사용할 수 있는 **[!UICONTROL Advanced mode]** 옵션을 통해 쿼리를 정의합니다.

   ![](assets/expression_editor_2.png)

* 워크플로우에서 표현식을 편집합니다. 예를 들어 활동에 추가 데이터를 추가합니다.
* 가시성 조건을 편집하여 HTML 콘텐츠 편집기에서 블록이 표시되는 방식을 정의합니다. 이 경우 표현식은 JavaScript 포맷으로 편집되며 고급 기능을 표준으로 사용할 수 없습니다.

## 표현식 편집 {#edit-an-expression}

고급 표현식 편집을 사용하면 필요에 따라 표현식을 수동으로 정의할 수 있습니다.

표현식 편집은 이메일을 만드는 동안 대상자 창에서 사용하거나 워크플로우를 만드는 동안 쿼리 활동에서 사용할 수 있습니다.

1. [고급 표현식 편집 기본 정보](../../automating/using/advanced-expression-editing.md#about-advanced-expression-editing) 섹션에 설명된 방법 중 하나를 사용하여 표현식 편집 창에 액세스합니다. 여기에는 다음 요소가 포함됩니다.

   * 표현식이 정의된 입력 필드.
   * 표현식에서 사용할 수 있고 쿼리의 타겟팅 차원에 해당하는 사용 가능한 필드 목록([타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources) 참조).
   * 카테고리별로 정렬한 사용 가능한 함수 목록.

   ![](assets/expression_editor_1.png)

1. 해당 필드에 직접 표현식을 입력하거나 사용 가능한 필드 및 함수 목록을 사용하여 표현식을 편집합니다.

   필드 또는 표현식을 두 번 클릭하면 커서가 위치한 표현식에 추가됩니다.

   워크플로우의 이벤트 변수를 사용하여 표현식을 작성할 수 있습니다. 자세한 내용은 [이벤트 변수를 사용하여 활동 사용자 지정](../../automating/using/customizing-workflow-external-parameters.md) 섹션을 참조하십시오.

1. 필요한 경우 규칙에 특정 이름을 지정합니다. 입력한 이름이 쿼리 편집기 작업 영역에서 규칙 이름으로 표시됩니다.

표현식을 편집하면 필요에 따라 모집단을 타겟팅한 Audiences 표현식을 개인화할 수 있습니다.

**관련 항목:**

* [표현식 구문](../../automating/using/advanced-expression-editing.md#expression-syntax)
* [함수 목록](../../automating/using/list-of-functions.md)

## 표현식 구문 {#expression-syntax}

### 표준 구문 {#standard-syntax}

표준 표현식은 다음 구문 요소와 관련된 하나 또는 여러 조건으로 구성됩니다.

* 각 조건은 **&lt;값1> &lt;비교 연산자> &lt;값2>** 형식을 취합니다.

   * **&lt;값1>**&#x200B;은 필드 또는 함수입니다. 예를 들어 프로필이 생성된 날짜의 경우 **@created** 또는 프로필이 생성된 연도의 경우 **Year(@created)**&#x200B;가 있습니다.
   * **&lt;비교 연산자>**&#x200B;는 [비교 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 섹션에 나열된 연산자 중 하나입니다. 이 연산자는 **&lt;값1>**&#x200B;과 **&lt;값2>** 간의 비교 방법을 정의합니다.
   * **&lt;값2>**&#x200B;는 수동으로 입력되는 필드, 함수 또는 값입니다.

   >[!NOTE]
   >
   >**&lt;값1>** 및 **&lt;값2>**&#x200B;의 형식 데이터는 동일해야 합니다. 예를 들어 **&lt;값1>**&#x200B;이 날짜인 경우 **&lt;값2>**&#x200B;도 날짜여야 합니다.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL AND]**: 두 가지 조건이 교차됩니다.
   * **[!UICONTROL OR]**: 두 가지 조건이 결합됩니다.

예제:

```
Year(@created) = Year(GetDate()) AND Month(@created) = Month(GetDate())
```

이 예에서는 생성 날짜가 현재 월 및 연도인 프로필이 타겟팅됩니다.

### JavaScript 구문 {#javascript-syntax}

HTML 콘텐츠 편집기의 텍스트 유형 블록의 가시성 조건을 정의할 때는 JavaScript 유형 구문이 있는 표현식을 사용해야 합니다.

JavaScript 표현식은 하나 이상의 조건으로 구성되며 다음 구문 요소를 사용합니다.

* 각 조건은 **&lt;컨텍스트> &lt;비교 연산자> &lt;값2>** 형식을 취합니다.

   * **&lt;컨텍스트>**&#x200B;는 컨텍스트를 지정할 수 있는 필드 또는 함수입니다. 예를 들어 **context.profile@email**&#x200B;의 프로필 이메일 주소 또는 **context.profile.firstName.length()**&#x200B;의 프로필 이름의 문자 수가 있습니다.
   * **&lt;비교 연산자>**&#x200B;는 [비교 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 섹션에 나열된 연산자 중 하나입니다. 이 연산자는 **&lt;컨텍스트>**&#x200B;와 **&lt;값2>** 간의 비교 방법을 정의합니다.
   * **&lt;값2>**&#x200B;는 수동으로 입력되는 필드, 함수 또는 값입니다.

   >[!NOTE]
   **&lt;컨텍스트>** 및 **&lt;값2>**&#x200B;의 형식 데이터는 동일해야 합니다. 예를 들어 **&lt;컨텍스트>**&#x200B;가 날짜인 경우 **&lt;값2>**&#x200B;도 날짜여야 합니다.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL &&]**: 두 가지 조건이 교차됩니다.
   * **[!UICONTROL ||]**: 두 가지 조건이 결합됩니다.

예제:

```
context.profile.age > 21 && context.profile.firstName.length() > 0
```

이 예제의 경우 21세 이상이고 이름이 제공된 프로필입니다(**firstName** 필드에 하나 이상의 문자 포함).

## 비교 연산자 {#comparison-operators}

일부 규칙의 경우 쿼리 편집기를 사용하여 조건을 정의할 값을 선택할 수 있습니다.

다음 연산자 중 하나를 사용하여 조건을 값에 연결해야 합니다.

<table> 
 <thead> 
  <tr> 
   <th> 연산자<br /> </th> 
   <th> 표준 구문<br /> </th> 
   <th> JavaScript 구문<br /> </th> 
   <th> 설명<br /> </th> 
   <th> 예제<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <span class="uicontrol">같음</span> <br /> </td> 
   <td> =<br /> </td> 
   <td> ==<br /> </td> 
   <td> 첫 번째 값은 두 번째 값과 완전히 같아야 합니다.<br /> </td> 
   <td> <strong>@lastName = Martin</strong>은 완전히 같은 문자만 사용하여 성이 'Martin'인 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보다 큼</span> <br /> </td> 
   <td> &gt;<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 명확히 커야 합니다.<br /> </td> 
   <td> <strong>@age &gt; 50</strong> 은 '50'보다 나이가 많은 프로필을 검색하므로 '51', '52' 등을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보다 작음</span> <br /> </td> 
   <td> &lt;<br /> </td> 
   <td> &lt;&gt;<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 명확히 작아야 합니다.<br /> </td> 
   <td> <strong>@created &lt; DaysAgo(100)</strong>은 100일 전 데이터베이스에 생성된 모든 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">크거나 같음</span> <br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 크거나 같아야 합니다.<br /> </td> 
   <td> <strong>@age &gt;= 30</strong>은 30세 이상의 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">작거나 같음</span> <br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> &lt;&gt;<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 작거나 같아야 합니다.<br /> </td> 
   <td> <strong>@age &lt;= 60은</strong> 60세 이하의 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">다름 </span> <br /> </td> 
   <td> !=<br /> </td> 
   <td> !=<br /> </td> 
   <td> 첫 번째 값은 두 번째 값과 달라야 합니다.<br /> </td> 
   <td> <strong>@language != English</strong>는 영어를 사용하지 않는 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">포함</span> <br /> </td> 
   <td> IN<br /> </td> 
   <td> N/A<br /> </td> 
   <td> 첫 번째 값은 두 번째 값을 포함해야 합니다.<br /> </td> 
   <td> <strong>@domain IN mail</strong>. 여기서 'mail' 값이 있는 모든 도메인 이름이 결과로 반환됩니다. 따라서 'gmail.com' 도메인 이름은 반환된 결과의 일부를 구성합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">비슷함</span> <br /> </td> 
   <td> LIKE<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> <span class="uicontrol">비슷함</span>은 <span class="uicontrol">포함</span> 연산자와 매우 유사합니다. 검색 중인 값에 <span class="uicontrol">%</span> 와일드카드 문자를 삽입할 수 있습니다.<br /> </td> 
   <td> <strong>@lastName LIKE Mart%n</strong>. 여기서 대체 문자 <strong>%</strong> 는 철자가 틀린 가상의 사례에서 이름 "Martin"을 찾기 위해 "조커" 역할을 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">비슷하지 않음</span> <br /> </td> 
   <td> NOT<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> <span class="uicontrol">비슷함</span>과 유사합니다. 입력한 값을 복구할 수 없습니다. 여기서도 입력한 값은 <span class="uicontrol">%</span> 와일드카드 문자를 포함해야 합니다.<br /> </td> 
   <td> <strong>@lastName NOT Smi%h</strong>. 여기에서 이름 'Smi%h'(Smith 등)에 해당하는 수신자는 결과로 반환되지 않습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">비어 있음</span> <br /> </td> 
   <td> IS NULL<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> 첫 번째 값은 빈 값에 해당해야 합니다.<br /> </td> 
   <td> <strong>@mobilePhone IS NULL</strong>은 휴대전화 번호가 제공되지 않은 모든 프로필을 검색합니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

