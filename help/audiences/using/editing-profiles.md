---
title: 프로필 편집
description: 기존 프로필을 편집하고 연락처 정보, 기본 채널, 추적 로그, 구독 등에 액세스하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 6fcdb719-6149-48fc-b400-64c24a51487f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: 8d3ba7bf-90ae-4c6d-aaeb-a48572a69f2f
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# 프로필 편집{#editing-profiles}

## 프로필 속성 액세스 {#accessing-profile-properties}

기존 프로파일을 편집하고 이와 관련된 데이터를 참조하거나 수정하려면 다음과 같이 하십시오.

1. Adobe Campaign 홈 페이지에서 **[!UICONTROL Customer profiles]** 카드나 **[!UICONTROL Profiles]** 탭을 클릭합니다.
1. 연락처를 선택합니다.
1. 프로필의 세부 정보에 액세스하려면 **[!UICONTROL Edit profile properties]** 아이콘을 클릭합니다.

   ![](assets/profile_creation2.png)

   프로필의 속성 창에는 모든 프로필 정보에 액세스할 수 있는 여러 탭이 있습니다.

   Adobe Campaign에서 만들거나 확장된 사용자 지정 리소스에 따라 다른 탭이 표시될 수도 있습니다. 사용자 지정 리소스에 대한 자세한 내용은 사용자 지정 [리소스](../../developing/using/data-model-concepts.md)정보를 참조하십시오.

   >[!NOTE]
   >
   >탭에서만 정보를 수정할 수 있습니다( **[!UICONTROL General]** **[!UICONTROL Traceability]** 섹션 제외).

Adobe Campaign Standard API를 사용하여 프로필 에디션을 사용할 수도 있습니다. 자세한 내용은 [전용 설명서를](../../api/using/updating-profiles.md) 참조하십시오.

관련 항목:

* [Integrated customer profile](../../audiences/using/integrated-customer-profile.md)
* [받는 사람의 시간대에서 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## 일반 프로필 데이터 {#general-profile-data}

이 **[!UICONTROL General]** 탭에는 프로필에 대한 다음 정보가 그룹화됩니다.

* 받는 사람의 이름, 성, 생년월일, 사진, 기본 언어( [다국어 이메일](../../channels/using/creating-a-multilingual-email.md)) 등이 포함된 연락처 정보.
* 받는 사람의 이메일 주소, 휴대폰 번호, 수신 거부 정보가 포함된 프로필에 연결할 수 있는 채널입니다.
* 우편 주소( [DM용](../../channels/using/about-direct-mail.md)) 및 연락처의 시간대(표준 시간대에서 [메시지를](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)예약하기 위한).
* 권한 [관리를 위해 받는 사람의 조직 구성 단위를 나타내는 액세스 권한](../../administration/using/about-access-management.md). 파티션 [프로필을](../../administration/using/organizational-units.md#partitioning-profiles)참조하십시오.

![](assets/profile_creation4.png)

## Sending and tracking logs {#sending-and-tracking-logs}

및 **[!UICONTROL Sending logs]** **[!UICONTROL Tracking logs]** 탭에서는 프로필로 전송된 배달 목록과 모든 관련 추적 데이터를 그룹화합니다.

로그 전송 및 추적에 대한 자세한 내용은 [배달 로그](../../sending/using/monitoring-a-delivery.md#delivery-logs) 및 [추적 메시지](../../sending/using/tracking-messages.md) 섹션을 참조하십시오.

## 구독 {#subscriptions}

연락처의 구독은 해당 탭에 나열됩니다. 서비스 구독에 대한 자세한 내용은 [이 섹션을](../../audiences/using/about-subscriptions.md)참조하십시오.

이 **[!UICONTROL Mobile App Subscriptions]** 탭은 푸시 알림을 나타냅니다. 자세한 내용은 푸시 알림 [채널을](../../channels/using/about-push-notifications.md) 참조하십시오.
