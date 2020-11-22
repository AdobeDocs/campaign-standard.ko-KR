---
solution: Campaign Standard
product: campaign
title: 가져온 파일에서 데이터 중복 제거
description: 이 예제에서는 데이터를 데이터베이스에 로드하기 전에 가져온 파일에서 데이터를 중복 제거하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 89%

---


# 가져온 파일에서 데이터 중복 제거 {#deduplicating-the-data-from-an-imported-file}

이 예제에서는 데이터를 데이터베이스에 로드하기 전에 가져온 파일에서 데이터를 중복 제거하는 방법을 보여줍니다. 이 절차는 데이터베이스에 로드되는 데이터의 품질을 향상시킵니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/deduplication_example2_workflow.png)

* A file that contains a list of profiles is imported using a [Load file](../../automating/using/load-file.md) activity. 이 예제에서 가져온 파일은 .csv 포맷이며 10개의 프로필이 포함되어 있습니다.

   ```
   lastname;firstname;dateofbirth;email
   Smith;Hayden;23/05/1989;hayden.smith@example.com
   Mars;Daniel;17/11/1987;dannymars@example.com
   Smith;Clara;08/02/1989;hayden.smith@example.com
   Durance;Allison;15/12/1978;allison.durance@example.com
   Lucassen;Jody;28/03/1988;jody.lucassen@example.com
   Binder;Tom;19/01/1982;tombinder@example.com
   Binder;Tommy;19/01/1915;tombinder@example.com
   Connor;Jade;10/10/1979;connor.jade@example.com
   Mack;Clarke;02/03/1985;clarke.mack@example.com
   Ross;Timothy;04/07/1986;timross@example.com
   ```

   이 파일은 샘플 파일로도 사용되어 열 포맷을 감지하고 정의할 수 있습니다. **[!UICONTROL Column definition]** 탭에서 가져온 파일의 각 열이 올바르게 구성되어 있는지 확인합니다.

   ![](assets/deduplication_example2_fileloading.png)

* 데이터 [중복 제거](../../automating/using/deduplication.md) 활동 중복 제거는 파일을 가져온 후 데이터베이스에 데이터를 삽입하기 전에 직접 수행됩니다. 그러므로 **[!UICONTROL Load file]** 활동의 **[!UICONTROL Temporary resource]**&#x200B;을(를) 기반으로 해야 합니다.

   이 예에서는 파일에 포함된 고유한 이메일 주소당 하나의 항목을 유지하려고 합니다. 따라서 임시 리소스의 **이메일** 열에 중복 식별이 수행됩니다. 그러나 파일에 두 개의 이메일 주소가 두 번 나타납니다. 따라서 두 줄은 중복으로 간주됩니다.

   ![](assets/deduplication_example2_dedup.png)

* An [Update data](../../automating/using/update-data.md) activity allows you to insert the data kept from the deduplication process into the database. 가져온 데이터가 프로필 차원에 속하는 것으로 식별되는 경우에만 데이터가 업데이트됩니다.

   여기서는 데이터베이스에 아직 존재하지 않는 프로필을 **[!UICONTROL Insert only]**&#x200B;합니다. 파일의 이메일 열과 **프로필** 차원의 이메일 필드를 조정 키로 사용하여 이를 수행합니다.

   ![](assets/deduplication_example2_writer1.png)

   **[!UICONTROL Fields to update]** 탭에서 데이터를 삽입할 파일의 열과 데이터베이스 필드 간의 매핑을 지정합니다.

   ![](assets/deduplication_example2_writer2.png)

그런 다음 워크플로우를 시작합니다. 중복 제거 프로세스에서 저장된 레코드는 데이터베이스의 프로필에 추가됩니다.
