---
title: 리소스 상태
description: 게시 상태에 따라 다른 리소스 상태를 검색합니다.
page-status-flag: never-activated
uuid: 215c0a2e-27ec-43f3-baac-1eaac7640784
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 85516477-1b95-4273-a0a7-d2cbb9950afd
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---


# 리소스 상태{#resource-statuses}

게시 또는 활성화 상태에 따라 자원의 상태가 다를 수 있습니다.

화면에 이러한 상태를 표시하는 데 사용되는 열이 두 개 **[!UICONTROL Custom resources]** 있습니다.

![](assets/schema_colonne_1.png)

**게시 상태**

* **초안**:리소스가 방금 생성되었거나 다시 작성되었습니다. 해당 API와 데이터베이스 테이블을 만들려면 리소스를 다시 게시해야 합니다. 리소스가 다시 작성되는 경우 게시 단계 후에 자동으로 비활성화됩니다.
* **보류 중인 다시 초안**:리소스가 다시 작성되었습니다. 초안 재작성 프로세스는 다음 발행물 중에 수행됩니다. 다시 드래프하는 것은 되돌릴 수 없다. 초안 작성 및 게시 준비 시 사용자에게 알리기 위해 몇 가지 경고 메시지가 표시됩니다.

   다시 드래프팅에 대한 자세한 내용은 리소스 [삭제를 참조하십시오](../../developing/using/deleting-a-resource.md).

   >[!NOTE]
   >
   >이 **[!UICONTROL Cancel re-draft]** 옵션은 다시 초안을 작성하려는 리소스에 &quot;게시됨&quot; 상태의 다른 리소스를 통한 링크가 여전히 포함되어 있는 경우에 사용할 수 있습니다. 이 옵션을 사용하면 &quot;다시 초안&quot; 프로세스를 되돌릴 수 있습니다. 그러면 사용자 지정 리소스가 원래 상태로 돌아갑니다.

* **게시됨**:리소스가 게시되었습니다. 마지막 수정 날짜 이후에 리소스가 수정되는 경우 최신 수정 사항을 고려하기 위해 리소스를 다시 게시하도록 초대하는 메시지가 표시됩니다.

이 **[!UICONTROL Do not publish latest modifications]** 필드는 향후 발행물 동안 수정 사항을 고려하지 않습니다.

이 필드는 사용자 지정 리소스 정의에서 구성할 수 있습니다.
