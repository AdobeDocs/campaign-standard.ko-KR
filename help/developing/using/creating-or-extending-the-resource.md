---
solution: Campaign Standard
product: campaign
title: 리소스 만들기 또는 확장
description: 리소스를 처음부터 정의하는 방법을 살펴볼 수 있습니다.
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---


# 리소스 만들기 또는 확장{#creating-or-extending-the-resource}

내장 데이터 모델에 속하지 않은 데이터에 대한 작업이 필요한 경우 관리자는 새 리소스를 처음부터 만들거나 기존 리소스의 확장을 만들 수 있습니다.

다음과 같은 내장 리소스만 확장할 수 있습니다.

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

1. **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]**&#x200B;에서 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**:및  **[!UICONTROL Label]** 필드를  **[!UICONTROL ID]** 입력합니다. **[!UICONTROL ID]** 필드는 필수입니다. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >최대 30자를 사용할 수 있습니다.

   * **[!UICONTROL Extend an existing resource]**:확장할 리소스를 선택합니다.

      ![](assets/schema_extension_10.png)

1. **[!UICONTROL Create]**&#x200B;을 클릭하여 리소스를 만듭니다. 이 리소스는 새 리소스의 경우 **[!UICONTROL Draft]** 상태나 확장 시 **[!UICONTROL Editing]** 상태를 사용합니다.

새 리소스가 만들어지고 이제 구성할 수 있습니다. 리소스 구성에 대한 자세한 내용은 [리소스의 데이터 구조 구성](../../developing/using/configuring-the-resource-s-data-structure.md)을 참조하십시오.
