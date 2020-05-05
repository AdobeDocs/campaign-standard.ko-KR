---
title: Campaign Standard 데이터 모델 시작하기
description: 고유한 필드 및 리소스로 Campaign Standard 데이터 모델을 확장하고 모든 데이터 모델 변경 사항을 하나의 보기로 모니터링합니다.
page-status-flag: never-activated
uuid: 7c1e8cea-90d0-491f-ab8f-6cd69f8a6c3b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 40503917-7a53-4d99-96a4-57aa9e98ec87
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 816d550d8bd0de085a47f97c1f6cc2fbb5e7acb9

---


# Campaign Standard 데이터 모델 시작하기 {#get-started-data-model}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_datamodel.svg" width="60px"><p><a href="#data-model">데이터 모델</a></p></td>
<td><img src="assets/do-not-localize/icon_custom.svg" width="60px"><p><a href="#custom-resources">사용자 정의 리소스</a></p></td><td><img src="assets/do-not-localize/icon_api.svg" width="60px"><p><a href="#custom-resources">API를 사용한 작업</a></p></td></tr>
</table>

고유한 필드 및 리소스로 Campaign Standard 데이터 모델을 확장하고 모든 데이터 모델 변경 사항을 하나의 보기로 모니터링합니다.

## 데이터 모델 {#data-model}

<img src="assets/do-not-localize/icon_datamodel.svg" width="60px">

캠페인에서 사용하는 데이터는 **사전 정의된 데이터 모델에 정의된 다른 리소스를 통해 정의됩니다**. 데이터 모델은 마케팅 관련 리소스 세트에 대한 기본 SQL 구조를 표시합니다. 전달, 대상, 랜딩 페이지, 프로필 등 각 리소스에는 관련 필터가 포함되어 있으므로 리소스를 탐색할 수 있습니다.

[ **진단** ] 메뉴를 사용하면 Campaign Standard에서 생성된 기술 개체를 나열할 수 있습니다. 데이터 스키마, 웹 페이지, 필터 등, 데이터 모델 및 변경된 데이터 모델을 모니터링할 수 있습니다.

자세한 내용:

* [데이터 모델 기본 개념](../../developing/using/data-model-concepts.md)
* [데이터 모델 모범 사례](../../developing/using/data-model-best-practices.md)
* [데이터 모델 설명](../../developing/using/datamodel-introduction.md)
* [데이터 모델 변경 모니터링](../../developing/using/monitoring-data-model-changes.md)

## 사용자 정의 리소스 {#custom-resources}

<img src="assets/do-not-localize/icon_custom.svg" width="60px">

Campaign Standard **를 사용하면 사전 정의된 데이터 모델을** 강화하여 고유한 리소스(예: 구매 또는 제품 테이블 추가)를 만들거나 새 필드로 기존 리소스를 확장할 수 있습니다. 만들어진 새 리소스 및 필드를 통해 탐색을 최적화하도록 캠페인 화면을 구성할 수도 있습니다.

또한 사용자 지정 리소스 프로필에 대한 APIs 확장 필드에 표시되도록 Campaign Standard REST API를 **확장할** 수 있습니다. 예를 들어 청구 시스템에서 생성된 프로모션 코드로 고객의 프로필을 업데이트할 수 있습니다.

자세한 내용:

* [리소스 추가 또는 확장](../../developing/using/key-steps-to-add-a-resource.md)
* [API 확장](../../developing/using/about-extending-the-api.md)
* [사용 사례: 새 필드를 사용하여 프로필 리소스 확장](../../developing/using/extending-the-profile-resource-with-a-new-field.md)
* [사용 사례: 애플리케이션 리소스로 구독 확장](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)

## API를 사용한 작업 {#apis}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Adobe Campaign Standard API를 사용하면 Adobe Campaign Standard에 대한 통합을 만들 수 있고 Campaign과 사용하는 기술의 패널을 통합하여 고유한 에코시스템을 구축할 수 있습니다. [Campaign Standard REST API 시작하기](../../api/using/get-started-apis.md)

## 추가 리소스

* [Adobe Experience Platform 데이터 커넥터 정보](../../developing/using/aep-about-data-connector.md)
* [사용자 정의 리소스 만들기(비디오)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/developing/custom-resources-develop/creating-custom-resources.html)
* [사용자 지정 리소스 내보내기/가져오기](https://helpx.adobe.com/campaign/kb/acs-get-started-with-cusres.html)
