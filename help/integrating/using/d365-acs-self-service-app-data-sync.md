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
source-wordcount: '1839'
ht-degree: 0%

---

# 데이터 동기화

Microsoft Dynamics 365에서 Campaign 및 Campaign 마케팅 지표를 Microsoft Dynamics 365로 테이블을 동기화할 수 있습니다. 동기화는 세 개의 전용 기술 워크플로우(**[!UICONTROL Microsoft Dynamics 365 to Campaign]**, **[!UICONTROL Campaign to Microsoft Dynamics 365]**, **[!UICONTROL Opt-In/Out]**)를 통해 실행됩니다. [자세한 정보](../../integrating/using/d365-acs-self-service-app-workflows.md)를 보려면 이 섹션을 참조하세요.

>[!IMPORTANT]
>변경 사항을 고려하려면 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로를 중지/시작해야 합니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-workflows.md)
>

## Microsoft Dynamics 365의 표를 Campaign에 매핑

**[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에는 Microsoft Dynamics 365의 엔터티 목록과 동기화되는 Adobe Campaign의 사용자 지정 리소스가 표시됩니다. 새 매핑을 추가하거나 기존 매핑을 편집 또는 삭제할 수 있습니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-top.png)

다음은 이 테이블의 각 열에 대한 설명입니다.

* **[!UICONTROL MICROSOFT DYNAMICS 365 TABLE]**: 이 열은 Microsoft Dynamics 365에서 매핑의 데이터 원본이 될 엔터티를 식별합니다.

* **[!UICONTROL CAMPAIGN TABLE]**: 이 열은 Adobe Campaign에서 매핑의 데이터 대상이 될 리소스를 식별합니다.

* **[!UICONTROL ACTIONS]**: 가능한 작업이 아래에 나열되어 있습니다.

   * 이 매핑을 편집하려면 **[!UICONTROL Edit]** 아이콘을 클릭하십시오.

   * 테이블 매핑을 삭제하려면 **[!UICONTROL Delete]** 아이콘을 사용하십시오.

   * Microsoft Dynamics 365 테이블의 모든 데이터를 다시 동기화하려면 **[!UICONTROL Replay Data]** 아이콘을 클릭하십시오. 일반적으로 통합 애플리케이션은 최근에 변경된 Microsoft Dynamics 365의 데이터만 동기화합니다.  그러나 경우에 따라(예: 변경 또는 실수를 한 경우) 모든 데이터를 다시 동기화할 수 있습니다.  이러한 경우 이 단추를 클릭하고 다음에 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로를 중지/시작하면 데이터가 동기화되기 시작합니다.

     **[!UICONTROL Replay Data]** 단추를 클릭하고 검사에 성공하면 아이콘이 비활성화됩니다. 이는 이 테이블 매핑 쌍의 데이터가 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우의 다음 실행과 다시 동기화됨을 나타냅니다.

     다음에 해당하는 경우 데이터를 재생하도록 선택할 수 없습니다.

      * **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로와 연결된 백로그 지표에 2,000,000개 이상의 항목이 있는 경우(**[!UICONTROL Workflows]** 페이지에 표시됨)
      * Microsoft Dynamics 365 테이블에 2,000,000개 이상의 레코드가 있는 경우

     다시 동기화해야 하는 레코드 수는 다양합니다. 레코드 수가 많은 경우 동기화 프로세스를 완료하는 데 시간이 걸릴 수 있습니다. 동기화 프로세스를 완료하기 위해 통합 응용 프로그램이 작동하므로 **[!UICONTROL Workflows]** 페이지에서 **[!UICONTROL Backlog]** 지표를 참조하십시오.

     >[!IMPORTANT]
     >
     > Adobe Campaign Standard 또는 Microsoft Dynamics 365에 변경 사항을 게시할 때 통합 워크플로우를 중지하는 것이 좋습니다. 적용 가능한 변경 사항에는 리소스/엔티티(및 관련 필드), 링크, 식별자 열 등에 대한 업데이트가 포함됩니다. 현재 통합에서 사용 중입니다.
     >

## 새 매핑 만들기 {#add-a-new-mapping}

새 매핑을 생성하려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에서 **[!UICONTROL Add New Mapping]** 단추를 클릭합니다.

