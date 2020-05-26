---
title: 가져오기 모범 사례
description: 데이터를 데이터베이스로 가져올 때 따라야 할 최상의 방법에 대해 자세히 알아보십시오.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# 가져오기 모범 사례 {#import-best-practices}

아래 설명된 몇 가지 간단한 규칙을 주의하여 준수하면 데이터베이스 내에서 데이터 일관성을 유지하고 데이터베이스 업데이트나 데이터 내보내기 중 일반적인 오류를 방지하는 데 많은 도움이 됩니다.

## 가져오기 템플릿 사용 {#using-import-templates}

대부분의 가져오기 워크플로우는 다음 활동을 포함해야 합니다. **[!UICONTROL Load file]**, **[!UICONTROL Reconciliation]**, **[!UICONTROL Segmentation]**, **[!UICONTROL Deduplication]**, **[!UICONTROL Update data]**

가져오기 템플릿을 사용하면 유사한 가져오기를 준비하고 데이터베이스 내에서 데이터를 일관되게 유지할 수 있습니다.

많은 프로젝트에서 가져오기는 프로젝트에 사용된 파일에 중복이 없으므로 **[!UICONTROL Deduplication]** 작업 없이 빌드됩니다. 여러 파일을 가져올 때 중복되는 경우가 있습니다. 데이터 중복 제거는 매우 어렵습니다. 따라서 데이터 중복 제거 단계는 모든 가져오기 워크플로우에 적합한 예방책입니다.

수신 데이터가 일관되고 올바르거나 IT 부서 또는 Adobe Campaign 감독자가 해결할 것이라고 가정할 때는 주의하지 마십시오. 프로젝트 중에 데이터 청소에 주의하십시오. 데이터를 가져올 때 데이터 중복 제거, 조정, 일관성 유지

데이터를 가져오기 위해 디자인된 일반 워크플로우 템플릿의 예는 다음 [예제에서 사용할 수 있습니다. 워크플로우 템플릿](#example--import-workflow-template) 섹션 가져오기

>[!NOTE]
>
>가져오기 템플릿을 사용할 수도 [있습니다](../../automating/using/importing-data-with-import-templates.md). 관리자가 정의한 워크플로우 템플릿으로서, 활성화한 후에는 가져올 데이터가 포함된 파일을 지정할 수 있습니다.

**관련 항목:**

* [파일 작업 로드](../../automating/using/load-file.md)
* [조정 활동](../../automating/using/reconciliation.md)
* [세분화 활동](../../automating/using/segmentation.md)
* [데이터 중복 제거 활동](../../automating/using/deduplication.md)
* [데이터 활동 업데이트](../../automating/using/update-data.md)

## 플랫 파일 포맷 사용 {#using-flat-file-formats}

가장 효율적인 포맷은 플랫 파일입니다. 데이터베이스 수준에서 플랫 파일을 벌크 모드로 가져올 수 있습니다.

예:

* 구분 문자: 탭 또는 세미콜론
* 머리글이 있는 첫 줄
* 문자열 구분 기호 없음
* 날짜 형식: YYYY/MM/DD HH:mm:SS

가져올 파일의 예:

```
lastname;firstname;birthdate;email;crmID
Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
Mars;Daniel;17/11/1987;dannymars@example.com;123545
Smith;Clara;08/02/1989;hayden.smith@example.com;124567
Durance;Allison;15/12/1978;allison.durance@example.com;120987
```

## 압축 사용 {#using-compression}

압축을 푼 파일을 가져와 내보낼 수 있습니다. GZIP은 기본적으로 지원됩니다. 파일을 가져올 때 또는 데이터를 추출할 때 각각 **[!UICONTROL Load file]** 및 워크플로우 활동에서 사전 처리를 추가할 수 **[!UICONTROL Extract file]** 있습니다.

**관련 항목:**

* [파일 작업 로드](../../automating/using/load-file.md)
* [파일 작업 추출](../../automating/using/extract-file.md)

## 델타 모드로 가져오기 {#importing-in-delta-mode}

일반 가져오기는 델타 모드에서 수행해야 합니다. 즉, 수정되거나 새 데이터만 매번 전체 테이블이 아닌 Adobe Campaign으로 전송됩니다.

전체 가져오기는 초기 로드에만 사용해야 합니다.

## 일관성 유지 {#maintaining-consistency}

Adobe Campaign 데이터베이스에서 데이터 일관성을 유지하려면 아래 원칙을 따르십시오.

* 가져온 데이터가 Adobe Campaign의 참조 테이블과 일치하는 경우 워크플로우의 해당 테이블과 조정되어야 합니다. 일치하지 않는 레코드는 거부해야 합니다.
* 가져온 데이터가 항상 **&quot;표준화&quot;** (이메일, 전화 번호, DM 주소)되었는지,이러한 표준화가 안정적이며 수년 동안 변경되지 않는지 확인합니다. 그렇지 않은 경우 데이터베이스에 일부 중복 항목이 나타날 수 있으며 Adobe Campaign에서 &quot;퍼지&quot; 일치를 수행하는 도구를 제공하지 않으므로 이러한 중복 항목을 관리하고 제거하는 것은 매우 어렵습니다.
* 트랜잭션 데이터에는 조정 키가 있어야 하며, 중복을 만들지 않도록 기존 데이터와 조정해야 합니다.
* **관련 파일을 순서대로 가져올 수 있습니다**. 가져오기가 서로 의존하는 여러 파일로 구성된 경우 워크플로우는 파일을 올바른 순서로 가져왔는지 확인해야 합니다. 파일이 실패하면 다른 파일을 가져올 수 없습니다.
* **데이터를 가져올 때**&#x200B;데이터 중복 제거, 조정, 일관성 유지
