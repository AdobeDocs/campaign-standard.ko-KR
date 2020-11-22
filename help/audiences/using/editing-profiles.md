---
solution: Campaign Standard
product: campaign
title: 프로필 편집
description: 기존 프로필을 편집하고 연락처 정보, 기본 채널, 추적 로그, 구독 등에 액세스하는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-profiles
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# 프로필 편집{#editing-profiles}

## 프로필 속성 액세스 {#accessing-profile-properties}

기존 프로파일을 편집하고 관련 데이터를 참조하거나 수정하려면 다음과 같이 하십시오.

1. From the Adobe Campaign home page, click the **[!UICONTROL Customer profiles]** card or the **[!UICONTROL Profiles]** tab.
1. 연락처를 선택합니다.
1. 이 **[!UICONTROL Edit profile properties]** 아이콘을 클릭하여 프로파일의 세부 정보에 액세스합니다.

   ![](assets/profile_creation2.png)

   프로파일의 속성 창에는 모든 프로필 정보에 액세스할 수 있는 여러 탭이 있습니다.

   다른 탭은 Adobe Campaign에서 만들거나 확장된 사용자 지정 리소스에 따라 표시될 수도 있습니다. 사용자 지정 리소스에 대한 자세한 내용은 사용자 지정 리소스 [정보를 참조하십시오](../../developing/using/data-model-concepts.md).

   >[!NOTE]
   >
   >탭 내의 정보만 수정할 수 있습니다. 단, 섹션 **[!UICONTROL General]** 은 **[!UICONTROL Traceability]** 제외됩니다.

프로필 에디션은 Adobe Campaign Standard API를 사용하여 가능합니다. 자세한 내용은 [전용 설명서](../../api/using/updating-profiles.md)를 참조하십시오.

관련 항목:

* [Integrated customer profile](../../audiences/using/integrated-customer-profile.md)
* [받는 사람의 시간대에서 보내기](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## 일반 프로필 데이터 {#general-profile-data}

이 **[!UICONTROL General]** 탭에는 프로필에 대한 다음 정보가 그룹화됩니다.

* 받는 사람의 이름, 성, 생년월일, 사진, 기본 언어( [다국어 이메일](../../channels/using/creating-a-multilingual-email.md)) 등이 포함된 연락처 정보
* 받는 사람의 이메일 주소, 휴대폰 번호, 수신 거부 정보가 포함된 프로필에 연결할 수 있는 채널입니다.
* 우편 주소( [DM용](../../channels/using/about-direct-mail.md)) 및 연락처의 시간대(해당 시간대에서 [메시지를 예약하려면](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)).
* 액세스 권한 부여를 참조하십시오. [](../../administration/using/about-access-management.md) [프로필 파티션 나누기](../../administration/using/organizational-units.md#partitioning-profiles)도 참조하십시오.

![](assets/profile_creation4.png)

## Sending and tracking logs {#sending-and-tracking-logs}

및 탭 **[!UICONTROL Sending logs]** **[!UICONTROL Tracking logs]** 은 프로필로 전송된 배달 목록과 모든 관련 추적 데이터를 그룹화합니다.

로그 전송 및 추적에 대한 자세한 내용은 [배달 로그](../../sending/using/monitoring-a-delivery.md#delivery-logs) 및 [추적 메시지](../../sending/using/tracking-messages.md) 섹션을 참조하십시오.

## 구독 {#subscriptions}

연락처의 가입은 해당 탭에 나열됩니다. 서비스 구독에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../audiences/using/about-subscriptions.md).

탭 **[!UICONTROL Mobile App Subscriptions]** 은 푸시 알림을 나타냅니다. 자세한 내용은 [푸시 알림](../../channels/using/about-push-notifications.md) 채널을 참조하십시오.
