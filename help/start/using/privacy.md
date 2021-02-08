---
title: Adobe Campaign Standard의 개인 정보 및 동의
description: 이 섹션에서는 Adobe Campaign Standard의 개인 정보, 개인 데이터 및 동의 관리에 대한 개요를 제공하고 이러한 정보를 처리하는 데 사용할 수 있는 도구에 대해 설명합니다.
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3
translation-type: ht
source-git-commit: 2879066634a8a123ef5d07d46aa96479f156a923
workflow-type: ht
source-wordcount: '1479'
ht-degree: 100%

---


# 개인 정보 및 동의{#privacy-and-consent}

## 일반 권장 사항 {#general-recommendations}

Adobe Campaign은 개인 정보와 중요한 데이터를 포함한 많은 양의 데이터를 수집하고 처리할 수 있는 강력한 데이터 도구입니다. 따라서 개인 정보를 신중하게 관리해야 합니다.

* 항상 개인 정보를 책임감 있고 윤리적으로 사용하십시오.

* 요청하지 않은 이메일, 푸시 알림 및 SMS 메시지(&quot;스팸&quot;)를 보내지 마십시오. Adobe는 고객 생애의 가치 및 충성도를 향상하기 위해 허가 마케팅의 원칙을 강력하게 믿고 있습니다. 따라서 원치 않는 메시지 발송에 Adobe Campaign을 사용하는 것을 엄격히 금하고 있습니다.

### 개인 정보 보호 규정 {#privacy-regulations}

