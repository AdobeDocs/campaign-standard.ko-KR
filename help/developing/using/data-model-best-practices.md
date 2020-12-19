---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard의 데이터 모델 모범 사례
description: Adobe Campaign Standard 데이터 모델을 디자인할 때의 모범 사례에 대해 알아보십시오.
audience: developing
content-type: reference
topic-tags: about-custom-resources
context-tags: cusResource,overview;eventCusResource,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1556'
ht-degree: 1%

---


# 데이터 모델 모범 사례{#data-model-best-practices}

이 문서에서는 Adobe Campaign 데이터 모델을 디자인하는 동안 주요 권장 사항에 대해 간략히 설명합니다.


>[!NOTE]
>
>Adobe Campaign 사전 정의된 데이터 모델을 확장하기 위해 리소스를 만들고 수정하려면 [이 섹션](../../developing/using/key-steps-to-add-a-resource.md)을 참조하십시오.
>
>[이 페이지](../../developing/using/datamodel-introduction.md)에서 내장 리소스의 데이터 모델 표현을 찾을 수 있습니다.

## 개요 {#overview}

Adobe Campaign 시스템은 매우 유연하므로 초기 구현 이후에도 확장할 수 있습니다. 그러나 가능성은 무한하지만 현명한 의사 결정을 내리고 데이터 모델 디자인을 시작할 강력한 기반을 구축하는 것이 중요합니다.

이 문서에서는 Adobe Campaign 툴을 적절하게 설계하는 방법을 배울 수 있는 일반적인 사용 사례와 모범 사례를 제공합니다.

## 데이터 모델 아키텍처 {#data-model-architecture}

Adobe Campaign Standard은 온라인과 오프라인 전략을 연계하여 개인화된 고객 경험을 구축할 수 있는 강력한 크로스채널 캠페인 관리 시스템입니다.

### 고객 중심의 접근 방식 {#customer-centric-approach}

대부분의 이메일 서비스 제공업체는 목록 중심의 접근 방식을 통해 고객과 커뮤니케이션하고 있지만 Adobe Campaign은 고객과 고객의 속성을 보다 광범위하게 파악하기 위해 관계형 데이터베이스를 사용합니다.

이 고객 중심의 접근 방법은 아래 차트에 나와 있습니다. 회색 **프로필** 리소스는 모든 것이 작성되고 있는 주 고객 테이블을 나타냅니다.

![](assets/customer-centric-data-model.png)

Adobe Campaign 기본 데이터 모델은 이 [섹션](../../developing/using/datamodel-introduction.md)에 제공됩니다.

<!--You can find a datamodel representation for the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).-->

<!--### What is a customer? {#customer-definition}

If you have customer data in more than one system, you need to determine which solution will allow you to identify records as one person. This work might require rules, eventually a match and merge processes to determine the primary record. This primary record should be the one sent to Adobe Campaign.

While some of this data cleansing might be performed in Adobe Campaign, the recommendation is to run these processes outside and only import clean data in Adobe Campaign. You should keep Campaign as a marketing solution more than a data cleansing tool.

Be able to provide a primary customer record which will be sent to Adobe Campaign.-->

### Adobe Campaign {#data-for-campaign}에 대한 데이터

Adobe Campaign으로 어떤 데이터를 전송해야 합니까? 마케팅 활동에 필요한 데이터를 결정하는 것은 매우 중요합니다.

>[!NOTE]
>
>Adobe Campaign은 데이터 웨어하우스가 아닙니다. 따라서 모든 가능한 고객과 관련 정보를 Adobe Campaign으로 가져오려고 하지 마십시오.

Adobe Campaign에서 속성을 필요로 하는지 여부를 결정하려면 속성이 다음 카테고리 중 하나에 해당하는지 여부를 결정합니다.
* **세그멘테이션**&#x200B;에 사용된 특성
* **데이터 관리 프로세스**&#x200B;에 사용되는 특성(예: 집계 계산)
* **개인화에 사용된 특성**
* **보고**&#x200B;에 사용되는 특성(사용자 지정 프로필 데이터를 기반으로 보고서를 만들 수 있음)

이러한 속성에 해당되지 않는 경우 Adobe Campaign에서 이 속성이 필요하지 않을 가능성이 큽니다.

### 데이터 유형 {#data-types}

시스템의 우수한 아키텍처와 성능을 유지하려면 아래 모범 사례를 따라 Adobe Campaign에서 데이터를 설정하십시오.
* 문자열 필드의 길이는 항상 열로 정의해야 합니다. 기본적으로 Adobe Campaign의 최대 길이는 255자입니다. 그러나 크기가 더 짧은 길이를 초과하지 않을 것을 이미 알고 있는 경우 필드를 더 짧게 유지하는 것이 좋습니다.
* 소스 시스템의 크기가 과대평가되어 도달하지 않았을 것이 확실한 경우 Adobe Campaign에서 소스 시스템보다 필드가 짧은 필드를 가질 수 있습니다. 이것은 Adobe Campaign에서 더 짧은 문자열 또는 더 작은 정수를 의미합니다.

## 데이터 구조 구성 {#configuring-data-structure}

