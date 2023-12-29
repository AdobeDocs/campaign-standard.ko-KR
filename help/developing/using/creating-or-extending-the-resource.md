---
title: 리소스 만들기 또는 확장
description: 리소스를 처음부터 정의하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
feature: Data Model
role: Developer
level: Experienced
exl-id: b8731088-a675-4070-9036-bf2b5254e4e8
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 11%

---

# 리소스 만들기 또는 확장{#creating-or-extending-the-resource}

기본 제공 데이터 모델의 일부가 아닌 데이터에 대한 작업이 필요한 경우 관리자는 새 리소스를 처음부터 만들거나 기존 리소스의 확장을 만들 수 있습니다.

다음 기본 제공 리소스만 확장할 수 있습니다.

* **[!UICONTROL Campaign (campaign)]**
* **[!UICONTROL Deliveries (delivery)]**
* **[!UICONTROL Landing page (Landingpage)]**
* **[!UICONTROL Profiles (profile)]**
* **[!UICONTROL Program (program)]**
* **[!UICONTROL Service (service)]**
* **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**
* **[!UICONTROL Test profiles (seedMember)]**
* **[!UICONTROL Workflow (workflow)]**

리소스를 만들거나 확장하려면 다음 작업을 수행하십시오.

1. 출처: **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]**&#x200B;를 클릭하고 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**: 다음을 입력합니다. **[!UICONTROL Label]** 및 **[!UICONTROL ID]** 필드. **[!UICONTROL ID]** 필드는 필수입니다. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

     ![](assets/schema_extension_2.png)

     >[!NOTE]
     >
     >최대 30자를 사용할 수 있습니다.

   * **[!UICONTROL Extend an existing resource]**: 확장할 리소스를 선택합니다.

     ![](assets/schema_extension_10.png)

1. 클릭 **[!UICONTROL Create]** 리소스를 만들고 이 리소스를 만든 후 **[!UICONTROL Draft]** 새 리소스의 경우 상태 또는 **[!UICONTROL Editing]** 확장 시 상태.

새 리소스가 만들어지고 이제 구성할 수 있습니다. 리소스 구성에 대한 자세한 내용은 [리소스의 데이터 구조 구성](../../developing/using/configuring-the-resource-s-data-structure.md).
