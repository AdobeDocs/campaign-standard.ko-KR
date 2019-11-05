---
title: 메시지 추적
description: 전달 받는 사람의 동작을 추적하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: 전송 및 추적 메시지
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 메시지 추적{#tracking-messages}

## 추적 정보 {#about-tracking}

추적 기능 덕분에 Adobe Campaign을 사용하면 게재 받는 사람의 동작을 추적할 수 있습니다. 이를 위해 Adobe Campaign은 세션 쿠키와 영구 쿠키를 사용합니다.

쿠키의 사용을 승인하는 확인란을 사용하여 승인 요청(예: 페이지 위로 올라오기)을 통해 사이트가 웹 추적 툴을 갖추고 있음을 사용자에게 알리거나, 쿠키가 첫번째로 방문한 페이지의 상단에 배너를 추가하는 등의 작업을 할 수 있습니다. 팝업 창은 브라우저에 의해 종종 차단되므로 사용하지 않아야 합니다.

Adobe Campaign에서는 두 가지 유형의 쿠키를 사용합니다.

* 세션 쿠키(nlid). 여기에는 연락처로 보낸 이메일의 식별자(broadlogId)와 메시지 템플릿의 식별자(deliveryId)가 포함됩니다. Adobe Campaign에서 보낸 이메일에 포함된 URL을 클릭하면 방문자가 추가되며, 이를 통해 웹에서 해당 행동을 추적할 수 있습니다. 브라우저를 닫으면 이 세션 쿠키가 자동으로 지워집니다. 연락처는 브라우저가 쿠키를 거부하도록 구성할 수 있습니다.
* Adobe Experience Cloud 솔루션 간에 공유된 쿠키입니다. 따라서 웹 사이트를 방문할 때 Experience Cloud 솔루션과 상호 작용하는 사용자를 식별할 수 있습니다. 이 쿠키에 대한 설명은 다음 링크를 참조하십시오.https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html [](https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html).

추적 정보는 데이터베이스의 각 연락처에서 사용할 수 **[!UICONTROL integrated customer profiles]**&#x200B;있습니다. For more on this, refer to [this section](../../audiences/using/integrated-customer-profile.md).

## 추적 로그 {#tracking-logs}

이 **[!UICONTROL Tracking logs]** 탭에는 이 게재의 추적 내역이 나열됩니다. 이 탭에는 Adobe Campaign에서 추적한 모든 URL과 같은 보낸 메시지에 대한 추적 정보가 표시됩니다. 이 탭의 추적 정보는 10분마다 업데이트됩니다.

>[!NOTE]
>
>게재에 대한 추적을 사용할 수 없는 경우 이 탭이 표시되지 않습니다. 추적 로그는 **이메일** 및 **푸시 알림** 채널에만 사용할 수 있습니다.

![](assets/tracking_logs.png)

위의 예에서 수신자는 다음과 같습니다.

* 메시지를 열었습니다.
* "자세한 내용" 사용자 지정 링크를 클릭합니다.
* 구독 취소 및 미러 페이지 링크를 클릭합니다.

열에서 가능한 값은 다음과 **[!UICONTROL Type]** 같습니다.

* **[!UICONTROL Email click]**:수신자가 사용자 지정 링크를 클릭했습니다.
* **[!UICONTROL Mirror page]**:수신자가 미러 페이지에 대한 링크를 클릭했습니다.
* **[!UICONTROL Open]**:수신자가 이메일을 열었습니다.
* **[!UICONTROL Opt-out]**:수신자가 구독 취소 링크를 클릭했습니다.

>[!NOTE]
>
>푸시 알림 **** 채널의 경우 모바일 알림에 대한 클릭만 추적됩니다. 이 경우 값이 **[!UICONTROL Click on mobile notification]**&#x200B;됩니다.

추적 링크를 삽입하는 방법에 대한 자세한 내용은 [이 페이지를](../../designing/using/links.md#inserting-a-link)참조하십시오.

## 추적된 URL {#tracked-urls}

이 **[!UICONTROL Tracked URLs]** 탭은 URL 유형 및 소스 URL을 비롯하여 보낸 메시지에 포함된 URL을 다시 그룹화합니다.

![](assets/sending_delivery6.png)

For more on tracking links, refer to [this section](../../designing/using/links.md#about-tracked-urls).