이 섹션에서는 [리소스의 데이터 구조](../../developing/using/configuring-the-resource-s-data-structure.md)를 구성할 때의 우수 사례를 대략적으로 설명합니다.

### 식별자 {#identifiers}

Adobe Campaign 리소스에는 3개의 식별자가 있으며 추가 식별자를 추가할 수 있습니다.

다음 표에서는 이러한 식별자 및 해당 용도를 설명합니다.

>[!NOTE]
>
>표시 이름은 Adobe Campaign 사용자 인터페이스를 통해 사용자에게 표시되는 필드의 이름입니다. 기술 이름은 리소스 정의(및 테이블 열 이름)의 실제 필드 이름입니다.

| 표시 이름 | 기술 이름 | 설명 | 모범 사례 |
|--- |--- |--- |--- |
|  | PKey | <ul><li>PKey는 Adobe Campaign 테이블의 실제 기본 키입니다.</li><li>이 식별자는 일반적으로 특정 Adobe Campaign 인스턴스에 고유합니다.</li><li>Adobe Campaign Standard에서 이 값은 최종 사용자에게 표시되지 않습니다(URL에서는 제외).</li></ul> | <ul><li>[API 시스템](../../api/using/get-started-apis.md)을 통해 PKey 값(실제 키가 아니라 생성/해시된 값)을 검색할 수 있습니다.</li><li>API를 통해 레코드를 검색, 업데이트 또는 삭제하는 것 이외의 경우에는 이 항목을 사용하는 것이 좋습니다.</li></ul> |
| ID | name 또는 internalName | <ul><li>이 정보는 테이블에 있는 레코드의 고유 식별자입니다. 이 값은 수동으로 업데이트할 수 있습니다.</li><li>이 식별자는 다른 Adobe Campaign 인스턴스에 배포할 때 값을 유지합니다. 패키지를 통해 내보낼 수 있도록 생성된 값과 다른 이름이 있어야 합니다.</li><li>이 키는 테이블의 실제 기본 키가 아닙니다.</li></ul> | <ul><li>공백 &quot;&quot;, 세미열 &quot;:&quot; 또는 하이픈 &quot;-&quot;과 같은 특수 문자는 사용하지 마십시오.</li><li>이러한 모든 문자는 밑줄 &quot;_&quot;(허용되는 문자)로 대체됩니다. 예를 들어 &quot;abc-def&quot; 및 &quot;abc:def&quot;는 &quot;abc_def&quot;로 저장되고 서로 덮어쓰게 됩니다.</li></ul> |
| 레이블 | label | <ul><li>레이블은 Adobe Campaign에서 개체 또는 레코드의 비즈니스 식별자입니다.</li><li>이 개체는 공백과 특수 문자를 허용합니다.</li><li>그렇다고 기록이 특유하다고 보지는 않는다.</li></ul> | <ul><li>개체 레이블의 구조를 결정하는 것이 좋습니다.</li><li>Adobe Campaign 사용자의 레코드 또는 개체를 식별할 수 있는 가장 사용자 친화적인 솔루션입니다.</li></ul> |
| ACS ID | acsId | <ul><li>추가 식별자를 생성할 수 있습니다.[ACS ID](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).</li><li>PKey는 Adobe Campaign 사용자 인터페이스에서 사용할 수 없으므로 프로필 레코드를 삽입하는 동안 생성된 고유한 값을 가져오는 솔루션입니다.</li><li>레코드가 Adobe Campaign에 삽입되기 전에 리소스에서 옵션을 활성화한 경우에만 값이 자동으로 생성됩니다.</li></ul> | <ul><li>이 UUID를 조정 키로 사용할 수 있습니다.</li><li>자동 생성된 ACS ID는 워크플로우 또는 패키지 정의에서 참조로 사용할 수 없습니다.</li><li>이 값은 Adobe Campaign 인스턴스에만 적용됩니다.</li></ul> |

### 식별 키 {#keys}

Adobe Campaign에서 만든 각 리소스에는 하나 이상의 고유한 [ID 키](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)가 있어야 합니다.

<!--Most organizations are importing records from external systems. While the physical key of a resource lies behind the PKey attribute, it is possible to determine a custom key in addition.

This custom key is the actual record primary key in the external system feeding Adobe Campaign.

When an out-of-the-box resource has both an internal auto-generated and an internal custom key, the internal key will be set as a unique index in the physical database table.-->

사용자 지정 리소스를 만들 때 다음 두 가지 옵션이 있습니다.

* 자동 생성된 키와 내부 사용자 지정 키의 조합입니다. 이 옵션은 시스템 키가 정수가 아니거나 합성 키인 경우 유용합니다. 정수는 큰 테이블에서 더 높은 성능을 제공하고 다른 테이블과 결합합니다.
* 기본 키를 외부 시스템 기본 키로 사용합니다. 이 솔루션은 일반적으로 서로 다른 시스템 간에 일관된 키를 사용하여 데이터를 가져오고 내보내는 방법을 간소화하므로 선호하는 솔루션입니다.

식별 키는 워크플로우에서 참조로 사용해서는 안 됩니다.

<!--For more on defining identification keys, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).-->

