---
solution: Campaign Standard
product: campaign
title: 캠페인 및 Microsoft Dynamics 365 데이터 관리
description: Campaign Standard 및 Microsoft Dynamics 365에서 일반적인 데이터를 관리하는 방법 살펴보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: cce30fd5cd3d5d63563d1dab3bb1e7554c26fb3e
workflow-type: tm+mt
source-wordcount: '2467'
ht-degree: 1%

---


# 모범 사례 및 제한 사항 {#acs-msdyn-best-practices}

## 데이터 관리 {#acs-msdyn-manage-data}

연락처 및 사용자 지정 엔터티 동기화의 경우 이 통합은 **Microsoft Dynamics 365를 진실**&#x200B;의 소스로 처리합니다.  동기화된 속성에 대한 변경 사항은 Adobe Campaign Standard이 아니라 Dynamics 365에서 수행해야 합니다.  동기화가 한 방향이므로 Campaign에서 변경하면 동기화 도중 Campaign에서 해당 변경 사항을 덮어쓸 수 있습니다.

데이터 무결성을 유지하기 위해 Dynamics 365에서 담당자가 삭제되면 Campaign에 대한 프로필 삭제 호출을 실행하도록 통합을 선택적으로 구성할 수 있습니다. 하지만 프로필 삭제는 개인 정보 삭제와 다릅니다. Campaign에서 개인 정보를 삭제하면 캠페인 프로필 레코드 및 관련 로그 항목이 제거됩니다.반면에, 일반 프로필 삭제는 캠페인 프로필 레코드만 삭제하며, 캠페인 로그에 남아 있습니다. 통합에서 프로필 삭제 기능이 활성화되면 데이터 주체의 개인 정보 보호 요청을 제대로 처리하기 위해 추가 단계를 수행해야 합니다. [개인 정보 섹션](#manage-privacy-requests)의 단계를 참조하십시오.

## 개인 정보{#acs-msdyn-manage-privacy}

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터를 전송하도록 설계되었습니다. 이 데이터에는 최종 사용자 데이터에 포함되어 있는 경우 개인 정보가 포함됩니다.  데이터 관리자로서, 귀하의 회사는 귀하의 개인 데이터 수집 및 사용에 적용되는 개인정보 보호 법 및 규정을 준수할 책임을 집니다.

이 통합은 Microsoft Dynamics 365와 Adobe Campaign Standard 간에 최종 사용자 데이터(최종 사용자 데이터에 포함되어 있는 경우 개인 정보를 포함하되 이에 제한되지 않음)를 전송하도록 설계되었습니다. 데이터 관리자로서, 귀하의 회사는 귀하의 개인 데이터 수집 및 사용에 적용되는 개인정보 보호 법 및 규정을 준수할 책임을 집니다.

통합은 데이터 주체의 개인 정보 보호(예: GDPR)를 발행하지 않으며, 다른 개인 정보 보호 요청도 삭제 또는 처리합니다(수신 거부 제외). 개인 정보 요청을 처리할 때는 Microsoft Dynamics 365와 Campaign(Adobe Experience Platform Privacy Service을 통해)에서 개별적으로 수행해야 합니다.

Dynamics 365에서 연락처를 삭제할 때 Campaign에 대한 일반 프로필 삭제 호출을 발생하도록 통합을 구성한 경우 아래 단계를 수행해야 합니다. 이 프로세스 동안 해당 레코드에 대한 업데이트가 수행되지 않도록 하십시오.

1. [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html)에 대한 개인 정보 삭제 요청을 발행합니다.

1. 요청이 성공적으로 완료될 때까지 요청 모니터링

1. 레코드가 더 이상 캠페인 인스턴스에 없는지 확인합니다.

1. (곧) Dynamics 365 내에서 개인 정보 삭제를 발행합니다.

1. 두 시스템에서 레코드가 제거되었는지 확인

아래는 각 시스템에서 액세스 및/또는 개인 정보 관련 요청을 삭제하는 데 도움이 되는 링크입니다.

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/)

* [Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)

