---
title: 프로필 편집
description: 기존 프로필을 편집하고 연락처 정보, 기본 채널, 추적 로그, 구독 등에 액세스하는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-profiles
feature: Profiles
role: User
level: Intermediate
exl-id: d0c7dc09-6f2b-4336-b545-7afe3a704164
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---

# 프로필 편집{#editing-profiles}

## 프로필 속성 액세스 {#accessing-profile-properties}

기존 프로필을 편집하고 연결된 데이터를 참조하거나 수정하려면 다음 단계를 수행합니다.

1. Adobe Campaign 홈페이지에서 **[!UICONTROL Customer profiles]** 카드 또는 **[!UICONTROL Profiles]** 탭을 클릭합니다.
1. 연락처를 선택합니다.
1. 프로필의 자세한 정보에 액세스하려면 **[!UICONTROL Edit profile properties]** 아이콘을 클릭하십시오.

   ![](assets/profile_creation2.png)

   프로필의 속성 창에는 모든 프로필 정보에 액세스할 수 있는 몇 가지 탭이 있습니다.

   Adobe Campaign에서 만들거나 확장한 사용자 지정 리소스에 따라 다른 탭이 나타날 수도 있습니다. 사용자 지정 리소스에 대한 자세한 내용은 [사용자 지정 리소스 정보](../../developing/using/data-model-concepts.md)를 참조하세요.

   >[!NOTE]
   >
   >**[!UICONTROL Traceability]** 섹션을 제외한 **[!UICONTROL General]** 탭의 정보만 수정할 수 있습니다.

Adobe Campaign Standard API를 사용하여 프로필 편집도 가능합니다. 자세한 내용은 [전용 설명서](../../api/using/updating-profiles.md)를 참조하십시오.

관련 항목:

* [Integrated Customer Profile](../../audiences/using/integrated-customer-profile.md)
* [수신자의 시간대에 전송](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## 일반 프로필 데이터 {#general-profile-data}

**[!UICONTROL General]** 탭은 프로필에 대한 다음 정보를 그룹화합니다.

* 받는 사람의 이름, 성, 생년월일, 사진, 선호 언어([다국어 이메일](../../channels/using/creating-a-multilingual-email.md)) 등이 포함된 연락처 정보
* 수신자의 이메일 주소, 휴대폰 번호 및 옵트아웃 정보가 포함된 프로필에 연결할 수 있는 채널.
* 우편 주소([DM](../../channels/using/about-direct-mail.md)용) 및 연락처의 시간대([해당 시간대의 예약 메시지](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)).
* 액세스 권한 부여는 받는 사람의 조직 단위([권한 관리](../../administration/using/about-access-management.md))를 나타냅니다. [프로필 파티션 나누기](../../administration/using/organizational-units.md#partitioning-profiles)도 참조하십시오.

![](assets/profile_creation4.png)

## 전송 및 추적 로그 {#sending-and-tracking-logs}

**[!UICONTROL Sending logs]** 및 **[!UICONTROL Tracking logs]** 탭은 프로필로 전송된 게재 목록과 모든 관련 추적 데이터를 그룹화합니다.

전송 및 추적 로그에 대한 자세한 정보는 [게재 로그](../../sending/using/monitoring-a-delivery.md#delivery-logs) 및 [추적 메시지](../../sending/using/tracking-messages.md) 섹션을 참조하세요.

## 구독 {#subscriptions}

연락처의 구독이 해당 탭에 나열됩니다. 서비스 구독에 대한 자세한 정보는 [이 섹션](../../audiences/using/about-subscriptions.md)을 참조하세요.

**[!UICONTROL Mobile App Subscriptions]** 탭은 푸시 알림을 참조합니다. 자세한 내용은 [푸시 알림](../../channels/using/about-push-notifications.md) 채널을 참조하세요.
