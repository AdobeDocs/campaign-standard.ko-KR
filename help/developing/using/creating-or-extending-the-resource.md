---
title: 리소스 만들기 또는 확장
description: 리소스를 처음부터 정의하는 방법을 살펴볼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 7c26b63d-9587-47 파섹
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 개발
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 8dc45c37-6908-407e-8e41-4a4188cba2b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 리소스 만들기 또는 확장{#creating-or-extending-the-resource}

즉시 사용 가능한 데이터 모델에 속하지 않는 데이터에 대해 작업해야 하는 경우 관리자는 처음부터 새 리소스를 만들거나 기존 리소스의 확장을 만들 수 있습니다.

다음과 같은 기본 리소스만 확장할 수 있습니다.

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

1. &gt; **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom Resources]**&#x200B;에서 **[!UICONTROL Create]** 단추를 클릭합니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**:및 **[!UICONTROL Label]** 필드를 **[!UICONTROL ID]** 입력합니다. 필수 **[!UICONTROL ID]** 필드입니다. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >최대 30자를 사용하는 것이 좋습니다.

   * **[!UICONTROL Extend an existing resource]**:확장할 리소스를 선택합니다.

      ![](assets/schema_extension_10.png)

1. 리소스를 **[!UICONTROL Create]** 만들려면 을(를) 클릭하십시오. 이렇게 하면 새 리소스의 경우 **[!UICONTROL Draft]** 상태나 확장 **[!UICONTROL Editing]** 시 상태가 적용됩니다.

새 리소스가 생성되어 이제 구성할 수 있습니다. 리소스 구성에 대한 자세한 내용은 [리소스의 데이터 구조](../../developing/using/configuring-the-resource-s-data-structure.md)구성을 참조하십시오.
