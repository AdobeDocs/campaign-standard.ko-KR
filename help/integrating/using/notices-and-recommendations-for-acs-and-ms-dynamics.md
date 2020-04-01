---
title: '"Campaign Standard 및 Microsoft Dynamics 365 작업:알림 및 추천"'
description: Campaign Standard 및 Microsoft Dynamics 365를 사용하여 작업하는 방법에 대한 알림 및 권장 사항 알아보기
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 620be6615d162672948c3dccdae2752b8c999c47

---


# Campaign Standard 및 Microsoft Dynamics 365를 사용한 작업:알림 및 추천

## 지역 지원

이 통합은 북미, EMEA 및 APAC 지역에서 사용할 수 있습니다.

EMEA 또는 APAC 지역에 거주하는 경우 이 통합의 일부로 일부 데이터가 미국에서 처리됩니다. For more information, refer to [this section](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## 단방향 연락처 동기화를 위한 진실

연락처 및 사용자 지정 엔티티 동기화에서 Dynamics 365를 진실의 소스로 처리합니다. 동기화된 속성에 대한 모든 변경 사항은 Adobe Campaign Standard가 아니라 Microsoft Dynamics 365에서 수행해야 합니다. 동기화가 한 방향이므로 Campaign에서 변경 사항이 발생하면 동기화 중에 Campaign에서 덮어쓸 수 있습니다.  또한 연락처 동기화는 모든 연락처 레코드를 Microsoft Dynamics 365에서 활성 또는 비활성 상태로 표시할지 여부에 따라 가져오도록 설계되었습니다.

## 개인 정보 요청 관리

이 통합은 최종 사용자 데이터(최종 사용자 데이터에 포함되어 있는 경우 개인 정보를 포함)를 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 전송하도록 설계되었습니다.  데이터 관리자인 경우 회사는 개인 데이터의 수집 및 사용에 적용되는 개인정보 보호 법 및 규정을 준수할 책임을 집니다.

이 통합을 위해 변경 사항이 두 데이터베이스에 모두 반영되도록 각 시스템에서 개별 데이터 주체 요청을 처리해야 합니다. 변경 사항은 먼저 Microsoft Dynamics 365에서 실행한 다음 Adobe Campaign Standard에서 실행해야 합니다. 단, 개인정보 보호 관련 삭제 요청은 Dynamics 365에서 연락처를 삭제하면 Campaign Standard의 개인 정보 도구 큐에 추가됩니다.

다음은 각 시스템에서 액세스 및/또는 개인정보 보호 관련 요청을 구현하는 데 도움이 되는 링크 링크입니다.

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)

## 연락처 삭제

Dynamics 365가 진실의 소스이므로 Dynamics 365의 연락처 삭제는 Campaign에 반영됩니다.

Dynamics 365에서 담당자가 삭제되면 통합이 캠페인 개인 정보 보호 요청/도구 화면에서 개인 정보 관련 삭제 요청을 대기열로 표시합니다.  개인 정보 관련 삭제 요청에 대한 2단계 프로세스를 비활성화한 경우 Campaign에서 삭제를 처리합니다.

그러나 2단계 프로세스가 활성화되면 개인 정보 보호 요청/도구 화면으로 이동한 후 개인 정보 기술 워크플로우가 제대로 삭제되었는지 확인해야 합니다.  그래야 Campaign이 삭제를 처리합니다.

자세한 내용은 Adobe Campaign [Standard에서 개인 정보 관련 삭제 요청을 실행하는 방법을 참조하십시오.](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/execute-privacy-requests.html)

>[!CAUTION]
>
>Campaign의 개인 정보 요청에 대해 2단계 프로세스를 활성화한 경우 Dynamics 365에서 삭제에 Campaign이 자동으로 반영되지 않습니다.  삭제를 확인하려면 [캠페인 개인 정보 요청] 화면으로 이동해야 합니다.

>[!NOTE]
>
>이 통합은 외부 ID(즉, Dynamics 365 연락처 ID)를 레코드/프로필 식별자로 사용하여 요청을 만듭니다.

## 옵트아웃

Dynamics 365와 Campaign 간의 옵트아웃 속성 차이점과 각 고객의 비즈니스 요구 사항의 차이로 인해 옵트아웃 매핑이 고객의 완료에 대한 연습으로 남아 있습니다. 최종 사용자 옵트아웃 기본 설정이 유지되도록 시스템 간에 옵트아웃을 제대로 매핑하고 옵트아웃한 채널을 통해 통신이 수신되지 않도록 하는 것이 중요합니다.

