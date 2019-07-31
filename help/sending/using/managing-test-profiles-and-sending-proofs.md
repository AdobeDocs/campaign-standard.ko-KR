---
title: 테스트 프로파일 관리 및 증명 전송
seo-title: 테스트 프로파일 관리 및 증명 전송
description: 테스트 프로파일 관리 및 증명 전송
seo-description: 테스트 프로파일과 교정을 관리하는 방법을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: EB 4 D 893 B -3724-4 B 15-9312-1 EC 74784368 D
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: preparing-and-testing-messages
discoiquuid: 37320 EC 5-196 C -4260-8156-98932 DA 3 E 4 A 5
context-tags: Seedmember, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 3cb698bc5025a59771128a8df493e7e126f00cab

---


# Managing test profiles and sending proofs{#managing-test-profiles-and-sending-proofs}

## About test profiles {#about-test-profiles}

테스트 프로필을 사용하면 정의된 타깃팅 기준과 일치하지 않는 추가 수신자를 타깃팅할 수 있습니다. 수신자의 데이터베이스에 대한 부정 사용을 탐지하거나 이메일이 받은 편지함에 도착하도록 메시지를 받는 사람의 대상에 추가됩니다.

You can manage your test profiles from the advanced menu **[!UICONTROL Profiles & audiences > Test profiles]**.

테스트 프로필에는 다음 컨텍스트의 메시지에서 사용할 수 있는 가상의 연락처 정보 또는 발신자에 의해 제어되는 연락처 정보가 포함되어 있습니다.

* For sending **Proofs**: the Proof is a specific message used to check the message before sending the finalized delivery to recipients. 증명 테스트 프로필은 컨텐츠 및 형식과 관련하여 배달을 확인하는 역할을 합니다. See [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).
* **이메일 렌더링의 경우: 이메일 렌더링 테스트 프로필은 메시지를 받는 메시지 받은 편지함에 따라 메시지가 표시되는 방식을 확인하는 데 사용됩니다.** 예를 들어, 웹메일, 메시지 서비스, 모바일 등을 들 수 있습니다. [이메일 렌더링을 참조하십시오](../../sending/using/email-rendering.md).

   **이메일 렌더링** 사용은 읽기 전용입니다. 이 사용 가능한 테스트 프로필은 Adobe Campaign에서 기본적으로 사용할 수 있습니다.

* ****&#x200B;트랩: 메시지는 클라이언트 파일이 부정적으로 사용되는지 여부를 식별하기 위한 수단으로 기본 Target에 전송된 대로 테스트 프로필로 전송됩니다.
* To **Preview** messages: a test profile can be selected when previewing a message to test the personalization elements.

![](assets/test_profile.png)

## Managing test profiles {#managing-test-profiles}

### Creating test profiles {#creating-test-profiles}

1. From the advanced menu, via the Adobe Campaign logo, select **Profiles &amp; audiences &gt; Test profiles** to access the list of test profiles.

   ![](assets/test_profile_creation_1.png)

1. **[!UICONTROL Test profiles]** 대시보드에서 **만들기를**&#x200B;클릭합니다.

   ![](assets/test_profile_creation_2.png)

1. 이 프로필에 대한 데이터를 입력합니다.

   ![](assets/test_profile_creation_3.png)

1. 테스트 프로필에 사용할 용도를 선택합니다.

   ![](assets/test_profile_creation_4.png)

1. Enter the contact channels **[!UICONTROL Email, Telephone, Mobile, Mobile app]**, as well as the test profile address if necessary.

   >[!NOTE]
   >
   >You can define a preferred email format: **[!UICONTROL Text]** or **[!UICONTROL HTML]**.

1. 트랜잭션 메시지의 개인화를 테스트하는 데 이 테스트 프로필을 사용하려면 이벤트 유형 및 이 이벤트의 데이터를 지정합니다.
1. Click **[!UICONTROL Create]** to save the test profile.

그러면 테스트 프로필이 프로필 목록에 추가됩니다.

**관련 항목:**

