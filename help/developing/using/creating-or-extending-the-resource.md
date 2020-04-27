---
title: 리소스 만들기 또는 확장
description: 리소스를 처음부터 정의하는 방법을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 7c26b63d-9587-472b-804f-cde5c45dfb3c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 8dc45c37-6908-407e-8e41-4a4188cba2b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# 리소스 만들기 또는 확장{#creating-or-extending-the-resource}

기본 데이터 모델에 속하지 않은 데이터에 대해 작업해야 하는 경우 관리자는 처음부터 새 리소스를 만들거나 기존 리소스의 확장을 만들 수 있습니다.

다음과 같은 기본 제공 리소스만 확장할 수 있습니다.

* **[!UICONTROL Campaign (campaign)]**
* **[!UICONTROL Deliveries (delivery)]**
* **[!UICONTROL Landing page (Landingpage)]**
* **[!UICONTROL Profiles (profile)]**
* **[!UICONTROL Program (program)]**
* **[!UICONTROL Service (service)]**
* **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**
* **[!UICONTROL Test profiles (seedMember)]**
* **[!UICONTROL Workflow (workflow)]**

리소스를 만들거나 확장하려면

1. > **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]**&#x200B;에서 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**:및 **[!UICONTROL Label]** 필드를 **[!UICONTROL ID]** 입력합니다. 필수 **[!UICONTROL ID]** 필드입니다. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >최대 30자를 사용합니다.

   * **[!UICONTROL Extend an existing resource]**:확장할 리소스를 선택합니다.

      ![](assets/schema_extension_10.png)

1. 아이콘을 **[!UICONTROL Create]** 클릭하여 리소스를 만들면 새 리소스의 경우 **[!UICONTROL Draft]** 상태나 확장 **[!UICONTROL Editing]** 시 상태가 적용됩니다.

새 리소스가 생성되어 이제 구성할 수 있습니다. 리소스 구성에 대한 자세한 내용은 [리소스의 데이터 구조](../../developing/using/configuring-the-resource-s-data-structure.md)구성을 참조하십시오.
