---
title: 발신자에게 반송
description: 잘못된 주소를 알리고 향후 통신에서 이를 제외하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 11981c2f-0b7f-4 파섹
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 다이렉트 메일
discoiquuid: 5f20ff3f-8242-4735-8c60-c57610edff52
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 발신자에게 반송{#return-to-sender}

보낸 사람에게 반환 정보가 포함된 DM 공급자와의 기본 파일 교환이 지원됩니다. 이를 통해 해당 우편 주소를 향후 통신에서 제외할 수 있습니다. 또한 잘못된 주소를 통보 받고 다른 채널을 통해 고객과 교류하거나 우편 주소를 업데이트하도록 유도할 수 있습니다.

예를 들어 연락처가 새 위치로 이동되었으며 새 우편 주소를 제공하지 않았습니다. 공급자가 잘못된 주소 목록을 검색하여 Adobe Campaign에 이 정보를 전송하면 잘못된 주소가 자동으로 블랙리스트에 표시됩니다.

이 기능이 작동하려면 DM 기본 배달 템플릿에는 배달 로그 ID가 포함되어 있습니다. 따라서 Adobe Campaign은 프로필 및 게재 데이터를 공급자가 반환한 정보와 동기화할 수 있습니다.

![](assets/direct_mail_return_sender_1.png)

가져오기 템플릿은 에서 사용할 수 **[!UICONTROL Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs]**&#x200B;있습니다. 이 템플릿을 복제하여 직접 만듭니다. 가져오기 템플릿 사용에 대한 자세한 내용은 가져오기 템플릿 [사용을 참조하십시오](../../automating/using/defining-import-templates.md).

![](assets/direct_mail_return_sender_2.png)

가져오기가 완료되면 Adobe Campaign은 다음 작업을 자동으로 수행합니다.

* 프로필 수준에서 잘못된 주소가 차단되었습니다.
* 전달 기본 지표(KPI)가 업데이트됩니다.
* 배달 로그가 업데이트됩니다.

