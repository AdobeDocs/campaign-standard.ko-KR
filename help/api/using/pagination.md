---
title: 쪽 매기기
description: 페이지 매김 작업을 수행하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 59405df2bbb51d7cd944a0630b2b82db864f3920

---


# 쪽 매기기

기본적으로 25개의 리소스가 목록에 로드됩니다.

_lineCount **** 매개 변수를 사용하면 응답에 나열된 리소스 수를 제한할 수 있습니다.  그런 다음 **다음** 노드를 사용하여 다음 결과를 표시할 수 있습니다.

>[!NOTE]
>
>항상 **다음** 노드에서 반환된 URL 값을 사용하여 페이지 매김 요청을 수행합니다.
>
>The **_lineStart** request is calculated and must be used within the URL returned in the **next** node.

<br/>

***샘플 요청&#x200B;***

프로필 리소스의 레코드 1개를 표시하는 샘플 GET 요청입니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

요청에 대한 응답으로, **다음** 노드가 페이지 매김을 수행합니다.

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

기본적으로 많은 양의 데이터를 갖는 테이블과 상호 작용할 때 **다음** 노드를 사용할 수 없습니다. 페이지 매김을 수행하려면 **_forcePagination=true** 매개 변수를 호출 URL에 추가해야 합니다.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

>[!NOTE]
>
>테이블이 큰 것으로 간주되는 위의 레코드 수는 Campaign Standard XtkBigTableThreshold **옵션에서 정의됩니다** . 기본값은 100,000개의 레코드입니다.
