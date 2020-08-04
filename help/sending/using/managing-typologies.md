---
title: 유형화 관리
description: 유형화를 사용하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
internal: n
snippet: y
translation-type: ht
source-git-commit: ba1fcca02ce9582d85e57bde815ccf3f551ac7a3
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---


# 유형화 관리 {#managing-typologies}

## 유형화 기본 정보 {#about-typologies}

유형화는 메시지를 보내기 전에 메시지의 유효성을 검사할 수 있는 규칙 세트입니다. 예를 들어 메시지 콘텐츠가 비어 있는지, 구독 취소가 있는지, 중복 항목을 제외했는지 등을 확인합니다.

유형화에는 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** 메뉴를 통해 액세스할 수 있습니다. 애플리케이션에는 기본적으로 사용할 수 있는 기본 유형화가 있습니다. 필요에 따라 고유한 유형화를 만들거나 기존 유형화를 수정할 수 있습니다.

![](assets/typologies-list.png)

각 유형화의 경우 메시지에 사용할 때 실행되는 규칙 세트 목록이 **[!UICONTROL Typology rules]** 섹션에 있습니다.

![](assets/typology_typo-rule-list.png)

>[!NOTE]
>
>유형화 규칙 중 하나에 대해 자세한 내용을 보려면 해당 규칙을 두 번 클릭합니다. 규칙이 읽기 전용 모드로 표시됩니다.

## 유형화 만들기 {#creating-a-typology}

새 유형화를 만들려면 다음 단계를 수행하십시오.

1. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** 메뉴에 액세스합니다.

1. 유형화 목록이 표시됩니다. **[!UICONTROL Create]** 버튼을 클릭합니다.

   ![](assets/typologies-create.png)

1. 유형화 **[!UICONTROL Label]**&#x200B;을(를) 정의한 다음 **[!UICONTROL Add an element]** 버튼을 클릭하여 포함할 유형화 규칙을 선택합니다. 유형화 규칙에 대한 자세한 정보는 [이 섹션](../../sending/using/managing-typology-rules.md)을 참조하십시오.

   ![](assets/typology_addrules.png)

   >[!NOTE]
   >
   >**[!UICONTROL IP affinity]** 필드에서는 구성에 따라 관심도를 관리할 수 있습니다. 이는 인스턴스의 구성 파일에 정의됩니다. 관심도 기능을 사용하려면 관리자에게 문의하십시오.

1. **[!UICONTROL Create]**&#x200B;을(를) 클릭하여 선택 항목을 확인합니다. 이제 유형화를 메시지에 사용할 준비가 되었습니다.

## 메시지에 유형화 적용 {#applying-typologies-to-messages}

유형화를 메시지 또는 메시지 템플릿과 연결하면 해당 유형화에 포함된 유형화 규칙이 실행되어 메시지의 유효성을 검사합니다.

>[!NOTE]
>
>각 메시지 또는 메시지 템플릿에는 유형화를 하나씩만 할당할 수 있습니다.

메시지에 유형화를 연결하려면 다음 단계를 따르십시오.

1. 메시지 속성에 액세스합니다. 메시지 템플릿은 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** 탐색 메뉴에서 액세스할 수 있습니다.

1. **[!UICONTROL Advanced parameters]** > **[!UICONTROL Prearation]** 섹션에서 메시지에 연결할 유형화를 선택합니다.

   ![](assets/typology_message.png)

1. **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

   이제 선택한 유형화가 메시지에 연결됩니다. 관련된 유형화 규칙이 모두 실행되어 메시지의 유효성을 검사합니다.
