---
title: Adobe Campaign Standard의 개인 정보 관리
description: 개인 정보 관리를 위한 Adobe Campaign Standard 기능에 대한 자세한 내용을 알아봅니다.
audience: start
content-type: reference
topic-tags: discovering-the-interface
feature: Privacy
role: User
level: Intermediate
exl-id: 84cf8f6e-9ba0-4cd5-80e2-a61cefa31e0a
source-git-commit: ede4bd97ffddca4a5e24f1e4114d50ca5140a01d
workflow-type: ht
source-wordcount: '827'
ht-degree: 100%

---

# 개인 정보 보호 관리 {#privacy-management}

Adobe Campaign은 GDPR, CCPA, PDPA 및 LGPD와 같은 [개인 정보 보호 규정](#privacy-management-regulations)을 준수하는 데 도움이 되는 다양한 도구를 제공합니다.

Adobe Campaign이 GDPR 및 기타 개인 정보 보호 규정을 준수하도록 보장하는 5가지 주요 기능은 다음과 같습니다.

![](assets/privacy-gdpr-use-cases.png)

* **액세스 권한**

* **삭제 권한**

자세한 내용은 [액세스 권한 및 잊혀질 권리](#right-access-forgotten)를 참조하십시오.

* **동의 관리**

* **데이터 유지**

* **권한 관리**

자세한 내용은 [동의, 보존 및 역할](#consent-retention-roles)을 참조하십시오.

<!--This section presents general information on what Privacy management is and the features provided by Adobe Campaign to manage the [Right to Access and Right to be Forgotten](#right-access-forgotten).

It also contains information on important features to manage Privacy ([consent, data retention and user roles](#consent-retention-roles)), as well as best practices to help you with your Privacy compliance when using Adobe Campaign.-->

## 개인 정보 관리에 관한 규정 {#privacy-management-regulations}

Adobe Campaign의 기능은 다음과 같은 규정을 준수하는 데 도움이 됩니다.

* **GDPR**([General Data Protection Regulation](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_en))은 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 개인 정보 보호법입니다. 다음의 링크를 통해 GDPR에 대한 일반적인 정보를 확인하십시오.

   * https://www.adobe.com/kr/privacy/general-data-protection-regulation.html
   * https://www.adobe.com/marketing-cloud/campaign/general-data-protection-regulation.html

* **CCPA**([California Consumer Privacy Act](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=))는 캘리포니아 거주자들에게 개인 정보에 대한 새로운 권리를 제공하고 캘리포니아에서 비즈니스를 수행하는 특정 엔터티에 데이터 보호 책임을 부과합니다.
* **PDPA**([Personal Data Protection Act](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/))은 태국에 대한 데이터 보호 요구 사항을 통합하고 현대화한 새로운 개인 정보 보호법입니다.
* **LGPD** ([Lei Geral de Proteção de Dados](https://iapp.org/media/pdf/resource_center/Brazilian_General_Data_Protection_Law.pdf))는 2021년 초부터 브라질에서 개인 데이터를 수집하거나 처리하는 모든 회사에 대해 효력을 발휘합니다.

이러한 모든 규정은 위에 언급된 각 지역 또는 국가(유럽 연합, 캘리포니아, 태국, 브라질)에 있는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다.

>[!NOTE]
>
>개인 데이터 및 데이터를 관리하는 다양한 엔터티(데이터 컨트롤러, 데이터 프로세서 및 데이터 주체)에 대한 자세한 내용은 [개인 데이터 및 가상 사용자를 참조하십시오](../../start/using/privacy.md#personal-data).

## 액세스 권리 및 잊혀질 권리 {#right-access-forgotten}

Adobe Campaign을 사용하면 개인정보 보호 준비를 원활히 수행할 수 있도록 **액세스** 및 **삭제** 요청을 처리할 수 있습니다 .

* **액세스 권한**&#x200B;은 데이터 주체가 데이터 주체의 확인을 통해 데이터 주체의 개인 데이터가 처리 중인지 여부, 처리 장소 및 목적을 알 수 있는 권리입니다. 데이터 컨트롤러는 개인 데이터의 사본을 무료로 전자 형식으로 제공해야 합니다.

* 데이터 삭제라고도 하는 **잊혀질 권리**(삭제 요청)는 데이터 주체에게 자신의 개인 데이터를 지우고, 데이터의 추가 배포를 중단하고, 제3자로 하여금 데이터 처리를 중단하도록 할 수 있는 권한을 부여합니다.

**액세스** 및 **삭제** 요청을 만드는 방법과 Adobe Campaign에서 이 요청을 처리하는 원리는 [구현 단계](../../start/using/privacy-requests.md#about-privacy-requests)를 참조하세요.

Campaign Standard의 개인 정보 관리에 대한 튜토리얼도 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/privacy-overview.html?lang=ko#privacy)에서 사용할 수 있습니다.

>[!NOTE]
>
>개인 데이터 및 데이터를 관리하는 다른 엔터티(데이터 컨트롤러, 데이터 프로세서 및 데이터 주체)에 대한 자세한 내용은 [개인 데이터 및 가상 사용자를 참조하십시오](../../start/using/privacy.md#personal-data).

## 동의, 보존 및 역할 {#consent-retention-roles}

Adobe Campaign은 최신 **액세스 권한** 및 **잊혀질 권리** 기능 외에도 다음과 같이 개인 정보 보호에 필수적인 기타 중요한 기능을 제공합니다.

* [동의 관리](#consent-management): 기본 설정 관리를 위한 구독 기능
* [데이터 보존](../../administration/using/data-retention.md): 모든 표준 로그 테이블의 데이터 보존 기간, 워크플로우로 추가 보존 기간을 설정할 수 있습니다.
* [권한 관리](#rights-management): 명명된 권한에 의해 관리되는 데이터 액세스

### 동의 관리 {#consent-management}

동의는 데이터 주체와 관련된 개인 데이터를 처리하는 데이터 주체의 동의를 의미합니다. 해당 처리에 필요한 동의를 얻는 것은 데이터 컨트롤러의 책임입니다. Adobe Campaign은 고객이 서비스와 관련된 동의를 관리하는 데 도움이 되는 일부 기능을 제공할 수 있지만, Adobe는 동의에 대한 책임이 없습니다. 고객은 자신의 법률 부서와 협력하여 필요한 동의에 대해 고유한 프로세스와 방침을 결정해야 합니다.

일부 동의 내용의 관리를 돕는 기능은 초기부터 Adobe Campaign의 핵심이었습니다. 구독 관리 프로세스를 통해 고객은 어떤 수신자가 뉴스레터, 일별 또는 주별 홍보, 기타 마케팅 프로그램 등 어떤 유형의 구독 유형을 옵트인했는지 추적할 수 있습니다.

![](assets/privacy-consent-management.png)

동의 관리에 대한 자세한 내용은 [구독 정보](../../audiences/using/about-subscriptions.md) 및 [랜딩 페이지 시작](../../channels/using/getting-started-with-landing-pages.md)을 참조하십시오.

Adobe Campaign이 제공하는 동의 관리 도구 외에도, 개인 정보 판매를 고객이 옵트아웃했는지 여부를 추적할 수 있습니다. [이 섹션](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa)을 참조하십시오.

### 권한 관리 {#rights-management}

Adobe Campaign은 다양한 사전 설치 또는 사용자 지정 역할을 통해 다양한 Campaign 운영자에게 할당된 권한을 관리하는 기능을 제공합니다.

한 가지 이점은 회사 내에서 다른 유형의 데이터에 액세스할 수 있는 사용자를 관리할 수 있다는 점입니다. 예를 들어 서로 다른 지역에 대해 서로 다른 마케터가 있고 각 마케터는 해당 지역의 데이터만 액세스할 수 있습니다.

마찬가지로, 이 기능을 사용하면 게재를 보낼 수 있는 사용자를 제한하고, 개인 정보 관리와 관련해서는 누가 데이터를 수정하거나 내보내내는지 제한할 수 있는 등, 각 사용자에 대해 서로 다른 기능을 구성할 수 있습니다.

![](assets/privacy-user-management.png)

액세스 관리에 대한 자세한 내용은 [이 섹션](../../administration/using/about-access-management.md)을 참조하십시오.
