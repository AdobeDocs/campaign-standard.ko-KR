---
solution: Campaign Standard
product: campaign
title: 목록 사용자 지정
description: '"Adobe Campaign Standard에서 디스플레이 사용자 정의 및 목록 화면 사용 방법: 요소 정렬, 필터링, 삭제 또는 복제. 화면에 하나 이상의 주어진 리소스의 표시 요소가 표시됩니다."'
audience: start
content-type: reference
topic-tags: discovering-the-interface
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 9%

---


# 프로필 및 대상을 사용한 작업

<table>
<tr>
    <td valign="top">
        <a href="../../start/using/work-with-audiences.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/creating-a-service.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a>
    </td>
</tr>
<tr>
<td>고객 프로필</td>
<td>데이터베이스 강화</td>
<td>고객 구성</td>
<td>개인 정보 관리</td>
</tr>
</table>

## 고객 프로필 {#customer-profiles}

<img width="60px" alt="조건" src="assets/icon_profile.svg"/>

Adobe Campaign 프로필은 데이터베이스에 저장된 모든 연락처를 나타냅니다. 각 프로파일은 해당 프로파일을 타깃팅하고 자격을 부여하며 개별적으로 추적하는 데 필요한 정보가 포함된 데이터베이스의 한 항목에 해당합니다. 즉, 프로필은 다음과 같습니다.클라이언트, 잠재 고객, 뉴스레터에 가입된 개인, 수신자, 사용자 또는 조직에 따라 기타 모든 디노미네이션이 포함됩니다.

**자세한 내용**

* [프로필 기본 정보](../../audiences/using/about-profiles.md)
* [조직의 활성 프로필 수 액세스](../../audiences/using/active-profiles.md)

## 데이터베이스 {#populating-database} 실행

<img width="60px" alt="조건" src="assets/icon_populate.svg"/>

Campaign Standard은 마케팅 데이터베이스를 확장하는 데 도움이 되는 여러 도구를 제공합니다. 이 섹션에서는 전용 문서에 대한 참조와 함께 데이터를 Campaign에 주입하는 데 사용할 수 있는 다양한 방법에 대해 자세히 설명합니다.

### 워크플로우 {#importing-data-through-workflows}을(를) 통해 데이터 가져오기

워크플로우를 사용하면 [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) 활동을 사용하여 데이터를 수집하고 캠페인 데이터베이스로 가져올 수 있습니다. 워크플로우를 통해 데이터를 가져올 때의 일반 정보 및 우수 사례는 [이 섹션](../../automating/using/about-data-import-and-export.md)에 있습니다.

또한 템플릿을 설정하여 데이터를 가져올 수 있습니다. 가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져와야 하는 경우에 가장 좋습니다. 다음과 같은 두 가지 유형의 템플릿을 설정할 수 있습니다.

* **워크플로우 템플릿**:이러한 워크플로우는 필요에 따라 한 번 설정하여 데이터를 가져오고 데이터베이스를 업데이트할 때마다 재사용할 수 있도록 미리 구성된 워크플로우입니다. 데이터를 가져오는 워크플로우 템플릿의 예는 [이 섹션](../../automating/using/creating-import-workflow-templates.md)에 자세히 설명되어 있습니다.

* **데이터 템플릿 가져오기**:워크플로우 템플릿과 마찬가지로 데이터베이스를 업데이트하기 위해 파일을 업로드하도록 설정된 워크플로우를 기반으로 하는 템플릿입니다. 구성된 후에는 **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** 메뉴에서 간소화된 보기를 사용하는 사용자가 사용할 수 있게 됩니다. 데이터 템플릿 가져오기에 대한 자세한 내용은 [전용 설명서](../../automating/using/importing-data-with-import-templates.md)를 참조하십시오.

### 랜딩 페이지 {#collecting-data-from-landing-pages}에서 데이터 수집

