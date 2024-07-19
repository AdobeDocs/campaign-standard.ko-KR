---
title: Campaign 및 Microsoft Dynamics 365 데이터 관리
description: Campaign Standard 및 Microsoft Dynamics 365에서 일반 데이터를 관리하는 방법 알아보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: aab6f005-f3da-4c0b-b856-da8504e611dc
source-git-commit: 17522f4df86c7fb46593472316d57b4ba4acee2b
workflow-type: tm+mt
source-wordcount: '2523'
ht-degree: 1%

---

# 모범 사례 및 제한 사항 {#acs-msdyn-best-practices}

## 데이터 관리 {#acs-msdyn-manage-data}

연락처 및 사용자 지정 엔터티 동기화의 경우 이 통합은 **Microsoft Dynamics 365를 신뢰할 수 있는 소스로 취급**&#x200B;합니다.  동기화된 특성에 대한 모든 변경은 Adobe Campaign Standard이 아닌 Dynamics 365에서 수행해야 합니다.  Campaign에서 변경 사항이 적용되면 동기화는 한 방향이므로 동기화하는 동안 Campaign에서 결국 덮어쓸 수 있습니다.

데이터 무결성을 유지하기 위해 Dynamics 365에서 연락처가 삭제될 때 Campaign에 프로필 삭제 호출을 발행하도록 통합을 선택적으로 구성할 수 있습니다. 그러나 프로필 삭제는 개인 정보 삭제와 다릅니다. Campaign에서 개인 정보를 삭제하면 Campaign 프로필 레코드와 관련 로그 항목이 제거됩니다. 반면 일반 프로필을 삭제하면 Campaign 프로필 레코드만 삭제되고 나머지 항목은 Campaign 로그에 남습니다. 통합에서 프로필 삭제 기능이 활성화된 경우 데이터 주체 개인 정보 보호 요청을 제대로 처리하려면 추가 단계가 뒤따라야 합니다. 아래 [개인 정보 보호 섹션](#manage-privacy-requests)의 단계를 참조하세요.

## 개인 정보 보호{#acs-msdyn-manage-privacy}

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터를 전송하도록 설계되었습니다. 이 데이터에는 최종 사용자 데이터에 포함된 개인 정보가 포함됩니다.  회사는 데이터 컨트롤러로서 개인 데이터의 수집 및 사용에 적용되는 개인정보 보호 법률 및 규정을 준수할 책임이 있습니다.

이 통합은 최종 사용자 데이터(최종 사용자 데이터에 개인 정보가 포함된 경우 이에 국한되지 않음)를 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 전송하도록 설계되었습니다. 회사는 데이터 컨트롤러로서 개인 데이터의 수집 및 사용에 적용되는 개인정보 보호 법률 및 규정을 준수할 책임이 있습니다.

통합은 데이터 주체 개인 정보(예: GDPR)를 발행하지 않으며 다른 개인 정보 보호 요청(옵트아웃은 제외)을 삭제하거나 처리합니다. 개인 정보 요청을 처리할 때는 Microsoft Dynamics 365와 Campaign(Adobe Experience Platform Privacy Service을 통해) 모두에서 독립적으로 수행해야 합니다.

Dynamics 365에서 연락처가 삭제될 때 Campaign에 대해 정기적인 프로필 삭제 호출을 발행하도록 통합을 구성한 경우 아래 단계를 따라야 합니다. 이 프로세스 중에 해당 레코드가 업데이트되지 않았는지 확인합니다.

1. [Adobe Experience Platform Privacy Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service)에 대한 문제 개인 정보 삭제 요청

1. 요청이 성공적으로 완료될 때까지 모니터링

1. 레코드가 더 이상 Campaign 인스턴스에 없는지 확인

1. (곧 이어) Dynamics 365 내에서 문제 개인 정보 보호 삭제

1. 두 시스템에서 레코드가 제거되었는지 확인


>[!IMPORTANT]
>
>고객의 Campaign 사용에 적용 가능한 개인 정보가 Campaign 사용자 지정 리소스 레코드에 포함된 경우 해당 Campaign 프로필 레코드에 해당 레코드를 직접 또는 다른 사용자 지정 리소스를 통해 연결해야 프로필 레코드의 개인 정보 관련 삭제에서 개인 정보가 포함된 연결된 사용자 지정 리소스 레코드도 삭제할 수 있습니다. 엔터티 간의 연결 및 삭제 옵션은 연결된 레코드를 계단식으로 제거할 수 있도록 구성해야 합니다. 프로필에 연결되지 않은 사용자 지정 리소스에 개인 정보를 입력할 수 없습니다.

## 옵트아웃 {#opt-out}

Microsoft Dynamics 365와 Campaign의 옵트아웃 속성 차이 및 각 고객의 비즈니스 요구 사항 차이로 인해 옵트아웃 매핑은 고객이 완료할 수 있는 연습으로 남았습니다.  최종 사용자 옵트아웃 환경 설정이 유지되고 옵트아웃한 채널을 통해 커뮤니케이션을 받지 않도록 시스템 간에 옵트아웃이 제대로 매핑되도록 하는 것이 중요합니다.

옵트아웃 매핑에는 다음 항목만 사용할 수 있습니다.

* &#39;더 이상 연락하지 않음&#39; 접두사가 있는 캠페인 속성(예: 더 이상 연락하지 않음 이메일) 또는

* ccpa에 대한 특정 속성

프로필 엔터티 필드에 대한 자세한 내용은 [여기](../../developing/using/datamodel-profile.md)에서 확인할 수 있습니다.

Dynamics 365에서 대부분의 옵트아웃 필드에는 &quot;donot&quot; 접두사가 있지만 데이터 형식이 호환되는 경우 옵트아웃 목적으로 다른 속성을 활용할 수도 있습니다.

통합을 프로비저닝할 때 비즈니스에 필요한 옵트아웃 구성을 지정할 수 있습니다.

* **단방향(Microsoft Dynamics 365에서 Campaign으로)**: Dynamics 365가 옵트아웃에 대한 올바른 원본입니다. 옵트아웃 속성은 Dynamics 365에서 Campaign Standard으로 한 방향으로 동기화됩니다.
* **단방향(Microsoft Dynamics 365에 대한 캠페인)**: Campaign Standard은 옵트아웃에 대한 신뢰할 수 있는 소스입니다. 옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다.
* **양방향**: Dynamics 365와 Campaign Standard은 모두 올바른 원본입니다. 옵트아웃 속성은 Campaign Standard과 Dynamics 365 간에 양방향으로 동기화됩니다.

또는 시스템 간의 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 흐름이 비활성화될 수 있습니다.

양방향 옵트아웃 구성은 논리를 사용하여 두 시스템에 쓸 값을 결정합니다. 논리는 두 시스템(Dynamics 365의 레코드 수준 변경, Campaign의 특성 수준 변경) 간의 타임스탬프를 비교하여 어느 시스템이 우세한지 확인합니다. Campaign에 최신 타임스탬프가 포함된 경우 Campaign 값이 우선합니다. Dynamics 365에 최신 타임스탬프가 포함되어 있거나 동일한 경우 옵트아웃=TRUE가 적용됩니다(값 중 하나가 TRUE라고 가정).

[이 섹션](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf)에서 옵트인/옵트아웃 옵션을 선택하는 방법을 알아보세요.

>[!NOTE]
>
>여기서 변경하기 전에 Adobe Campaign에서 기본적이고 구체적인 유형화 규칙을 검토하고 업데이트하여 그러한 변경 사항이 모든 발신 통신에 올바르게 적용되도록 하십시오. 예를 들어 옵트아웃 환경 설정에 대한 모든 매핑이 수신자의 의도/커뮤니케이션 선택 사항을 정확하게 반영하고 고객 주문 확인과 같은 관계 또는 트랜잭션 메시지의 전달을 실수로 중단하지 않도록 하십시오.

**양방향** 또는 **단방향(Microsoft Dynamics 365에 대한 캠페인)** 옵트아웃 구성을 선택한 경우 Campaign 옵트아웃 데이터는 주기적으로 워크플로우를 통해 Campaign SFTP 저장소 영역으로 내보내집니다(&quot;아래 캠페인 SFTP 사용&quot; 참조). Campaign 옵트아웃 워크플로우가 실행되지 않는 경우, 누락된 옵트아웃 동기화를 줄이기 위해 가능한 한 빨리 수동으로 다시 시작해야 합니다.

>[!IMPORTANT]
>
>**양방향** 또는 **단방향(Microsoft Dynamics 365에 대한 캠페인)** 옵트아웃 구성이 필요한 경우 Adobe 기술 담당자에게 요청하여 Campaign 인스턴스에 옵트아웃 워크플로를 설정해야 합니다

## Campaign SFTP 사용

아래 사용 사례에서 통합은 Campaign SFTP 스토리지를 활용해야 합니다.  SFTP 계정에 이러한 사용 사례를 수용할 수 있는 적절한 저장소 용량이 있는지 확인해야 합니다. 라이선스가 부여된 SFTP 스토리지 용량을 초과하면 Campaign, 통합 및/또는 SFTP 계정의 기능 사용에 심각한 지장이 있을 수 있습니다.

| 활용 사례 | 설명 |
|---|---|
| 양방향 및 단방향(Microsoft Dynamics 365에 대한 캠페인) | 양방향 및 단방향(Microsoft Dynamics 365에 대한 캠페인) 옵트아웃 데이터 흐름은 Campaign SFTP 저장소를 활용합니다. Campaign 워크플로우는 증분 변경 사항을 SFTP 폴더로 내보냅니다. 여기에서 통합이 레코드와 프로세스를 선택합니다. |
| 옵트아웃 로그 | 커넥터의 출력 로그는 통합 문제를 해결할 때 유용합니다. 출력 로그를 설정/해제할 수 있습니다. |


>[!IMPORTANT]
>
>SFTP 폴더에서 액세스하고 다운로드하는 정보는 사용자가 담당합니다. 정보에 개인 데이터가 포함되어 있는 경우 귀하는 해당 개인 정보 보호 법률 및 규정을 준수할 책임이 있습니다. [자세히 알아보기](#acs-msdyn-manage-privacy).

## 데이터 관리

### 기존 캠페인 데이터

이 통합은 연락처 및 사용자 지정 엔터티를 Microsoft Dynamics 365에서 Campaign으로 동기화합니다. 통합 외부에서 생성된(즉, 동기화 작업으로 생성되지 않은) 캠페인 레코드는 통합 구성 시 존재하는 캠페인 레코드를 포함하여 통합에 의해 수정되지 않습니다.

이 통합에서는 Campaign의 **[!UICONTROL externalId]** 필드를 사용하여 Campaign 프로필 레코드를 Dynamics 365 연락처 레코드와 동기화하므로 Microsoft Dynamics 365에서 동기화할 레코드에 대해 이 Campaign 필드(**[!UICONTROL externalId]**)를 Microsoft Dynamics 365 **[!UICONTROL contactId]**(으)로 채워야 합니다.  사용자 지정 엔터티도 Microsoft Dynamics 365 고유 ID를 사용하여 동기화됩니다. Campaign 사용자 지정 엔티티는 이 ID 속성을 테이블 열로 포함해야 합니다. externalId 열은 이 속성 값을 저장하는 데 사용할 수 있지만 Campaign 사용자 지정 엔터티에 필요하지 않습니다.

Microsoft Dynamics 365는 여전히 신뢰할 수 있는 소스이며 통합이 Dynamics 365측의 업데이트를 감지하므로 Campaign 프로필 데이터를 덮어쓸 수 있습니다.  기존 배포에 따라 통합을 활성화하는 데 다른 단계가 필요할 수도 있습니다. 따라서 Adobe 기술 담당자와 긴밀히 협력하는 것이 좋습니다.

>[!NOTE]
>
>기존 고객 배포의 복잡성으로 인해 통합을 계획하고 설정할 때 Adobe 기술 담당자와 협력하는 것이 좋습니다.

### 데이터 동기화 빈도

통합은 Microsoft Dynamics 365에서 업데이트가 발생한 직후 검색 및 처리 &quot;큐&quot;에 추가할 수 있는 아키텍처를 사용합니다(즉, 일괄 처리가 아닌 스트리밍). 이러한 이유로, 데이터 흐름 실행 빈도 또는 스케줄을 지정할 필요가 없다.

Dynamics 365의 옵트아웃 데이터 흐름은 예외입니다. 이러한 옵트아웃 구성의 경우 업데이트된 Campaign 레코드는 하루에 한 번 Campaign 워크플로우를 통해 SFTP로 내보내지며, 이후 통합 도구가 파일을 읽고 레코드를 처리합니다.

### 데이터 사용 계약

EMEA 또는 APAC 지역에 있는 경우 이 통합의 일부로 일부 데이터가 미국에서 처리됩니다. 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)을 참조하십시오.

## 보호 기능 및 제한 사항

>[!IMPORTANT]
>
>부품에 대한 특정 작업(예: 레코드의 초기 수집, 레코드 데이터 재생 등) 이로 인해 Microsoft Dynamics 365에서 Adobe Campaign 인스턴스로 많은 양의 레코드가 수집될 수 있습니다. 성능 문제의 위험을 줄이려면 모든 Campaign 프로세스를 중지하는 것이 좋습니다(예: 마케팅 활동 없음, 워크플로우 실행 없음 등) 대량의 레코드가 Campaign에 수집될 때까지.

### 사용자 지정 엔티티

[Microsoft Dynamics 365-Adobe Campaign Standard 통합](../../integrating/using/d365-acs-get-started.md)은(는) 사용자 지정 엔터티를 지원하므로 Dynamics 365의 사용자 지정 엔터티를 Campaign의 해당 사용자 지정 리소스와 동기화할 수 있습니다.

통합은 연결된 테이블과 연결되지 않은 테이블을 모두 지원합니다.

사용자 지정 엔티티 데이터 흐름을 구성할 때는 다음 사항에 유의해야 합니다.

* Campaign 사용자 지정 리소스를 만들고 수정하는 작업은 전문가 사용자만 수행해야 하는 중요한 작업입니다.
* 사용자 지정 엔터티 데이터 흐름의 경우 동기화된 사용자 지정 엔터티에 대해 Dynamics 365 내에서 변경 내용 추적을 사용하도록 설정해야 합니다.
* 통합의 병렬 처리로 인해 Dynamics 365에서 부모 레코드와 연결된 자식 레코드가 거의 동시에 만들어지는 경우 새 자식 레코드가 부모 레코드보다 먼저 Campaign에 기록될 수 있습니다.

* 상위 레코드와 하위 레코드가 **1 카디널리티 단순 링크** 옵션을 사용하여 Campaign 측에서 연결된 경우 상위 레코드가 Campaign에 도착할 때까지 하위 레코드는 숨겨지고 액세스할 수 없습니다(UI 또는 API를 통해).

* (Campaign에서 **1 카디널리티 단순 링크** 가정) Dynamics 365에서 하위 레코드가 업데이트되거나 삭제되고 해당 변경 내용이 Campaign에 상위 레코드가 표시되기 전에 Campaign에 기록되는 경우(가능성이 높지 않지만 원격 가능성이 있음), 해당 업데이트 또는 삭제가 Campaign에서 처리되지 않고 오류가 발생합니다. 업데이트하는 경우 업데이트된 레코드를 동기화하려면 Dynamics 365에서 해당 레코드를 다시 업데이트해야 합니다. 삭제하는 경우 Dynamics 365에 삭제하거나 업데이트할 레코드가 더 이상 없으므로 해당 레코드는 캠페인 측에서 별도로 처리해야 합니다.

* 숨겨진 하위 레코드가 있고 이 레코드에 액세스할 수 없는 상황이 발생하는 경우 일시적으로 카디널리티 링크 형식을 **0 또는 1개의 카디널리티 단순 링크**(으)로 변경하여 해당 레코드에 액세스할 수 있습니다.

Campaign 사용자 지정 리소스에 대한 보다 포괄적인 개요는 이 섹션](../../developing/using/key-steps-to-add-a-resource.md)에서 [을(를) 찾을 수 있습니다.

### 통합 가드 레일

이 통합을 사용하려면 다음 보호 기능을 고려해야 합니다. 이 보호 기능을 초과했다고 생각되는 경우 Adobe 기술 담당자에게 문의하십시오.

* 통합에서 생성된 엔진 호출 볼륨을 지원하려면 적절한 Campaign 패키지에 라이선스를 부여해야 합니다. 라이선스가 부여된 엔진 호출 볼륨을 초과하면 Campaign 성능이 저하될 수 있습니다.

  다음을 사용하여 통합에서 엔진 호출 볼륨을 추정합니다.

   * 레코드 삽입(즉, 새 레코드): 1개의 엔진 호출
   * 삭제 기록: 엔진 호출 1개
   * 레코드 업데이트: 2개의 엔진 호출(대상 레코드가 소스 레코드와 동일한 경우(즉, 캠페인 레코드가 변경되지 않은 경우) 1개의 호출만)

  전체 Campaign 엔진 호출 볼륨을 예측할 때는 랜딩 페이지, WebApps, JSSP, API, 모바일 앱 등록 등을 포함하여 엔진 호출의 다른 소스를 고려하는 것이 중요합니다.

  여기에서 Adobe Campaign Standard 패키지 정보를 보십시오. [https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html)

* 통합은 Campaign의 리소스에 대한 초기 동기화에 대해 최대 1,500만 개의 총 레코드를 지원합니다. 증분 동기화는 Adobe Campaign Standard 패키지에 의해 제한됩니다.

* 표준 통합 기능에는 각각 최대 50개의 열 크기를 가진 최대 20개의 사용자 지정 엔터티에 대한 지원이 포함됩니다.

* 통합을 구현하기 전에 사용자 지정 리소스를 만들고 게시해야 합니다.

* 테이블을 연결할 때 최대 테이블 깊이는 두 개입니다(예: table1->table2->table3).

* 통합은 사용자 지정 리소스당 최대 5개의 연결된 열을 지원합니다. 사용자 지정 리소스 간에 여러 열을 연결하면 성능에 큰 영향을 줄 수 있습니다. **0 또는 1개의 카디널리티 단순 링크**&#x200B;가 **1개의 카디널리티 단순 링크**&#x200B;보다 선호됩니다.

* 이 통합은 기본 Microsoft Dynamics 365 데이터 유형(부울, 정수, 십진수, 실수, 문자열, 날짜 시간, 날짜)과 Adobe Campaign Standard 데이터 유형(정수, 부울, 부동, 실수, 날짜, 날짜, 날짜, 날짜, 시간, 문자열) 간의 변환을 지원합니다. 고급 데이터 유형은 문자열로 해석되고 그대로 동기화됩니다.

* Adobe과 고객 간에 온보딩 유지 관리 기간을 설정해야 할 수 있습니다.

* 통합 사용의 현저한 증가 또는 &quot;스파이크&quot;(예: 신규 또는 업데이트된 레코드의 급격한 증가)는 데이터 동기화 속도를 저하할 수 있습니다.

* 통합의 일부로 Microsoft Azure 및 Dynamics 365의 통합 전 구성 단계를 완료해야 합니다. 이 페이지에서 구성 단계 [을(를) 참조하십시오](../../integrating/using/d365-acs-configure-d365.md)

* Dynamics 365 및 Campaign 데이터 모델을 통합으로 가져와 유지 관리할 수 있습니다.

### 통합 경계

이 통합은 Microsoft Dynamics 365와 Campaign 간의 일반적인 데이터 이동 사용 사례를 해결하기 위해 고안되었지만 각 고객에게만 해당되는 모든 사용 사례를 해결하기 위해 고안된 것은 아닙니다.

* 통합은 개인 정보(예: GDPR) 삭제를 발행하지 않습니다. 최종 사용자 개인 정보 보호 요청을 이행하는 책임은 고객에게 있습니다. 이러한 요청은 Campaign(Adobe Experience Platform Privacy Service을 통해)과 Dynamics 365에서 독립적으로 수행되어야 합니다. 원하는 경우 통합에서 데이터 동기화에 도움이 되도록 정기적인 삭제를 실행할 수 있습니다.   자세한 내용은 [개인 정보 섹션](#manage-privacy-requests)을(를) 검토하세요.

* 옵트아웃 정보(고객이 구성한 경우)를 제외하고 프로필 또는 사용자 지정 엔티티 데이터가 Campaign에서 Dynamics 365로 동기화되지 않습니다.

* Campaign 구독 관리(즉, 구독/구독 취소)는 기본적으로 지원되지 않습니다.

* Dynamics 365 내에서 Campaign 이메일 캠페인을 작성 및 트리거할 수 없습니다.

* 통합은 Dynamics 365와 Campaign Standard 데이터 모델 간의 데이터 리모델링을 지원하지 **않습니다**. 통합에서 하나의 Dynamics 365 테이블을 하나의 Campaign 테이블로 동기화해야 합니다.
