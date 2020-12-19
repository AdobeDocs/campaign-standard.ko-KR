---
solution: Campaign Standard
product: campaign
title: 캠페인 및 Microsoft Dynamics 365 데이터 관리
description: Campaign Standard 및 Microsoft Dynamics 365에서 일반적인 데이터를 관리하는 방법 살펴보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 1%

---


# Campaign과 Microsoft Dynamics 365 간의 데이터 관리

## 단방향 동기화를 위한 진실의 소스

연락처 및 맞춤형 엔티티 동기화를 위해 이 통합은 Dynamics 365를 진실의 소스로 취급합니다.  동기화된 속성에 대한 모든 변경 사항은 캠페인이 아니라 Dynamics 365에서 수행해야 합니다.  동기화가 한 방향이므로 Campaign에서 변경하면 동기화 도중 Campaign에서 해당 변경 사항을 덮어쓸 수 있습니다.

## 연락처 삭제

원하는 경우 Dynamics 365에서 담당자가 삭제되면 Campaign에 대한 프로필 삭제 호출을 실행하도록 통합을 구성하여 데이터 무결성을 유지할 수 있습니다.

하지만 프로필 삭제는 개인 정보 삭제와 다릅니다. Campaign에서 개인 정보를 삭제하면 캠페인 프로필 레코드 및 관련 로그 항목이 제거됩니다.반면에, 일반 프로필 삭제는 ACS 프로필 레코드만 삭제하여 Campaign 로그에 남아 있습니다.

통합에서 프로필 삭제 기능이 활성화되면 데이터 주체의 개인 정보 보호 요청을 제대로 처리하기 위해 추가 단계를 수행해야 합니다. ](#manage-privacy-requests) 아래의 [섹션에 있는 단계를 참조하십시오.

## 개인 정보

### 개인 정보 요청 관리 {#manage-privacy-requests}

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터(최종 사용자 데이터에 포함되어 있는 경우 개인 정보를 포함하되 이에 제한되지 않음)를 전송하도록 설계되었습니다. 데이터 관리자로서, 귀하의 회사는 귀하의 개인 데이터 수집 및 사용에 적용되는 개인정보 보호 법 및 규정을 준수할 책임을 집니다.

통합은 데이터 주체의 개인 정보 보호(예: GDPR)를 발행하지 않으며, 다른 개인 정보 보호 요청도 삭제 또는 처리합니다(수신 거부 제외). 개인 정보 요청을 처리할 때는 Dynamics 365와 Campaign(Adobe Experience Platform Privacy Service을 통해) 모두에서 개별적으로 수행해야 합니다.

Dynamics 365에서 연락처를 삭제할 때 Campaign에 대한 일반 프로필 삭제 호출을 발생하도록 통합을 구성한 경우 아래 단계를 수행해야 합니다. 이 프로세스 동안 해당 레코드에 대한 업데이트가 수행되지 않도록 하십시오.

1. [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html)에 대한 개인 정보 삭제 요청을 발행합니다.

1. 요청이 성공적으로 완료될 때까지 요청 모니터링

1. 레코드가 더 이상 캠페인 인스턴스에 없는지 확인합니다.

1. (곧) Dynamics 365 내에서 개인 정보 삭제를 발행합니다.

1. 두 시스템에서 레코드가 제거되었는지 확인

아래는 각 시스템에서 액세스 및/또는 개인 정보 관련 요청을 삭제하는 데 도움이 되는 링크입니다.

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)


### 개인 정보 및 연결된 리소스 {#privacy-linked-resources}

캠페인 사용자 지정 리소스 레코드에 고객의 캠페인 사용에 적용되는 개인 정보가 포함되어 있는 경우, 이러한 레코드는 해당 캠페인 프로필 레코드(직접 또는 다른 사용자 지정 리소스를 통해)에 연결되어 프로필 레코드에 있는 개인 정보 관련 삭제도 개인 정보가 포함된 연결된 사용자 지정 리소스 레코드를 삭제할 수 있습니다.연결된 레코드를 캐스케이드처럼 제거할 수 있도록 엔티티 간 연결 및 삭제 옵션을 구성해야 합니다. 개인 정보는 프로필과 연결되지 않은 사용자 지정 리소스에 입력해서는 안 됩니다.

