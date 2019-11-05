---
title: 고급 표현식 편집
description: 쿼리 에디션 마법사를 사용하여 고급 표현식을 정의할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: a635f999-27ce-41e0-a88c-8a3882e31efe
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 필터링
discoiquuid: 4375153c-0621-4d4c-bfcc-66d157f04f6c
context-tags: queryFilter,overview;audience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 고급 표현식 편집{#advanced-expression-editing}

## 고급 표현식 편집 정보 {#about-advanced-expression-editing}

표현식을 편집하면 규칙을 형성하기 위한 조건을 수동으로 입력해야 합니다.

이 모드에서는 고급 함수를 사용할 수 있습니다. 이러한 함수를 사용하면 날짜, 문자열, 숫자 필드, 정렬 등과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있습니다.

표현식을 편집할 때 이벤트 변수를 사용할 수도 있습니다. 자세한 내용은 이벤트 변수를 사용하여 [활동 사용자 지정](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) 섹션을 참조하십시오.

다음 순서로 표현식을 편집할 수 있습니다.

* 규칙을 추가할 때 사용할 수 있는 **[!UICONTROL Advanced mode]** 옵션을 통해 쿼리를 정의합니다.

   ![](assets/expression_editor_2.png)

* 워크플로우에서 표현식을 편집합니다. 예를 들어 활동에 데이터를 더 추가합니다.
* 가시성 조건을 편집하여 HTML 컨텐츠 편집기에서 블록이 표시되는 방식을 정의합니다. 이 경우 표현식은 JavaScript 형식으로 편집되며, 고급 함수를 표준으로 사용할 수 없습니다.

## 표현식 편집 {#edit-an-expression}

고급 표현식 에디션을 사용하면 요구 사항에 맞는 표현식을 수동으로 정의할 수 있습니다.

표현식 편집은 워크플로우를 만드는 동안 대상 창에서 이메일 또는 쿼리 활동에 사용할 수 있습니다.

1. 고급 표현식 편집 [](../../automating/using/advanced-expression-editing.md#about-advanced-expression-editing) 정보 섹션에 설명된 방법 중 하나를 통해 표현식 편집 창에 액세스합니다. 여기에는 다음 요소가 포함됩니다.

   * 표현식이 정의된 입력 필드입니다.
   * 표현식에 사용할 수 있고 쿼리의 타깃팅 차원에 해당하는 사용 가능한 필드 목록( [차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)타깃팅 참조)
   * 범주별로 정렬된 사용 가능한 함수 목록입니다.
   ![](assets/expression_editor_1.png)

1. 해당 필드에 직접 표현식을 입력하거나 사용 가능한 필드 및 함수 목록을 사용하여 표현식을 편집합니다.

   필드나 표현식을 두 번 클릭하면 커서가 놓인 표현식에 추가됩니다.

   워크플로의 이벤트 변수를 사용하여 표현식을 작성할 수 있습니다. 자세한 내용은 이벤트 변수를 사용하여 [활동 사용자 지정](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables) 섹션을 참조하십시오.

1. 필요한 경우 규칙에 특정 이름을 지정합니다. 입력한 이름은 쿼리 편집기 작업 영역에 규칙 이름으로 표시됩니다.

표현식을 편집하면 필요에 따라 모집단을 타깃팅하기 위해 대상자 표현식을 개인화할 수 있습니다.

**관련 항목:**

* [표현식 구문](../../automating/using/advanced-expression-editing.md#expression-syntax)
* [함수 목록](../../automating/using/list-of-functions.md)

## 표현식 구문 {#expression-syntax}

### 표준 구문 {#standard-syntax}

표준 표현식은 다음 구문 요소를 참조하는 하나 또는 여러 조건으로 구성됩니다.

* 각 조건은 **&lt;value1&gt; &lt;comparison operator&gt; &lt;value2&gt;** 형식을 사용합니다.

   * **&lt;value1&gt;** 는 필드 또는 함수입니다. 예를 들어 **@created** for the date a profile was created **or** Year(@created)for the year for the year an created.
   * **&lt;comparison operator&gt;** 는 비교 연산자 [섹션에 나열된 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 중 하나입니다. 이 연산자는 **&lt;value1&gt;** 및 **&lt;value2&gt;**&#x200B;간의 비교 메서드를 정의합니다.
   * **&lt;value2&gt;** 는 수동으로 입력되는 필드, 함수 또는 값입니다.
   >[!NOTE]
   >
   >&lt;value1&gt; **** 및 **&lt;value2&gt;** 형식 데이터는 동일해야 합니다. 예를 들어 **&lt;value1&gt;** 이 **날짜이면** &lt;value2&gt;날짜도 되어야 합니다.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL AND]**:두 조건이 교차됩니다.
   * **[!UICONTROL OR]**:두 조건이 결합됩니다.

예:

```
Year(@created) = Year(GetDate()) AND Month(@created) = Month(GetDate())
```

이 예에서는 작성 날짜가 현재 월과 연도인 프로필이 타깃팅됩니다.

### JavaScript 구문 {#javascript-syntax}

HTML 콘텐츠 편집기의 텍스트 유형 블록의 가시성 조건을 정의할 때는 JavaScript 유형 구문의 표현식을 사용해야 합니다.

JavaScript 표현식은 하나 이상의 조건으로 구성되며 다음 구문 요소를 사용합니다.

* 각 조건은 **&lt;context&gt; &lt;comparison operator&gt; &lt;value2&gt;** 형식을 사용합니다.

   * **&lt;context&gt;** 은 컨텍스트를 지정할 수 있는 필드 또는 함수입니다. 예: **context.profile.프로필의 이메일 주소 또는** context.profile.firstName.length() **프로필 이름의 문자 수에 대한 @email** .
   * **&lt;comparison operator&gt;** 는 비교 연산자 [섹션에 나열된 연산자](../../automating/using/advanced-expression-editing.md#comparison-operators) 중 하나입니다. 이 연산자는 **&lt;context&gt;** 및 **&lt;value2&gt;**&#x200B;간의 비교 방법을 정의합니다.
   * **&lt;value2&gt;** 는 수동으로 입력되는 필드, 함수 또는 값입니다.
   >[!NOTE]
   &lt;context&gt; **** 및 **&lt;value2&gt;** 형식 데이터는 동일해야 합니다. 예를 들어 **&lt;context&gt;** 가 날짜이면 **&lt;value2&gt;** 날짜도 되어야 합니다.

* 여러 조건을 사용하려면 논리 연산자를 사용하여 결합할 수 있습니다.

   * **[!UICONTROL &&]**:두 조건이 교차됩니다.
   * **[!UICONTROL ||]**:두 조건이 결합됩니다.

예:

```
context.profile.age > 21 && context.profile.firstName.length() > 0
```

이 예에서는 21세 이상의 프로파일과 이름이 제공된 프로파일이 있습니다( **firstName** 필드에 하나 이상의 문자가 포함되어 있음을 나타냅니다).

## 비교 연산자 {#comparison-operators}

일부 규칙의 경우 쿼리 편집기를 사용하여 조건을 정의하는 값을 선택할 수 있습니다.

조건은 다음 연산자 중 하나를 사용하여 값에 연결해야 합니다.

<table> 
 <thead> 
  <tr> 
   <th> 연산자<br /> </th> 
   <th> 표준 구문<br /> </th> 
   <th> JavaScript 구문<br /> </th> 
   <th> 설명<br /> </th> 
   <th> 예<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <span class="uicontrol">같음</span><br /> </td> 
   <td> =<br /> </td> 
   <td> ==<br /> </td> 
   <td> 첫 번째 값은 두 번째 값과 완전히 동일해야 합니다.<br /> </td> 
   <td> <strong>@lastName =</strong> Martin은 성이 'Martin'인 프로필과 동일한 문자만 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">보다 큼</span><br /> </td> 
   <td> &gt;<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 커야 합니다.<br /> </td> 
   <td> <strong>@age &gt; 50은</strong> '50' 이상, '51', '52' 등 "50세 이상" 프로파일을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">미만</span><br /> </td> 
   <td> &lt;<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 절대적으로 작아야 합니다.<br /> </td> 
   <td> <strong>@created &lt; DaysAgo(100)</strong> 는 100일 전 데이터베이스에 작성된 모든 프로필을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">크거나 같음</span><br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 크거나 같아야 합니다.<br /> </td> 
   <td> <strong>@age &gt;= 30은</strong> 30세 이상의 오래된 프로파일을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">작거나 같음</span><br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> 첫 번째 값은 두 번째 값보다 작거나 같아야 합니다.<br /> </td> 
   <td> <strong>@age &lt;= 60은</strong> 60세 이하의 프로파일을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Different </span><br /> </td> 
   <td> !=<br /> </td> 
   <td> !=<br /> </td> 
   <td> 첫 번째 값은 두 번째 값과 달라야 합니다.<br /> </td> 
   <td> <strong>@language != 영어는</strong> 영어로 정의되지 않은 프로파일을 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">포함</span><br /> </td> 
   <td> IN<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> 첫 번째 값은 두 번째 값을 포함해야 합니다.<br /> </td> 
   <td> <strong>@domain in mail</strong>. 여기에서 'mail' 값이 있는 모든 도메인 이름이 결과에 반환됩니다. 따라서 'gmail.com' 도메인 이름은 반환된 결과의 일부를 구성합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">좋아요</span><br /> </td> 
   <td> LIKE<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> <span class="uicontrol">좋아요</span> 기능은 포함 <span class="uicontrol">연산자와 매우</span> 유사합니다. 검색 중인 값에 <span class="uicontrol">%</span> 와일드카드 문자를 삽입할 수 있습니다.<br /> </td> 
   <td> <strong>@lastName LIKE Mart%n</strong>. 여기에서 대체 문자 <strong>%</strong> 는 "조커"로 작동하여 맞춤법이 올바르지 않은 가설 사례에서 "Martin"이라는 이름을 찾습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">좋아요</span> 아님 <br /> </td> 
   <td>  NOT<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> Like와 <span class="uicontrol">유사합니다</span>. 이렇게 하면 입력한 값을 복구할 수 없습니다. 여기에서 입력한 값은 <span class="uicontrol">%</span> 와일드카드 문자를 포함해야 합니다.<br /> </td> 
   <td> <strong>@lastName NOT Smi%h</strong>. 여기에서 받는 사람은 'Smi%h'(so Smith, 등)라는 이름에 해당합니다. 는 결과로 반환되지 않습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">비어</span> 있음 <br /> </td> 
   <td> IS NULL<br /> </td> 
   <td> 해당 없음<br /> </td> 
   <td> 첫 번째 값은 빈 값에 해당되어야 합니다.<br /> </td> 
   <td> <strong>@mobilePhone IS NULL은</strong> 휴대폰 번호가 제공되지 않은 모든 프로필을 검색합니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

