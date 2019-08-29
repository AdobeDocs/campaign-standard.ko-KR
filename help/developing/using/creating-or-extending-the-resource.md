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
source-git-commit: 50620788c05b76cc2f69c19c26f968ca15a02048

---


# 리소스 만들기 또는 확장{#creating-or-extending-the-resource}

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

1. 시작 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom Resources]****[!UICONTROL Create]** 단추를 클릭합니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Create a new resource]**: **[!UICONTROL Label]** AND **[!UICONTROL ID]** 필드를 입력합니다. 필드는 **[!UICONTROL ID]** 필수입니다. 레이블 필드를 비워 두면 ID에서 자동으로 완료됩니다.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >최대 30 자를 사용하는 것이 좋습니다.

   * **[!UICONTROL Extend an existing resource]**: 확장할 리소스를 선택합니다.

      ![](assets/schema_extension_10.png)

1. 을 클릭하여 **[!UICONTROL Create]** 리소스를 만든 다음, 새 리소스의 경우 **[!UICONTROL Draft]** 상태 또는 확장의 경우 **[!UICONTROL Editing]** 상태를 선택합니다.

새 리소스가 만들어지고 이제 구성할 수 있습니다. 리소스 구성에 대한 자세한 내용은 리소스 데이터 구조 [구성을](../../developing/using/configuring-the-resource-s-data-structure.md)참조하십시오.
