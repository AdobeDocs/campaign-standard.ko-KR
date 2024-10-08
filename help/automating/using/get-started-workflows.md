---
title: 프로세스 및 데이터 관리 시작
description: 워크플로를 통해 프로세스를 자동화하고 데이터 및 대상자를 관리하며 메시지 전송 등을 수행할 수 있습니다.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Workflows
role: Data Architect
level: Beginner
exl-id: 26be942a-c252-458f-a590-eb235567ca67
source-git-commit: 69621657e1d367043200f741d93972664e6eb8fb
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 26%

---

# 프로세스 및 데이터 관리 시작 {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">워크플로 활동</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">활용 사례</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">데이터 필터링</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">데이터 가져오기/내보내기</a></p></td></tr>
</table>

Adobe Campaign은 세그먼테이션, 캠페인 실행, 파일 처리 등 복잡한 프로세스를 디자인할 수 있는 포괄적인 그래픽 환경을 제공합니다. 예를 들어 워크플로를 통해 서버에서 파일을 다운로드하고 압축을 해제한 다음 Adobe Campaign 데이터베이스에 포함된 레코드를 가져올 수 있습니다.

워크플로는 다음과 같이 서로 다른 컨텍스트에서 사용할 수 있습니다.

* 대상자를 관리하거나 메시지를 보내기 위해 타기팅할 수 있습니다.
* ETL(데이터 관리)을 통해 데이터를 조작할 수 있습니다.
* 데이터를 Campaign 데이터베이스로 가져옵니다.
* 데이터베이스 정리, 추적 정보 복구 등의 기술 프로세스

>[!IMPORTANT]
>
> Adobe은 고객이 20개 이상의 활성 워크플로우 실행을 동시에 실행하지 않도록 하고, 시간에 따라 워크플로우 실행의 우선 순위를 지정하고 분산하도록 권장합니다. 자세한 내용은 [이 페이지](../../automating/using/best-practices-workflows.md)에 제공된 모범 사례를 참조하세요.

## 워크플로 활동 {#workflow-activities}

워크플로우를 디자인하는 데 도움이 되는 다양한 활동을 사용할 수 있습니다.

[타깃팅 활동](../../automating/using/about-targeting-activities.md)을 사용하면 집합을 정의하고 교차, 결합 또는 제외 작업을 사용하여 이러한 집합을 분할하거나 결합하여 하나 이상의 대상을 만들 수 있습니다.

[실행 활동](../../automating/using/about-execution-activities.md)을 사용하여 워크플로우와 해당 활동을 조정하고, [채널 활동](../../automating/using/about-channel-activities.md)을 사용하여 Campaign Standard 통신 채널을 결합하여 크로스채널 워크플로우를 만들 수 있습니다.

마지막으로 [데이터 관리 활동](../../automating/using/about-data-management-activities.md)을 사용하면 데이터베이스에서 데이터를 조작할 수 있습니다.

자세한 내용:

* [워크플로 작성](../../automating/using/building-a-workflow.md)
* [워크플로우 실행](../../automating/using/about-workflow-execution.md)
* [워크플로 모범 사례](../../automating/using/best-practices-workflows.md)

## 데이터 필터링 {#filter-data}

**쿼리 편집기**&#x200B;를 활용하여 데이터베이스에서 데이터를 필터링하고, 받는 사람을 더 잘 타겟팅할 수 있는 모집단을 만드십시오. 쿼리 편집기는 Campaign Standard에서 쿼리 유형 대상 만들기, 게재 대상 정의 또는 워크플로우 활동의 모집단과 같은 몇 가지 작업을 수행할 수 있습니다.

쿼리 편집기에는 빠르고 쉽게 필터링할 수 있도록 **사전 정의된 필터 및 규칙**&#x200B;이 제공됩니다. 그러나 **고급 표현식 편집** 기능을 사용할 수도 있습니다. 이렇게 하면 조건을 수동으로 입력하고 함수를 사용하여 고유한 규칙을 형성할 수 있습니다.

자세한 내용:

* [쿼리 편집](../../automating/using/editing-queries.md)
* [고급 표현식 편집](../../automating/using/advanced-expression-editing.md)
* [함수 목록](../../automating/using/list-of-functions.md)

## 데이터 가져오기/내보내기 {#import-export-data}

Campaign Standard은 데이터를 가져오고 내보낼 수 있는 여러 **데이터 관리 기능**&#x200B;과 함께 제공됩니다.

[워크플로우 데이터 관리 활동](../../automating/using/about-data-management-activities.md)을 통해 데이터를 가져오거나, 필드에 대한 대량 업데이트를 수행하거나, 파일을 받거나 보내거나, 알 수 없는 데이터를 기존 리소스에 연결할 수 있습니다.

[가져오기 템플릿](../../automating/using/importing-data-with-import-templates.md)을 사용하여 관리자가 정의한 특정 유형의 가져오기를 간소화된 가져오기 기능을 통해 관리하십시오.

[로그 내보내기](../../automating/using/exporting-logs.md)를 사용하면 간단한 워크플로우를 통해 로그 데이터를 내보낼 수 있으므로 자체 보고 또는 BI 도구에서 마케팅 캠페인의 결과를 분석할 수 있습니다.

[패키지](../../automating/using/managing-packages.md)를 사용하여 서로 다른 캠페인 인스턴스 간에 리소스를 교환하거나(예: 인스턴스의 구성을 복제하거나) 서버에서 사용자 지정 리소스를 포함한 다른 서버로 데이터를 전송합니다.

마지막으로 [목록 내보내기](../../automating/using/exporting-lists.md)를 사용하면 Campaign Standard에서 테스트 프로필 목록, 격리 전자 메일 주소 목록 등과 같은 목록을 내보낼 수 있습니다.

자세한 내용:

* [데이터 가져오기 및 내보내기](../../automating/using/about-data-import-and-export.md)
* [사용 사례: 사용자 정의 리소스 내보내기/가져오기](../../automating/using/exporting-importing-custom-resources.md)

## 추가 리소스

* [프로세스 및 데이터 관리 자습서 비디오](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/managing-processes-and-data/creating-a-workflow.html?lang=ko)
* [기술 워크플로](../../administration/using/technical-workflows.md)
* [Campaign Standard 데이터 모델 시작](../../developing/using/get-started-data-model.md)
