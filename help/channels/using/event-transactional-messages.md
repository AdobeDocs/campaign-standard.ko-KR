---
title: 이벤트 트랜잭션 메시지
description: 이벤트 트랜잭션 메시지를 만들고 게시하는 방법에 대해 알아봅니다.
page-status-flag: never-activated
uuid: d747feb5-58fb-4e12-a176-404f0eca5391
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: 4f6317a1-9dfe-4714-bc1c-393629d855cd
context-tags: deliveryTransactionalTemplate,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b70e18be29fd48d102313f6d741e9ffe053cc34

---


# 이벤트 트랜잭션 메시지{#event-transactional-messages}

이벤트를 타깃팅하는 이벤트 트랜잭션 메시지를 보낼 수 있습니다. 이 유형의 트랜잭션 메시지에 프로필 정보가 포함되어 있지 않습니다.전달 대상은 이벤트 자체에 포함된 데이터로 정의됩니다.

이벤트를 만들고 게시하면( [이 섹션에](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle)설명된 대로 장바구니 포기) 해당 트랜잭션 메시지가 자동으로 생성됩니다.

구성 단계는 트랜잭션 메시지를 [보낼 이벤트 구성](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) 섹션에 나와 있습니다.

이벤트가 트랜잭션 메시지 전송을 트리거하려면 메시지를 개인화한 다음 테스트하여 게시해야 합니다.

>[!NOTE]
>
>트랜잭션 메시지에 액세스하려면 **[!UICONTROL Administrators (all units)]** 보안 그룹의 일부여야 합니다.
>
>거래 메시지에 프로필 정보가 포함되어 있지 않으므로 피로 규칙과 호환하지 않습니다(프로필로 인해 농축된 경우에도). 피로 [규칙을](../../administration/using/fatigue-rules.md#choosing-the-channel)참조하십시오.

## 트랜잭션 메시지에서 테스트 프로필 정의 {#defining-a-test-profile-in-a-transactional-message}

메시지를 미리 보고 확인할 수 있는 증명을 보낼 수 있도록 적용된 테스트 프로필을 정의합니다.

### 트랜잭션 메시지 내에 테스트 프로필 만들기 {#creating-a-test-profile-within-the-transactional-----------message}

1. 만든 메시지에 액세스하려면 **[!UICONTROL Adobe Campaign]** 로고를 클릭하고 왼쪽 상단 모서리에서 **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Transactional messages]**&#x200B;을 선택합니다.

   ![](assets/message-center_4.png)

1. 이벤트에 연결할 테스트 프로필을 만듭니다.

   ![](assets/message-center_test-profile.png)

1. 섹션에서 JSON 형식으로 전송할 정보를 **[!UICONTROL Event data used for personalization]** 지정합니다. 이는 메시지를 미리 볼 때와 테스트 프로필에서 증거를 받을 때 사용되는 컨텐츠입니다.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >프로파일 테이블과 관련된 정보를 입력할 수도 있습니다. 트랜잭션 [메시지 컨텐츠](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content)강화를 참조하십시오.

1. 생성된 후 트랜잭션 메시지에 테스트 프로필이 미리 지정됩니다. 메시지 **[!UICONTROL Test profiles]** 블록을 클릭하여 증명 대상을 확인합니다.

   ![](assets/message-center_5.png)

### 트랜잭션 메시지 외부에 테스트 프로필 만들기 {#creating-a-test-profile-outside-the-transactional-----------message}

새 테스트 프로필을 만들거나 **[!UICONTROL Test profiles]** 메뉴에 이미 있는 테스트 프로필을 사용할 수도 있습니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Adobe Campaign]** 로고를 클릭한 다음 **[!UICONTROL Profiles & audiences]** &gt; 를 **[!UICONTROL Test profiles]**&#x200B;선택합니다.
1. 선택한 테스트 프로필의 페이지 **[!UICONTROL Event]** 섹션에서 방금 만든 이벤트를 선택합니다. 이 예에서 "장바구니 포기(EVTcart포기)"를 선택합니다.
1. 텍스트 **[!UICONTROL Event data]** 상자에서 JSON 형식으로 전송할 정보를 지정합니다.

   ![](assets/message-center_3.png)

1. 변경 내용을 저장합니다.

