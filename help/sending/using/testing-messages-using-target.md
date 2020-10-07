---
title: 타겟팅된 프로필을 사용하여 이메일 메시지 테스트
description: 타깃팅된 프로필 및 대체 주소를 사용하여 메시지를 테스트하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1502'
ht-degree: 4%

---


# 타겟팅된 프로필을 사용하여 이메일 메시지 테스트 {#testing-message-profiles}

## 개요 {#overview}

또한 [프로필을](../../audiences/using/managing-test-profiles.md)테스트하려면 타깃팅된 프로필 중 하나의 위치에 자신을 배치하여 이메일 메시지를 테스트할 수 있습니다. 그러면 프로필에서 받게 될 메시지(사용자 정의 필드, 동적 및 개인화된 정보, 워크플로우의 추가 데이터 등)를 정확하게 표현할 수 있습니다.

>[!NOTE]
>
> 이 기능은 이메일 메시지만 사용할 수 있습니다.

주요 단계는 다음과 같습니다.

1. 메시지를 구성한 다음 준비 **단계를** 시작합니다.
1. **메시지가 타깃팅한 프로필** 중에서 하나 또는 여러 프로필을 선택합니다.
1. 각 프로파일과 **연결하여 교정을** 보낼 대체 주소를 지정합니다.
1. (선택 사항) 각 프로필에 대해 **입증** 제목 라인에 추가할 접두사를 정의합니다.
1. **이메일 디자이너는** 프로필에 대한 메시지가 표시되는 방식을 미리 봅니다.
1. 증거 자료 전송

글로벌 프로세스에 대한 자세한 내용은 [여기](https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html)있는 자습서 비디오를 참조하십시오.

>[!IMPORTANT]
>
>이 기능을 사용하면 프로필 개인 정보를 외부 이메일 주소로 보낼 수 있습니다. Campaign Standard에서 개인 정보 요청(GDPR 및 CPA)을 실행하면 해당 요청이 외부에서 실행되지 않습니다.

## 프로필 및 대체 주소 선택 {#selecting-profiles}

