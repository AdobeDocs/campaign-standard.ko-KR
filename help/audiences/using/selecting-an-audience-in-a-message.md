---
title: 메시지에서 대상자 선택
description: '"이메일 고객을 선택하는 단계별 절차:주요 대상 모집단 및 테스트 프로필"'
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
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# 메시지에서 대상자 선택{#selecting-an-audience-in-a-message}

Adobe Campaign을 사용하면 메시지의 대상자 내에 여러 프로필 유형을 구성할 수 있습니다.

작성 마법사를 통해 메시지를 만들 때 또는 메시지가 이미 만들어진 경우 메시지 대시보드에서 대상을 정의할 수 있습니다.

>[!NOTE]
>
>고객이 워크플로우 내에서 구축되어 추가 데이터를 확보한 경우 이러한 데이터를 사용하여 독립 실행형 전달을 개인화할 수 없습니다. 워크플로우에서 실행되는 전달에서만 사용할 수 있습니다.

1. 대시보드에서 대상 블록으로 이동하여 시작합니다.

   ![](assets/delivery_audience_definition_1.png)

   대상을 정의하는 화면이 열립니다. 메시지를 수신할 각 유형의 대상을 별도로 정의할 수 있는 두 개의 탭이 있습니다.

   * Target
   * 테스트 프로필
   ![](assets/delivery_audience_definition_2.png)

1. 이메일의 기본 **[!UICONTROL Target]** 내용을 정의합니다. 이메일의 일반 대상 대상입니다.

   대상은 **[!UICONTROL Target]** 탭에 정의되고 데이터베이스에서 식별된 프로필로 구성됩니다.

   [쿼리 편집기](../../automating/using/editing-queries.md#creating-queries) 기능을 사용하여 기본 대상을 설정할 수 있습니다.

   이 탭에서 **[!UICONTROL Shortcuts]** 팔레트에는 사전 정의된 필터와 식별된 프로파일에 정의된 대상만 포함됩니다. 이 **[!UICONTROL Explorer]** 탭에서는 추가 구성에 액세스할 수 있습니다.

   따라서 기존 대상을 다시 사용 및 결합하고 추가 필터를 적용하는 등

1. 이메일에 사용할 **[!UICONTROL Test profiles]** 항목을 정의합니다. 테스트 프로필은 이메일을 기본 타겟으로 보내기 전에 테스트하기 위해 전송할 수 있는 증명 자료를 받게 됩니다.

   테스트 프로필 구성에 대한 자세한 내용은 테스트 프로필 [섹션을](../../audiences/using/managing-test-profiles.md) 참조하십시오.

그러면 대상 블록이 업데이트되고 해당 이메일에 대해 타겟 및 테스트 프로필이 선택되었음을 표시합니다.

![](assets/delivery_audience_definition_3.png)

