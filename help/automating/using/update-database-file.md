---
solution: Campaign Standard
product: campaign
title: 외부 데이터로 데이터베이스 업데이트
description: 이 사용 사례에서는 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로파일을 추가하거나 업데이트하는 방법을 설명합니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: writer,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 33%

---


# 외부 데이터로 데이터베이스 업데이트 {#update-database-file}

다음 예는 **[!UICONTROL Load file]** 활동 다음에 오는 **[!UICONTROL Update data]** 활동의 구성을 보여줍니다. 이 워크플로우의 목적은 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 것입니다.

이 예에서 사용된 조정 키는 **이메일 주소**&#x200B;입니다. [Load file](../../automating/using/load-file.md) 활동에 로드된 파일은 다음 예제 데이터를 포함하는 **.txt** 형식 파일입니다.

```
lastname;firstname;email;birthdate
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

[데이터 업데이트](../../automating/using/update-data.md) 활동은 다음과 같이 구성됩니다.

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)
