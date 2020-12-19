---
solution: Campaign Standard
product: campaign
title: 파일에서 여러 구독 상태 업데이트
description: 이 사용 사례는 프로필이 포함된 파일을 가져오고 파일에 지정된 여러 서비스에 대한 해당 구독을 업데이트하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: setOfService,workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 76%

---


# 파일에서 여러 구독 상태 업데이트 {#updating-multiple-subscription-statuses-from-a-file}

이 예에서는 프로필이 포함된 파일을 가져오고 파일에 지정된 여러 서비스에 대한 구독을 업데이트하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 서비스 링크가 있는 프로필로 식별할 수 있도록 조정을 수행해야 합니다. 파일에 중복 항목을 포함하지 않는지 확인하기 위해 데이터 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* [Load file](../../automating/using/load-file.md) 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다.

   이 예제에서 로드된 파일은 .csv 형식으로 되어 있으며 다음 데이터를 포함합니다.

   ```
   lastname;firstname;email;birthdate;service;operation
   jackman;megan;megan.jackman@testmail.com;07/08/1975;SVC2;sub
   phillips;edward;phillips@testmail.com;09/03/1986;SVC3;unsub
   weaver;justin;justin_w@testmail.com;11/15/1990;SVC3;sub
   martin;babeth;babeth_martin@testmail.net;11/25/1964;SVC3;unsub
   reese;richard;rreese@testmail.com;02/08/1987;SVC3;sub
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989;SVC3;sub
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992;SVC4;sub
   grimes;daryl;daryl_890@testmail.com;12/06/1979;SVC3;unsub
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971;SVC2;sub
   ```

   ![](assets/subscription_example_load_file.png)

   아시다시피, 작업은 파일에 &quot;구독&quot; 또는 &quot;구독 취소&quot;로 지정되어 있습니다. 시스템은 **부울** 또는 **정수** 값으로 수행할 작업을 인식합니다. &quot;0&quot;은 구독을 취소하고, &quot;1&quot;은 구독합니다. 이 요구 사항과 일치하도록 &quot;작업&quot; 열의 세부 사항에서 값 재매핑이 수행됩니다.

   ![](assets/subscription_example_remapping.png)

   파일이 이미 &quot;0&quot; 및 &quot;1&quot;을 사용하여 작업을 식별하는 경우 해당 값을 다시 매핑할 필요가 없습니다. **[!UICONTROL Column definition]** 탭에서 열이 **부울** 또는 **정수**&#x200B;로 처리되었는지 확인하기만 하면 됩니다.

* [조정](../../automating/using/reconciliation.md) 활동은 파일의 데이터를 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 것으로 식별합니다. **[!UICONTROL Identification]** 탭을 통해 파일의 **이메일** 필드가 프로필 리소스의 **이메일** 필드와 일치됩니다.

   ![](assets/subscription_activity_example3.png)

   **[!UICONTROL Relations]** 탭에는 파일의 **서비스** 필드를 인식할 수 있도록 서비스 리소스와 함께 링크가 만들어집니다. 이 예에서 값은 서비스 리소스의 **이름** 필드와 일치합니다.

   ![](assets/subscription_example_service_relation.png)

* 조정을 통해 발생한 임시 리소스의 **이메일** 필드를 기반으로 한 [중복 제거](../../automating/using/deduplication.md)는 중복을 식별합니다. 중복되는 경우 모든 데이터에 대한 서비스 구독이 실패하므로 중복을 제거하는 것이 중요합니다.

   ![](assets/subscription_activity_example5.png)

* [구독 서비스](../../automating/using/subscription-services.md) 활동은 **[!UICONTROL Reconciliation]** 활동에 생성된 링크를 통해 전환에서 온 것으로 업데이트할 서비스를 식별합니다.

   **[!UICONTROL Operation type]**&#x200B;은(는) 파일의 **작업** 필드에서 나온 것으로 식별됩니다. 여기에서는 부울 또는 정수 필드만 선택할 수 있습니다. 수행할 작업이 포함된 파일의 열이 목록에 표시되지 않는 경우 이 예제의 앞부분에서 설명한 대로 **[!UICONTROL Load file]** 활동에서 열 형식을 올바르게 설정했는지 확인하십시오.

   ![](assets/subscription_activity_example_from_file.png)
