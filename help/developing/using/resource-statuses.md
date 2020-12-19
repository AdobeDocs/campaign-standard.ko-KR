---
solution: Campaign Standard
product: campaign
title: 리소스 상태
description: 게시 상태에 따라 다른 리소스 상태를 검색합니다.
audience: developing
content-type: reference
topic-tags: about-custom-resources
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---


# 리소스 상태{#resource-statuses}

게시 또는 활성화 상태에 따라 자원의 상태가 다를 수 있습니다.

**[!UICONTROL Custom resources]** 화면에 이러한 상태를 표시하는 데 사용되는 열이 두 개 있습니다.

![](assets/schema_colonne_1.png)

**게시 상태**

* **초안**:리소스가 방금 생성되었거나 다시 작성되었습니다. 해당 API와 데이터베이스 테이블을 만들려면 리소스를 다시 게시해야 합니다. 리소스를 다시 작성하고 있는 경우 게시 단계 후에 자동으로 비활성화됩니다.
* **보류 중인 다시 초안**:리소스가 다시 작성되었습니다. 초안 재작성 프로세스는 다음 게시 중에 수행됩니다. 드래프팅은 되돌릴 수 없다. 초안 작성 및 게시 준비 시 사용자에게 알리기 위해 몇 가지 경고 메시지가 표시됩니다.

   다시 드래프팅에 대한 자세한 내용은 [리소스 삭제](../../developing/using/deleting-a-resource.md)를 참조하십시오.

   >[!NOTE]
   >
   >다시 초안을 설정하려는 리소스에 &quot;게시됨&quot; 상태의 다른 리소스를 통한 링크가 여전히 포함되어 있는 경우 **[!UICONTROL Cancel re-draft]** 옵션을 사용할 수 있습니다. 이 옵션을 사용하면 &quot;다시 초안&quot; 프로세스를 되돌릴 수 있습니다. 그러면 사용자 지정 리소스가 원래 상태로 돌아갑니다.

* **게시됨**:리소스가 게시되었습니다. 마지막 수정 날짜 이후에 리소스가 수정되면 최신 수정 사항을 고려하기 위해 리소스를 다시 게시하도록 요청하는 메시지가 표시됩니다.

**[!UICONTROL Do not publish latest modifications]** 필드는 향후 발행물 제작 시 수정 사항을 고려하지 않습니다.

이 필드는 사용자 지정 리소스 정의에서 구성할 수 있습니다.
