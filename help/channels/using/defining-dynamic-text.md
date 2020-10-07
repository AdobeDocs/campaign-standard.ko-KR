---
title: 동적 텍스트 정의
description: Adobe Campaign에 정의된 조건에 따라 사용자에게 동적으로 다른 텍스트를 표시하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: bbcd200c-4fb4-467b-ba39-09b8bee9bcaa
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: defining-conditional-content
discoiquuid: 6bb6cee3-5674-4113-8073-5a9572b3e830
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---


# 동적 텍스트 정의{#defining-dynamic-text}

동적 텍스트는 동적 컨텐츠와 동일한 방식으로 정의됩니다. 동적 컨텐츠 [정의 섹션을](../../designing/using/personalization.md#defining-dynamic-content-in-an-email) 참조하십시오.

>[!NOTE]
>
>SMS 및 푸시 기능의 경우 동적 텍스트만 정의할 수 있습니다. 랜딩 페이지에서 동적 컨텐츠와 텍스트를 모두 정의할 수 있습니다. 이메일 [디자이너](../../designing/using/designing-content-in-adobe-campaign.md)를 사용하여 동적 텍스트를 정의하려면, 이메일에서 [동적 컨텐츠 정의를 참조하십시오](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

유니코드 문자 세트의 기본 다국어 평면에 포함되지 않은 문자를 대체 쌍으로 2바이트(16비트)로 저장할 수 없으며 2UTF-16자로 인코딩해야 합니다. 이러한 문자에는 일부 CJK 비디오, 대부분의 이모지 및 일부 언어가 포함됩니다.
<br>이러한 문자는 동적 텍스트에서 일부 비호환성 문제를 일으킬 수 있습니다. 메시지를 보내기 전에 강력한 테스트를 수행해야 합니다.


아래 예제는 SMS 메시지에서 동적 텍스트를 정의하는 방법을 보여줍니다.

1. 메시지 본문 또는 랜딩 페이지에서 텍스트를 선택합니다.
1. **[!UICONTROL Enable dynamic text]**&#x200B;을(를) 클릭합니다.

   ![](assets/dynamic_text_sms_1.png)

   이 **[!UICONTROL Dynamic text]** 옵션이 팔레트에 표시됩니다. 동적 컨텐츠와 동일한 방식으로 구성됩니다.

1. 변형을 선택합니다.

   ![](assets/dynamic_text_sms_2.png)

1. 이 변형의 조건을 정의합니다.

   ![](assets/dynamic_text_sms_4.png)

하나 이상의 변형에 대해 조건을 정의하면 동적 텍스트 주위에 자주색 프레임이 표시됩니다.

![](assets/dynamic_text_sms_3.png)
