---
title: Campaign 및 Microsoft Dynamics 365 데이터 관리
description: Campaign Standard 및 Microsoft Dynamics 365에서 일반 데이터를 관리하는 방법을 알아봅니다
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: aab6f005-f3da-4c0b-b856-da8504e611dc
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '2507'
ht-degree: 1%

---

# 모범 사례 및 제한 사항 {#acs-msdyn-best-practices}

## 데이터 관리 {#acs-msdyn-manage-data}

연락처 및 사용자 지정 엔티티 동기화를 위해 이 통합은 을 처리합니다 **Microsoft Dynamics 365 를 진실의 소스로 사용**.  동기화된 속성에 대한 변경 사항은 Adobe Campaign Standard이 아니라 Dynamics 365에서 수행해야 합니다.  Campaign에서 변경된 경우 동기화가 한 방향으로 진행되므로 동기화 중에 Campaign에서 덮어쓸 수 있습니다.

데이터 무결성을 유지하기 위해 Dynamics 365에서 연락처가 삭제될 때 Campaign에 프로필 삭제 호출을 실행하도록 선택적으로 구성할 수 있습니다. 하지만 프로필 삭제는 개인 정보 삭제와 다릅니다. Campaign에서 개인 정보 보호를 삭제하면 Campaign 프로필 레코드 및 관련 로그 항목이 제거됩니다. 반면에 일반 프로필 삭제는 Campaign 프로필 레코드만 삭제하여 Campaign 로그에 남아 있습니다. 통합에서 프로필 삭제 기능이 활성화된 경우 데이터 주체 개인 정보 보호 요청을 제대로 처리하려면 추가 단계를 수행해야 합니다. 의 단계를 참조하십시오 [아래의 개인 정보 섹션](#manage-privacy-requests).

## 개인 정보 보호{#acs-msdyn-manage-privacy}

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터를 전송하도록 설계되었습니다. 이 데이터에는 최종 사용자 데이터에 포함된 경우 개인 정보가 포함됩니다.  데이터 제어자는 개인 데이터 수집 및 사용에 적용되는 개인 정보 보호 법 및 규정을 준수할 책임이 있습니다.

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터(최종 사용자 데이터에 포함된 경우 개인 정보를 포함하되, 이에 제한되지 않음)를 전송하도록 설계되었습니다. 데이터 제어자는 개인 데이터 수집 및 사용에 적용되는 개인 정보 보호 법 및 규정을 준수할 책임이 있습니다.

통합은 데이터 주체 개인 정보(예: GDPR)를 발행 하지 않으며 다른 개인 정보 보호 요청(옵트아웃 제외)을 삭제하거나 처리하지 않습니다. 개인 정보 보호 요청을 처리할 때는 Microsoft Dynamics 365와 Campaign(Adobe Experience Platform Privacy Service을 통해) 모두에서 독립적으로 이 작업을 수행해야 합니다.

Dynamics 365에서 연락처를 삭제할 때 Campaign에 일반 프로필 삭제 호출을 실행하도록 통합을 구성한 경우 아래 단계를 수행해야 합니다. 이 프로세스 중에 해당 레코드에 대한 업데이트가 수행되지 않도록 합니다.

1. 에 대한 개인 정보 보호 삭제 요청 문제 [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html)

1. 요청이 성공적으로 완료될 때까지 요청 모니터링

1. 레코드가 Campaign 인스턴스에 더 이상 없는지 확인합니다.

1. (곧) Dynamics 365 내에서 개인 정보 보호 삭제 문제

1. 두 시스템에서 레코드가 제거되었는지 확인합니다.

다음은 각 시스템에서 액세스 및/또는 개인 정보 보호 관련 요청 삭제를 안내하는 도움말 링크입니다.

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/)

* [Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)

>[!IMPORTANT]
>
>Campaign 사용자 지정 리소스 레코드에 고객의 Campaign 사용에 적용되는 개인 정보가 포함되어 있는 경우 이러한 레코드는 해당 Campaign 프로필 레코드(직접 또는 다른 사용자 지정 리소스를 통해)에 연결되어 프로필 레코드에 대한 개인 정보 보호 관련 삭제도 개인 정보가 포함된 연결된 사용자 지정 리소스 레코드를 삭제할 수 있습니다. 연결된 레코드를 캐스케이드처럼 제거할 수 있도록 엔티티 간 연결 및 삭제 옵션을 구성해야 합니다. 프로필에 연결되지 않은 사용자 지정 리소스에 개인 정보를 입력해서는 안 됩니다.

