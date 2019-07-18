---
title: 두 개의 필드로 구성된 식별 키를 사용하여 리소스 호출
seo-title: 두 개의 필드로 구성된 식별 키를 사용하여 리소스 호출
description: 두 개의 필드로 구성된 식별 키를 사용하여 리소스 호출
seo-description: 두 개의 필드로 구성된 식별 키를 사용하여 리소스를 호출하는 방법 학습
translation-type: tm+mt
source-git-commit: 6d4f814ecd3862a632a25728545bc98a5e336fb5

---


# 두 개의 필드로 구성된 식별 키를 사용하여 리소스 호출

경우에 따라, 리소스에 대해 두 개의 필드로 구성된 식별 키를 정의해야 할 수 있습니다. ID 키가 구성되면 캠페인 표준 인터페이스 또는 API에서 이 식별 키를 사용하여 리소스를 호출할 수 있도록 필터 정의를 구성해야 합니다.

In this use case, the **Profile** resource has been extended with custom **"CRM ID"** and **"category"** field. 프로필 리소스에 대한 ID 키가 생성됩니다. 이 키는 두 개의 필드로 구성됩니다. 그런 다음 필터 정의를 구성하면 ID 키를 사용하여 프로필 리소스에 액세스할 수 있습니다.

이 사용 사례의 기본 단계는 다음과 같습니다.

1. 두 필드를 기반으로 프로필 리소스에 대한 식별 키를 구성합니다.
1. ID 키를 사용하여 프로필 리소스를 호출할 수 있도록 필터 정의를 구성합니다.
1. 인터페이스 또는 API에서 프로필 리소스를 호출합니다.

관련 항목:

* [리소스 만들기 또는 확장](../../developing/using/creating-or-extending-the-resource.md)
* [식별 키 정의](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)
* [Campaign Standard REST API](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)

## 1 단계: ID 키 구성

>[!NOTE]
> Global concepts when configuring identification keys are detailed in [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).

1. ID 키를 구성하기 전에 리소스가 원하는 필드로 확장되었고 게시되었는지 확인하십시오. For more on this, refer to [this section](../../developing/using/creating-or-extending-the-resource.md).

1. **[!UICONTROL Administration]** / **[!UICONTROL Developement]** / **[!UICONTROL Custom resources]** 메뉴로 이동한 다음 **[!UICONTROL Profile]** 리소스를 엽니다.

   ![](assets/uc_idkey1.png)

1. **[Uicontrol ID 키]** 섹션에서 **[!UICONTROL Create element]** 단추를 클릭합니다.

   ![](assets/uc_idkey2.png)

1. Add the two custom "CRM ID" and "Category" fields, then click **[UICONTROL Confirm]**.

   ![](assets/uc_idkey3.png)

   >[!NOTE]
   > If you want to display the two custom fields in the profile's interface, configure the **[UICONTROL Screen definition]** tab. For more on this, refer to [this section](../../developing/using/configuring-the-screen-definition.md).

1. 이제 ID 키를 사용하여 리소스를 호출할 수 있도록 필터 정의를 구성할 수 있습니다.

## 2 단계: 필터 정의 구성

>[!NOTE]
> Global concepts when configuring filter definitions are detailed in [this section](../../developing/using/configuring-filter-definition.md).

1. **[Uicontrol 필터 정의]** 탭에서, 요소 추가를 클릭한 **[다음 필터 정의의 레이블 및 ID를 입력합니다]**.

1. 필터 정의의 속성을 편집하여 해당 규칙을 구성합니다.

   ![](assets/uc_idkey4.png)

1. 작업 영역에 드래그하여 ID 키에 사용된 필드를 포함하는 테이블을 끌어다 놓습니다.

   ![](assets/uc_idkey5.png)

1. Select the first field used in the identification key ("CRM ID"), then activate the **[UICONTROL Switch to parameters]** option.

   ![](assets/uc_idkey6.png)

1. **[Uicontrol 필터 조건]** 섹션에서 **[Uicontrol 같음]** 연산자를 유지하고 매개 변수 이름을 정의하고 더하기 기호를 클릭하여 만듭니다.

   ![](assets/uc_idkey7.png)

   >[!NOTE]
   > 더하기 단추를 클릭하면 매개 변수 이름이 자동으로 생성됩니다. API의 필터를 사용하려면 이 정보를 필요로 합니다.

1. 위의 단계를 반복하여 ID 키 ("카테고리") 를 구성하는 모든 필드를 만든 다음 변경 사항을 저장합니다.

   ![](assets/uc_idkey8.png)

1. 이제 필터 정의가 구성됩니다. 필터를 사용할 수 있도록 리소스를 게시할 수 있습니다.

## 3 단계: ID 키를 기반으로 리소스 호출

식별 키와 해당 필터 정의가 구성되면, 캠페인 표준 인터페이스 또는 REST API에서 리소스를 호출하는 데 사용할 수 있습니다.

To use the filter definition from the interface, use a **[UICONTROL Query]** activity in a workflow (see [this section](../../automating/using/query.md)). 그런 다음 왼쪽 창에서 필터를 사용할 수 있습니다.

![](assets/uc_idkey9.png)

Campaign Standard REST API에서 필터 정의를 사용하려면 아래 구문을 사용하십시오.

\ «GET /profileAndServicesExt/ &lt; resourcename &gt; &lt; filtername &gt;? &lt; param 1_ parameter &gt; = &lt; value &gt; &amp; &lt; param 2_ parameter &gt; = &lt; value &gt;\ "

In our case, the syntax to retrieve a profile from the "spring" category and with the "123456" CRM ID would be:

\ «GET https://mc.adobe.io/ &lt; 조직 &gt;/campaign/profileandservicesext/profile/identification_ key? category_ parameter = Spring &amp; CRM_ ID_ parameter = 123456\ "

For more details, refer to [Campaign Standard REST APIs documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#filtering).