---
title: Experience Cloud에서 Triggers 구성
description: Adobe Experience Cloud Triggers 통합을 구성하여 이전 동작을 기반으로 고객에게 개인화된 게재 전송을 시작하는 방법에 대해 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 50e9fb7a-b28a-40b0-9f2c-3673c792529a
source-git-commit: 5a7e48da3d62b186f96cd7451fb5a7b2cf94e09c
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 7%

---

# Experience Cloud에서 Triggers 구성{#configuring-triggers-in-experience-cloud}

## 기능 활성화 {#activating-the-functionality}

기능은 Adobe Campaign에서 Adobe으로 활성화해야 합니다. Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오.

트리거를 활성화하려면 Adobe 팀에 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* 조직 ID
* Analytics 로그인 회사(Marketing Cloud 회사 이름과 같을 수 있음)

## 솔루션 및 서비스 구성 {#configuring-solutions-and-services}

이 기능을 사용하려면 다음 솔루션/핵심 서비스에 액세스할 수 있어야 합니다.

* Adobe Campaign
* Adobe Analytics Ultimate, Premium, Foundation, OD, Select, Prime, Mobile Apps, Select 또는 Standard.
* Experience Cloud 트리거 핵심 서비스

   ![](assets/trigger_uc_prereq_1.png)

* Experience Cloud DTM 핵심 서비스

   ![](assets/trigger_uc_prereq_2.png)

* Experience Cloud 방문자 ID 및 Experience Cloud People 핵심 서비스

   ![](assets/trigger_uc_prereq_3.png)

또한 작동하는 웹사이트가 필요합니다.

![](assets/trigger_uc_prereq_4.png)

>[!CAUTION]
>
>하위 도메인 구성은 게재 가능성 키 요소입니다. Adobe Campaign 이메일이 웹 사이트에서 사용하는 도메인과 동일한 도메인에서 전송되었는지 확인합니다.