## 옵트아웃 {#opt-out}

Microsoft Dynamics 365와 Campaign 간의 옵트아웃 특성 및 각 고객의 비즈니스 요구 사항에 차이가 있으므로 옵트아웃 매핑은 고객이 완료할 수 있도록 연습으로 남아 있습니다.  최종 사용자 옵트아웃 환경 설정이 유지 관리되고 옵트아웃한 채널을 통해 통신을 받지 않도록 시스템 간에 옵트아웃을 제대로 매핑하는 것이 중요합니다.

옵트아웃 매핑에는 다음 항목만 사용할 수 있습니다.

* &#39;더 이상 연락하지 않음&#39; 접두사가 있는 Campaign 속성(예: 더 이상 이메일로 연락하지 않음) 또는

* CCPA에 대한 특정 속성

프로필 엔티티 필드에 대한 자세한 내용을 찾을 수 있습니다 [여기](../../developing/using/datamodel-profile.md).

Dynamics 365에서는 대부분의 옵트아웃 필드에 &quot;doot&quot; 접두사가 있지만, 데이터 형식이 호환되는 경우 옵트아웃 목적으로 다른 특성을 활용할 수도 있습니다.

통합을 프로비저닝할 때 비즈니스에 필요한 옵트아웃 구성을 지정할 수 있습니다.

* **일방향(Microsoft Dynamics 365에서 Campaign으로)**: Dynamics 365는 옵트아웃에 대한 진실의 원본입니다. 옵트아웃 속성은 Dynamics 365에서 Campaign Standard으로 한 방향으로 동기화됩니다
* **일방향(Campaign에서 Microsoft Dynamics 365로)**: Campaign Standard은 옵트아웃의 진실입니다. 옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다
* **양방향**: Dynamics 365와 Campaign Standard 모두 진실의 근원이다. 옵트아웃 속성은 Campaign Standard과 Dynamics 365 간에 양방향 동기화됩니다

또는 시스템 간 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 플로우를 비활성화할 수 있습니다.

양방향 옵트아웃 구성은 논리를 사용하여 두 시스템에 쓸 값을 결정합니다. 이 논리는 두 시스템(Dynamics 365의 레코드 수준 변경, Campaign의 속성 수준 변경) 간의 타임스탬프를 비교하여 어떤 시스템이 우선하는지 결정합니다. Campaign에 더 최근 타임스탬프가 포함되어 있으면 캠페인 값이 우선합니다. Dynamics 365에 최신 타임스탬프가 들어 있거나 타임스탬프가 같은 경우 opt-out=TRUE가 됩니다(값 중 하나가 TRUE라고 가정).

에서 옵트인/아웃 옵션을 선택하는 방법을 알아봅니다. [이 섹션](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!NOTE]
>
>해당되는 경우 Adobe Campaign에서 기본 및 특정 유형화 규칙을 업데이트한 후 여기에서 변경할 수 있으므로 모든 발신 통신에 이러한 변경 사항이 올바르게 적용되는지 확인하십시오. 예를 들어 옵트아웃 환경 설정에 대한 매핑은 수신자의 의도/통신 선택 사항을 정확하게 반영하며 고객 주문 확인과 같은 관계 또는 트랜잭션 메시지 전달을 실수로 중단하지 않도록 하십시오.

을(를) 선택한 경우 **양방향** 또는 **일방향(Campaign에서 Microsoft Dynamics 365로)** 옵트아웃 구성, Campaign 옵트아웃 데이터는 워크플로우를 통해 주기적으로 Campaign SFTP 저장소 영역으로 내보내집니다(&quot;아래 Campaign SFTP 사용&quot; 참조). Campaign 옵트아웃 워크플로우가 실행되지 않는 경우 옵트아웃 동기화 가능성을 줄이려면 가능한 한 빨리 수동으로 다시 시작해야 합니다.

