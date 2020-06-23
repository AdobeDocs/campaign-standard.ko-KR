---
title: 메시지 추적
description: 전달 받는 사람의 동작을 추적하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f7adb7a4725129727010c2486ca34bbc2021c539
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 3%

---


# 메시지 추적{#tracking-messages}

## 추적 정보 {#about-tracking}

추적 기능 덕분에 Adobe Campaign을 통해 전달 받는 사람의 동작을 추적할 수 있습니다. 이를 위해 Adobe Campaign은 세션 쿠키와 영구 쿠키를 사용합니다.

쿠키의 사용을 승인하는 확인란을 사용하여 사이트에 권한 부여 요청을 통해(예: 페이지에 위로 표시됨) 웹 추적 도구가 설치되어 있는지 사용자에게 알리거나, 첫 번째 페이지에 배너를 추가하는 등의 작업을 할 수 있습니다. 팝업 창은 브라우저에 의해 종종 차단되므로 사용하지 않아야 합니다.

추적 정보는 데이터베이스의 각 연락처에서 사용할 수 있습니다 **[!UICONTROL integrated customer profiles]**. 이 작업에 대한 자세한 정보는 [이 섹션](../../audiences/using/integrated-customer-profile.md)을 참조하십시오.

Adobe Campaign은 두 가지 유형의 쿠키를 사용합니다.

* 세션 쿠키(기본). 여기에는 연락처로 보낸 이메일의 식별자(broadlogId)와 메시지 템플릿의 식별자(deliveryId)가 포함됩니다. 이 URL은 연락처가 Adobe Campaign이 보낸 이메일에 포함된 URL을 클릭할 때 추가되며, 이를 통해 웹에서 해당 동작을 추적할 수 있습니다. 브라우저를 닫으면 이 세션 쿠키가 자동으로 지워집니다. 연락처는 브라우저가 쿠키를 거부하도록 구성할 수 있습니다.
* Adobe Experience Cloud 솔루션 간에 공유되는 쿠키 따라서 웹 사이트를 방문할 때 Experience Cloud 솔루션과 상호 작용하는 사용자를 식별할 수 있습니다. 이 쿠키에 대한 설명은 [여기에서 확인할 수 있습니다](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-mc.html).

Adobe Campaign Standard을 사용하여 추적하면 다음 기능에 액세스할 수 있습니다.

<table>
<tr>
    <td valign="top">
        <a href="../../administration/using/configuring-email-channel.md#tracking-parameters"><img width="60px" alt="조건" src="assets/icon_email_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="https://helpx.adobe.com/campaign/kb/push-tracking.html"><img width="60px" alt="조건" src="assets/icon_push_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="../../designing/using/links.md#about-tracked-urls"><img width="60px" alt="조건" src="assets/icon_url.png"/></a>
    </td>
        <td valign="top">
          <a href="../../sending/using/tracking-messages.md#tracking-logs"><img width="60px" alt="조건" src="assets/icon_log.png"/></a>
    </td>
    </td>
    <td valign="top">
          <a href="../../reporting/using/tracking-indicators.md"><img width="60px" alt="조건" src="assets/icon_report.png"/></a>
</tr>
<tr>
<td>이메일 추적</td>
<td>푸시 추적</td>
<td>추적된 URL</td>
<td>추적 로그</td>
<td>추적 보고서</td>
</tr>
</table>

## Tracking logs {#tracking-logs}

이 게재의 추적 내역이 **[!UICONTROL Tracking logs]** 탭에 나열됩니다. 이 탭에는 Adobe Campaign에 의해 추적된 모든 URL과 같이 전송된 메시지에 대한 추적 정보가 표시됩니다. 이 탭의 추적 정보는 10분마다 업데이트됩니다.

>[!NOTE]
>
>게재에 대한 추적이 활성화되지 않으면 이 탭이 표시되지 않습니다. 추적 로그는 **이메일** 및 **푸시 알림** 채널에만 사용할 수 있습니다.

![](assets/tracking_logs.png)

위의 예에서 수신자는

* 메시지를 열었습니다.
* &quot;자세한 내용&quot; 사용자 지정 링크를 클릭합니다.
* 구독 취소 및 미러 페이지 링크를 클릭합니다.

열에서 가능한 **[!UICONTROL Type]** 값은 다음과 같습니다.

* **[!UICONTROL Email click]**: 수신자가 사용자 지정 링크를 클릭했습니다.
* **[!UICONTROL Mirror page]**: 수신자가 미러 페이지에 대한 링크를 클릭했습니다.
* **[!UICONTROL Open]**: 수신자가 이메일을 열었습니다.
* **[!UICONTROL Opt-out]**: 수신자가 구독 취소 링크를 클릭했습니다.

>[!NOTE]
>
>푸시 **알림** 채널의 경우 모바일 알림에 대한 클릭만 추적됩니다. 이 경우 값이 됩니다 **[!UICONTROL Click on mobile notification]**.

추적 링크를 삽입하는 방법에 대한 자세한 내용은 [이 페이지를 참조하십시오](../../designing/using/links.md#inserting-a-link).

## 추적된 URL {#tracked-urls}

이 **[!UICONTROL Tracked URLs]** 탭은 URL 유형 및 소스 URL을 포함하여 보낸 메시지에 포함된 URL을 다시 그룹화합니다.

![](assets/sending_delivery6.png)

For more on tracking links, refer to [this section](../../designing/using/links.md#about-tracked-urls).
