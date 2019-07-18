---
title: 리소스 만들기 또는 확장
seo-title: 리소스 만들기 또는 확장
description: 리소스 만들기 또는 확장
seo-description: 리소스를 처음부터 정의하는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 7 C 26 B 63 D -9587-472 B -804 F-CDE 5 C 45 DFB 3 C
contentOwner: Sauviat
products: sg_ campaign/standard
audience: developing
content-type: 참조
topic-tags: adding-or-extending-a-resource
discoiquuid: 8 DC 45 C 37-6908-407 E -8 E 41-4 A 4188 CBA 2 B 3
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Creating or extending the resource{#creating-or-extending-the-resource}

기본 데이터 모델의 일부가 아닌 데이터에 대해 작업이 필요한 경우 관리자는 처음부터 새로 만들거나 기존 리소스의 확장을 만들 수 있습니다.

다음과 같은 기본 리소스를 확장할 수 있습니다.

* **[!UICONTROL Campaign (campaign)]**
* **[!UICONTROL Deliveries (delivery)]**
* **[!UICONTROL Landing page (Landingpage)]**
* **[!UICONTROL Profiles (profile)]**
* **[!UICONTROL Program (program)]**
* **[!UICONTROL Service (service)]**
* **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**
* **[!UICONTROL Test profiles (seedMember)]**
* **[!UICONTROL Workflow (workflow)]**

리소스를 만들거나 확장하려면:

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom Resources]**, click the **[!UICONTROL Create]** button.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**: **[!UICONTROL Label]** AND **[!UICONTROL ID]** 필드를 입력합니다. The **[!UICONTROL ID]** field is mandatory. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

      ![](assets/schema_extension_2.png)

   * **[!UICONTROL Extend an existing resource]**: 확장할 리소스를 선택합니다.

      ![](assets/schema_extension_10.png)

1. Click **[!UICONTROL Create]** to create the resource, which will then take on the **[!UICONTROL Draft]** status in case of new resource or the **[!UICONTROL Editing]** status in case of extension.

새 리소스가 만들어지고 이제 구성할 수 있습니다. For more on resource configuration, refer to [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).
