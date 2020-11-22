---
solution: Campaign Standard
product: campaign
title: 다국어 메시지 템플릿
description: 자동으로 세그먼트화된 고객의 선호 언어를 기반으로 하는 단일 게재를 통해 다국어 이메일/SMS 게재를 정의하고 실행하는 방법을 알아봅니다. 언어 및 개인 수준에 대한 모든 게재의 성과를 보고합니다.
audience: start
content-type: reference
topic-tags: managing-templates
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 100%

---


# 다국어 메시지 템플릿 {#multilingual-messages-template}

다국어 템플릿은 다국어 메시지를 관리하기 위한 특정 템플릿입니다. 이 유형의 템플릿은 **이메일** 및 **SMS 메시지**&#x200B;에 대해 사용할 수 있으며, 워크플로우나 되풀이하는 게재에서 독립 실행형 모드로 사용 가능합니다.

다국어 기능 템플릿에서 언어 관리는 변형을 기반으로 합니다. **각 변형은 하나의 언어를 나타냅니다**. Adobe Campaign Standard에서는 최대 40개의 변형을 설정할 수 있습니다.

Adobe Campaign에는 **영어**&#x200B;가 기본 언어로 설정되어 있습니다. 기본 언어를 다른 변형으로 변경할 수 있지만 삭제할 수는 없습니다.

템플릿을 만들 때 메시지에 필요한 언어 수에 해당하는 변형 수를 추가할 수 있습니다.

SMS 또는 이메일 템플릿을 만들려면 다음 단계를 수행하십시오.

1. 기존 다국어 템플릿(SMS 또는 이메일)을 복제합니다.

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >템플릿 속성에서 **[!UICONTROL Initialize content variant]** 버튼을 클릭하여 다국어 템플릿의 기존 표준 템플릿을 수정할 수도 있습니다.

1. 속성을 수정하여 레이블, 추적 등을 사용자 정의합니다.

1. 변형 타일을 클릭하여 원하는 변형 수를 수정합니다. 변형 창이 표시됩니다.

   ![](assets/multi_template_variants.png)

   변형을 추가하거나 제거할 수 있습니다. 변형을 추가하려면 **[!UICONTROL New content variant]** 창을 완성합니다.

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >&quot;기본&quot; 변형을 삭제하면 안 됩니다. 선호 언어 매개 변수가 완성되지 않은 프로필에는 기본 변형이 전송되기 때문입니다.

1. 필요한 경우 레이블 변형을 사용자 지정하고 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

1. 각 변형에 대한 콘텐츠를 직접 추가할 수도 있습니다.

이제 다국어 템플릿을 기반으로 이메일 또는 SMS 메시지를 만들 수 있습니다.

**관련 항목:**

* [다국어 이메일 만들기](../../channels/using/creating-a-multilingual-email.md)
* [프로필 만들기](../../audiences/using/creating-profiles.md)
