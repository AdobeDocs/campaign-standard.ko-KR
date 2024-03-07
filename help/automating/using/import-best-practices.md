---
title: 가져오기 모범 사례
description: 데이터를 데이터베이스로 가져올 때 따라야 할 모범 사례에 대해 자세히 알아보십시오.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
role: Data Architect
exl-id: bb651b91-145f-4e87-92dd-a8b04662e380
source-git-commit: 21bcc9818b881212985988ef3377687069a1dbea
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 3%

---

# 가져오기 모범 사례 {#import-best-practices}

>[!CAUTION]
>
>이 기능을 사용하는 동안 Adobe Campaign 계약에 따라 SFTP 스토리지, DB 스토리지 및 활성 프로필 제한을 염두에 두십시오.

아래에 설명된 몇 가지 간단한 규칙을 준수하는 것은 데이터베이스 내에서 데이터 일관성을 보장하고 데이터베이스 업데이트 또는 데이터 내보내기 중 일반적인 오류를 방지하는 데 많은 도움이 됩니다.

## 가져오기 템플릿 사용 {#using-import-templates}

대부분의 가져오기 워크플로우에는 다음 활동이 포함되어야 합니다. **[!UICONTROL Load file]**, **[!UICONTROL Reconciliation]**, **[!UICONTROL Segmentation]**, **[!UICONTROL Deduplication]**, **[!UICONTROL Update data]**.

가져오기 템플릿을 사용하면 유사한 가져오기를 준비하고 데이터베이스 내에서 데이터 일관성을 유지하는 것이 매우 편리합니다.

많은 프로젝트에서 가져오기는 **[!UICONTROL Deduplication]** 프로젝트에 사용된 파일에 중복 항목이 없기 때문입니다. 경우에 따라 다른 파일을 가져올 때 중복이 나타납니다. 그러면 중복 제거는 어렵습니다. 따라서 중복 제거 단계는 모든 가져오기 워크플로우에서 좋은 예방책입니다.

들어오는 데이터가 일관되고 정확하다거나 IT 부서나 Adobe Campaign 감독자가 처리한다는 가정 하에 머무르지 마십시오. 프로젝트 진행 중에는 데이터 정리를 염두에 두십시오. 데이터를 가져올 때 중복 제거, 조정 및 일관성 유지

데이터 가져오기를 위해 설계된 일반 워크플로 템플릿의 예는 [예제: 가져오기 워크플로우 템플릿](../../automating/using/creating-import-workflow-templates.md) 섹션.

>[!NOTE]
>
>다음을 사용할 수도 있습니다. [템플릿 가져오기](../../automating/using/importing-data-with-import-templates.md). 관리자가 정의한 워크플로 템플릿으로, 활성화된 후에는 가져올 데이터가 포함된 파일을 지정할 수만 있습니다.

**관련 항목:**

* [파일 활동 로드](../../automating/using/load-file.md)
* [조정 활동](../../automating/using/reconciliation.md)
* [세분화 활동](../../automating/using/segmentation.md)
* [중복 제거 활동](../../automating/using/deduplication.md)
* [데이터 활동 업데이트](../../automating/using/update-data.md)

## 플랫 파일 형식 사용 {#using-flat-file-formats}

가져오기에 가장 효율적인 형식은 플랫 파일입니다. 플랫 파일은 데이터베이스 레벨에서 벌크 모드로 가져올 수 있습니다.

예제:

* 구분 기호: 탭 또는 세미콜론
* 머리글이 있는 첫 번째 줄
* 문자열 구분 기호 없음
* 날짜 형식: `YYYY/MM/DD HH:mm:SS`

가져올 파일의 예:

```
lastname;firstname;birthdate;email;crmID
Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
Mars;Daniel;17/11/1987;dannymars@example.com;123545
Smith;Clara;08/02/1989;hayden.smith@example.com;124567
Durance;Allison;15/12/1978;allison.durance@example.com;120987
```

## 압축 사용 {#using-compression}

가능하면 압축 파일을 사용하여 가져오고 내보냅니다. GZIP은 기본적으로 지원됩니다. 파일을 가져올 때 전처리 작업을 추가하거나 데이터를 추출할 때 후처리를 추가할 수 있습니다. **[!UICONTROL Load file]** 및 **[!UICONTROL Extract file]** 워크플로우 활동.

**관련 항목:**

* [파일 로드 활동](../../automating/using/load-file.md)
* [파일 추출 활동](../../automating/using/extract-file.md)

## 델타 모드에서 가져오기 {#importing-in-delta-mode}

일반 가져오기는 델타 모드에서 수행해야 합니다. 즉, 매번 전체 테이블이 아닌 수정된 데이터나 새로운 데이터만 Adobe Campaign으로 전송됩니다.

전체 가져오기는 초기 로드에만 사용해야 합니다.

## 일관성 유지 {#maintaining-consistency}

Adobe Campaign 데이터베이스에서 데이터 일관성을 유지하려면 아래 원칙을 따르십시오.

* 가져온 데이터가 Adobe Campaign의 참조 테이블과 일치하는 경우 워크플로우의 해당 테이블과 조정되어야 합니다. 일치하지 않는 레코드는 거부해야 합니다.
* 가져온 데이터가 항상 인지 확인합니다. **&quot;정규화됨&quot;** (이메일, 전화번호, DM 주소) 및 이 표준화는 신뢰할 수 있으며 수년에 걸쳐 변경되지 않습니다. 그렇지 않으면 일부 중복 항목이 데이터베이스에 표시될 수 있으며, Adobe Campaign에서 &quot;퍼지&quot; 일치를 수행하는 도구를 제공하지 않으므로 이를 관리하고 제거하기가 매우 어려울 수 있습니다.
* 트랜잭션 데이터는 조정 키를 가져야 하며, 중복을 방지하려면 기존 데이터와 조정되어야 합니다.
* **관련 파일을 순서대로 가져오기**. 가져오기가 서로 종속된 여러 파일로 구성된 경우 워크플로는 파일을 올바른 순서로 가져오는지 확인해야 합니다. 파일이 실패하면 다른 파일은 가져오지 않습니다.
* **중복 제거**&#x200B;데이터를 가져올 때 을 조정하고 일관성을 유지합니다.