>[!IMPORTANT]
>
>캠페인 사용자 지정 리소스 레코드에 고객의 캠페인 사용에 적용되는 개인 정보가 포함되어 있는 경우, 이러한 레코드는 해당 캠페인 프로필 레코드(직접 또는 다른 사용자 지정 리소스를 통해)에 연결되어 프로필 레코드에 있는 개인 정보 관련 삭제도 개인 정보가 포함된 연결된 사용자 지정 리소스 레코드를 삭제할 수 있습니다.연결된 레코드를 캐스케이드처럼 제거할 수 있도록 엔티티 간 연결 및 삭제 옵션을 구성해야 합니다. 개인 정보는 프로필과 연결되지 않은 사용자 지정 리소스에 입력해서는 안 됩니다.

## 옵트아웃 {#opt-out}

Microsoft Dynamics 365와 Campaign 간의 옵트아웃 속성 차이점과 각 고객의 비즈니스 요구 사항의 차이로 인해 옵트아웃 매핑이 고객의 완료에 대한 연습으로 남아 있습니다.  최종 사용자 옵트아웃 기본 설정이 유지되며 옵트아웃한 채널을 통해 통신이 수신되지 않도록 시스템 간에 옵트아웃을 올바르게 매핑해야 합니다.

옵트아웃 매핑에서는 다음 사항만 사용할 수 있습니다.

* &#39;더 이상 연락하지 않음&#39; 접두사가 붙은 캠페인 속성(예: 더 이상 이메일에 연락하지 않음) 또는

* CPA에 대한 특정 속성

프로필 엔티티 필드에 대한 자세한 내용은 [여기](../../developing/using/datamodel-profile.md)를 참조하십시오.

Dynamics 365에서는 대부분의 옵트아웃 필드에 &quot;donot&quot; 접두어가 있지만 데이터 유형이 호환하는 경우 옵트아웃 목적으로 다른 속성을 사용할 수도 있습니다.

통합을 프로비저닝할 때 비즈니스에 필요한 옵트아웃 구성을 지정할 수 있습니다.

* **단방향(Microsoft Dynamics 365에서 캠페인)**:Dynamics 365는 옵트아웃을 위한 진실의 근원입니다. 옵트아웃 속성은 Dynamics 365에서 Campaign Standard으로 한 방향으로 동기화됩니다.
* **단방향(Campaign to Microsoft Dynamics 365)**:Campaign Standard은 옵트아웃을 위한 진실의 근원이다. 옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다.
* **양방향**:역학 365와 Campaign Standard은 모두 진실의 근원이다. 옵트아웃 속성은 Campaign Standard과 Dynamics 365 간에 양방향 동기화됩니다.

또는 시스템 간의 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 흐름을 비활성화할 수 있습니다.

양방향 옵트아웃 구성은 논리를 사용하여 두 시스템에 쓸 값을 결정합니다. 논리 구조는 두 시스템(Dynamics 365의 레코드 수준 변경, 캠페인의 속성 수준 변경) 간 타임스탬프를 비교하여 어떤 시스템이 사용되고 있는지 결정합니다. 캠페인에 최신 타임스탬프가 포함되어 있으면 캠페인 값이 우선합니다. Dynamics 365에 최신 타임스탬프가 포함되어 있거나 이러한 타임스탬프가 동일하면 opt-out=TRUE가 반환됩니다(값 중 하나가 TRUE라고 가정함).

[이 섹션](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf)에서 옵트인/아웃 옵션을 선택하는 방법에 대해 알아봅니다.

>[!NOTE]
>
>해당되는 경우, 여기에서 변경하기 전에 Adobe Campaign의 기본 및 특정 유형 규칙을 검토하고 업데이트하여 이러한 변경 사항이 나가는 모든 통신에 올바르게 적용되는지 확인하십시오. 예를 들어 옵트아웃 기본 설정에 대한 매핑이 받는 사람의 의도/통신 선택 사항을 정확하게 반영하고 고객 주문 확인과 같은 거래 메시지 또는 관계 제공을 실수로 중단하지 않도록 하십시오.

**양방향** 또는 **단방향(Microsoft Dynamics 365로의 캠페인)** 옵트아웃 구성을 선택한 경우 캠페인 옵트아웃 데이터는 캠페인 SFTP 저장 영역에 대한 워크플로우를 통해 정기적으로 내보내집니다(&quot;아래의 캠페인 SFTP 사용량&quot; 참조). 캠페인 옵트아웃 워크플로의 실행이 중단된 경우, 옵트아웃 동기화 실패 가능성을 줄이기 위해 되도록 빨리 수동으로 다시 시작해야 합니다.

