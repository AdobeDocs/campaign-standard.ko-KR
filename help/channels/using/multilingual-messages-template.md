---
title: 다국어 메시지 템플릿
description: 자동으로 세그먼트화된 고객의 선호 언어를 기반으로 한 단일 전달을 통해 다국어 이메일/SMS 전달을 정의하고 실행하는 방법을 알아봅니다. 언어 및 개별 수준에 대한 모든 전달의 성과를 보고합니다.
page-status-flag: never-activated
uuid: 7a2cd5f7-c0fc-4825-a770-a62816c66b3f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: managing-templates
discoiquuid: 064c5c4a-f579-4bab-adf3-51c92eb4518f
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: efb1f14e0094e200d186423f98bfad65d25cfab2

---


# 다국어 메시지 템플릿 {#multilingual-messages-template}

다국어 템플릿은 다국어 메시지를 관리하는 특정 템플릿입니다. 이러한 유형의 템플릿은 이메일 및 SMS **메시지에** 사용할 수 있으며, **워크플로우** 내 또는 반복 전달에서 독립 실행형 모드에서 사용할 수 있습니다.

다국어 기능 템플릿에서 언어 관리는 변형을 기반으로 합니다. **각 변형은 하나의 언어를**&#x200B;나타냅니다. Adobe Campaign Standard는 최대 40개의 변형을 설정할 수 있습니다.

Adobe Campaign은 EN으로 설정된 기본 언어와 함께 **제공됩니다**. 기본 언어를 다른 변형으로 변경할 수 있지만 삭제할 수 없습니다.

템플릿을 만드는 동안 메시지의 필요한 언어 수에 해당하는 변형 수를 추가할 수 있습니다.

SMS 또는 이메일 템플릿을 만들려면 다음 단계를 따르십시오.

1. 기존 다국어 템플릿(SMS 또는 이메일)을 복제합니다.

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >템플릿 속성에 있는 **[!UICONTROL Initialize content variant]** 단추를 클릭하여 다국어 템플릿의 기존 표준 템플릿을 수정할 수도 있습니다.

1. 속성을 수정하여 레이블, 추적 등을 사용자 정의합니다.
1. 변형 타일을 클릭하여 원하는 변형 수를 수정합니다. 변형 창이 표시됩니다.

   ![](assets/multi_template_variants.png)

   변형을 추가하거나 제거할 수 있습니다. 변형을 추가하려면 **[!UICONTROL New content variant]** 창을 완료하십시오.

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >완성된 기본 언어 매개 변수 없이 프로파일로 전송된 변형이므로 &quot;기본&quot; 변형을 삭제하지 마십시오.

1. 필요한 경우 레이블 변형을 사용자 정의하고 을 클릭합니다 **[!UICONTROL Confirm]**.
1. 각 변형의 컨텐츠를 직접 추가할 수도 있습니다.

다국어 템플릿을 기반으로 이메일 또는 SMS 메시지를 만들 준비가 되었습니다.

**관련 항목:**

* [다국어 이메일 만들기](../../channels/using/creating-a-multilingual-email.md)
* [프로필 만들기](../../audiences/using/creating-profiles.md)
