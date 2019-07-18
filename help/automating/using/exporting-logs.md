---
title: 로그 내보내기
seo-title: 로그 내보내기
description: 로그 내보내기
seo-description: 로그 데이터는 배달 또는 구독과 관련이 있는지 여부를 간단한 워크플로우를 통해 내보낼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 954 E 919 C -0 A 33-47 C 3-9 A 3 C -63 C 7 A 2 A 4 EDC 4
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: CA 8 A 95 D 8-523 F -4085-A 2 FC-E 1 D 8262 CFBAE
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 36727e82d3aa73add6116fa2916752ff0e407d9d

---


# Exporting logs{#exporting-logs}

로그 데이터는 배달 또는 구독과 관련이 있는지 여부를 간단한 워크플로우를 통해 내보낼 수 있습니다. 이 도구를 사용하면 자체 보고 또는 BI 도구에서 캠페인 결과를 분석할 수 있습니다.

By using an **[!UICONTROL Incremental query]** that only retrieves new logs every time the workflow is executed and a simple **[!UICONTROL Extract file]** activity to define the output columns, you can get a file with the format and all the data you need. Then use a **[!UICONTROL Transfer file]** activity to retrieve the final file. Each workflow execution is planned by a **[!UICONTROL Scheduler]**.

내보내기 로그 작업은 표준 사용자가 수행할 수 있습니다. Private resources such as: broadlogs, tracking logs, exclusion logs subscription logs and subscription history logs on **Profiles** can only be managed by functional administrator.

1. Create a new workflow as detailed in [this section](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. **[!UICONTROL Scheduler]** 활동을 추가하고 필요에 따라 설정합니다. 다음은 월별 실행의 예입니다.

   ![](assets/export_logs_scheduler.png)

1. **[!UICONTROL Incremental query]** 활동을 추가하고 필요한 로그를 선택하도록 구성합니다. 예를 들어, 새로 추가되거나 업데이트된 모든 확장 로그를 선택하려면 (프로필 배달 로그):

   * **[!UICONTROL Properties]** 탭에서 대상 리소스를 **배달 로그** (Broadlogrcp) 로 변경합니다.

      ![](assets/export_logs_query_properties.png)

   * **[!UICONTROL Target]** 탭에서 2016 년 이후에 전송된 배달에 해당하는 모든 배달 로그를 검색할 조건을 설정합니다. For more information, refer to the [Editing queries](../../automating/using/editing-queries.md#creating-queries) section.

      ![](assets/export_logs_query_target.png)

   * **[!UICONTROL Processed data]** 탭에서 **[!UICONTROL Use a date field]****Lastmodified** 필드를 선택하고 선택합니다. 다음 워크플로우의 실행 시 마지막 실행 후에 수정되거나 만들어진 로그만 검색됩니다.

      ![](assets/export_logs_query_processeddata.png)

      워크플로우의 처음 실행 후 다음 실행에 사용할 마지막 실행 날짜를 이 탭에서 확인할 수 있습니다. 워크플로우가 실행될 때마다 자동으로 업데이트됩니다. 필요에 따라 새 값을 수동으로 입력하여 이 값을 무시할 수 있습니다.

1. Add an **[!UICONTROL Extract file]** activity that will export the queried data in a file:

   * **[!UICONTROL Extraction]** 탭에서 파일 이름을 지정합니다. 이 이름은 내보내기 날짜로 자동으로 완료되어 추출된 모든 파일이 고유한지 확인합니다.

      파일에서 내보낼 열을 선택합니다. 여기에는 배달 또는 프로필 정보와 같은 관련 리소스에서 오는 데이터를 선택할 수 있습니다. 최종 파일을 구성하려면 정렬을 적용할 수 있습니다. 예를 들어, 아래 예에서 보듯이 로그 날짜에 표시됩니다.

      ![](assets/export_logs_extractfile_extraction.png)

      >[!NOTE]
      >
      >로그 리소스의 고유 식별자 (기본 키) 는 내보낼 수 없습니다.

   * **[!UICONTROL File structure]** 탭에서 사용자의 요구 사항에 맞는 출력 파일의 형식을 정의합니다.

      Check the **[!UICONTROL Export labels instead of internal values of enumerations]** option in case you export enumeration values. 이 옵션을 사용하면 ID 대신 이해하기 쉬운 짧은 레이블을 검색할 수 있습니다.

1. **[!UICONTROL Transfer file]** 활동을 추가하고 새로 만든 파일을 Sftp 서버와 같이 액세스할 수 있는 다른 위치에 Adobe Campaign Server에서 전송하도록 구성합니다.

   * **[!UICONTROL General]** 탭에서 **[!UICONTROL File upload]** Adobe Campaign의 파일을 다른 서버로 전송하는 용도이므로 선택합니다.
   * **[!UICONTROL Protocol]** 탭에서 전송 매개 변수를 지정하고 사용할 [외부 계정을](../../administration/using/external-accounts.md#creating-an-external-account) 선택합니다.

1. **[!UICONTROL End]** 활동을 추가하여 제대로 끝났는지 확인하고 워크플로우를 저장합니다.

   ![](assets/export_logs_example_workflow.png)

이제 워크플로우를 실행하고 외부 서버에서 출력 파일을 검색할 수 있습니다.

**관련 항목:**

[워크플로우](../../automating/using/discovering-workflows.md)