다음을 구성해야 합니다. [DTM 핵심 서비스 Experience Cloud](#configuring-experience-cloud-dtm-core-service), [Experience Cloud 사용자 핵심 서비스](#configuring-experience-cloud-people-core-service) 및 [캠페인](#configuring-triggers-and-aliases-in-campaign) 을 클릭하여 이러한 사용 사례를 실행합니다.

### Experience Cloud DTM 핵심 서비스 구성 {#configuring-experience-cloud-dtm-core-service}

1. DTM 코어 서비스(Dynamic Tag Management) Experience Cloud에서 웹 사이트 페이지에 대한 Experience Cloud ID 및 Adobe Analytics을 활성화합니다.

   ![](assets/trigger_uc_conf_1.png)

1. 웹 사이트, Adobe Analytics 및 Adobe Campaign 간의 ID 조정에는 앨리어싱을 사용해야 합니다. 예를 들어 &quot;visitorid&quot;라는 별칭을 만듭니다.

   ![](assets/trigger_uc_conf_2.png)

### Experience Cloud 사용자 핵심 서비스 구성 {#configuring-experience-cloud-people-core-service}

이전에 DTM에서 참조한 별칭은 고객 속성을 통해 Experience Cloud People 핵심 서비스에서 생성해야 합니다. 새 별칭을 만들고 통합 코드에서 동일한 DTM 별칭(예: &quot;visitorid&quot;)을 참조해야 합니다.

![](assets/trigger_uc_conf_3.png)

>[!NOTE]
>
>Adobe Campaign의 데이터 소스에서 이 고객 속성을 사용합니다(다음 단계).

### Campaign에서 트리거 및 별칭 구성 {#configuring-triggers-and-aliases-in-campaign}

1. 다음을 수행했는지 확인하십시오. **[!UICONTROL Experience Cloud triggers]** Adobe Campaign Standard 인스턴스에 표시됩니다. 그렇지 않은 경우 Adobe Campaign 관리자에게 문의하십시오.

   ![](assets/remarketing_1.png)

1. 별칭을 사용하면 Analytics의 연락처가 Campaign의 프로필과 조정될 수 있습니다. Experience Cloud ID 서비스에 정의된 별칭을 Campaign의 공유 데이터 소스와 일치시켜야 합니다. 데이터 소스( )를 통해 Adobe Campaign에서 별칭 확인을 구성해야 합니다. **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Shared Data Sources]** ). 에서 올바른 데이터 소스를 선택했는지 확인합니다. **[!UICONTROL Data Source/Alias]** 드롭다운 메뉴 - 이전 단계에서 만든 것과 동일한 고객 속성 데이터 소스와 매핑됩니다.

   ![](assets/trigger_uc_conf_5.png)

   >[!NOTE]
   >
   >익명 사용자와 로그인한 사용자 모두에 대해 트리거를 조정할 수 있습니다. 익명 사용자의 경우 프로필이 Adobe Campaign에 있어야 하며 이전에 사용자에게 이메일이 전송되었습니다. 이 경우 방문자 ID 구성이면 충분합니다. 그러나 로그인한 사용자에 대한 트리거를 조정하려면 선언된 ID 데이터 소스를 설정해야 합니다. 자세한 내용은 다음을 참조하십시오. [데이터 소스 구성](../../integrating/using/integration-with-audience-manager-or-people-core-service.md#step-2--configure-the-data-sources).

## Experience Cloud 인터페이스에서 트리거 만들기 {#creating-a-trigger-in-the-experience-cloud-interface}

Campaign에서 사용할 수 있도록 Adobe Experience Cloud 트리거를 만들어야 합니다.

Experience Cloud에서 새 트리거를 만들고 웹 사이트에서 사용되는 보고서 세트를 선택해야 합니다. 트리거가 실행될 수 있도록 올바른 차원을 선택해야 합니다.

다음을 참조하십시오. [Adobe Experience Cloud 설명서](https://experienceleague.adobe.com/docs/core-services/interface/activation/triggers.html) 그리고 이걸 봐 [비디오](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two).

## 모범 사례 및 제한 사항 트리거 {#triggers-best-practices-and-limitations}

다음은 Campaign - 트리거 통합 사용에 대한 우수 사례 및 제한 사항 목록입니다.

* Campaign Standard 인스턴스가 여러 개 있는 경우 트리거는 동일한 조직에 있는 한 모든 인스턴스에서 받을 수 있습니다. Analytics도 동일한 조직에 있어야 합니다.
* 트리거 핵심 서비스에서는 두 개의 서로 다른 보고서 세트의 이벤트를 사용하여 트리거를 만들 수 없습니다.
* 트리거는 트랜잭션 메시지를 기반으로 합니다. 트랜잭션 메시지는 메시지를 매우 빠르게 보내야 할 때마다 사용됩니다. 트랜잭션 메시지를 대기열에 넣은 다음 일괄적으로 반복할 수 없습니다.
* 유발인자는 기본적으로 결정적이지 않습니다. 트리거가 생성되면 쿠키와 관련된 모든 별칭을 전송하므로 소매 키오스크, 라이브러리, 사이버 카페 또는 집의 공유 디바이스(남편과 아내가 동일한 디바이스에서 로그인)와 같은 공유 브라우저의 경우 올바른 ID에 매핑할 수 없습니다. 브라우저로 로그인하는 데 사용되는 모든 ID는 첫 번째 조정에 따라 메시지를 보내는 Campaign으로 전송됩니다. 조정에 적합한 &quot;이메일 ID&quot;가 여러 개 있는 경우 Campaign에서 이메일을 보내지 않습니다. Analytics에서 ID를 캡처하여 보내지 않으면 Campaign에서 올바른 이메일 ID가 무엇인지 알 수 없습니다.
* Campaign에는 페이로드의 콘텐츠를 저장할 수 없습니다. 트리거를 사용하여 프로필의 데이터를 업데이트할 수 없습니다.
* 고객 속성은 트리거에서 지원되지 않습니다(즉, 보고서 세트 데이터만 트리거 비즈니스 규칙을 정의하는 데 사용할 수 있음).
* 컬렉션은 Campaign에서 지원되지 않습니다.

>[!CAUTION]
>
>웹 사이트가 Adobe Campaign 서버와 동일한 도메인에서 실행되고 있어야 합니다. 그렇지 않으면 방문자 ID를 사용하여 조정하고 웹 사이트를 방문하는 사용자에게 익명으로 연락할 수 없습니다.
