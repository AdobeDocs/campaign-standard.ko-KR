---
solution: Campaign Standard
product: campaign
title: 트리거 테스트
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: 트리거
role: 데이터 아키텍트
level: 중간
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 2%

---


# 트리거 테스트{#testing-your-triggers}

다음 문제 해결 팁은 Adobe Campaign에서 트리거를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 됩니다.

**기능이 활성화됩니까?**

트리거 - 캠페인 통합이 활성화되었는지 확인하려면 왼쪽 상단 모서리에서 Adobe Campaign 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]**&#x200B;을 선택합니다. **[!UICONTROL Experience Cloud Triggers]** 항목이 표시됩니다.

이 메시지가 표시되면 다음 단계로 이동합니다.

그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. [기능 활성화](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality)를 참조하십시오.

**트리거 만들기**

[Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign)에서 매핑된 트리거 만들기에 설명된 단계에 따라 트리거를 만듭니다.

트리거가 만들어지면 다음 단계로 이동합니다. 그렇지 않으면 트리거 끝점 연결이 실패했음을 의미합니다. 트리거가 Experience Cloud(활성화 서비스)에서 제공되는지 확인합니다. 그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오. 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* IMS 조직 ID
* Analytics 로그인 회사(Marketing Cloud 회사 이름과 같을 수 있음)

**트리거 게시**

[Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign)에서 매핑된 트리거 만들기에 설명된 단계에 따라 트리거를 게시합니다.

게시에 성공하면 다음 단계로 이동합니다. 없는 경우 Adobe에 문의하여 인스턴스를 다시 시작하고 다시 시도하십시오.

**웹 사이트에서 트리거 생성**

트랜잭션 템플릿을 편집하고 게시하려면 [트랜잭션 메시지 템플릿](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template)에 설명된 단계를 수행합니다. 그런 다음 웹 사이트에서 트리거 생성을 테스트합니다.

Analytics에서 트리거를 받으면 다음 단계로 이동합니다. 없는 경우 다음 항목을 확인하십시오.

* Analytics에 대해 트리거가 활성화되어 있습니다.
* MCID 및 Analytics를 사용한 웹 사이트가 DTM에서 활성화됩니다
* 트리거를 만드는 동안 올바른 Analytics 보고서 세트가 사용됩니다.

**트리거가 Campaign에서 수신됩니까?**

그렇지 않은 경우 트리거가 파이프라인에서 수신되었는지 확인합니다.

그렇지 않은 경우 Adobe에 문의하여 파이프라인 끝점 구성을 확인합니다.

그렇다면 다음 지침을 따르십시오.

* 캠페인 데이터 소스에서 조정 ID 유형을 확인합니다.
* CustomerId Datasource는 고객 속성을 통해 만들어집니다.
* 데이터 소스 ID를 확인합니다.
* 데이터 소스 구성 후 Adobe에 캠페인 인스턴스를 다시 시작하도록 요청합니다.
* 트리거 보고서에서 구문 분석 문제를 확인하십시오.

**트리거가 보류 중인 상태입니까?**

그렇지 않으면 다음 단계로 이동합니다. 그렇다면 다음 지침을 따르십시오.

* 트랜잭션 템플릿이 게시되었는지 확인합니다.
* 프로필이에 없는지 차단 목록 확인합니다.
* 유형 규칙 적용을 확인합니다.
* 트랜잭션 메시지 로그를 확인합니다.

**메시지가 유효합니까?**

메시지가 유효하지 않은 경우 다음 항목을 확인하십시오.

* 데이터 연계 강화 개인화 필드가 잘못됨으로 표시된 경우 관련 eventCusResource 컬렉션에서 트랜잭션 템플릿을 확인합니다.
* 메시지 형식 유효성 확인

