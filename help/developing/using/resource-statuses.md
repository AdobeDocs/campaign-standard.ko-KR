---
title: 리소스 상태
description: 게시 상태에 따라 다른 리소스 상태를 검색합니다.
page-status-flag: 활성화 안 함
uuid: 215c0a2e-27ec-43f3-baac-1eaac7640784
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 개발
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 8516477-1b95-4273-a0a7-d2cbb9950afd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 리소스 상태{#resource-statuses}

리소스의 게시 또는 활성화 상태에 따라 상태가 다를 수 있습니다.

화면에 이러한 상태를 표시하는 데 사용되는 열이 두 개 **[!UICONTROL Custom resources]** 있습니다.

![](assets/schema_colonne_1.png)

**게시 상태**

* **초안**:리소스가 방금 생성되었거나 다시 작성되었습니다. 데이터베이스 테이블과 해당 API를 만들려면 리소스를 다시 게시해야 합니다. 리소스가 다시 작성되는 경우 게시 단계에 따라 자동으로 비활성화됩니다.
* **다시 초안**&#x200B;대기 중:리소스가 다시 작성되었습니다. 다시 초안 작성 프로세스는 다음 게시 중에 수행됩니다. 다시 드래프하는 것은 되돌릴 수 없다. 여러 경고 메시지는 다시 초안을 작성할 때와 게시 준비 시 모두 이 사실을 사용자에게 경고합니다.

   다시 드래프팅에 대한 자세한 내용은 리소스 [삭제를](../../developing/using/deleting-a-resource.md)참조하십시오.

   >[!NOTE]
   >
   >이 **[!UICONTROL Cancel re-draft]** 옵션은 다시 작성하려는 리소스에 "게시됨" 상태의 다른 리소스를 통한 링크가 여전히 포함되어 있는 경우에 사용할 수 있습니다. 이 옵션을 사용하면 "다시 초안" 프로세스를 되돌릴 수 있습니다. 그러면 사용자 지정 리소스가 원래 상태로 돌아갑니다.

* **게시됨**:리소스가 게시되었습니다. 마지막 수정 날짜 이후에 리소스가 수정되면 사용자에게 최신 수정 사항을 고려하도록 다시 게시하라는 메시지가 표시됩니다.

이 **[!UICONTROL Do not publish latest modifications]** 필드는 향후 발행물 동안 수정 사항을 고려하지 않습니다.

이 필드는 사용자 지정 리소스 정의에서 구성할 수 있습니다.
