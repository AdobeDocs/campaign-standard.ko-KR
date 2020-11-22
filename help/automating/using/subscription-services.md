---
solution: Campaign Standard
product: campaign
title: 구독 서비스
description: 구독 서비스 활동을 통해 프로필을 대량으로 가져와 서비스를 구독하거나 구독 취소할 수 있습니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: setOfService,workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 98%

---


# 구독 서비스 {#subscription-services}

## 설명 {#description}

![](assets/wf_subscription.png)

**[!UICONTROL Subscription Services]** 활동을 통해 프로필을 대량으로 가져와 서비스를 구독하거나 구독 취소할 수 있습니다.

>[!CAUTION]
>
>워크플로우의 컨텍스트에서 구독을 관리하는 경우 구독했거나 구독을 취소한 프로필은 서비스 속성에 정의된 다른 확인 이메일을 받지 않습니다.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Subscription Services]** 활동은 하나의 동작으로 여러 프로필을 서비스 구독 또는 구독 취소하도록 하는 유일한 Adobe Campaign 기능입니다.

타겟팅을 수행하거나 식별된 데이터가 있는 파일을 가져온 후에 이 활동을 사용할 수 있습니다.

전용 열을 통해 파일에 지정한 경우, 이 활동을 통해 작업(구독 또는 구독 취소)과 작업을 수행할 서비스를 선택할 수도 있습니다.

**관련 항목:**

* [사용 사례:파일에서 여러 구독 상태 업데이트](../../automating/using/updating-subscriptions-from-file.md)
* [사용 사례:파일에서 특정 서비스에 프로필 가입](../../automating/using/subscribing-profiles-from-file.md)

## 구성 {#configuration}

