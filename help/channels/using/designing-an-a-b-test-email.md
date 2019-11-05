---
title: A/B 테스트 이메일 디자인
description: A/B 테스트 기능을 살펴보고 다음 단계에 따라 Adobe Campaign의 A/B 테스트 템플릿에서 이메일을 만듭니다.
page-status-flag: 활성화 안 함
uuid: 104f6973-68a7-4692-a90a-a5570a980ec7
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 이메일 메시지
discoiquuid: e249ba70-90d0-43f2-868c-ce9fdc7e642d
context-tags: delivery,abTesting,back;deliveryCreation,wizard;delivery,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# A/B 테스트 이메일 디자인{#designing-an-a-b-test-email}

Adobe Campaign의 A/B 테스트 기능을 사용하면 2-3개의 이메일 변형을 정의할 수 있습니다. 각 변형은 최상의 결과를 얻을 수 있는 것을 결정하기 위해 모집단 샘플로 전송됩니다. 확인 후 우승한 변형이 나머지 모집단으로 전송됩니다.

이메일의 컨텐츠, 제목 또는 발신자를 다르게 선택할 수 있습니다.

>[!NOTE]
>
>Adobe Experience Manager에서 만든 이메일에 대해 A/B 테스트를 수행할 수 없습니다.

## Creating an A/B test email {#creating-an-a-b-test-email}

A/B 테스트는 A/B 테스트 구성 단계가 추가되는 표준 이메일 작성 마법사를 사용하여 생성할 수 있습니다. 표준 이메일 만들기는 이메일 [만들기](../../channels/using/creating-an-email.md) 섹션에서 자세히 설명합니다.

A/B 테스트의 특정 컨텍스트에서:

1. 변경할 요소에 따라 세 개의 A/B 테스트 특정 템플릿 중 하나에서 새 이메일을 만듭니다.

   * 보낸 사람의 A/B 테스트
   * 컨텐츠에 대한 A/B 테스트
   * 주제에 대한 A/B 테스트
   ![](assets/create_ab_testing.png)

   >[!NOTE]
   >
   >후속 작업 및 A/B 테스트 템플릿은 기본적으로 숨겨집니다. 왼쪽에 있는 A/B 테스트 상자( **[!UICONTROL Filter]** 측면 패널)를 선택하여 표시합니다.

1. 표준 이메일과 마찬가지로 이메일의 일반 속성과 대상 고객을 정의합니다. 대상자 [만들기](../../audiences/using/creating-audiences.md) 섹션을 참조하십시오.
1. 작성 마법사의 네 번째 단계에서 A/B 테스트 매개 변수를 정의합니다.

   * **[!UICONTROL Number of variants]**:2 또는 3개의 변형을 사용할 수 있습니다. 세 가지 변형을 선택하는 경우 마법사에서 이 단계를 확인한 후에는 이 선택 사항을 수정할 수 없습니다.
   * **[!UICONTROL Winning strategy]**:우승한 변형을 결정하는 데 사용할 기준을 선택합니다.
   * **[!UICONTROL Target breakdown]**:각 변형을 받을 대상의 백분율을 선택합니다. 나머지 백분율은 우승자가 결정되면 우승 변형을 받습니다. 대상 프로파일이 임의로 선택됩니다.
   * **[!UICONTROL Winner sending method]**:우승한 변형을 결정한 후 자동으로 전송할지 또는 나머지 모집단으로의 전송을 수동으로 확인할지 여부를 선택합니다.
   * **[!UICONTROL Test duration]**:테스트 기간을 지정합니다. 우승 변형은 이 기간 후에 자동으로 결정됩니다. 이메일 대시보드에서 테스트가 종료되기 전에 우승 변형을 수동으로 선택할 수 있습니다.

      모든 추적 데이터를 수집하고 올바른 계산에 포함시켜 우승 변형을 선택하려면 테스트가 최소한 1시간 이상이어야 합니다.
   ![](assets/ab_parameters.png)

1. A/B 테스트 매개 변수가 정의되면 마법사의 다음 단계로 전달하여 이메일 컨텐츠를 정의합니다. 선택한 템플릿에 따라 여러 주체, 여러 보낸 사람 이름 또는 여러 개의 서로 다른 컨텐츠를 정의할 수 있습니다. 회전판을 사용하여 요소의 다른 변형을 탐색합니다. 자세한 내용은 [컨텐츠 편집기](../../designing/using/overview.md) 섹션을 참조하십시오.

   ![](assets/create_ab_testing2.png)

1. 이메일 만들기를 확인합니다. 그러면 이메일 대시보드가 표시됩니다.
1. 전송을 예약합니다. 정의된 날짜는 A/B 테스트의 시작을 나타냅니다.
1. 블록에 표시된 A/B 테스트 매개 변수를 **[!UICONTROL A/B test parameters]** 확인합니다. 블록을 선택하여 테스트(9단계) 전송을 확인할 때까지 수정할 수 있습니다.

   ![](assets/create_ab_testing3.png)

1. 보낼 대상 및 메시지 수를 분석하기 위해 이메일 전송을 준비합니다. 보내기 [준비](../../sending/using/preparing-the-send.md) 섹션을 참조하십시오.
1. A/B 테스트를 보내기 전에 교정본을 보내 이메일을 확인하십시오.
1. 준비가 완료되면 테스트 전송을 확인합니다. 확인되면 A/B 테스트 매개 변수를 수정할 수 없습니다.

   A/B 테스트는 에 정의된 날짜에 시작됩니다. **[!UICONTROL Schedule]**&#x200B;및 **[!UICONTROL A/B test]** **[!UICONTROL Deployment]** 블록을 사용하여 진행 상태를 추적할 수 있습니다.

   테스트 기간을 짧게 줄이려면 언제든지 우승 변형을 수동으로 선택할 수 있습니다.

   테스트가 완료되면 요약 테이블이 **[!UICONTROL A/B Test]** 블록에 표시되어 테스트된 여러 변형의 다양한 지표를 볼 수 있습니다.

1. 전송 **[!UICONTROL Send after confirmation]** 방법으로 선택한 경우 우승하는 변형을 수동으로 선택하여 나머지 모집단으로 전송해야 합니다. 이 옵션을 선택한 **[!UICONTROL Automatic]**&#x200B;경우 선택된 변형이 시스템에 의해 결정되면 나머지 모집단으로 자동 전송됩니다.

   >[!NOTE]
   >
   >타이가 있는 경우 우승 변형을 수동으로 선택해야 합니다. 이메일 생성자 및 수정자에게 변형을 선택했거나 선택해야 한다는 사실을 알릴 수 있습니다. Adobe [Campaign 알림을](../../administration/using/sending-internal-notifications.md)참조하십시오.

이제 이메일이 정의 및 전송됩니다. 해당 로그와 보고서에 액세스하여 캠페인의 성공을 측정할 수 있습니다.

**관련 항목**:

[이메일](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-email-from-homepage-feature-video-use.html) 비디오 만들기

## A/B 테스트 지표 정보 {#about-a-b-test-indicators}

이메일 대시보드에서 A/B 테스트를 측정하는 데 도움이 되는 몇 가지 지표를 사용할 수 있습니다.클릭 수, 열기, 바운스 수 등

표시기는 **[!UICONTROL Estimated recipient reactivity]** 클릭한 받는 사람 수와 이메일을 연 받는 사람 수를 비교하는 비율입니다. 예를 들어 10명의 수신자가 이메일을 열고 5명의 수신자가 이메일을 클릭한 경우 재활동 비율은 50%입니다.
