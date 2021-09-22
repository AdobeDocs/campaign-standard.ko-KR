---
title: Campaign Standard Mobile 안내서
description: 모바일 애플리케이션을 구성하거나 푸시 알림 및 인앱 메시지를 만드는 방법 등 Adobe Campaign Standard에서 모바일 게재에 대한 일반 지침에 대해 자세히 알아보십시오.
audience: channels
content-type: reference
topic-tags: mobile-guide
feature: Overview
role: User
level: Beginner
hidefromtoc: true
source-git-commit: 34270a2caff0932b56d00ccf721bdba87eb61f81
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 23%

---

# 모바일 채널 시작 {#mobile-guide}

<table style="table-layout:fixed">
<tr>
<td><img src="assets/do-not-localize/config_push.png" width="60px"><p>푸시 알림에 대해 모바일 애플리케이션을 구성하는 방법 알아보기 </br><a href="#configuration-push">여기</a>를 클릭하십시오.</p></td>
<td><img src="assets/do-not-localize/config_inapp.png" width="60px"><p>인앱 메시지에 대해 모바일 애플리케이션을 구성하는 방법을 알아봅니다 </br><a href="#configuring-mobile-app">여기</a>를 클릭하십시오.</p></td>
</tr>
<tr>
<td><img src="assets/do-not-localize/push2.png" width="60px"><p>푸시 알림을 만드는 방법에 대해 자세히 알아보기 </br><a href="#create-push">여기</a>를 클릭하십시오.</p></td>
<td><img src="assets/do-not-localize/inapp.png" width="60px"><p>인앱 메시지를 만드는 방법 알아보기</br><a href="#create-inapp">여기</a>를 클릭하십시오.</p></td></tr>
</table>

## 모바일 게재 기본 정보 {#about-mobile}

Adobe Campaign을 사용하면 다양한 채널에서 개인화된 메시지를 만들고 전송할 수 있으며, 전용 보고서를 통해 그 효과를 측정할 수 있습니다.

Adobe Campaign Standard을 사용하면 세 개의 서로 다른 채널을 통해 모바일 게재를 보낼 수 있습니다.

* SMS 메시지 정보 섹션에 나와 있는 SMS.
* 푸시 알림 기본 정보 섹션에 나와 있는 푸시 알림.
* 인앱 메시지 정보 섹션에 있는 인앱 메시지.

## 푸시 알림에 대한 모바일 애플리케이션 구성 {#configuration-push}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Adobe Experience Platform SDK를 사용한 모바일 애플리케이션 구성</strong></p>
    </div>
    <p>인앱 메시지 및 푸시 알림을 전송하려면 Adobe Experience Platform SDK를 활용하여 Adobe Campaign에서 모바일 애플리케이션을 설정해야 합니다.자세한 정보를 보려면 </br><a href="../../administration/using/configuring-a-mobile-application.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Campaign Standard 푸시 알림 페이로드 구조 이해</strong></p>
    </div>
    <p>푸시 알림이 Adobe Campaign Standard에서 앱으로 성공적으로 전송될 때 모바일 애플리케이션에서 받는 페이로드 구조에 대해 자세히 알아보십시오.자세한 정보를 보려면 </br><a href="../../administration/using/push-payload.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>로컬 알림 추적 구현</strong></p>
    </div>
    <p>로컬 알림 추적이 올바로 구현되었는지 확인하는 방법을 여기에서 알아봅니다. 자세한 정보를 보려면 </br><a href="../../administration/using/local-tracking.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>푸시 추적 구현</strong></p>
    </div>
    <p>iOS 및 Android에서 푸시 알림 추적이 올바르게 구현되었는지 확인하는 방법을 알아봅니다.자세한 정보를 보려면 </br><a href="../../administration/using/push-tracking.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
</table>

## 인앱 메시지에 대한 모바일 애플리케이션 구성 {#configuring-mobile-app}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Adobe Experience Platform SDK를 사용한 모바일 애플리케이션 구성</strong></p>
    </div>
    <p>인앱 메시지 및 푸시 알림을 전송하려면 Adobe Experience Platform SDK를 활용하여 Adobe Campaign에서 모바일 애플리케이션을 설정해야 합니다.자세한 정보를 보려면 </br><a href="../../administration/using/configuring-a-mobile-application.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Adobe Experience Platform SDK를 사용하여 지원되는 모바일 사용 사례</strong></p>
    </div>
    <p>Adobe Experience Platform SDK를 사용하여 Adobe Campaign Standard에서 지원되는 모바일 사용 사례에 대해 자세히 알아보십시오.자세한 정보를 보려면 </br><a href="../../administration/using/supported-mobile-use-cases.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Adobe Campaign Standard 사용 사례를 지원하기 위한 Adobe Experience Platform Launch 규칙 구성</strong></p>
    </div>
    <p><a href="../../administration/using/configuring-rules-launch.md"><strong>을(를) </strong></a> 클릭하여 Adobe Experience Platform Launch에서 데이터 요소 및 규칙 만들기를 시작하여 모바일 애플리케이션에서 Adobe Campaign Standard으로 PII 및 기타 데이터를 전송합니다.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>로컬 알림 추적 구현</strong></p>
    </div>
    <p>로컬 알림 추적이 올바로 구현되었는지 확인하는 방법을 여기에서 알아봅니다. 자세한 정보를 보려면 </br><a href="../../administration/using/local-tracking.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
