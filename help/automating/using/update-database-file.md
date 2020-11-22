---
solution: Campaign Standard
product: campaign
title: 외부 데이터로 데이터베이스 업데이트
description: 이 사용 사례에서는 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 방법을 설명합니다.
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

The following example shows the configuration of an **[!UICONTROL Update data]** activity following a **[!UICONTROL Load file]** activity. 이 워크플로우의 목적은 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 것입니다.

이 예에서 사용된 조정 키는 **이메일 주소입니다**. 파일 [로드](../../automating/using/load-file.md) 작업으로 로드되는 파일은 다음 예제 데이터가 포함된 **.txt** 형식 파일입니다.

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

The [Update data](../../automating/using/update-data.md) activity is configured as follows:

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)