테스트를 위해 대상 프로파일을 사용하려면 먼저 선택한 다음 교정을 받을 대체 주소를 정의해야 합니다. 이렇게 하려면 타깃팅된 프로필 [중에서 특정 프로필을](#selecting-individual-profiles) 선택하거나 기존 대상의 프로필을 [가져올 수 있습니다](#importing-from-audience).

>[!NOTE]
>
>테스트할 프로파일을 최대 100개까지 선택할 수 있습니다.

### 개별 프로필 선택 {#selecting-individual-profiles}

1. 메시지 대시보드에서 메시지 준비가 성공했는지 확인한 다음 **[!UICONTROL Audience]** 블록을 클릭합니다.

   ![](assets/substitution_preparation.png)

1. 탭에서 **[!UICONTROL Profile substitutions]** 단추를 클릭하여 테스트에 사용할 프로필을 선택합니다 **[!UICONTROL Create element]** .

   ![](assets/substitution_tab.png)

1. 메시지를 기준으로 하는 프로필 목록을 표시하려면 프로필 선택 단추를 클릭합니다.

   ![](assets/substitution_recipient_selection.png)

1. 테스트에 사용할 프로필을 선택한 다음 원하는 대체 주소를 **[!UICONTROL Address]** 필드에 입력한 다음 을 클릭합니다 **[!UICONTROL Confirm]**. 프로필을 대상으로 하는 모든 교정은 이 프로필에 대해 데이터베이스에 정의된 교정이 아닌 이 이메일 주소로 전송됩니다.

   교정의 제목 줄에 특정 접두사를 추가하려면 **[!UICONTROL Subject line prefix]** 필드를 채웁니다.

   >[!NOTE]
   >
   >제목 줄 접두사는 최대 500자까지 사용할 수 있습니다.

   ![](assets/substitution_address.png)

   접두사가 다음과 같이 표시됩니다.

   ![](assets/substitution_prefixsample.png)

1. 프로필에는 대체 주소와 접두사가 연결되어 있습니다. 테스트에 사용할 모든 프로필에 대해 위 단계를 반복한 다음 을 클릭합니다 **[!UICONTROL Confirm]**.

   ![](assets/substitution_recipients_confirm.png)

   동일한 프로필에 대해 여러 대체 주소로 교정을 보내려면 필요한 만큼 이 프로필을 추가해야 합니다.

   아래 예에서 프로필 John Smith를 기반으로 한 자료는 두 개의 다른 대체 주소로 전송됩니다.

   ![](assets/substitution_multiple_addresses.png)

1. 모든 프로필 및 대체 주소가 정의된 경우 메시지를 테스트하기 위한 증거를 보낼 수 있습니다. 이렇게 하려면 **[!UICONTROL Test]** 단추를 클릭한 다음 수행할 테스트 유형을 선택합니다.

   메시지 대상에 테스트 프로필이 추가되지 않은 경우 **[!UICONTROL Email rendering]** 및 **[!UICONTROL Proof + Email rendering]** 옵션을 사용할 수 없습니다.  For more information on proofs sending, refer to [this section](../../sending/using/sending-proofs.md).

   ![](assets/substitution_send_test.png)

>[!IMPORTANT]
>
>메시지를 변경한 경우 메시지 준비를 다시 시작하십시오. 그렇지 않으면 변경 사항이 증명에 반영되지 않습니다.

### 대상자로부터 프로필 가져오기 {#importing-from-audience}

Campaign Standard을 사용하면 테스트에 사용할 수 있는 프로필 대상을 가져올 수 있습니다. 예를 들어, 다른 프로필을 대상으로 하는 전체 메시지 세트와 고유한 이메일 주소로 보낼 수 있습니다.

또한 대상이 주소와 접두사 열로 이미 구성된 경우 **[!UICONTROL Profile substitutions]** 탭에서 이러한 정보를 가져올 수 있습니다. 대체 주소가 있는 대상 가져오기의 예는 [이 섹션에 자세히 설명되어 있습니다](#use-case).

>[!NOTE]
>
>대상을 가져올 때 메시지 대상에 해당하는 프로파일만 선택되어 **[!UICONTROL Profile substitutions]** 탭에 추가됩니다.

대상자로부터 테스트에 사용할 프로필을 가져오려면 다음 단계를 수행하십시오.

1. 메시지 대시보드에서 메시지 준비에 성공했는지 확인한 다음 **[!UICONTROL Audience]** 블록을 클릭합니다.

   ![](assets/substitution_preparation.png)

1. **[!UICONTROL Profile substitutions]** 탭에서 **[!UICONTROL Import from an audience]**&#x200B;을(를) 클릭합니다 .

   ![](assets/substitution_audience_import.png)

1. 사용할 대상을 선택한 다음 대체 주소와 대상자에게 전송된 교정에 사용할 접두사를 입력합니다.

   >[!NOTE]
   >
   >제목 줄 접두사는 최대 500자까지 사용할 수 있습니다.

   ![](assets/substitution_audience_define.png)

   사용할 대체 주소 및/또는 접두사가 이미 대상에 정의되어 있는 경우 옵션을 선택한 다음 해당 정보를 검색하는 데 사용할 열을 **[!UICONTROL From Audience]** 지정합니다.

   ![](assets/substitution_fromaudience.png)

1. **[!UICONTROL Import]** 버튼을 클릭합니다. 메시지 대상에 해당하는 대상의 프로필은 **[!UICONTROL Profile substitution]** 탭 및 관련 대체 주소 및 접두사에 추가됩니다.

![](assets/substitution_audience_imported.png)

>[!NOTE]
>
>동일한 대상을 다시 한 번 가져오는 경우, 다른 대체 주소 및/또는 접두사가 있는 경우, 프로필은 이전 가져오기에서 가져온 프로필 외에 목록에 추가됩니다.

## 대상 프로필로 메시지 미리 보기

>[!NOTE]
>
>미리 보기는 이메일 디자이너에서만 사용할 수 있습니다.

타깃팅된 프로파일을 사용하여 메시지를 미리 보려면 이러한 프로필을 **[!UICONTROL Profile substitution]** 목록에 추가해야 합니다(프로필 및 대체 주소 [정의 참조](#selecting-profiles)).

메시지에 개인화 필드를 사용하려면 메시지 준비를 시작하기 **전에** 필드를 추가해야 합니다. 그렇지 않으면 미리 보기에서 고려하지 않습니다. 따라서 개인화 필드가 변경되면 메시지 준비를 다시 실행해야 합니다.

프로필 대체를 사용하여 메시지를 미리 보려면 다음 단계를 수행합니다.

1. 메시지 대시보드에서 컨텐츠 스냅샷을 클릭하여 이메일 디자이너에서 메시지를 엽니다.

   ![](assets/substitution_preview_access.png)

1. Select the **[!UICONTROL Preview]** tab, then click **[!UICONTROL Change profile]**.

   ![](assets/substitution_preview_changeprofile.png)

1. 테스트를 위해 추가된 대체 프로필을 표시하려면 **[!UICONTROL Profile Substitution]** 탭을 클릭합니다.

   미리 보기에 사용할 프로파일을 선택한 다음 을 클릭합니다 **[!UICONTROL Select]**.

   ![](assets/substitution_preview_selection.png)

1. 메시지 미리 보기가 표시됩니다. 화살표를 사용하여 선택한 프로필 간을 이동할 수 있습니다.

   ![](assets/substitution_preview.png)

## 사용 사례 {#use-case}

이 경우 특정 프로필 세트에 개인화된 이메일 뉴스레터를 발송하려고 합니다. 뉴스레터를 보내기 전에 타깃팅된 프로필 중 일부를 사용하여 미리 보고 외부 파일에 정의된 내부 이메일 주소로 교정을 전송하려고 합니다.

이 사용 사례의 주요 단계는 다음과 같습니다.

1. 테스트에 사용할 대상을 만듭니다.
1. 프로파일을 타깃팅하고 뉴스레터를 전송하는 워크플로우를 만듭니다.
1. 메시지의 프로필 대체 요소를 구성합니다.
1. 타깃팅된 프로필을 사용하여 메시지를 미리 봅니다.
1. 증명을 보냅니다.

### 1단계:테스트에 사용할 대상 만들기

1. 대상을 만들기 위해 가져올 파일을 준비합니다. 본사의 경우, 증빙 자료에 사용할 대체 주소와 증빙 제목 줄에 추가할 접두사가 포함되어야 합니다.

   이 예에서, &quot;oliver.vaughan@internal.com&quot; 이메일 주소는 &quot;john.doe@mail.com&quot; 이메일 주소를 사용하여 프로파일을 타깃팅하는 메시지 증거를 수신하게 됩니다. &quot;JD&quot; 접두사가 증표의 제목 줄에 추가됩니다.

   ![](assets/substitution_uc1.png)

1. 파일에서 대상을 만드는 워크플로우를 만듭니다. 이렇게 하려면 아래 활동을 추가하고 구성합니다.

   * **[!UICONTROL Load file]** 활동:CSV 파일을 가져옵니다(이 활동에 대한 자세한 내용은 [이 섹션](../../automating/using/load-file.md)참조).
   * **[!UICONTROL Reconciliation]** 활동:파일의 정보를 데이터베이스의 정보에 연결합니다. 이 예에서는 프로필 이메일 주소를 조정 필드로 사용합니다(이 활동에 대한 자세한 내용은 [이 섹션](../../automating/using/reconciliation.md)참조).
   * **[!UICONTROL Save audience]** 활동:가져온 파일을 기준으로 대상을 만듭니다(이 활동에 대한 자세한 내용은 [이 섹션](../../automating/using/save-audience.md)참조).

   ![](assets/substitution_uc2.png)

1. 워크플로우를 실행한 다음 **[!UICONTROL Audiences]** 탭으로 이동하여 원하는 정보가 포함된 대상이 생성되었는지 확인합니다.

   이 예에서는 대상이 세 개의 프로필로 구성됩니다. 각 이메일은 교정을 받을 수 있는 대체 이메일 주소에 연결되며 증명 제목 줄에 사용할 접두사가 추가됩니다.

   ![](assets/substitution_uc3.png)

### 2단계:프로파일을 타깃팅하고 뉴스레터를 전송하는 워크플로우 구축

1. 추가 **[!UICONTROL Query]** 및 **[!UICONTROL Email delivery]** 활동을 선택한 다음 필요에 따라 구성합니다( [쿼리](../../automating/using/query.md) 및 [이메일 배달](../../automating/using/email-delivery.md) 섹션 참조).

   ![](assets/substitution_uc4.png)

1. 워크플로우를 실행하고 메시지 준비가 성공했는지 확인합니다.

### 3단계:메시지의 프로필 대체 탭 구성

1. 활동을 **[!UICONTROL Email delivery]** 엽니다. In the message dashboard, click the **[!UICONTROL Audience]** block.

   ![](assets/substitution_uc5.png)

1. Select the **[!UICONTROL Profile substitutions]** tab, then click **[!UICONTROL Import from an audience]**.

   ![](assets/substitution_uc6.png)

1. 필드에서 **[!UICONTROL Audience]** 파일에서 만든 대상을 선택합니다.

   ![](assets/substitution_uc7.png)

1. 교정을 전송할 때 사용할 대체 주소와 제목 줄 접두사를 정의합니다.

   이렇게 하려면 **[!UICONTROL From audience]** 옵션을 선택한 다음 정보가 포함된 대상의 열을 선택합니다.

   ![](assets/substitution_uc8.png)

1. **[!UICONTROL Import]** 버튼을 클릭합니다. 대상 프로필의 관련 대체 주소 및 제목 줄 접두사와 함께 목록에 추가됩니다.

   ![](assets/substitution_uc9.png)

   >[!NOTE]
   >
   >이 경우, 대상의 모든 프로필은 **[!UICONTROL Query]** 활동의 타깃팅입니다. 이러한 프로필 중 하나가 메시지 대상에 속하지 않으면 목록에 추가되지 않습니다.

### 4단계:타깃팅된 프로필을 사용하여 메시지 미리 보기

1. 메시지 대시보드에서 컨텐츠 스냅샷을 클릭하여 이메일 디자이너에서 메시지를 엽니다.

   ![](assets/substitution_uc10.png)

1. Select the **[!UICONTROL Preview]** tab, then click **[!UICONTROL Change profile]**.

   ![](assets/substitution_uc_preview.png)

1. 이전에 추가된 대체 프로필을 표시하려면 **[!UICONTROL Profile Substitution]** 탭을 클릭합니다.

   미리 보기에 사용할 프로파일을 선택한 다음 을 클릭합니다 **[!UICONTROL Select]**.

   ![](assets/substitution_uc_selectpreview.png)

1. 메시지 미리 보기가 표시됩니다. 화살표를 사용하여 선택한 프로필 간을 이동할 수 있습니다.

   ![](assets/substitution_uc_previewprofile.png)

### 5단계:교정본 보내기

1. In the message dashboard, click the **[!UICONTROL Test]** button, then confirm.

   ![](assets/substitution_uc_sendproof.png)

1. 교정본은 **[!UICONTROL Profile substitutions]** 탭에 구성된 내용에 따라 전송됩니다.

   ![](assets/substitution_uc_proofs.png)
