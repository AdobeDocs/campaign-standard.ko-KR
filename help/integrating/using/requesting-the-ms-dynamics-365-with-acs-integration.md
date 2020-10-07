---
title: Microsoft Dynamics 365 통합 요청 및 구성
description: Campaign Standard 통합을 통해 Microsoft Dynamics 365를 요청하고 구성하는 방법 살펴보기
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 3%

---


# Microsoft Dynamics 365 통합 요청 및 구성

이 통합을 프로비저닝하려면 아래 단계를 따라야 합니다.

통합을 요청하고 구성하려면 아래 순서도와 순서도를 따르십시오.

![](assets/provisioning-wf.png)

순서도 세부 사항(위 단계에 매핑):

* **1단계** - 세일즈 및 Adobe Campaign Standard용 Microsoft Dynamics 365에 대한 라이선스를 이미 보유하고 있거나 구매 진행 중인 것으로 가정합니다.

* **2단계** - 표준 통합 솔루션은 모든 고객에게 무료로 제공됩니다.그러나 요구 사항에 따라 추가 비용이 발생할 수 있습니다( [통합 보안 및 경계](../../integrating/using/ms-dynamics-365-integration-guardrails.md)참조). 통합을 활용하려면 새로운 판매 주문에 서명해야 합니다.

* **3단계** - Dynamics 365 및 Campaign에 대한 완벽한 사전 통합 단계 이 [통합 구성을 참조하십시오](#configure-this-integration).

* **4-7** 단계 - Adobe 온보딩 팀이 온보딩 과정을 통해 귀하와 함께 작업할 것입니다.

## 이 통합 구성 {#configure-this-integration}

이 통합을 위해 세 개의 시스템을 프로비저닝하고 구성해야 합니다.Adobe Campaign Standard, Microsoft Dynamics 365 for Sales 및 통합 툴 구성 아티클은 아래에 연결되어 있습니다.

>[!CAUTION]
>
>각 시스템의 경우 관리자가 이러한 단계를 수행해야 합니다.
>
>아래 문서의 단계에서는 권한 및/또는 관리자 액세스 권한을 할당하는 것과 관련된 통합/등록을 만드는 과정을 안내합니다.  이러한 단계가 수행 전에 회사 정책을 준수하고 신중하게 수행하는 것은 귀하의 책임입니다.

Adobe Campaign에서 API 액세스를 설정하고 통합 도구에 대한 새 통합을 구성해야 합니다. 이를 실현하려면 [이 문서를 참조하십시오](../../integrating/using/configure-adobe-io-for-ms-dynamic.md).

MICROSOFT DYNAMICS 365에서는 새 앱 등록을 만들고 응용 프로그램 사용자가 통합을 사용하도록 설정해야 합니다.  이 통합을 위해 Microsoft Dynamics 365를 구성하려면 [이 문서를 참조하십시오](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

수신, 수신 및 수신 거부 데이터 흐름에 대한 구성을 설정하려면 Adobe 온보딩 팀과 함께 작업해야 합니다.


## 지원 요청

지원 티켓은 평소대로 Adobe 사용자 지정 서비스로 기록할 수 있습니다.고객 지원 센터는 필요에 따라 지원 인력을 데려올 것입니다.

통합 데이터 흐름과 관련된 문제에 대해서는 보고서 세트를 문제 설명의 일부로 포함시키고 다음 정보를 포함해야 합니다.

* **프로세스 소유자**:엔지니어링 건축가

* **ES 프로세스 ID**:온보딩 프로세스 중 제공

* **프로세스 제목**:Dynamics 365 / Adobe Campaign Standard 통합

* **문제 설명**:문제에 대한 설명

통합 지원 서비스는 현재 24x5(Adobe 휴가 및 휴가 제외)입니다.