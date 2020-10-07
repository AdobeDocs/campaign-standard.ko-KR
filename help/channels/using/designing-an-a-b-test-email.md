---
title: A/B 테스트 이메일 디자인
description: A/B 테스트 기능을 살펴보고 다음 단계에 따라 Adobe Campaign의 A/B 테스트 템플릿에서 이메일을 만듭니다.
page-status-flag: never-activated
uuid: 104f6973-68a7-4692-a90a-a5570a980ec7
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: e249ba70-90d0-43f2-868c-ce9fdc7e642d
context-tags: delivery,abTesting,back;deliveryCreation,wizard;delivery,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 100%

---


# A/B 테스트 이메일 디자인{#designing-an-a-b-test-email}

Adobe Campaign의 A/B 테스트 기능을 사용하면 2~3개의 이메일 변형을 정의할 수 있습니다. 각 변형은 가장 좋은 결과를 판단하기 위해 모집단 샘플로 전송됩니다. 일단 결정되면 채택된 변형은 나머지 모집단으로 전송됩니다.

이메일의 콘텐츠, 제목 또는 발신자를 변경하도록 선택할 수 있습니다.

>[!NOTE]
>
>Adobe Experience Manager에서 만든 이메일에 대한 A/B 테스트는 수행할 수 없습니다.

## A/B 테스트 이메일 만들기 {#creating-an-a-b-test-email}

A/B 테스트 구성 단계가 추가되는 표준 이메일 생성 마법사를 사용하여 A/B 테스트를 만들 수 있습니다. 표준 이메일 만들기는 [이메일 만들기](../../channels/using/creating-an-email.md) 섹션에 자세히 설명되어 있습니다.

A/B 테스트의 특정 컨텍스트에서 다음을 수행합니다.

1. 변경하려는 요소에 따라 세 가지 A/B 테스트 특정 템플릿 중 하나에서 새 이메일을 만듭니다.

   * 발신자에 대한 A/B 테스트
   * 콘텐츠에 대한 A/B 테스트
   * 제목에 대한 A/B 테스트

   ![](assets/create_ab_testing.png)

   >[!NOTE]
   >
   >후속 및 A/B 테스트 템플릿은 기본적으로 숨겨져 있습니다. 왼쪽(**[!UICONTROL Filter]** 측면 패널)에 있는 A/B 테스트 상자를 체크하여 표시합니다.

1. 표준 이메일과 마찬가지로 이메일의 일반 속성 및 타겟 대상자를 정의합니다. [대상자 만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.
1. 생성 마법사의 네 번째 단계에서 A/B 테스트 매개 변수를 정의합니다.

   * **[!UICONTROL Number of variants]**: 2개 또는 3개의 변형을 사용하도록 선택할 수 있습니다. 3개의 변형을 선택하는 경우 마법사에서 이 단계를 확인한 후에는 이 선택을 수정할 수 없습니다.
   * **[!UICONTROL Winning strategy]**: 채택 변형을 결정하는 데 사용할 기준을 선택합니다. 
   * **[!UICONTROL Target breakdown]**: 각 변형을 받을 타겟의 비율을 선택합니다. 나머지 비율은 일단 결정되면 채택된 변형을 받게 됩니다. 타겟 프로필이 임의로 선택됩니다.
   * **[!UICONTROL Winner sending method]**: 일단 결정되면 채택 변형이 자동으로 전송되도록 할지 또는 나머지 모집단으로의 전송을 수동으로 확인할지 여부를 선택합니다.
   * **[!UICONTROL Test duration]**: 테스트 기간을 지정합니다. 이 기간 후에 채택 변형이 자동으로 결정됩니다. 이메일 대시보드에서 테스트 종료 전에 채택 변형을 수동으로 선택할 수 있습니다.

      모든 추적 데이터를 수집하고 채택 변형을 선택하기 위해 올바르게 고려하려면 테스트가 최소 1시간 이상이어야 합니다.
   ![](assets/ab_parameters.png)

1. A/B 테스트 매개 변수가 정의되면 마법사의 다음 단계로 전달하여 이메일 콘텐츠를 정의합니다. 선택한 템플릿에 따라 여러 제목, 여러 발신자 이름 또는 여러 가지 다른 콘텐츠를 정의할 수 있습니다. 회전식을 사용하여 요소의 다른 변형 간을 탐색합니다. 자세한 정보는 [콘텐츠 편집기](../../designing/using/designing-content-in-adobe-campaign.md) 섹션을 참조하십시오.

   ![](assets/create_ab_testing2.png)

1. 이메일 만들기를 확인합니다. 그러면 이메일 대시보드가 표시됩니다.
1. 전송을 예약합니다. 정의된 날짜는 A/B 테스트의 시작 날짜를 나타냅니다.
1. **[!UICONTROL A/B test parameters]** 블록에 표시된 A/B 테스트 매개 변수를 확인합니다. 블록을 선택하여 테스트(9단계) 전송을 확인할 때까지 수정할 수 있습니다.

   ![](assets/create_ab_testing3.png)

1. 전송 타겟 및 메시지 수를 분석하기 위해 이메일 전송을 준비합니다. [전송 준비](../../sending/using/preparing-the-send.md) 섹션을 참조하십시오.
1. A/B 테스트를 보내기 전에 증명을 보내 이메일을 확인합니다.
1. 준비가 완료되면 테스트 전송을 확인합니다. 확인되면 A/B 테스트 매개 변수는 수정할 수 없습니다.

   A/B 테스트는 **[!UICONTROL Schedule]**&#x200B;에 정의된 날짜에 시작됩니다. **[!UICONTROL A/B test]** 및 **[!UICONTROL Deployment]** 블록을 사용하여 진행 상황을 추적할 수 있습니다.

   테스트 기간을 짧게 줄이려면 언제든지 채택 변형을 수동으로 선택할 수 있습니다.

   테스트가 완료되면, 요약 테이블이 **[!UICONTROL A/B Test]** 블록에 표시되므로 테스트된 여러 변형의 다양한 지표를 볼 수 있습니다.

1. 전송 방법으로 **[!UICONTROL Send after confirmation]**&#x200B;을(를) 선택한 경우 채택 변형을 수동으로 선택하여 나머지 모집단으로 전송해야 합니다. **[!UICONTROL Automatic]**&#x200B;을(를) 선택한 경우, 채택 변형은 시스템에서 결정하는 즉시 나머지 모집단으로 자동 전송됩니다.

   >[!NOTE]
   >
   >동률인 경우 채택 변형을 수동으로 선택해야 합니다. 이메일 생성자 및 수정자에게 변형이 선택되었거나 선택되어야 함을 알릴 수 있습니다. [Adobe Campaign 알림](../../administration/using/sending-internal-notifications.md)을 참조하십시오.

이제 이메일이 정의 및 전송되었습니다. 해당 로그 및 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다.

**관련 항목**:

[이메일 만들기](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/create-email-from-homepage.html) 비디오

## A/B 테스트 지표 기본 정보 {#about-a-b-test-indicators}

이메일 대시보드에서 A/B 테스트를 측정하는 데 도움이 되는 몇 가지 지표(클릭 수, 열람 수, 반송 수 등)를 사용할 수 있습니다.

**[!UICONTROL Estimated recipient reactivity]** 지표는 클릭한 수신자 수와 이메일을 열람한 수신자 수를 비교하는 비율입니다. 예를 들어 10명의 수신자가 이메일을 열고 5명의 수신자가 이메일을 클릭한 경우 반응성 비율은 50%입니다.
