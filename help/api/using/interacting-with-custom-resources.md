---
title: 사용자 정의 리소스
description: API를 사용한 사용자 정의 리소스 관리에 대한 자세한 내용/
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
source-git-commit: 538739417c4ed28ff2991186dac5fb69d1af3afd

---


# 사용자 정의 리소스와 상호 작용 {#interacting-with-custom-resources}

/customResources **종단점을** 사용하면 ACS 사용자 지정 리소스를 REST에 표시할 수 있습니다. 이 API를 기반으로 사용자 지정 엔티티와 외부 끝점 간의 통합을 사용할 수 있습니다.

/customResources 끝점은 /profileAndServices 끝점과 정확하게 동일한 비헤이비어를 갖습니다.

이 API 내에 노출된 사용자 지정 리소스는 다음과 같습니다.

* 프로필 엔티티에 연결된 모든 엔티티
* 프로필 엔티티의 자식에 연결된 모든 엔티티
* 프로필에 연결되지 않은 모든 개체, 이러한 개체, 그 자식 및 손주 개체입니다.

>[!NOTE]
>/profileAndServicesExt 아래에서 사용할 수 있는 사용자 지정 리소스는 /customResources API에 노출되지 않습니다.

다음은 사용자 지정 리소스에서 메타데이터를 검색하는 예입니다.

```
GET /customResources/resourceType/<customResourceName>
```

생성, 업데이트 또는 삭제를 수행하기 위해 GET, POST, PATCH, DELETE가 사용됩니다.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>개인 정보 API 끝점 및 워크플로(/privacy/privacyTool)가 프로필 엔티티에 연결되지 않은 사용자 지정 리소스를 관리하지 않습니다.
>이러한 사용자 정의 리소스에 대한 PII를 관리하고 정리할 책임이 있습니다. 개인 정보 보호 도구에 대한 자세한 내용을 보려면 여기를 [클릭하십시오](../../api/using/creating-a-privacy-request.md).

