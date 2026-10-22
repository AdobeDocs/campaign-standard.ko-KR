---
title: '3단계: 확장 확인'
description: Rest API를 사용하여 확장 필드에 액세스하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: use-case-extending-the-api
feature: Data Model
role: Developer
level: Experienced
exl-id: 34cb416c-ee3d-4b7c-a75b-640432db320d
TQID: 'https://experienceleague.adobe.com/XadrenC5de4Xh6MSCUiQUc-qXaTKr-xpG-7znnlWeeQ'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: d5ef99fa-df0c-4153-bf94-105ad0724167
    internal-label: Integrations
  - id: a658c786-869b-4194-a780-2594d663adda
    internal-label: Data management
subfeature_v2:
  - id: a1681cd8-6b2e-4955-9113-33b5f7a22b8c
    internal-label: Data model architecture
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 16%
---
# 3단계: 확장 확인{#step-verify-the-extension}

1. Profiles &amp; Services 확장 API의 메타데이터에 대해 GET 작업을 수행하여 Profiles 사용자 지정 리소스에 추가된 필드를 이제 사용할 수 있는지 확인합니다.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. 반환:

   ![](assets/extendpandsapiview.png)

   이제 이 필드를 추가 개발 및 통합에 사용할 수 있습니다.
