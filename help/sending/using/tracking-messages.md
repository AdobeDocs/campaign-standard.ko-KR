---
title: 추적 메시지
seo-title: 추적 메시지
description: 추적 메시지
seo-description: 전달 수신자의 행동을 추적하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: C 3721647-0663-4614-A 9 C 9-3 B 3 A 40 AF 328 A
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: 전송 및 추적 메시지
discoiquuid: 6 fa 50 f 0 d -3 dcf -4 a 9 e-bccc -1 ecda 2 bfb 449
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Tracking messages{#tracking-messages}

## About tracking {#about-tracking}

Adobe Campaign의 추적 기능 덕분에 배달 수신자의 행동을 추적할 수 있습니다. 이렇게 하려면 Adobe Campaign에서 세션 쿠키 및 영구 쿠키를 사용합니다.

쿠키의 사용을 승인하는 확인란을 선택하거나, 사용자가 도착하는 첫 번째 페이지의 맨 위에 배너를 추가하는 등의 인증 요청 (예: 페이지 위로 가져옴) 를 통해 사이트에 웹 추적 도구가 포함되어 있음을 사용자에게 알릴 수 있습니다. 팝업 창은 브라우저에 의해 차단되는 경우가 많기 때문에 피해야 합니다.

Adobe Campaign 에서는 두 가지 유형의 쿠키를 사용합니다.

* 세션 쿠키 (nlid). 여기에는 연락처 (Broadlogid) 에 보낸 이메일의 식별자 및 메시지 템플릿 (deliveryid) 의 식별자가 포함됩니다. 담당자가 Adobe Campaign에서 보낸 이메일에 포함된 URL를 클릭하고 웹에서 해당 행동을 추적할 때 추가됩니다. 이 세션 쿠키는 브라우저를 닫으면 자동으로 지워집니다. 담당자는 쿠키를 거부하도록 브라우저를 구성할 수 있습니다.
* Adobe Experience Cloud 솔루션 간에 공유되는 쿠키입니다. 따라서 웹 사이트를 방문할 때 Experience Cloud 솔루션과 상호 작용하는 사용자를 식별할 수 있습니다. The description of this cookie is available here: [https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html](https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_mc.html).

Tracking information are available for each contact of your database into **[!UICONTROL integrated customer profiles]**. For more on this, refer to [this section](../../audiences/using/integrated-customer-profile.md).

## Tracking logs {#tracking-logs}

**[!UICONTROL Tracking logs]** 탭에 이 게시에 대한 추적 내역이 나열됩니다. 이 탭에는 Adobe Campaign에서 추적된 모든 URL와 같이 전송된 메시지에 대한 추적 정보가 표시됩니다. 이 탭의 추적 정보는 10 분마다 업데이트됩니다.

>[!NOTE]
>
>게시에 대해 추적이 활성화되지 않은 경우 이 탭이 표시되지 않습니다. Tracking logs are available for the **email** and **push notification** channels only.

![](assets/tracking_logs.png)

위의 예에서 받는 사람은 다음과 같습니다.

* 메시지를 열었습니다.
* " 자세한 정보 "사용자 지정 링크를 클릭합니다.
* 가입 취소 및 미러 페이지 링크를 클릭합니다.

**[!UICONTROL Type]** 열에서 가능한 값은 다음과 같습니다.

* **[!UICONTROL Email click]**: 받는 사람이 사용자 지정 링크를 클릭했습니다.
* **[!UICONTROL Mirror page]**: 받는 사람이 미러 페이지에 대한 링크를 클릭했습니다.
* **[!UICONTROL Open]**: 수신자가 이메일을 열었습니다.
* **[!UICONTROL Opt-out]**: 받는 사람이 구독 취소 링크를 클릭했습니다.

>[!NOTE]
>
>**푸시 알림** 채널의 경우 모바일 알림의 클릭만 추적됩니다. **[!UICONTROL Click on mobile notification]**&#x200B;이 경우 값이 됩니다.

For more on how to insert tracking links, refer to [this page](../../designing/using/inserting-a-link.md).

## Tracked URLs {#tracked-urls}

**[!UICONTROL Tracked URLs]** 탭은 URL 유형 및 소스 URL를 포함하여 전송된 메시지에 포함된 URL를 재그룹화합니다.

![](assets/sending_delivery6.png)

For more on tracking links, refer to [this section](../../designing/using/about-tracked-urls.md).