개인 정보를 올바로 처리하고 개인 데이터를 관리하기 위해 운영하는 지역에 적용되는 법규 내에서 작업하십시오. 다음과 같은 규정이 있습니다.
* [GDPR](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_en) (European General Data Protection Regulation)
* [DPA](https://www.gov.uk/data-protection) (UK’s implementation of GDPR)
* [개인 정보 및 전자 통신에 관한 유럽 지침](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02002L0058-20091219)
* [CAN-SPAM Act](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business) (상업용 이메일에 관한 규정 및 요구 사항에 설정된 미국 법)
* [CPA](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=) (California Consumer Privacy Act)
* [PDPA](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/) (Thailand Personal Data Protection Act)

>[!NOTE]
>
>GDPR, CPA 및 PDPA가 Adobe Campaign에 적용되는 방법에 대한 자세한 내용은 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html#whatisgdpr)를 참조하십시오.

### Adobe Experience Cloud 개인 정보 보호 {#experience-cloud-privacy}

Adobe Campaign은 Adobe Experience Cloud 솔루션의 일부입니다. Campaign에서 개인 정보를 처리하는 방식은 다음과 같은 Adobe Experience Cloud 일반 원칙을 따릅니다.

* **Adobe Experience Cloud 사용 시 수집되는 정보**

   Adobe Experience Cloud 솔루션을 사용하는 회사는 수집할 정보를 선택하고 Adobe Experience Cloud 계정으로 보냅니다. 수집할 수 있는 정보의 유형에는 웹 검색 활동, IP 주소, 모바일 디바이스의 위치 정보, 캠페인 성공률, 장바구니에서 구매 또는 장바구니로 배치된 항목 등이 있습니다.

   >[!NOTE]
   >
   >모든 Adobe 제품에 대해 Campaign은 앱 및 웹 사이트 사용자에 대한 정보를 수집합니다. 자세한 내용은 [Adobe 개인 정보 보호 정책](https://www.adobe.com/privacy/policy.html)을 참조하십시오.

* **Adobe Experience Cloud을 정보를 수집하는 데 사용하는 방법**

   * Adobe Experience Cloud 솔루션은 사용자가 정보를 수집할 수 있도록 쿠키 및 웹 비콘(태그 또는 픽셀로도 알려져 있음)과 같은 유사한 기술을 사용합니다. Adobe Campaign의 쿠키 및 추적 기능에 대한 자세한 내용은 [이 섹션](#tracking-capabilities)을 참조하십시오.
   * 또한 모바일 앱에서 Adobe Experience Cloud 기술을 사용할 수 있습니다. Campaign으로 모바일 게재 전송에 대한 자세한 내용은 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/acs-mobile.html)를 참조하십시오.

* **Adobe Experience Cloud 사용에 대한 사용자의 개인 정보 보호 선택**

   Adobe는 고객에게 다음과 같은 내용을 설명하는 개인 정보 보호 정책을 제공하도록 요구합니다.

   * Adobe Experience Cloud과 관련된 개인 정보 보호 사례
   * 사용자가 Adobe Experience Cloud과 관련하여 자신의 정보를 수집하거나 사용하는 것에 대한 환경 설정을 하는 방법

   >[!NOTE]
   >
   >모든 Adobe 제품에서 Campaign 사용자는 앱 및 웹 사이트를 통해 수집된 정보의 공유를 옵트아웃할 수 있습니다. 자세한 내용은 [Adobe Experience Cloud 사용 정보 FAQ](https://www.adobe.com/privacy/experience-cloud-usage-info-faq.html)를 참조하십시오.

Adobe Experience Cloud 개인 정보 보호에 대한 자세한 내용은 [이 페이지](https://www.adobe.com/privacy/marketing-cloud.html)를 참조하십시오.

## 개인 데이터 및 가상 사용자 {#personal-data}

개인 정보 관리 시 누가 어떤 데이터를 주의 깊게 처리할지를 정의하는 것이 중요합니다.
* **개인 데이터**&#x200B;는 살아있는 개인을 직접 또는 간접적으로 식별할 수 있는 정보입니다.
* **중요한 개인 데이터**&#x200B;는 노동조합 멤버십뿐 아니라 개인의 인종, 정치적 관점, 종교적 신념, 범죄 기록, 유전자 정보, 건강 정보, 성적 선호도, 생체 인식 정보 등과 관련된 정보입니다.

[기본 규정](#privacy-regulations)은 다음과 같이 데이터를 관리하는 서로 다른 엔터티를 의미합니다.
* **데이터 컨트롤러**&#x200B;는 개인 데이터를 수집, 사용 및 공유하는 방법과 목적을 결정하는 인증 기관입니다.
* **데이터 프로세서**&#x200B;는 데이터 컨트롤러의 지시에 따라 개인 데이터를 수집, 사용 또는 공유하는 개인 또는 주체입니다.
* **데이터 주체**&#x200B;는 개인 데이터를 수집, 사용 또는 공유하며 해당 개인 데이터를 참조해서 직접 또는 간접적으로 식별할 수 있는 살아있는 개인입니다.

따라서 개인 데이터를 수집 및 공유하는 회사는 데이터 컨트롤러이며 클라이언트는 데이터 주체이고 Adobe Campaign은 데이터 프로세서의 역할을 합니다. [개인 정보 보호 요청](#privacy-requests)을 관리할 때와 같이 데이터 주체와의 관계를 처리하는 것은 데이터 컨트롤러로서의 책임입니다.

[대상자 대상 서비스](../../audiences/using/aep-about-audience-destinations-service.md), [Adobe Analytics](../../integrating/using/about-campaign-analytics-integration.md), [Audience Manager 또는 People 핵심 서비스](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)와 같이 대상을 다른 시스템으로 전송할 수 있는 다른 Experience Cloud 솔루션이나 [Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md)와 같은 다른 솔루션과 Campaign을 통합하면 개인 데이터 보호를 위해 추가 비용을 지불해야 합니다.

## 데이터 획득 {#data-acquisition}

Adobe Campaign을 사용하면 개인 및 중요한 정보를 포함한 데이터를 수집할 수 있습니다. 따라서 수신자로부터 동의를 받고 모니터링하는 것이 중요합니다.

* 항상 수신자가 커뮤니케이션 수신에 동의하도록 합니다. 이를 위해서는 옵트아웃 요청을 최대한 빨리 준수하고 이중 옵트인 프로세스를 통해 동의를 확인하십시오. 이에 대한 자세한 내용은 [Campaign에서 옵트인 및 옵트아웃 관리](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) 및 이중 옵트인 프로세스 설정[을 참조하십시오](../../channels/using/setting-up-a-double-opt-in-process.md).
* 클라이언트 파일이 사기성으로 사용되지 않고 있음을 확인하기 위해 허위 파일을 가져와서 트랩으로 사용하지 마십시오. 자세한 내용은 [트랩 사용](../../sending/using/using-traps.md)을 참조하십시오.
* 동의 및 권한 관리를 통해 수신자의 환경 설정을 추적할 수 있을 뿐만 아니라 조직 내에서 누가 어떤 데이터에 액세스할 수 있는지를 관리할 수 있습니다. 자세한 내용은 [이 섹션](#consent)을 참조하십시오.
* 수신자의 개인 정보 보호 요청을 간편하게 지원하고 관리할 수 있습니다. 자세한 내용은 [이 섹션](#privacy-requests)을 참조하십시오.

## 개인 정보 관리 {#privacy-management}

개인 정보 관리는 개인 정보 보호 규정(GDPR, CPA 등)을 준수하는 데 도움이 되는 모든 프로세스 및 도구를 의미합니다. [이 페이지](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html)에서 개인 정보 관리 기능에 대한 개요를 살펴보십시오.

Adobe Campaign은 개인 정보 관리를 위한 다양한 기능을 제공합니다.
* 동의 관리, 데이터 보존 및 사용자 역할. [이 섹션](#consent)을 참조하십시오.
* 개인 정보 보호 요청(액세스 권한 및 잊혀질 권리). [이 섹션](#privacy-requests)을 참조하십시오.
* 개인 정보 판매 옵트아웃 (CCPA-특정). [이 섹션](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ccpa)을 참조하십시오.

Campaign의 주요 개인 정보 보호 기능과 관련된 개인의 예가 [이 섹션](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-faq.html?lang=ko#getting-started)에 나와 있습니다.


### 동의, 보존 및 역할 {#consent}

기본적으로 Adobe Campaign은 다음과 같은 개인 정보에 필수적인 중요한 기능을 제공합니다.

* **동의 관리**: 구독 관리 프로세스를 통해 수신자의 환경 설정을 관리하고 어떤 수신자가 어떤 구독 유형을 옵트인했는지 추적할 수 있습니다. 자세한 내용은 [구독](../../audiences/using/about-subscriptions.md) 및 [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md)를 참조하십시오.
* **데이터 보존**: 모든 기본 제공 표준 로그 테이블에는 사전 설정된 보존 기간이 있으며 일반적으로 데이터 저장소를 6개월 이하로 제한합니다. 워크플로우로 추가 보존 기간을 설정할 수 있습니다. 자세한 내용은 Adobe 컨설턴트나 기술 관리자에게 문의하십시오.
* **권한 관리**: Adobe Campaign은 다양한 사전 설치 또는 사용자 지정 역할을 통해 다양한 캠페인 운영자에게 할당된 권한을 관리할 수 있는 기능을 제공합니다. 이를 통해 회사 내에서 다른 유형의 데이터에 액세스, 수정 또는 내보낼 수 있는 사용자를 관리할 수 있습니다. 자세한 내용은 [액세스 관리 정보](../../administration/using/about-access-management.md)를 참조하십시오.

이러한 기능과 Adobe Campaign에서 관리하는 방법에 대한 자세한 내용은 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html#consent)를 참조하십시오.

### 개인 정보 보호 요청 {#privacy-requests}

Adobe Campaign은 특정 개인 정보 보호 요청에 대해 데이터 컨트롤러로서 사용자의 준비를 용이하게 하는 데 도움이 되는 추가 기능을 제공합니다.

* **액세스 권한**&#x200B;은 데이터 주체가 데이터 주체의 확인을 통해 데이터 주체의 개인 데이터가 처리 중인지 여부, 처리 장소 및 그 이유를 알 수 있는 권리입니다.

* **잊혀질 권리**(삭제 요청)는 데이터 주체가 자신의 개인 데이터를 삭제하도록 권한을 부여합니다.

>[!NOTE]
>
>이 도구를 사용하면 GDPR, CPA 및 PDPA에 대한 개인 정보 보호 규정을 준수할 수 있습니다. 이러한 다른 규정에 대한 자세한 내용은 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/campaign-privacy-overview.html#whatisgdpr)를 참조하십시오.

<!--* **GDPR** (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

* **CCPA** (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

* **Thailand's PDPA** (Personal Data Protection Act) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.-->

**액세스** 및 **삭제** 요청이 [이 페이지](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=ko#getting-started)에 표시됩니다. 이러한 요청을 만드는 구현 단계는 [이 페이지](https://helpx.adobe.com/kr/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)에 자세히 설명되어 있습니다. 튜토리얼도 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/privacy-overview.html?lang=ko#privacy)에서 사용 가능합니다.

## 추적 기능 {#tracking-capabilities}

Adobe Campaign은 추적 기능 덕분에 세션 쿠키와 영구 쿠키를 사용하여 게재 수신자의 행동을 추적할 수 있습니다. 추적에 대한 자세한 내용은 [이 페이지](../../sending/using/tracking-messages.md)를 참조하십시오.

>[!NOTE]
>
>GDPR(General Data Protection Regulation)과 같은 규정에서는 회사가 쿠키를 설치하기 전에 웹 사이트 사용자의 계약을 요구하는 것을 명시합니다. 인증 요청을 통해 사이트에 웹 추적 도구가 설치되어 있음을 사용자에게 알려야 합니다.

또한 메시지에 [추적된 링크](../../designing/using/links.md#about-tracked-urls)를 추가하여 게재 및 수신자 행동의 영향을 [추적 지표](../../reporting/using/tracking-indicators.md) 기본 보고서에서 측정하거나 [전용 보고서](../../reporting/using/about-dynamic-reports.md)를 만들 수도 있습니다.
