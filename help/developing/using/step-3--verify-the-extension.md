---
title: '"3단계: 확장 확인"'
description: Rest API를 사용하여 확장 필드에 액세스하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 35ba89a5-a354-46 파섹
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 개발
content-type: reference
topic-tags: use-case—extending-the-api
discoiquuid: 21bad242-5921-445c-8df9-3d57dbe35197
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 3단계: 확장 확인{#step-verify-the-extension}

1. 프로필 및 서비스 확장 API의 메타데이터에 대한 GET 작업을 수행하여 프로필 사용자 지정 리소스에 추가된 필드를 이제 사용할 수 있는지 확인합니다.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. 반환:

   ![](assets/extendpandsapiview.png)

   이제 추가 개발 및 통합을 위해 필드를 사용할 수 있습니다.