이제 만든 메시지에 액세스하고 업데이트된 테스트 프로필을 선택할 수 있습니다.

**관련 항목:**

* [테스트 프로필 관리](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [대상 정의](../../audiences/using/creating-audiences.md)

## 트랜잭션 메시지 개인화 {#personalizing-a-transactional-message}

트랜잭션 메시지에서 개인화를 설정하려면 아래 단계를 따르십시오.

1. 메시지의 제목과 내용을 수정하려면 **[!UICONTROL Content]** 블록을 클릭합니다. 이 예에서는 이미지와 텍스트가 포함된 템플릿을 선택합니다. 이메일 컨텐츠 템플릿에 대한 자세한 내용은 템플릿을 [사용하여](../../designing/using/using-reusable-content.md#designing-templates)디자인을 참조하십시오.

   ![](assets/message-center_6.png)

1. 제목을 추가하고 필요에 따라 메시지 내용을 편집합니다.

   >[참고]
   >
   >중단된 장바구니에 대한 링크는 사용자를 장바구니에 리디렉션하는 외부 URL에 대한 링크입니다. 이 매개 변수는 Adobe Campaign에서 관리되지 않습니다.

1. 이 예에서는 이벤트를 [만들 때 정의한 필드를](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message)세 개 추가하려고 합니다.이름, 마지막 제품 상담, 총 장바구니 금액 이렇게 하려면 메시지 컨텐츠에 개인화 필드를 [삽입합니다](../../designing/using/personalization.md#inserting-a-personalization-field) .

1. &gt; **[!UICONTROL Context]****[!UICONTROL Real-time event]** &gt; **[!UICONTROL Event context]**&#x200B;을 통해 해당 필드를 찾습니다.

   ![](assets/message-center_7.png)

1. 메시지의 컨텐츠를 강화하려면 이벤트를 연결한 표에서 필드를 선택하여 필드를 추가합니다. 이 예제에서는 &gt; &gt; &gt; 를 통해 **[!UICONTROL Title (salutation)]** 표의 **[!UICONTROL Profile]** 필드를 선택합니다 **[!UICONTROL Context]** **[!UICONTROL Real-time event]** **[!UICONTROL Event context]**.

   ![](assets/message-center_7-enrichment.png)

1. 필요한 모든 필드를 삽입합니다.

   ![](assets/message-center_8.png)

1. 이 이벤트에 대해 정의한 프로필을 선택하여 메시지를 미리 봅니다.

   메시지 미리 보기 단계는 메시지 [미리 보기](../../sending/using/previewing-messages.md) 섹션에 자세히 설명되어 있습니다.

   ![](assets/message-center_9.png)

   개인화 필드가 테스트 프로필에 입력된 정보와 일치하는지 확인할 수 있습니다. 자세한 내용은 트랜잭션 [메시지에서](#defining-a-test-profile-in-a-transactional-message)테스트 프로필 정의를 참조하십시오.

## 트랜잭션 메시지에서 제품 목록 사용 {#using-product-listings-in-a-transactional-message}

트랜잭션 이메일의 내용에서 하나 이상의 데이터 컬렉션을 참조하는 제품 목록을 만들 수 있습니다. 예를 들어 장바구니 포기 이메일에는 사용자가 웹 사이트를 떠날 때 장바구니에 있었던 모든 제품 목록과 이미지, 가격 및 각 제품에 대한 링크가 포함될 수 있습니다.

>[!CAUTION]
>
>제품 목록은 이메일 디자이너 인터페이스를 통해 트랜잭션 이메일 메시지를 편집할 때만 [사용할 수](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface) 있습니다.

트랜잭션 메시지에 중단된 제품 목록을 추가하려면 아래 단계를 따르십시오.

트랜잭션 이메일에서 제품 목록을 구성하는 데 필요한 단계를 설명하는 비디오 세트를 볼 수도 있습니다. 자세한 내용은 [이 페이지를](https://helpx.adobe.com/campaign/kt/acs/using/acs-product-listings-in-transactional-emails-feature-video-setup.html)참조하십시오.

>[!NOTE]
>
>Adobe Campaign은 중첩된 제품 목록을 지원하지 않습니다. 즉, 다른 제품 목록 내에 제품 목록을 포함할 수 없습니다.

### 제품 목록 정의 {#defining-a-product-listing}

거래 메시지에서 제품 목록을 사용하려면 이벤트 수준에서 표시할 목록의 각 제품에 대한 제품 목록과 필드를 정의해야 합니다. 자세한 내용은 데이터 [컬렉션](../../administration/using/configuring-transactional-messaging.md#defining-data-collections)정의를 참조하십시오.

1. 트랜잭션 메시지에서 **[!UICONTROL Content]** 블록을 클릭하여 이메일 컨텐츠를 수정합니다.
1. 구조 구성 요소를 작업 영역으로 드래그하여 놓습니다. 자세한 내용은 이메일 [구조](../../designing/using/designing-from-scratch.md#defining-the-email-structure)편집을 참조하십시오.

   예를 들어, 1열 구조 구성 요소를 선택하고 텍스트 구성 요소, 이미지 구성 요소 및 단추 구성 요소를 추가합니다. 자세한 내용은 조각 및 [구성 요소](../../designing/using/designing-from-scratch.md#defining-the-email-structure)추가를 참조하십시오.

1. 방금 만든 구조 구성 요소를 선택하고 컨텍스트 도구 모음에서 **[!UICONTROL Enable product listing]** 아이콘을 클릭합니다.

   ![](assets/message-center_loop_create.png)

   구조 구성 요소는 주황색 프레임으로 강조 표시되고 **[!UICONTROL Product listing]** 설정은 왼쪽 팔레트에 표시됩니다.

   ![](assets/message-center_loop_palette.png)

1. 컬렉션의 요소가 표시되는 방식을 선택합니다.

   * **[!UICONTROL Row]**:가로로, 다른 행 아래의 각 요소를 의미합니다.
   * **[!UICONTROL Column]**:수직(같은 행에서 다른 요소 옆에 있는 각 요소)을 의미합니다.
   >[!NOTE]
   >
   >이 **[!UICONTROL Column]** 옵션은 다중 열 구조 구성 요소( **[!UICONTROL 2:2 column]**, **[!UICONTROL 3:3 column]** 및 **[!UICONTROL 4:4 column]** )를 사용할 때만 사용할 수 있습니다. 제품 목록을 편집할 때 첫 번째 열만 채웁니다.다른 열은 고려되지 않습니다. 구조 구성 요소 선택에 대한 자세한 내용은 [이메일 구조](../../designing/using/designing-from-scratch.md#defining-the-email-structure)편집을 참조하십시오.

1. 트랜잭션 메시지와 관련된 이벤트를 구성할 때 만든 데이터 수집을 선택합니다. &gt; **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]** &gt; **[!UICONTROL Event context]** 노드에서 찾을 수 있습니다.

   ![](assets/message-center_loop_selection.png)

   이벤트 구성에 대한 자세한 내용은 데이터 [컬렉션](../../administration/using/configuring-transactional-messaging.md#defining-data-collections)정의를 참조하십시오.

1. 드롭다운 목록을 사용하여 이메일에 표시된 목록을 시작할 요소를 선택합니다. **[!UICONTROL First item]**

   예를 들어 2를 선택하면 컬렉션의 첫 번째 항목이 이메일에 표시되지 않습니다. 제품 목록은 두 번째 항목에서 시작됩니다.

1. 목록에 표시할 최대 항목 수를 선택합니다.

   >[!NOTE]
   >
   >목록의 요소를 세로( **[!UICONTROL Column]** )로 표시하려면 선택한 구조 구성 요소(2, 3 또는 4열)에 따라 최대 항목 수가 제한됩니다. 구조 구성 요소 선택에 대한 자세한 내용은 [이메일 구조](../../designing/using/designing-from-scratch.md#defining-the-email-structure)편집을 참조하십시오.

### 제품 목록 채우기 {#populating-the-product-listing}

트랜잭션 이메일에 연결된 이벤트에서 오는 제품 목록을 표시하려면 아래 단계를 따르십시오.

이벤트 구성 시 컬렉션 및 관련 필드 만들기에 대한 자세한 내용은 데이터 [컬렉션](../../administration/using/configuring-transactional-messaging.md#defining-data-collections)정의를 참조하십시오.

1. 삽입한 이미지 구성 요소를 선택하고 설정 창에서 연필을 **[!UICONTROL Enable personalization]** 선택한 다음 클릭합니다.

   ![](assets/message-center_loop_image.png)

1. 열려 **[!UICONTROL Add personalization field]** 있는 **[!UICONTROL Image source URL]** 창에서 선택합니다.

   &gt; **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]** &gt; **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기 **[!UICONTROL Product list]** )를 열고 정의한 이미지 필드를 선택합니다(여기 **[!UICONTROL Product image]** ). Click **[!UICONTROL Save]**.

   ![](assets/message-center_loop_product-image.png)

   이제 선택한 개인화 필드가 설정 창에 표시됩니다.

1. 원하는 위치의 컨텍스트 도구 모음에서 **[!UICONTROL Insert personalization field]** 을 선택합니다.

   ![](assets/message-center_loop_product.png)

1. &gt; **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]** &gt; **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기 **[!UICONTROL Product list]** )를 열고 만든 필드를 선택합니다(여기 **[!UICONTROL Product name]** ). Click **[!UICONTROL Confirm]**.

   ![](assets/message-center_loop_product_node.png)

   이제 선택한 개인화 필드가 이메일 컨텐츠의 원하는 위치에 표시됩니다.

1. 가격을 삽입하려면 비슷하게 진행하십시오.
1. 일부 텍스트를 선택하고 상황에 맞는 툴바에서 **[!UICONTROL Insert link]** 선택합니다.

   ![](assets/message-center_loop_link_insert.png)

1. 열려 **[!UICONTROL Add personalization field]** 있는 **[!UICONTROL Insert link]** 창에서 선택합니다.

   &gt; **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event]** &gt; **[!UICONTROL Event context]** 노드에서 만든 컬렉션에 해당하는 노드(여기 **[!UICONTROL Product list]** )를 열고 만든 URL 필드(여기 **[!UICONTROL Product URL]** )를 선택합니다. Click **[!UICONTROL Save]**.

   >[!CAUTION]
   >
   >보안상의 이유로 올바른 정적 도메인 이름으로 시작하는 링크 내에 개인화 필드를 삽입해야 합니다.

   ![](assets/message-center_loop_link_select.png)

   이제 선택한 개인화 필드가 설정 창에 표시됩니다.

1. 제품 목록이 적용되는 구조 구성 요소를 선택하고 기본 컨텐츠를 **[!UICONTROL Show fallback]** 정의하려면 선택합니다.

   ![](assets/message-center_loop_fallback_show.png)

1. 하나 이상의 컨텐츠 구성 요소를 드래그하여 필요에 따라 편집합니다.

   ![](assets/message-center_loop_fallback.png)

   예를 들어 고객이 장바구니에 아무것도 없는 경우, 이벤트가 트리거될 때 컬렉션이 비어 있는 경우 대체 컨텐츠가 표시됩니다.

1. 설정 창에서 제품 목록의 스타일을 편집합니다. 자세한 내용은 이메일 [스타일](../../designing/using/styles.md)편집을 참조하십시오.
1. 관련 거래 이벤트에 연결된 테스트 프로필과 수집 데이터를 정의한 테스트 프로필을 사용하여 이메일을 미리 봅니다. 예를 들어 사용할 테스트 프로필의 **[!UICONTROL Event data]** 섹션에 다음 정보를 추가합니다.

   ![](assets/message-center_loop_test-profile_payload.png)

   거래 메시지에서 테스트 프로필을 정의하는 방법에 대한 자세한 내용은 [이 섹션을](#defining-a-test-profile-in-a-transactional-message)참조하십시오.

## 트랜잭션 메시지 테스트 {#testing-a-transactional-message}

트랜잭션 메시지를 저장한 후 테스트하기 위해 증거를 보낼 수 있습니다.

![](assets/message-center_10.png)

증명 보내기 단계는 증명 [보내기](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs) 섹션에 자세히 설명되어 있습니다.

## 트랜잭션 메시지 게시 {#publishing-a-transactional-message}

트랜잭션 메시지를 확인한 후 게시할 수 있습니다.

![](assets/message-center_12.png)

이제 "장바구니 포기" 이벤트가 트리거되는 즉시 수신자의 제목과 성, 장바구니 URL, 마지막으로 상담한 제품 또는 제품 목록을 정의한 경우 제품 목록, 보낼 총 장바구니 금액이 포함된 메시지가 자동으로 표시됩니다.

트랜잭션 메시지에 대한 보고서에 액세스하려면 **[!UICONTROL Reports]** 단추를 사용하십시오. 보고서를 [참조하십시오](../../reporting/using/about-dynamic-reports.md).

![](assets/message-center_13.png)

## 트랜잭션 메시지 게시 일시 중단 {#suspending-a-transactional-message-publication}

예를 들어 메시지에 포함된 데이터를 수정하는 **[!UICONTROL Pause]** 단추와 같은 방법으로 트랜잭션 메시지 게시를 일시 중지할 수 있습니다. 따라서 이벤트는 더 이상 처리되지 않고 대신 Adobe Campaign 데이터베이스의 큐에 보관됩니다.

큐에 있는 이벤트는 REST API에 정의된 기간 동안(REST API [설명서](../../api/using/about-campaign-standard-apis.md)참조) 또는 트리거 코어 서비스를 사용하는 경우 트리거 이벤트에서 보관됩니다(캠페인 및 Experience Cloud 트리거 [작업 참조](../../integrating/using/about-adobe-experience-cloud-triggers.md)).

![](assets/message-center_pause.png)

을 클릭하면 **[!UICONTROL Resume]**&#x200B;큐에 있는 모든 이벤트(만료되지 않은 경우)가 처리됩니다. 템플릿 게시가 일시 중단된 동안 수행된 모든 수정 사항이 포함되어 있습니다.

## 트랜잭션 메시지 게시 취소 {#unpublishing-a-transactional-message}

을 **[!UICONTROL Unpublish]** 클릭하면 트랜잭션 메시지 게시를 취소할 수 있지만, 이전에 만든 이벤트에 해당하는 리소스를 REST API에서 삭제하는 해당 이벤트의 게시도 취소할 수 있습니다. 이제 웹 사이트를 통해 이벤트가 트리거되더라도 해당 메시지는 더 이상 전송되지 않고 데이터베이스에 저장되지 않습니다.

![](assets/message-center_unpublish-template.png)

>[!NOTE]
>
>메시지를 다시 게시하려면 해당 이벤트 구성으로 돌아가서 게시한 다음 메시지를 게시해야 합니다. 자세한 내용은 트랜잭션 메시지 [게시를 참조하십시오](#publishing-a-transactional-message).

일시 중지된 트랜잭션 메시지의 게시를 취소하는 경우 다시 게시하기 전에 최대 24시간을 기다려야 할 수 있습니다. 이는 **[!UICONTROL Database cleanup]** 워크플로우가 대기열로 전송된 모든 이벤트를 정리하도록 하기 위한 것입니다. 메시지 일시 중지 단계는 트랜잭션 메시지 [게시](#suspending-a-transactional-message-publication) 일시 중단 섹션에 자세히 설명되어 있습니다.

매일 오전 4시에 실행되는 **[!UICONTROL Database cleanup]** 워크플로우는 **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt;를 통해 액세스할 수 있습니다 **[!UICONTROL Workflows]**.

## 트랜잭션 메시지 삭제 {#deleting-a-transactional-message}

![](assets/message-center_delete-template.png)

트랜잭션 메시지를 선택하면 이미 게시된 **[!UICONTROL Delete element]** 단추와 함께 삭제할 수 있습니다. 그러나 트랜잭션 메시지를 삭제하는 것은 특정 조건에서만 수행할 수 있습니다.

* **트랜잭션 메시지**:트랜잭션 메시지를 삭제하려면 메시지를 게시 취소하고 일시 중지하지 않아야 합니다.

   트랜잭션 메시지의 게시를 취소하면 다른 트랜잭션 메시지가 해당 이벤트에 연결되어 있지 않은 경우 트랜잭션 메시지를 성공적으로 삭제하려면 이벤트 구성의 게시를 취소해야 합니다. 트랜잭션 메시지의 게시 취소 방법에 대한 자세한 내용은 이 [섹션을](#unpublishing-a-transactional-message)참조하십시오.

   >[!CAUTION]
   >
   >이미 알림을 보낸 트랜잭션 메시지를 삭제하면 해당 전송 및 추적 로그도 삭제됩니다.

* **즉시 사용 가능한 이벤트 템플릿의 트랜잭션 메시지(내부 트랜잭션 메시지)**:내부 트랜잭션 메시지를 삭제하려면 메시지를 게시 취소하고 일시 중지하지 않아야 합니다.

   또한 이벤트에 트랜잭션 메시지만 있으면 안 됩니다. 다른 메시지는 해당 이벤트에 연결되어 있어야 합니다.

## 트랜잭션 메시지 재시도 프로세스 {#transactional-message-retry-process}

배달되지 않은 트랜잭션 메시지는 배달이 만료될 때까지 자동으로 다시 시도합니다. 배달 기간에 대한 자세한 내용은 유효 [기간 매개 변수를](../../administration/using/configuring-email-channel.md#validity-period-parameters)참조하십시오.

트랜잭션 메시지가 전송되지 않으면 두 개의 재시도 시스템이 있습니다.

* 트랜잭션 메시징 수준에서, 이벤트를 실행 배달에 할당하기 전에 트랜잭션 메시지가 실패할 수 있습니다. 이는 이벤트 수신과 배달 준비 사이의 간격입니다. 이벤트 [처리 재시도 프로세스를](#event-processing-retry-process)참조하십시오.
* 전송 프로세스 수준에서 이벤트가 실행 전달에 할당되면 임시 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. 메시지 [전송 재시도 프로세스를](#message-sending-retry-process)참조하십시오.

### 이벤트 처리 다시 시도 프로세스 {#event-processing-retry-process}

이벤트를 실행 배달에 할당할 수 없는 경우 이벤트 처리가 연기됩니다. 그런 다음 새 실행 배달에 할당될 때까지 재시도가 수행됩니다.

>[!NOTE]
>
>지연된 이벤트는 아직 실행 전달에 할당되지 않았기 때문에 트랜잭션 메시지 전송 로그에 표시되지 않습니다.

예를 들어, 컨텐츠가 올바르지 않거나, 액세스 권한 또는 브랜딩에 문제가 있거나, 유형 규칙 등을 적용할 때 오류가 발견되었기 때문에 이벤트를 실행 배달에 할당할 수 없었습니다. 이 경우 메시지를 일시 중지하고 편집하여 문제를 수정한 후 다시 게시할 수 있습니다. 그런 다음 다시 시도 시스템이 새 실행 배달에 할당합니다.

### 메시지 전송 재시도 프로세스 {#message-sending-retry-process}

이벤트가 실행 배달에 할당되면 받는 사람의 사서함이 가득 찬 경우 일시적인 오류로 인해 트랜잭션 메시지가 실패할 수 있습니다. 자세한 내용은 배달 임시 실패 [후 재시도를](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure)참조하십시오.

>[!NOTE]
>
>이벤트가 실행 전달에 할당되면 이 이벤트는 이 실행 전달의 전송 로그에 나타나며 이 시간에만 나타납니다. 실패한 배달은 트랜잭션 메시지의 **[!UICONTROL Execution list]** 탭에 표시됩니다.

### 제한 사항 {#limitations}

**로그 전송 업데이트**

재시도 프로세스에서는 새 실행 전달의 전송 로그가 즉시 업데이트되지 않습니다(업데이트는 예약된 워크플로우를 통해 수행). 즉, 트랜잭션 이벤트가 새 실행 배달에서 처리되었더라도 메시지가 **[!UICONTROL Pending]** 상태에 있을 수 있습니다.

**배달 실패**

실행 배달을 중지할 수 없습니다. 그러나 현재 실행 배달이 실패하면 새 이벤트가 수신되는 즉시 새 이벤트가 만들어지고 모든 새 이벤트가 이 새 실행 배달로 처리됩니다. 실패한 실행 전달에 의해 새 이벤트가 처리되지 않습니다.

실행 배달에 이미 할당된 일부 이벤트가 연기된 경우 해당 실행 배달에 실패하면 다시 시도 시스템에서 연기된 이벤트를 새 실행 배달에 할당하지 않으므로 이러한 이벤트가 손실됩니다.