[테스트 프로필](https://helpx.adobe.com/campaign/kt/acs/using/acs-test-profiles-feature-video-use.html) 비디오 만들기

### Editing test profiles {#editing-test-profiles}

테스트 프로필을 편집하고 연결되어 있는 데이터를 참조하거나 이 프로필을 수정하려면 다음을 수행하십시오.

1. 해당 이미지를 클릭하여 편집할 테스트 프로필을 선택합니다.
1. 필드를 참조하거나 수정합니다.

   ![](assets/test_profile_edit.png)

1. Click **[!UICONTROL Save]** if you have entered your changes, or select the name of the test profile then **[!UICONTROL Test profiles]** in the section at the top of the screen to go back to the test profiles dashboard.

## Sending proofs {#sending-proofs}

증명은 메시지를 주 타겟으로 보내기 전에 메시지를 테스트할 수 있는 특정 메시지입니다.

증명 받는 사람은 메시지 (컨텐츠 및 양식) 승인을 담당하는 사람입니다. They are defined in the **Test profiles**. For more on this, see [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles).

증명을 보내려면 메시지 대상자에 테스트 프로필을 포함해야 합니다.

메시지:

1. **[!UICONTROL Send a test]** 단추를 클릭합니다.

   ![](assets/bat_select.png)

1. 사용할 증빙 유형을 선택하십시오.

   * **[!UICONTROL Email rendering]**: 받은 편지함에 따라 메시지가 수신되는 방식을 테스트하려면 이 옵션을 선택합니다. For more information, refer to [Email rendering](../../sending/using/email-rendering.md).
   * **[!UICONTROL Proof]**: 메시지를 기본 타겟으로 보내기 전에 테스트하려면 이 옵션을 선택합니다. 증빙 수신자는 콘텐츠와 형식을 모두 확인하여 배달 승인 권한을 받습니다.
   * **[!UICONTROL Proof + Email rendering]**: 이 옵션은 두 가지 이전 옵션을 결합합니다.
   ![](assets/bat_select1.png)

1. 선택 사항을 확인합니다.

   교정본이 테스트 프로필에 전송됩니다.

   ![](assets/bat_select2.png)

1. You can view your proofs using the **[!UICONTROL Proofs]** drop-down list.

   ![](assets/bat_view.png)

1. 요약에 액세스할 증명을 선택합니다. For an email, if you have selected the **Email rendering** option as the proof type, the **[!UICONTROL Access email rendering]** icon is displayed on the right of the proof label. [이메일 렌더링을 참조하십시오](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

증명을 받은 사람의 주석에 따라 게재 컨텐츠를 변경하라는 메시지가 표시될 수 있습니다. 수정 사항이 완료되면 이메일 준비를 다시 시작하고 증거 자료를 다시 보내야 합니다. Each new proof can be accessed using the **[!UICONTROL Show proofs]** button.

배달 내용을 완성할 때까지 필요한 만큼 증서를 보내야 합니다. 이 작업이 완료되면, 배달을 기본 Target로 보내고 승인 주기를 닫을 수 있습니다.

**관련 항목:**

[테스트 전송, 이메일 준비 및 보내기](https://helpx.adobe.com/campaign/kt/acs/using/acs-sending-test-preparing-sending-email-feature-video-use.html) 비디오

<!-- ## Sending proofs using additional data {#sending-proofs-using-additional-data}

This section describes how to send proofs using real customer data accessible via a workflow, as opposed to using fake test profile data. This allows you to check that the variables used in the workflow are accurate and to get a view of the message that your recipients will receive.

1. Create a test profile and enable **[!UICONTROL Proof]** and **[!UICONTROL Trap]** as the intended usage. For more on this, see [Managing test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles).

    This test profile becomes part of the targeted audience.

   >[!NOTE]
   >
   >When using a test profile as a trap, for any enriched fields in a message, the corresponding additional data is randomly picked from a real targeted profile and assigned to the trap test profile.

1. Access the marketing activity list and create a test workflow.

   See [Creating a workflow](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. Drag and drop a **[!UICONTROL Query]** activity into your workflow and open it.

   The Query activity is presented in the [Query](../../automating/using/query.md) section.

1. Add additional data from a linked table. For more on this, see [Enriching data](../../automating/using/query.md#enriching-data).

1. Drag and drop an **Email delivery** activity into your workflow and open it.

   The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.

1. From the email message dashboard, select the test profile with trap usage that you created.

1. Add to your email content personalization fields using the additional data that you defined in the Query activity.

1. Save the email and start the workflow.

During message preparation, the target count includes the test profile that you selected.
Once the message is sent, additional data is replaced by data from a real profile.

>[!NOTE]
   >
   >Only additional data are replaced. No real profile data such as first name or last name will be used for the test profile. -->
