---
title: Experience Cloud 트리거 구성
description: '이전 행동을 바탕으로 고객에게 개인화된 전달을 전송하도록 Adobe Experience Cloud 트리거 통합을 구성하는 방법을 살펴볼 수 있습니다. '
page-status-flag: never-activated
uuid: 8fd7b804-9528-46a5-a060-bf16b8dc555d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
discoiquuid: 4163dc0c-8103-4425-b8bf-7aa45c4d3a06
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: bd74905985734412b4fb11ad11d70faf9fcc9ca6
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 1%

---


# Experience Cloud 트리거 구성{#configuring-triggers-in-experience-cloud}

## 기능 활성화 {#activating-the-functionality}

기능은 Adobe에서 Adobe Campaign에서 활성화해야 합니다. Adobe 계정 담당자 또는 전문 서비스 파트너에게 문의하십시오.

Adobe 팀은 트리거를 활성화하려면 다음 정보가 필요합니다.

* Marketing Cloud 회사 이름
* IMS 조직 ID
* Analytics 로그인 회사(Marketing Cloud 회사 이름과 같을 수 있음)

## 솔루션 및 서비스 구성 {#configuring-solutions-and-services}

이 기능을 사용하려면 다음 솔루션/핵심 서비스에 액세스해야 합니다.

* Adobe Campaign
* Adobe Analytics Ultimate, Premium, Foundation, OD, Select, Prime, Mobile Apps, Select 또는 Standard.
* Experience Cloud 트리거 핵심 서비스

   ![](assets/trigger_uc_prereq_1.png)

* Experience Cloud DTM 핵심 서비스

   ![](assets/trigger_uc_prereq_2.png)

* Experience Cloud 방문자 ID 및 Experience Cloud 사용자 코어 서비스

   ![](assets/trigger_uc_prereq_3.png)

또한 작업 웹 사이트가 필요합니다.

![](assets/trigger_uc_prereq_4.png)

>[!CAUTION]
>
>하위 도메인 위임은 배달 가능 키 요소입니다. Adobe Campaign 이메일이 웹 사이트에서 사용하는 이메일과 동일한 도메인에서 전송되었는지 확인합니다.

이러한 사용 사례를 실행하려면 [Experience Cloud DTM 코어 서비스](#configuring-experience-cloud-dtm-core-service), [Experience Cloud 사용자 코어 서비스](#configuring-experience-cloud-people-core-service) 및 [캠페인](#configuring-triggers-and-aliases-in-campaign) 을 구성해야합니다.

### Experience Cloud DTM 핵심 서비스 구성 {#configuring-experience-cloud-dtm-core-service}

1. Experience Cloud DTM 핵심 서비스(다이내믹 태그 관리)에서 웹 사이트 페이지에 대한 Experience Cloud ID 및 Adobe Analytics을 활성화합니다.

   ![](assets/trigger_uc_conf_1.png)

1. 웹 사이트, Adobe Analytics 및 Adobe Campaign 간의 ID 조정을 사용하려면 앨리어스를 사용해야 합니다. 예를 들어 &quot;visitorid&quot;라는 별칭을 만듭니다.

   ![](assets/trigger_uc_conf_2.png)

### Experience Cloud 사용자 핵심 서비스 구성 {#configuring-experience-cloud-people-core-service}

DTM에서 이전에 참조한 별칭은 고객 속성을 통해 Experience Cloud 사용자 핵심 서비스에서 만들어야 합니다. 새 DTM 별칭을 만들고 통합 코드에 동일한 DTM 별칭을 참조해야 합니다(예: &quot;visitorid&quot;).

![](assets/trigger_uc_conf_3.png)

>[!NOTE]
>
>Adobe Campaign의 데이터 소스에서 이 고객 속성을 사용합니다(다음 단계).

### 캠페인에서 트리거 및 별칭 구성 {#configuring-triggers-and-aliases-in-campaign}

1. Adobe Campaign Standard 인스턴스에 **[!UICONTROL Experience Cloud triggers]** 표시되는지 확인하십시오. 그렇지 않은 경우 Adobe Campaign 관리자에게 문의하십시오.

   ![](assets/remarketing_1.png)

1. 별칭을 사용하면 Analytics의 담당자가 Campaign의 프로필과 대사될 수 있습니다. Experience Cloud ID 서비스에 정의된 별칭을 캠페인의 공유 데이터 소스와 일치해야 합니다. 데이터 소스( **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Shared Data Sources]** )를 통해 Adobe Campaign에서 별칭 해상도를 구성해야 합니다. 이전 단계에서 만든 동일한 고객 속성 데이터 소스와 매핑되는 **[!UICONTROL Data Source/Alias]** 드롭다운 메뉴에서 올바른 데이터 소스를 선택해야 합니다.

   ![](assets/trigger_uc_conf_5.png)

   >[!NOTE]
   >
   >익명 사용자와 로그인한 사용자 모두에 대해 트리거를 조정할 수 있습니다. 익명의 사용자의 경우 프로필은 Adobe Campaign에 존재해야 하며 이전에 사용자에게 이메일을 보냈습니다. 이 경우 방문자 ID 구성이 충분합니다. 그러나 로그인한 사용자에 대한 트리거를 대사하려면 선언된 ID 데이터 소스를 설정해야 합니다. 자세한 내용은 [데이터 소스 구성을 참조하십시오](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-2--configure-the-data-sources).

