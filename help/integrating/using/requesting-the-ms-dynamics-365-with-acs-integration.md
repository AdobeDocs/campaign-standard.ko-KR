---
title: Campaign Standard 통합을 통해 Microsoft Dynamics 365 요청 및 구성
description: Campaign Standard 통합을 사용하여 Microsoft Dynamics 365를 요청하고 구성하는 방법 살펴보기
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
source-git-commit: 4dd1ada05b6681a4e2f7676b177747bdfb0e9bff

---


# Campaign Standard 통합을 통해 Microsoft Dynamics 365 요청

이 통합을 제공하려면 아래 단계를 따라야 합니다.

이 통합은 타사 공급자인 Unifi를 사용합니다.  지원 요청 관련 Adobe는 Adobe Campaign 인스턴스 정보를 Unifi와 공유해야 할 수 있습니다.

아래 순서도와 순서도를 따라 통합을 요청하고 구성하십시오.

![](assets/provisioning-wf.png)

순서도 세부 사항(위의 단계에 매핑):

1. 이 통합 구현을 시작하려면 관리자 액세스 권한이 있는 Campaign Standard 및 Microsoft Dynamics 365가 이미 프로비저닝되어 있어야 합니다.

1. 이 문서를 읽고 알림 및 구성 단계를 확인하십시오.

1. 계정 요청을 adobe-support@unifisoftware.com으로 보내기;Unifi는 계정을 요청할 때 다음 정보가 필요합니다.
   * 사용자 이름
   * 사용자 성
   * 사용자 이메일
   * 회사 이름
   * 지역(북미, EMEA 또는 APAC)
   * 사용 유형: 고객 유형(이 통합에서 프로덕션 데이터를 사용하게 될 고객 사용자) 또는 파트너 유형(Campaign 고객에게 도움이 되도록 통합을 테스트하여 더 잘 이해하도록 하는 파트너 컨설턴트) 또는 내부 유형(솔루션에 대한 더 나은 이해를 위해 통합을 테스트하고 있는 Adobe 내부 사용자)
   * Campaign Standard 데이터 상태(깔끔한 데이터베이스 또는 기존 데이터를 통합으로 가져오기)
   * 캠페인 테넌트 ID(테넌트 ID를 얻으려면 캠페인 통합 구성 섹션 3단계 참조)
   * 캠페인 인스턴스 URL
   Unifi 예상 응답 시간:정규 미국 근무 시간 중 1시간(오전 9시에서 오후 5시, 월 - 금, 공휴일 제외)

1. Microsoft Dynamics 365 및 Campaign Standard에 대한 사후 프로비저닝 단계를 완료합니다.
또한 Adobe 고객 지원 센터(직접 또는 Adobe 담당자를 통해)에 티켓을 제출하여 Campaign 인스턴스에서 Single-Sign-On 기능 플래그를 사용하도록 설정하십시오. 파트너는 Adobe 고객 지원 센터에 연락하여 기능 플래그를 활성화하도록 Adobe 파트너 샌드박스 담당자에게 연락해야 합니다.
Campaign에 통합하려는 기존 데이터가 있는 경우 &quot;기존 캠페인 데이터&quot;의 지침을 따르고 계속하기 전에 Adobe 기술 담당자에게 문의하십시오.

1. Unifi로 이동, 온보딩 화면 클릭, Dynamics 365 및 Campaign Standard 계정 자격 증명 채우기, 완료 시 Unifi에 통보 등을 통해 Unifi의 초기 온보딩 단계를 완료합니다.

1. Unifi는 고객에게 원하는 옵트아웃 구성 및 옵트아웃 속성 매핑을 요청합니다.

1. 고객은 선택한 옵트아웃 구성 및 옵트아웃 속성 매핑을 나타냅니다.
Unifi 예상 응답 시간:영업일 기준 1일(월 - 금, 휴일 제외)

1. Unifi 구성에는 OOTB 매핑, 필터, 작업 등의 검토가 포함됩니다. 필요한 경우 수정합니다.  자세한 내용은 Unifi 사용 안내서를 참조하십시오.
이 단계에서는 Unifi 일정의 실행 빈도를 설정합니다
* Unifi의 예약 화면에서 예약 실행 빈도를 설정합니다.하지만 &quot;수신&quot; 및 &quot;수신&quot; 예약의 경우 예약 빈도 수를 설정하기 전에 수동으로 한 번 실행하십시오
* 다음과 같은 예약 빈도를 권장합니다.수신(15분), 수신(15분), 삭제(하루에 한 번), 옵트아웃(하루에 한 번)

**Unifi 구성 시 Unifi 및/또는 Adobe 컨설팅(Adobe 계정 팀에 문의)을 사용하는 것이 좋습니다.**

Adobe Campaign Standard와 Microsoft Dynamics 365 간의 통합을 활성화하려면 이 문서에 설명된 대로 고객은 타사 제공업체인 Unifi를 사용하여 사용자 계정을 만들어야 합니다.   Unifi 시스템의 최종 사용자는 Unifi 시스템 내에서 고객이 시작한 데이터 요청과 관련된 모든 문의에 대해 Unifi에 문의해야 합니다.

## 이 통합 구성

이 통합을 위해 세 개의 시스템을 프로비저닝하고 구성해야 합니다.Adobe Campaign Standard, Microsoft Dynamics 365 for Sales and Unifi. 구성 아티클은 아래에 연결되어 있습니다.

>[!CAUTION]
>
>각 시스템의 경우 관리자가 이러한 단계를 수행해야 합니다.
>
>아래 문서의 단계에서는 권한 및/또는 관리자 액세스 권한을 할당하는 것과 관련된 통합/등록을 만드는 과정을 안내합니다.  이러한 단계는 수행 전에 회사 정책을 준수하고 신중하게 수행하는 것이 귀하의 책임입니다.

ADOBE CAMPAIGN 파섹 이를 위해서는 [이 문서를](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)참조하십시오.

MICROSOFT DYNAMICS 365에서는 새 앱 등록을 만들고 애플리케이션 사용자가 통합을 사용할 수 있도록 설정해야 합니다.  이 통합을 위해 Microsoft Dynamics 365를 구성하려면 [이 문서를](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)참조하십시오.

UNIFI에서는 통합을 설정하고 매핑을 구성하거나 사용자 지정 속성을 추가해야 합니다. 이 통합에 대해 Unifi를 구성하려면 [이 문서를](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md)참조하십시오.

## 지원 요청

문제가 발생하는 경우 Unifi 고객 지원에 문의하십시오.support@unifisoftware.atlassian.net [](mailto:support@unifisoftware.atlassian.net).

Unifi 예상 응답 시간:정규 미국 근무 시간 중 4시간(오전 9시에서 오후 5시, 월 - 금, 공휴일 제외)

>[!CAUTION]
>
>지원 요청 관련 Adobe는 Adobe Campaign 인스턴스 정보를 Unifi와 공유해야 할 수 있습니다.