---
title: 트리거 테스트
seo-title: 트리거 테스트
description: 트리거 테스트
seo-description: null
page-status-flag: 정품 인증 안 함
uuid: B 3 A 6667 D-E 843-4 AD 6-817 E-D 91542 B 5 F 2 E 2
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-triggers
discoiquuid: f 67 e 69 f 2-09 fb -4 f 33-b 2 c 3-c 67 a 060743 e 3
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Testing your triggers{#testing-your-triggers}

다음 문제 해결 팁은 Adobe Campaign와 함께 트리거를 사용할 때 발생할 수 있는 가장 일반적인 문제를 해결하는 데 도움이 됩니다.

**기능이 활성화됩니까?**

To check if the Triggers - Campaign integration is activated, click the Adobe Campaign logo, in the top left corner, then select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]**. You should see the **[!UICONTROL Experience Cloud Triggers]** item.

이 경우 다음 단계로 이동합니다.

그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에 문의하십시오. See [Activating the functionality](../../integrating/using/configuring-triggers-in-experience-cloud.md#activating-the-functionality).

**트리거 만들기**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to create a trigger.

트리거가 만들어지면 다음 단계로 이동합니다. 그렇지 않으면 종료 지점 연결 연결이 실패했음을 의미합니다. 트리거가 Experience Cloud (활성화 서비스) 에서 프로비저닝되는지 확인합니다. 그렇지 않은 경우 Adobe 계정 담당자 또는 전문 서비스 파트너에 문의하십시오. 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* IMS 조직 ID
* Analytics 로그인 회사 (Marketing Cloud 회사 이름과 같을 수 있음)

**트리거 게시**

Follow the steps described in [Creating a mapped trigger in Campaign](../../integrating/using/using-triggers-in-campaign.md#creating-a-mapped-trigger-in-campaign) to publish the trigger.

게재가 성공하면 다음 단계로 이동합니다. 그렇지 않은 경우, Adobe에 문의하여 인스턴스를 다시 시작하고 다시 시도하십시오.

**웹 사이트에서 트리거 생성**

Follow the steps described in [Editing the transactional message template](../../integrating/using/using-triggers-in-campaign.md#editing-the-transactional-message-template) to edit and publish the transactional template. 그런 다음 웹 사이트에서 트리거 생성을 테스트합니다.

트리거가 트리거를 받으면 다음 단계로 이동합니다. 그렇지 않은 경우 다음 항목을 확인하십시오.

* 트리거가 Analytics에 대해 활성화되어 있습니다.
* 웹 사이트에서 MCID 및 Analytics가 사용되는 경우 DTM에서 사용 가능
* 트리거를 만드는 동안 올바른 Analytics 보고서 세트가 사용됩니다.

**트리거가 캠페인으로 수신됩니까?**

없을 경우, 파이프라인으로부터 트리거를 수신했는지 확인하십시오.

그렇지 않은 경우, Adobe에 연락하여 파이프라인 끝점의 구성을 확인하십시오.

해당하는 경우 다음 지침을 따르십시오.

* 캠페인 데이터 소스의 조정 ID 유형을 확인합니다.
* Customerid 데이터 소스는 고객 속성을 통해 만들어집니다.
* Datasource ID를 확인합니다.
* Adobe에서 Datasource 구성 후에 캠페인 인스턴스를 다시 시작하도록 요청합니다.
* 트리거 보고서에서 분석 문제를 트리거합니다.

**보류 중인 상태가 트리거입니까?**

그렇지 않다면 다음 단계로 이동하십시오. 해당하는 경우 다음 지침을 따르십시오.

* 트랜잭션 템플릿이 게시되었는지 확인합니다.
* Propensityscore 임계값이 캠페인에 대해 활성화된 경우, 파이프라인에서 트리거의 성향 점수를 확인하십시오.
* 프로파일이 차단되지 않았는지 확인합니다.
* 유형 규칙 적용을 확인하십시오.
* 트랜잭션 메시지 로그를 확인합니다.

**메시지가 유효합니까?**

메시지가 유효하지 않으면 다음 항목을 확인하십시오.

* 잘못된 것으로 표시된 오퍼 보강 개인화 필드에 대해 관련 Eventcusresource 컬렉션에서 트랜잭션 템플릿의 유효성을 확인합니다.
* 메시지 형식 유효성 검사

