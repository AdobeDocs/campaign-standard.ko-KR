---
title: 프로필 만들기
description: API, 가져오기 기능, 온라인 획득, 자동 또는 수동 업데이트 등을 사용하여 프로파일을 만들고 연락처에 데이터를 수집하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: a5f5a58a-e798-400f-8648-05dc843d5557
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: 4ab8a984-f898-4fff-ad8c-ed8f95362f96
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 816d550d8bd0de085a47f97c1f6cc2fbb5e7acb9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---


# 프로필 만들기{#creating-profiles}

Adobe Campaign에서 프로필은 기본적으로 메시지의 기본 대상을 정의하는 데 사용됩니다.

Campaign에서 프로필을 만들거나 업데이트하려면 다음을 수행할 수 있습니다.

* 워크플로우를 통해 파일에서 프로필 목록 [가져오기](../../automating/using/importing-data.md#example--import-workflow-template)
* 랜딩 페이지를 통해 온라인 데이터 [수집](../../channels/using/getting-started-with-landing-pages.md)
* REST [API를 통해 벌크 만들기](../../api/using/get-started-apis.md)
* Microsoft [Dynamics에서 프로필 동기화](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* 아래에 설명된 대로 그래픽 인터페이스 화면을 사용하여 데이터를 입력합니다

예를 들어 사용자 인터페이스에서 직접 새 프로파일을 만들려면 아래 단계를 수행하십시오.

1. Adobe Campaign 홈 페이지에서 **고객 프로필** 카드 또는 **프로필** 탭을 클릭하여 프로필 목록에 액세스합니다.

   ![](assets/profile_creation_1.png)

1. 그런 다음 을 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/profile_creation.png)

1. 프로필 데이터를 입력합니다.

   ![](assets/profile_creation1.png)

   * 이름, 성, 성별, 생년월일, 사진, 기본 언어( [다국어 이메일의 경우](../../channels/using/creating-a-multilingual-email.md))와 같은 연락처 정보는 배달 내용을 보다 효과적으로 개인화합니다.
   * 프로필 **[!UICONTROL Time zone]** 은 프로필의 표준 시간대에서 배달물을 보내는 데 사용됩니다. For more on this, refer to this [section](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).
   * 이메일 주소, 휴대폰 번호, 옵트아웃 정보가 포함된 카테고리를 사용하여 프로필에 연결할 수 있는 채널을 알 수 있습니다. **[!UICONTROL Channels]**
   * 프로필 구독 **[!UICONTROL No longer contact]** 취소와 동시에 카테고리가 업데이트됩니다.
   * 카테고리에는 이 프로필에 **[!UICONTROL Address]** 직접 메일을 **[!UICONTROL Address specified]** [](../../channels/using/about-direct-mail.md) 보내는 옵션과 함께 채워야 하는 우편 주소가 포함되어 있습니다. 이 옵션이 선택되어 있지 않으면 이 프로필은 모든 DM 전달에서 제외됩니다. **[!UICONTROL Address specified]**
   * 카테고리는 프로필의 조직 구성 단위(권한 **[!UICONTROL Access authorization]** 관리 [](../../administration/using/about-access-management.md))를 나타냅니다. 파티션 [프로필을 참조하십시오](../../administration/using/organizational-units.md#partitioning-profiles).
   * 카테고리는 프로필을 만들거나 수정한 사용자에 대한 정보로 자동 업데이트됩니다. **[!UICONTROL Traceability]**

1. 아이콘을 **[!UICONTROL Create]** 클릭하여 프로필을 저장합니다.

이제 프로필이 목록에 나타납니다.

>[!NOTE]
>
>Adobe Campaign Standard API를 사용하여 프로필을 만들 수도 있습니다. 자세한 내용은 [전용 설명서를 참조하십시오](../../api/using/creating-profiles.md).

또한 프로필은 조직의 단위에 따라 분할할 수도 있습니다. 프로필에 조직 필드를 추가하려면 [파티션 프로필](../../administration/using/organizational-units.md#partitioning-profiles) 섹션을 참조하십시오.

>[!NOTE]
>
>다국어 메시지를 보낼 때 언어를 선택하는 데 기본 언어 필드가 사용됩니다. 다국어 메시지에 대한 자세한 내용은 이 페이지 [를 참조하십시오](../../channels/using/creating-a-multilingual-email.md).

**관련 항목:**

* [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md) 단계별 안내서 정보
* [프로필](https://video.tv.adobe.com/v/24993?captions=kor) 비디오 가져오기
