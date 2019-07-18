---
title: 보낸 사람으로 돌아가기
seo-title: 보낸 사람으로 돌아가기
description: 보낸 사람으로 돌아가기
seo-description: 잘못된 주소를 통보 받고 향후 커뮤니케이션에서 제외되는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 11981 c 2 f -0 b 7 f -4166-9 daa-ec 6 a 6 b 4 d 5367
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: DM
discoiquuid: 5 F 20 FF 3 F -8242-4735-8 C 60-C 57610 EDFF 52
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# Return to sender{#return-to-sender}

발신자 정보로 돌아가는 기능이 포함된 일반 메일 공급자와의 일반 파일 교환이 지원됩니다. 이에 따라 해당 우편 주소는 향후 커뮤니케이션에서 제외됩니다. 또한 다른 채널을 통해 고객에게 잘못된 주소를 알려주고 고객과의 관계를 강화하거나 우편 주소를 업데이트할 것을 권장할 수 있습니다.

예를 들어, 연락처가 새 위치로 이동되었고 새 우편 주소를 제공하지 않았습니다. 공급자가 잘못된 주소 목록을 검색하고 잘못된 주소를 자동으로 표시하는 Adobe Campaign로 이 정보를 보냅니다.

이 기능이 작동하려면 다이렉트 메일 기본 배달 템플릿에는 컨텐츠에 배달 로그 ID가 포함됩니다. 따라서 Adobe Campaign는 프로필 및 배달 데이터를 공급자가 반환한 정보와 동기화할 수 있게 됩니다.

![](assets/direct_mail_return_sender_1.png)

An import template is available under **[!UICONTROL Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs]**. 이 템플릿을 복제하여 직접 만듭니다. For more on using import templates, refer to [Using import templates](../../automating/using/defining-import-templates.md).

![](assets/direct_mail_return_sender_2.png)

가져오기가 완료되면 Adobe Campaign에서 자동으로 다음 작업을 수행합니다.

* 잘못된 주소가 프로필 수준에서 차단되었습니다.
* 배달 기본 표시기 (KPI) 가 업데이트되었습니다.
* 배달 로그가 업데이트됩니다.