>[!IMPORTANT]
>
>필요한 경우 **양방향** 또는 **일방향(Campaign에서 Microsoft Dynamics 365로)** 옵트아웃 구성을 수행하려면, Campaign 인스턴스에 설정할 옵트아웃 워크플로우를 Adobe 기술 담당자에게 요청해야 합니다

## Campaign SFTP 사용

아래 사용 사례에서 통합으로 Campaign SFTP 저장소를 활용해야 합니다.  SFTP 계정에 이러한 사용 사례를 수용할 수 있는 적절한 스토리지 용량이 있는지 확인해야 합니다. 라이선스가 있는 SFTP 스토리지 용량을 초과하면 Campaign, 통합 및/또는 SFTP 계정의 기능 사용이 심각하게 손상될 수 있습니다.

| 활용 사례 | 설명 |
|---|---|
| 양방향 및 단방향(Campaign에서 Microsoft Dynamics 365로) | 양방향 및 단방향(Campaign에서 Microsoft Dynamics 365로) 옵트아웃 데이터 흐름은 Campaign SFTP 저장소를 사용합니다. Campaign 워크플로우는 증분 변경 사항을 SFTP 폴더로 내보냅니다. 여기에서 통합은 레코드와 프로세스를 선택합니다. |
| 옵트아웃 로그 | 커넥터의 출력 로그는 통합을 해결할 때 유용합니다. 출력 로그를 설정/해제할 수 있습니다. |


>[!IMPORTANT]
>
>SFTP 폴더에서 액세스 및 다운로드하는 정보는 사용자가 책임집니다. 정보에 개인 데이터가 포함되어 있는 경우 해당 개인 정보 보호 법 및 규정을 준수할 책임이 있습니다. [자세히 알아보기](#acs-msdyn-manage-privacy)

## 데이터 관리

### 기존 Campaign 데이터

이 통합은 Microsoft Dynamics 365의 연락처 및 사용자 지정 엔터티를 Campaign과 동기화합니다. 통합 외부에서 만든 캠페인 레코드(즉, 동기화 작업으로 만들지 않음)는 통합 구성 시 기존 캠페인 레코드를 포함하여 통합에 의해 수정되지 않습니다.

이 통합은 **[!UICONTROL externalId]** 캠페인 프로필 레코드를 Dynamics 365 연락처 레코드와 동기화하기 위한 Campaign의 필드, 이 캠페인 필드(**[!UICONTROL externalId]** )을 Microsoft Dynamics 365로 채워야 합니다. **[!UICONTROL contactId]** Microsoft Dynamics 365에서 동기화할 레코드의 경우.  사용자 지정 엔티티는 Microsoft Dynamics 365 고유 ID를 사용하여 동기화하기도 합니다. Campaign 사용자 지정 엔티티는 이 ID 속성을 테이블 열로 포함해야 합니다. externalId 열은 이 속성 값을 저장하는 데 사용할 수 있지만, Campaign 사용자 지정 엔티티에 필요하지 않습니다.

Microsoft Dynamics 365는 여전히 진실의 소스이며, 통합이 Dynamics 365 측에서 업데이트를 감지하면 캠페인 프로필 데이터를 덮어쓸 수 있습니다.  기존 배포에 따라 통합을 활성화하는 데 필요한 다른 단계도 있을 수 있습니다. 따라서 Adobe 기술 담당자와 긴밀히 협력하는 것이 좋습니다.

>[!NOTE]
>
>기존 고객 배포의 복잡성으로 인해 통합을 계획 및 설정할 때 Adobe 기술 담당자와 협력하는 것이 좋습니다.

### 데이터 동기화 빈도

통합은 Microsoft Dynamics 365에서 업데이트가 발생한 후 바로 처리 &quot;큐&quot;에 업데이트를 감지하고 추가할 수 있는 아키텍처를 사용합니다(예: 일괄 처리가 아닌 스트리밍). 이러한 이유로 데이터 흐름 실행 빈도 또는 일정을 지정할 필요가 없습니다.

단, 양방향 및 Campaign에서 Dynamics 365 옵트아웃 데이터 흐름이 예외입니다. 이러한 옵트아웃 구성의 경우, 업데이트된 Campaign 레코드는 매일 한 번 Campaign 워크플로우를 통해 SFTP에 내보내지며 통합 도구는 파일을 읽고 레코드를 처리합니다.

### 데이터 사용 계약

EMEA 또는 APAC 지역에 있는 경우 일부 데이터가 미국에서 이 통합의 일부로 처리됩니다. 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)을 참조하십시오.

