---
title: 프로필 검색
description: API를 사용하여 프로필을 검색하는 방법을 자세히 알아봅니다
feature: API
role: Data Engineer
level: Experienced
exl-id: 19679804-f728-49fa-b26e-8f31b67c29bf
source-git-commit: 64f24fb692754973331b4fb2f7b95e9a6f31cd0d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 4%

---

# API를 사용하여 프로필 검색 {#retrieving-profiles}

프로필 검색은 **GET** 요청.

그런 다음 필터, 순서 지정 및 페이지 매김을 사용하여 검색을 세분화할 수 있습니다. 자세한 내용은 [추가 작업](../../api/using/sorting.md) 섹션을 참조하십시오.

또한 Campaign Standard API를 사용하면 다음 필드 중 하나를 기반으로 프로필을 검색할 수 있습니다. 이메일, 이름, 성 또는 사용자 지정 필드. 이 작업에 대한 자세한 정보는 [이 섹션](#searching-field)을 참조하십시오.

<br/>

***샘플 요청***

* 모든 프로필을 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다.

   ```
   {
       "content": [
           {
               "PKey": "<PKEY>",
               "firstName": "John",
               "lastName":"Doe",
               "birthDate": "1980-10-24",
               ...
           },
           ...
   }
   ```

* 처음 10개의 이메일 값을 검색하기 위한 샘플 GET 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   요청에 대한 응답입니다. 다음 노드는 10개의 다음 이메일 값에 대한 액세스 권한을 제공하는 URL을 반환합니다.

   ```
   {
   "content": [
       "amy.dakota@mail.com",
       "kristen.smith@mail.com",
       "omalley@mail.com",
       "xander.harrys@mail.com",
       "jane.summer@mail.com",
       "gloria.boston@mail.com",
       "edward.snow@mail.com",
       "dorian.simons@mail.com",
       "peter.paolini@mail.com",
       "mingam+test08@adobe.com"
   ],
   "next": {
       "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
       lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
   }
   }
   ```

## 필드를 기반으로 프로필 검색 {#searching-field}

다음 **[!UICONTROL filterType]** 매개 변수를 사용하면 다음 필드 중 하나를 기반으로 프로필을 검색할 수 있습니다. 프로필 리소스를 확장할 때 고급 필터링에서 추가한 이메일, 이름, 성 또는 사용자 지정 필드.

>[!NOTE]
>
>검색은 대소문자를 구분하며 접두사에서만 수행됩니다. 예를 들어 성의 성을 사용하여 프로필을 찾을 수 없습니다.

***샘플 요청***

* 이름을 기반으로 프로필을 필터링하는 샘플 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John&filterType=firstName \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* 성을 기준으로 프로필을 필터링하는 샘플 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=Miller&filterType=lastName \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* 이메일을 기반으로 프로필을 필터링하는 샘플 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John%40gmail.com&filterType=email \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* &quot;취미&quot; 사용자 정의 필드를 기반으로 프로필을 필터링하기 위한 샘플 요청.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byText?cusHobby=Dancing&filterType=Hobby \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```
