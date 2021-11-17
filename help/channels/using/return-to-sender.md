---
title: 발신자에게 반송
description: 잘못된 주소에 대한 알림을 받고 향후 통신에서 제외하는 방법을 알아봅니다.
audience: channels
content-type: reference
topic-tags: direct-mail
feature: Direct Mail
role: User
level: Intermediate
exl-id: 6783aa68-7fd7-4f53-86bf-853c0fea5899
source-git-commit: 8be43668d1a4610c3388ad27e493a689925dc88c
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---

# 발신자에게 반송{#return-to-sender}

보낸 사람에게 반환 정보가 포함된 DM 공급자와의 플랫 파일 교환이 지원됩니다. 이를 통해 해당 우편 주소를 향후 통신에서 제외할 수 있습니다. 또한 잘못된 주소에 대한 알림을 받고 다른 채널을 통해 고객에게 연락하거나 우편 주소를 업데이트하도록 유도할 수 있습니다.

예를 들어 연락처가 새 위치로 이동했으며 새 우편 주소를 제공하지 않았습니다. 공급자가 잘못된 주소 목록을 검색하고 이 정보를 Adobe Campaign으로 보내면 자동으로 잘못된 주소를 차단 목록합니다.

이 기능이 작동하기 위해 DM 기본 게재 템플릿에는 콘텐츠에 게재 로그 ID가 포함됩니다. 따라서 Adobe Campaign은 프로필 및 게재 데이터를 공급자가 반환한 정보와 동기화할 수 있습니다.

![](assets/direct_mail_return_sender_1.png)

가져오기 템플릿은 **[!UICONTROL Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs]**. 이 템플릿을 복제하여 직접 만듭니다. 가져오기 템플릿 사용에 대한 자세한 내용은 [가져오기 템플릿 사용](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates).

![](assets/direct_mail_return_sender_2.png)

가져오기가 완료되면 Adobe Campaign에서 자동으로 다음 작업을 수행합니다.

* 프로필 수준에서 잘못된 주소차단 목록이에 추가됩니다
* 게재 기본 지표(KPI)가 업데이트됩니다
* 게재 로그가 업데이트됩니다
