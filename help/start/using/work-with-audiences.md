---
title: 목록 사용자 정의
description: '"Learn how to customize display and act on list screens in Adobe Campaign Standard:sorting, filtering, deleting or duplicating elements. 화면에 하나 또는 여러 개의 지정된 리소스의 요소가 표시됩니다."'
audience: start
content-type: reference
topic-tags: discovering-the-interface
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---


# 프로필 및 대상자를 사용한 작업

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
<td>Enriching your database</td>
<td>대상자 구성</td>
<td>개인 정보 보호 관리</td>
</tr>
</table>

## 고객 프로필 {#customer-profiles}

<img width="60px" alt="조건" src="assets/icon_profile.svg"/>

Adobe Campaign profiles represent all of the contacts stored in the database. 각 프로필은 데이터베이스의 한 항목에 해당하며, 이 항목에는 해당 프로필을 타겟팅하고 검증하며 개별적으로 추적하는 데 필요한 정보가 포함됩니다. This means that a profile can be: a client, a prospect, an individual subscribed to a newsletter, a recipient, a user, or any other denomination depending on the organization.

**자세히 표시**

* [프로필 기본 정보](../../audiences/using/about-profiles.md)
* [조직의 활성 프로필 수 액세스](../../audiences/using/active-profiles.md)

## 데이터베이스 강화 {#populating-database}

<img width="60px" alt="조건" src="assets/icon_populate.svg"/>

Campaign Standard은 마케팅 데이터베이스를 확장하는 데 도움이 되는 몇 가지 도구를 제공합니다. 이 섹션에서는 Campaign에 데이터를 주입하는 데 사용할 수 있는 다양한 방법과 전용 설명서에 대한 참조를 자세히 설명합니다.

### 워크플로우를 통해 데이터 가져오기 {#importing-data-through-workflows}

Workflows allow you to collect data and import it into Campaign database through the use of [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) activities. 워크플로우를 통해 데이터를 가져올 때 일반적인 정보 및 모범 사례는 다음과 같습니다. [이 섹션](../../automating/using/about-data-import-and-export.md).

또한 템플릿을 설정하여 데이터를 가져올 수도 있습니다. 가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져오는 가장 좋은 방법입니다. You can set up two types of templates:

* **워크플로우 템플릿**: 미리 구성된 워크플로우로서, 필요에 따라 한 번 설정하고, 데이터를 가져오고 데이터베이스를 업데이트할 때마다 재사용할 수 있습니다. 데이터를 가져오는 워크플로우 템플릿의 예는 다음과 같습니다. [이 섹션](../../automating/using/creating-import-workflow-templates.md).

* **Import data templates**: like workflow templates, these are templates based on workflows, that are set up to upload files to update the database. Once configured, they are made available to users with a simplified view under the **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** menu. 데이터 템플릿 가져오기에 대한 자세한 내용은 [전용 설명서](../../automating/using/importing-data-with-import-templates.md).

### 랜딩 페이지에서 데이터 수집 {#collecting-data-from-landing-pages}

Landing pages are web forms that can be used to collect data and create or update existing information in your database. 원칙은 다음과 같습니다.

* 입력 필드를 추가하여 데이터(이름, 성, 이메일 등)를 수집하여 랜딩 페이지를 만들고 디자인합니다.
* 각 입력 필드를 데이터베이스의 해당 필드에 매핑합니다.
* 랜딩 페이지를 웹 사이트를 통해 또는 메시지에 대한 직접 링크를 통해 온라인으로 사용할 수 있도록 합니다.

랜딩 페이지에 대한 자세한 내용은 [전용 설명서](../../channels/using/getting-started-with-landing-pages.md).

**자세히 표시**

* xxxx
* xxxx

### Microsoft Dynamics 365에서 프로필 동기화

Microsoft Dynamics 365와 Campaign Standard 통합을 통해 Microsoft Dynamics 365의 연락처 데이터를 Campaign 데이터베이스에 전달할 수 있습니다.
These contacts are then visible in the Profiles list and can be targeted in marketing campaigns. 이 통합에 대한 자세한 내용은 [전용 설명서](../../integrating/using/d365-acs-get-started.md).

>[!NOTE]
>
>Campaign Standard-Microsoft Dynamics 365 커넥터는 현재 제한된 사용 가능 상태이며 문서에 자세히 설명된 몇 가지 제한 사항을 따라야 합니다.

**자세히 표시**

* xxxx
* xxxx

### API 호출을 통해 데이터 가져오기

Campaign Standard API를 사용하면 프로필 또는 서비스의 만들기, 업데이트 또는 삭제와 같은 데이터베이스를 업데이트하는 작업을 수행할 수 있습니다. API 사용 방법에 대한 자세한 내용은 [전용 설명서](../../api/using/get-started-apis.md).

>[!CAUTION]
>
>API 호출을 통해 프로필을 대량 만들거나 업데이트하기 전에 라이선스 계약에 해당하는 크기 제한 사항을 확인하십시오. 자세한 정보는 이 [페이지](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers)를 참조하십시오.

**자세히 표시**

* xxxx
* xxxx

## 대상자 구성 {#organizing-audiences}

<img width="60px" alt="조건" src="assets/icon_audience.svg"/>

To enable you to deliver relevant and effective messages, and engage your customers effectively, Adobe Campaign integrates advanced analysis and targeting functionalities.

Thanks to the workflows and the query editor, you can build audiences that will be targeted by your different campaigns, depending on the information that you have on them, their activities, their language, their preferences or their marketing history. This allows you to filter subscribed profiles for example, or create target audiences on an unlimited number of criteria.

**자세히 표시**

* [대상자 기본 정보](../../audiences/using/about-audiences.md)
* [대상자 만들기](../../audiences/using/creating-audiences.md)

## 개인 정보 관리 {#privacy-management}

<img width="60px" alt="조건" src="assets/icon_privacy.svg"/>

GDPR은 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호법입니다. GDPR은 유럽 연합에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다. In addition to the privacy capabilities already available in Adobe Campaign (including consent management, data retention settings, and user roles), we are taking this opportunity in our role as a Data Processor to include additional capabilities, to help facilitate your readiness as a Data Controller for certain GDPR requests.

다음을 참조하십시오 [안내서](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=ko#getting-started) Adobe Campaign이 GDPR을 준수하는 데 도움이 되는 도구와 기능에 대해 자세히 알아보십시오.

**자세히 표시**

* xxxx
* xxxx