## Experience Cloud 인터페이스에서 트리거 만들기 {#creating-a-trigger-in-the-experience-cloud-interface}

Adobe Experience Cloud 트리거를 만들어 Campaign에서 사용할 수 있어야 합니다.

Experience Cloud에서 새 트리거를 만들고 웹 사이트에서 사용되는 보고서 세트를 선택해야 합니다. 트리거가 실행되도록 적절한 차원을 선택해야 합니다.

Adobe [Experience Cloud 설명서를](https://docs.adobe.com/content/help/en/core-services/interface/activation/triggers.html) 참조하여 이 [비디오를 시청하십시오](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two).

## 모범 사례 및 제한 사항 트리거 {#triggers-best-practices-and-limitations}

다음은 캠페인 - 트리거 통합 사용에 대한 우수 사례 및 제한 사항의 목록입니다.

* Campaign Standard 인스턴스가 여러 개 있는 경우 트리거가 동일한 IMS 조직 ID에 있는 한 모든 인스턴스에서 수신될 수 있습니다. Analytics은 동일한 IMS 조직 ID여야 합니다.
* 두 개의 다른 보고서 세트의 이벤트를 사용하여 트리거 코어 서비스에 트리거를 만들 수 없습니다.
* 트리거는 트랜잭션 메시지를 기반으로 합니다. 트랜잭션 메시지는 메시지를 매우 빠르게 보내야 할 때마다 사용됩니다. 트랜잭션 메시지를 대기열에 넣은 다음 일괄적으로 루프할 수 없습니다.
* 트리거는 자연에서 결정적이지 않다. 트리거가 생성되면 쿠키와 연관된 모든 별칭을 전송하므로 소매 키오스크, 라이브러리, 사이버 카페 또는 집에서 공유 장치(동일한 장치에서 남편과 아내가 로그인)와 같은 공유 브라우저의 경우 올바른 ID에 매핑할 수 없습니다. 브라우저로 로그인하는 데 사용되는 모든 ID가 Campaign으로 전송되어 첫 번째 조정을 기반으로 메시지를 보냅니다. 조정할 수 있는 &quot;이메일 ID&quot;가 여러 개 있는 경우 Campaign은 이메일을 보내지 않습니다. Analytics에서 캡처 및 보내지 않는 한 Campaign이 올바른 이메일 ID를 알 수 있는 방법은 없습니다.
* Campaign에 페이로드 컨텐츠를 저장할 수 없습니다. 트리거는 프로필 데이터를 업데이트하는 데 사용할 수 없습니다.
* 고객 속성은 트리거에서 지원되지 않습니다(즉, 보고서 세트 데이터만 트리거 비즈니스 규칙을 정의하는 데 사용할 수 있음).
* 컬렉션 컬렉션은 Campaign에서 지원되지 않습니다.

>[!CAUTION]
>
>웹 사이트가 Adobe Campaign 서버와 동일한 도메인에서 실행되고 있어야 합니다. 그렇지 않은 경우 방문자 ID를 사용하여 조정하거나 익명으로 웹 사이트를 방문하는 사용자에게 연락할 수 없습니다.

