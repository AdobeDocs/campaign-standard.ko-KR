---
title: 데이터 모델 개념
seo-title: 데이터 모델 개념
description: 데이터 모델 개념
seo-description: Adobe Campaign 데이터 모델과 수정 방법에 대해 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: cacd 563 f -6936-4 b 3 e -83 e 3-5 d 4 ae 31 d 44 e 8
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: About-custom-resources
discoiquuid: 4 E 0468 DA -3052-4 CE 5-8174-45 ABA 1 F 5 C 4 ED
context-tags: Cusresource, overview; Eventcusresource, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: c880b265cf83cb76b2cdbe3cbdd77182adb71bb1

---


# Data model concepts{#data-model-concepts}

Adobe Campaign 에는 사전 정의된 데이터 모델이 포함되어 있습니다. This data model can be modified by [administrators](../../administration/using/types-of-users.md#functional-administrators) who are able to add new resources or extensions to existing resources.

>[!CAUTION]
>
>리소스를 만들고 수정하는 작업은 민감한 작업입니다. 전문가 사용자만 수행해야 합니다.

The **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.

Adobe Campaign에서 사용되는 데이터는 다른 리소스를 통해 정의됩니다.

You can **enrich the data template** that is provided by creating your own custom resources, such as purchase or product tables.

기본 리소스 (캠페인, 이메일 또는 대상자 등) 는 수정할 수 없습니다. 그러나 사용자 지정 리소스를 확장하여 새 필드를 추가할 수 있습니다.

>[!NOTE]
>
>You can find a datamodel representation for the out-of-the-box resources [here](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

You can also **configure the navigation** in the screens corresponding to the resource created.

확장 필드는 기본 필드와 충돌하지 않도록 접두사로 생성됩니다.