</table>

## 푸시 알림 만들기 {#create-push}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>푸시 알림 준비 및 보내기</strong></p>
    </div>
    <p><a href="../../channels/using/preparing-and-sending-a-push-notification.md"><strong>푸시 </strong></a> 알림을 준비한 다음 타겟팅된 대상자에게 보내는 방법을 알아봅니다.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>푸시 알림 사용자 정의</strong></p>
    </div>
    <p>게재를 세밀하게 조정하기 위해 Adobe Campaign에서 푸시 알림을 디자인하는 동안 옵션 세트에 액세스할 수 있습니다.자세한 정보를 보려면 </br><a href="../../channels/using/customizing-a-push-notification.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>다국어 푸시 알림 만들기</strong></p>
    </div>
    <p>사용자의 선호 언어 및 지역에 따라 메시지를 전송하여 푸시 알림 콘텐츠를 개인화할 수 있습니다.자세한 정보를 보려면 </br><a href="../../channels/using/creating-a-multilingual-push-notification.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Adobe Campaign Standard 푸시 알림의 이미지 표시</strong></p>
    </div>
    <p><a href="../../administration/using/image-push-notification.md"><strong>iOS </strong></a> 장치에서 Adobe Campaign 푸시 알림의 이미지를 표시하는 방법을 알아봅니다.</p>
    <br>
  </td>
</tr>
</table>

## 인앱 메시지 만들기 {#create-inapp}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>인앱 메시지 준비 및 보내기</strong></p>
    </div>
    <p><a href="../../channels/using/preparing-and-sending-an-in-app-message.md"><strong></strong></a> 여기서 인앱 메시지를 준비하여 타겟팅된 대상자에게 보내는 방법을 알아봅니다.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>인앱 메시지 사용자 지정</strong></p>
    </div>
    <p>게재를 세밀하게 조정하기 위해 Adobe Campaign에서 인앱을 디자인하는 동안 고급 옵션 세트에 액세스할 수 있습니다.자세한 정보를 보려면 </br><a href="../../channels/using/customizing-an-in-app-message.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>로컬 알림 메시지 유형 사용자 지정</strong></p>
    </div>
    <p>로컬 알림은 특정 시간과 이벤트에 따라 앱에 의해서만 트리거할 수 있습니다. 자세한 정보를 보려면 </br><a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>인앱 보고서</strong></p>
    </div>
    <p>인앱 보고서는 인앱 게재와 관련된 세부 사항을 제공합니다.자세한 정보를 보려면 </br><a href="../../reporting/using/in-app-report.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
</table>

## SMS 메시지 만들기 {#create-sms}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>SMS 메시지 만들기</strong></p>
    </div>
    <p>SMS 게재를 만드는 것은 일반 이메일을 만드는 것과 매우 유사합니다. </br>이  <a href="../../channels/using/creating-an-sms-message.md"><strong>단계</strong></a> 에 대해서는 이 채널과 관련된 구성을 설명합니다.</br></p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>SMS 메시지 사용자 지정
</strong></p>
    </div>
    <p>게재를 세밀하게 조정하기 위해 Adobe Campaign에서 SMS 메시지를 디자인하는 동안 고급 옵션 세트에 액세스할 수 있습니다.자세한 정보를 보려면 </br><a href="../../channels/using/sms-and-push-content-editor-interface.md"><strong>여기를 클릭하십시오.</br><a href="../../channels/using/sms-and-push-content-editor-interface.md"><strong></p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>수신 SMS 관리</strong></p>
    </div>
    <p>Campaign을 통해 보낸 SMS 메시지에 프로필이 답장할 경우 수행할 작업과 자동으로 다시 보낼 메시지를 구성할 수 있습니다.로컬 알림 메시지 유형 사용자 지정</br><a href="../../channels/using/managing-incoming-sms.md"><strong>자세한 내용을 보려면 여기를 클릭하십시오.</br><a href="../../channels/using/managing-incoming-sms.md"><strong></p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>SMS 보고서</strong></p>
    </div>
    <p>SMS 보고서는 배달된 비율 및 바운스 비율 등 SMS 게재에 대한 세부 사항을 제공합니다.자세한 정보를 보려면 </br><a href="../../reporting/using/sms-report.md"><strong>여기를 클릭</strong></a>하십시오.</p>
    <br>
  </td>
</tr>
</table>

## 모바일 문제 해결 {#mobile-troubleshooting}

다음 페이지는 Adobe Campaign Classic에서 모바일 게재를 사용할 때 발생하는 가장 일반적인 문제를 해결하는 데 도움이 됩니다.

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>푸시 알림 FAQ</strong></p>
    </div>
    <p><a href="../../channels/using/about-push-notifications.md#push-faq"><strong>자세한 정보를 보려면 여기를 클릭하십시오.</p>
  </td>
  <td>
    <div>
    <p><strong>Adobe 실행 동기화 FAQ</strong></p>
    </div>
    <p><a href="../../channels/using/in-app-faq.md"><strong>자세한 정보를 보려면 여기를 클릭하십시오.</p>
  </td>
  <td>
    <div>
    <p><strong>인앱 FAQ</strong></p>
    </div>
    <p><a href="../../administration/using/syncwithlaunch-faq.md"><strong>자세한 정보를 보려면 여기를 클릭하십시오.</p>
  </td>
</tr>
</table>


