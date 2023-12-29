---
title: 목록 사용자 정의
description: "Adobe Campaign Standard에서 목록 화면 표시 및 작업을 사용자 지정하는 방법: 요소 정렬, 필터링, 삭제 또는 복제. 화면에 지정된 하나 또는 여러 리소스의 요소가 표시됩니다."
audience: start
content-type: reference
topic-tags: discovering-the-interface
source-git-commit: bee4da592e0b3727949bc44c6e41b81d4e7e73d4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 6%

---


# 프로필 및 대상자 작업

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
<td>대상자 구성</td>
<td>개인 정보 보호 관리</td>
</tr>
</table>

## 고객 프로필 {#customer-profiles}

<img width="60px" alt="조건" src="assets/icon_profile.svg"/>

Adobe Campaign 프로필은 데이터베이스에 저장된 모든 연락처를 나타냅니다. 각 프로필은 데이터베이스의 한 항목에 해당하며, 여기에는 해당 프로필이 타겟팅되고 검증되고 개별적으로 추적되는 데 필요한 정보가 포함되어 있습니다. 즉, 프로필은 클라이언트, 잠재 고객, 뉴스레터를 구독한 개인, 수신자, 사용자 또는 조직에 따른 기타 모든 단체일 수 있습니다.

**자세히 보기**

* [프로필 기본 정보](../../audiences/using/about-profiles.md)
* [조직의 활성 프로필 수에 액세스](../../audiences/using/active-profiles.md)

## 데이터베이스 강화 {#populating-database}

<img width="60px" alt="조건" src="assets/icon_populate.svg"/>

Campaign Standard은 마케팅 데이터베이스를 확장하는 데 도움이 되는 몇 가지 도구를 제공합니다. 이 섹션에서는 전용 설명서를 참조하여 Campaign에 데이터를 삽입하는 데 사용할 수 있는 다양한 방법에 대해 자세히 설명합니다.

### 워크플로우를 통해 데이터 가져오기 {#importing-data-through-workflows}

워크플로우를 사용하면 데이터를 수집하고 을 사용하여 Campaign 데이터베이스로 가져올 수 있습니다. [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) 활동. 워크플로우를 통해 데이터를 가져올 때의 일반 정보 및 모범 사례는에 나와 있습니다. [이 섹션](../../automating/using/about-data-import-and-export.md).

또한 템플릿을 설정하여 데이터를 가져올 수 있습니다. 가져오기 템플릿을 사용하는 것은 정기적으로 동일한 구조의 파일을 가져오는 가장 좋은 방법입니다. 두 가지 유형의 템플릿을 설정할 수 있습니다.

* **워크플로 템플릿**: 사전 구성된 워크플로우로서, 필요에 따라 한 번 설정하고 데이터를 가져오고 데이터베이스를 업데이트할 때마다 재사용할 수 있습니다. 데이터를 가져오기 위한 워크플로우 템플릿의 예는에 자세히 설명되어 있습니다. [이 섹션](../../automating/using/creating-import-workflow-templates.md).

* **데이터 템플릿 가져오기**: 워크플로우 템플릿과 마찬가지로 데이터베이스를 업데이트할 파일을 업로드하도록 설정된 워크플로우를 기반으로 하는 템플릿입니다. 구성하고 나면 아래에 간소화된 보기가 있는 사용자가 사용할 수 있습니다. **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** 메뉴 아래의 제품에서 사용할 수 있습니다. 데이터 템플릿 가져오기에 대한 자세한 내용은 [전용 설명서](../../automating/using/importing-data-with-import-templates.md).

### 랜딩 페이지에서 데이터 수집 {#collecting-data-from-landing-pages}

랜딩 페이지는 데이터를 수집하고 데이터베이스에서 기존 정보를 만들거나 업데이트하는 데 사용할 수 있는 웹 양식입니다. 원칙은 다음과 같습니다.

* 데이터(이름, 성, 이메일 등)를 수집하기 위한 입력 필드를 추가하여 랜딩 페이지를 만들고 디자인합니다.
* 각 입력 필드를 데이터베이스의 해당 필드와 매핑합니다.
* 랜딩 페이지를 웹 사이트 또는 메시지에 대한 직접 링크를 통해 온라인으로 사용할 수 있도록 합니다.

랜딩 페이지에 대한 자세한 내용은 [전용 설명서](../../channels/using/getting-started-with-landing-pages.md).

**자세히 보기**

* xxxx
* xxxx

### Microsoft Dynamics 365에서 프로필 동기화

Microsoft Dynamics 365와 Campaign Standard을 통합하면 Microsoft Dynamics 365의 연락처 데이터를 Campaign 데이터베이스에 전달할 수 있습니다.
그러면 이러한 연락처는 프로필 목록에 표시되며 마케팅 캠페인에서 타겟팅할 수 있습니다. 이 통합에 대한 자세한 내용은 [전용 설명서](../../integrating/using/d365-acs-get-started.md).

>[!NOTE]
>
>Campaign Standard-Microsoft Dynamics 365 커넥터는 현재 제한된 가용성이며 설명서에 자세히 나와 있는 몇 가지 제한 사항이 있습니다.

**자세히 보기**

* xxxx
* xxxx

### API 호출을 통해 데이터 가져오기

Campaign Standard API를 사용하면 프로필 또는 서비스의 만들기, 업데이트 또는 삭제와 같이 데이터베이스를 업데이트하는 작업을 수행할 수 있습니다. API 사용 방법에 대한 자세한 내용은 [전용 설명서](../../api/using/get-started-apis.md).

>[!CAUTION]
>
>API 호출을 통해 프로필을 대량으로 만들거나 업데이트하기 전에 라이선스 계약에 해당하는 크기 제한 사항을 확인하십시오. 자세한 정보는 이 [페이지](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers)를 참조하십시오.

**자세히 보기**

* xxxx
* xxxx

## 대상자 구성 {#organizing-audiences}

<img width="60px" alt="조건" src="assets/icon_audience.svg"/>

Adobe Campaign은 관련성 있고 효과적인 메시지를 전달하고 효과적으로 고객을 참여시킬 수 있도록 고급 분석 및 타기팅 기능을 통합합니다.

워크플로우 및 쿼리 편집기 덕분에 보유한 정보, 활동, 언어, 환경 설정 또는 마케팅 내역에 따라 다양한 캠페인이 타겟팅하는 대상을 구축할 수 있습니다. 이를 통해 구독한 프로필 등을 필터링하거나 기준을 제한 없이 타겟 대상자를 만들 수 있습니다.

**자세히 보기**

* [대상자 기본 정보](../../audiences/using/about-audiences.md)
* [대상자 만들기](../../audiences/using/creating-audiences.md)

## 개인 정보 관리 {#privacy-management}

<img width="60px" alt="조건" src="assets/icon_privacy.svg"/>

GDPR은 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호법입니다. GDPR은 EU에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다. Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 보존 설정 및 사용자 역할 포함) 외에도 데이터 처리자로서의 역할에서 이 기회를 포착하여 추가 기능을 포함하여 특정 GDPR 요청에 대한 데이터 컨트롤러로서의 준비를 용이하게 합니다.

을(를) 참조하십시오 [이 섹션](../../start/using/privacy.md) Adobe Campaign이 GDPR을 준수하는 데 도움이 되는 도구 및 기능에 대해 자세히 알아보십시오.

**자세히 보기**

* xxxx
* xxxx