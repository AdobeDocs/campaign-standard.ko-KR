---
title: 외부 데이터로 데이터베이스 업데이트
description: 이 사용 사례에서는 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가 또는 업데이트하는 방법을 설명합니다.
page-status-flag: never-activated
uuid: 1dc55db5-affd-4688-b673-adfb8c1338b5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 4db83c95-4b75-4a16-8dbf-bd8940431fa9
context-tags: writer,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# 외부 데이터로 데이터베이스 업데이트 {#update-database-file}

다음 예제는 활동 **[!UICONTROL Update data]** 후의 활동 구성을 **[!UICONTROL Load file]** 보여줍니다. 이 워크플로우의 목적은 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로파일을 추가하거나 업데이트하는 것입니다.

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

데이터 [업데이트](../../automating/using/update-data.md) 활동은 다음과 같이 구성됩니다.

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)
