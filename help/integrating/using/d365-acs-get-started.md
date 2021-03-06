---
title: Microsoft Dynamics 365 통합 시작
description: Microsoft Dynamics 365 통합을 시작하는 방법 알아보기
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: fa0f790d-6a4d-4b83-a51f-f565e9545a1a
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 5%

---

# Microsoft Dynamics 365 통합 시작

채널 간 통신에서 CRM 데이터 활성화: Microsoft Dynamics 365에서 Adobe Campaign으로 연락처를 전달하고 캠페인 성능 데이터(전송, 열기, 클릭 및 바운스)를 Adobe Campaign에서 Microsoft Dynamics 365로 다시 공유하는 방법을 알아봅니다.

이 통합을 사용하려면 다음 소프트웨어 버전이 필요합니다.

* Sales Online용 Microsoft Dynamics 365, 최신 버전용

* Adobe Campaign Standard, 최신 버전

>[!CAUTION]
>
>이 기능은 제품의 일부로 기본 제공되지 않습니다. 구현하려면 Adobe Consulting 서비스가 필요합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

## 원칙

Microsoft Dynamics 365와 Adobe Campaign Standard 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다.

반대로 Adobe Campaign Standard 내의 프로필은 메시지와 상호 작용하므로 그러한 데이터(예: 전송, 열기, 클릭 수 및 바운스)가 Microsoft Dynamics 365로 자동 플로우되어 마케팅 활동에서도 연락처 레코드가 완료됩니다.

통합은 또한 활성화를 지원합니다 [사용자 지정 엔티티](../../integrating/using/d365-acs-self-service-app-settings.md) Dynamics 365에서 해당 **사용자 지정 리소스** 입니다.

이 통합은 다음 네 가지 주요 사용 사례를 지원하도록 설계되었습니다.

1. Dynamics 365에서 Campaign으로 연락처를 동기화하여 마케팅 캠페인에서 타겟팅할 수 있습니다
1. 사용자 지정 엔터티를 Dynamics 365에서 Campaign으로 동기화하여 세그멘테이션 및 개인화에 사용할 수 있습니다
1. Campaign에서 Dynamics 365로 이메일 마케팅 이벤트(전송, 열기, 클릭, 바운스)를 전송하여 Dynamics 365 인터페이스의 판매 리포지토리에 표시합니다
1. Dynamics 365와 Campaign 간의 옵트아웃(예: 이메일을 보내지 않음) 상태를 동기화하여 고객 개인 정보 보호 환경 설정을 유지합니다.

주요 이점은 다음과 같습니다.

* 영업 및 마케팅 간의 일관된 메시지: Dynamics 365와 Adobe Campaign Standard 통합을 통해 두 시스템 모두 고객 인사이트와 이메일 마케팅 기록에 액세스할 수 있으므로 고객에게 모든 메시지가 동일한 일관된 메시지를 공유할 수 있습니다.

* 모든 잠재 고객 및 고객 데이터의 전체적인 파악: Adobe Campaign Standard과 Dynamics 365를 통합하여 CRM 시스템 내에서 각 연락처에서 전자 메일 마케팅 내역을 공유 및 액세스할 수 있습니다.

* 모든 채널에서 Dynamics 365 데이터 활성화: Adobe Campaign에 동기화된 연락처 데이터를 사용하면 모바일 푸시, 인앱, 이메일 또는 DM을 포함한 Campaign을 사용하여 모든 온라인 또는 오프라인 채널에서 커뮤니케이션을 전송할 수 있습니다. Campaign은 각 연락처의 기본 설정 채널에 관계없이 &quot;You Cover&quot;를 적용했습니다.

>[!CAUTION]
>
>이 통합에서는 Dynamics 365를 연락처 및 사용자 지정 엔티티 동기화를 위한 진실의 소스로 간주합니다.  동기화된 속성에 대한 모든 변경 사항은 Adobe Campaign Standard이 아니라 Dynamics 365에서 수행해야 합니다.  Campaign에서 변경 작업을 수행하면 결국 동기화 중에 덮어쓸 수 있습니다.

