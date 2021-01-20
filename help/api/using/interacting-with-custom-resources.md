---
solution: Campaign Standard
product: campaign
title: 사용자 정의 리소스
description: API를 사용한 사용자 정의 리소스 관리에 대한 자세한 내용/
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 9eca72e744524cf201d998abd9acf718fdaca0f8
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 3%

---


# 사용자 정의 리소스와 상호 작용 {#interacting-with-custom-resources}

**/customResources** 끝점을 사용하면 REST에 캠페인 사용자 지정 리소스를 표시할 수 있습니다. 이 API를 기반으로 사용자 지정 엔터티 및 외부 끝점 간의 통합을 사용할 수 있습니다.

/customResources 끝점은 /profileAndServices 끝점과 정확하게 동일한 비헤이비어를 갖습니다.

이 API 내에 표시되는 사용자 지정 리소스는 다음과 같습니다.

* 프로파일 엔티티에 연결된 모든 엔티티
* 프로필 엔티티의 자식에 연결된 모든 엔티티
* 프로필에 연결되어 있지 않은 모든 개체, 이러한 개체, 해당 자식 및 손자손녀

>[!NOTE]
>/profileAndServicesExt 아래에 있는 사용자 지정 리소스는 /customResources API에 노출되지 않습니다.

다음은 사용자 지정 리소스에서 메타데이터를 검색하는 예입니다.

```
GET /customResources/resourceType/<customResourceName>
```

생성, 업데이트 또는 삭제를 수행하려면 GET, POST, PATCH, DELETE이 사용됩니다.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>개인 정보 API 끝점 및 워크플로(/privacy/privacyTool)가 프로필 엔터티에 연결되지 않은 사용자 지정 리소스를 관리하지 않습니다.
>이러한 사용자 정의 리소스에 대한 PII를 관리하고 정리할 책임이 있습니다. 개인 정보 보호 도구에 대한 자세한 내용을 보려면 [여기](../../api/using/creating-a-privacy-request.md)를 클릭하십시오.