>[!IMPORTANT]
>
>**양방향** 또는 **단방향(Microsoft Dynamics 365로의 캠페인)** 옵트아웃 구성이 필요한 경우 캠페인 인스턴스에 설정할 옵트아웃 워크플로에 대해 Adobe 기술 담당자에게 요청해야 합니다

## 캠페인 SFTP 사용

아래 사용 사례의 통합으로 캠페인 SFTP 저장소를 활용해야 합니다.  SFTP 계정에 이러한 사용 사례를 수용할 수 있는 충분한 저장 공간이 있는지 확인해야 합니다. 라이선스가 부여된 SFTP 스토리지 용량을 초과하는 경우 Campaign, 통합 및/또는 SFTP 계정의 기능 사용에 심각한 문제가 발생할 수 있습니다.

| 사용 사례 | 설명 |
|---|---|
| 양방향 및 단방향(Campaign to Microsoft Dynamics 365) | 양방향 및 단방향(Campaign to Microsoft Dynamics 365) 옵트아웃 데이터 플로우는 캠페인 SFTP 저장소를 사용합니다. 캠페인 워크플로우는 증분 변경 내용을 SFTP 폴더로 내보냅니다. 여기에서 통합은 레코드와 프로세스를 선택합니다. |
| 옵트아웃 로그 | 통합 문제를 해결할 때 커넥터의 출력 로그가 유용합니다. 출력 로그는 켜기/끄기로 전환할 수 있습니다. |


