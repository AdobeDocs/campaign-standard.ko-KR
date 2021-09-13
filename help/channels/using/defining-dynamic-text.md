---
title: 동적 텍스트 정의
description: Adobe Campaign에 정의된 조건에 따라 사용자에게 서로 다른 텍스트를 동적으로 표시하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: defining-conditional-content
feature: SMS
role: User
level: Beginner
exl-id: 649e3428-a3bf-470f-923c-04d9a57a208f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# 동적 텍스트 정의{#defining-dynamic-text}

다이내믹 텍스트는 다이내믹 콘텐츠와 동일한 방식으로 정의됩니다. [동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email) 섹션을 참조하십시오.

>[!NOTE]
>
>SMS 및 푸시의 경우 다이내믹 텍스트만 정의할 수 있습니다. 랜딩 페이지에서 동적 콘텐츠와 텍스트를 모두 정의할 수 있습니다. [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)를 사용하여 동적 텍스트를 정의하려면 [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)를 참조하십시오.

유니코드 문자 집합의 기본 다국어 평면에 포함되지 않은 문자인 대리 쌍은 2바이트(16비트)로 저장할 수 없으며 2UTF-16자로 인코딩되어야 합니다. 이러한 문자에는 일부 CJK IDEOGRAPHS, 대부분의 이모지와 일부 언어가 포함됩니다.
<br>이러한 문자로 인해 동적 텍스트에 일부 비호환성 문제가 발생할 수 있습니다. 메시지를 보내기 전에 강력한 테스트를 수행해야 합니다.


아래 예는 SMS 메시지에서 동적 텍스트를 정의하는 방법을 보여줍니다.

1. 메시지 또는 랜딩 페이지 본문에서 텍스트를 선택합니다.
1. **[!UICONTROL Enable dynamic text]**&#x200B;를 클릭합니다.

   ![](assets/dynamic_text_sms_1.png)

   팔레트에 **[!UICONTROL Dynamic text]** 옵션이 표시됩니다. 다이내믹 콘텐츠와 동일한 방식으로 구성됩니다.

1. 변형을 선택합니다.

   ![](assets/dynamic_text_sms_2.png)

1. 이 변형에 대한 조건을 정의합니다.

   ![](assets/dynamic_text_sms_4.png)

하나 이상의 변형에 대해 조건이 정의되면 동적 텍스트 주위에 자주색 프레임이 표시됩니다.

![](assets/dynamic_text_sms_3.png)
