---
title: 조정을 사용한 데이터 업데이트
description: 다음 예제에서는 새로운 고객을 포함하는 파일을 가져와 직접 대상자 프로필을 만드는 워크플로우를 보여줍니다.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 67%

---


# 조정을 사용한 데이터 업데이트 {#data-update-reconciliation}

다음 예제에서는 새로운 고객을 포함하는 파일을 가져와 직접 대상자 프로필을 만드는 워크플로우를 보여줍니다. 워크플로우는 다음 활동으로 구성됩니다.

![](assets/identification_example2.png)

* A [Load file](../../automating/using/load-file.md) activity, which loads and detects tshe data of the file to import. 가져온 파일에는 다음 데이터가 포함됩니다.

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

* A [Reconciliation](../../automating/using/reconciliation.md) activity, which links each column of the loaded file to a profile dimension column. 식별할 수 없는 파일 레코드(데이터 누락, 호환되지 않는 데이터 형식 등)는 최종 대상자 데이터의 무결성을 유지하기 위해 무시됩니다.

   ![](assets/identification_example1.png)

* A [Save audience](../../automating/using/save-audience.md) activity, which saves the audience of profiles.

   ![](assets/identification_example3.png)