## 보호 및 제한 사항

>[!IMPORTANT]
>
>부품에 대한 특정 작업(예: 레코드 초기 수집, 레코드 데이터 재재생 등) 이로 인해 Microsoft Dynamics 365에서 Adobe Campaign 인스턴스로 많은 레코드를 수집할 수 있습니다. 성능 문제의 위험을 줄이기 위해 모든 Campaign 프로세스를 중지하는 것이 좋습니다(예: 마케팅 활동, 워크플로우 실행 없음 등). 대량의 레코드를 Campaign에 수집하기 전까지.

### 사용자 지정 엔티티

다음 [Microsoft Dynamics 365-Adobe Campaign Standard 통합](../../integrating/using/d365-acs-get-started.md) 은 사용자 지정 엔티티를 지원하므로 Dynamics 365의 사용자 지정 엔티티가 Campaign의 해당 사용자 지정 리소스와 동기화될 수 있습니다.

통합은 연결된 테이블과 연결되지 않은 테이블을 모두 지원합니다.

사용자 지정 엔티티 데이터 플로우를 구성할 때는 다음 사항을 알고 있어야 합니다.

* Campaign 사용자 지정 리소스를 만들고 수정하는 작업은 전문가 사용자만 수행해야 하는 중요한 작업입니다.
* 사용자 지정 엔티티 데이터 흐름의 경우 동기화된 사용자 지정 엔티티에 대해 Dynamics 365 내에서 변경 추적을 활성화해야 합니다.
* 통합의 병렬 처리로 인해 Dynamics 365에서 상위 레코드와 연결된 하위 레코드가 거의 동시에 만들어지는 경우 새 하위 레코드를 상위 레코드 전에 Campaign에 쓸 수 있는 가능성이 약간 있습니다.

* 상위 및 하위 항목이 **1개의 카디널리티 단순 링크** 옵션을 선택하면 상위 레코드가 Campaign에 도착할 때까지 하위 레코드가 숨겨지고 액세스할 수 없는 상태로 유지됩니다(UI 또는 API를 통해).

* (다음과 같은 경우 **1개의 카디널리티 단순 링크** campaign에서) 하위 레코드가 Dynamics 365에서 업데이트 또는 삭제되고 상위 레코드가 Campaign에 표시되기 전에 해당 변경 사항이 Campaign에 기록되는 경우(그럴 가능성은 없지만 원격 가능성)에는 해당 업데이트 또는 삭제가 Campaign에서 처리되지 않고 오류가 발생합니다. 업데이트되는 경우 업데이트된 레코드를 동기화하려면 해당 레코드를 Dynamics 365에서 다시 업데이트해야 합니다. 삭제의 경우 Dynamics 365에서 삭제하거나 업데이트하는 레코드가 없으므로 해당 레코드는 캠페인 측에서 별도로 관리해야 합니다.

* 숨겨진 자식 레코드가 있고 자식 레코드에 액세스할 방법이 없는 상황이 발생하면 카디널리티 링크 유형을 일시적으로 로 변경할 수 있습니다 **0 또는 1 카디널리티 단순 링크** 해당 레코드에 액세스할 수 있습니다.

Campaign 사용자 지정 리소스에 대한 보다 포괄적인 개요를 찾을 수 있습니다 [이 섹션](../../developing/using/key-steps-to-add-a-resource.md).

### 통합 가드 레일

이 통합을 사용할 계획을 세울 때 다음 가드 레일을 고려해야 합니다. 이러한 보호 기능을 초과하는 경우 Adobe 기술 담당자에게 문의하십시오.

