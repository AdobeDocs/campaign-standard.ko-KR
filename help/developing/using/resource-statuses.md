---
title: 리소스 상태
seo-title: 리소스 상태
description: 리소스 상태
seo-description: 게시 상태에 따라 다른 리소스 상태를 발견할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 215 C 0 A 2 E -27 EC -43 F 3-BAAC -1 EAAC 7640784
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: About-custom-resources
discoiquuid: 85516477-1 b 95-4273-a 0 a 7-d 2 CBB 9950 AFD
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Resource statuses{#resource-statuses}

리소스는 게시 또는 활성화 상태에 따라 다른 상태를 가질 수 있습니다.

There are two columns dedicated to displaying these statuses in the **[!UICONTROL Custom resources]** screen.

![](assets/schema_colonne_1.png)

**게시 상태**

* **Draft**: 리소스가 방금 만들어졌거나 다시 작성되었습니다. 데이터베이스 표와 해당 API를 만들려면 리소스를 다시 게시해야 합니다. 리소스를 다시 작성하는 경우 게시 단계 다음에 자동으로 렌더링되지 않습니다.
* **보류 중인 초안**: 리소스가 다시 작성되었습니다. 다음 게시 중에 초안 프로세스가 발생합니다. 재작성은 되돌릴 수 없습니다. 다시 작성할 때 그리고 게시를 준비할 때 이 사실을 알리는 몇 가지 경고 메시지가 표시됩니다.

   For more on re-drafting, see [Deleting a resource](../../developing/using/deleting-a-resource.md).

   >[!NOTE]
   >
   >The **[!UICONTROL Cancel re-draft]** option is available when the resource that you want to re-draft still contains links through other resources with the "Published" status. 이 옵션을 사용하면 "초안 재설정" 프로세스를 되돌릴 수 있습니다. 그러면 사용자 지정 리소스가 원래 상태로 돌아갑니다.

* **게시일: 리소스가 게시되었습니다.** 마지막 수정 날짜 이후에 리소스가 수정되는 경우 최신 수정 사항을 고려하기 위해 다시 게시하라는 메시지가 표시됩니다.

**[!UICONTROL Do not publish latest modifications]** 이 필드는 향후 발행물 중에 수정 사항이 고려되지 않도록 합니다.

이 필드는 사용자 지정 리소스 정의에서 구성할 수 있습니다.
