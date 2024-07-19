---
title: 리소스 상태
description: 게시 상태에 따라 다양한 리소스 상태를 살펴봅니다.
audience: developing
content-type: reference
topic-tags: about-custom-resources
feature: Data Model
role: Developer
level: Experienced
exl-id: 7290ebc5-8a58-4b7f-99bf-d942e37c944e
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---

# 리소스 상태{#resource-statuses}

게시 또는 활성화 상태에 따라 리소스의 상태가 다를 수 있습니다.

**[!UICONTROL Custom resources]** 화면에 이러한 상태를 표시하는 데 사용되는 열이 두 개 있습니다.

![](assets/schema_colonne_1.png)

**게시 상태**

* **초안**: 리소스가 방금 만들어졌거나 다시 초안 상태가 되었습니다. 데이터베이스 테이블과 해당 API를 만들려면 리소스를 다시 게시해야 합니다. 리소스를 다시 초안 중인 경우 게시 단계 후 자동으로 비활성화됩니다.
* **다시 초안 보류 중**: 리소스가 다시 초안 처리되었습니다. 재초안 프로세스는 다음 게시 중에 수행됩니다. 초안을 다시 만드는 것은 돌이킬 수 없다. 다시 초안을 작성할 때와 게시 준비를 할 때 사용자에게 알리기 위해 몇 가지 경고 메시지가 표시됩니다.

  다시 초안에 대한 자세한 내용은 [리소스 삭제](../../developing/using/deleting-a-resource.md)를 참조하세요.

  >[!NOTE]
  >
  >**[!UICONTROL Cancel re-draft]** 옵션은 다시 초안을 작성하려는 리소스에 &quot;게시됨&quot; 상태의 다른 리소스를 통한 링크가 여전히 포함되어 있을 때 사용할 수 있습니다. 이 옵션을 사용하면 &quot;초안으로 되돌리기&quot; 프로세스를 되돌릴 수 있습니다. 그러면 사용자 지정 리소스는 원래 상태로 돌아갑니다.

* **게시됨**: 리소스가 게시되었습니다. 리소스가 마지막 수정 날짜 이후에 수정된 경우, 최신 수정 사항을 고려하기 위해 리소스를 다시 게시하도록 초대하는 메시지가 표시됩니다.

**[!UICONTROL Do not publish latest modifications]** 필드를 사용하면 나중에 게시할 때 수정 사항을 고려하지 않습니다.

이 필드는 사용자 지정 리소스 정의에서 구성할 수 있습니다.