## Microsoft Dynamics 365 통합을 구현하는 주요 단계{#request-and-implement-this-integration}

이 통합을 프로비저닝하려면 아래 단계를 수행해야 합니다.

통합을 요청하고 구성하려면 아래 순서도 및 순서도 세부 정보를 따르십시오.

![](assets/provisioning-wf.png)

순서도 세부 정보(위의 단계에 매핑):

* **1단계** - Microsoft Dynamics 365 for Sales 및 Adobe Campaign Standard에 대한 라이센스가 이미 있거나 구입 중인 것으로 가정합니다.
* **2단계** - 모든 고객에게 표준 통합 제공 그러나 요구 사항에 따라 추가 비용이 발생할 수 있습니다. 추가 정보 [우수 사례 및 제한 사항](../../integrating/using/d365-acs-notices-and-recommendations.md). 원래 SO에 포함되지 않은 경우 통합을 활용하려면 새로운 판매 주문(SO)에 서명해야 합니다.
* **3단계** - Dynamics 365 및 Campaign에 대한 전체 사전 통합 단계. 자세한 내용은 [이 통합 구성](#configure-this-integration).
* **4단계** - Adobe 온보딩 팀이 통합 애플리케이션 사용자 인터페이스(UI)에 대한 액세스 권한을 제공합니다.
* **5단계** - 데이터 매핑, 교체, 필터 등을 구성할 수 있습니다. 통합 애플리케이션 UI 내에서 통합을 테스트합니다.

   >[!IMPORTANT]
   >
   > 양방향 또는 Campaign에서 Dynamics 365 옵트아웃 구성이 필요한 경우 옵트아웃 워크플로우가 Campaign 인스턴스에 설정되도록 Adobe 기술 담당자에게 요청해야 합니다. [자세히 알아보기](../../integrating/using/d365-acs-notices-and-recommendations.md#opt-out)

### 이 통합 구성 {#configure-this-integration}

이 통합을 위해 세 개의 시스템을 프로비저닝하고 구성해야 합니다.

* **Adobe Campaign Standard**: api 액세스를 설정하고 통합 도구에 대한 새 통합을 구성해야 합니다. 이를 수행하려면 다음을 참조하십시오 [이 문서](../../integrating/using/d365-acs-configure-adobe-io.md).
* **Microsoft Dynamics 365**: 새 앱 등록을 만들고 애플리케이션 사용자가 통합을 사용할 수 있도록 해야 합니다.  이 통합을 위해 Microsoft Dynamics 365를 구성하려면 다음을 참조하십시오 [이 문서](../../integrating/using/d365-acs-configure-d365.md).
* **Microsoft Dynamics 365 셀프 서비스 앱과 Adobe Campaign Standard 통합**: 의 단계를 따라야 합니다. [이 문서](../../integrating/using/d365-acs-self-service-app-control-access.md).

>[!IMPORTANT]
>
>각 시스템의 경우 다음 단계를 **관리자**.
>
>이 설명서의 단계에서는 권한 및/또는 관리자 액세스 권한을 지정하는 통합/등록을 만드는 과정을 안내합니다.  이러한 단계가 수행 전에 회사 정책을 준수하고 신중하게 수행하는 것은 귀하의 책임입니다.

### 지원 요청

지원 티켓은 Adobe 고객 지원 센터에 로그인할 수 있습니다.

통합 데이터 흐름과 관련된 문제에 대해서는 다음 정보를 포함해야 합니다.

* **프로세스 소유자**: 엔지니어링 설계자
* **ES 프로세스 ID**: 온보딩 프로세스 중에 제공됩니다
* **프로세스 제목**: Microsoft Dynamics 365 / Adobe Campaign Standard 통합
* **문제 설명**: 문제에 대한 설명

통합 지원 범위는 현재 24x5(Adobe 휴일 및 휴가 기간을 제외하고 월요일부터 금요일까지 제공)입니다.
