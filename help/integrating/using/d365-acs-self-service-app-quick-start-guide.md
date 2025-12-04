---
title: 통합 도구 시작
description: 통합 도구 시작
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: e73e2069-e86d-4be2-bf73-22e6dc164340
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# 셀프서비스 통합 앱 시작 {#gs-self-service-app}

Microsoft Dynamics 365 셀프서비스 통합 애플리케이션과 Adobe Campaign Standard을 통합하면 데이터 흐름을 구성하고, 실행 여부 및 환경을 제어할 수 있습니다. 그러나 셀프 서비스 통합 응용 프로그램을 사용하기 전에 몇 가지 전제 조건을 완료해야 합니다.

## 개념 및 제한 사항 {#concepts-and-restrictions}

통합 도구를 시작하기 전에 통합과 관련된 개념과 가드레일을 이해하고 액세스 권한을 받기 위한 몇 가지 초기 단계를 수행해야 합니다.

다음 섹션에서 자세히 알아보기:

* [Microsoft Dynamics 365 통합 시작](../../integrating/using/d365-acs-get-started.md)
* [통합 우수 사례 및 제한 사항](../../integrating/using/d365-acs-notices-and-recommendations.md)
* [이 통합을 구현하는 주요 단계 알아보기](../../integrating/using/d365-acs-get-started.md#request-and-implement-this-integration)
* [Microsoft Dynamics 365 통합 사용](../../integrating/using/d365-acs-using-the-integration.md)

## 필수 구성 요소 {#self-service-app-prerequisites}

통합 앱이 데이터에 액세스할 수 있도록 Microsoft Dynamics 365 및 Adobe Campaign Standard을 구성해야 합니다. Dynamics 365, Adobe Campaign Standard 및 Adobe I/O에서 구성하는 데 시간이 다소 걸리지만 구성하고 나면 셀프 서비스 통합 애플리케이션의 사용자 인터페이스를 통해 통합을 제어할 수 있습니다.

다음 섹션에서 자세히 알아보기:

* [Campaign 통합을 위해 Microsoft Dynamics 365 구성](../../integrating/using/d365-acs-configure-d365.md)
* [Adobe I/O 구성](../../integrating/using/d365-acs-configure-adobe-io.md)
* [Campaign 사용자 지정 리소스 및 Microsoft Dynamics 365 사용자 지정 엔터티 매핑](../../integrating/using/d365-acs-notices-and-recommendations.md)

## 셀프서비스 통합 앱을 구성하는 주요 단계 {#self-service-app-configuration-steps}

그런 다음 통합 도구로 시작할 수 있습니다. 아래 단계를 따르십시오.

1. [통합 앱에 액세스](../../integrating/using/d365-acs-self-service-app-control-access.md)
1. [사용을 위한 통합 앱 구성](../../integrating/using/d365-acs-self-service-app-settings.md)
1. [데이터 동기화 구현](../../integrating/using/d365-acs-self-service-app-data-sync.md)
1. [동기화 워크플로우 구성](../../integrating/using/d365-acs-self-service-app-workflows.md)

## 통합 앱에 연결 {#self-service-app-link}

브라우저를 열고 지역과 연관된 커넥터를 찾습니다.

* [아시아 태평양](https://d365-acs-ap.ea.adobe.com/)
* [유럽, 중동 또는 아프리카(EMEA)](https://d365-acs-em.ea.adobe.com/)
* [아메리카](https://d365-acs-am.ea.adobe.com/)

## 개인 정보 보호 요청 승인 {#self-service-app-acknowledgement}

셀프서비스 UI를 처음 탐색하면 개인 정보 보호 승인이 표시됩니다. 계속하려면 먼저 Campaign 및 Microsoft Dynamics 365에서 개별적으로 개인 정보 보호 요청을 수행하는 역할을 이해했음을 확인해야 합니다.
개인 정보 보호 책임에 대해 자세히 알아보고 [이 섹션](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy)에서 개인 정보 보호 요청을 관리하는 방법에 대해 자세히 알아보세요.

## 자격 증명 설정 {#self-service-app-credentials}

UI를 처음 탐색하면 다음과 같은 머리글이 있는 페이지가 표시됩니다.

![](assets/do-not-localize/d365-to-acs-ui-header.png)

>[!NOTE]
>
> 앱 설정이 아직 구성되지 않은 경우 Adobe Campaign Standard 또는 Microsoft Dynamics 365에 &quot;연결할 수 없음&quot;이라고 언급하는 경고를 받는 것이 일반적입니다.

&quot;ORG&quot; 및 &quot;INSTANCE&quot; 선택 항목이 구성할 것인지 확인하십시오.  그렇지 않은 경우 드롭다운 목록을 클릭하고 올바른 조직과 인스턴스를 선택합니다.

>[!IMPORTANT]
>
> 커넥터를 처음 구성하는 경우 및/또는 이 프로세스를 처음 사용하는 경우 **강력하게**&#x200B;하여 &quot;stage&quot; 또는 &quot;dev&quot; 인스턴스를 선택해 주십시오. 프로덕션에서 설정을 시도하기 전에 구성이 제대로 작동하는지 확인해야 합니다.

올바른 조직과 인스턴스가 있는 경우 &quot;햄버거&quot; 메뉴를 클릭하여 드롭다운 메뉴를 표시합니다. 그런 다음 드롭다운 메뉴에서 **[!UICONTROL Settings...]**&#x200B;을(를) 클릭하여 Microsoft Dynamics 365 및 Campaign에 대한 자격 증명을 입력하는 페이지를 방문합니다(아래 참조).

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-menu-pointers.png)

**[!UICONTROL Settings]** 페이지에서 다음 섹션을 작성하십시오.

* Microsoft Dynamics 365 자격 증명
* Adobe 자격 증명

각 입력에 대한 정보를 찾을 수 있는 위치에 대한 자세한 정보를 보려면 [여기](../../integrating/using/d365-acs-self-service-app-settings.md)로 이동하십시오. 완료되면 하단의 **[!UICONTROL Save]** 단추를 클릭합니다.

## 초기 구성 확인 {#self-service-app-initial-config}

위의 필수 구성 요소를 완료하고 모든 자격 증명을 올바르게 추가했다고 가정할 경우 이제 **[!UICONTROL Workflows]** 페이지로 이동하겠습니다. [이 페이지](../../integrating/using/d365-acs-self-service-app-workflows.md)에서 통합 앱 워크플로에 대해 자세히 알아보세요.

**[!UICONTROL Workflows]** 페이지에서 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로와 연결된 연필 아이콘을 클릭하여 해당 구성을 편집합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-ingress-edit-pointer.png)

**[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에서 구성한 테이블 매핑 목록에 액세스할 수 있습니다.  기본 담당자/프로필 매핑이 기본 설정됩니다. 다른 모든 사용자 지정 엔터티는 별도로 구성해야 합니다.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-top-pointers.png)

**[!UICONTROL Edit Table Mapping]** 페이지에서 **[!UICONTROL Mappings]** 섹션을 확인하여 Microsoft Dynamics 365의 필드가 Campaign의 올바른 필드에 매핑되어 있는지 확인하십시오. 다른 매핑을 추가해야 하는 경우 대체 요소나 필터뿐만 아니라 지금 추가합니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md)

새 매핑을 추가하려면 [이 섹션](../../integrating/using/d365-acs-self-service-app-data-sync.md#add-a-new-mapping)을 참조하세요.

구성이 올바르면 **[!UICONTROL Play]** 워크플로 옆에 있는 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 단추를 클릭하여 통합 및 데이터 흐름을 시작합니다.

>[!IMPORTANT]
>
>프로덕션에서 실행하기 전에 스테이징 또는 개발 환경에서 먼저 실행하는 것이 **좋습니다**. 헤더에서 단계/개발 인스턴스가 선택되어 있는지 확인하십시오.
>

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-ingress-play-pointer.png)

실행 후 몇 분 안에 Microsoft Dynamics 365에서 항목을 추가하거나 수정하고 Adobe Campaign에서 이러한 변경 사항을 관찰하여 테스트할 수 있습니다. 언제든지 이 프로세스를 중지해야 하는 경우 동일한 버튼을 눌러 중지하면 됩니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-workflows.md#workflow-status)


## 통합 앱 작업 영역 {#self-service-app-workspace}

### 앱 헤더 {#app-header}

셀프서비스 앱 내의 헤더를 통해 현재 보고 및/또는 구성 중인 조직 및 인스턴스를 정의할 수 있습니다.

보거나 편집할 **조직** 및 **인스턴스**&#x200B;을(를) 선택하십시오. 이러한 필드는 읽기 전용으로 표시되지만 마우스 커서를 위에 놓으면 편집할 수 있습니다.

머리글 오른쪽에 세 개의 가로줄이 ![](assets//do-not-localize/d365-to-acs-icon-hamburger.png)인 단추를 클릭하면 드롭다운 메뉴가 표시됩니다.

드롭다운 메뉴의 항목은 다음과 같습니다.

* **설정**: 이 옵션을 선택하면 Microsoft Dynamics 365 및 Adobe Campaign에 대한 API 자격 증명과 응용 프로그램에 대한 기타 일반 설정을 지정할 수 있는 화면으로 이동합니다.

* **설명서**: 이 옵션은 이 통합과 관련된 Adobe Campaign 설명서에 대한 링크입니다

* **고객 지원 센터**: 고객 지원 센터 티켓 열기와 관련된 Experience Cloud 설명서에 대한 링크입니다

* **로그아웃**: 이 경우 응용 프로그램에서 로그아웃되고 다른 사용자로 다시 로그인할 수 있습니다.

* **정보**: 저작권 정보를 포함하여 응용 프로그램에 대한 정보가 포함된 대화 상자가 표시됩니다.

### 탐색 표시 {#app-breadcrumbs}

앱을 탐색할 때 일부 화면 상단에 이동 경로가 표시됩니다.

**예:**

다음은 이동 경로와 페이지 제목을 표시하는 **[!UICONTROL Edit Table Mapping]** 화면의 예입니다. 이 경우 **[!UICONTROL Workflows]** 또는 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 텍스트를 클릭하여 이전 화면 중 하나로 이동할 수 있습니다. 이 경우 이동 경로의 **[!UICONTROL Edit Table Mapping]**&#x200B;은(는) 현재 화면이므로 클릭할 수 없습니다.

![](assets/do-not-localize/d365-to-acs-breadcrumbs-ingress.png)

### 공통 버튼 {#app-buttons}

다음 아이콘은 셀프서비스 앱의 여러 페이지에서 사용됩니다.

![](assets/do-not-localize/d365-to-acs-icon-add.png) - 새 항목을 목록에 추가합니다.

![](assets/do-not-localize/d365-to-acs-icon-edit.png) - 이미 있는 항목 편집

![](assets/do-not-localize/d365-to-acs-icon-delete.png) - 항목 목록에서 항목 삭제
