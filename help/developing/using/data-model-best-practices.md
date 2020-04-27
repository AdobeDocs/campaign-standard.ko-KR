---
title: Adobe Campaign Standard의 데이터 모델 모범 사례
description: Adobe Campaign Standard 데이터 모델을 디자인할 때의 모범 사례에 대해 알아봅니다.
page-status-flag: never-activated
uuid: cacd563f-6936-4b3e-83e3-5d4ae31d44e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 4e0468da-3052-4ce5-8174-45aba1f5c4ed
context-tags: cusResource,overview;eventCusResource,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# 데이터 모델 모범 사례{#data-model-best-practices}

이 문서에서는 Adobe Campaign 데이터 모델을 디자인하는 동안 주요 권장 사항에 대해 간략하게 설명합니다.


>[!NOTE]
>
>사전 정의된 Adobe Campaign 데이터 모델을 확장하기 위해 리소스를 만들고 수정하려면 [이 섹션을](../../developing/using/key-steps-to-add-a-resource.md)참조하십시오.
>
>기본 제공 리소스의 데이터 모델 표현을 [이 페이지에서](../../developing/using/datamodel-introduction.md)찾을 수 있습니다.

## 개요 {#overview}

Adobe Campaign 시스템은 매우 유연하며 초기 구현 이상으로 확장할 수 있습니다. 그러나 가능성은 무한하지만 현명한 의사 결정을 내리고 데이터 모델을 디자인하기 위한 강력한 기반을 구축하는 것이 중요합니다.

이 문서에서는 Adobe Campaign 툴을 적절하게 설계하는 방법을 배울 수 있는 일반적인 사용 사례와 모범 사례를 제공합니다.

## 데이터 모델 아키텍처 {#data-model-architecture}

Adobe Campaign Standard는 강력한 크로스 채널 캠페인 관리 시스템으로 온라인 및 오프라인 전략을 연계하여 개인화된 고객 경험을 제작할 수 있습니다.

### 고객 중심의 접근 방식 {#customer-centric-approach}

대부분의 이메일 서비스 제공업체는 목록 중심의 접근 방식을 통해 고객과 커뮤니케이션하고 있지만 Adobe Campaign은 관계형 데이터베이스를 사용하여 고객과 고객의 속성을 보다 광범위하게 파악할 수 있습니다.

이 고객 중심의 접근 방법은 아래 차트에 나와 있습니다. 회색 **프로필** 리소스는 모든 것이 작성되는 주된 고객 테이블을 나타냅니다.

![](assets/customer-centric-data-model.png)

Adobe Campaign 기본 데이터 모델은 이 [섹션에](../../developing/using/datamodel-introduction.md)표시됩니다.

<!--You can find a datamodel representation for the out-of-the-box resources [here](../../developing/using/datamodel-introduction.md).-->

<!--### What is a customer? {#customer-definition}

If you have customer data in more than one system, you need to determine which solution will allow you to identify records as one person. This work might require rules, eventually a match and merge processes to determine the master record. This master record should be the one sent to Adobe Campaign.

While some of this data cleansing might be performed in Adobe Campaign, the recommendation is to run these processes outside and only import clean data in Adobe Campaign. You should keep Campaign as a marketing solution more than a data cleansing tool.

Be able to provide a master customer record which will be sent to Adobe Campaign.-->

### Adobe Campaign용 데이터 {#data-for-campaign}

Adobe Campaign으로 전송할 데이터는 무엇입니까? 마케팅 활동에 필요한 데이터를 결정하는 것은 매우 중요합니다.

>[!NOTE]
>
>Adobe Campaign은 데이터 웨어하우스가 아닙니다. 따라서 모든 가능한 고객과 관련 정보를 Adobe Campaign으로 가져오려고 하지 마십시오.

Adobe Campaign에서 속성이 필요한지 여부를 결정하려면 속성이 다음 카테고리 중 하나에 속하는지 여부를 결정합니다.
* 세그멘테이션에 사용되는 **속성**
* 데이터 **관리 프로세스에** 사용되는 속성(예: 집계 계산)
* 개인화에 사용되는 **속성**
* 보고에 **** 사용되는 속성(사용자 지정 프로필 데이터를 기반으로 보고서를 만들 수 있음)

이러한 속성에 해당되지 않는 경우 Adobe Campaign에서 이 속성이 필요하지 않을 수 있습니다.

### 데이터 유형 {#data-types}

시스템의 우수한 아키텍처와 성능을 유지하려면 아래 모범 사례를 따라 Adobe Campaign에서 데이터를 설정하십시오.
* 문자열 필드의 길이는 항상 열로 정의되어야 합니다. 기본적으로 Adobe Campaign의 최대 길이는 255자입니다. 그러나 크기가 더 짧은 길이를 초과하지 않을 것을 이미 알고 있는 경우 필드를 더 짧게 유지하는 것이 좋습니다.
* 소스 시스템의 크기가 과대평가되어 도달하지 않은 경우 Adobe Campaign의 필드가 소스 시스템보다 짧을 수 있습니다. 이는 Adobe Campaign에서 더 짧은 문자열 또는 더 작은 정수를 의미합니다.

