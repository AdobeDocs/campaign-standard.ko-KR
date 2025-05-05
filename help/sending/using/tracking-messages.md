---
title: 메시지 추적
description: 게재 수신자의 동작을 추적하는 방법에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
feature: Performance Monitoring
role: User
level: Intermediate
exl-id: fac29bc2-57fa-40f9-a160-cd75f695b91e
source-git-commit: affd4f9716235a283df20de5539e43c4832762f7
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 23%

---

# 메시지 추적{#tracking-messages}

## 추적 기본 정보 {#about-tracking}

추적 기능 덕분에 Adobe Campaign을 사용하면 게재 수신자의 동작을 추적할 수 있습니다. 이를 위해 Adobe Campaign은 세션 쿠키와 영구 쿠키를 사용합니다.

쿠키의 사용을 승인하는 확인란이 포함된 권한 부여 요청(예: 페이지 위로 올라오는 요청)을 통해 사이트가 웹 추적 도구를 갖추고 있음을 사용자에게 알리거나, 첫 번째 랜딩 페이지 등에 배너를 추가할 수 있습니다. 팝업 창은 브라우저에 의해 종종 차단되므로 사용하지 않아야 합니다.

**[!UICONTROL integrated customer profiles]**&#x200B;에 있는 데이터베이스의 각 연락처에 대해 추적 정보를 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../audiences/using/integrated-customer-profile.md)을 참조하십시오.

Adobe Campaign은 다음 두 가지 유형의 쿠키를 사용합니다.

* 세션 쿠키(nlid). 여기에는 연락처로 보낸 전자 메일의 식별자(broadlogId)와 메시지 템플릿의 식별자(deliveryId)가 포함됩니다. 이 URL은 연락처가 Adobe Campaign이 보낸 전자 메일에 포함된 URL을 클릭할 때 추가되며, 이를 통해 웹에서 해당 동작을 추적할 수 있습니다. 브라우저를 닫으면 이 세션 쿠키가 자동으로 지워집니다. 연락처는 브라우저가 쿠키를 거부하도록 구성할 수 있습니다.
* Adobe Experience Cloud 솔루션 간에 공유되는 쿠키입니다. 이렇게 하면 웹 사이트를 방문할 때 Experience Cloud 솔루션과 상호 작용하는 사용자를 식별할 수 있습니다. 이 쿠키의 설명은 [여기](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-mc.html?lang=ko)에서 사용할 수 있습니다.

Adobe Campaign Standard을 사용하여 추적하면 다음 기능에 액세스할 수 있습니다.

<table>
<tr>
    <td valign="top">
        <a href="../../administration/using/configuring-email-channel.md#tracking-parameters"><img width="60px" alt="조건" src="assets/icon_email_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="../../administration/using/push-tracking.md"><img width="60px" alt="조건" src="assets/icon_push_parameters.png"/></a>
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

## 추적 로그 {#tracking-logs}

**[!UICONTROL Tracking logs]** 탭에 이 게재의 추적 기록이 나열됩니다. 이 탭에는 Adobe Campaign에서 추적한 모든 URL과 같은 보낸 메시지에 대한 추적 정보가 표시됩니다. 이 탭의 추적 정보는 10분마다 업데이트됩니다.

>[!NOTE]
>
>게재에 대해 추적이 활성화되지 않은 경우 이 탭이 표시되지 않습니다. 추적 로그는 **전자 메일** 및 **푸시 알림** 채널에서만 사용할 수 있습니다.

![](assets/tracking_logs.png)

위의 예에서 수신자는

* 메시지를 열었습니다.
* 미러 페이지 링크를 클릭했습니다.
* &quot;자세히 알아보기&quot; 사용자 지정 링크를 클릭합니다.

**[!UICONTROL Type]** 열에서 가능한 값은 다음과 같습니다.

* **[!UICONTROL Email click]**: 수신자가 사용자 지정 링크를 클릭했습니다.
* **[!UICONTROL Mirror page]**: 받는 사람이 미러 페이지 링크를 클릭했습니다.
* **[!UICONTROL Open]**: 받는 사람이 전자 메일을 열었습니다.
* **[!UICONTROL Opt-out]**: 수신자가 구독 취소 링크를 클릭했습니다.

>[!NOTE]
>
>**푸시 알림** 채널의 경우 모바일 알림에 대한 클릭만 추적됩니다. 이 경우 값은 **[!UICONTROL Click on mobile notification]**&#x200B;이(가) 됩니다.

추적 링크를 삽입하는 방법에 대한 자세한 내용은 [이 페이지](../../designing/using/links.md#inserting-a-link)를 참조하세요.

**[!UICONTROL Tracking indicators]** 보고서에는 전자 메일 메시지를 받은 후 추적 동작에 대한 주요 지표가 포함되어 있습니다. 자세한 정보는 이 [페이지](../../reporting/using/tracking-indicators.md)를 참조하십시오.

## 추적된 URL {#tracked-urls}

**[!UICONTROL Tracked URLs]** 탭은 보낸 메시지의 URL 유형 및 소스 URL을 포함하여 보낸 메시지에 포함된 URL을 다시 그룹화합니다.

![](assets/sending_delivery6.png)

링크 추적에 대한 자세한 정보는 [이 섹션](../../designing/using/links.md#about-tracked-urls)을 참조하세요.
