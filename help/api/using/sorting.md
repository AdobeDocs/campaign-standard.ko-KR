---
solution: Campaign Standard
product: campaign
title: 정렬
description: 정렬 작업을 수행하는 방법에 대해 자세히 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 11%

---


# 정렬

정렬은 오름차순이나 내림차순으로 사용할 수 있습니다. 이렇게 하려면 **%20desc** 또는 **%20asc** 매개 변수를 요청에 사용하십시오.

필드를 정렬할 수 있는지 확인하려면 &quot;정렬 가능한&quot; 매개 변수를 리소스 메타데이터에 포함시킵니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/metadata-mechanism.md)을 참조하십시오.

<br/>

***샘플 요청***

* GET 요청 샘플을 선택하여 알파벳순으로 정렬된 데이터베이스에서 이메일을 검색합니다.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email/email?_order=email \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
   "content": [
       "adam@email.com",
       "allison.durance@example.com",
       "amy.dakota@mail.com",
       "andrea.johnson@mail.com",
       ...
   ]
   ...
   }
   ```

* 데이터베이스에서 내림차순으로 이메일을 검색하기 위한 샘플 GET 요청입니다.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email%20desc \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
   "content": [
       "tombinder@example.com",
       "tombinder@example.com",
       "timross@example.com",
       "john.smith@example.com",
       ...
   ]
   }
   ```