1. 드롭다운 목록을 사용하여 매핑할 Microsoft Dynamics 365 및 Campaign 테이블을 선택합니다.
페이지에 있는 다른 대부분의 입력은 선택한 테이블에 따라 달라집니다.

   ![](assets/do-not-localize/d365-to-acs-ui-page-ingress-choose-tables.png)

   >[!NOTE]
   >각 테이블을 두 번 이상 매핑할 수 없습니다. 따라서 드롭다운 선택 항목에는 이미 매핑된 테이블이 포함되지 않습니다.

1. 확인하려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오. 응용 프로그램에서 선택한 테이블과 관련된 필드 정보를 잠시 읽어야 합니다.

그런 다음 매핑 구성을 계속할 수 있습니다. [자세히 알아보기](#new-mapping-settings)

>[!IMPORTANT]
>
>매핑을 처음 추가할 때만 이 페이지에서 테이블을 선택할 수 있습니다. **[!UICONTROL Save]** 단추를 클릭하기 전에 올바른 테이블을 선택했는지 확인하십시오. 저장하면 테이블 선택 필드가 **읽기 전용**&#x200B;이 됩니다.

### 기존 매핑 편집

기존 매핑을 편집하면 테이블 선택을 편집할 수 없습니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-table-read-only.png)

페이지 아래쪽에 있는 입력은 이러한 테이블과 연관된 필드를 기반으로 하기 때문에 이는 기본적으로 수행됩니다. 테이블을 변경하면 이러한 테이블과 연관된 모든 필드가 유효하지 않게 됩니다.  매핑할 테이블을 변경하려면 이전 페이지로 돌아가서 변경할 매핑을 삭제하고 새 매핑을 추가해야 합니다.

### 개별 테이블 매핑 구성 {#new-mapping-settings}

이 섹션에서는 하나의 Microsoft Dynamics 365 테이블을 하나의 Adobe Campaign 테이블로 **단일** 매핑을 구성하는 방법에 대해 알아봅니다.

다음 설정을 정의할 수 있습니다.