랜딩 페이지는 데이터를 수집하고 데이터베이스에서 기존 정보를 만들거나 업데이트하는 데 사용할 수 있는 웹 양식입니다. 그 원리는 다음과 같다.

* 입력 필드를 추가하여 데이터(이름, 성, 이메일 등)를 수집함으로써 랜딩 페이지를 만들고 디자인합니다.
* 각 입력 필드를 데이터베이스의 해당 필드에 매핑합니다.
* 랜딩 페이지를 웹 사이트를 통해 또는 메시지에 직접 링크를 통해 온라인으로 사용할 수 있도록 합니다.

랜딩 페이지에 대한 자세한 내용은 [전용 설명서](../../channels/using/getting-started-with-landing-pages.md)를 참조하십시오.

**자세한 내용**

* xxxx
* xxxx

### Microsoft Dynamics 365에서 프로필 동기화

Microsoft Dynamics 365와의 Campaign Standard 통합을 통해 Microsoft Dynamics 365의 연락처 데이터를 Campaign 데이터베이스로 전달할 수 있습니다.
그런 다음 이러한 연락처는 프로필 목록에 표시되며 마케팅 캠페인에서 타깃팅할 수 있습니다. 이 통합에 대한 자세한 내용은 [전용 설명서](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)를 참조하십시오.

>[!NOTE]
>
>Campaign Standard-Microsoft Dynamics 365 커넥터는 현재 제한된 사용 가능 여부에 따라 몇 가지 제한 사항이 설명서에 설명되어 있습니다.

**자세한 내용**

* xxxx
* xxxx

### API 호출을 통해 데이터 가져오기

Campaign Standard API를 사용하면 프로필 또는 서비스의 생성, 업데이트 또는 삭제와 같은 데이터베이스를 업데이트하는 작업을 수행할 수 있습니다. API 사용 방법에 대한 자세한 내용은 [전용 설명서](../../api/using/get-started-apis.md)를 참조하십시오.

>[!CAUTION]
>
>API 호출을 통해 프로파일 대량 생성 또는 업데이트를 수행하기 전에 라이센스 계약에 해당하는 비율 제한을 확인하십시오. 자세한 정보는 이 [페이지](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers)를 참조하십시오.

**자세한 내용**

* xxxx
* xxxx

## 대상 구성 {#organizing-audiences}

<img width="60px" alt="조건" src="assets/icon_audience.svg"/>

Adobe Campaign은 고객의 관심사와 연관성 있고 효과적인 메시지를 전달하고 고객의 효과적인 참여를 유도하기 위해 고급 분석 및 타깃팅 기능을 통합합니다.

워크플로우 및 쿼리 편집기 덕분에, 고객에 대한 정보, 활동, 언어, 기본 설정 또는 마케팅 내역에 따라 다른 캠페인으로 타깃팅되는 대상을 만들 수 있습니다. 이렇게 하면 예를 들어 가입된 프로필을 필터링하거나 기준 수에 제한 없이 타겟 대상을 만들 수 있습니다.

**자세한 내용**

* [대상자 기본 정보](../../audiences/using/about-audiences.md)
* [대상자 만들기](../../audiences/using/creating-audiences.md)

## 개인 정보 관리 {#privacy-management}

<img width="60px" alt="조건" src="assets/icon_privacy.svg"/>

GDPR은 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호법입니다. GDPR은 유럽 연합에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다. Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 보존 설정 및 사용자 역할 포함) 이외에도 Adobe는 데이터 프로세서로서 추가적인 기능을 제공하여 특정 GDPR 요청에 대해 데이터 컨트롤러로서의 준비를 용이하게 하기 위해 이 기회를 활용하고 있습니다.

GDPR 준수를 위해 Adobe Campaign에서 제공하는 툴과 기능에 대한 자세한 내용은 이 [안내서](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html)를 참조하십시오.

**자세한 내용**

* xxxx
* xxxx