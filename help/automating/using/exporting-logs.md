---
title: 로그 내보내기
description: 배달 또는 구독과 관련이 있는지 여부와 상관없이 로그 데이터를 간단한 워크플로우를 통해 내보낼 수 있습니다.
page-status-flag: never-activated
uuid: 954e919c-0a33-47c3-9a3c-63c7a2a4edc4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: ca8a95d8-523f-4085-a2fc-e1d8262cfbae
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# 로그 내보내기{#exporting-logs}

배달 또는 구독과 관련이 있는지 여부와 상관없이 로그 데이터를 간단한 워크플로우를 통해 내보낼 수 있습니다. 이를 통해 자체 보고 또는 BI 도구에서 캠페인 결과를 분석할 수 있습니다.

워크플로우가 실행될 때마다 새로운 로그만 **[!UICONTROL Incremental query]** 검색하는 것과 출력 열을 정의하는 간단한 **[!UICONTROL Extract file]** 활동을 사용하면 필요한 모든 데이터와 포맷의 파일을 가져올 수 있습니다. 그런 다음 **[!UICONTROL Transfer file]** 활동을 사용하여 최종 파일을 검색합니다. 각 워크플로우 실행은 한 프로그램에 의해 계획됩니다 **[!UICONTROL Scheduler]**.

내보내기 로그 작업은 표준 사용자가 수행할 수 있습니다. 다음과 같은 개인 리소스 profiles의 broadlogs, tracking logs, exclusion logs subscription logs and subscription history logs on **** can only manage by functional administrator.

1. 이 섹션에 자세히 설명된 대로 새 워크플로우 [를 만듭니다](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. 활동을 추가하고 필요에 따라 설정합니다. **[!UICONTROL Scheduler]** 다음은 월별 실행의 예입니다.

   ![](assets/export_logs_scheduler.png)

1. 필요한 로그를 선택하도록 **[!UICONTROL Incremental query]** 활동을 추가하고 구성합니다. 예를 들어, 새 또는 업데이트된 브로드로그(프로필 배달 로그)를 모두 선택하려면 다음을 수행합니다.

   * 탭에서 대상 리소스를 **[!UICONTROL Properties]** 배달 로그 **** (broadLogRcp)로 변경합니다.

      ![](assets/export_logs_query_properties.png)

   * 탭에서 **[!UICONTROL Target]** 조건을 설정하여 2016년 또는 그 이후에 전송된 게재에 해당하는 모든 배달 로그를 검색합니다. 자세한 내용은 쿼리 [편집 섹션을](../../automating/using/editing-queries.md#creating-queries) 참조하십시오.

      ![](assets/export_logs_query_target.png)

   * 탭에서 **[!UICONTROL Processed data]** 마지막 수정 **[!UICONTROL Use a date field]** 필드 **를** 선택하고 워크플로우의 다음 실행에서는 마지막 실행 후에 수정되거나 생성될 로그만 검색됩니다.

      ![](assets/export_logs_query_processeddata.png)

      워크플로우가 처음 실행된 후 다음 실행에 사용될 마지막 실행 날짜를 이 탭에서 확인할 수 있습니다. 워크플로우가 실행될 때마다 자동으로 업데이트됩니다. 여전히 필요에 맞게 새 값을 직접 입력하여 이 값을 무시할 수 있습니다.

1. 쿼리된 데이터를 파일로 내보낼 **[!UICONTROL Extract file]** 활동을 추가합니다.

   * 탭에서 **[!UICONTROL Extraction]** 파일 이름을 지정합니다.

      이 **[!UICONTROL Add date and time to the file name]** 옵션을 선택하면 추출된 모든 파일이 고유하도록 내보내기 날짜와 함께 이 이름이 자동으로 완성됩니다. 파일에서 내보낼 열을 선택합니다. 배달 또는 프로필 정보와 같은 관련 리소스에서 오는 데이터를 선택할 수 있습니다.

      >[!NOTE]
      >
      >각 로그에 대한 고유 식별자를 내보내려면 요소를 **[!UICONTROL Delivery log ID]** 선택합니다.

      최종 파일을 구성하려면 정렬을 적용할 수 있습니다. 예를 들어 아래 예와 같이 로그 날짜에 표시됩니다.

      ![](assets/export_logs_extractfile_extraction.png)

   * 탭에서 **[!UICONTROL File structure]** 필요에 맞게 출력 파일의 형식을 정의합니다.

      열거형 값을 내보낼 **[!UICONTROL Export labels instead of internal values of enumerations]** 경우 옵션을 선택합니다. 이 옵션을 사용하면 ID 대신 이해하기 쉬운 짧은 레이블을 검색할 수 있습니다.

1. 활동을 추가하고 새로 만든 파일을 Adobe Campaign 서버에서 액세스할 수 있는 다른 위치(예: SFTP 서버)로 전송하도록 구성합니다. **[!UICONTROL Transfer file]**

   * Adobe Campaign **[!UICONTROL General]** **[!UICONTROL File upload]** 에서 다른 서버로 파일을 전송하는 용도로 탭에서 선택합니다.
   * 탭에서 전송 매개 변수를 지정하고 사용할 **[!UICONTROL Protocol]** 외부 계정 [](../../administration/using/external-accounts.md#creating-an-external-account) 을 선택합니다.

1. 활동을 추가하여 **[!UICONTROL End]** 워크플로우가 올바르게 종료되고 저장되도록 합니다.

   ![](assets/export_logs_example_workflow.png)

이제 워크플로우를 실행하고 외부 서버에서 출력 파일을 검색할 수 있습니다.

**관련 항목:**

[워크플로우](../../automating/using/get-started-workflows.md)
