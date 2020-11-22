---
solution: Campaign Standard
product: campaign
title: 다국어 이메일 만들기
description: 다음 단계에 따라 다양한 기본 언어를 사용하는 다국어 이메일 수신자를 대상으로 이메일을 작성합니다.
audience: channels
content-type: reference
topic-tags: email-messages
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 25%

---


# 다국어 이메일 만들기{#creating-a-multilingual-email}

선호하는 언어가 다른 프로필로 다국어 이메일을 보낼 수 있습니다.각 프로필은 자신의 기본 언어로 작성된 e-메일 변형이 수신됩니다.

다국어 이메일 템플릿을 사용할 수 있는지 확인하십시오. 없는 경우 [이 섹션에서](../../channels/using/multilingual-messages-template.md)만드는 방법을 학습합니다.

대상은 작성된 기본 언어 정보가 있는 프로필을 기반으로 합니다.

1. 다국어 템플릿을 기반으로 새로운 이메일을 [만듭니다](../../channels/using/multilingual-messages-template.md).

   ![](assets/multi_create1.png)

1. 표준 이메일과 마찬가지로 이메일의 일반 속성 및 타겟 대상자를 정의합니다. [대상자 만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.
1. 생성 마법사의 네 번째 단계에서 변형 옵션을 정의합니다. 다국어 템플릿 [에 모든 올바른 매개 변수가 이미 포함되어 있는 경우](../../channels/using/multilingual-messages-template.md) **[!UICONTROL Create]** 단추를 직접 클릭하면 됩니다.

   ![](assets/multi_create4.png)

   필요한 경우 **[!UICONTROL Add an element]** 단추를 사용하여 변형을 추가합니다. **[!UICONTROL Default]** 변형은 삭제할 수 없습니다. 로 설정된 **[!UICONTROL default]**&#x200B;경우 프로필 [의 기본 언어](../../audiences/using/creating-profiles.md) 를 사용하여 변형을 선택합니다. 다른 언어로 **[!UICONTROL Default]** 변형을 설정할 수도 있습니다.

1. 이메일 작성 확인:그러면 이메일 대시보드가 표시됩니다.
1. 각 변형의 이메일 컨텐츠를 정의합니다. 선택한 템플릿에 따라 여러 제목, 여러 발신자 이름 또는 여러 가지 다른 콘텐츠를 정의할 수 있습니다. 드롭다운 메뉴를 사용하여 요소의 다른 변형 간을 탐색할 수 있습니다. 자세한 정보는 [콘텐츠 편집기](../../designing/using/designing-content-in-adobe-campaign.md) 섹션을 참조하십시오.

   ![](assets/multi_selectcontent.png)

1. 메시지를 테스트하고 확인합니다. 전송 [증명](../../sending/using/sending-proofs.md) 섹션을 참조하십시오.
1. 전송과 함께 **[!UICONTROL Send after confirmation option]**&#x200B;예약합니다.
1. 이메일이 전송되면 해당 로그와 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md)을 참조하십시오.

**관련 항목:**

* [하나의 워크플로우를 통해 다국어 사용자에게 전달](https://helpx.adobe.com/kr/campaign/kb/simplify-campaign-management.html#Engageyourcustomersateverystep)
