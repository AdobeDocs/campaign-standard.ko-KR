---
title: DM 만들기
description: 다음 단계에 따라 Adobe Campaign에서 직접 메일 배달을 만듭니다.
page-status-flag: never-activated
uuid: 3b1365c4-4ea1-4434-818b-05ff0c9b42c1
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: 5b02227f-9438-4001-bc2f-3d8661d173b3
context-tags: delivery,directMailContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 155ed7e50e207e4c4dc0569e5e96b24e712e4be8

---


# DM 만들기{#creating-the-direct-mail}

다이렉트 메일 배달을 만드는 것은 일반 이메일을 만드는 것과 매우 유사합니다. 다음 단계에서는 이 채널과 관련된 구성을 설명합니다. 다른 [옵션에 대한 자세한 내용은 이메일](../../channels/using/creating-an-email.md) 만들기를 참조하십시오.

1. 새 DM 배달 만들기 Adobe Campaign [홈 페이지](../../start/using/interface-description.md#home-page), [캠페인](../../start/using/marketing-activities.md#creating-a-marketing-activity) 또는 [마케팅 활동 목록에서](../../start/using/programs-and-campaigns.md#creating-a-campaign)만들 수 있습니다.

   >[!NOTE]
   >
   >워크플로우에서 DM 활동을 추가할 수도 있습니다. 자세한 내용은 워크플로우 [안내서를 참조하십시오](../../automating/using/direct-mail-delivery.md) .

   ![](assets/direct_mail_1.png)

1. 기본 **[!UICONTROL Direct mail]** 템플릿 또는 고유한 템플릿 중 하나를 선택합니다. 템플릿에 대한 자세한 내용은 템플릿 [관리](../../start/using/marketing-activity-templates.md) 섹션을 참조하십시오.

   ![](assets/direct_mail_2.png)

1. 게재의 일반 속성을 입력합니다.

   ![](assets/direct_mail_3.png)

1. 추출 파일뿐만 아니라 테스트 및 트랩 프로필에도 포함할 대상을 정의합니다. See [Defining the direct mail audience](../../channels/using/defining-the-direct-mail-audience.md).

   ![](assets/direct_mail_4.png)

   >[!NOTE]
   >
   >대상 정의는 일반 이메일 대상을 정의하는 것과 매우 유사합니다. 대상자 [만들기를](../../audiences/using/creating-audiences.md)참조하십시오.

1. 파일의 컨텐츠를 편집합니다.각 프로필, 파일 구조, 머리글 및 바닥글에 포함할 열 See [Defining the direct mail content](../../channels/using/defining-the-direct-mail-content.md).

   ![](assets/direct_mail_5.png)

1. 배달 대시보드의 **[!UICONTROL Schedule]** 섹션을 클릭하여 연락처 날짜를 정의합니다. DM의 경우 연락처 날짜는 필수입니다. 자세한 내용은 전송 [예약을](../../sending/using/about-scheduling-messages.md)참조하십시오.

   ![](assets/direct_mail_8.png)

1. 테스트 프로필을 추가한 경우(테스트 및 [트랩 프로필](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)추가 참조) 최종 파일을 준비하기 전에 배달을 테스트할 수 있습니다. 선택한 테스트 프로필만 포함하는 샘플 파일을 만들 수 있습니다.

   아이콘을 **[!UICONTROL Test]** 클릭하여 샘플 파일을 생성합니다. 왼쪽 **[!UICONTROL Summary]**&#x200B;위 모서리에서 을 클릭하고 **[!UICONTROL Proofs]**&#x200B;선택합니다. 화면 왼쪽에서 교정본을 선택하고 을 클릭합니다 **[!UICONTROL Download file]**.

   >[!NOTE]
   >
   >Adobe Campaign이 파일을 내보내고 다운로드할 수 있도록 하려면 **[!UICONTROL Export]** 역할이 필요합니다. 관리자에게 문의하십시오.

   ![](assets/direct_mail_19.png)

1. 배달 컨텐츠, 대상 및 연락처 날짜를 정의했으면 배달 대시보드에서 **[!UICONTROL Prepare]** 단추를 클릭합니다.

   ![](assets/direct_mail_16.png)

   유형 규칙이 적용됩니다. 예를 들어 지정되지 않은 모든 우편 주소는 대상에서 제외됩니다. 이 때문에 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택해야 합니다(권장 사항 참조 [)](../../channels/using/about-direct-mail.md#recommendations). DM 속성 또는 템플릿 수준에서 **[!UICONTROL Maximum volume of message]** 을 정의한 경우 여기에 적용됩니다.

   ![](assets/direct_mail_25.png)

   >[!NOTE]
   >
   >캠페인에서 과다 복제된 프로파일을 자동으로 제외시키는 글로벌 크로스 채널 피로 규칙을 설정할 수 있습니다. 피로 [규칙을](../../sending/using/fatigue-rules.md)참조하십시오.

1. 파일의 처음 100개 줄을 미리 **[!UICONTROL Explore file]** 보려면 클릭하십시오.

   ![](assets/direct_mail_18.png)

   전체 파일은 화면의 왼쪽에서 로컬 다운로드용으로 액세스할 수 있습니다. 파일을 다운로드하면 **[!UICONTROL Export audits]** 메뉴에서 로그 항목이 생성됩니다. 내보내기 감사에 대한 자세한 내용은 감사 내보내기 [섹션을](../../administration/using/auditing-export-logs.md) 참조하십시오.

   >[!NOTE]
   >
   >Adobe Campaign이 파일을 내보내고 다운로드할 수 있도록 하려면 **[!UICONTROL Export]** 역할이 필요합니다. 관리자에게 문의하십시오.

   배달 컨텐츠를 변경해야 하는 경우 **[!UICONTROL Regenerate file]** 단추를 클릭하기만 하면 변경 사항을 고려합니다. 다시 준비 작업을 수행할 필요가 없습니다.

   ![](assets/direct_mail_21.png)

1. 파일이 최종 파일인지 확인하려면 배달 **[!UICONTROL Confirm]** 대시보드에서 를 클릭합니다.

   ![](assets/direct_mail_20.png)

이제 추출 파일을 DM 공급자에게 보낼 준비가 되었습니다. 이에 대해 다음과 같은 여러 옵션이 있습니다.

* 파일을 첨부하여 일반 이메일로 보내기
* Campaign을 통해 전송:캠페인 [워크플로우](../../automating/using/direct-mail-delivery.md) 내에서 다이렉트 메일을 수행하고 FTP를 통해 파일을 보낼 **[!UICONTROL Transfer file]** 수 있는 링크를 추가합니다. 파일 [전송을](../../automating/using/transfer-file.md)참조하십시오.

공급자가 잘못된 주소 목록을 검색하여 Adobe Campaign에 이 정보를 전송하면 잘못된 주소가 자동으로 블랙리스트에 표시됩니다. See [Return to sender](../../channels/using/return-to-sender.md).
