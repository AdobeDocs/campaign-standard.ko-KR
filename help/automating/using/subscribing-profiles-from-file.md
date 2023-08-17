---
title: 파일에서 특정 서비스에 프로필 가입
description: 이 사용 사례에서는 프로필이 포함된 파일을 가져와 기존 서비스에 구독하는 방법을 보여줍니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: setOfService,workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 06ae4a5c-f112-4aac-b776-437ac35a8f02
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 53%

---

# 파일을 가져온 후 특정 서비스에 프로필 가입 {#subscribing-profiles-to-a-specific-service-after-importing-a-file}

이 예에서는 프로필이 포함된 파일을 가져와 기존 서비스에 구독하는 방법을 보여줍니다. 파일을 가져온 후에는 가져온 데이터를 프로필로 식별할 수 있도록 조정을 수행해야 합니다. 파일에 중복 항목을 포함하지 않는지 확인하기 위해 데이터 중복 제거 활동이 실행됩니다.

워크플로우는 다음과 같이 표시됩니다.

![](assets/subscription_activity_example1.png)

* A [파일 로드](../../automating/using/load-file.md) 활동은 프로필 파일을 로드하고 가져온 열의 구조를 정의합니다.

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

* A [조정](../../automating/using/reconciliation.md) 활동은 파일의 데이터를 Adobe Campaign 데이터베이스의 프로필 차원에 속하는 것으로 식별합니다. **[!UICONTROL Identification]** 탭만 구성됩니다. 프로필의 이메일 주소에 따라 파일 데이터를 식별합니다.

  ![](assets/subscription_activity_example3.png)

* A [중복 제거](../../automating/using/deduplication.md) 를 기반으로 함 **이메일** 임시 리소스의 필드(조정 결과)는 모든 중복을 식별합니다. 파일에서 가져온 데이터에 중복된 항목이 있으면 모든 데이터에 대한 서비스 구독이 실패합니다.

  ![](assets/subscription_activity_example5.png)

* A [구독 서비스](../../automating/using/subscription-services.md) 활동을 통해 프로필을 구독해야 하는 서비스, 구독 날짜에 해당하는 필드 및 구독 출처를 선택할 수 있습니다.

  ![](assets/subscription_activity_example4.png)
