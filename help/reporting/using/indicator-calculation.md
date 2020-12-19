---
solution: Campaign Standard
product: campaign
title: 지표 계산
description: 모든 지표의 공식 목록을 사용하여 보고서 결과를 이해합니다.
audience: reporting
content-type: reference
topic-tags: about-reporting
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 2%

---


# 지표 계산{#indicator-calculation}

>[!NOTE]
>
>높은 볼륨 및 실시간 분석을 보다 효과적으로 처리하고 관리하기 위해 Dynamic Reporting은 정확한 계산 예상치를 위해 대략적인 집계 결과를 사용합니다. 대략적인 집계는 제한적인 메모리 사용을 제공하며 종종 정확한 계산보다 빠릅니다.

아래 표에는 배달 유형에 따라 다른 보고서에 사용된 지표 목록과 계산 공식이 나와 있습니다.

## 이메일 게재 {#email-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>레이블</strong> <br /> </th> 
   <th> <strong>필드 이름</strong> <br /> </th> 
   <th> <strong>표시기 계산 공식</strong> <br /> </th> 
   <th> <strong>댓글</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 계정 비활성화<br /> </td> 
   <td> @disabled<br /> </td> 
   <td> count(@failureReason=4)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 차단 목록<br /> </td> 
   <td> @blacklisted<br /> </td> 
   <td> count(@failureReason=8, @failureType=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 차단 목록 비율<br /> </td> 
   <td> @rateBlacklisted<br /> </td> 
   <td> @blacklisted/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류<br /> </td> 
   <td> @bounces<br /> </td> 
   <td> count(@status=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> @rateBounces<br /> </td> 
   <td> @bounces/@sent<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> @clicks<br /> </td> 
   <td> count(@trackingUrlType=1 또는 10 또는 11)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> @clickthrough<br /> </td> 
   <td> @uniqueclicks/@delivered<br /> </td> 
   <td> 비율 계산의 분모는 [배달됨]만 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> count(@status=1)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 배달 비율<br /> </td> 
   <td> @rateDelivered<br /> </td> 
   <td> @delivered/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스<br /> </td> 
   <td> @hardBounces<br /> </td> 
   <td> count(@failureType=2 AND @failureReason=8)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스 비율<br /> </td> 
   <td> @rateHardBounces<br /> </td> 
   <td> @hardBounces/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 잘못된 도메인<br /> </td> 
   <td> @invalidDomain<br /> </td> 
   <td> count(@failureReason=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 사서함 전체<br /> </td> 
   <td> @mailBoxFull<br /> </td> 
   <td> count(@failureReason=5)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지<br /> </td> 
   <td> @mirrorPage<br /> </td> 
   <td> count(@trackingUrlType=6)<br /> </td> 
   <td> 비율 계산의 분모는 [배달됨]만 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지 속도<br /> </td> 
   <td> @rateMirrorPage<br /> </td> 
   <td> @mirrorPage/@delivered<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 연결되지 않음<br /> </td> 
   <td> @notConnected<br /> </td> 
   <td> count(@failureReason=6)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> @uniqueOpens<br /> </td> 
   <td> count(@trackingUrlType=2 + unique(@trackingUrlType=1,2,3,6,10,11) - unique(@trackingUrlType=2))<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 열기 속도<br /> </td> 
   <td> @rateOpens<br /> </td> 
   <td> @opens/@delivered<br /> </td> 
   <td> 비율 계산의 분모는 [배달됨]만 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리<br /> </td> 
   <td> @quarantine<br /> </td> 
   <td> isQuarantine=true<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 격리 비율<br /> </td> 
   <td> @rateQuarantine<br /> </td> 
   <td> @quarantine/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr>
  <tr> 
   <td> 거부됨<br /> </td> 
   <td> @rejected<br /> </td> 
   <td> count(@failureReason=20, @failureType=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 거부된 속도<br /> </td> 
   <td> @rateRejected<br /> </td> 
   <td> @rejected/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @delivered + @bounces<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스<br /> </td> 
   <td> @softBounces<br /> </td> 
   <td> count(@failureType=1)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스 비율<br /> </td> 
   <td> @rateSoftBounces<br /> </td> 
   <td> @softBounces/@sent<br /> </td> 
   <td> 비율 계산의 분모는 전송 횟수(배달됨 + 바운스 수)를 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> @uniqueclicks<br /> </td> 
   <td> ThetaSketch 개념을 사용하여 고유 클릭 수를 계산합니다. 자세한 내용은 이 <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">예</a>.<br />를 참조하십시오. </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> @uniqueopens<br /> </td> 
   <td> unique(@trackingUrlType=1,2,3,6,10,11)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 연결할 수 없습니다. <br /> </td> 
   <td> @unreachable<br /> </td> 
   <td> count(@failureReason=3)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소<br /> </td> 
   <td> @unsubscribes<br /> </td> 
   <td> count(@trackingUrlType=3)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소 비율<br /> </td> 
   <td> @rateUnsubscribes<br /> </td> 
   <td> @unsubscribes/@delivered<br /> </td> 
   <td> 비율 계산의 분모는 [배달됨]만 기반으로 합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 사용자 알 수 없음<br /> </td> 
   <td> @unknownUser<br /> </td> 
   <td> count(@failureReason=1)<br /> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

## 푸시 알림 게재 {#push-notification-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>레이블</strong> <br /> </th> 
   <th> <strong>필드 이름</strong> <br /> </th> 
   <th> <strong>표시기 계산 공식</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @count(status=sent)<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 비율<br /> </td> 
   <td> @rateDelivered<br /> </td> 
   <td> (@delivered/@sent)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> @rateBounces<br /> </td> 
   <td> (@delivered/@sent)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> @opens<br /> </td> 
   <td> @count(status=open)<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기 속도<br /> </td> 
   <td> @rateOpens<br /> </td> 
   <td> (@opens/@delivered)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> @uniqueopens<br /> </td> 
   <td> 고유 열기 횟수는 고유한 RecipientIds의 ThetaSketch 개념을 사용하여 계산됩니다. 자세한 내용은 이 <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">예</a>.<br />를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> @impressions<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> @uniqueimpressions<br /> </td> 
   <td> @unique(@count(status=view)<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> @clicks<br /> </td> 
   <td> @count(status=interact)<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> @uniqueclicks<br /> </td> 
   <td> ThetaSketch 개념을 사용하여 고유 클릭 수를 계산합니다. 자세한 내용은 이 <a href="https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">예</a>.<br />를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> @clickthrough<br /> </td> 
   <td> (@interact/@delivered)*100<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 인앱 게재 {#in-app-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>레이블</strong> <br /> </th> 
   <th> <strong>필드 이름</strong> <br /> </th> 
   <th> <strong>표시기 계산 공식</strong> <br /> </th> 
   <th> <strong>댓글</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @count(status=sent)<br /> </td> 
   <td> sent=delivered<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
   <td> deliver=sent<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> @impressions<br /> </td> 
   <td> @count(status=view) 또는 @count(status=button 1 클릭 + 단추 2 클릭 + 무시)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> @uniqueimpressions<br /> </td> 
   <td> @unique(@count(status=view)<br /> </td> 
   <td> 캠페인 프로필(inAppProfile)</span> 템플릿을 기반으로 한 <span class="uicontrol">Target 사용자의 경우 사용자 = 수신자 ID입니다.<br /> 모바일 앱(inAppBroadcast)의 모든 사용자 <span class="uicontrol">와 모바일 프로파일(inApp) 템플릿을 기반으로 한 </span> Target 사용자를 Target <span class="uicontrol">의 경우 사용자, 모바일 앱 및 디바이스의 고유한 조합을 나타내는 사용자 = MC Id 또는 동등</span> 이 됩니다.<br /> </span></td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭 <br /> </td> 
   <td> @inappclicks<br /> </td> 
   <td> @count (status=click)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 고유 인앱 클릭<br /> </td> 
   <td> @uniqueinapp<br /> </td> 
   <td> @unique(@count (status=clicks)<br /> </td> 
   <td> 캠페인 프로필(inAppProfile)</span> 템플릿을 기반으로 한 <span class="uicontrol">Target 사용자의 경우 사용자 = 수신자 ID입니다.<br /> 모바일 앱(inAppBroadcast)의 모든 사용자 <span class="uicontrol">와 모바일 프로파일(inApp) 템플릿을 기반으로 한 </span> Target 사용자를 Target <span class="uicontrol">의 경우 사용자, 모바일 앱 및 디바이스의 고유한 조합을 나타내는 사용자 = MC Id 또는 동등</span> 이 됩니다.<br /> </span></td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭스루 비율<br /> </td> 
   <td> @inappclickthrough<br /> </td> 
   <td> 단추 1 또는 단추 2/총 노출 횟수*100<br />에 대한 총 클릭 수 </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 인앱 해지<br /> </td> 
   <td> @dismissal<br /> </td> 
   <td> @count (status=close)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 고유한 인앱 무시<br /> </td> 
   <td> @uniquedismissal<br /> </td> 
   <td> @unique(@count (status=close))<br /> </td> 
   <td> 캠페인 프로필(inAppProfile)</span> 템플릿을 기반으로 한 <span class="uicontrol">Target 사용자의 경우 사용자 = 수신자 ID입니다.<br /> 모바일 앱(inAppBroadcast)의 모든 사용자 <span class="uicontrol">와 모바일 프로파일(inApp) 템플릿을 기반으로 한 </span> Target 사용자를 Target <span class="uicontrol">의 경우 사용자, 모바일 앱 및 디바이스의 고유한 조합을 나타내는 사용자 = MC Id 또는 동등</span> 이 됩니다.<br /> </span></td> 
  </tr> 
  <tr> 
   <td> 인앱 해촉률<br /> </td> 
   <td> @dismissalrate<br /> </td> 
   <td> 전체 닫기/총 노출 수*100<br /> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

