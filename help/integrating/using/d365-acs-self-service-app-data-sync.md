---
title: Campaign과 Microsoft Dynamics 간의 데이터 동기화
description: Campaign과 Dynamics 간의 데이터 동기화
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 66623c76-96aa-45cd-9637-19d8a9732c04
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: tm+mt
source-wordcount: '1795'
ht-degree: 0%

---

# 데이터 동기화

Microsoft Dynamics 365에서 Campaign 및 Campaign 마케팅 지표로 테이블을 Microsoft Dynamics 365로 동기화할 수 있습니다. 동기화는 세 가지 전용 기술 워크플로우를 통해 실행됩니다. **[!UICONTROL Microsoft Dynamics 365 to Campaign]**, **[!UICONTROL Campaign to Microsoft Dynamics 365]**, **[!UICONTROL Opt-In/Out]**. 이 섹션을 참조하여 다음을 수행하십시오. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-workflows.md).

>[!IMPORTANT]
>를 중지/시작해야 합니다. **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우 를 사용하여 변경 사항을 고려합니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-workflows.md)

## Microsoft Dynamics 365의 표를 Campaign에 매핑

다음 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에는 Microsoft Dynamics 365의 엔티티 목록과 이러한 엔티티가 동기화되는 Adobe Campaign의 사용자 지정 리소스가 표시됩니다. 새 매핑을 추가하거나 기존 매핑을 편집하거나 삭제할 수 있습니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-top.png)

다음은 이 테이블의 각 열에 대한 설명입니다.

* **[!UICONTROL MICROSOFT DYNAMICS 365 TABLE]**: 이 열은 Microsoft Dynamics 365에서 매핑에 대한 데이터 소스가 될 엔터티를 식별합니다.

* **[!UICONTROL CAMPAIGN TABLE]**: 이 열은 Adobe Campaign에서 매핑에 대한 데이터 대상이 되는 리소스를 식별합니다.

* **[!UICONTROL ACTIONS]**: 가능한 작업은 아래에 나열되어 있습니다.

   * 을(를) 클릭합니다. **[!UICONTROL Edit]** 아이콘 을 클릭하여 이 매핑을 편집합니다.

   * 를 사용하십시오  **[!UICONTROL Delete]** 아이콘을 사용하여 테이블 매핑을 삭제할 수 있습니다.

   * 을(를) 클릭합니다. **[!UICONTROL Replay Data]** 아이콘을 사용하여 Microsoft Dynamics 365 테이블의 모든 데이터를 다시 동기화합니다. 일반적으로 통합 애플리케이션은 최근에 변경된 Microsoft Dynamics 365의 데이터만 동기화합니다.  그러나 일부 경우(예: 사용자가 변경했거나 실수를 한 경우) 모든 데이터를 다시 동기화해야 할 수도 있습니다.  이러한 경우 이 단추를 클릭하고 다음에 을 중지/시작할 때 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우에서 데이터가 동기화되기 시작합니다.

      을(를) 클릭하면 **[!UICONTROL Replay Data]** 버튼을 누르면 아이콘이 비활성화됩니다. 이 테이블 매핑 쌍의 데이터가 다음 실행 시 다시 동기화됨을 나타냅니다 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우.

      다음 내용이 true인 경우에는 데이터를 재생하도록 선택할 수 없습니다.

      * 백로그 지표와 연관된 항목이 2,000,000개 이상인 경우 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우(에 표시됨) **[!UICONTROL Workflows]** page)
      * Microsoft Dynamics 365 표에 200만 개 이상의 레코드가 있는 경우

      다시 동기화해야 하는 레코드 수는 다릅니다. 레코드가 많으면 동기화 프로세스를 완료하는 데 시간이 걸릴 수 있습니다. 자세한 내용은 **[!UICONTROL Backlog]** 의 지표 **[!UICONTROL Workflows]** 통합 응용 프로그램이 동기화 프로세스를 완료하기 위해 작동하는 페이지입니다.

      >[!IMPORTANT]
      >
      > Adobe Campaign Standard 또는 Microsoft Dynamics 365에 변경 사항을 게시할 때 통합 워크플로우를 중지하는 것이 좋습니다. 적용 가능한 변경 사항은 다음과 같습니다. 리소스/엔티티(및 관련 필드), 링크, 식별자 열 등에 대한 업데이트. 현재 통합에서 사용 중입니다.


