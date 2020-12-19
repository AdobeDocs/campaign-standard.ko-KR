---
solution: Campaign Standard
product: campaign
title: API를 통한 데이터 수집 트리거
description: API를 통해 데이터 수집을 트리거하는 방법을 알아봅니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 5%

---


# API를 통한 데이터 수집 트리거 {#triggering-data-ingestion-apis}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 사전 예고 없이 빈번하게 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

Adobe Campaign Standard을 사용하면 API를 통해 데이터 매핑의 즉각적인 수집을 트리거할 수 있고 통합 요청의 상태를 검색할 수 있습니다.

이 페이지에서는 데이터 매핑의 통합 상태를 트리거하고 검색하는 방법에 대해 설명합니다. Campaign Standard API에 대한 전역 정보는 [이 섹션](../../api/using/get-started-apis.md)을 참조하십시오.

## 사전 요구 사항 {#prerequisites}

API를 사용하기 전에 먼저 데이터 매핑이 Campaign Standard 인터페이스 내에서 구성 및 게시되어야 합니다. 자세한 내용은 다음 섹션을 참조하십시오.

* [매핑 정의](../../developing/using/aep-mapping-definition.md)
* [매핑 활성화](../../developing/using/aep-mapping-activation.md)

데이터 매핑이 생성되면 원할 때마다 API에서 트리거할 수 있도록 데이터 매핑이 실행되지 않도록 중지해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. Campaign Standard에서 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** 메뉴로 이동합니다.

1. 데이터 매핑을 두 번 클릭하여 연 다음 **[!UICONTROL Stop]** 단추를 클릭합니다.

   ![](assets/aep_datamapping_stop.png)

1. 변경 내용을 저장합니다

이제 데이터 매핑 실행이 중지됩니다. Campaign Standard API를 사용하여 수동으로 트리거할 수 있습니다.

## 데이터 매핑 {#starting-immediate-ingestion}에 대한 즉각적인 인제스트 시작

XDM 매핑을 Adobe Experience Platform에 즉시 수집하는 작업은 POST 작업으로 트리거됩니다.

`POST https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest`

>[!NOTE]
>
>인제스트 POST API 호출을 실행하려면 사용자에게 **SQL 함수 실행** 역할이 있어야 합니다. 이 역할은 Campaign Standard 관리자가 JS 스크립트 아래 를 실행하여 제공할 수 있습니다.
>
>
```
>var sqlRoleObj = REST.head.roleBase.sql.get();
>REST.head.securityGroup.Administrators.roles.post(sqlRoleObj);
>```

POST 작업은 생성된 요청 상태와 관련된 정보를 반환합니다.

* XDM 매핑에 대한 요청을 제출했습니다.

```
{
"requestId": <value>,
"info": "Ingestion request submitted successfully for the Mapping ID: <value>",
"status":"Success"
}
```

* XDM 매핑에 대한 요청이 이미 진행 중입니다.

```
{
"requestId": <value>,
"info": "Ingestion request already in progress for the Mapping ID: <value>",
"status":"In Progress"
}
```

* XDM 매핑이 게시되지 않았거나 중지되어 요청이 실패했습니다.

```
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not stopped",
"status": "Failed"
}
{
"info": "Unable to submit data ingestion request, XDM Mapping ID: <value> is not published",
"status": "Failed"
}
```

## 통합 요청 상태 검색 중 {#retrieving-status}

통합 요청의 상태는 매개 변수에서 GET 작업과 원하는 요청 ID를 사용하여 검색할 수 있습니다.

```
GET https://mc.adobe.io/<ORGANIZATION>/campaign/dataIngestion/xdmIngestion/<XDM Mapping ID>/ingest
{"requestId"="<value>"}
```

>[!NOTE]
>
>XDM 매핑 요청 상태 및 관련 작업에 대한 자세한 내용은 **[!UICONTROL Status of data export to platform]** 메뉴([매핑 활성화](../../developing/using/aep-mapping-activation.md) 참조)에서 Campaign Standard 인터페이스에서 확인할 수 있습니다.

GET 작업은 아래 정보를 반환합니다.

* **batchId**:이 필드는 일괄 준비 및 업로드 후에 오류가 발생한 경우에만 채워집니다.
* **정보**:XDM 매핑 ID,
* **numRecords**:인제스트한 레코드 수(성공 상태만 해당),
* **상태**:인제스트 요청 상태(성공/실패/진행 중)

GET 작업에 가능한 응답은 다음과 같습니다.

* 요청을 인제스트했습니다.

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ",
   "numRecords": 15,
   "requestId": 3520,
   "status": "Success"
   }
   ```

* 인제스트된 레코드 0으로 인제스트 요청이 실패했습니다.

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. ACP-880056 Failed to fetch the record from the database.",
   "numRecords": 0,
   "requestId": 3520,
   "status": "Failed"
   }
   ```

* 인제스트 요청이 실패했습니다. 일부 레코드가 일괄 처리 아래에 업로드되었습니다.

   ```
   {
   "batchId": "<value>",
   "info": "Mapping Id: <value>. ACP-880096 Sync Job failed to upload. Please check the error in the Platform UI.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Failed"
   }
   ```

* 일부 레코드를 인제스트한 후 인제스트 요청이 중단되었습니다(충돌 시나리오에서 발생할 수 있음).

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>. Ingestion request aborted due to some issue with data ingestion service. Please submit a new request",
   "numRecords": 0,
   "requestId": <value>,
   "status": "Aborted"
   }
   ```

* 요청 인제스트 진행 중(요청이 데이터를 일괄 처리로 업로드한 경우 또는 일괄적으로 요청을 준비하는 경우):

   ```
   {
   "batchId": "",
   "info": "Mapping Id: <value>.",
   "numRecords": 0,
   "requestId": <value>,
   "status": "In Progress"
   }
   ```