* 통합에서 생성한 엔진 호출 볼륨을 지원하려면 적절한 Campaign 패키지의 라이선스가 있어야 합니다. 라이선스가 있는 엔진 호출 볼륨을 초과하면 Campaign 성능이 저하될 수 있습니다.

   통합에서 엔진 호출 볼륨을 추정하는 데 도움이 되도록 다음을 사용하십시오.

   * 레코드 삽입(즉, 새 레코드): 엔진 호출 1회
   * 레코드 삭제: 엔진 호출 1회
   * 레코드 업데이트: 2개의 엔진 호출(대상 레코드가 소스 레코드와 동일한 경우, 즉 캠페인 레코드가 변경되지 않는 경우에만 1개의 호출)

   전체 캠페인 엔진 호출 볼륨을 추정할 때 랜딩 페이지, WebApps, JSSP, API, 모바일 앱 등록 등을 비롯한 다른 엔진 호출 소스를 평가하는 것이 중요합니다.

   다음 위치에서 Adobe Campaign Standard 패키지 정보를 봅니다. [https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html)

* 통합은 Campaign의 리소스에 대한 초기 동기화에 대한 최대 1,500만 개의 레코드를 지원합니다. 증분 동기화는 Adobe Campaign Standard 패키지에 의해 제한됩니다.

* 표준 통합 서비스에는 최대 20개의 사용자 지정 엔티티가 지원되며 각각 최대 50개의 열이 포함되어 있습니다.

* 통합을 구현하기 전에 사용자 지정 리소스를 만들고 게시해야 합니다.

* 테이블을 연결할 때 최대 테이블 깊이는 2입니다(예: table1->table2->table3).

* 통합은 사용자 지정 리소스당 최대 5개의 연결된 열을 지원합니다. 사용자 지정 리소스 간에 여러 열을 연결하면 성능에 크게 영향을 줄 수 있습니다. **0 또는 1 카디널리티 단순 링크** 보다 선호됨 **1개의 카디널리티 단순 링크**.

* 통합은 기본 Microsoft Dynamics 365 데이터 형식(부울, 정수, 십진수, Double, 문자열, DateTime, Date)과 Adobe Campaign Standard 데이터 유형(정수, 부울, 부동, double, date, datetime, 문자열) 간의 변형을 지원합니다. 더 고급 데이터 유형은 문자열로 해석되고 그대로 동기화됩니다.

* Adobe과 고객 간에 온보딩 유지 관리 창을 설정해야 할 수도 있습니다.

* 통합 사용(예: 새 레코드나 업데이트된 레코드가 급격히 늘어나면 데이터 동기화 속도가 느려질 수 있습니다.)

* 통합의 일부로 Microsoft Azure 및 Dynamics 365에서 사전 통합 구성 단계를 완료해야 합니다. 구성 단계를 참조하십시오 [이 페이지에서](../../integrating/using/d365-acs-configure-d365.md)

* Dynamics 365 및 Campaign 데이터 모델을 통합에 가져와 유지 관리할 것으로 예상됩니다.

### 통합 경계

통합은 Microsoft Dynamics 365와 Campaign 간의 일반적인 데이터 이동 사용 사례를 해결하기 위해 고안되었지만, 각 고객에게만 적용되는 모든 사용 사례를 해결하기 위한 것은 아닙니다.

* 통합은 개인 정보(예: GDPR)를 발행 하지 않습니다. 최종 사용자 개인 정보 보호 요청을 이행할 책임은 고객에게 있습니다. 이러한 요청은 Campaign(Adobe Experience Platform Privacy Service을 통해) 및 Dynamics 365를 모두 독립적으로 해야 합니다. 필요한 경우 통합에서 데이터 동기화에 도움이 되도록 정기적으로 삭제를 실행할 수 있습니다.   검토 [개인 정보 섹션](#manage-privacy-requests) 추가 정보.

* 옵트아웃 정보를 제외하고(고객이 구성한 경우) 프로필 또는 사용자 지정 엔티티 데이터가 Campaign에서 Dynamics 365로 동기화되지 않습니다.

* Campaign 구독 관리(즉, 구독/구독 취소)는 기본적으로 지원되지 않습니다.

* Dynamics 365 내에서 Campaign 이메일 캠페인을 구성하고 트리거하는 것은 지원되지 않습니다.

* 통합은 다음을 수행합니다 **not** Dynamics 365와 Campaign Standard 데이터 모델 간의 데이터 리모델링을 지원합니다. 통합에서 하나의 Dynamics 365 테이블을 하나의 캠페인 테이블에 동기화할 것으로 예상됩니다.
