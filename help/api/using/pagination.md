---
solution: Campaign Standard
product: campaign
title: 쪽 매기기
description: 페이지 매김 작업을 수행하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 쪽 매기기

기본적으로 25개의 리소스가 목록에 로드됩니다.

**_lineCount** 매개 변수를 사용하여 응답에 나열된 리소스 수를 제한할 수 있습니다.  그런 다음 **next** 노드를 사용하여 다음 결과를 표시할 수 있습니다.

>[!NOTE]
>
>페이지 매김 요청을 수행하려면 항상 **next** 노드에서 반환되는 URL 값을 사용하십시오.
>
>**_lineStart** 요청은 계산되며 **next** 노드에서 반환되는 URL 내에 항상 사용해야 합니다.

<br/>

***샘플 요청***

프로필 리소스의 레코드 1개를 표시하는 샘플 GET 요청입니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

요청에 대한 응답으로, 페이지 매김을 수행할 **next** 노드가 있습니다.

```
{
    "content": [
        {
            "PKey": "<PKEY>",
            "firstName": "John",
            "lastName":"Doe",
            "birthDate": "1980-10-24",
            ...
        }
    ],
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
        lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
    }
    ...
}
```

기본적으로 많은 양의 데이터로 테이블과 상호 작용할 때는 **next** 노드를 사용할 수 없습니다. 페이지 매김을 수행하려면 호출 URL에 **_forcePagination=true** 매개 변수를 추가해야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

>[!NOTE]
>
>테이블을 큼으로 간주하는 위의 레코드 수가 Campaign Standard **XtkBigTableThreshold** 옵션에 정의되어 있습니다. 기본값은 100,000개의 레코드입니다.
