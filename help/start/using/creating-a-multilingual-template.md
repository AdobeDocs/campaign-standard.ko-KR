---
title: 다국어 템플릿 만들기
seo-title: 다국어 템플릿 만들기
description: 다국어 템플릿 만들기
seo-description: 자동 세그먼트화된 고객의 기본 언어를 기반으로 한 단일 배달을 통해 다국어 이메일/SMS 전달 방식을 정의하고 실행하는 방법을 살펴봅니다. 언어 및 개별 수준까지 다운로드에 대한 성과를 보고합니다.
page-status-flag: 정품 인증 안 함
uuid: 7 a 2 CD 5 F 7-C 0 FC -4825-A 770-A 72816 C 66 B 3 F
contentOwner: Sauviat
products: sg_ campaign/standard
audience: start
content-type: 참조
topic-tags: 관리 템플릿
discoiquuid: 064 c 5 c 4 a-f 579-4 bab-adf 3-51 c 92 eb 4518 f
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Creating a multilingual template{#creating-a-multilingual-template}

다국어 템플릿은 다국어 메시지를 관리하는 특정 템플릿입니다.

This kind of template is available for **Email and SMS messages** and useable in standalone mode, within a workflow or in a recurring delivery.

다국어 기능 템플릿에서 언어 관리는 변형을 기반으로 합니다. **각 변형은 하나의 언어를 나타냅니다.**

Adobe Campaign Standard는 최대 40 개의 변형을 설정할 수 있습니다.

Adobe Campaign는 기본 언어가 en로 설정되어 있습니다. 기본 언어는 다른 변형으로 변경할 수 있지만 절대 삭제되지 않아야 합니다.

템플릿 작성 중에 메시지에서 필요한 언어 수에 해당하는 변형 수를 추가할 수 있습니다.

SMS 또는 이메일 템플릿을 만들려면 다음 단계를 수행하십시오.

1. 기존 다국어 템플릿 (SMS 또는 이메일) 를 복제할 수 있습니다.

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >You can also modify an existing standard template in a multilingual template by clicking on the **[!UICONTROL Initialize content variant]** button in the template properties.

1. 속성을 수정하여 레이블, 추적 등을 사용자 지정합니다.
1. 변형 타일을 클릭하여 원하는 변형 수를 수정합니다. 변형 창이 표시됩니다.

   ![](assets/multi_template_variants.png)

   변형을 추가하거나 제거할 수 있습니다. To add a variant, complete the **[!UICONTROL New content variant]** window.

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >" 기본 "변형이 완료된 기본 언어 매개 변수 없이 프로필에 전송된 변형이므로 삭제하지 마십시오.

1. 필요한 경우 레이블 변형을 사용자 지정하고 확인을 클릭합니다.
1. 각 변형에 대한 컨텐츠를 직접 추가할 수도 있습니다.

이제 이 다국어 템플릿을 기반으로 이메일 또는 SMS 메시지를 만들 준비가 되었습니다.

**관련 항목:**

* [다국어 이메일 만들기](../../channels/using/creating-a-multilingual-email.md)
* [프로필 만들기](../../audiences/using/creating-profiles.md)

