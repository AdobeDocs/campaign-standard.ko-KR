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
source-git-commit: 27447db9ee0dd387c39976c7bd4e157a4b7899b8

---


# 테스트 프로파일 관리 및 증명 전송{#managing-test-profiles-and-sending-proofs}

## 테스트 프로필 정보 {#about-test-profiles}

테스트 프로필을 사용하면 정의된 타깃팅 기준과 일치하지 않는 추가 수신자를 타깃팅할 수 있습니다. 수신자의 데이터베이스에 대한 부정 사용을 탐지하거나 이메일이 받은 편지함에 도착하도록 메시지를 받는 사람의 대상에 추가됩니다.

고급 메뉴에서 테스트 프로필을 관리할 **[!UICONTROL Profiles & audiences > Test profiles]**&#x200B;수 있습니다.

테스트 프로필에는 다음 컨텍스트의 메시지에서 사용할 수 있는 가상의 연락처 정보 또는 발신자에 의해 제어되는 연락처 정보가 포함되어 있습니다.

* 증거 자료 전송 ****: 증빙 자료는 수신자에게 최종 배달을 보내기 전에 메시지를 확인하는 데 사용되는 특정 메시지입니다. 증명 테스트 프로필은 컨텐츠 및 형식과 관련하여 배달을 확인하는 역할을 합니다. 증명 [전송을 참조하십시오](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).
* **이메일 렌더링의 경우: 이메일 렌더링 테스트 프로필은 메시지를 받는 메시지 받은 편지함에 따라 메시지가 표시되는 방식을 확인하는 데 사용됩니다.** 예를 들어, 웹메일, 메시지 서비스, 모바일 등을 들 수 있습니다. [이메일 렌더링을 참조하십시오](../../sending/using/email-rendering.md).

   **이메일 렌더링** 사용은 읽기 전용입니다. 이 사용 가능한 테스트 프로필은 Adobe Campaign에서 기본적으로 사용할 수 있습니다.

* ****&#x200B;트랩: 메시지는 기본 Target에 전송된 대로 테스트 프로필로 전송됩니다. 트랩 [사용을 참조하십시오](../../sending/using/managing-test-profiles-and-sending-proofs.md#using-traps).
* 메시지를 **미리 보려면** : 개인화 요소를 테스트하기 위해 메시지를 미리 볼 때 테스트 프로필을 선택할 수 있습니다. 메시지 [미리 보기를 참조하십시오](/help/sending/using/previewing-messages.md).

![](assets/test_profile.png)

## 테스트 프로필 관리 {#managing-test-profiles}

### 테스트 프로필 만들기 {#creating-test-profiles}

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **프로필 및 대상 &gt; 테스트 프로필을** 선택하여 테스트 프로필 목록에 액세스합니다.

   ![](assets/test_profile_creation_1.png)

1. **[!UICONTROL Test profiles]** 대시보드에서 **만들기를**&#x200B;클릭합니다.

   ![](assets/test_profile_creation_2.png)

1. 이 프로필에 대한 데이터를 입력합니다.

   ![](assets/test_profile_creation_3.png)

1. 테스트 프로필에 사용할 용도를 선택합니다.

   ![](assets/test_profile_creation_4.png)

1. 필요한 경우 연락처 채널뿐만 **[!UICONTROL Email, Telephone, Mobile, Mobile app]**&#x200B;아니라 테스트 프로필 주소를 입력합니다.

   >[!NOTE]
   >
   >다음과 같은 기본 이메일 형식을 정의할 수 있습니다. **[!UICONTROL Text]** **[!UICONTROL HTML]**&#x200B;또는

1. 트랜잭션 메시지의 개인화를 테스트하는 데 이 테스트 프로필을 사용하려면 이벤트 유형 및 이 이벤트의 데이터를 지정합니다.
1. 을 클릭하여 **[!UICONTROL Create]** 테스트 프로필을 저장합니다.

그러면 테스트 프로필이 프로필 목록에 추가됩니다.

**관련 항목:**

