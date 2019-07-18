---
title: 구독 서비스
seo-title: 구독 서비스
description: 구독 서비스
seo-description: 구독 서비스 활동을 통해 일괄적으로 프로파일을 취하여 서비스에 구독하거나 서비스에서 가입을 해지할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 56637024-15 AB -4145-9 C 48-3 FBD 27 AB 8 AF 8
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 데이터 관리 활동
discoiquuid: 74 A 6 DF 0 E-FD 85-4404-A 42 C -9 A 7406512717
context-tags: Setofservice, workflow, main
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Subscription Services{#subscription-services}

## Description {#description}

![](assets/wf_subscription.png)

**[!UICONTROL Subscription Services]** 활동을 통해 일괄적으로 프로필을 가져와 서비스에 구독하거나 서비스에서 가입을 해지할 수 있습니다.

>[!CAUTION]
>
>워크플로우 컨텍스트에서 구독이 관리되는 경우 구독되거나 가입 취소된 프로필은 서비스 속성에 정의된 서로 다른 확인 이메일을 받지 않습니다.

## Context of use {#context-of-use}

**[!UICONTROL Subscription Services]** 활동은 한 번의 클릭으로 서비스를 구독하거나 가입을 해지할 수 있는 유일한 Adobe Campaign 기능입니다.

타깃팅을 수행한 후 또는 식별된 데이터로 파일을 가져온 후 이 활동을 사용할 수 있습니다.

전용 열을 통해 파일에 지정된 경우 이 활동을 사용하면 작업 (가입 또는 가입 해지) 와 작업을 수행할 서비스를 선택할 수도 있습니다.

## Configuration {#configuration}

1. **[!UICONTROL Subscription Services]** 워크플로우를 워크플로우로 드래그하여 놓습니다.
1. 가져오기 이후의 쿼리 또는 조정 등의 다른 타깃팅 활동 뒤에 연결하십시오.
1. Select the activity, then open it using the ![](assets/edit_darkgrey-24px.png) button from the quick actions that appear.
1. Select the **[!UICONTROL Service]** for which you would like to manage the subscriptions using one of the following options:

   * **[!UICONTROL Select a specific service]**: 서비스를 수동으로 선택합니다.
   * **[!UICONTROL Select services from the inbound transition]**: 서비스가 인바운드 전환에 지정되어 있습니다. 예를 들어, 각 라인에 대해 관리할 서비스를 지정하는 파일을 가져올 수 있습니다. If you choose this option, make sure a link has been created beforehand between the data and the **Service** resource, as shown in [this example](../../automating/using/subscription-services.md#example--updating-multiple-subscription-statuses-from-a-file).

      작업을 수행할 서비스가 각 레코드에 대해 동적으로 선택됩니다.

1. Select the **[!UICONTROL Operation type]** to execute using one of the following options:

   * **[!UICONTROL Select a specific operation type]**: 원하는 경우 수동으로 또는 **[!UICONTROL Subscribe]****[!UICONTROL Unsubscribe]** 프로필을 선택합니다.
   * **[!UICONTROL Select an operation type from a path of inbound transition]**: 각 레코드에 대해 수행할 작업을 지정하는 인바운드 데이터의 열을 선택합니다.

      이 열에서 작업은 부울 또는 정수여야 합니다. **0** 를 사용하여 레코드 가입을 취소하고 **1** 를 사용하여 구독을 구독 취소합니다.

      In case the values contained in an imported file do not match the above requirements, you can still use the [Remapping of values](../../automating/using/load-file.md#column-format) option available in the **[!UICONTROL Load file]** activity

1. 인바운드 데이터에 프로필의 구독 날짜에 해당하는 열이 포함된 경우 해당 데이터를 선택합니다. 워크플로우를 실행할 때 설정된 가입 날짜는 비워 둘 수 없습니다.
1. 구독 원본을 정의합니다. You can set it to one of the fields of the inbound data or to a constant value of your choice by checking the **[!UICONTROL Set a constant as origin]** option. 이 작업은 비워 둘 수 있지만 워크플로우를 실행할 때에는 원본이 설정되지 않습니다.
1. 필요한 경우 아웃바운드 전환을 생성할 수 있습니다. 이 전환에는 인바운드 활동에서와 동일한 데이터가 포함되어 있습니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.

   이제 실행될 준비가 되었습니다. 실행된 후에는 서비스의 세부 정보에서 서비스에 가입했거나 가입을 해지한 프로필을 볼 수 있습니다.

## Example: Subscribing profiles to a specific service after importing a file {#example--subscribing-profiles-to-a-specific-service-after-importing-a-file}

이 예에서는 프로파일이 포함된 파일을 가져오고 기존 서비스에 가입하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 프로필로 식별할 수 있도록 조정 작업을 수행해야 합니다. 파일에 중복이 없도록 하기 위해 데이터에서 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* **[!UICONTROL Load file]** 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다.

   이 예에서 로드되는 파일은. csv 형식이며 다음 데이터를 포함합니다.

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

* **[!UICONTROL Reconciliation]** 활동은 파일에서 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 데이터를 식별합니다. **[!UICONTROL Identification]** 탭만 구성됩니다. 프로필의 이메일 주소에 따라 파일 데이터를 식별합니다.

   ![](assets/subscription_activity_example3.png)

* A **[!UICONTROL Deduplication]** based on the **email** field of the temporary resource (resulting from the reconciliation) identifies any duplicates. 파일에서 가져온 데이터에 중복 항목이 포함되어 있으면 모든 데이터에 대한 서비스 구독이 실패합니다.

   ![](assets/subscription_activity_example5.png)

* **[!UICONTROL Subscription Services]** 활동을 사용하면 프로필을 구독해야 하는 서비스, 구독 날짜에 해당하는 필드, 구독 원본 등을 선택할 수 있습니다.

   ![](assets/subscription_activity_example4.png)

## Example: Updating multiple subscription statuses from a file {#example--updating-multiple-subscription-statuses-from-a-file}

이 예에서는 프로파일이 포함된 파일을 가져오고 파일에 지정된 여러 서비스에 대한 해당 가입을 업데이트하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 서비스에 대한 링크가 있는 프로필로 식별할 수 있도록 조정 작업을 수행해야 합니다. 파일에 중복이 없도록 하기 위해 데이터에서 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* **[!UICONTROL Load file]** 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다.

   이 예에서 로드되는 파일은. csv 형식이며 다음 데이터를 포함합니다.

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

   지금까지 살펴본 것처럼 이 작업은 파일에 "sub" 또는 "unsub" 로 지정되어 있습니다. The system expects a **Boolean** or **Integer** value to recognize the operation to perform: "0" to unsubscribe and "1" to subscribe. 이 요구 사항을 충족하기 위해 값 재매핑이 "작업" 열의 세부 사항에서 수행됩니다.

   ![](assets/subscription_example_remapping.png)

   파일에서 이미 "0" 및 "1" 를 사용하여 작업을 식별하는 경우 해당 값을 다시 매핑할 필요가 없습니다. Only make sure that the column is processed as a **Boolean** or **Integer** in the **[!UICONTROL Column definition]** tab.

* **[!UICONTROL Reconciliation]** 활동은 파일에서 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 데이터를 식별합니다. **[!UICONTROL Identification]** 탭을 통해 파일의 **이메일** 필드가 프로필 리소스의 **이메일** 필드와 일치합니다.

   ![](assets/subscription_activity_example3.png)

   **[!UICONTROL Relations]** 탭에서 서비스 필드를 사용하여 파일의 **서비스** 필드를 인식할 수 있도록 링크가 만들어집니다. In this example, the values match the **name** field of the service resource.

   ![](assets/subscription_example_service_relation.png)

* A **[!UICONTROL Deduplication]** based on the **email** field of the temporary resource (resulting from the reconciliation) identifies duplicates. 중복이 발생하는 경우 모든 데이터에 대한 서비스 구독이 실패하므로 중복을 제거해야 합니다.

   ![](assets/subscription_activity_example5.png)

* A **[!UICONTROL Subscription Services]** identifies the services to update as coming from the transition, through the link created in the **[!UICONTROL Reconciliation]** activity.

   The **[!UICONTROL Operation type]** is identified as coming from the **operation** field of the file. 여기에서 부울 또는 정수 필드만 선택할 수 있습니다. If the column of your file that contains the operation to perform does not appear in the list, make sure that you have correctly set your column format in the **[!UICONTROL Load file]** activity, as explained earlier in this example.

   ![](assets/subscription_activity_example_from_file.png)

