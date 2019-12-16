---
title: 다국어 이메일 만들기
description: 다음 단계에 따라 다양한 기본 언어를 사용하는 다국어 이메일 타깃팅 수신자를 만듭니다.
page-status-flag: never-activated
uuid: e90f4ec8-14e3-4304-b5fc-bce0ba08a4ef
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 79231445-1d51-499a-adcf-0c0f6db1cfa3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b70e18be29fd48d102313f6d741e9ffe053cc34

---


# 다국어 이메일 만들기{#creating-a-multilingual-email}

다음과 같이 여러 언어를 선호하는 프로필로 다국어 이메일을 보낼 수 있습니다.각 프로필은 자신의 기본 언어로 변형된 이메일을 수신하게 됩니다.

다국어 이메일 템플릿을 사용할 수 있는지 확인하십시오. 없는 경우 [이 섹션에서](../../start/using/creating-a-multilingual-template.md)만드는 방법을 알아봅니다.

대상은 작성된 기본 언어 정보가 있는 프로필을 기반으로 합니다.

1. [다국어 템플릿을](../../start/using/creating-a-multilingual-template.md)기반으로 새로운 이메일을 만듭니다.

   ![](assets/multi_create1.png)

1. 표준 이메일과 마찬가지로 이메일의 일반 속성과 대상 고객을 정의합니다. 대상자 [만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.
1. 작성 마법사의 네 번째 단계에서 변형 옵션을 정의합니다. 다국어 템플릿에 [모든 올바른 매개 변수가 이미 포함되어 있는 경우](../../start/using/creating-a-multilingual-template.md) **[!UICONTROL Create]** 단추를 직접 클릭할 수 있습니다.

   ![](assets/multi_create4.png)

   필요한 경우 **[!UICONTROL Add an element]** 단추를 사용하여 변형을 추가합니다. **[!UICONTROL Default]** variant는 삭제할 수 없습니다. 로 **[!UICONTROL default]**&#x200B;설정하면 [프로파일의 기본 언어가](../../audiences/using/creating-profiles.md) 변형을 선택하는 데 사용됩니다. 다른 언어로 변형을 설정할 수도 **[!UICONTROL Default]** 있습니다.

1. 이메일 작성 확인:그러면 이메일 대시보드가 표시됩니다.
1. 각 변형의 이메일 컨텐츠를 정의합니다. 선택한 템플릿에 따라 여러 주체, 여러 보낸 사람 이름 또는 여러 개의 서로 다른 컨텐츠를 정의할 수 있습니다. 드롭다운 메뉴를 사용하여 요소의 다양한 변형을 탐색합니다. 자세한 내용은 [컨텐츠 편집기](../../designing/using/designing-content-in-adobe-campaign.md) 섹션을 참조하십시오.

   ![](assets/multi_selectcontent.png)

1. 메시지를 테스트하고 확인합니다. 전송 [증명](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) 섹션을 참조하십시오.
1. 전송과 함께 **[!UICONTROL Send after confirmation option]**&#x200B;예약을 참조하십시오.
1. 이메일이 전송되면 해당 로그와 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다. For more on reporting, refer to [this section](../../reporting/using/about-dynamic-reports.md).

**관련 항목:**

* [하나의 워크플로우를 통해 다국어 사용자에게 전달](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Engageyourcustomersateverystep)