[테스트 프로필](https://helpx.adobe.com/campaign/kt/acs/using/acs-test-profiles-feature-video-use.html) 비디오 만들기

### 테스트 프로필 편집 {#editing-test-profiles}

테스트 프로필을 편집하고 연결되어 있는 데이터를 참조하거나 이 프로필을 수정하려면 다음을 수행하십시오.

1. 해당 이미지를 클릭하여 편집할 테스트 프로필을 선택합니다.
1. 필드를 참조하거나 수정합니다.

   ![](assets/test_profile_edit.png)

1. 변경 사항을 입력한 **[!UICONTROL Save]** 경우를 클릭하거나 화면 맨 위의 섹션에서 테스트 프로필 **[!UICONTROL Test profiles]** 이름을 선택한 다음, 화면 맨 위의 섹션에서 테스트 프로필 대시보드로 돌아갑니다.

## 증거 자료 전송 {#sending-proofs}

증명은 메시지를 주 타겟으로 보내기 전에 메시지를 테스트할 수 있는 특정 메시지입니다.

증명 받는 사람은 메시지 (컨텐츠 및 양식) 승인을 담당하는 사람입니다. 테스트 프로필에 **정의됩니다**. 이에 대한 자세한 내용은 테스트 프로필 [관리를](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles)참조하십시오.

증명을 보내려면 메시지 대상자에 테스트 프로필을 포함해야 합니다.

메시지:

1. **[!UICONTROL Send a test]** 단추를 클릭합니다.

   ![](assets/bat_select.png)

1. 사용할 증빙 유형을 선택하십시오.

   * **[!UICONTROL Email rendering]**: 받은 편지함에 따라 메시지가 수신되는 방식을 테스트하려면 이 옵션을 선택합니다. 자세한 내용은 [이메일 렌더링을](../../sending/using/email-rendering.md)참조하십시오.
   * **[!UICONTROL Proof]**: 메시지를 기본 타겟으로 보내기 전에 테스트하려면 이 옵션을 선택합니다. 증빙 수신자는 콘텐츠와 형식을 모두 확인하여 배달 승인 권한을 받습니다.
   * **[!UICONTROL Proof + Email rendering]**: 이 옵션은 두 가지 이전 옵션을 결합합니다.
   ![](assets/bat_select1.png)

1. 선택 사항을 확인합니다.

   교정본이 테스트 프로필에 전송됩니다.

   ![](assets/bat_select2.png)

1. 드롭다운 목록을 사용하여 교정본을 **[!UICONTROL Proofs]** 볼 수 있습니다.

   ![](assets/bat_view.png)

1. 요약에 액세스할 증명을 선택합니다. 이메일의 경우 **, 이메일 렌더링** 옵션을 증명 유형으로 선택한 경우, 증빙 레이블의 오른쪽에 아이콘이 **[!UICONTROL Access email rendering]** 표시됩니다. [이메일 렌더링을 참조하십시오](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

증명을 받은 사람의 주석에 따라 게재 컨텐츠를 변경하라는 메시지가 표시될 수 있습니다. 수정 사항이 완료되면 이메일 준비를 다시 시작하고 증거 자료를 다시 보내야 합니다. 단추를 사용하여 각각의 새 증빙 자료를 액세스할 **[!UICONTROL Show proofs]** 수 있습니다.

배달 내용을 완성할 때까지 필요한 만큼 증서를 보내야 합니다. 이 작업이 완료되면, 배달을 기본 Target로 보내고 승인 주기를 닫을 수 있습니다.

**관련 항목:**

[테스트 전송, 이메일 준비 및 보내기](https://helpx.adobe.com/campaign/kt/acs/using/acs-sending-test-preparing-sending-email-feature-video-use.html) 비디오

## 트랩 사용 {#using-traps}

트랩을 사용할 때, 클라이언트 파일이 사기적 사용 중인지 여부를 식별하기 위한 수단으로 기본 Target에 전송된 대로 테스트 프로필로 메시지가 전송됩니다.

트랩은 원래 우편 배달을 위해 설계되었습니다. 이를 통해 다음을 수행할 수 있습니다.
* 다이렉트 메일 공급자가 실제로 통신을 보내고 있는지 확인합니다.
* 고객과 동일한 조건에서 동시에 메일을 받을 수 있습니다.
* 전송된 메일의 정확한 사본을 보관하십시오.
* 다이렉트 메일 공급자가 클라이언트 목록을 오용하지 않았는지 확인합니다. 실제로 다른 커뮤니케이션이 테스트 프로필의 주소로 전송되면 클라이언트 파일이 모르게 사용되었을 수 있습니다. 따라서 테스트 프로필의 주소는 이러한 목적으로만 사용해야 합니다.

DM (Direct Mail) 대상자에게 트랩 추가에 대한 자세한 내용은 테스트 및 트랩 프로필 [추가를](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles)참조하십시오.

다른 통신 채널의 경우, 기본 Target에 트랩 테스트 프로필을 추가하여 다음을 수행할 수 있습니다.
* 메시지가 성공적으로 전송되었는지 확인합니다.
* 메시지를 정확하게 복사하여 보관할 수 있습니다.
* 전송 및 수신 시기를 추적합니다.

테스트 프로필을 트랩으로 사용하려면 메시지 대상에 포함해야 합니다.

>[!NOTE]
>
>[증명](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) 또는 [이메일 렌더링에](../../sending/using/email-rendering.md)사용된 테스트 프로필을 테스트하는 것과 달리, 메시지는 기본 Target와 트랩으로 사용되는 테스트 프로필에 동시에 전송됩니다.

메시지 대상을 정의할 때:

1. **[!UICONTROL Test profiles]** 탭에서 테스트 프로필을 선택합니다. **[!UICONTROL Trap]** 의도한 대로 사용해야 합니다.

   ![](assets/trap_select.png)

1. 메시지 콘텐트가 준비되면 **[!UICONTROL Prepare]** 버튼을 클릭합니다. 보내기 [준비를 참조하십시오](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >메인 타겟을 선택했는지 확인합니다. 그렇지 않으면 메시지를 보낼 수 없습니다.

1. **[!UICONTROL Confirm]** 단추를 클릭합니다. 전송 [확인을 참조하십시오](../../sending/using/confirming-the-send.md).

   ![](assets/trap_confirm.png)

메시지는 기본 Target와 테스트 프로필에 전송됩니다.

>[!NOTE]
>
>테스트 프로필을 트랩으로 사용할 때, 메시지의 모든 농축 필드에 대해 해당 추가 데이터는 실제 타깃팅된 프로필에서 임의로 선택되고 트랩 테스트 프로필에 할당됩니다. 강화에 대한 자세한 내용은 [이 예제를](../../automating/using/enrichment.md#example--enriching-profile-data-with-data-contained-in-a-file)참조하십시오.
