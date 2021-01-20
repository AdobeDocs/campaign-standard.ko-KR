---
title: '통합 도구 시작하기 '
description: 통합 도구 시작하기
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: 1e05db3fecc87a026750f40acb0ff063706e3f38
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 2%

---


# 셀프 서비스 통합 앱 {#gs-self-service-app} 시작하기

Microsoft Dynamics 365 셀프 서비스 통합 애플리케이션과 Adobe Campaign Standard의 통합을 통해 데이터 흐름을 구성하고 실행 여부와 환경을 제어할 수 있습니다. 그러나 셀프 서비스 통합 응용 프로그램을 사용하기 전에 일부 사전 요구 사항을 완료해야 합니다.

## 개념 및 제한 사항 {#concepts-and-restrictions}

통합 툴을 사용하기 전에 통합 관련 개념과 지침을 이해하고 초기 단계에 따라 액세스할 수 있어야 합니다.

다음 섹션에서 자세한 내용을 살펴보십시오.

* [Microsoft Dynamics 365 통합 시작](../../integrating/using/d365-acs-get-started.md)
* [통합 모범 사례 및 제한 사항](../../integrating/using/d365-acs-notices-and-recommendations.md)
* [이 통합을 구현하는 주요 단계를 알아봅니다.](../../integrating/using/d365-acs-get-started.md#request-and-implement-this-integration)
* [Microsoft Dynamics 365 통합 사용](../../integrating/using/d365-acs-using-the-integration.md)

## 사전 요구 사항 {#self-service-app-prerequisites}

통합 앱에서 데이터에 액세스할 수 있도록 Microsoft Dynamics 365 및 Adobe Campaign Standard을 구성해야 합니다. Dynamics 365, Adobe Campaign Standard 및 Adobe I/O에서 구성하는 데 시간이 다소 소요됩니다.그러나 구성 후에는 셀프 서비스 통합 애플리케이션의 사용자 인터페이스를 통해 통합을 제어할 수 있습니다.

다음 섹션에서 자세한 내용을 살펴보십시오.

* [Campaign 통합을 위해 Microsoft Dynamics 365 구성](../../integrating/using/d365-acs-configure-d365.md)
* [Adobe I/O 구성](../../integrating/using/d365-acs-configure-adobe-io.md)
* [캠페인 사용자 지정 리소스 및 Microsoft Dynamics 365 사용자 지정 엔터티 매핑](../../integrating/using/d365-acs-notices-and-recommendations.md)

## 셀프 서비스 통합 앱 {#self-service-app-configuration-steps} 구성을 위한 주요 단계

그런 다음 통합 도구로 시작할 수 있습니다. 다음 단계를 수행합니다.

1. [통합 앱 이용](../../integrating/using/d365-acs-self-service-app-control-access.md)
1. [사용용으로 통합 앱 구성](../../integrating/using/d365-acs-self-service-app-settings.md)
1. [데이터 동기화 구현](../../integrating/using/d365-acs-self-service-app-data-sync.md)
1. [동기화 워크플로우 구성](../../integrating/using/d365-acs-self-service-app-workflows.md)

## 통합 앱 {#self-service-app-link} 링크

브라우저를 열고 해당 지역과 연결된 커넥터를 찾습니다.

* [아시아 태평양](http://d365-acs-ap.ea.adobe.com/)
* [유럽, 중동 또는 아프리카(EMEA)](http://d365-acs-em.ea.adobe.com/)
* [아메리카](http://d365-acs-na.ea.adobe.com/)

## 개인 정보 요청 확인 {#self-service-app-acknowledgement}

셀프 서비스 UI를 처음으로 검색할 때 개인 정보 확인 메시지가 표시됩니다. 계속하기 전에 Campaign 및 Microsoft Dynamics 365에서 개인 정보 요청을 수행하는 데 있어 자신의 역할을 개별적으로 이해한다는 점을 인정해야 합니다.
[이 섹션](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy)에서 개인 정보 보호 요청을 관리하는 방법에 대한 자세한 내용을 살펴보십시오.

## 자격 증명 {#self-service-app-credentials} 설정

처음으로 UI를 검색할 때 다음과 같은 헤더가 있는 페이지가 표시됩니다.

![](assets/d365-to-acs-ui-header.png)

>[!NOTE]
>
> 앱 설정이 아직 구성되지 않은 경우 Adobe Campaign Standard 또는 Microsoft Dynamics 365에 &quot;연결할 수 없습니다&quot;라는 경고가 표시되는 것이 정상입니다.

&quot;ORG&quot; 및 &quot;INSTANCE&quot; 선택 사항이 구성하려는 항목인지 확인하십시오.  그렇지 않은 경우 드롭다운 목록을 클릭하고 올바른 조직과 인스턴스를 선택합니다.

>[!IMPORTANT]
>
> 처음 커넥터를 구성하거나 이 프로세스를 처음 사용하는 경우, **strongly**&#x200B;에 &quot;stage&quot; 또는 &quot;dev&quot; 인스턴스를 선택해야 합니다. 프로덕션에서 설정을 시도하기 전에 구성이 제대로 작동하는지 확인해야 합니다.

올바른 조직과 인스턴스가 있는 경우 &quot;햄버거&quot; 메뉴를 클릭하여 드롭다운 메뉴를 표시합니다. 그런 다음 드롭다운 메뉴에서 **[!UICONTROL Settings...]**&#x200B;을 클릭하여 Microsoft Dynamics 365 및 Campaign에 대한 자격 증명을 입력하는 페이지를 방문합니다(아래 참조).

![](assets/d365-to-acs-ui-page-workflows-menu-pointers.png)

**[!UICONTROL Settings]** 페이지에서 다음 섹션을 입력합니다.

* Microsoft Dynamics 365 자격 증명
* Adobe 자격 증명

각 입력에 대한 정보를 찾을 위치에 대한 자세한 정보를 보려면 [여기](../../integrating/using/d365-acs-self-service-app-settings.md)로 이동하십시오. 완료되면 맨 아래에 있는 **[!UICONTROL Save]** 단추를 클릭합니다.

## 초기 구성 {#self-service-app-initial-config} 확인

위의 전제 조건을 완료하고 자격 증명을 모두 올바르게 추가했다고 가정할 경우, 이제 **[!UICONTROL Workflows]** 페이지로 이동합니다. [이 페이지](../../integrating/using/d365-acs-self-service-app-workflows.md)의 통합 앱 작업 과정에 대해 자세히 알아보십시오.

**[!UICONTROL Workflows]** 페이지에서 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로우와 연관된 연필 아이콘을 클릭하여 구성을 편집합니다.

![](assets/d365-to-acs-ui-page-workflows-ingress-edit-pointer.png)

**[!UICONTROL Microsoft Dynamics 365 to Campaign]** 페이지에서 구성한 테이블 매핑 목록에 액세스할 수 있습니다.  기본 연락처/프로필 매핑이 기본적으로 설정되어 있습니다. 다른 모든 사용자 지정 엔터티는 별도로 구성해야 합니다.

![](assets/d365-to-acs-ui-page-ingress-top-pointers.png)

**[!UICONTROL Edit Table Mapping]** 페이지에서 **[!UICONTROL Mappings]** 섹션을 확인하여 Microsoft Dynamics 365의 필드가 Campaign의 올바른 필드에 매핑되고 있는지 확인합니다. 다른 매핑을 추가해야 하는 경우 이제 바꾸거나 필터뿐만 아니라 다른 매핑도 추가합니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md)

새 매핑을 추가하려면 [이 섹션](../../integrating/using/d365-acs-self-service-app-data-sync.md#add-a-new-mapping)을 참조하십시오.

구성이 올바르면 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 워크플로 옆의 **[!UICONTROL Play]** 단추를 클릭하여 통합 및 데이터 흐름을 시작합니다.

>[!IMPORTANT]
>
>**strongly**&#x200B;에서는 프로덕션 환경에서 실행하기 전에 먼저 스테이지나 개발 환경에서 이 작업을 실행하는 것이 좋습니다. 헤더에서 단계/개발 인스턴스가 선택되었는지 확인하십시오.


![](assets/d365-to-acs-ui-page-workflows-ingress-play-pointer.png)

실행 후에는 Microsoft Dynamics 365에서 항목을 추가 또는 수정하고 몇 분 내에 Adobe Campaign에서 이러한 변경 사항을 준수하여 테스트할 수 있습니다. 언제든지 이 프로세스를 중지해야 하는 경우 동일한 버튼을 눌러 중단하면 됩니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-workflows.md#workflow-status)


## 통합 앱 작업 공간 {#self-service-app-workspace}

### 앱 헤더 {#app-header}

셀프 서비스 앱 내의 헤더를 사용하여 현재 보고/또는 구성하고 있는 조직과 인스턴스를 정의할 수 있습니다.

보고 편집할 **ORG** 및 **INSTANCE**&#x200B;을 선택합니다. 이러한 필드는 읽기 전용으로 표시되지만 마우스 커서를 필드 위에 놓으면 편집할 수 있습니다.

머리글 오른쪽에 3개의 가로 줄 ![](assets/d365-to-acs-icon-hamburger.png)이 있는 단추를 클릭하면 드롭다운 메뉴가 표시됩니다.

드롭다운 메뉴의 항목은

* **설정**:이 옵션을 선택하면 Microsoft Dynamics 365 및 Adobe Campaign에 대한 API 자격 증명과 애플리케이션에 대한 다른 일반 설정을 지정할 수 있는 화면이 표시됩니다.

* **설명서**:이 옵션은 이 통합 관련 Adobe Campaign 문서에 대한 링크입니다

* **고객 지원**:고객 지원 티켓 열기와 관련된 Experience Cloud 설명서에 대한 링크입니다.

* **로그아웃**:애플리케이션에서 로그아웃되어 다른 사용자로 다시 로그인할 수 있습니다.

* **정보**:저작권 정보를 포함하여 응용 프로그램에 대한 정보가 포함된 대화 상자가 표시됩니다.

### 탐색 표시 {#app-breadcrumbs}

앱을 탐색할 때 일부 화면 상단에 탐색 표시가 나타납니다.

**예제:**

다음은 탐색 표시 및 페이지 제목을 표시하는 **[!UICONTROL Edit Table Mapping]** 화면의 예입니다. 이 경우 **[!UICONTROL Workflows]** 또는 **[!UICONTROL Microsoft Dynamics 365 to Campaign]** 텍스트를 클릭하여 이전 화면 중 하나로 이동할 수 있습니다. **[!UICONTROL Edit Table Mapping]** 탐색 표시는 현재 화면이므로 이 경우 클릭할 수 없습니다.

![](assets/d365-to-acs-breadcrumbs-ingress.png)

### 공통 단추 {#app-buttons}

다음 아이콘은 셀프 서비스 앱의 여러 페이지에 사용됩니다.

![](assets/d365-to-acs-icon-add.png) - 목록에 새 항목을 추가합니다.

![](assets/d365-to-acs-icon-edit.png) - 이미 존재하는 항목 편집

![](assets/d365-to-acs-icon-delete.png) - 항목 목록에서 항목 삭제
