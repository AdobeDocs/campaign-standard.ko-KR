---
title: 외부 데이터로 데이터베이스 업데이트
description: 이 사용 사례에서는 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 방법을 설명합니다.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: writer,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 2df7fbed-b979-4706-bd56-83f712cc3070
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 33%

---

# 외부 데이터로 데이터베이스 업데이트 {#update-database-file}

다음 예제에서는 **[!UICONTROL Load file]** 활동 다음에 나오는 **[!UICONTROL Update data]** 활동의 구성을 보여줍니다. 이 워크플로우의 목적은 파일에서 복구한 데이터로 Adobe Campaign 데이터베이스에 프로필을 추가하거나 업데이트하는 것입니다.

이 예제에서 사용되는 조정 키는 **전자 메일 주소**&#x200B;입니다. [파일 로드](../../automating/using/load-file.md) 활동에 로드된 파일은 다음 예제 데이터가 포함된 **.txt** 형식 파일입니다.

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
