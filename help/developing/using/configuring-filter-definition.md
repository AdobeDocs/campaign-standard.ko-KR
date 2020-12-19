---
solution: Campaign Standard
product: campaign
title: 필터 정의 구성
description: 필터 기능으로 대용량 데이터 세트를 관리하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
context-tags: cusResource,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 95%

---


# 필터 정의 구성{#configuring-filter-definition}

**[!UICONTROL Filter definition]** 탭에서 사용자가 대상자를 정의할 때와 같이 복잡한 쿼리를 만들 때 직접 액세스할 수 있는 고급 필터를 만들 수 있습니다. 

워크플로우, 대상자 및 REST API를 통해 리소스를 채우고 해당 데이터에 액세스할 수 있으므로 이 단계는 필수가 아닙니다.

![](assets/custom_resource_filter-definition.png)

이러한 필터는 쿼리 편집기에서 사전 구성된 규칙 형태로 사용됩니다. 이를 통해 원하는 구성에 필요한 단계 수를 제한할 수 있습니다. 이는 특히 반복적인 세분화에 유용합니다.

예를 들어 지난 3개월 내에 특정 금액보다 큰 트랜잭션을 모두 선택할 수 있게 해주는 필터를 만들 수 있습니다.

이렇게 하려면 **[!UICONTROL Profiles]** 리소스를 확장한 뒤 (이전에 만든) 트랜잭션 표에 연결하는 필터를 정의해야 합니다. 필터에는 트랜잭션 값이 주어진 매개 변수 이상이어야 하며 트랜잭션 날짜가 지난 3개월에 해당하는 범위 안에 있어야 함을 나타내는 규칙을 적용합니다.

1. 먼저 트랜잭션 표를 만들고 게시했는지 확인합니다. [리소스 만들기 또는 확장](../../developing/using/creating-or-extending-the-resource.md)을 참조하십시오.

   >[!NOTE]
   >
   >여기에서는 사용자 지정 트랜잭션 표의 예시를 사용합니다. 표는 비즈니스 요구 사항에 맞추어 조정하십시오.

1. **[!UICONTROL Profiles]** 리소스의 트랜잭션 표와 관련된 필터를 정의하기에 앞서 이 테이블에 대한 링크를 정의하고 변경 사항을 게시합니다. [다른 리소스와 연결된 링크 정의](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)와 [데이터베이스 구조 업데이트](../../developing/using/updating-the-database-structure.md)를 참조하십시오.
1. 새 필터 정의 화면의 **[!UICONTROL Definition]** 탭에서 트랜잭션 표를 선택합니다.

   ![](assets/custom_resource_filter-definition_example-empty.png)

1. **[!UICONTROL Add a rule - Profiles/Transactions]** 창에서 트랜잭션 표를 작업 영역으로 끌어다 놓습니다. 그 다음 표시되는 창에서 사용할 필드를 선택합니다.

   ![](assets/custom_resource_filter-definition_example-field.png)

1. **[!UICONTROL Add a rule - Transactions]** 창의 **[!UICONTROL Optional parameter settings]**&#x200B;에서 **[!UICONTROL Switch to parameters]** 상자를 선택합니다.

   **[!UICONTROL Filter conditions]**&#x200B;에서 **[!UICONTROL Greater than or equal to]** 연산자를 선택합니다. **[!UICONTROL Parameters]** 필드에 이름을 입력하고 더하기 기호를 클릭하여 새 매개 변수를 만듭니다.

   ![](assets/custom_resource_filter-definition_example-parameter.png)

1. 변경 사항을 확인합니다. 이 정의는 구성 가능한 필드에 해당하며, 나중에 사용자가 해당 필드를 입력해야 쿼리를 실행할 수 있습니다.

   ![](assets/custom_resource_filter-definition_ex_edit-rule.png)

1. 트랜잭션 날짜가 지난 3개월 동안의 범위 내에 포함되어야 한다고 지정하는 다른 규칙과 이 규칙을 결합합니다.

   ![](assets/custom_resource_filter-definition_example.png)

1. 필터를 표시할 카테고리를 선택합니다.

   ![](assets/custom_resource_filter-definition_category.png)

1. 필터 정의 화면의 **[!UICONTROL Parameters]** 탭에서 설명 및 레이블을 수정하여 사용자가 필터의 주제를 명확히 알아볼 수 있도록 합니다. 이 정보는 쿼리 편집기에 표시됩니다.

   ![](assets/custom_resource_filter-definition_parameters.png)

   구성 가능한 필드를 여러 개 정의하는 경우 인터페이스에 표시되는 순서를 수정할 수 있습니다.

1. 변경 내용을 저장하고 리소스를 게시합니다. 자세한 내용은 [데이터베이스 구조 업데이트](../../developing/using/updating-the-database-structure.md) 섹션을 참조하십시오.

**[!UICONTROL Profiles]** 리소스 확장이 게시되면 사용자는 [쿼리 편집기](../../automating/using/editing-queries.md) 인터페이스의 바로 가기 탭 아래에서 이 필터를 확인할 수 있습니다.

이렇게 하면 사용자가 지난 3개월 동안 일정 금액 이상을 소비한 모든 고객에게 보낼 이메일을 만들 때 대상자를 쉽게 정의할 수 있습니다.

![](assets/custom_resource_filter-definition_email-audience.png)

대상자를 직접 구성할 필요 없이 나타나는 대화 상자에 원하는 금액을 입력하기만 하면 됩니다.

![](assets/custom_resource_filter-definition_email-audience_filter.png)

필터가 구성되면 다음 구문을 사용하여 Campaign Standard API에서 필터를 사용할 수 있습니다.

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/by<customFilterName>?<customFilterparam>=<customFilterValue>`

자세한 내용은 [Campaign Standard API 설명서](../../api/using/filtering.md#custom-filters)를 참조하십시오.
