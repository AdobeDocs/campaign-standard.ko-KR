---
title: '"3단계: 확장 확인"'
description: Rest API를 사용하여 확장 필드에 액세스하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
feature: Data Model
role: Developer
level: Experienced
exl-id: 34cb416c-ee3d-4b7c-a75b-640432db320d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 13%

---

# 3단계: 확장 확인{#step-verify-the-extension}

1. 프로필 및 서비스 확장 API의 메타데이터에 대한 GET 작업을 수행하여 프로필 사용자 지정 리소스에 추가된 필드를 이제 사용할 수 있는지 확인합니다.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. 반환:

   ![](assets/extendpandsapiview.png)

   이제 추가 개발 및 통합에 필드를 사용할 수 있습니다.