>[!IMPORTANT]
>
>SFTP 폴더에서 액세스 및 다운로드한 정보에 대한 책임은 사용자에게 있습니다. 정보에 개인 데이터가 포함되어 있는 경우, 귀하는 해당 개인정보 보호 법 및 규정을 준수할 책임을 집니다. [자세히 알아보기](#acs-msdyn-manage-privacy)

## 데이터 관리

### 기존 캠페인 데이터

이 통합은 Microsoft Dynamics 365의 연락처와 사용자 지정 개체를 Campaign과 동기화합니다. 통합 외부에서 만들어진 캠페인 레코드(즉, 동기화 작업에서 만들어지지 않음)는 통합 구성 시 존재하는 캠페인 레코드를 포함하여 통합에 의해 수정되지 않습니다.

이 통합은 캠페인의 **[!UICONTROL externalId]** 필드를 사용하여 Dynamics 365 연락처 레코드와 캠페인 프로필 레코드를 동기화하므로 Microsoft Dynamics 365에서 동기화할 레코드에 대해 이 캠페인 필드(**[!UICONTROL externalId]**)를 Microsoft Dynamics 365 **[!UICONTROL contactId]**&#x200B;로 채워야 합니다.  사용자 지정 엔터티도 Microsoft Dynamics 365 고유 ID를 사용하여 동기화됩니다. Campaign 사용자 지정 엔티티는 이 ID 속성을 테이블 열로 포함해야 합니다. externalId 열을 사용하여 이 속성 값을 저장할 수 있지만 Campaign 사용자 지정 엔터티에는 필요하지 않습니다.

Microsoft Dynamics 365는 여전히 진실의 소스이며 통합이 Dynamics 365쪽에서 업데이트를 감지하면 캠페인 프로필 데이터를 덮어쓸 수 있습니다.  기존 배포에 따라 통합을 활성화하는 데 필요한 다른 단계가 있을 수도 있습니다.따라서 Adobe 기술 담당자와 긴밀하게 협력할 것을 권장합니다.

>[!NOTE]
>
>기존 고객 배포의 복잡성 때문에 통합을 계획 및 설정할 때 Adobe 기술 담당자와 함께 작업하는 것이 좋습니다.

### 데이터 동기화 빈도

통합은 Microsoft Dynamics 365(일괄 처리가 아닌 스트리밍)에서 업데이트가 발생하고 바로 처리 &quot;대기열&quot;에 추가되도록 허용하는 아키텍처를 활용합니다. 이러한 이유로 데이터 흐름 실행 빈도 또는 일정을 지정할 필요가 없습니다.

이에 대한 예외는 양방향 및 Campaign에서 Dynamics 365 옵트아웃 데이터 플로우입니다. 이러한 옵트아웃 구성의 경우 업데이트된 캠페인 레코드는 매일 한 번 캠페인 워크플로우를 통해 SFTP로 내보내지며 통합 도구가 파일을 읽고 레코드를 처리합니다.

### 데이터 사용 계약

EMEA 또는 APAC 지역에 거주하는 경우, 이 통합의 일부로 일부 데이터가 미국에서 처리됩니다. 자세한 정보는 [이 섹션](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement)을 참조하십시오.

## 가드레일 및 제한 사항

>[!IMPORTANT]
>
>부품의 특정 작업(예: 레코드 초기 인제스트, 레코드 데이터 재재생 등) Microsoft Dynamics 365에서 Adobe Campaign 인스턴스로 인제스트된 레코드가 대량으로 로드될 수 있습니다. 성능 문제의 위험을 줄이기 위해 모든 캠페인 프로세스를 중지하는 것이 좋습니다(예: 마케팅 활동 없음, 워크플로우 실행 안 함 등). 대량의 레코드를 Campaign으로 인제스트한 후까지.

### 맞춤형 엔티티

[Microsoft Dynamics 365-Adobe Campaign Standard 통합](../../integrating/using/d365-acs-get-started.md)은 사용자 지정 개체를 지원하므로 Dynamics 365의 사용자 지정 엔터티가 Campaign의 해당 사용자 지정 리소스와 동기화될 수 있습니다.

통합은 연결된 테이블과 연결되지 않은 테이블을 모두 지원합니다.

사용자 지정 엔티티 데이터 흐름을 구성할 때 다음을 알아야 합니다.

* Campaign 사용자 지정 리소스를 만들고 수정하는 것은 전문가 사용자에게만 수행해야 하는 중요한 작업입니다.
* 사용자 지정 엔터티 데이터 플로우의 경우 동기화된 사용자 지정 엔터티에 대해 Dynamics 365 내에서 변경 추적을 활성화해야 합니다.
* 통합의 병렬 처리로 인해 상위 레코드와 연결된 하위 레코드가 Dynamics 365에서 거의 같은 시간에 만들어지는 경우 새 하위 레코드를 부모 레코드 전에 Campaign에 기록할 수 있는 가능성이 약간 있습니다.

* 상위 및 하위가 **1 카디널리티 단순 링크** 옵션을 사용하여 캠페인 측에 연결된 경우, 상위 레코드가 Campaign에 도착할 때까지 하위 레코드는 숨겨지고 액세스할 수 없게 됩니다(UI 또는 API를 통해).

* (캠페인에서 **1 카디널리티 단순 링크**&#x200B;라고 가정함) Dynamics 365에서 하위 레코드가 업데이트되거나 삭제되고 상위 레코드가 캠페인에 표시되기 전에 해당 변경이 캠페인에 기록되면(그럴 가능성은 없지만 원격 가능성) 해당 업데이트 또는 삭제가 Campaign에서 처리되지 않고 오류가 발생합니다. 업데이트되는 경우 업데이트된 레코드를 동기화하려면 문제의 레코드를 Dynamics 365에서 다시 업데이트해야 합니다. 삭제의 경우 삭제 또는 업데이트에 필요한 Dynamics 365의 레코드가 더 이상 없으므로 해당 레코드를 캠페인 측에서 별도로 처리해야 합니다.

* 숨겨진 자식 레코드가 있고 액세스할 방법이 없는 경우에 발생하는 경우, 일시적으로 카디널리티 링크 유형을 **0 또는 1 카디널리티 단순 링크**&#x200B;로 변경하여 해당 레코드에 액세스할 수 있습니다.

캠페인 사용자 지정 리소스의 보다 포괄적인 개요는 이 섹션](../../developing/using/key-steps-to-add-a-resource.md)에서 [을 참조할 수 있습니다.

### 통합 가드레일

이 통합을 사용할 계획이라면 다음 지침을 고려해야 합니다. 이러한 보증서를 초과한다고 생각되면 Adobe 기술 담당자에게 문의하십시오.

* 통합으로 생성된 엔진 호출 볼륨을 지원하기 위해 적절한 캠페인 패키지에 라이선스를 부여해야 합니다. 라이센스가 있는 엔진 호출 볼륨을 초과하면 캠페인 성능이 저하될 수 있습니다.

   통합에서 엔진 호출 볼륨을 예상하는 데 도움이 되도록 다음을 사용하십시오.

   * 레코드 삽입(새 레코드):엔진 호출 1회
   * 레코드 삭제:엔진 호출 1회
   * 업데이트 기록:2개의 엔진 호출(대상 레코드가 소스 레코드와 동일한 경우(즉, 캠페인 레코드에 변경 사항이 없는 경우) 1개의 호출만)

   전체 캠페인 엔진 호출 볼륨을 계산할 때 랜딩 페이지, 웹 앱, JSSP, API, 모바일 앱 등록 등을 비롯한 다른 엔진 호출 소스를 고려하는 것이 중요합니다.

   다음 사이트에서 캠페인 패키지 정보를 봅니다.https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html

* 통합은 최대 3천만 명의 연락처를 지원합니다.

* 표준 통합 서비스에는 최대 5개의 사용자 정의 엔티티에 대한 지원이 포함되어 있으며 각 엔티티는 최대 50개의 열 크기로 제공됩니다.

* 통합을 구현하기 전에 사용자 지정 리소스를 만들고 게시해야 합니다.

* 테이블을 연결할 때의 최대 테이블 깊이는 2개입니다(예: table1->table2->table3).

* Microsoft Dynamic 365 데이터 유형에 대한 지원이 제한적입니다. 데이터 모델에 단순 데이터 유형(예: 문자열, 정수, 소수 등)이 아닌 데이터 유형이 포함되어 있는 경우 통합을 사용하기 전에 데이터 모델을 업데이트해야 할 수 있습니다.

* Campaign 사용자 지정 엔티티의 기존 데이터를 보존하도록 선택한 경우 통합을 위해 데이터를 준비해야 합니다.

* 온보딩 유지 관리 기간은 Adobe과 고객 사이에 수립되어야 할 수 있습니다.

* 통합 사용(예: 새 레코드 또는 업데이트된 레코드의 급격한 증가)에서 상당한 증가 또는 &quot;스파이크&quot;가 데이터 동기화를 지연시킬 수 있습니다.

* 통합의 일부로 Microsoft Azure 및 Dynamics 365의 사전 통합 구성 단계를 완료해야 합니다. 이 페이지에서 [구성 단계를 참조하십시오](../../integrating/using/d365-acs-configure-d365.md)

* Dynamics 365 및 Campaign 데이터 모델을 통합으로 가져오고 유지 관리하게 됩니다.

### 통합 경계

이 통합은 Microsoft Dynamics 365와 Campaign 간의 일반적인 데이터 이동 사례를 해결하기 위해 고안되었지만 각 고객별 모든 사용 사례를 해결하기 위한 것은 아닙니다.

* 통합은 개인 정보(예: GDPR)를 삭제하지 않습니다. 최종 사용자 개인 정보 보호 요청을 이행하는 책임은 고객에게 있습니다.이러한 요청은 Adobe Experience Platform Privacy Service을 통해 Campaign과 Dynamics 365의 모두에 독립적으로 해야 합니다. 원할 경우 데이터 동기화를 지원하기 위해 정기적으로 삭제를 실행할 수 있습니다.   자세한 내용은 [개인정보 보호 섹션](#manage-privacy-requests)을 검토하십시오.

* 옵트아웃 정보(고객이 구성한 경우)를 제외하고 Campaign에서 Dynamics 365로 프로필 또는 사용자 지정 엔티티 데이터가 동기화되지 않습니다.

* 캠페인 구독 관리(즉, 가입/가입 해지)는 기본적으로 지원되지 않습니다.

* Dynamics 365 내에서 캠페인 이메일 캠페인을 구성하고 트리거하는 것은 지원되지 않습니다.

* 통합은 Dynamics 365와 Campaign Standard 데이터 모델 간의 데이터 리모델링을 지원하지 **않습니다.** 하나의 Dynamics 365 테이블을 하나의 캠페인 테이블에 동기화해야 합니다.