### 인덱스 {#indexes}

Adobe Campaign은 리소스에 정의된 모든 기본 및 내부 키에 [index](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes)를 자동으로 추가합니다.

* Adobe은 성능을 향상시킬 수 있으므로 추가 인덱스를 정의하는 것이 좋습니다.
* 그러나 데이터베이스에서 공간을 사용할 때는 색인이 너무 많이 추가되지 않습니다. 또한 많은 인덱스는 성능에 부정적인 영향을 줄 수 있습니다.
* 정의해야 하는 인덱스를 주의 깊게 선택합니다.

<!--For more on defining indexes, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes).

When you are performing an initial import with very high volumes of data insert in Adobe Campaign database, it is recommended to run that import without custom indexes at first. It will allow to accelerate the insertion process. Once you’ve completed this important import, it is possible to enable the index(es).-->

### 링크 {#links}

다른 리소스와 링크를 정의하는 방법은 [이 섹션](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)에 있습니다.

* 워크플로우에서 테이블을 조인할 수 있지만 Adobe은 데이터 구조 정의에서 직접 리소스 간에 공통 링크를 정의하는 것이 좋습니다.
* 링크는 표의 실제 데이터와 일치하도록 정의해야 합니다. 잘못된 정의는 링크를 통해 검색된 데이터에 영향을 줄 수 있습니다(예: 예기치 않게 레코드를 복제하는 경우).
* 링크 이름을 리소스 이름과 일관되게 지정합니다.링크 이름은 먼 테이블이 무엇인지 이해하는 데 도움이 됩니다.
* &quot;id&quot;를 접미어로 지정한 링크 이름을 지정하지 마십시오. 예를 들어 &quot;transactionId&quot;가 아닌 &quot;transaction&quot;이라는 이름을 지정합니다.

<!--For more on defining links with other resources, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources).-->

## 성능 {#performance}

언제든지 더 나은 성능을 보장하려면 아래 모범 사례를 따르십시오.

### 일반 권장 사항 {#general-recommendations}

* 쿼리에 &quot;CONTAINS&quot;와 같은 작업을 사용하지 마십시오. 예상 내용을 알고 있고 필터링하려는 경우 &quot;EQUAL TO&quot; 또는 기타 특정 필터 연산자와 동일한 조건을 적용합니다.
* 워크플로우에서 데이터를 작성할 때 인덱싱되지 않은 필드와 결합하지 마십시오.
* 가져오기 및 내보내기와 같은 프로세스가 업무 시간 경과에 따라 진행되는지 확인하십시오.
* 모든 일일별 활동들에 대한 일정이 있는지 확인하고 일정대로 해라.
* 일일 프로세스 중 하나 또는 일부가 실패하여 해당 날짜에 실행해야 할 경우 수동 프로세스를 시작하면 시스템 성능에 영향을 줄 수 있으므로 실행 중인 프로세스가 충돌하지 않아야 합니다.
* 가져오기 프로세스 동안 또는 수동 프로세스가 실행될 때 일일 캠페인이 실행되지 않도록 하십시오.
* 모든 행에서 필드를 복제하는 대신 하나 또는 여러 개의 참조 테이블을 사용합니다. 키/값 쌍을 사용할 때는 숫자 키를 선택하는 것이 좋습니다.
* 짧은 문자열을 사용할 수 있습니다. 참조 테이블이 외부 시스템에 이미 있는 경우 동일한 항목을 다시 사용하면 Adobe Campaign와의 데이터 통합이 촉진됩니다.

### 일대다 관계 {#one-to-many-relationships}

* 데이터 디자인은 유용성과 기능에 영향을 줍니다. 일대다 관계가 많은 데이터 모델을 설계하는 경우 애플리케이션에서 의미 있는 로직을 만드는 것이 더 어렵습니다. 일대다 필터 로직은 기술적 지식이 없는 마케터가 올바르게 구성하거나 이해하는 데 어려울 수 있습니다.
* 사용자가 쿼리를 쉽게 작성할 수 있도록 하기 때문에 모든 필수 필드를 하나의 테이블에 두는 것이 좋습니다. 조인을 피할 수 있는 경우 테이블 간에 일부 필드를 복제하는 것이 성능으로도 좋습니다.
* 특정 내장 기능에서는 1대 다 관계를 참조할 수 없습니다(예: 오퍼 가중치 공식 및 배달).

### 큰 테이블 {#large-tables}

다음은 큰 테이블과 복잡한 조인을 사용하여 데이터 모델을 디자인할 때 따라야 하는 몇 가지 우수 사례입니다.

* 사용하지 않은 열을 식별하여 열 수를 줄입니다.
* 여러 조건 및/또는 여러 열에 연결된 연결과 같은 복잡한 연결과는 피하여 데이터 모델 관계를 최적화합니다.
* 조인 키의 경우 문자 문자열이 아닌 숫자 데이터를 항상 사용하십시오.
* 로그 보존 깊이를 최대한 줄일 수 있습니다. 더 깊은 작업 내역이 필요한 경우 계산 및/또는 사용자 정의 로그 테이블을 처리하여 더 큰 내역을 저장할 수 있습니다.