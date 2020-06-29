---
title: 조정을 사용한 데이터 업데이트
description: 다음 예에서는 새 클라이언트가 들어 있는 가져온 파일에서 직접 프로필 대상자를 만드는 워크플로우를 보여 줍니다.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 175709a41607bb9d64da7fac77dd749fa84f7360
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 조정을 사용한 데이터 업데이트 {#data-update-reconciliation}

다음 예에서는 새 클라이언트가 들어 있는 가져온 파일에서 직접 프로필 대상자를 만드는 워크플로우를 보여 줍니다. 다음 활동으로 구성됩니다.

![](assets/identification_example2.png)

* 가져올 파일의 데이터를 로드하고 검색하는 [파일](../../automating/using/load-file.md) 로드 활동. 가져온 파일에는 다음 데이터가 포함됩니다.

   ```
   lastname;firstname;email;dateofbirth
   jackman;megan;megan.jackman@testmail.com;07/08/1975
   phillips;edward;phillips@testmail.com;09/03/1986
   weaver;justin;justin_w@testmail.com;11/15/1990
   martin;babeth;babeth_martin@testmail.net;11/25/1964
   reese;richard;rreese@testmail.com;02/08/1987
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
   grimes;daryl;daryl_890@testmail.com;12/06/1979
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
   ```

* 로드된 파일의 각 열을 프로필 [차원](../../automating/using/reconciliation.md) 열에 연결하는 조정 활동입니다. 식별할 수 없는 파일 레코드(데이터 누락, 호환되지 않는 데이터 유형 등) 최종 대상 데이터의 무결성을 유지하기 위해 무시됩니다.

   ![](assets/identification_example1.png)

* 프로필 [대상을 저장하는 대상](../../automating/using/save-audience.md) 저장 활동입니다.

   ![](assets/identification_example3.png)