## 데이터 구조 구성 {#configuring-data-structure}

이 섹션에서는 리소스의 데이터 구조를 [구성할 때의 우수 사례에 대해 설명합니다](../../developing/using/configuring-the-resource-s-data-structure.md).

### 식별자 {#identifiers}

Adobe Campaign 리소스에는 세 개의 식별자가 있으며 추가 식별자를 추가할 수 있습니다.

다음 표에서는 이러한 식별자 및 해당 용도를 설명합니다.

>[!NOTE]
>
>표시 이름은 Adobe Campaign 사용자 인터페이스를 통해 사용자에게 표시되는 필드의 이름입니다. 기술 이름은 리소스 정의(및 테이블 열 이름)의 실제 필드 이름입니다.

| 표시 이름 | 기술 이름 | 설명 | 권장사항 |
|--- |--- |--- |--- |
|  | PKey | <ul><li>PKey는 Adobe Campaign 테이블의 실제 기본 키입니다.</li><li>이 식별자는 일반적으로 특정 Adobe Campaign 인스턴스에 고유합니다.</li><li>Adobe Campaign Standard에서 이 값은 최종 사용자가 볼 수 없습니다(URL에서는 제외).</li></ul> | <ul><li>API [시스템을](../../api/using/about-campaign-standard-apis.md)통해 PKey 값(물리적 키가 아닌 생성/해시된 값)을 검색할 수 있습니다.</li><li>API를 통해 레코드를 검색, 업데이트 또는 삭제하는 것 외에는 사용하지 않는 것이 좋습니다.</li></ul> |
| ID | name 또는 internalName | <ul><li>이 정보는 테이블에 있는 레코드의 고유 식별자입니다. 이 값은 수동으로 업데이트할 수 있습니다.</li><li>이 식별자는 다른 Adobe Campaign 인스턴스에 배포할 때 값을 유지합니다. 패키지를 통해 내보낼 수 있도록 생성된 값과 다른 이름이 있어야 합니다.</li><li>이 키는 테이블의 실제 기본 키가 아닙니다.</li></ul> | <ul><li>공백 &quot;&quot;, 세미열 &quot;:&quot; 또는 하이픈 &quot;-&quot;과 같은 특수 문자는 사용하지 마십시오.</li><li>이러한 모든 문자는 밑줄 &quot;_&quot;(허용되는 문자)로 대체됩니다. 예를 들어 &quot;abc-def&quot; 및 &quot;abc:def&quot;는 &quot;abc_def&quot;로 저장되고 서로를 덮어씁니다.</li></ul> |
| 레이블 | label | <ul><li>레이블은 Adobe Campaign에서 개체 또는 레코드의 비즈니스 식별자입니다.</li><li>이 개체는 공백과 특수 문자를 허용합니다.</li><li>그렇다고 기록의 고유성을 보장하지 않는다.</li></ul> | <ul><li>개체 레이블의 구조를 결정하는 것이 좋습니다.</li><li>Adobe Campaign 사용자의 레코드 또는 개체를 식별하기 위한 가장 사용자 친화적인 솔루션입니다.</li></ul> |
| ACS ID | acsId | <ul><li>추가 식별자를 생성할 수 있습니다.acs [ID](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).</li><li>Adobe Campaign 사용자 인터페이스에서 PKey를 사용할 수 없으므로 프로필 레코드를 삽입하는 동안 생성된 고유한 값을 가져오는 솔루션입니다.</li><li>레코드가 Adobe Campaign에 삽입되기 전에 리소스에서 옵션을 활성화한 경우에만 값이 자동으로 생성됩니다.</li></ul> | <ul><li>이 UUID를 조정 키로 사용할 수 있습니다.</li><li>자동 생성된 ACS ID는 워크플로우 또는 패키지 정의에서 참조로 사용할 수 없습니다.</li><li>이 값은 Adobe Campaign 인스턴스에만 적용됩니다.</li></ul> |

### 식별 키 {#keys}

Adobe Campaign에서 만든 각 리소스에는 하나 이상의 고유 [ID 키가](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)있어야 합니다.

<!--Most organizations are importing records from external systems. While the physical key of a resource lies behind the PKey attribute, it is possible to determine a custom key in addition.

This custom key is the actual record primary key in the external system feeding Adobe Campaign.

When an out-of-the-box resource has both an internal auto-generated and an internal custom key, the internal key will be set as a unique index in the physical database table.-->

사용자 지정 리소스를 만들 때 다음 두 가지 옵션이 있습니다.

* 자동 생성된 키와 내부 사용자 지정 키의 조합입니다. 이 옵션은 시스템 키가 복합 키이거나 정수가 아닌 경우에 유용합니다. 정수는 큰 테이블에서 더 높은 성과를 제공하고 다른 테이블과 결합합니다.
* 기본 키를 외부 시스템 기본 키로 사용합니다. 이 솔루션은 일반적으로 서로 다른 시스템 간에 일관된 키를 사용하여 데이터를 가져오고 내보내는 방법을 간소화하므로 선호됩니다.

식별 키는 워크플로우에서 참조로 사용해서는 안 됩니다.

