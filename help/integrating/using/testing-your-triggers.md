---
title: 트리거 테스트
description: Adobe Campaign에서 트리거를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 되는 문제 해결 팁을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 66628f2a-6ed3-4b12-b2ed-9b9eec440dc3
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# 트리거 테스트{#testing-your-triggers}

다음 문제 해결 팁은 Adobe Campaign에서 트리거를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 됩니다.

**기능이 활성화됩니까?**

트리거 - Campaign 통합이 활성화되었는지 확인하려면 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭한 다음 을(를) 선택합니다 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]**. 다음을 볼 수 있습니다. **[!UICONTROL Experience Cloud Triggers]** 항목.

표시되면 다음 단계로 이동합니다.

그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. 자세한 내용은 [기능 활성화](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**트리거 만들기 시도**

에 설명된 단계를 수행합니다. [Campaign에서 매핑된 트리거 만들기](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) 트리거를 만듭니다.

트리거가 만들어지면 다음 단계로 이동합니다. 그렇지 않으면 트리거 끝점 연결에 실패했음을 의미합니다. 트리거가 Experience Cloud(활성화 서비스)에서 제공되는지 확인합니다. 그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* IMS 조직 ID
* Analytics 로그인 회사 (Marketing Cloud 회사 이름과 같을 수 있음)

**트리거 게시 시도**

에 설명된 단계를 수행합니다. [Campaign에서 매핑된 트리거 만들기](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) 트리거를 게시하려면 다음을 수행하십시오.

게시에 성공하면 다음 단계로 이동합니다. 없는 경우 Adobe에 문의하여 인스턴스를 다시 시작한 후 다시 시도하십시오.

**웹 사이트에서 트리거 생성**

에 설명된 단계를 수행합니다. [트랜잭션 메시지 템플릿 편집](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template) 트랜잭션 템플릿을 편집하고 게시하려면 다음을 수행하십시오. 그런 다음 웹 사이트에서 트리거 생성을 테스트합니다.

Analytics에서 트리거를 받으면 다음 단계로 이동합니다. 없는 경우 다음 항목을 확인하십시오.

* Analytics에 대해 트리거가 활성화되어 있습니다.
* MCID 및 Analytics를 사용한 웹 사이트가 DTM에서 활성화되어 있습니다
* 트리거를 만들 때 올바른 Analytics 보고서 세트가 사용됩니다

**Campaign에서 트리거를 수신합니까?**

그렇지 않은 경우 파이프라인에서 트리거가 수신되는지 확인합니다.

없는 경우 Adobe에 문의하여 파이프라인 끝점 구성을 확인합니다.

이 경우 다음 지침을 따르십시오.

* Campaign 데이터 소스에서 조정 ID 유형을 확인합니다.
* 고객 ID 데이터 소스는 고객 속성을 통해 만들어집니다.
* 데이터 소스 ID를 확인합니다.
* 데이터 소스 구성 후 Adobe에게 Campaign 인스턴스를 다시 시작하도록 요청합니다.
* 트리거 보고서에서 트리거 구문 분석 문제를 확인하십시오.

**트리거가 보류 중 상태입니까?**

없는 경우 다음 단계로 이동합니다. 이 경우 다음 지침을 따르십시오.

* 트랜잭션 템플릿이 게시되었는지 확인합니다.
* 프로필이에 차단 목록 있지 않은지 확인합니다.
* 유형화 규칙의 적용을 확인합니다.
* 트랜잭션 메시지의 로그를 확인합니다.

**메시지가 유효합니까?**

메시지가 올바르지 않으면 다음 항목을 확인하십시오.

* 잘못된 것으로 표시된 트리거 데이터 보강 개인화 필드의 경우 연결된 eventCusResource 컬렉션에서 트랜잭션 템플릿의 유효성을 확인합니다.
* 메시지 형식의 유효성 검사
