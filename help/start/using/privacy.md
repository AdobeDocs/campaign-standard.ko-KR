---
title: Adobe Campaign Standard의 개인 정보 보호 및 동의
description: 이 섹션에서는 Adobe Campaign Standard의 개인 정보, 개인 데이터 및 동의 관리에 대한 개요와 이러한 정보를 처리하는 데 사용할 수 있는 도구에 대해 설명합니다.
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3
translation-type: tm+mt
source-git-commit: 7f0af4deeaf641e2aded9278b97eb498edd85d08
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 3%

---


# Privacy and Consent{#privacy-and-consent}

## 일반 추천 {#general-recommendations}

Adobe Campaign은 개인 정보와 민감한 데이터를 포함하여 매우 많은 양의 데이터를 수집하고 처리하기 위한 강력한 도구입니다. 따라서 개인 정보를 신중하게 관리해야 합니다.

* 항상 개인 정보를 책임감 있고 윤리적으로 활용하십시오.

* 요청하지 않은 이메일, 푸시 알림 및 SMS 메시지(&quot;스팸&quot;)를 보내지 마십시오. Adobe은 고객생애가치 및 충성도를 높이기 위한 마케팅 허가 원칙을 강력하게 믿고 있기 때문에 Adobe Campaign이 요청하지 않은 메시지를 보내는 것을 엄격히 금하고 있다.

### 개인 정보 보호 규정 {#privacy-regulations}

