---
title: 프로필 만들기
description: API, 가져오기 기능, 온라인 확보, 자동 또는 수동 업데이트 등을 사용하여 프로필을 만들고 연락처 데이터를 수집하는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-profiles
feature: Profiles
role: User
level: Beginner
exl-id: 827df9f6-070c-466a-890c-e363de6b129b
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 83%

---

# 프로필 만들기{#creating-profiles}

Adobe Campaign에서 프로필은 메시지의 주요 타겟을 정의할 때 기본적으로 사용됩니다.

>[!NOTE]
>
>Adobe Campaign Standard API를 사용하여 프로필을 만들 수도 있습니다. 자세한 내용은 [전용 설명서](../../api/using/creating-profiles-api.md)를 참조하십시오.

![](assets/do-not-localize/how-to-video.png) [비디오에서 워크플로우를 사용하여 프로필을 가져오는 방법을 알아봅니다](#video)

Campaign에서 프로필을 만들거나 업데이트하기 위해 다음을 수행할 수 있습니다.

* [워크플로우](../../automating/using/creating-import-workflow-templates.md)를 통해 파일에서 프로필 목록 가져오기
* [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md)를 통해 온라인으로 데이터 수집
* [REST API](../../api/using/get-started-apis.md)를 통해 벌크 만들기
* [Microsoft Dynamics](../../integrating/using/d365-acs-get-started.md)에서 프로필 동기화
* 아래 설명된 대로 사용자 인터페이스를 사용하여 데이터를 입력합니다

예를 들어 사용자 인터페이스에서 직접 새 프로필을 만들려면 아래 단계를 수행하십시오.

1. Adobe Campaign 홈페이지에서 **고객 프로필** 카드 또는 **프로필** 탭을 클릭하여 프로필 목록에 액세스합니다.

   ![](assets/profile_creation_1.png)

1. **[!UICONTROL Create]**&#x200B;를 클릭합니다.

   ![](assets/profile_creation.png)

1. 프로필 데이터를 입력합니다.

   ![](assets/profile_creation1.png)

   * 이름, 성, 성별, 생년월일, 사진, 선호 언어([다국어 이메일](../../channels/using/creating-a-multilingual-email.md)의 경우)와 같은 연락처 정보를 통해 게재를 개인화할 수 있습니다.
   * 프로필의 **[!UICONTROL Time zone]**&#x200B;을(를) 사용하여 해당 프로필의 시간대에 맞춰 게재를 보낼 수 있습니다. 자세한 정보는 이 [섹션](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)을 참조하십시오.
   * **[!UICONTROL Channels]** 카테고리에는 이메일 주소, 휴대전화 번호, 옵트아웃 정보가 있으며 프로필이 도달할 수 있는 채널을 알려줍니다.

      >[!NOTE]
      > 휴대폰 번호는 항상 국제 형식이어야 합니다(`+<country><number>`) 프로필 테이블의 형식입니다.

   * **[!UICONTROL No longer contact]** 카테고리는 프로필이 채널 구독을 취소하면 즉시 업데이트됩니다.
   * **[!UICONTROL Address]** 카테고리에는 우편 주소가 있으며, 프로필에 [DM](../../channels/using/about-direct-mail.md)을 보낼 수 있는 **[!UICONTROL Address specified]** 옵션도 선택되어 있어야 합니다. **[!UICONTROL Address specified]** 옵션이 선택되어 있지 않은 프로필은 모든 DM 게재에서 제외됩니다. 
   * 다음 **[!UICONTROL Access authorization]** 카테고리는 프로필의 조직 단위를 다음과 같이 나타냅니다. [권한 관리](../../administration/using/about-access-management.md). 프로필에 조직 필드를 추가하려면 [프로필 파티션 나누기](../../administration/using/organizational-units.md#partitioning-profiles) 섹션을 참조하십시오.
   * **[!UICONTROL Traceability]** 카테고리는 프로필을 만들거나 수정한 사용자에 대한 정보로 자동 업데이트됩니다. 

1. **[!UICONTROL Create]**&#x200B;을(를) 클릭하여 프로필을 저장합니다.

이제 프로필이 목록에 나타납니다.

>[!NOTE]
>선호 언어 필드는 다국어 메시지를 보낼 때 언어를 선택하는 데 사용됩니다. 다국어 메시지에 대한 자세한 내용은 [이 페이지를 참조하십시오](../../channels/using/creating-a-multilingual-email.md).

## 튜토리얼 비디오 {#video}

이 비디오는 워크플로우로 프로필을 가져오는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/24993?quality=12)

추가 Campaign Standard 방법 비디오를 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko).
