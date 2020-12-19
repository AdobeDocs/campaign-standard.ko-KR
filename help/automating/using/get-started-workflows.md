---
solution: Campaign Standard
product: campaign
title: 프로세스 및 데이터 관리 시작하기
description: 작업 과정을 통해 프로세스를 자동화하고 데이터 및 고객을 관리하며 메시지 전송 등을 수행할 수 있습니다.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 13%

---


# 프로세스 및 데이터 관리 시작하기 {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">워크플로우 활동</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">사용 사례</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">데이터 필터링</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">데이터 가져오기/내보내기</a></p></td></tr>
</table>

Adobe Campaign은 세그먼테이션, 캠페인 실행, 파일 처리 등 복잡한 프로세스를 디자인할 수 있는 포괄적인 그래픽 환경을 제공합니다. 예를 들어 작업 과정을 사용하여 서버에서 파일을 다운로드하고 압축을 푼 다음 해당 레코드를 Adobe Campaign 데이터베이스로 가져올 수 있습니다.

또한 워크플로우에는 작업을 할당하거나 사용자가 수행한 작업을 승인하도록 하여 사용자를 포함할 수 있습니다. 즉, 메시지를 보내기 전에 하나 이상의 사용자에게 컨텐츠를 작업하거나 대상을 지정하고 교정본을 승인할 작업을 지정할 수 있습니다.

워크플로우는 다음과 같이 서로 다른 컨텍스트에서 사용할 수 있습니다.

* 대상을 관리하거나 메시지를 보내기 위한 타깃팅입니다.
* ETL(데이터 관리)을 통해 데이터를 조작할 수 있습니다.
* 데이터를 Campaign 데이터베이스로 가져옵니다.
* 데이터베이스 정리, 추적 정보 복구 등의 기술 프로세스

## 워크플로 활동 {#workflow-activities}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

워크플로우를 디자인하는 데 도움이 되는 다양한 활동을 사용할 수 있습니다.

[타깃팅 활동](../../automating/using/about-targeting-activities.md) 을 사용하면 세트를 정의하고 교차, 결합 또는 제외 작업을 사용하여 이러한 세트를 분할하거나 결합하여 하나 이상의 대상을 만들 수 있습니다.

[실행 활동](../../automating/using/about-execution-activities.md)을 사용하여 작업 과정 및 해당 활동을 조정할 수 있고, [채널 활동](../../automating/using/about-channel-activities.md)을 사용하면 Campaign Standard 통신 채널을 결합하여 크로스 채널 워크플로우를 만들 수 있습니다.

마지막으로 [데이터 관리 활동](../../automating/using/about-data-management-activities.md)을 사용하면 데이터베이스의 데이터를 조작할 수 있습니다.

자세한 내용:

* [워크플로우 구축](../../automating/using/building-a-workflow.md)
* [워크플로우 실행](../../automating/using/about-workflow-execution.md)
* [워크플로우 모범 사례](../../automating/using/best-practices-workflows.md)

## 데이터 필터링 {#filter-data}

<img src="assets/do-not-localize/icon_filter.svg" width="60px">

**쿼리 편집기**&#x200B;를 활용하여 데이터베이스의 데이터를 필터링하고 수신자를 더 잘 타깃팅할 수 있도록 모집단을 구성합니다. 쿼리 편집기를 사용하여 Campaign Standard에서 여러 작업을 수행할 수 있습니다.쿼리 유형 대상을 만들고, 전달 대상 또는 모집단을 워크플로우 활동에 정의합니다.

쿼리 편집기에는 빠르고 간편한 필터링을 위해 **사전 정의된 필터 및 규칙**&#x200B;이 포함되어 있습니다. 그러나 **고급 표현식 편집** 기능을 사용할 수도 있습니다. 따라서 고유한 규칙을 구성하기 위해 조건을 수동으로 입력하고 함수를 사용할 수 있습니다.

자세한 내용:

* [쿼리 편집](../../automating/using/editing-queries.md)
* [고급 표현식 편집](../../automating/using/advanced-expression-editing.md)
* [함수 목록](../../automating/using/list-of-functions.md)

## 데이터 가져오기/내보내기 {#import-export-data}

<img src="assets/do-not-localize/icon_manage.svg" width="60px">

Campaign Standard에는 데이터를 가져오고 내보낼 수 있는 **데이터 관리 기능**&#x200B;이 여러 개 포함되어 있습니다.

[워크플로우 데이터 관리 활동](../../automating/using/about-data-management-activities.md) 을 사용하면 데이터를 가져오고, 필드에 대한 일괄 업데이트를 수행하고, 파일을 수신 또는 보내거나, 식별되지 않은 데이터를 기존 리소스에 연결할 수 있습니다.

[템플릿 가져오기](../../automating/using/importing-data-with-import-templates.md)를 사용하면 관리자가 단순화된 가져오기 기능을 통해 정의한 특정 유형의 가져오기를 관리할 수 있습니다.

[로그 ](../../automating/using/exporting-logs.md) 내보내기를 사용하면 간단한 워크플로우를 통해 로그 데이터를 내보낼 수 있으므로 자체 보고 또는 BI 도구에서 마케팅 캠페인의 결과를 분석할 수 있습니다.

예를 들어 인스턴스 구성을 복제하거나 사용자 지정 리소스를 포함하는 다른 서버로 데이터를 전송하기 위해 [패키지](../../automating/using/managing-packages.md)를 활용하여 다른 캠페인 인스턴스 간에 리소스를 교환할 수 있습니다.

마지막으로, [내보내기 목록](../../automating/using/exporting-lists.md)을 사용하면 테스트 프로파일 목록, 검역이메일 주소 목록 등과 같은 Campaign Standard에서 목록을 내보낼 수 있습니다.

자세한 내용:

* [데이터 가져오기 및 내보내기](../../automating/using/about-data-import-and-export.md)
* [사용 사례: 사용자 정의 리소스 내보내기/가져오기](../../automating/using/exporting-importing-custom-resources.md)

## 추가 리소스

* [프로세스 및 데이터 관리 자습서 비디오](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/getting-started/create-workflow.html)
* [기술 워크플로우](../../administration/using/technical-workflows.md)
* [Campaign Standard 데이터 모델 시작](../../developing/using/get-started-data-model.md)