* **[!UICONTROL Tables]**: 이 섹션에는 Microsoft Dynamics 365 테이블의 이름과 매핑될 Campaign 테이블이 나열됩니다.
* **[!UICONTROL Field Mappings]**: [이 섹션](#field-mappings)에서 자세히 알아보기
* **[!UICONTROL Field Replacements]**: [이 섹션](#field-replacements)에서 자세히 알아보기
* **[!UICONTROL Filters]**: [이 섹션](#filters)에서 자세히 알아보기
* **[!UICONTROL Advanced Settings]**: [이 섹션](#advanced-settings)에서 자세히 알아보기

### 필드 매핑 {#field-mappings}

#### 기본 키

새 Microsoft Dynamics 365를 Campaign 테이블에 추가할 때 ID 필드를 식별해야 합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-mappings-first-key.png)

Microsoft Dynamics 365 기본 키는 애플리케이션에서 감지하므로 읽기 전용입니다.

Campaign의 경우 고유 키가 될 필드를 선택해야 합니다. [CRM ID 사용자 지정 리소스](../../developing/using/uc-calling-resource-id-key.md)(으)로 구성해야 하며, 중복이 없어야 합니다.

>[!NOTE]
>
>**[!UICONTROL Add New Mapping]**&#x200B;을(를) 선택한 경우에만 테이블의 ID 필드를 선택할 수 있습니다. 기존 테이블 매핑을 편집하기 위해 편집 단추를 클릭하면 ID 필드가 읽기 전용으로 표시됩니다.

기본 키는 항상 **[!UICONTROL Field Mappings]** 섹션에 나열된 첫 번째 필드 이름이 됩니다. 알림 메시지로서 오른쪽에 다음 아이콘이 나열되어 기본 키임을 알려 줍니다.

![](assets/do-not-localize/d365-to-acs-icon-primary-key.png)

#### 다른 필드 매핑 추가

**[!UICONTROL Field Mappings]** 섹션에서 기본 키 이외의 필드 매핑을 추가할 수 있습니다. Microsoft Dynamics 365에서 Adobe Campaign으로 필드의 새 매핑을 추가하려면 **[!UICONTROL Add new field mapping]** 단추를 클릭하십시오.

목록에서 Microsoft Dynamics 365 및 Campaign 필드를 선택합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-new-field-mapping.png)

이러한 목록에는 페이지 맨 위에서 선택한 Microsoft Dynamics 365 및 Campaign 테이블과 연결된 필드 이름이 포함되어 있습니다.

**[!UICONTROL Apply updates]** 전환기를 사용하면 이 필드에 대한 업데이트를 Microsoft Dynamics 365에서 Campaign으로 전파할지 여부를 제어할 수 있습니다.
* ![](assets/do-not-localize/d365-to-acs-icon-switch-on.png)에서 전환되면 업데이트가 발생할 때 Microsoft Dynamics 365의 값에 대한 업데이트가 Adobe Campaign에 전파됩니다.

* ![](assets/do-not-localize/d365-to-acs-icon-switch-off.png)을(를) 해제하면 데이터가 처음 로드되거나 재생될 때 값이 전파되지만 Microsoft Dynamics 365의 필드에 대한 증분 업데이트는 전파되지 않습니다.

>[!NOTE]
>
>**[!UICONTROL Apply updates]** 열 머리글을 클릭하여 스위치의 **모두**&#x200B;를 켜거나 끕니다.
>

필드 값을 선택하면 드롭다운 메뉴 아래에 데이터 유형이 표시됩니다.   한 필드에서 다른 필드로 값을 매핑할 때 유의해야 할 사항입니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-mappings-fields-selected.png)

>[!NOTE]
>
> 여러 Microsoft Dynamics 365 필드를 단일 Campaign 필드에 매핑할 수 없습니다.

### 필드 대체 {#field-replacements}

**[!UICONTROL Add New Field Replacement]** 단추를 사용하여 새 필드 대체를 정의합니다.

필드 대체 기능을 사용하여 다음을 식별할 수 있습니다.

* Microsoft Dynamics 365 필드 이름(필드 매핑 섹션에서 위에 추가됨),
* 기존 값(Microsoft Dynamics 365에 있음) 및
* Adobe Campaign에 쓸 새 값

선택 목록, 열거형 및 부울 값에 대한 드롭다운 목록이 제공됩니다. 텍스트 상자는 다른 문자열 및 숫자 유형에 사용됩니다.

### 필터 {#filters}

**[!UICONTROL Add New Filter]** 단추를 사용하여 Campaign에 전파할 Microsoft Dynamics 365 레코드를 선택하십시오. 레코드와 연결된 필드를 선택하여 필터에 추가할 수 있습니다(필드 이름은 필드 매핑에 추가할 필요가 없음).

다음 정보를 입력하여 필터를 지정합니다.

* Microsoft Dynamics 365 필드 이름
* 비교 값 및
* 값(Microsoft Dynamics 365에서)
주어진 레코드에 대해 필드 이름, 비교 및 값이 true로 평가되면 레코드가 Adobe Campaign으로 전파됩니다.

**[!UICONTROL Choose the filter comparison operator]** 레이블이 지정된 입력을 설정하여 이러한 필터를 평가하는 방법을 선택할 수 있습니다.  **및**&#x200B;을(를) 선택하는 경우 레코드가 Campaign에 전파되려면 모든 필터가 true여야 합니다. **Or**&#x200B;을(를) 선택하면 둘 중 하나라도 true로 평가되면 레코드가 전파됩니다.

**[!UICONTROL Do you want to delete records in Adobe Campaign Standard that will be filtered out from Microsoft Dynamics 365?]** 옵션은 필터링된 레코드를 Campaign에서 삭제할 것인지 여부를 제어합니다. **아니요**&#x200B;를 선택하면 레코드가 Adobe Campaign에 남아 있습니다. 통합 논리로 삭제하려면 **예**&#x200B;를 선택하십시오.

>[!NOTE]
>
> 필터가 추가되지 않으면 수정된 모든 레코드가 Adobe Campaign으로 전파됩니다.
>

### 고급 설정 {#advanced-settings}

매핑을 구성할 때 다음과 같은 추가 옵션을 설정할 수 있습니다.

* 필드 이름 매핑을 기반으로 Microsoft Dynamics 365에서 발생하는 삭제를 Adobe Campaign의 해당 필드에 전파하려면 **[!UICONTROL Apply deletes in Microsoft Dynamics 365 to Campaign?]** 옵션을 **예**(으)로 설정하십시오. Microsoft Dynamics 365에서 삭제를 무시하려면 **아니요**&#x200B;를 선택하십시오.

* Microsoft Dynamics 365 선택 목록과 연결된 표시 값을 Campaign으로 전파하려면 **[!UICONTROL Use technical values in Microsoft Dynamics 365 picklists?]** 옵션을 **아니요**(으)로 설정하십시오. 기술 값을 전파하려면 **예**&#x200B;를 선택하십시오.

## Campaign 마케팅 이벤트를 Microsoft Dynamics 365에 동기화

**[!UICONTROL Campaign to Microsoft Dynamics 365]** 페이지에서 Adobe Campaign에서 Microsoft Dynamics 365로 매핑될 이메일 마케팅 이벤트를 식별할 수 있습니다.

제어할 수 있는 네 가지 지표는 **전송**, **클릭 수**, **열기 수** 및 **바운스 수**&#x200B;입니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-egress.png)

해당 유형의 이벤트가 Microsoft Dynamics 365로 연결되도록 하려면 **예**&#x200B;를 선택하십시오.

전자 메일 이벤트 흐름에 대한 자세한 내용을 보려면 [여기](../../integrating/using/d365-acs-self-service-app-workflows.md)를 클릭하세요.

## 옵트인/옵트아웃 워크플로 {#opt-in-out-wf}

**옵트인/옵트아웃** 워크플로를 사용하면 Microsoft Dynamics 365와 Adobe Campaign 간의 옵트인/옵트아웃 정보 흐름을 식별할 수 있습니다. 데이터가 Microsoft Dynamics 365 엔티티 &quot;연락처&quot; 및 Adobe Campaign 리소스 &quot;프로필&quot;과 연결되어 있다고 가정합니다.

[이 섹션](../../integrating/using/d365-acs-notices-and-recommendations.md#opt-out)에서 옵트아웃 관리에 대해 자세히 알아보세요.

선택 사항을 저장하려면 &quot;저장&quot;을 클릭해야 합니다. 또한 **Campaign to Microsoft Dynamics 365** 워크플로우를 중지한 다음 통합을 위해 재생을 클릭하여 변경 내용을 통합해야 합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-optinout-disabled.png)

### 동기화 방향 옵트인/옵트아웃

다음은 데이터 동기화에 사용 가능한 옵션 목록입니다.

* **[!UICONTROL Disabled]**: 이 옵션을 선택하면 옵트인/옵트아웃 정보가 Adobe Campaign과 Microsoft Dynamics 365 간에 이동하지 않습니다.

* **[!UICONTROL Unidirectional (Microsoft Dynamics 365 to Campaign)]**: 이 옵션은 Microsoft Dynamics 365에서 Adobe Campaign으로만 옵트인/옵트아웃을 전달하는 데 사용됩니다. 통합 응용 프로그램을 사용하면 이 화면에서 흐름을 구성할 수 없습니다. 대신 **[!UICONTROL Save button]**&#x200B;을(를) 클릭하고 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우로 이동합니다. 이 워크플로우에서는 연락처/프로필 테이블 매핑을 편집하여 옵트인/아웃 필드를 매핑하는 방법을 식별할 수 있습니다.

* **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]**: 이 옵션을 사용하면 **매핑** 섹션이 표시됩니다. 이러한 입력을 통해 데이터를 Microsoft Dynamics 365의 필드에 매핑할 Adobe Campaign 필드를 정의할 수 있습니다. 즉, Microsoft Dynamics 365에서 값을 수동으로 업데이트하는 경우 변경되는 경우 해당 값을 Adobe Campaign 값으로 덮어씁니다.

* **[!UICONTROL Bidirectional]**: 이 옵션을 사용하면 **매핑** 섹션이 표시됩니다. 이러한 쌍은 Microsoft Dynamics 365와 Adobe Campaign에서 서로 매핑될 필드를 식별합니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md).

### 매핑

이 섹션은 옵트인/옵트아웃 동기화 방향 필드가 **[!UICONTROL Unidirectional (Campaign to Microsoft Dynamics 365)]** 또는 **[!UICONTROL Bidirectional]**(으)로 설정된 경우에만 적용됩니다. Microsoft Dynamics 365에서 Adobe Campaign의 입력에 매핑되는 필드를 정의할 수 있습니다.

Microsoft Dynamics 365 필드 이름에는 **부울** 유형의 필드 이름이 모두 포함됩니다.

Adobe Campaign 필드 이름은 옵트인/옵트아웃에 해당하는 고정된 값 세트입니다. Adobe Campaign 필드 이름은 옵트인/옵트아웃에 해당하는 고정된 값 세트입니다. **이 목록의 값 집합을 변경할 수 없습니다**.
