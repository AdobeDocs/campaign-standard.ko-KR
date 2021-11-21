---
title: 사용자 정의 리소스
description: API를 사용한 사용자 지정 리소스 관리에 대해 자세히 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 19bfeecb-da60-479c-a929-0cfb72ef59e3
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---

# 사용자 정의 리소스와 상호 작용 {#interacting-with-custom-resources}

다음 **/customResources** 엔드포인트를 사용하면 REST에 Campaign 사용자 지정 리소스를 표시할 수 있습니다. 이 API를 기반으로 사용자 지정 엔티티와 외부 엔드포인트 간의 통합을 사용할 수 있습니다.

/customResources 종단점은 /profileAndServices 종단점과 동일한 동작을 갖습니다.

이 API 내에 노출된 사용자 지정 리소스는 다음과 같습니다.

* /profileAndServicesExt 아래에 노출되지 않은 모든 엔터티
* 프로필과 연결되지 않은 모든 개체, 이러한 엔터티, 그 자식 및 손자손녀
* 기본적으로 어떤 항목에도 연결되어 있지 않은 모든 엔티티와 해당 자식 및 손자손녀입니다.

>[!NOTE]
>/profileAndServicesExt에서 사용할 수 있는 사용자 지정 리소스는 /customResources API에 노출되지 않습니다.


다음은 사용자 지정 리소스에서 메타데이터를 검색하는 예입니다.

```
GET /customResources/resourceType/<customResourceName>
```

생성, 업데이트 또는 삭제를 수행하려면 GET, POST, PATCH, DELETE이 사용됩니다.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>개인 정보 보호 API 엔드포인트 및 워크플로우(/privacy/privacyTool)는 프로필 엔티티에 연결되어 있지 않은 사용자 지정 리소스를 관리하지 않습니다.
>이러한 사용자 지정 리소스에 대한 PII를 관리하고 정리할 책임이 있습니다. 개인 정보 도구에 대한 자세한 내용은 [여기를 클릭하십시오.](../../api/using/creating-a-privacy-request.md).
