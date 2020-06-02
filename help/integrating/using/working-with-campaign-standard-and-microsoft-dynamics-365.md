---
title: Microsoft Dynamics 365 통합 시작하기
description: Microsoft Dynamics 365 통합 시작 방법 살펴보기
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 21135f27fd1d8297edd3dd067446d09c39de9f4f
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---


# Microsoft Dynamics 365 통합 시작하기

>[!IMPORTANT]
>
>현재 이 통합을 사용할 수 없습니다. 새 커넥터가 개발되고 있으며 향후 출시될 예정입니다. 자세한 내용은 Adobe 세일즈 담당자에게 문의하십시오.

크로스채널 통신 시 CRM 데이터 활성화: Microsoft Dynamics 365에서 Adobe Campaign으로 연락처를 전달하고 캠페인 성과 데이터(전송, 열기, 클릭 및 바운스)를 Adobe Campaign에서 Microsoft Dynamics 365로 다시 공유하는 방법을 알아봅니다.

>[!NOTE]
>
>Microsoft Dynamics 365/Adobe Campaign Standard 통합에서는 **Microsoft Dynamics 365 Sales 앱만** 지원합니다.

## 원칙

Adobe Campaign 및 Microsoft Dynamics 365 통합을 통해 CRM 시스템에서 사용 가능한 모든 연락처 데이터를 동기화할 수 있으므로 모든 관련 연락처 데이터를 캠페인 활동에 사용할 수 있습니다.

반대로 Adobe Campaign 내의 프로필과 메시지가 상호 작용하므로 이러한 데이터(예: 전송, 열기, 클릭 및 바운스)가 Microsoft Dynamics 365로 자동 전달되므로 연락처 기록에서 마케팅 활동을 모두 수행할 수 있습니다.

통합의 최신 릴리스는 사용자 지정 개체에 대한 지원을 추가하여 Dynamics 365의 사용자 지정 엔터티를 Campaign의 해당 사용자 지정 엔터티에 동기화할 수 있습니다.

이 통합은 다음 세 가지 주요 사용 사례를 지원하도록 설계되었습니다.

1. Dynamics 365에서 Campaign으로 연락처를 동기화하여 마케팅 캠페인에서 타깃팅할 수 있습니다.
1. Dynamics 365 인터페이스의 판매 저장소에 표시하기 위해 Campaign에서 Dynamics 365로 이메일 마케팅 이벤트(전송, 열기, 클릭, 바운스)를 보냅니다.
1. 세분화 및 개인화에 사용할 수 있도록 Dynamics 365에서 Campaign으로 맞춤형 개체 동기화

## 주요 이점

* 세일즈 및 마케팅 간의 일관된 메시지

Adobe Campaign과 Microsoft Dynamics 365 간의 통합을 통해 고객 인사이트와 이메일 마케팅 내역을 모두 이용할 수 있으므로 고객에게 모든 메시지를 일관된 메시지를 공유할 수 있습니다.

* 모든 잠재 고객 및 고객 데이터의 거시적 관점

Adobe Campaign과 Dynamics 365를 통합하면 CRM 시스템 내에서 각 연락처의 이메일 마케팅 내역을 공유하고 액세스할 수 있습니다.

* 모든 채널에서 Dynamics 365 데이터 활성화

연락처 데이터는 Adobe Campaign에 동기화되므로 모바일 푸시, 인앱, 이메일 또는 DM 등 모든 온라인 또는 오프라인 채널에서 커뮤니케이션을 보낼 수 있습니다. 각 연락처의 기본 채널에 관계없이 Campaign은 고객을 대상으로 합니다.

>[!CAUTION]
>
>연락처 동기화의 경우 이 통합은 Dynamics 365를 진실의 소스로 간주합니다.  동기화된 연락처 속성에 대한 모든 변경 사항은 Campaign이 아니라 Dynamics 365에서 수행해야 합니다.  Campaign에서 변경한 경우 동기화 도중 최종적으로 덮어쓸 수 있습니다.
