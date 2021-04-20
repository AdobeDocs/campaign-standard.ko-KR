---
solution: Campaign Standard
product: campaign
title: '"3단계: 확장 확인"'
description: Rest API를 사용하여 확장 필드에 액세스하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
feature: Data Model
role: Developer
level: Experienced
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

---


# 3단계: 확장 확인{#step-verify-the-extension}

1. 프로필 및 서비스 확장 API의 메타데이터에 대한 GET 작업을 만들어 프로필 사용자 지정 리소스에 추가된 필드를 사용할 수 있는지 확인합니다.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. 반환:

   ![](assets/extendpandsapiview.png)

   이 필드는 이제 추가 개발과 통합으로 사용할 수 있습니다.