1. **[!UICONTROL Subscription Services]** 활동을 워크플로우로 끌어서 놓습니다.
1. 가져오기 후 쿼리 또는 조정과 같은 다른 타겟팅 활동 뒤에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 다음 옵션 중 하나를 사용하여 구독을 관리할 **[!UICONTROL Service]**&#x200B;을(를) 선택합니다.

   * **[!UICONTROL Select a specific service]**: 서비스를 수동으로 선택합니다.
   * **[!UICONTROL Select services from the inbound transition]**: 서비스가 인바운드 전환에서 지정됩니다. 예를 들어 각 행에 대해 관리할 서비스를 지정하는 파일을 가져올 수 있습니다. 이 옵션을 선택하는 경우, [이 예제](#example--updating-multiple-subscription-statuses-from-a-file)와 같이 데이터와 **서비스** 리소스 간에 미리 링크가 생성되었는지 확인해야 합니다.

      그런 다음 각 레코드에 대해 작업을 수행할 서비스가 동적으로 선택됩니다.

1. 다음 옵션 중 하나를 사용하여 실행할 **[!UICONTROL Operation type]**&#x200B;을(를) 선택합니다.

   * **[!UICONTROL Select a specific operation type]**: **[!UICONTROL Subscribe]** 또는 **[!UICONTROL Unsubscribe]** 프로필을 수동으로 선택합니다.
   * **[!UICONTROL Select an operation type from a path of inbound transition]**: 각 레코드에 대해 수행할 작업을 지정하는 인바운드 데이터의 열을 선택합니다.

      이 열에서 작업을 부울 또는 정수로 지정해야 합니다. 레코드 구독을 취소하려면 **0** 을 사용하고 구독하려면 **1** 을 사용합니다.

      가져온 파일에 포함된 값이 위의 요구 사항과 일치하지 않는 경우에도 **[!UICONTROL Load file]** 활동에서 사용할 수 있는 [값 재매핑](../../automating/using/load-file.md#column-format) 옵션을 사용할 수 있습니다.

1. 인바운드 데이터에 프로필이 서비스를 구독한 날짜에 해당하는 열이 포함된 경우 해당 열을 선택합니다. 비워 둘 수 있지만, 워크플로우를 실행할 때 구독 날짜가 설정되지 않습니다.
1. 구독의 출처를 정의합니다. **[!UICONTROL Set a constant as origin]** 옵션을 확인하여 인바운드 데이터의 필드 중 하나 또는 선택한 상수 값으로 설정할 수 있습니다. 비워 둘 수 있지만, 워크플로우를 실행할 때 출처가 설정되지 않습니다.
1. 필요한 경우 아웃바운드 전환을 생성할 수 있습니다. 이 전환에는 인바운드 활동의 데이터와 정확히 동일한 데이터가 포함됩니다.
1. 활동 구성을 확인하고 워크플로우를 저장합니다.

   이제 실행할 준비가 되었습니다. 실행되면 서비스에 구독했거나 구독을 취소한 프로필을 서비스 세부 정보에서 볼 수 있습니다.

## 예: 파일을 가져온 후 특정 서비스에 프로필 구독 {#example--subscribing-profiles-to-a-specific-service-after-importing-a-file}

이 예에서는 프로필이 포함된 파일을 가져와 기존 서비스에 구독하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 프로필로 식별할 수 있도록 조정을 수행해야 합니다. 파일에 중복 항목을 포함하지 않는지 확인하기 위해 데이터 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* **[!UICONTROL Load file]** 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다. 

   이 예제에서 로드된 파일은 .csv 형식으로 되어 있으며 다음 데이터를 포함합니다.

   ```
   lastname;firstname;email;birthdate;subdate
   jackman;megan;megan.jackman@testmail.com;07/08/1975;10/08/2017
   phillips;edward;phillips@testmail.com;09/03/1986;10/08/2017
   weaver;justin;justin_w@testmail.com;11/15/1990;10/08/2017
   martin;babeth;babeth_martin@testmail.net;11/25/1964;10/08/2017
   reese;richard;rreese@testmail.com;02/08/1987;11/08/2017
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989;11/08/2017
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992;11/08/2017
   grimes;daryl;daryl_890@testmail.com;12/06/1979;12/08/2017
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971;12/08/2017
   ```

   ![](assets/subscription_activity_example2.png)

* **[!UICONTROL Reconciliation]** 활동은 파일의 데이터를 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 것으로 식별합니다. **[!UICONTROL Identification]** 탭만 구성됩니다. 프로필의 이메일 주소에 따라 파일 데이터를 식별합니다.

   ![](assets/subscription_activity_example3.png)

* 임시 리소스의 **이메일** 필드(조정 결과)를 기반으로 한 **[!UICONTROL Deduplication]**&#x200B;은(는) 모든 중복을 식별합니다. 파일에서 가져온 데이터에 중복된 항목이 있으면 모든 데이터에 대한 서비스 구독이 실패합니다.

   ![](assets/subscription_activity_example5.png)

* **[!UICONTROL Subscription Services]** 활동을 통해 프로필을 구독해야 하는 서비스, 구독 날짜에 해당하는 필드 및 구독 출처를 선택할 수 있습니다.

   ![](assets/subscription_activity_example4.png)

## 예: 파일에서 여러 구독 상태 업데이트 {#example--updating-multiple-subscription-statuses-from-a-file}

이 예에서는 프로필이 포함된 파일을 가져오고 파일에 지정된 여러 서비스에 대한 구독을 업데이트하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 서비스 링크가 있는 프로필로 식별할 수 있도록 조정을 수행해야 합니다. 파일에 중복 항목을 포함하지 않는지 확인하기 위해 데이터 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* **[!UICONTROL Load file]** 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다. 

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

* **[!UICONTROL Reconciliation]** 활동은 파일의 데이터를 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 것으로 식별합니다. **[!UICONTROL Identification]** 탭을 통해 파일의 **이메일** 필드가 프로필 리소스의 **이메일** 필드와 일치됩니다.

   ![](assets/subscription_activity_example3.png)

   **[!UICONTROL Relations]** 탭에는 파일의 **서비스** 필드를 인식할 수 있도록 서비스 리소스와 함께 링크가 만들어집니다. 이 예에서 값은 서비스 리소스의 **이름** 필드와 일치합니다.

   ![](assets/subscription_example_service_relation.png)

* 임시 리소스의 **이메일** 필드(조정 결과)를 기반으로 한 **[!UICONTROL Deduplication]**&#x200B;은(는) 중복을 식별합니다. 중복되는 경우 모든 데이터에 대한 서비스 구독이 실패하므로 중복을 제거하는 것이 중요합니다.

   ![](assets/subscription_activity_example5.png)

* **[!UICONTROL Reconciliation]**&#x200B;은(는) **[!UICONTROL Subscription Services]** 활동에서 생성된 링크를 통하여 업데이트할 서비스를 전환에서 나온 것으로 식별합니다.

   **[!UICONTROL Operation type]**&#x200B;은(는) 파일의 **작업** 필드에서 나온 것으로 식별됩니다. 여기에서는 부울 또는 정수 필드만 선택할 수 있습니다. 수행할 작업이 포함된 파일의 열이 목록에 표시되지 않는 경우 이 예제의 앞부분에서 설명한 대로 **[!UICONTROL Load file]** 활동에서 열 형식을 올바르게 설정했는지 확인하십시오.

   ![](assets/subscription_activity_example_from_file.png)

