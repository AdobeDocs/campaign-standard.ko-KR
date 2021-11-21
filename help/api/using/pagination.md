---
title: 쪽 매기기
description: 페이지 매김 작업을 수행하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: d6ebce3c-1e84-4b3b-a68d-90df4680af64
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# 쪽 매기기

기본적으로 25개의 리소스가 목록에 로드됩니다.

다음 **_lineCount** 매개 변수를 사용하면 응답에 나열된 리소스 수를 제한할 수 있습니다.  그런 다음 **다음** 노드 아래의 다음 결과를 표시합니다.

>[!NOTE]
>
>항상 **다음** 노드 아래의 페이지 매김 요청을 수행합니다.
>
>다음 **_lineStart** 요청은 계산되며, 항상 **다음** 노드 아래에 있어야 합니다.

<br/>

***샘플 요청***

프로필 리소스의 1개 레코드를 표시하는 샘플 GET 요청.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

요청에 대한 응답과 **다음** 노드 아래의 페이지 매기기를 수행합니다.

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

기본적으로 **다음** 많은 양의 데이터를 테이블에 상호 작용할 때 노드를 사용할 수 없습니다. 페이지 매김을 수행하려면 다음을 추가해야 합니다 **_forcePagination=true** 매개 변수를 사용하십시오.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

>[!NOTE]
>
>Campaign Standard에서 테이블이 큰 것으로 간주되는 위의 레코드 수입니다 **XtkBigTableThreshold** 선택 사항입니다. 기본값은 100,000개의 레코드입니다.
