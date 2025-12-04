---
title: Microsoft Dynamics 365 통합 사용
description: Microsoft Dynamics 365와 Campaign Standard 통합을 함께 사용하는 방법에 대해 알아봅니다
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: fb464183-13bf-4b47-ac27-4b785bafef37
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '1652'
ht-degree: 0%

---

# Microsoft Dynamics 365 통합 사용

Microsoft Dynamics 365와의 Adobe Campaign Standard 통합에서 수행하는 몇 가지 데이터 흐름이 있습니다. 이러한 흐름은 [이 페이지](../../integrating/using/d365-acs-self-service-app-workflows.md)에 자세히 설명되어 있습니다.

데이터 흐름에 대한 자세한 내용은 이 문서의 아래 [데이터 흐름](#data-flows) 섹션에서 확인할 수 있습니다.

## Adobe Campaign Standard 사용자 경험

Microsoft Dynamics 365에서 연락처를 작성, 수정 또는 삭제하면(삭제되는 경우) Campaign Standard으로 전송됩니다. 이러한 연락처는 Campaign의 프로필 화면에 표시되며 마케팅 캠페인에서 타겟팅할 수 있습니다. 아래의 프로필 화면을 참조하십시오.

![](assets/MSdynamicsACS-usage1.png)

Campaign에서 옵트아웃 특성이 수정되면 **단방향(Microsoft Dynamics 365에 대한 캠페인)** 또는 **양방향** 옵트아웃 구성을 선택한 경우 및 해당 특정 특성이 올바르게 매핑된 경우 Dynamics 365에 반영됩니다.

## Microsoft Dynamics 365 사용자 경험

이그레스의 경우 다음 이메일 마케팅 이벤트가 Campaign에서 Dynamics 365로 전송되고 Microsoft Dynamics 365 타임라인 보기에 사용자 지정 활동으로 표시됩니다.

* Adobe Campaign 이메일 보내기

* Adobe Campaign 이메일 열기

* Adobe Campaign 이메일 URL 클릭

* Adobe Campaign 이메일 바운스

연락처의 타임라인을 보려면 Dynamics 365 드롭다운 메뉴에서 Sales Hub를 클릭하여 연락처 목록으로 이동합니다. 그런 다음 왼쪽 메뉴 막대에서 연락처 를 클릭하고 연락처를 선택합니다.

>[!NOTE]
>
>이러한 이벤트를 보려면 AppSource의 **Microsoft Dynamics for Adobe Campaign 365** 앱을 Microsoft Dynamics 365 인스턴스에 설치해야 합니다. [자세히 알아보기](../../integrating/using/d365-acs-configure-d365.md#install-appsource-app)

아래에서 &quot;Dynamics 사용자&quot;에 대한 연락처 화면의 스냅샷을 볼 수 있습니다. 타임라인 보기에서 Dynamics 사용자에게 캠페인 이름 &quot;2019LoyaltyCamp&quot; 및 배달 이름 &quot;DM190&quot;과 연결된 이메일이 전송되었음을 알 수 있습니다. Dynamics 사용자는 이메일을 열고 이메일의 URL도 클릭했습니다. 이 두 작업 모두 아래에 표시되는 이벤트를 만들었습니다. 오른쪽 모서리에 있는 경우 관계 도우미(RA) 카드가 표시됩니다. 현재는 클릭한 URL을 후속 처리하는 작업이 포함되어 있습니다.

![](assets/do-not-localize/MSdynamicsACS-usage4.png)

Dynamics 사용자에 대한 타임라인 보기를 보려면 아래를 참조하십시오.

![](assets/do-not-localize/MSdynamicsACS-usage5.png)

다음은 관계 도우미(RA) 카드의 요약입니다. AppSource 앱에는 Adobe 이메일 URL 클릭 이벤트를 감시하는 워크플로가 포함되어 있습니다. 이 이벤트가 발생하면 작업이 생성되고 기한을 설정합니다. 이렇게 하면 작업이 RA 카드에 표시되어 추가 가시성을 제공합니다. Adobe 이메일 바운스 이벤트에 대해 유사한 워크플로우가 있으며 잘못된 이메일 주소를 조정하는 작업을 추가합니다. 솔루션에서 이러한 워크플로를 끌 수 있습니다.

![](assets/do-not-localize/MSdynamicsACS-usage6.png)

전송 이벤트의 제목을 클릭하면 아래 양식과 유사한 양식이 표시됩니다. 열기 및 바운스 이벤트의 양식은 유사합니다.

![](assets/do-not-localize/mirror_page_url_send.png)

이메일 URL 클릭 이벤트의 양식은 클릭한 URL에 대한 추가 속성을 추가합니다.

![](assets/do-not-localize/mirror_page_url_click.png)

다음은 속성 목록과 설명입니다.

* **제목**: 이벤트 제목, 이메일 게재의 캠페인 ID와 게재 ID로 구성

* **소유자**: 사후 프로비저닝 단계에서 생성된 응용 프로그램 사용자

* **관련 항목**: 연락처 이름

* **캠페인 이름**: Campaign Standard의 캠페인 ID

* **배달 이름**: Campaign Standard의 배달 ID

* **전송/열기/클릭/바운스된 날짜**: 이벤트가 만들어진 날짜/시간

* **추적 URL**: 클릭한 URL

* **미러 페이지 URL**: 전송/열기/클릭/반송된 전자 메일의 미러 페이지에 대한 URL입니다. 해당 캠페인 이메일 채널 활동의 구성 화면에서 이메일 미러 페이지의 만료 기간을 수정할 수 있습니다. [자세히 알아보기](../../administration/using/configuring-email-channel.md#validity-period-parameters)

>[!NOTE]
>
>옵트아웃의 경우 Microsoft Dynamics 365에서 옵트아웃 특성이 수정되면 **단방향(Microsoft Dynamics 365에 대한 캠페인)** 또는 **양방향** 옵트아웃 구성을 선택한 경우와 해당 특정 특성이 올바르게 매핑된 경우 Campaign에 반영됩니다.

## 데이터 흐름 {#data-flows}

### 연락처 및 사용자 지정 엔티티 인그레스

새 레코드, 업데이트 레코드 및 삭제된 레코드(참고: 삭제된 레코드를 활성화해야 함)가 Microsoft Dynamics 365 연락처 테이블에서 Campaign 프로필 테이블로 전송됩니다.

통합 애플리케이션 UI에서 테이블 매핑을 구성하여 Microsoft Dynamics 365 테이블 속성을 Campaign 테이블 속성에 매핑할 수 있습니다. 필요에 따라 테이블 매핑을 수정하여 속성을 추가/제거할 수 있습니다.

데이터 흐름의 초기 실행은 &quot;비활성&quot;으로 표시된 레코드를 포함하여 매핑된 모든 레코드를 전송하도록 설계되었습니다. 이후 통합은 증분 업데이트만 처리합니다. 데이터를 재생하거나 필터가 구성된 경우는 예외입니다. 기본, 속성 기반 필터링 규칙을 구성하여 Campaign에 동기화할 레코드를 결정할 수 있습니다.

기본 대체 규칙은 속성 값을 다른 값으로 대체하도록 통합 애플리케이션 UI에 구성할 수 있습니다(예: &quot;#00FF00&quot;의 경우 &quot;녹색&quot;, 1의 경우 &quot;F&quot; 등).

레코드의 볼륨에 따라 초기 데이터 전송을 위해 Campaign SFTP 저장소를 사용해야 할 수 있습니다. [자세히 알아보기](#initial-data-transfer)

연락처 인그레스가 작동하려면 Campaign 프로필 테이블 특성 externalId를 Dynamics 365 연락처 특성 contactId로 채워야 합니다. Campaign 사용자 지정 엔티티도 Dynamics 365 고유 ID 속성으로 채워야 합니다. 그러나 이 속성은 모든 Campaign 사용자 지정 엔티티 속성에 저장할 수 있습니다(즉, externalId가 아니어도 됨).

>[!NOTE]
>
>사용자 지정 엔티티 인그레스의 경우 동기화된 사용자 지정 엔티티에 대해 Dynamics 365 내에서 변경 내용 추적을 사용하도록 설정해야 합니다.

#### 사용자 지정 엔티티

[Microsoft Dynamics 365-Adobe Campaign Standard 통합](../../integrating/using/d365-acs-get-started.md)은(는) 사용자 지정 엔터티를 지원하므로 Dynamics 365의 사용자 지정 엔터티를 Campaign의 해당 사용자 지정 리소스와 동기화할 수 있습니다.

사용자 지정 리소스의 새 데이터는 세분화 및 개인화를 비롯한 여러 용도로 사용할 수 있습니다.

통합은 연결된 테이블과 연결되지 않은 테이블을 모두 지원합니다. 링크는 최대 3개 수준(예: level1->level2->level3)까지 지원됩니다.

>[!IMPORTANT]
>
>Campaign 사용자 지정 리소스 레코드에 개인 정보가 포함된 경우 특정 권장 사항이 적용됩니다. 자세한 내용은 [이 섹션](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-data)을 참조하세요.
>

사용자 지정 엔티티 데이터 흐름을 구성할 때는 다음 사항에 유의해야 합니다.

* Campaign 사용자 지정 리소스를 만들고 수정하는 작업은 전문가 사용자만 수행해야 하는 중요한 작업입니다.
* 사용자 지정 엔터티 데이터 흐름의 경우 동기화된 사용자 지정 엔터티에 대해 Dynamics 365 내에서 변경 내용 추적을 사용하도록 설정해야 합니다.
* 통합의 병렬 처리로 인해 Dynamics 365에서 부모 레코드와 연결된 자식 레코드가 거의 동시에 만들어지는 경우 새 자식 레코드가 부모 레코드보다 먼저 Campaign에 기록될 수 있습니다.

* 상위 레코드와 하위 레코드가 **1 카디널리티 단순 링크** 옵션을 사용하여 Campaign 측에서 연결된 경우 상위 레코드가 Campaign에 도착할 때까지 하위 레코드는 숨겨지고 액세스할 수 없습니다(UI 또는 API를 통해).

* (Campaign에서 **1 카디널리티 단순 링크** 가정) Dynamics 365에서 하위 레코드가 업데이트되거나 삭제되고 해당 변경 내용이 Campaign에 상위 레코드가 표시되기 전에 Campaign에 기록되는 경우(가능성이 높지 않지만 원격 가능성이 있음), 해당 업데이트 또는 삭제가 Campaign에서 처리되지 않고 오류가 발생합니다. 업데이트하는 경우 업데이트된 레코드를 동기화하려면 Dynamics 365에서 해당 레코드를 다시 업데이트해야 합니다. 삭제하는 경우 Dynamics 365에 삭제하거나 업데이트할 레코드가 더 이상 없으므로 해당 레코드는 캠페인 측에서 별도로 처리해야 합니다.

* 숨겨진 하위 레코드가 있고 이 레코드에 액세스할 수 없는 상황이 발생하는 경우 일시적으로 카디널리티 링크 형식을 **0 또는 1개의 카디널리티 단순 링크**(으)로 변경하여 해당 레코드에 액세스할 수 있습니다.

Campaign 사용자 지정 리소스에 대한 보다 포괄적인 개요는 이 섹션[에서 ](../../developing/using/key-steps-to-add-a-resource.md)을(를) 찾을 수 있습니다.

### 이메일 마케팅 이벤트 흐름{#email-marketing-event-flow}

이메일 마케팅 이벤트는 타임라인 보기에 표시되도록 Campaign에서 Microsoft Dynamics 365로 전송됩니다.

지원되는 마케팅 이벤트 유형:
* 보내기 - 수신자에게 전송된 이메일
* 열기 - 수신자가 연 이메일
* 클릭 - 수신자가 클릭한 이메일 내 URL
* 바운스 - 수신자 이메일에 하드 바운스가 발생했습니다.

Dynamics 365 내에 다음 이벤트 특성이 표시됩니다.
* 마케팅 캠페인 이름
* 이메일 게재 이름
* 타임스탬프
* 이메일 미러 페이지 URL
* 클릭한 URL(클릭 이벤트만)

전자 메일 마케팅 이벤트는 선택한 이벤트 유형만 Dynamics 365로 전달되도록 유형(보내기, 열기, 클릭, 바운스)별로 활성화/비활성화할 수 있습니다.

### 옵트아웃 흐름 {#opt-out-flow}

옵트아웃 (예: 차단 목록에 추가하다) 값은 시스템 간에 동기화됩니다. 온보딩 시 다음 옵션을 선택할 수 있습니다.

* **단방향(Microsoft Dynamics 365에서 Campaign으로)**: Dynamics 365는 옵트아웃에 대한 신뢰할 수 있는 소스입니다. 옵트아웃 속성은 Dynamics 365에서 Campaign Standard으로 한 방향으로 동기화됩니다.&quot;
* **단방향(Microsoft Dynamics 365에 대한 캠페인)**: Campaign Standard은 옵트아웃에 대한 올바른 소스입니다. 옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다.
* **양방향**: Dynamics 365와 Campaign Standard은 모두 신뢰할 수 있는 소스입니다. 옵트아웃 속성은 Campaign Standard과 Dynamics 365 간에 양방향으로 동기화됩니다.

또는 시스템 간의 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 흐름이 비활성화될 수 있습니다.

>[!NOTE]
>
>통합 애플리케이션 UI에서 **단방향(Microsoft Dynamics 365 - Campaign)** 및 **양방향** 옵트아웃 사용 사례는 별도의 옵트아웃 워크플로우에서 구성됩니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf)
>
>**단방향(Campaign to Microsoft Dynamics 365)** 옵트아웃 사용 사례는 예외입니다. 수신(프로필 연락처) 워크플로우 내에서 구성됩니다.
>

옵트아웃 흐름 매핑은 기업 간에 비즈니스 요구 사항이 다를 수 있으므로 고객이 지정합니다. Campaign 측에서는 OOTB 옵트아웃 속성만 옵트아웃 매핑에 사용할 수 있습니다.

* 차단 목록
* denyListEmail
* denyList팩스
* denyListMobile
* denyListPhone
* 거부 목록 우편 메일
* denyListPushnotification
* ccpaOptOut

Dynamics 365에서 대부분의 옵트아웃 필드에는 &quot;donot&quot; 접두사가 있지만 데이터 형식이 호환되는 경우 옵트아웃 목적으로 다른 속성을 활용할 수도 있습니다.

### 초기 데이터 전송 {#initial-data-transfer}

Microsoft Dynamics 365에서 수집하는 레코드 수에 따라 초기 데이터 전송에 시간이 걸릴 수 있습니다. 초기 데이터 전송 후 통합에서 증분 업데이트를 선택합니다.
