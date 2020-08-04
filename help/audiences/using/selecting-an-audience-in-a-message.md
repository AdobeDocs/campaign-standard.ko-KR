---
title: 메시지에서 대상자 선택
description: '"이메일의 대상자를 선택하는 단계별 절차: 주요 타겟 모집단 및 테스트 프로필"'
page-status-flag: never-activated
uuid: 7d8f8446-f2e0-49c1-83f6-9667b29bc228
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 158da6ff-8899-4e7b-b925-8a42c3de46a1
context-tags: deliveryCreation,wizard;delivery,audience,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705
workflow-type: ht
source-wordcount: '294'
ht-degree: 100%

---


# 메시지에서 대상자 선택{#selecting-an-audience-in-a-message}

Adobe Campaign에서는 메시지 대상자 내에 여러 프로필 유형을 구성할 수 있습니다.

대상자는 만들기 마법사를 통해 메시지를 만들 때 정의하거나 메시지가 이미 만들어진 경우 메시지 대시보드에서 정의할 수 있습니다.

>[!NOTE]
>
>대상자가 워크플로우 내에서 만들어지고 추가 데이터로 보강된 경우, 이 데이터를 사용하여 독립 실행형 게재를 개인화할 수는 없습니다. 이 데이터는 워크플로우에서 실행되는 게재에서만 사용할 수 있습니다.

1. 먼저 대시보드에서 대상자 블록으로 이동합니다.

   ![](assets/delivery_audience_definition_1.png)

   대상자를 정의하는 화면이 열립니다. 두 개의 탭에서 메시지를 받을 대상자의 각 유형을 별도로 정의할 수 있습니다.

   * 타겟
   * 테스트 프로필
   ![](assets/delivery_audience_definition_2.png)

1. 이메일의 주요 **[!UICONTROL Target]**&#x200B;을(를) 정의합니다. 이메일의 일반적인 타겟 대상자입니다.

   타겟은 **[!UICONTROL Target]** 탭에서 정의되며, 데이터베이스에서 식별된 프로필로 구성됩니다.

   [쿼리 편집기](../../automating/using/editing-queries.md#creating-queries) 기능을 사용하여 주요 타겟을 설정할 수 있습니다.

   이 탭의 **[!UICONTROL Shortcuts]** 팔레트에는 사전 정의된 필터와 식별된 프로필에서 정의한 대상자만 포함됩니다. **[!UICONTROL Explorer]** 탭에서는 추가 구성에 액세스할 수 있습니다.

   따라서 기존 대상자를 다시 사용 및 결합하고 추가 필터를 적용하는 등의 작업을 할 수 있습니다.

1. 이메일에 사용할 **[!UICONTROL Test profiles]**&#x200B;을(를) 정의합니다. 테스트 프로필에게 증명을 보내어 주요 타겟에게 보내기 전에 테스트할 수 있습니다.

   테스트 프로필 구성에 대한 자세한 내용은 [테스트 프로필](../../audiences/using/managing-test-profiles.md) 섹션을 참조하십시오.

그러면 대상자 블록이 업데이트되고, 문제가 되는 이메일에 대해 타겟 및 테스트 프로필이 선택되었음을 표시합니다.

![](assets/delivery_audience_definition_3.png)