## 새 매핑 만들기 {#add-a-new-mapping}

새 매핑을 생성하려면 아래 단계를 수행하십시오.

1. 에서 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에서 **[!UICONTROL Add New Mapping]** 버튼을 클릭합니다.

1. 드롭다운 목록을 사용하여 매핑할 Microsoft Dynamics 365 및 Campaign 테이블을 선택합니다.
페이지의 다른 입력 대부분은 선택한 테이블에 따라 달라집니다.

   ![](assets/do-not-localize/d365-to-acs-ui-page-ingress-choose-tables.png)

   >[!NOTE]
   >각 테이블을 두 번 이상 매핑할 수 없습니다. 따라서 드롭다운 선택에는 이미 매핑된 테이블이 포함되지 않습니다.

1. 클릭 **[!UICONTROL OK]** 확인하려면: 선택한 테이블과 연관된 필드 정보를 보려면 간단한 시간이 필요합니다.

그런 다음 매핑 구성을 계속 진행할 수 있습니다. [자세히 알아보기](#new-mapping-settings)

>[!IMPORTANT]
>
>매핑을 처음 추가할 때만 이 페이지에서 테이블을 선택할 수 있습니다. 를 클릭하기 전에 올바른 테이블을 선택했는지 확인합니다. **[!UICONTROL Save]** 버튼: 일단 저장되면 테이블 선택 필드가 저장됩니다 **읽기 전용**.

### 기존 매핑 편집

기존 매핑을 편집하면 테이블 선택을 편집할 수 없다는 것을 확인할 수 있습니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-table-read-only.png)

이는 페이지에서 더 아래쪽 입력이 이러한 테이블과 연결된 필드를 기반으로 하기 때문에 디자인되었습니다. 표를 변경하면 이 테이블과 연결된 모든 필드가 올바르지 않게 됩니다.  매핑할 테이블을 변경하려면 이전 페이지로 돌아가서 변경할 매핑을 삭제하고 새 매핑을 추가해야 합니다.

### 개별 테이블 매핑 구성 {#new-mapping-settings}

이 섹션에서는 **단일** 하나의 Microsoft Dynamics 365 테이블을 하나의 Adobe Campaign 테이블에 매핑

다음 설정을 정의할 수 있습니다.

