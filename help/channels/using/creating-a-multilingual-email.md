---
title: 다국어 이메일 만들기
description: 다음 단계에 따라 다양한 선호 언어로 다국어 이메일 타겟팅 수신자를 만듭니다.
audience: channels
content-type: reference
topic-tags: email-messages
feature: Email
role: User
level: Intermediate
exl-id: fcf192cb-f2d5-4340-bc2f-add0c195ad4e
source-git-commit: b5e98c07ee55cab0b6a628a97162ccd64711501a
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 24%

---

# 다국어 이메일 만들기{#creating-a-multilingual-email}

다음과 같이 다양한 선호 언어를 사용하는 프로필에 다국어 이메일을 보낼 수 있습니다. 각 프로필은 이메일의 변형을 자신의 기본 언어로 받게 됩니다.

다국어 이메일 템플릿을 사용할 수 있는지 확인합니다. 없는 경우 [이 섹션](../../channels/using/multilingual-messages-template.md)에서 만드는 방법을 알아봅니다.

대상자는 선호 언어 정보가 완료된 프로필을 기반으로 합니다.

1. [다국어 템플릿](../../channels/using/multilingual-messages-template.md)을(를) 기반으로 새 이메일을 만듭니다.

   ![](assets/multi_create1.png)

1. 표준 이메일과 마찬가지로 이메일의 일반 속성 및 타겟 대상자를 정의합니다. [대상자 만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.
1. 만들기 마법사의 네 번째 단계에서 변형 옵션을 정의합니다. [다국어 템플릿](../../channels/using/multilingual-messages-template.md)에 이미 모든 올바른 매개 변수가 포함되어 있는 경우 **[!UICONTROL Create]** 버튼을 직접 클릭할 수 있습니다.

   ![](assets/multi_create4.png)

   필요한 경우 **[!UICONTROL Add an element]** 버튼을 사용하여 변형을 추가합니다. **[!UICONTROL Default]** 변형을 삭제하면 안 됩니다. **[!UICONTROL default]**&#x200B;으로 설정하면 [프로필의 기본 언어](../../audiences/using/creating-profiles.md)가 변형을 선택하는 데 사용됩니다. **[!UICONTROL Default]** 변형을 다른 언어로 설정할 수도 있습니다.

1. 전자 메일 만들기 확인: 그러면 이메일 대시보드가 표시됩니다.
1. 각 변형에 대한 이메일 콘텐츠를 정의합니다. 선택한 템플릿에 따라 여러 제목, 여러 발신자 이름 또는 여러 가지 다른 콘텐츠를 정의할 수 있습니다. 드롭다운 메뉴를 사용하여 요소의 다른 변형 간을 탐색합니다. 자세한 정보는 [콘텐츠 편집기](../../designing/using/designing-content-in-adobe-campaign.md) 섹션을 참조하십시오.

   ![](assets/multi_selectcontent.png)

1. 메시지를 테스트하고 확인합니다. [증명 보내기](../../sending/using/sending-proofs.md) 섹션을 참조하십시오.
1. 전송을 **[!UICONTROL Send after confirmation option]**&#x200B;으로 예약합니다.
1. 전자 메일이 전송되면 해당 로그 및 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md)을 참조하십시오.

