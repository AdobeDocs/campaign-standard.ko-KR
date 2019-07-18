---
title: 프로필 편집
seo-title: 프로필 편집
description: 프로필 편집
seo-description: 기존 프로필을 편집하고 연락처 정보, 선호 채널, 추적 로그, 구독 등을 액세스하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 6 FCDB 719-6149-48 FC-B 400-64 C 24 A 51487 F
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: managing-profiles
discoiquuid: 8 d 3 ba 7 bf -90 ae -4 c 6 d-aaeb-a 48572 a 69 f 2 f
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6df0e764750a31f29d6fe3ec4d92e19b3f07f728

---


# Editing profiles{#editing-profiles}

## Accessing profile properties {#accessing-profile-properties}

기존 프로필을 편집하고 그와 연관된 데이터를 참조하거나 수정할 수 있도록 단계는 다음과 같습니다.

1. From the Adobe Campaign home page, click the **[!UICONTROL Customer profiles]** card or the **[!UICONTROL Profiles]** tab.
1. 연락처를 선택합니다.
1. **[!UICONTROL Edit profile properties]** 아이콘을 클릭하여 프로필의 세부 정보에 액세스합니다.

   ![](assets/profile_creation2.png)

   프로필의 속성 창은 모든 프로필 정보에 액세스할 수 있는 여러 탭을 제공합니다.

   다른 탭은 Adobe Campaign에서 만들었거나 확장된 사용자 지정 리소스에 따라 나타날 수도 있습니다. For more information about custom resources, see [About custom resources](../../developing/using/data-model-concepts.md).

   >[!NOTE]
   >
   >You can only modify the information in the **[!UICONTROL General]** tab - except for the **[!UICONTROL Traceability]** section.

Adobe Campaign Standard API를 사용하여 프로필 에디션을 만들 수도 있습니다. For more on this, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#updating-profiles) .

관련 항목:

* [통합된 고객 프로파일](../../audiences/using/integrated-customer-profile.md)
* [수신자의 시간대에서 전송](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## General profile data {#general-profile-data}

**[!UICONTROL General]** 탭에는 프로필에 대한 다음 정보가 그룹화됩니다.

* Contact information, which contains the recipient's first name, last name, date of birth, photo, preferred language (for [multilingual emails](../../channels/using/creating-a-multilingual-email.md)), etc.
* 수신자의 이메일 주소, 휴대폰 번호, 옵트아웃 정보가 포함된 프로필을 연결할 수 있는 채널입니다.
* Postal address (for [direct mail](../../channels/using/about-direct-mail.md)), and the contact's time zone (to [schedule messages in its time zone](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)).
* Access authorization, which indicates the recipient's organisational unit (to [manage permissions](../../administration/using/about-access-management.md)). [프로필 분할을 참조하십시오](../../administration/using/organizational-units.md#partitioning-profiles).

![](assets/profile_creation4.png)

## Sending and tracking logs {#sending-and-tracking-logs}

**[!UICONTROL Sending logs]** AND **[!UICONTROL Tracking logs]** 탭은 프로필로 전송된 배달 목록과 관련된 모든 추적 데이터를 그룹화합니다.

For more on sending and tracking logs, refer to the [delivery logs](../../sending/using/monitoring-a-delivery.md#delivery-logs) and the [tracking messages](../../sending/using/tracking-messages.md) sections.

## Subscriptions {#subscriptions}

해당 탭에 연락처의 구독이 나열됩니다. For more on subscribing to a service, refer to [this section](../../audiences/using/about-subscriptions.md).

**[!UICONTROL Mobile App Subscriptions]** 탭은 푸시 알림을 참조합니다. For more information, refer to the [Push notification](../../channels/using/about-push-notifications.md) channel.