* **[!UICONTROL Tables]**: 이 섹션에는 Microsoft Dynamics 365 테이블의 이름과 매핑될 캠페인 테이블이 나열됩니다.
* **[!UICONTROL Field Mappings]**: 자세히 알아보기 [이 섹션](#field-mappings)
* **[!UICONTROL Field Replacements]**: 자세히 알아보기 [이 섹션](#field-replacements)
* **[!UICONTROL Filters]**: 자세히 알아보기 [이 섹션](#filters)
* **[!UICONTROL Advanced Settings]**: 자세히 알아보기 [이 섹션](#advanced-settings)

### 필드 매핑 {#field-mappings}

#### 기본 키

새 Microsoft Dynamics 365를 Campaign 테이블 매핑에 추가할 때 ID 필드를 식별해야 합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-mappings-first-key.png)

Microsoft Dynamics 365 기본 키는 애플리케이션이 검색하므로 읽기 전용입니다.

Campaign의 경우 고유한 키가 될 필드를 선택해야 합니다. 다음과 같이 구성해야 합니다. [CRM ID 사용자 지정 리소스](../../developing/using/uc-calling-resource-id-key.md) 에는 중복이 없어야 합니다.

>[!NOTE]
>
>선택한 경우에만 테이블에서 ID 필드를 선택할 수 있습니다 **[!UICONTROL Add New Mapping]**. 편집 단추를 클릭하여 기존 테이블 매핑을 편집하는 경우 ID 필드는 읽기 전용입니다.

기본 키는 항상 **[!UICONTROL Field Mappings]** 섹션을 참조하십시오. 미리 알림으로 다음 아이콘이 오른쪽에 표시되어 기본 키임을 알려줍니다.

![](assets/do-not-localize/d365-to-acs-icon-primary-key.png)

#### 다른 필드 매핑 추가

다음 **[!UICONTROL Field Mappings]** 섹션에서 기본 키 이외의 필드 매핑을 추가할 수 있습니다. Microsoft Dynamics 365에서 Adobe Campaign으로 필드의 새 매핑을 추가하려면 **[!UICONTROL Add new field mapping]** 버튼을 클릭합니다.

목록에서 Microsoft Dynamics 365 및 Campaign 필드를 선택합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-new-field-mapping.png)

이러한 목록에는 페이지 맨 위에서 선택한 Microsoft Dynamics 365 및 Campaign 테이블과 연결된 필드 이름이 포함되어 있습니다.

다음 **[!UICONTROL Apply updates]** 전환기를 사용하면 이 필드에 대한 업데이트를 Microsoft Dynamics 365에서 Campaign으로 전파할지 여부를 제어할 수 있습니다.
* 켜진 경우 ![](assets/do-not-localize/d365-to-acs-icon-switch-on.png), 업데이트가 발생하면 Microsoft Dynamics 365의 값에 대한 업데이트가 Adobe Campaign에 전파됩니다.

* 꺼져 있으면 ![](assets/do-not-localize/d365-to-acs-icon-switch-off.png)를 지정하면 데이터가 처음 로드될 때(또는 다시 재생) 값이 전파되지만 Microsoft Dynamics 365의 필드에 대한 증분 업데이트는 전파되지 않습니다.

>[!NOTE]
>
>을(를) 클릭합니다. **[!UICONTROL Apply updates]** 업데이트할 열 제목 **모두** 스위치를 켜거나 끕니다.

필드 값을 선택하면 드롭다운 메뉴 아래에 데이터 유형이 표시됩니다.   한 필드에서 다른 필드에 값을 매핑할 때 이것을 기억하십시오.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-mappings-fields-selected.png)

>[!NOTE]
>
> 여러 Microsoft Dynamics 365 필드를 단일 캠페인 필드에 매핑할 수 없습니다.

### 필드 교체 {#field-replacements}

를 사용하십시오 **[!UICONTROL Add New Field Replacement]** 새 필드 대체를 정의하는 단추입니다.

필드 교체를 사용하여 다음을 식별할 수 있습니다.

* Microsoft Dynamics 365 필드 이름(필드 매핑 섹션에서 위에 추가됨)입니다.
* 기존 값(Microsoft Dynamics 365에 있음)과
* Adobe Campaign에 쓸 새 값

picklist, 열거형 및 부울 값에 대한 드롭다운 목록이 제공됩니다. 텍스트 상자는 다른 문자열 및 숫자 유형에 사용됩니다.

### 필터 {#filters}

를 사용하십시오 **[!UICONTROL Add New Filter]** 단추를 클릭하여 Campaign에 전파할 Microsoft Dynamics 365 레코드를 선택합니다. 레코드에 연결된 필드를 선택하여 필터에 추가할 수 있습니다(필드 이름을 필드 매핑에 추가할 필요가 없음).

다음 정보를 입력하여 필터를 지정합니다.

* Microsoft Dynamics 365 필드 이름
* 비교 값 및
* 값(Microsoft Dynamics 365에서) 필드 이름, 비교 및 값이 지정된 레코드에 대해 true로 평가되면 레코드가 Adobe Campaign에 전파됩니다.

라는 레이블이 지정된 입력을 설정하여 이러한 필터를 평가하는 방법을 선택할 수 있습니다 **[!UICONTROL Choose the filter comparison operator]**.  만약 **및**&#x200B;를 지정하는 경우 레코드가 Campaign으로 전파되려면 모든 필터가 true여야 합니다. 만약 **또는**&#x200B;를 활성화하면 레코드가 true로 평가되면 전파됩니다.

옵션 **[!UICONTROL Do you want to delete records in Adobe Campaign Standard that will be filtered out from Microsoft Dynamics 365?]** 필터링된 레코드를 Campaign에서 삭제할지 여부를 제어합니다. 선택하는 경우 **아니요** 그러면 레코드가 Adobe Campaign에 유지됩니다. 선택 **예** 통합 논리에 의해 삭제되도록 합니다.

>[!NOTE]
>
> 필터가 추가되지 않으면 수정된 모든 레코드는 Adobe Campaign에 전파됩니다.

### 고급 설정 {#advanced-settings}

매핑을 구성할 때 다음 추가 옵션을 설정할 수 있습니다.

* 설정 **[!UICONTROL Apply deletes in Microsoft Dynamics 365 to Campaign?]** 옵션 **예** Microsoft Dynamics 365에서 발생하는 삭제를 Adobe Campaign의 해당 필드에 전파하려면 필드 이름 매핑을 기반으로 합니다. 선택 **아니요** Microsoft Dynamics 365에서 삭제를 무시합니다.

* 설정 **[!UICONTROL Use technical values in Microsoft Dynamics 365 picklists?]** 옵션 **아니요** campaign에 전파하려면 Microsoft Dynamics 365 선택 목록과 연결된 표시 값을 표시합니다. 선택 **예** 기술 값을 전파하려면

## Campaign 마케팅 이벤트를 Microsoft Dynamics 365에 동기화

다음 **[!UICONTROL Campaign to Microsoft Dynamics 365]** 페이지에서는 Adobe Campaign에서 Microsoft Dynamics 365로 매핑될 이메일 마케팅 이벤트를 식별할 수 있습니다.

제어할 수 있는 네 가지 지표는 다음과 같습니다. **전송**, **클릭 수**, **열기**, 및 **바운스 수**.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-egress.png)

