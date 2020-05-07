---
title: 복합 식별 키로 리소스 호출
description: 복합 식별 키를 사용하여 리소스를 호출하는 방법 학습
translation-type: tm+mt
source-git-commit: 816d550d8bd0de085a47f97c1f6cc2fbb5e7acb9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 복합 식별 키로 리소스 호출{#calling-a-resource-using-a-composite-identification-key}

경우에 따라 두 필드로 구성된 리소스 및 식별 키를 정의해야 할 수 있습니다. 식별 키가 구성되면 Campaign Standard 인터페이스 또는 API에서 이 식별 키로 리소스를 호출할 수 있도록 필터 정의를 구성해야 합니다.

이 사용 사례에서 **프로필** 리소스는 사용자 지정 **&quot;CRM ID&quot;** 및 **&quot;카테고리** &quot;필드로확장되었습니다. 이 두 필드로 구성된 프로필 리소스에 대한 식별 키를 만듭니다. 그런 다음 필터 정의를 구성하여 식별 키를 사용하여 프로필 리소스에 액세스할 수 있습니다.

이 사용 사례에 대한 주요 단계는 다음과 같습니다.

1. 두 필드를 기반으로 프로필 리소스의 식별 키를 구성합니다.
1. 식별 키를 사용하여 프로필 리소스를 호출할 수 있도록 필터 정의를 구성합니다.
1. 인터페이스 또는 APis에서 프로필 리소스를 호출합니다.

관련 항목:

* [리소스 만들기 또는 확장](../../developing/using/creating-or-extending-the-resource.md)
* [식별 키 정의](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)
* [Campaign Standard REST API](../../api/using/get-started-apis.md)

## 1단계: 식별 키 구성{#step-1-configure-the-identification-key}

>[!NOTE]
> 식별 키를 구성할 때의 글로벌 개념은 [이 섹션에 자세히 설명되어 있습니다](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).

1. 식별 키를 구성하기 전에 리소스가 원하는 필드로 확장되었는지, 게시되었는지 확인하십시오. For more on this, refer to [this section](../../developing/using/creating-or-extending-the-resource.md).

1. / **[!UICONTROL Administration]** / **[!UICONTROL Developement]** / **[!UICONTROL Custom resources]** 메뉴로 이동한 다음 **[!UICONTROL Profile]** 리소스를 엽니다.

   ![](assets/uc_idkey1.png)

1. 섹션에서 **[!UICONTROL Identification keys]** 단추를 **[!UICONTROL Create element]** 클릭합니다.

   ![](assets/uc_idkey2.png)

1. 두 개의 사용자 지정 &quot;CRM ID&quot; 및 &quot;카테고리&quot; 필드를 추가한 다음 을 클릭합니다 **[!UICONTROL Confirm]**.

   ![](assets/uc_idkey3.png)

   >[!NOTE]
   > 프로필 인터페이스에 두 개의 사용자 지정 필드를 표시하려면 **[!UICONTROL Screen definition]** 탭을 구성합니다. For more on this, refer to [this section](../../developing/using/configuring-the-screen-definition.md).

1. 이제 해당 식별 키를 사용하여 리소스를 호출할 수 있도록 필터 정의를 구성할 수 있습니다.

## 2단계: 필터 정의 구성{#step-2-configure-the-filter-definition}

>[!NOTE]
> 필터 정의를 구성할 때의 글로벌 개념은 [이 섹션에 자세히 설명되어 있습니다](../../developing/using/configuring-filter-definition.md).

1. 탭 **[!UICONTROL Filter definition]** 에서 을 **[!UICONTROL Add an element]**&#x200B;클릭한 다음 필터 정의의 레이블과 ID를 입력합니다.

1. 필터 정의의 속성을 편집하여 규칙을 구성합니다.

   ![](assets/uc_idkey4.png)

1. 식별 키에 사용된 필드가 포함된 테이블을 작업 공간으로 끌어다 놓습니다.

   ![](assets/uc_idkey5.png)

1. 식별 키(&quot;CRM ID&quot;)에서 사용되는 첫 번째 필드를 선택한 다음 **[!UICONTROL Switch to parameters]** 옵션을 활성화합니다.

   ![](assets/uc_idkey6.png)

1. 섹션에서 **[!UICONTROL Filter conditions]** 연산자를 유지하고 **[!UICONTROL Equal]** 매개 변수의 이름을 정의한 다음 더하기 기호를 클릭하여 매개 변수를 만듭니다.

   ![](assets/uc_idkey7.png)

   >[!NOTE]
   > 더하기 단추를 클릭하면 매개 변수의 이름이 자동으로 생성됩니다. API의 필터를 사용하는 데 필요한 정보이므로 이 정보를 참고하십시오.

1. 식별 키를 구성하는 모든 필드(&quot;카테고리&quot;)와 함께 위의 단계를 반복한 다음 변경 사항을 저장합니다.

   ![](assets/uc_idkey8.png)

1. 이제 필터 정의가 구성됩니다. 필터를 사용할 수 있도록 리소스를 게시할 수 있습니다.

## 3단계: 식별 키를 기준으로 리소스에 전화 걸기{#step-3-call-the-resource-based-on-its-identification-key}

식별 키 및 해당 필터 정의가 구성되면 Campaign 표준 인터페이스 또는 REST API에서 해당 리소스를 호출하는 데 사용할 수 있습니다.

인터페이스에서 필터 정의를 사용하려면 워크플로우의 **[!UICONTROL Query]** 활동을 사용하십시오( [이 섹션 참조](../../automating/using/query.md)). 그런 다음 왼쪽 창에서 필터를 사용할 수 있습니다.

![](assets/uc_idkey9.png)

Campaign Standard REST API의 필터 정의를 사용하려면 아래 구문을 사용하십시오.

```
GET /profileAndServicesExt/<resourceName>/by<filterName>?<param1_parameter>=<value>&<param2_parameter>=<value>
```

>[!NOTE]
>고객 필터를 호출하려면 [2단계에서 필터 정의를 구성할 때 정의된 필터 이름 뒤에 &quot;by&quot; 접두사를 사용하십시오](../../developing/using/uc-calling-resource-id-key.md#step-2-configure-the-filter-definition).

이 경우 &quot;123456&quot; CRM ID가 있는 &quot;spring&quot; 카테고리에서 프로파일을 검색하는 구문은 다음과 같습니다.

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byidentification_key?category_parameter=spring&crm_id_parameter=123456
```

자세한 내용은 [Campaign Standard REST API 설명서를 참조하십시오](../../api/using/filtering.md).