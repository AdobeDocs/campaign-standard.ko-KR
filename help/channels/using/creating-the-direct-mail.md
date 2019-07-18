---
title: 다이렉트 메일 만들기
seo-title: 다이렉트 메일 만들기
description: 다이렉트 메일 만들기
seo-description: 다음 단계에 따라 Adobe Campaign에서 직접 메일 배달을 만듭니다.
page-status-flag: 정품 인증 안 함
uuid: 3 B 1365 C 4-4 EA 1-4434-818 B -05 FF 0 C 9 B 42 C 1
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: DM
discoiquuid: 5 B 02227 F -9438-4001-BC 2 F -3 D 8661 D 173 B 3
context-tags: 전달, Directmailcontent, 뒤로
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Creating the direct mail{#creating-the-direct-mail}

직접 메일 배달을 만드는 일은 일반 이메일을 만드는 방법과 매우 유사합니다. 다음 단계는 이 채널에 적용되는 구성을 설명합니다. Refer to [Creating an email](../../channels/using/creating-an-email.md) for more information on other options.

1. 새 직접 메일 배달을 만듭니다. You can create one from the Adobe Campaign [home page](../../start/using/interface-description.md#home-page), in a [campaign](../../start/using/marketing-activities.md#creating-a-marketing-activity) or in a [marketing activity list](../../start/using/programs-and-campaigns.md#creating-a-campaign).

   >[!NOTE]
   >
   >워크플로우에서 직접 메일 활동을 추가할 수도 있습니다. For more on this, refer to the [Workflows](../../automating/using/direct-mail-delivery.md) guide.

   ![](assets/direct_mail_1.png)

1. Choose either the out-of-the-box **[!UICONTROL Direct mail]** template or one of your own templates. For more information on templates, refer to the [Managing templates](../../start/using/about-templates.md) section.

   ![](assets/direct_mail_2.png)

1. 게재의 일반 속성을 입력합니다.

   ![](assets/direct_mail_3.png)

1. 추출 파일에 포함할 대상 및 테스트 및 트랩 프로필을 정의합니다. See [Defining the direct mail audience](../../channels/using/defining-the-direct-mail-audience.md).

   ![](assets/direct_mail_4.png)

   >[!NOTE]
   >
   >대상자 정의는 일반 이메일 대상을 정의하는 것과 매우 유사합니다. See [Creating audiences](../../audiences/using/creating-audiences.md).

1. 파일의 컨텐츠를 편집합니다. 각 프로필, 파일 구조, 머리글 및 바닥글에 대해 포함할 열. See [Defining the direct mail content](../../channels/using/defining-the-direct-mail-content.md).

   ![](assets/direct_mail_5.png)

1. Click on the **[!UICONTROL Schedule]** section of the delivery dashboard to define the contact date. 우편의 경우, 연락처 날짜는 필수입니다. For more information, refer to [Scheduling the send](../../sending/using/about-scheduling-messages.md).

   ![](assets/direct_mail_8.png)

1. If you added test profiles (refer to [Adding test and trap profiles](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)), you can test your delivery before preparing the final file. 선택한 테스트 프로파일만 포함하는 샘플 파일을 만들 수 있습니다.

   Click on **[!UICONTROL Test]** to generate the sample file. Click on **[!UICONTROL Summary]**, in the top left corner, then select **[!UICONTROL Proofs]**. On the left part of the screen, select the proof and click on **[!UICONTROL Download file]**.

   >[!NOTE]
   >
   >**[!UICONTROL Export]** Adobe Campaign에서 파일을 내보내고 다운로드할 수 있도록 하려면 역할이 필요합니다. 관리자에게 문의하십시오.

   ![](assets/direct_mail_19.png)

1. Once you have defined your delivery content, audience and contact date, click on the **[!UICONTROL Prepare]** button, on the delivery dashboard.

   ![](assets/direct_mail_16.png)

   유형 지정 규칙이 적용됩니다. 예를 들어, 지정되지 않은 모든 우편 주소는 대상에서 제외됩니다. This is why you need to make sure you have checked the **[!UICONTROL Address specified]** box in your profiles' information (see [Recommendations](../../channels/using/about-direct-mail.md#recommendations)). If you have defined a **[!UICONTROL Maximum volume of message]** in the direct mail properties or at the template level, it will also be applied here.

   ![](assets/direct_mail_25.png)

   >[!NOTE]
   >
   >캠페인에서 오버레이된 프로필을 자동으로 제외시키는 글로벌 크로스채널 피로도 규칙을 설정할 수 있습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).

1. Click on **[!UICONTROL Explore file]** to preview the first 100 lines of the file.

   ![](assets/direct_mail_18.png)

   전체 파일은 화면의 왼쪽 부분에 있는 로컬 다운로드를 위해 액세스할 수 있습니다. Downloading the file generates a log entry in the **[!UICONTROL Export audits]** menu. For more information on export audits, refer to the [Auditing exports](../../administration/using/auditing-export-logs.md) section.

   >[!NOTE]
   >
   >**[!UICONTROL Export]** Adobe Campaign에서 파일을 내보내고 다운로드할 수 있도록 하려면 역할이 필요합니다. 관리자에게 문의하십시오.

   If you need to change the delivery content, you only have to click on the **[!UICONTROL Regenerate file]** button to take the change into account. 다시 준비할 필요가 없습니다.

   ![](assets/direct_mail_21.png)

1. To confirm that the file is final, click on **[!UICONTROL Confirm]** in the delivery dashboard.

   ![](assets/direct_mail_20.png)

이제 추출 파일을 DM 공급자에게 전송할 준비가 되었습니다. 이를 위해 다음과 같은 옵션이 있습니다.

* 일반 이메일을 통해 첨부 파일로 전송
* Send it via Campaign: perform your direct mail within a campaign [workflow](../../automating/using/direct-mail-delivery.md) and add a **[!UICONTROL Transfer file]** to send the file via FTP for example. [파일 전송을 참조하십시오](../../automating/using/transfer-file.md).

공급자가 잘못된 주소 목록을 검색하고 잘못된 주소를 자동으로 표시하는 Adobe Campaign로 이 정보를 보냅니다. See [Return to sender](../../channels/using/return-to-sender.md).