선택 **예** 해당 유형의 이벤트가 Microsoft Dynamics 365로 이동되는지 확인합니다.

클릭 [여기](../../integrating/using/d365-acs-self-service-app-workflows.md) 를 참조하십시오.

## 옵트인/아웃 워크플로우 {#opt-in-out-wf}

다음 **옵트인/옵트아웃** 워크플로우를 통해 Microsoft Dynamics 365와 Adobe Campaign 간의 옵트인/아웃 정보 흐름을 식별할 수 있습니다. 이 섹션에서는 데이터가 Microsoft Dynamics 365 엔티티 &quot;연락처&quot; 및 Adobe Campaign 리소스 &quot;프로필&quot;과 연결되어 있다고 가정합니다.

의 옵트아웃 관리에 대해 자세히 알아보십시오 [이 섹션](../../integrating/using/d365-acs-notices-and-recommendations.md#opt-out).

선택 항목을 저장하려면 &quot;저장&quot;을 클릭해야 한다는 점을 기억하십시오. 또한 다음을 중지해야 합니다 **Campaign에서 Microsoft Dynamics 365로** 워크플로우를 만든 다음 통합을 위해 재생 을 클릭하여 변경 사항을 통합합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-optinout-disabled.png)

### 옵트인/아웃 동기화 방향

다음은 데이터를 동기화하는 데 사용할 수 있는 옵션 목록입니다.

* **[!UICONTROL Disabled]**: 이 옵션을 선택하면 Adobe Campaign과 Microsoft Dynamics 365 간에 옵트인/아웃 정보가 이동되지 않습니다.

* **[!UICONTROL Unidirectional (Microsoft Dynamics 365 to Campaign)]**: 이 옵션은 Microsoft Dynamics 365에서 Adobe Campaign으로만 옵트인/아웃을 플로우하는 데 사용됩니다. 통합 애플리케이션에서 이 화면에서 흐름을 구성할 수 없습니다. 대신, **[!UICONTROL Save button]**&#x200B;로 이동하고 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우. 이 워크플로우에서는 연락처/프로필 테이블 매핑을 편집하여 옵트인/아웃 필드를 매핑할 방법을 식별할 수 있습니다.

* **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]**: 이 옵션을 선택하면 **매핑** 섹션을 참조하십시오. 이러한 입력을 사용하면 Microsoft Dynamics 365의 필드에 데이터를 매핑할 Adobe Campaign 필드를 정의할 수 있습니다. 즉, Microsoft Dynamics 365에서 값을 수동으로 업데이트하는 경우 값이 변경되면 Adobe Campaign 값으로 해당 값을 덮어씁니다.

* **[!UICONTROL Bidirectional]**: 이 옵션을 선택하면 **매핑** 섹션을 참조하십시오. 이러한 쌍은 Microsoft Dynamics 365와 Adobe Campaign에서 서로 매핑되는 필드를 식별합니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md)

### 매핑

이 섹션은 옵트인/옵트아웃 동기화 방향 필드가 **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]** 또는 **[!UICONTROL Bidirectional]**. Microsoft Dynamics 365에서 Adobe Campaign의 입력에 매핑되는 필드를 정의할 수 있습니다.

Microsoft Dynamics 365 필드 이름에는 유형인 모든 필드 이름이 포함됩니다 **부울**.

Adobe Campaign 필드 이름은 옵트인/아웃에 관련된 고정 값 세트입니다. Adobe Campaign 필드 이름은 옵트인/아웃에 관련된 고정 값 세트입니다. **이 목록의 값 집합을 변경할 수 없습니다**.
