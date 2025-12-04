---
title: 트리거 테스트
description: Adobe Campaign에서 트리거 를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 되는 문제 해결 팁에 대해 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 66628f2a-6ed3-4b12-b2ed-9b9eec440dc3
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 트리거 테스트{#testing-your-triggers}

다음 문제 해결 팁은 Adobe Campaign에서 트리거를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 됩니다.

**기능이 활성화되었습니까?**

트리거 - Campaign 통합이 활성화되었는지 확인하려면 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]**&#x200B;을(를) 선택합니다. **[!UICONTROL Experience Cloud Triggers]** 항목이 표시됩니다.

만약 당신이 그것을 본다면, 다음 단계로 넘어가세요.

그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. [기능 활성화](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality)를 참조하세요.

**트리거를 만들어 보세요**

[Campaign에서 매핑된 트리거 만들기](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign)에 설명된 단계에 따라 트리거를 만듭니다.

트리거가 만들어지면 다음 단계로 이동합니다. 그렇지 않으면 트리거 끝점 연결에 실패했음을 의미합니다. Experience Cloud(활성화 서비스)에서 트리거가 프로비저닝되었는지 확인합니다. 그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* 조직 ID
* Analytics 로그인 회사(Marketing Cloud 회사 이름과 같을 수 있음)

**트리거를 게시해 보세요**

[Campaign에서 매핑된 트리거 만들기](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign)에 설명된 단계에 따라 트리거를 게시합니다.

게시가 성공하면 다음 단계로 이동합니다. 그렇지 않은 경우 Adobe에 문의하여 인스턴스를 다시 시작하고 다시 시도하십시오.

**웹 사이트에서 트리거 생성**

트랜잭션 템플릿을 편집하고 게시하려면 [트랜잭션 메시지 템플릿 편집](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template)에 설명된 단계를 따르십시오. 그런 다음 웹 사이트에서 트리거 생성을 테스트합니다.

트리거가 Analytics에 의해 수신되면 다음 단계로 이동합니다. 그렇지 않으면 다음 항목을 확인하십시오.

* Analytics에 대한 트리거가 활성화되었습니다.
* MCID 및 Analytics를 사용하는 웹 사이트는 DTM에서 활성화됩니다
* 트리거를 만들 때 올바른 Analytics 보고서 세트가 사용됩니다

**Campaign에서 트리거를 받았습니까?**

그렇지 않은 경우 파이프라인에서 트리거가 수신되는지 확인합니다.

그렇지 않은 경우 Adobe에 문의하여 파이프라인 끝점의 구성을 확인하십시오.

해당하는 경우 다음 지침을 따르십시오.

* Campaign 데이터 소스의 조정 ID 유형을 확인합니다.
* CustomerId 데이터 소스는 고객 특성을 통해 만들어집니다.
* 데이터 소스 ID를 확인합니다.
* 데이터 소스 구성 후 Adobe에 Campaign 인스턴스를 다시 시작하도록 요청합니다.
* 트리거 보고서에서 트리거 구문 분석 문제를 확인합니다.

**트리거가 보류 중 상태입니까?**

그렇지 않으면 다음 단계로 이동합니다. 해당하는 경우 다음 지침을 따르십시오.

* 트랜잭션 템플릿이 게시되었는지 확인합니다.
* 프로필이 차단 목록에 추가하다에 있지 않은지 확인하십시오.
* 유형화 규칙의 적용을 확인합니다.
* 트랜잭션 메시지의 로그를 확인합니다.

**메시지가 유효합니까?**

메시지가 유효하지 않은 경우 다음 항목을 확인하십시오.

* 잘못된 것으로 표시된 데이터 보강 개인화 필드를 트리거하려면 연결된 eventCusResource 컬렉션에서 트랜잭션 템플릿의 유효성을 검사하십시오.
* 메시지 포맷 유효성 검사
