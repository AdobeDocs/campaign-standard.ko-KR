---
title: 다국어 이메일 만들기
description: 다음 단계에 따라 다양한 기본 언어를 사용하는 다국어 이메일 타겟팅 수신자를 만듭니다.
audience: channels
content-type: reference
topic-tags: email-messages
feature: Email
role: User
level: Intermediate
exl-id: fcf192cb-f2d5-4340-bc2f-add0c195ad4e
source-git-commit: d234d7fab039b602eff06c03ba0d8f7ce2a0cf3f
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 24%

---

# 다국어 이메일 만들기{#creating-a-multilingual-email}

서로 다른 기본 언어를 사용하는 프로필에 다국어 이메일을 보낼 수 있습니다. 각 프로필은 기본 언어로 변형 이메일을 받게 됩니다.

이렇게 하려면 다국어 이메일 템플릿을 사용할 수 있는지 확인하십시오. 그렇지 않으면 [이 섹션](../../channels/using/multilingual-messages-template.md)에서 만드는 방법을 알아보세요.

대상자는 완성된 기본 언어 정보가 있는 프로필을 기반으로 합니다.

1. [다국어 템플릿](../../channels/using/multilingual-messages-template.md)을(를) 기반으로 새 전자 메일을 만듭니다.

   ![](assets/multi_create1.png)

1. 표준 이메일과 마찬가지로 이메일의 일반 속성 및 타겟 대상자를 정의합니다. [대상자 만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.

1. 만들기 마법사의 네 번째 단계에서 변형 옵션을 정의합니다. [다국어 템플릿](../../channels/using/multilingual-messages-template.md)에 이미 올바른 매개 변수가 모두 포함되어 있는 경우 **[!UICONTROL Create]** 단추를 직접 클릭할 수 있습니다.

   ![](assets/multi_create4.png)

   필요한 경우 **[!UICONTROL Add an element]** 단추를 사용하여 변형을 추가합니다. **[!UICONTROL Default]** 변형은 삭제할 수 없습니다. **[!UICONTROL default]**(으)로 설정하면 [프로필의 기본 언어](../../audiences/using/creating-profiles.md)가 변형을 선택하는 데 사용됩니다. **[!UICONTROL Default]** 변형을 다른 언어로 설정할 수도 있습니다.

1. 이메일 만들기 확인: 이메일 대시보드가 표시됩니다.
1. 각 변형에 대한 이메일 콘텐츠를 정의합니다. 선택한 템플릿에 따라 여러 제목, 여러 발신자 이름 또는 여러 가지 다른 콘텐츠를 정의할 수 있습니다. 드롭다운 메뉴를 사용하여 요소의 다른 변형 간을 탐색합니다. 자세한 정보는 [콘텐츠 편집기](../../designing/using/designing-content-in-adobe-campaign.md) 섹션을 참조하십시오.

   ![](assets/multi_selectcontent.png)

1. 메시지 테스트 및 유효성 검사 [증명 보내기](../../sending/using/sending-proofs.md) 섹션을 참조하십시오.
1. **[!UICONTROL Send after confirmation option]**(으)로 전송을 예약합니다.
1. 이메일이 전송되면 해당 로그 및 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md)을 참조하십시오.