개인 정보를 올바로 처리하고 개인 데이터를 관리하려면, 귀하가 운영하는 지역에 적용되는 입법 내에서 작업하십시오. 다음과 같은 규정이 있습니다.
* [GDPR](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_en) (유럽 개인 정보 보호 규정)
* [DPA](https://www.gov.uk/data-protection) (영국의 GDPR 구현)
* [개인 정보 및 전자 통신에 대한 유럽 지침](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02002L0058-20091219)
* [CAN-SPAM Act](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business) (미국 법률에 상업용 이메일에 대한 규칙 및 요구 사항 설정)
* [CPA](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=) (California Consumer Privacy Act)
* [PDPA](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/) (태국 개인정보 보호법)

>[!NOTE]
>
>GDPR, CPA 및 PDPA가 Adobe Campaign에 적용되는 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../start/using/privacy-management.md#privacy-management-regulations).

### Adobe Experience Cloud privacy {#experience-cloud-privacy}

Adobe Campaign은 Adobe Experience Cloud 솔루션의 일부입니다. Campaign에서 개인 정보를 처리하는 방법은 다음과 같은 Adobe Experience Cloud 일반 원칙을 따릅니다.

* **Adobe Experience Cloud 사용 시 수집되는 정보**

   Adobe Experience Cloud 솔루션을 사용하는 회사는 수집할 정보를 선택하고 Adobe Experience Cloud 계정으로 보냅니다. 수집될 수 있는 정보의 유형에는 웹 검색 활동, IP 주소, 모바일 장치의 위치 정보, 캠페인 성공률, 장바구니에 구매 또는 배치된 항목 등이 있습니다.

   >[!NOTE]
   >
   >모든 Adobe 제품에 대해 Campaign은 앱 및 웹 사이트 사용자에 대한 정보를 수집합니다. 자세한 내용은 [Adobe 개인정보 보호 정책을 참조하십시오](https://www.adobe.com/privacy/policy.html).

* **Adobe Experience Cloud이 정보를 수집하는 방법**

   * Adobe Experience Cloud 솔루션은 사용자가 정보를 수집할 수 있도록 쿠키 및 웹 비콘(태그 또는 픽셀로도 알려져 있음)과 같은 유사한 기술을 사용합니다. Adobe Campaign의 쿠키 및 추적 기능에 대한 자세한 내용은 [이 섹션을 참조하십시오](#tracking-capabilities).
   * 또한 모바일 앱에서 Adobe Experience Cloud 기술을 사용할 수 있습니다. Campaign과 함께 모바일 게재 전송에 대한 자세한 내용은 [이 페이지를 참조하십시오](https://helpx.adobe.com/kr/campaign/kb/acs-mobile.html).

* **Adobe Experience Cloud 사용에 대한 사용자의 개인정보 보호 선택**

   Adobe은 고객에게 다음과 같은 내용을 설명하는 개인정보 보호 정책을 제공하도록 요구합니다.

   * Adobe Experience Cloud과 관련된 귀하의 개인정보 보호 방침
   * 사용자가 Adobe Experience Cloud과 관련하여 자신의 정보를 수집하거나 사용하는 것에 대한 환경 설정을 설정할 수 있는 방법

   >[!NOTE]
   >
   >모든 Adobe 제품의 경우 Campaign 사용자는 앱 및 웹 사이트를 통해 수집된 정보의 공유를 거부할 수 있습니다. 자세한 내용은 [Adobe Experience Cloud 사용 정보 FAQ를 참조하십시오](https://www.adobe.com/privacy/experience-cloud-usage-info-faq.html).

Adobe Experience Cloud 개인 정보에 대한 자세한 내용은 [이 페이지를 참조하십시오](https://www.adobe.com/privacy/marketing-cloud.html).

## 개인 데이터 및 개인 {#personal-data}

개인 정보 관리 시, 어떤 데이터를 관리 및 누구에게 처리할지를 정의하는 것이 중요합니다.
* **개인 데이터는** 살아있는 개인을 직접 또는 간접적으로 식별할 수 있는 정보입니다.
* **민감한 개인 데이터는** 노동 조합 회원뿐 아니라 개인의 인종, 정치적 관점, 종교적 신념, 범죄 배경, 유전자 정보, 건강 정보, 성적 선호도, 생체 인식 정보 등과 관련된 정보입니다.

기본 [규정](#privacy-regulations) 은 다음과 같이 데이터를 관리하는 서로 다른 개체를 의미합니다.
* 데이터 **컨트롤러는** 개인 데이터를 수집, 사용 및 공유하는 방법과 목적을 결정하는 기관입니다.
* 데이터 **프로세서는** 데이터 관리자의 지시에 따라 개인 데이터를 수집, 사용 또는 공유하는 개인 또는 당사자입니다.
* 데이터 **주체가** 개인 데이터를 수집, 사용 또는 공유하고 해당 개인 데이터를 참조해서 직접 또는 간접적으로 식별할 수 있는 살아있는 개인입니다.

따라서 개인 데이터를 수집 및 공유하는 회사는 데이터 관리자이며, 클라이언트는 데이터 주체이며, Adobe Campaign은 데이터 프로세서의 역할을 합니다. 개인정보 보호 요청을 관리할 때와 같이 데이터 주체와의 관계를 처리하는 것은 데이터 [관리자로서 귀하의 책임입니다](#privacy-requests).

대상 대상 서비스 [,](../../audiences/using/aep-about-audience-destinations-service.md)Adobe Analytics [,](../../integrating/using/about-campaign-analytics-integration.md)Audience Manager 또는 국민 핵심 서비스 [와 같이 대상을 다른 시스템으로 전송할 수 있는 다른 Experience Cloud 솔루션이나 Microsoft Dynamics 365와 같은 다른 솔루션과 Adobe Campaign을 통합하면](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)[](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)개인 데이터 보호를 위해 추가 비용을 지불해야 합니다.

## 데이터 수집 {#data-acquisition}

Adobe Campaign을 사용하면 개인 및 민감한 정보를 비롯한 데이터를 수집할 수 있습니다. 따라서 수신자로부터 동의를 받고 모니터링하는 것이 중요합니다.

* 항상 수신자가 커뮤니케이션 수신에 동의하도록 합니다. 이를 위해서는 옵트아웃 요청을 최대한 빨리 준수하고 이중 옵트인 프로세스를 통해 동의를 확인하십시오. 이에 대한 자세한 내용은 [캠페인에서 옵트인 및 옵트아웃 관리](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) 및 이중 옵트인 프로세스 [설정을 참조하십시오](../../channels/using/setting-up-a-double-opt-in-process.md).
* 사기성 목록을 가져오고 트랩을 사용하여 클라이언트 파일이 잘못 사용되고 있는지 확인하지 마십시오. 자세한 내용은 트랩 [사용을 참조하십시오](../../sending/using/using-traps.md).
* 동의 및 권한 관리를 통해 수신자의 환경 설정을 추적할 수 있을 뿐만 아니라 조직 내에서 누가 어떤 데이터에 액세스할 수 있는지를 관리할 수 있습니다. 자세한 내용은 [이 섹션](#consent)을 참조하십시오.
* 수신자의 개인 정보 보호 요청을 간편하게 관리하고 관리할 수 있습니다. 자세한 내용은 [이 섹션](#privacy-requests)을 참조하십시오.

## 개인 정보 관리 {#privacy-management}

개인 정보 관리는 개인 정보 보호 규정(GDPR, CPA 등)을 준수하는 데 도움이 되는 모든 프로세스 및 툴을 의미합니다. 이 [페이지에서 개인정보 관리 기능에 대한 개요를 살펴보십시오](../../start/using/privacy-management.md).

Adobe Campaign은 개인 정보 관리를 위한 다양한 기능을 제공합니다.
* 동의 관리, 데이터 유지 및 사용자 역할. [이 섹션](#consent)을 참조하십시오.
* 개인 정보 보호 요청(액세스 권한 및 잊혀질 권리). [이 섹션](#privacy-requests)을 참조하십시오.
* 개인 정보 판매 거부(CPA 특정). [이 섹션](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ccpa)을 참조하십시오.

Campaign의 주요 개인정보 보호 기능과 여기에 포함된 개인의 예가 나와 [있습니다](https://helpx.adobe.com/campaign/kb/campaign-privacy-more.html#gdprpersonasandflow).


### 동의, 보존 및 역할 {#consent}

원래 Adobe Campaign은 개인 정보에 필수적인 중요한 기능을 제공합니다.

* **동의 관리**:구독 관리 프로세스를 통해 수신자의 환경 설정을 관리하고 어떤 수신자가 구독 유형을 선택했는지 추적할 수 있습니다. 자세한 내용은 구독 및 [랜딩 페이지](../../audiences/using/about-subscriptions.md) 를 [참조하십시오](../../channels/using/getting-started-with-landing-pages.md).
* **데이터 유지**:모든 기본 제공 표준 로그 테이블에는 사전 설정된 보존 기간이 있으며 일반적으로 데이터 저장소를 6개월 이하로 제한합니다. 워크플로우로 추가 보존 기간을 설정할 수 있습니다. 자세한 내용은 Adobe 컨설턴트나 기술 관리자에게 문의하십시오.
* **권한 관리**:Adobe Campaign은 다양한 사전 빌드 또는 사용자 지정 역할을 통해 다양한 캠페인 운영자에게 할당된 권한을 관리할 수 있는 기능을 제공합니다. 이를 통해 회사 내에서 다른 유형의 데이터에 액세스하거나 수정하거나 내보낼 수 있는 사용자를 관리할 수 있습니다. 자세한 내용은 액세스 관리 [정보를 참조하십시오](../../administration/using/about-access-management.md).

이러한 기능과 Adobe Campaign에서 이러한 기능을 관리하는 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../start/using/privacy-management.md#consent-retention-roles).

### 개인 정보 요청 {#privacy-requests}

Adobe Campaign은 특정 개인 정보 보호 요청에 대해 데이터 컨트롤러로서 사용자의 준비를 용이하게 하는 데 도움이 되는 추가 기능을 제공합니다.

* 액세스 **권한** 은 데이터 주체가 데이터 주체의 확인을 통해 데이터 주체의 개인 데이터가 처리 중인지, 처리 장소 및 그 이유를 알 수 있는 권리입니다.

* 잊혀질 **권리** (요청 삭제)는 데이터 주체가 자신의 개인 데이터를 삭제하도록 권한을 부여합니다.

>[!NOTE]
>
>이 툴을 사용하면 GDPR, CPA 및 PDPA에 대한 개인 정보 보호 규정을 준수할 수 있습니다. 이러한 다른 규정에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../start/using/privacy-management.md#privacy-management-regulations).

<!--* **GDPR** (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

* **CCPA** (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

* **Thailand's PDPA** (Personal Data Protection Act) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.-->

**액세스** 및 **삭제** 요청이 [이 페이지에](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess)표시됩니다. 이러한 요청을 만드는 구현 단계는 [이 페이지에 자세히 설명되어 있습니다](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ManagingPrivacyRequests). Tutorials도 [여기에서](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/privacy/privacy-overview.html)이용 가능합니다.

## 추적 기능 {#tracking-capabilities}

Adobe Campaign은 추적 기능 덕분에 세션 쿠키와 영구 쿠키를 사용하여 배달 받는 사람의 행동을 추적할 수 있습니다. For more on tracking, see [this section](../../sending/using/tracking-messages.md).

>[!NOTE]
>
>개인 정보 보호 규정(GDPR)과 같은 규정에서는 회사가 쿠키를 설치하기 전에 웹 사이트 사용자의 계약을 요구하는 것을 명시합니다. 귀하는 인증 요청을 통해 사이트에 웹 추적 도구가 설치되어 있음을 사용자에게 알려야 합니다.

또한 메시지에 [추적된 링크](../../designing/using/links.md#about-tracked-urls) 를 추가하여 배달 및 수신자 동작의 영향을 [추적 지표](../../reporting/using/tracking-indicators.md) 기본 보고서에서 측정하거나 [전용 보고서를 만들 수도 있습니다](../../reporting/using/about-dynamic-reports.md).