<!--For more on defining identification keys, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).-->

### 인덱스 {#indexes}

Adobe Campaign은 리소스에 정의된 모든 기본 및 내부 키에 [인덱스를](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes) 자동으로 추가합니다.

* 성능을 향상시킬 수 있으므로 추가 인덱스를 정의하는 것이 좋습니다.
* 하지만 데이터베이스에서 공간을 사용할 때 색인이 너무 많이 추가되지 않습니다. 또한 많은 인덱스가 부정적인 성능에 영향을 줄 수 있습니다.
* 정의해야 하는 인덱스를 신중하게 선택합니다.

<!--For more on defining indexes, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-indexes).

When you are performing an initial import with very high volumes of data insert in Adobe Campaign database, it is recommended to run that import without custom indexes at first. It will allow to accelerate the insertion process. Once you’ve completed this important import, it is possible to enable the index(es).-->

### 링크 {#links}

다른 리소스와 링크를 정의하는 방법은 [이 섹션에](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)나와 있습니다.

* 워크플로우에서 모든 표에 연결할 수 있지만, 데이터 구조 정의에서 바로 리소스 간의 공통 링크를 정의하는 것이 좋습니다.
* 링크는 표의 실제 데이터와 일치하도록 정의해야 합니다. 잘못된 정의는 링크를 통해 검색된 데이터에 영향을 줄 수 있습니다(예: 예기치 않게 레코드 복제).
* 리소스 이름과 일관되게 링크 이름 지정:링크 이름은 먼 테이블이 무엇인지 이해하는 데 도움이 됩니다.
* &quot;id&quot;로 링크의 이름을 접미어로 지정하지 마십시오. 예를 들어 &quot;transactionId&quot;가 아닌 &quot;transaction&quot;으로 이름을 지정합니다.

<!--For more on defining links with other resources, see [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources).-->

## 성능 {#performance}

언제든지 더 나은 성능을 위해 아래 모범 사례를 따르십시오.

### 일반 추천 {#general-recommendations}

* 쿼리에 &quot;CONTAINS&quot;와 같은 작업을 사용하지 마십시오. 예상 내용을 알고 필터링하려는 경우 &quot;EQUAL TO&quot; 또는 기타 특정 필터 연산자와 동일한 조건을 적용합니다.
* 워크플로우에서 데이터를 작성하는 동안 인덱싱되지 않은 필드와 연결하지 마십시오.
* 가져오기 및 내보내기와 같은 프로세스가 업무 시간 경과에 따라 수행되는지 확인합니다.
* 모든 일별 활동들에 대한 일정이 있는지 확인하고 일정표를 지키세요.
* 일별 프로세스 중 하나 또는 일부가 실패하여 동시에 실행해야 하는 경우, 수동 프로세스를 시작하면 시스템 성능에 영향을 줄 수 있으므로 실행 중인 프로세스가 충돌하지 않아야 합니다.
* 가져오기 프로세스 동안 또는 수동 프로세스가 실행될 때 일별 캠페인이 실행되지 않도록 하십시오.
* 모든 행에서 필드를 복제하는 대신 하나 또는 여러 개의 참조 표를 사용합니다. 키/값 쌍을 사용할 때는 숫자 키를 선택하는 것이 좋습니다.
* 짧은 문자열을 사용할 수 있습니다. 참조 테이블이 외부 시스템에서 이미 제자리에 있는 경우 동일한 항목을 다시 사용하면 Adobe Campaign과의 데이터 통합이 수월해집니다.

### 일대다 관계 {#one-to-many-relationships}

* 데이터 디자인은 유용성과 기능에 영향을 줍니다. 일대다 관계로 데이터 모델을 설계하면 애플리케이션에서 의미 있는 로직을 만드는 것이 더 어렵습니다. 일대다 필터 로직은 기술적인 면을 잘 모르는 마케터가 올바르게 구성하고 이해하기가 어려울 수 있습니다.
* 사용자가 쿼리를 쉽게 작성할 수 있도록 하기 때문에 하나의 테이블에 모든 필수 필드를 포함하는 것이 좋습니다. 때때로 조인을 피할 수 있는 경우 표 간에 일부 필드를 복제하는 것이 성능에도 좋습니다.
* 특정 기본 제공 기능은 일대다 관계(예: 오퍼 가중치 공식 및 배달)를 참조할 수 없습니다.

### 큰 표 {#large-tables}

다음은 큰 테이블과 복잡한 조인을 사용하여 데이터 모델을 디자인할 때 따라야 하는 몇 가지 우수 사례입니다.

* 특히 사용하지 않은 열을 식별하여 열 수를 줄입니다.
* 여러 조건 및/또는 여러 열에 연결된 경우와 같이 복잡한 조인을 방지하여 데이터 모델 관계를 최적화합니다.
* 조인 키의 경우 항상 문자 문자열이 아닌 숫자 데이터를 사용합니다.
* 로그 보존 깊이를 최대한 줄일 수 있습니다. 더 깊은 작업 내역이 필요한 경우 계산 및/또는 사용자 정의 로그 테이블을 처리하여 더 큰 내역을 저장할 수 있습니다.