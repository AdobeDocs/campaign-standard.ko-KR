---
title: 필터 정의 구성
description: 필터 기능을 사용하여 대용량 데이터 세트를 관리합니다.
page-status-flag: never-activated
uuid: c9db95fe-e9aa-40f8-9c0a-e74bb21ac14b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 993ab2bd-e05f-468e-9ef8-a603761247f8
context-tags: cusResource,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: cabe064632c9c2e3de93bc1cff6fa217b4fdf3e6
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---


# 필터 정의 구성{#configuring-filter-definition}

탭에서는 대상을 정의할 때와 같이 복잡한 쿼리를 만들 때 직접 액세스할 수 있는 고급 필터를 만들 수 있습니다. **[!UICONTROL Filter definition]**

워크플로우, 대상 및 REST API를 통해 리소스를 채우고 해당 데이터에 액세스할 수 있으므로 이 단계는 필수가 아닙니다.

![](assets/custom_resource_filter-definition.png)

이러한 필터는 사전 구성된 규칙 형태로 쿼리 편집기에서 사용됩니다. 이러한 구성 요소를 사용하면 원하는 구성을 얻는 데 필요한 단계 수를 제한할 수 있으며, 이는 반복적인 세그먼트에 특히 유용할 수 있습니다.

예를 들어 지난 3개월 동안 특정 금액보다 큰 모든 거래를 선택할 수 있도록 필터를 만들 수 있습니다.

이렇게 하려면 **[!UICONTROL Profiles]** 자원을 확장하고 트랜잭션 테이블(이전에 생성한 항목)에 대한 필터 링크를 정의해야 합니다. 여기에는 트랜잭션 가격이 주어진 매개변수보다 크거나 같아야 하며 트랜잭션 날짜가 지난 3개월에 해당하는 범위 내에 있어야 함을 나타내는 규칙이 있습니다.

1. 트랜잭션 테이블을 만들고 게시해야 합니다. See [Creating or extending the resource](../../developing/using/creating-or-extending-the-resource.md).

   >[!NOTE]
   >
   >이 절차에서는 사용자 지정 트랜잭션 테이블의 예를 사용합니다. 비즈니스 요구 사항에 맞게 조정

1. 리소스의 트랜잭션 테이블과 관련된 필터를 정의하기 전에 이 테이블에 대한 링크를 정의하고 변경 사항을 게시해야 **[!UICONTROL Profiles]** 합니다. 다른 [리소스와 링크](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources) 정의 및 데이터베이스 구조 [업데이트를 참조하십시오](../../developing/using/updating-the-database-structure.md).
1. 새 필터 정의 화면의 **[!UICONTROL Definition]** 탭에서 트랜잭션 테이블을 선택합니다.

   ![](assets/custom_resource_filter-definition_example-empty.png)

1. 창에서 트랜잭션 테이블을 **[!UICONTROL Add a rule - Profiles/Transactions]** 작업 공간으로 드래그하여 놓습니다. 표시되는 다음 창에서 사용할 필드를 선택합니다.

   ![](assets/custom_resource_filter-definition_example-field.png)

1. 창 **[!UICONTROL Optional parameter settings]** 에서 **[!UICONTROL Add a rule - Transactions]** 상자를 **[!UICONTROL Switch to parameters]** 선택합니다.

   에서 **[!UICONTROL Filter conditions]**&#x200B;연산자를 **[!UICONTROL Greater than or equal to]** 선택합니다. 필드에 이름을 **[!UICONTROL Parameters]** 입력하고 더하기 기호를 클릭하여 새 매개 변수를 만듭니다.

   ![](assets/custom_resource_filter-definition_example-parameter.png)

1. 변경 사항을 확인합니다. 이 정의는 사용자가 쿼리를 실행하기 위해 나중에 입력해야 하는 구성 가능한 필드에 해당합니다.

   ![](assets/custom_resource_filter-definition_ex_edit-rule.png)

1. 거래 날짜가 지난 3개월 동안의 범위 내에 포함되어야 함을 지정하는 다른 규칙과 이 규칙을 결합합니다.

   ![](assets/custom_resource_filter-definition_example.png)

1. 필터를 표시할 카테고리를 선택합니다.

   ![](assets/custom_resource_filter-definition_category.png)

1. 필터 정의 화면 **[!UICONTROL Parameters]** 의 탭에서 설명 및 레이블을 수정하여 사용자에게 필터의 제목을 명확히 지정합니다. 이 정보는 쿼리 편집기에 표시됩니다.

   ![](assets/custom_resource_filter-definition_parameters.png)

   구성 가능한 여러 필드를 정의하는 경우 인터페이스에 표시되는 순서를 수정할 수 있습니다.

1. 변경 내용을 저장하고 리소스를 게시합니다. 자세한 내용은 데이터베이스 구조 [업데이트 섹션을](../../developing/using/updating-the-database-structure.md) 참조하십시오.

리소스 확장자가 게시되면 사용자는 **[!UICONTROL Profiles]** 쿼리 편집기 [](../../automating/using/editing-queries.md) 인터페이스의 바로 가기 탭 아래에 이 필터가 표시됩니다.

이렇게 하면 사용자가 지난 3개월 동안 일정 금액 이상을 보낸 모든 클라이언트에 보낼 이메일을 만들 때 고객을 쉽게 정의할 수 있습니다.

![](assets/custom_resource_filter-definition_email-audience.png)

직접 구성하는 대신 나타나는 대화 상자에 원하는 금액을 입력해야 합니다.

![](assets/custom_resource_filter-definition_email-audience_filter.png)

필터가 구성되면 다음 구문을 사용하여 Campaign Standard API에서 사용할 수 있습니다.

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/by<customFilterName>?<customFilterparam>=<customFilterValue>`

자세한 내용은 [Campaign Standard API 설명서를 참조하십시오](../../api/using/filtering.md#custom-filters).
