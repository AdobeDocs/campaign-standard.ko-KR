---
title: 프로필 만들기
seo-title: 프로필 만들기
description: 프로필 만들기
seo-description: API, 가져오기 기능, 온라인 획득, 자동 또는 수동 업데이트를 사용하여 연락처에 프로파일을 생성하고 데이터를 수집하는 방법을 살펴봅니다.
page-status-flag: 정품 인증 안 함
uuid: A 5 F 5 A 58 A-E 798-400 F -8648-05 DC 843 D 5557
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 대상
content-type: 참조
topic-tags: managing-profiles
discoiquuid: 4 ab 8 a 984-f 898-4 fff-ad 8 c-ed 8 f 95362 f 96
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: f883986392f6b739832093e0473591aa39dfcbfe

---


# Creating profiles{#creating-profiles}

Adobe Campaign에서 프로필은 기본적으로 메시지의 기본 대상을 정의하기 위해 사용됩니다.

캠페인에서 프로필을 만들거나 업데이트하려면 다음을 수행할 수 있습니다.

* Import a profile list from a file, via a [workflow](https://helpx.adobe.com/campaign/kt/acs/using/acs-importing-profiles-feature-video-using.html)
* Collect data online, via [landing pages](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html)
* Create bulk via [REST API](http://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)
* [Microsoft Dynamics에서 프로필 동기화](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html)
* 아래 설명된 대로 그래픽 인터페이스 화면을 사용하여 데이터를 입력합니다.

예를 들어 사용자 인터페이스에서 직접 새 프로필을 만들려면 아래 단계를 수행하십시오.

1. From the Adobe Campaign home page, click the **Customer Profiles** card or the **Profiles** tab to access the list of profiles.

   ![](assets/profile_creation_1.png)

1. **[!UICONTROL Create]**&#x200B;그런 다음을 클릭합니다.

   ![](assets/profile_creation.png)

1. 프로필 데이터를 입력합니다.

   ![](assets/profile_creation1.png)

   * The contact information, such as first name, last name, gender, date of birth, photo, preferred language (for [multilingual emails](../../channels/using/creating-a-multilingual-email.md)) helps better personalize deliveries.
   * The profile's **[!UICONTROL Time zone]** is used to send deliveries at the profile's time zone. For more on this, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).
   * The **[!UICONTROL Channels]** category, which contains the email address, mobile phone number, opt-out information, lets you know on which channel the profile is reachable.
   * The **[!UICONTROL No longer contact]** category is updated as soon as the profile unsubscribe to a channel.
   * **[!UICONTROL Address]** 이 프로필에는 **[!UICONTROL Address specified]** 이 프로필에 [직접 메일을](../../channels/using/about-direct-mail.md) 보내는 옵션과 함께 작성해야 하는 우편 주소가 포함되어 있습니다. **[!UICONTROL Address specified]** 이 옵션을 선택하지 않으면 모든 직접 메일 배달에서 이 프로필이 제외됩니다.
   * **[!UICONTROL Access authorization]** 카테고리는 프로필의 조직 단위 (관리 권한) [를 나타냅니다](../../administration/using/about-access-management.md). [프로필 분할을 참조하십시오](../../administration/using/organizational-units.md#partitioning-profiles).
   * **[!UICONTROL Traceability]** 카테고리는 프로필을 만들거나 변경한 사용자와 관련된 정보로 자동으로 업데이트됩니다.

1. Click **[!UICONTROL Create]** to save the profile.

이제 프로필이 목록에 표시됩니다.

>[!NOTE]
>
>Adobe Campaign Standard API를 사용하여 프로필을 만들 수도 있습니다. For more on this, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#creating-profiles) .

프로필은 조직 단위로 나눌 수도 있습니다. To add the organizational fields to your profiles, refer to the [Partitioning profiles](../../administration/using/organizational-units.md#partitioning-profiles) section.

>[!NOTE]
>
>다국어 메시지를 보낼 때 언어를 선택하는 데 기본 언어 필드를 사용합니다. For more information about the multilingual messages [refer to this page](../../channels/using/creating-a-multilingual-email.md).

**관련 항목:**

* [랜딩 페이지](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_CreateLandingPage.html) 단계별 안내서 만들기
* [프로필 가져오기](https://helpx.adobe.com/campaign/kt/acs/using/acs-importing-profiles-feature-video-using.html)