&quot;blackList&quot; 접두어(예: blackListEmail)를 가진 캠페인 속성이나 CPA 옵트아웃 매핑에 특정 특성을 사용할 수 있습니다.  Dynamics 365에서는 대부분의 옵트아웃 필드에 &quot;doNot&quot; 접두사가 있습니다.그러나 데이터 유형이 호환되는 경우 옵트아웃 목적으로 만든 사용자 지정 속성을 활용할 수도 있습니다.

통합을 프로비저닝할 때 비즈니스에 필요한 옵트아웃 구성을 지정할 수 있습니다.

* Dynamics 365는 옵트아웃을 위한 진실의 근원입니다.옵트아웃 속성은 Dynamics 365에서 Campaign Standard로 한 방향으로 동기화됩니다.
* Campaign Standard는 옵트아웃을 위한 진실의 소스입니다.옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다.
* Dynamics 365 AND Campaign Standard는 모두 진실의 원천입니다.옵트아웃 속성은 Campaign Standard와 Dynamics 365 간에 양방향 동기화됩니다.

Unifi 사용자 안내서의 [](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn) 제공 후 지침에 따라 이러한 값을 제대로 매핑합니다.

양방향 옵트아웃 구성은 논리를 사용하여 두 시스템에 쓸 값을 결정합니다.  로직은 두 시스템(Dynamics 365의 레코드 수준 변경, Campaign의 속성 수준 변경) 간의 타임스탬프를 비교하여 어떤 시스템이 우선하는지 결정합니다.  캠페인에 최신 타임스탬프가 포함되어 있으면 캠페인 값이 우선합니다.  Dynamics 365에 최신 타임스탬프가 포함되어 있거나 이러한 타임스탬프가 동일하면 opt-out=TRUE가 설정됩니다(값 중 하나가 TRUE라고 가정할 경우).

**CCPA(California Consumer Protection Act)와 유사한 법률에 따른 옵트아웃**

양방향 옵트아웃 구성 기능은 현재 CPA 및/또는 기타 데이터 개인 정보 보호 법에 의거하여 특정 법적 요구 사항을 준수할 수 없습니다. CPA 또는 이와 유사한 법적 요구 사항을 준수해야 하는 고객은 양방향 동기화를 수행하기 위해 자사의 타사 솔루션을 구현할 책임이 있습니다.

>[!NOTE]
>
>회사에서 양방향 옵트아웃 지원이 필요하지 않은 경우 한 방향 옵트아웃 옵션을 선택하는 것이 좋습니다.

>[!NOTE]
>
>해당되는 경우, 여기에서 변경하기 전에 Adobe Campaign의 기본 유형 및 특정 분류 규칙을 검토하여 이러한 변경 사항이 모든 나가는 통신에 올바르게 적용되었는지 확인하십시오. 예를 들어 옵트아웃 기본 설정에 대한 매핑이 받는 사람의 의도/커뮤니케이션 선택 사항을 정확하게 반영하며 고객 주문 확인과 같은 거래 메시지 또는 관계 제공을 실수로 중단하지 않도록 하십시오.

## 기존 캠페인 데이터

이 통합은 Dynamics 365의 연락처와 사용자 지정 개체를 Campaign과 동기화합니다. 통합 외부에서 만들어진 캠페인 레코드(즉, 동기화 작업에 의해 만들어지지 않음)는 통합 구성 시 존재하는 캠페인 레코드를 포함하여 통합에 의해 수정되지 않습니다.

이 통합은 Campaign Standard의 **[!UICONTROL externalId]** 필드를 사용하여 Campaign 프로필 레코드를 Dynamics 365 연락처 레코드와 동기화하므로 이 캠페인 필드(**[!UICONTROL externalId]** )는 Dynamics 365에서 동기화하려는 **[!UICONTROL contactId]** 레코드에 대해 Dynamics 365로 채워야 합니다.  사용자 지정 엔터티도 이 필드를 올바로 채워야 동기화를 유지할 수 있습니다.  그러나 Dynamics 365는 여전히 진실의 소스이며 통합이 Dynamics 365측에서 업데이트를 감지하면 캠페인 프로필 데이터를 덮어쓸 수 있음을 염두에 두십시오.  기존 배포에 따라 통합을 활성화하는 데 필요한 다른 단계가 있을 수도 있습니다.따라서 Adobe 기술 담당자와 긴밀하게 협력하는 것이 좋습니다.

>[!NOTE]
>
>기존 고객 배포의 복잡성으로 인해 통합 계획 및 설정 시 Adobe 기술 담당자와 함께 작업하는 것이 좋습니다.
