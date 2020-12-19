---
solution: Campaign Standard
product: campaign
title: Microsoft Dynamics 365 통합 시작
description: Microsoft Dynamics 365 통합을 시작하는 방법 살펴보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 10%

---


# Microsoft Dynamics 365 통합 시작

크로스 채널 통신 시 CRM 데이터 활성화:Microsoft Dynamics 365에서 Adobe Campaign으로 연락처를 전달하고 캠페인 성능 데이터(전송, 열기, 클릭 수 및 바운스)를 Adobe Campaign에서 Microsoft Dynamics 365로 다시 공유하는 방법을 알아봅니다.

지원되는 버전이 이 섹션](#support-software-versions)에 [나열됩니다.

>[!CAUTION]
>
>이 기능은 제품의 일부로 기본 제공되지 않습니다. 구현하려면 Adobe Consulting 서비스가 필요합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

## 원칙

Adobe Campaign 및 Microsoft Dynamics 365 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화하여 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다.

반대로 Adobe Campaign 내의 프로필은 메시지와 상호 작용하므로 이러한 데이터(예:보내기, 열기, 클릭 수 및 바운스)가 Microsoft Dynamics 365로 자동 유입되므로 연락처 기록에서 마케팅 활동을 모두 수행할 수 있습니다.

통합은 사용자 지정 엔티티도 지원하므로 Dynamics 365의 [사용자 지정 엔티티](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md)를 Campaign의 해당 사용자 지정 엔티티에 동기화할 수 있습니다.

이 통합은 4가지 주요 사용 사례를 지원하도록 설계되었습니다.

1. Dynamics 365에서 Campaign으로 연락처를 동기화하여 마케팅 캠페인에서 타깃팅할 수 있습니다.
1. 세분화 및 개인화에 사용할 수 있도록 Dynamics 365에서 Campaign으로 맞춤형 개체 동기화
1. Dynamics 365 인터페이스의 판매 저장소에 표시하기 위해 Campaign에서 Dynamics 365로 이메일 마케팅 이벤트(전송, 열기, 클릭, 바운스)를 전송합니다.
1. Dynamics 365와 ACS 간의 옵트아웃(이메일 금지) 상태를 동기화하여 고객 개인 정보 보호 설정을 유지합니다.

## 주요 이점

* 세일즈 및 마케팅 간의 일관된 메시지

Adobe Campaign과 Microsoft Dynamics 365의 통합을 통해 고객 인사이트와 이메일 마케팅 내역 정보를 모두 이용할 수 있으므로 고객에게 메시지를 일관되게 전달할 수 있습니다.

* 모든 잠재 고객 및 고객 데이터의 거시적인 관점

Dynamics 365와 Adobe Campaign을 통합하면 CRM 시스템 내에서 각 연락처에서 이메일 마케팅 내역을 공유하고 액세스할 수 있습니다.

* 모든 채널에서 Dynamics 365 데이터 활성화

연락처 데이터를 Adobe Campaign에 동기화하면 모바일 푸시, 인앱, 이메일 또는 다이렉트 메일을 포함하여 모든 온라인 또는 오프라인 채널에서 커뮤니케이션을 보낼 수 있습니다. 각 연락처의 기본 채널에 상관없이 Campaign은 해당 정보를 제공합니다.

>[!CAUTION]
>
>연락처 및 맞춤형 엔티티 동기화를 위해 이 통합은 Dynamics 365를 진실의 소스로 간주합니다.  동기화된 속성에 대한 모든 변경 사항은 캠페인이 아니라 Dynamics 365에서 수행해야 합니다.  Campaign에서 변경한 경우 동기화 도중 최종적으로 덮어쓸 수 있습니다.

## 지원 소프트웨어 버전 {#support-software-versions}

이 통합을 사용하려면 다음 소프트웨어 버전이 필요합니다.

* Microsoft Dynamics 365 for Sales Online 전용, 최신 버전

* Adobe Campaign Standard, 최신 버전