이 섹션](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md)에서 캠페인 리소스와 Dynamics 365 개체 [를 매핑하는 방법을 알아봅니다.

## 옵트아웃

Dynamics 365와 Campaign 간의 옵트아웃 속성 차이와 각 고객의 비즈니스 요구 사항의 차이로 인해 옵트아웃 매핑이 고객의 완료에 대한 연습으로 남아 있습니다.  최종 사용자 옵트아웃 기본 설정이 유지되며 옵트아웃한 채널을 통해 통신이 수신되지 않도록 시스템 간에 옵트아웃을 올바르게 매핑해야 합니다.

&#39;더 이상 연락하지 않음&#39; 접두어(예: 이메일에 더 이상 연락하지 않음)나 CPA 옵트아웃 특정 속성을 가진 캠페인 특성만 옵트아웃 매핑에 사용할 수 있습니다. [자세히 알아보기](../../developing/using/datamodel-profile.md)
Dynamics 365에서는 대부분의 옵트아웃 필드에 &quot;doot&quot; 접두어가 있습니다.그러나 데이터 유형이 호환하는 경우 옵트아웃 용도로 다른 속성을 사용할 수도 있습니다.

통합을 프로비저닝할 때 비즈니스에 필요한 옵트아웃 구성을 지정할 수 있습니다.

* Dynamics 365는 옵트아웃을 위한 진실의 근원입니다.옵트아웃 속성은 Dynamics 365에서 Campaign으로 한 방향으로 동기화됩니다.
* 캠페인은 옵트아웃을 위한 진실의 근원입니다.옵트아웃 속성은 캠페인에서 Dynamics 365로 한 방향으로 동기화됩니다.
* Dynamics 365 AND Campaign은 두 가지 진실의 소스입니다.옵트아웃 속성은 Campaign과 Dynamics 365 간에 양방향 동기화됩니다.

또는 시스템 간의 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 흐름을 비활성화할 수 있습니다.

양방향 옵트아웃 구성은 논리를 사용하여 두 시스템에 쓸 값을 결정합니다. 논리 구조는 두 시스템(Dynamics 365의 레코드 수준 변경, 캠페인의 속성 수준 변경) 간 타임스탬프를 비교하여 어떤 시스템이 사용되고 있는지 결정합니다. 캠페인에 최신 타임스탬프가 포함되어 있으면 캠페인 값이 우선합니다. Dynamics 365에 최신 타임스탬프가 포함되어 있거나 이러한 타임스탬프가 동일하면 opt-out=TRUE가 반환됩니다(값 중 하나가 TRUE라고 가정함).

>[!NOTE]
>
>해당되는 경우, 여기에서 변경하기 전에 Adobe Campaign의 기본 및 특정 유형 규칙을 검토하고 업데이트하여 이러한 변경 사항이 나가는 모든 통신에 올바르게 적용되는지 확인하십시오. 예를 들어 옵트아웃 기본 설정에 대한 매핑이 받는 사람의 의도/통신 선택 사항을 정확하게 반영하고 고객 주문 확인과 같은 거래 메시지 또는 관계 제공을 실수로 중단하지 않도록 하십시오.

양방향 또는 Campaign에서 Dynamics 365 옵트아웃 구성을 선택한 경우, 캠페인 옵트아웃 데이터는 작업 과정을 통해 캠페인 SFTP 저장 영역으로 주기적으로 내보내집니다(&quot;아래의 캠페인 SFTP 사용량&quot; 참조). 캠페인 옵트아웃 워크플로의 실행이 중단된 경우, 옵트아웃 동기화 실패 가능성을 줄이기 위해 되도록 빨리 수동으로 다시 시작해야 합니다.

## 캠페인 SFTP 사용

아래 사용 사례의 통합으로 캠페인 SFTP 저장소를 활용해야 합니다.  SFTP 계정에 이러한 사용 사례를 수용할 수 있는 충분한 저장 공간이 있는지 확인해야 합니다.  라이선스가 부여된 SFTP 스토리지 용량을 초과하는 경우 Campaign, 통합 및/또는 SFTP 계정의 기능 사용에 심각한 문제가 발생할 수 있습니다.

| 사용 사례 | 설명 |
|---|---|
| 초기 데이터 로드 | 500k 레코드가 넘는 Dynamics 365개의 표를 Campaign SFTP 저장소로 내보내 워크플로우를 통해 가져와야 합니다. 이 시점부터 통합은 증분 업데이트에 API를 사용합니다. |
| 양방향 옵트아웃 및 Campaign에서 Dynamics 365로의 단방향 옵트아웃 | 양방향 옵트아웃 및 Campaign에서 Dynamics 365로의 단방향 옵트아웃 데이터 플로우는 캠페인 SFTP 저장소를 사용합니다. ACS 워크플로우는 증분 변경 내용을 SFTP 폴더로 내보냅니다. 여기에서 통합은 레코드와 프로세스를 선택합니다. |
| 재해 복구 | 시스템 재해가 발생할 가능성이 없는 경우 &quot;초기 데이터 로드&quot; 사용 사례 뒤에 누락된 Campaign에 증분 업데이트를 공급합니다. |

## 기존 캠페인 데이터

이 통합은 Dynamics 365의 연락처와 사용자 지정 개체를 Campaign과 동기화합니다. 통합 외부에서 만들어진 캠페인 레코드(즉, 동기화 작업에서 만들어지지 않음)는 통합 구성 시 존재하는 캠페인 레코드를 포함하여 통합에 의해 수정되지 않습니다.

이 통합은 캠페인의 **[!UICONTROL externalId]** 필드를 사용하여 캠페인 프로필 레코드를 Dynamics 365 연락처 레코드와 동기화하므로 이 캠페인 필드(**[!UICONTROL externalId]**)는 Dynamics 365에서 동기화하려는 레코드에 대해 Dynamics 365 **[!UICONTROL contactId]**&#x200B;로 채워야 합니다.  또한 사용자 지정 엔티티는 Dynamics 365 고유 ID를 사용하여 동기화됩니다. Campaign 사용자 지정 엔티티는 이 ID 속성을 테이블 열로 포함해야 합니다. externalId 열을 사용하여 이 속성 값을 저장할 수 있지만 Campaign 사용자 지정 엔터티에는 필요하지 않습니다.

Dynamics 365는 여전히 진실의 소스이며 통합이 Dynamics 365쪽에서 업데이트를 감지하면 캠페인 프로필 데이터를 덮어쓸 수 있습니다.  기존 배포에 따라 통합을 활성화하는 데 필요한 다른 단계가 있을 수도 있습니다.따라서 Adobe 기술 담당자와 긴밀하게 협력할 것을 권장합니다.

>[!NOTE]
>
>기존 고객 배포의 복잡성 때문에 통합을 계획 및 설정할 때 Adobe 기술 담당자와 함께 작업하는 것이 좋습니다.

## 데이터 동기화 빈도

통합은 Dynamics 365(일괄 처리가 아닌 스트리밍)에서 업데이트가 발생하고 바로 처리 &quot;대기열&quot;에 추가되도록 허용하는 아키텍처를 활용합니다. 이러한 이유로 데이터 흐름 실행 빈도 또는 일정을 지정할 필요가 없습니다.

이에 대한 예외는 양방향 및 Campaign에서 Dynamics 365 옵트아웃 데이터 플로우입니다. 이러한 옵트아웃 구성의 경우, 업데이트된 ACS 레코드는 ACS 작업 과정을 통해 하루에 한 번 SFTP로 내보내지고 통합 도구가 파일을 읽고 레코드를 처리합니다.

## 데이터 사용 계약

EMEA 또는 APAC 지역에 거주하는 경우, 이 통합의 일부로 일부 데이터가 미국에서 처리됩니다. 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)을 참조하십시오.
