---
title: Campaign Standard 데이터 모델 시작
description: 사용자 정의 필드 및 리소스로 Campaign Standard 데이터 모델을 강화하고 REST API를 확장하여 확장된 필드를 표시할 수 있습니다.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Data Model
role: Developer
level: Intermediate
exl-id: a8d15053-c20f-4334-a732-3b36cb00794d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 31%

---

# Campaign Standard 데이터 모델 시작 {#get-started-data-model}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_datamodel.svg" width="60px"><p><a href="#data-model">데이터 모델</a></p></td>
<td><img src="assets/do-not-localize/icon_custom.svg" width="60px"><p><a href="#custom-resources">사용자 정의 리소스</a></p></td><td><img src="assets/do-not-localize/icon_api.svg" width="60px"><p><a href="#custom-resources">API 작업</a></p></td></tr>
</table>

고유한 필드 및 리소스로 Campaign Standard 데이터 모델을 확장하고 모든 데이터 모델 변경 사항을 하나의 보기로 모니터링합니다.

## 데이터 모델 {#data-model}

<img src="assets/do-not-localize/icon_datamodel.svg" width="60px">

Campaign에서 사용하는 데이터는 **사전 정의된 데이터 모델**. 데이터 모델은 마케팅 관련 리소스 세트에 대한 기본 SQL 구조를 표시합니다. 게재, 대상, 랜딩 페이지, 프로필 등 각 리소스에는 관련 필터가 포함되어 있어 리소스를 탐색할 수 있습니다.

다음 **진단** 메뉴를 사용하면 Campaign Standard에서 생성한 기술 객체를 나열할 수 있습니다. 데이터 스키마, 웹 페이지, 필터 등을 사용하면 데이터 모델과 변경된 모든 것을 모니터링할 수 있습니다.

자세히 표시:

* [데이터 모델 기본 개념](../../developing/using/data-model-concepts.md)
* [데이터 모델 모범 사례](../../developing/using/data-model-best-practices.md)
* [데이터 모델 설명](../../developing/using/datamodel-introduction.md)
* [데이터 모델 변경 모니터링](../../developing/using/monitoring-data-model-changes.md)

## 사용자 정의 리소스 {#custom-resources}

<img src="assets/do-not-localize/icon_custom.svg" width="60px">

Campaign Standard을 통해 다음을 수행할 수 있습니다 **사전 정의된 데이터 모델을 보강합니다** 리소스를 직접 만들거나(예: 구매 또는 제품 테이블 추가) 새 필드로 기존 리소스를 확장합니다. 또한 만들어진 새 리소스 및 필드를 통해 탐색을 최적화하도록 Campaign 화면을 구성할 수도 있습니다.

또한 다음을 수행할 수 있습니다 **Campaign Standard REST API 확장** 를 추가하여 사용자 지정 리소스 프로필의 API 확장 필드에 노출합니다. 예를 들어 청구 시스템에서 생성된 프로모션 코드로 고객의 프로필을 업데이트할 수 있습니다.

자세히 표시:

* [리소스 추가 또는 확장](../../developing/using/key-steps-to-add-a-resource.md)
* [API 확장](../../developing/using/about-extending-the-api.md)
* [사용 사례: 새 필드로 프로필 리소스 확장](../../developing/using/extending-the-profile-resource-with-a-new-field.md)
* [사용 사례: 구독을 확장해 애플리케이션 리소스로 만들기](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)

## API 작업 {#apis}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Campaign Standard API를 사용하면 Campaign을 사용하는 기술 패널과 연결하여 Adobe Campaign Standard을 위한 통합을 만들고 고유한 에코시스템을 구축할 수 있습니다. [Campaign Standard REST API 시작](../../api/using/get-started-apis.md)

## 추가 리소스

* [사용자 지정 리소스 내보내기/가져오기](https://helpx.adobe.com/campaign/kb/acs-get-started-with-cusres.html)
* [Campaign에서 Adobe Experience Platform으로 데이터 내보내기](../../integrating/using/export-campaign-data.md)
