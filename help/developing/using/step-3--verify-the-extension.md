---
title: '"3단계: 확장 확인"'
description: Rest API를 사용하여 확장 필드에 액세스하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 35ba89a5-a354-466f-91a0-50de111a2e00
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 21bad242-5921-445c-8df9-3d57dbe35197
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 13%

---


# 3단계: 확장 확인{#step-verify-the-extension}

1. 프로필 및 서비스 확장 API의 메타데이터에 대한 GET 작업을 만들어 프로필 사용자 지정 리소스에 추가된 필드를 사용할 수 있는지 확인합니다.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. 반환:

   ![](assets/extendpandsapiview.png)

   이 필드는 이제 추가 개발과 통합으로 사용할 수 있습니다.

