---
title: 2018년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2018년 릴리스가 모두 나열되어 있습니다.
page-status-flag: never-activated
uuid: 99f92a54-4b3d-48b9-b08d-e98b24e75f62
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: e54f8305-7e32-4193-8e5a-b5d87b03038c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b1fb4a0dc0f7881e24e10f8ac171feab2ac8cba
workflow-type: tm+mt
source-wordcount: '5400'
ht-degree: 6%

---


# 2018년 릴리스 정보{#release-notes}

Adobe Campaign Standard의 2018년 특정 릴리스를 찾고 계십니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 해당 콘텐츠를 보려면 릴리스를 클릭하십시오.

Adobe Campaign Standard에 대한 최신 [설명서 업데이트를](../../rn/using/documentation-updates.md) 확인하십시오. 최신 릴리스를 원하는 경우 이 [페이지를 참조하십시오](../../rn/using/release-notes.md).

## 릴리스 18.9 - 2018년 9월 {#release-18-9---september-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 인앱 메시지(베타)<br /> </td> 
   <td> 인앱 메시징을 사용하면 상황에 맞는 인터랙션을 제공하고 푸시 알림을 옵트아웃했을 수 있는 사용자에게 도달할 수 있으므로 모바일 앱 사용자의 참여를 보다 효과적으로 유도할 수 있습니다. 푸시 알림과 함께 인앱 메시지를 사용하여 개인화되고 고객과 연관성 높은 경험을 제작할 수 있습니다. 따라서 앱 사용자의 전환율과 유지율이 향상됩니다.<br /> 자세한 내용은 <a href="../../channels/using/about-in-app-messaging.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Launch integration for mobile apps (beta)<br /> </td> 
   <td> 이제 Adobe Campaign과 Adobe 실행 통합을 통해 Mobile SDK V5를 사용하여 Campaign에서 모바일 앱 속성 활성화 프로세스를 간소화하고 자동화합니다.<br /> 자세한 내용은 <a href="https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**개선 사항**

* Adobe Campaign Standard은 이제 Amazon S3 API 버전 4를 지원합니다.

**기타 변경 사항**

* 이제 브로드캐스팅에는 최대 연결 수와 시간당 최대 메시지 수 사이에 차이가 있습니다. When the limits are reached, it is possible to know why the throughput is limited. 이전에는, 동일한 메시지(&#39;할당량 충족&#39;)가 두 경우 모두에 적용되었습니다.
* Campaign에서 모바일 응용 프로그램을 구성할 때 이제 사용자는 iOS 인증서 및 Android 서버 키가 성공적으로 업로드되었는지 및 만료일을 알 수 있습니다.

   자세한 내용은 [SDK V4](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdkv4.html) 및 [SDK V5를 사용하여 모바일 애플리케이션을 구성하는 방법에 대한 자세한 설명서를 참조하십시오](https://helpx.adobe.com/kr/campaign/kb/configuring-app-sdk.html).

* 캠페인 속성을 정의하는 동안 모바일 앱을 선택하여 특정 모바일 앱에 있는 Target 사용자 이 기능은 푸시 및 인앱 메시지 채널 모두에 적용됩니다.

   자세한 내용은 [세부 설명서](../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification)를 참조하십시오.

* Creative Designer 인터페이스를 사용하여 콘텐츠 블록을 선택하면 목록에 있는 모든 콘텐츠 블록이 로드되어 표시됩니다. (CAMP-27311)

   For more on this, refer to the [detailed documentation](../../designing/using/personalization.md#adding-a-content-block).

**패치**

* 트랜잭션 이메일에 대한 이메일 대시보드와 이메일 요약 보고서 간 로그 카운트에 불일치가 표시되는 문제를 수정했습니다. (CAMP-28237
* 파일 전송 활동을 통해 파일을 가져올 때 오류 메시지를 표시할 수 있는 워크플로우의 문제를 수정했습니다. (CAMP-27435)
* 25개 이상의 서비스가 포함된 랜딩 페이지의 문제를 해결했습니다. 이로 인해 서비스는 양식에서 임의로 선택 해제되었습니다. (CAMP-26572)
* 파일 전송 활동을 사용할 때 SFTP URL로 외부 계정을 구성할 수 없는 워크플로우의 문제를 수정했습니다. (CAMP-26475)
* 서비스 요약 보고서가 업데이트되지 않는 문제를 해결했습니다. (CAMP-26301)
* 데이터 연계 강화 활동을 사용할 때 사용자 지정 필드가 올바른 날짜를 표시하지 못하는 문제를 해결했습니다. (CAMP-26242)
* 파일 가져오기를 통해 가져올 때 서비스 구독 날짜가 업데이트되지 않는 문제를 해결했습니다.
* 워크플로우가 파일을 가져올 수 없는 로드 파일 작업(CAMP-27068) 오류를 수정했습니다.
* 서비스 요약 보고서에 잘못된 수의 구독(CAMP-25587)이 표시되던 문제를 수정했습니다.
* Adobe Analytics 보고서와 Adobe Campaign 보고서 간의 데이터 불일치 문제가 해결되었습니다. (CAMP-25393)
* 제한된 액세스 사용자가 로그인하지 못하게 하는 문제가 해결되었습니다. (CAMP-27381)
* Creative Designer를 사용하여 이메일을 편집할 때 Adobe Experience Manager 콘텐츠 목록이 표시되지 않는 문제를 해결했습니다. (CAMP-27181)
* Creative Designer가 열리지 않아 오류가 발생하는 문제를 해결했습니다. (CAMP-27304)
* Internet Explorer 11을 사용할 때 Creative Designer에서 드래그 앤 드롭이 제대로 작동하지 않는 문제를 해결했습니다.
* 카메라 및 세로 모드에서 업로드한 사진이 원하지 않는 회전 위치로 표시되는 문제를 해결했습니다.
* Creative Designer에서 쿼리 편집기 인터페이스를 사용할 때 선택 정보가 불명확하게 표시되는 문제를 해결했습니다.
* Creative Designer에서 쿼리 편집기 인터페이스를 사용할 때 요소를 올바르게 복제할 수 없는 문제를 해결했습니다.
* 자동 답글을 통해 구독이 해지되었음에도 불구하고의 수신자에게 SMS 메시지를 계속 전달하던 문제가 차단 목록 해결되었습니다. (CAMP-27128)
* 데이터베이스 정리 워크플로가 실패했던 오류를 **표시하지** 못하는 문제를 해결했습니다. (CAMP-26876)
* 푸시 알림 정의에서 사용자 정의 필드가 삭제되지 않는 문제를 해결했습니다. (CAMP-25588)

## 릴리스 18.7 - 2018년 7월 {#release-18-7---july-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Android 푸시 알림에 대한 높은 우선 순위 플래그<br /> </td> 
   <td> Android의 높은 우선 순위 플래그 - 대기 장치가 일어나 일부 제한된 처리를 실행하는 Android 앱에 우선 순위가 높은 푸시 알림을 제공할 수 있습니다. 기본 우선 순위는 Normal(표준)로, 이로 인해 메시지 전달이 지연되어 배터리 절약 <br /> 자세한 내용은 <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모바일 앱 가입자를 위한 유형 필터<br /> </td> 
   <td> 분류 필터에서 구독 지원 - 유형 규칙에 대한 필터링 기준을 지정할 때 애플리케이션 가입을 필터링 및 타깃팅 차원으로 선택할 수 있으므로, 프로파일을 포함하거나 포함하지 않은 사용자에 대해 속성을 필터링할 수 있습니다. <br /> 자세한 내용은 <a href="../../sending/using/about-typology-rules.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 메시지 준비 중 URL에서 자동 컨텐츠 가져오기<br /> </td> 
   <td> 이제 준비 단계 동안 URL에서 이메일 컨텐츠를 가져올 수 있습니다. 반복되는 이메일 게재의 경우, 이메일 전송 시 컨텐츠가 항상 최신 상태로 유지되도록 메시지가 준비될 때마다 최신 HTML 컨텐츠가 검색됩니다. 이 기능을 사용하면 컨텐츠가 아직 준비되지 않은 경우에도 URL의 컨텐츠가 포함된 예약된 전달을 만들 수도 있습니다.<br /> 자세한 내용은 <a href="../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 캠페인 릴리스 알림 메시지<br /> </td> 
   <td> 이제 인스턴스가 새 버전으로 업그레이드된 후 사용자가 로그인할 때 팝업 메시지가 표시됩니다. 이 메시지는 버전 번호를 나타내며 릴리스 노트에 대한 링크를 포함합니다. 다음 릴리스까지 메시지를 숨기도록 선택할 수 있습니다. <br /> </td> 
  </tr> 
  <tr> 
   <td> 사용자 관리<br /> </td> 
   <td> 18.7 릴리스부터 지리학적 단위가 만들어지지 않은 기존 인스턴스는 물론, 새로운 Campaign Standard 인스턴스에는 지리적 단위 기능을 사용할 수 없습니다.<br /> 자세한 내용은 이 <a href="https://helpx.adobe.com/kr/campaign/kb/acs-deprecated-and-removed-features.html">페이지를 참조하십시오</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**개선 사항**

* 이제 Adobe Campaign 및 Adobe Target 통합을 통해 Target [권한](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/properties-overview.html) 기능을 활용할 수 있습니다. 이제 이메일에 Adobe Target의 동적 이미지를 포함할 때 Target 속성(at_property 코드)을 지정할 수 있습니다.
* 프로필 리소스에 대한 다운로드 링크가 있는 사용자 지정 리소스는 이제 GDPR 개인 정보 액세스/삭제 요청에 의해 고려됩니다. 1개의 카디널리티 단순 링크 및 N 카디널리티 수집 링크의 경우, 사용자 지정 리소스에서 &quot;대상 레코드를 삭제/복제하는 것은 링크가 참조하는 레코드를 삭제/복제하는 것을 의미함&quot;을 선택해야 합니다. 0개 또는 1개의 카디널리티 단순 링크의 경우 &quot;레코드를 삭제/복제하는 것은 링크에서 참조하는 대상 레코드를 삭제/복제하는 것을 의미함&quot;을 선택합니다.

**기타 변경 사항**

* 제한 시간이 1~4분으로 증가하여 제한 시간 오류가 발생하지 않도록 했습니다.
* 이메일 컨텐츠를 편집할 때 새로운 Creative Designer가 기본적으로 열립니다. 원할 경우 변경 사항을 저장한 후에도 언제든지 기본 컨텐츠 편집기로 돌아갈 수 있습니다. For more on this, refer to the [detailed documentation](../../designing/using/designing-content-in-adobe-campaign.md).
* 이제 Creative Designer에서 새 컨텐츠 구성 요소를 이메일에 추가할 수 있습니다.회전판입니다. For more on this, refer to the [detailed documentation](../../designing/using/designing-from-scratch.md#about-content-components).
* 트랜잭션 메시지 핫 클릭 보고서에서 프로필 **변경** 단추를 클릭하면 트랜잭션 메시지에 대해 정의한 이벤트에 연결된 테스트 프로필만 나열됩니다.

**패치**

* 결과를 반환하지 못하는 byEmail 쿼리 필터 문제를 해결했습니다. (CAMP-23420)
* 표준 사용자가 관리자(/rest/head/* 엔드포인트, 트랜잭션 메시지 화면, 프로필 및 대상 가져오기 화면)로 제한된 특정 기능 또는 화면에 액세스할 수 있었던 문제를 수정했습니다.
* 이름이 숫자로 시작된 경우 GDPR 개인 정보 삭제 요청이 사용자 지정 리소스를 처리하지 못하는 문제를 해결했습니다.
* 대상자 저장 활동이 Adobe Experience Cloud에서 응용 프로그램 구독자를 공유할 수 없는 오류를 수정했습니다.
* 파일 이름에 빈 공백이 있을 때 발생할 수 있는 파일 전송 작업 문제를 수정했습니다. (CAMP-25936)
* 세션이 만료된 후 다시 연결 단추를 사용할 때 발생할 수 있는 문제를 수정했습니다. (CAMP-25560)
* 파티트 규칙과 연관된 표준 시간대 최적화를 사용하여 배달 전송 시 제외되도록 만들 수 있는 문제를 수정했습니다. (CAMP-25425)
* API GDPR 기능을 사용할 때 0-1 유형 링크가 있는 데이터를 삭제하지 못하는 문제가 해결되었습니다.
* 피로 유형 규칙 에디션을 취소할 때 오류 메시지가 표시되는 문제를 해결했습니다.
* 게재 컨텐츠를 편집한 후 미리 볼 때 발생할 수 있는 문제를 수정했습니다.
* 압축 해제 옵션을 사용하는 동안 CSV zip 파일을 처리할 때 발생할 수 있는 문제를 수정했습니다.
* 스타일이 내장되어 있는 일부 텍스트를 링크로 변경하거나 해당 링크를 편집할 때 원하지 않는 색상 글꼴과 서식이 발생하는 Creative Designer의 문제를 수정했습니다. (CAMP-26001)
* 동적 컨텐츠가 들어 있는 배달에서 각 조건에 대한 백분율을 표시할 수 없는 문제를 해결했습니다. 이전에는 기본 변형에 대한 클릭만 표시되었습니다.

## 릴리스 18.6 - 2018년 6월 {#release-18-6---june-2018}

**개선 사항**

* API가 Adobe.IO에 추가되었습니다. **[!UICONTROL History]** 프로필의 마케팅 내역과 관련된 정보에 액세스할 수 있습니다.터치포인트, 전송, 미러 페이지 URL 등 수 For more on this, refer to the [dedicated use case](../../api/using/interacting-with-marketing-history.md) .
* 데이터베이스 **[!UICONTROL Database cleanup]** 백업에 대한 성능 향상을 위해 기술 워크플로우가 최적화되었습니다.
* 이메일용 Creative Designer는 이제 프랑스어 및 독일어로도 제공됩니다.

**기타 변경 사항**

* 전송 창에 **[!UICONTROL Compute stats]** 단추가 **[!UICONTROL Deployment]** 추가되었습니다. 이 보고서를 사용하면 최신 KPI를 검색할 수 있습니다. 예를 들어 전송 결과를 업데이트하는 데 시간이 너무 오래 걸리거나 고려하지 않은 경우입니다. 자세한 정보는 이 [섹션](../../sending/using/confirming-the-send.md)을 참조하십시오.
* 즉시 사용 가능한 기술 작업 **흐름을 위한** 업데이트 **에서 기능 관리자는 이제** 업데이트 규칙javascript 활동에서 무시할 연속 오류 수를 정의할 수 있습니다. 기본적으로 필드 값은 0으로 설정되므로 모든 오류가 무시됩니다.
* 장치 액세스 제한 조건을 관리할 때 생성된 SQL이 최적화되었습니다.
* 이제 **[!UICONTROL Update]** 활동에서 구독과 관련된 데이터를 추가, 업데이트 또는 삭제할 수 있습니다(nms:appSubscriptionRcp 테이블).
* 기술 워크플로우는 성능을 최적화하기 위해 두 개의 워크플로우로 구분되었습니다. **[!UICONTROL Update delivery execution]** - **[!UICONTROL Update delivery execution]**:게재 추적을 업데이트합니다. 기본적으로 10분마다 시작됩니다. **[!UICONTROL Update delivery indicators]**:전달 KPI를 업데이트하면 기본적으로 매시간마다 시작됩니다. For more on technical workflows, refer to this [section](../../administration/using/technical-workflows.md#list-of-technical-workflows).
* 배달에서 메시지를 전송하는 경우 이제 섹션의 상태 **[!UICONTROL Deployment]** 에 두 개의 값이 있을 수 있습니다. **[!UICONTROL Sending]**:메시지를 보내는 중입니다. **[!UICONTROL Sending (retry)]**:재시도 패스가 진행 중입니다.
* 이제 해당 **[!UICONTROL Delivery preparation]** 역할의 사용자가 교정본을 보낼 수 있습니다. (CAMP-24313)
* SMPP **외부 계정을 통해** SMS **라우팅** 에 TLS 사용옵션이추가되었습니다. For more on this refer to this [section](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).

**패치**

* Adobe Target의 동적 이미지를 포함할 때 이메일이 전송되지 않도록 하는 문제를 해결했습니다(CAMP-24848).
* 요청이 실패할 경우 완료되지 않은 **[!UICONTROL Privacy Access/Delete Request]** 기술 워크플로우 문제를 해결했습니다.
* 개인 정보 핵심 서비스가 Campaign에서 요청 상태 업데이트를 받지 못하는 문제를 해결했습니다.
* Fixed an issue which could prevent the **[!UICONTROL Import shared audience]** technical workflow from working properly (CAMP-25465).
* 캠페인 개인 정보 요청이 핵심 Privacy Service에서 완료된 것으로 표시되지 않는 문제를 해결했습니다.
* Adobe ID이 너무 길었을 때 특정 사용자가 IMS 인증을 통해 Campaign Standard에 로그인하지 못하게 하는 문제가 해결되었습니다. (CAMP-24095)
* 콘텐츠 모듈을 제거할 때 발생할 수 있는 Creative Designer 문제를 해결했습니다. (CAMP-25242)
* 데이터베이스에 프로필이 없는 가입자에 대해 푸시 알림 피로 규칙을 사용할 때 발생하는 문제가 해결되었습니다. (CAMP-25344)
* 배달 제외 로그에 액세스할 때 오류 메시지가 표시되는 문제를 해결했습니다. (CAMP-24724)
* 확장된 전송 로그가 있는 경우 교정본을 준비할 수 없는 문제를 해결했습니다.
* 확장 기능이 활성화된 사용자 지정 리소스를 게시할 때 발생할 수 있는 두 가지 문제를 **[!UICONTROL Sending log]** 수정했습니다.
* 반복 배달에서 배달 기간이 고려되지 않는 문제가 해결되었습니다.
* 100K가 넘는 사용자 지정 리소스에 대해 **[!UICONTROL Client data]** 메뉴에서 데이터를 정렬할 때 발생할 수 있는 문제를 수정했습니다. (CAMP-24308)
* 동적 보고서에서 검색 기능을 사용할 때 고려되지 않은 사용자 지정 프로필 차원 문제를 수정했습니다.
* 동적 보고서에서 계정 수준에 대한 국제 데이터 표시 문제를 해결했습니다.
* 이제 구독 또는 구독 취소 확인 메시지 없이 서비스를 만들 수 있습니다.

## 릴리스 18.5 - 2018년 5월 {#release-18-5---may-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> GDPR:핵심 서비스 통합<br /> </td> 
   <td> 개인 정보 핵심 서비스 통합을 통해 단일 JSON API 호출을 통해 멀티 솔루션 컨텍스트에서 GDPR 요청을 자동화할 수 있습니다. <br /> 개인 정보 핵심 서비스에서 모든 Experience Cloud 솔루션으로 푸시된 GDPR 요청은 이제 Campaign에서 자동으로 처리됩니다. <br /> 자세한 내용은 <a href="https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 향상된 푸시 - 자세한 전달 피드백<br /> </td> 
   <td> 이제 Adobe Campaign은 MCPNS를 통해 공급자로부터 푸시 메시지(APNS/GCM)에 대한 자세한 피드백(로그 세트 제외 로그 전송)을 받는 기능을 제공합니다.<br /> 자세한 내용은 <a href="../../channels/using/preparing-and-sending-a-push-notification.md#sending-the-notification">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 로그 확장<br /> </td> 
   <td> 전달 로그 확장 기능을 사용하면 워크플로우에서 생성된 프로필 데이터 및 세그먼트 코드로 전송 로그를 확장할 수 있습니다. 그런 다음 이 정보를 동적 보고서에서 사용할 수 있으며 배달 시 일부 정보의 스냅숏을 유지할 수 있습니다.<br /> 다음 두 가지 사용 사례가 더 있습니다.<br /> 
    <ul> 
     <li> "동결" 데이터로 확장 브로드로그를 내보낼 수 있습니다.마케터는 세그먼트 코드가 "A"(워크플로우 엔진에서 제공)인 모든 프로파일을 내보내고 싶어합니다. </li> 
     <li> "동결" 데이터의 세그멘테이션:마케터는 마지막 전송 이후 1000개의 로열티 포인트 획득 또는 세그먼트 코드가 "A"와 동일한 경우 모든 프로파일을 <strong>리타겟팅하고</strong> 싶습니다. </li> 
    </ul> 자세한 내용은 <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamic reporting with Custom profile data<br /> </td> 
   <td> 이 기능을 사용하면 프로필 리소스 확장 중에 생성된 사용자 지정 프로필 데이터를 기반으로 보고서를 만들고 관리할 수 있습니다. 충성도 프로그램, 기본 채널 등과 같은 프로필 속성별로 보고서를 분류할 수 있습니다.<br /> 자세한 내용은 <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**개선 사항**

* 응용 프로그램의 전체 메모리 및 CPU 사용이 개선되었습니다.

**기타 변경 사항**

* 이제 대상 읽기 워크플로우 활동이 Experience Cloud 대상을 읽을 수 있습니다. 이전에는 이 활동에서는 쿼리 및 목록 대상만 읽을 수 있었습니다. 자세한 [설명서를 참조하십시오](../../automating/using/read-audience.md). (CAMP-23623)
* 기본 공유 데이터 소스의 식별자는 이제 읽기 전용 모드이며 더 이상 변경할 수 없습니다. 이 식별자를 변경하면 대상을 Experience Cloud과 공유할 때 일부 문제가 발생할 수 있습니다.
* 이제 Audience Manager에서 대상을 가져오는 기능이 분할된 파일에서 작동합니다. 이전에는 importSharedAudience 기술 워크플로우에서 세그먼트의 마지막 파일만 가져왔습니다.
* 이제 AWS S3 외부 계정은 지역 및 버전 4 인증 메커니즘을 지원합니다. 자세한 [설명서를 참조하십시오](../../administration/using/external-accounts.md).
* 이제 자산 선택 창이 더 빠르게 로드되고 자산을 선택한 다음 아무 문제 없이 창을 종료합니다.
* 이제 관리 권한이 있고 &quot;모든&quot; 조직 및 지역 단위에 속한 사용자가 기술 워크플로우의 속성 및 구조를 수정할 수 있습니다.
* 새 세그먼트를 만들 때 세그멘테이션 활동 인터페이스에서 개선되었습니다.이제 제한 탭이 제한을 추가한 후 바로 나타납니다. 이제 새 세그먼트 이름이 증가됩니다(&quot;세그먼트 1&quot;, &quot;세그먼트 2&quot; 등).
* &quot;nextProcessingDate&quot; 필드가 워크플로 리소스에 추가됩니다. 이 필드는 REST API 호출을 통해서만 표시되므로 다음 처리 날짜에 워크플로우를 시각화할 수 있습니다.
* 이제 &quot;sourceId&quot; 필드가 추적 로그 리소스(nms:trackingLog)에 노출됩니다.
* 이제 워크플로우를 통해 플랫 파일로 &quot;총 열기&quot; 및 &quot;총 클릭 수&quot; 값을 내보낼 수 있습니다. (CAMP-24186)
* &quot;영어 - Danmark&quot;는 이제 프로필의 기본 언어 목록에서 사용할 수 있습니다. (CAMP-23728)
* 이제 추가 데이터(targetData) 링크와 함께 세그멘테이션 활동을 사용할 때 워크플로우 외부에서 데이터를 사용할 수 없다는 메시지가 표시됩니다. 이 메시지는 세그멘테이션 활동에서 카운트 또는 미리 보기 단추를 클릭하면 표시됩니다. (CAMP-23651)
* 워크플로우에서 사용하는 디스크 공간을 최적화하기 위해 향상된 기능이 제공됩니다.(CAMP-21979):이제 &quot;파일 로드&quot; 활동으로 처리된 파일이 기본적으로 삭제됩니다. 옵션을 사용하면 특정 요구 사항에 맞게 유지할 수 있습니다. 워크플로우가 삭제되면 전용 폴더가 서버 디렉토리에서 자동으로 억제됩니다.

**패치**

* eventDate 필드가 제대로 채워지지 않아 일부 원시 보고 이벤트에 추적 이벤트가 연결되어 있지 않았던 문제를 수정했습니다.
* 개인화된 필드가 푸시 알림 전달의 미리 보기 창에 표시되지 않던 문제를 수정했습니다.
* 텍스트가 미리 보기 창에서 푸시 알림의 메시지 본문을 단어 래핑하지 않는 문제를 해결했습니다.
* 기본 대상이 비어 있을 때 워크플로우에서 재지정 배달을 보낼 때 발생하는 문제를 해결했습니다.
* 기존 스키마에 연결된 경우 대상 매핑에 액세스할 수 없는 문제를 수정했습니다.
* 파일 로드 활동을 통해 zip 파일을 가져올 때 발생할 수 있는 문제를 수정했습니다. (CAMP-24309)
* 반복 배달을 보낼 때 PostgreSQL 오류가 발생하는 문제를 해결했습니다. (CAMP-23613)
* 빈 JSON 특성이 있는 REST API 요청을 전송할 때 오류 메시지가 표시되던 문제를 수정했습니다. (CAMP-23506)
* &quot;S&quot; 문자 다음에 문자를 대문자로 설정하는 프로필의 문제를 수정했습니다. (CAMP-23136)
* 연결된 프로필 스키마의 특성을 사용하는 동안 개인화 또는 동적 콘텐츠 블록의 자격 조건에 사용되는 배달을 전송할 때 발생하는 문제가 해결되었습니다. (CAMP-22751)
* 서비스를 삭제할 수 없는 문제를 수정했습니다. (CAMP-22050)
* 테스트 프로필의 국가 또는 상태 값을 변경할 수 없는 문제를 수정했습니다. (CAMP-20426)
* Creative Designer가 로드되지 않는 문제를 해결했습니다. (CAMP-24573)
* 이메일 제목에 있는 개인화 필드 후에 추가된 문자가 제거되는 문제를 수정했습니다. (CAMP-24113)

## 릴리스 18.4 - 2018년 4월 {#release-18-4---april-2018}

**패치**

_플랫폼_

* GDPR 액세스 또는 삭제 요청을 올바로 처리하지 못하는 오류를 수정했습니다. 이러한 동작은 추출된 데이터에 다음 문자 중 하나가 포함된 드문 경우에 관찰되었습니다.&amp; &lt; > &quot; &#39;.

_이메일, SMS 메시지 및 DM_

* 브로드캐스트 동기화 시간이 1시간 이상 걸리는 경우 KPI를 잘못된 값으로 덮어쓸 수 있는 문제를 수정했습니다.

_워크플로우_

* 워크플로우에서 메모리 관리 및 최적화된 성능을 개선했습니다.

_보고_

* 이제 KPI 공유 워크플로우는 지난 6개월 대신 최근 2개월 동안 배달 값을 검색합니다. 잘린 날짜를 표시하는 KPI 공유 외부 계정 문제가 해결되었습니다.
* 보낸 사람, 배달된 사람 **및 바운스 지표에서 특정 메시지가**&#x200B;고려되지 않는 문제 **** 를 ****&#x200B;해결했습니다.
* 배달 요약 보고서에서 선택한 시간 범위가 너무 **길었을 때 발생하는** 오류를 수정했습니다.

_사용자 정의 리소스_

* 사용자 지정 리소스 준비에 실패하는 오류를 수정했습니다.

## 릴리스 18.3 - 2018년 3월 {#release-18-3---march-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> EU General Data Protection Regulation (GDPR)<br /> </td> 
   <td> GDPR은 2018년 5월 25일부터 적용되는 데이터 보호 요구 사항을 통합하고 현대화한 유럽 연합의 새로운 개인 정보 보호법입니다. GDPR은 유럽 연합에 거주하는 데이터 주체의 데이터를 보유하고 있는 Adobe Campaign 고객에게 적용됩니다.<br /> Adobe는 Adobe Campaign에서 이미 사용 가능한 개인 정보 보호 기능(동의 관리, 데이터 유지 설정 및 사용자 역할 포함) 이외에도 데이터 프로세서로서의 Adobe의 기능을 통해 특정 GDPR 요청에 대해 데이터 컨트롤러로서 사용자의 준비를 촉진할 수 있도록 다음과 같은 추가 기능을 제공합니다.<br /> 
    <ul> 
     <li> 액세스 권한:데이터 주체가 데이터 관리자가 캡처한 개인 데이터의 사본을 받을 수 있도록 허용하며, 여기에는 잠재적으로 Adobe Campaign에 저장된 데이터가 포함됩니다. </li> 
     <li> 삭제할 권한:데이터 주체가 데이터 컨트롤러로부터 캡처한 개인 데이터를 삭제하도록 하며, 여기에는 Adobe Campaign에 저장된 데이터도 포함됩니다. </li> 
    </ul> 자세한 내용은 <a href="https://helpx.adobe.com/kr/campaign/kb/campaign-privacy.html">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이메일을 위한 Creative Designer(베타)<br /> </td> 
   <td> Adobe Campaign의 새로운 크리에이티브 디자이너는 Adobe Campaign과 완벽하게 통합된 제작 경험을 제공하므로 코드를 단 한 줄도 스크립팅하지 않고도 개인화된 매력적인 이메일을 빠르고 손쉽게 제작할 수 있습니다. Creative Designer는 강력한 드래그 앤 드롭 인터페이스에서 사용자가 빈 슬레이트 상태에서 시작하거나 기존 컨텐츠 조각 또는 템플릿을 활용하더라도 이메일 작성을 확장할 수 있도록 지원합니다. <br /> 주요 기능은 다음과 같습니다.<br /> 
    <ul> 
     <li> 드래그 앤 드롭 방식의 인터페이스, 기본 Creative Cloud 통합을 통해 개인화된 반응형 이메일을 시각적으로 디자인 및 제작 </li> 
     <li> 이메일 컨텐츠 템플릿 작성 및 저장 및 저장된 템플릿 활용을 통해 이메일 제작 확장 </li> 
     <li> 컨텐츠 조각(머리글, 바닥글, 아티클 등)을 만들고 저장합니다. 컨텐츠 제작 간소화 및 브랜드 일관성 보장 </li> 
     <li> 드래그 앤 드롭 인터페이스에서 만들기 간을 원활하게 전환할 수 있고 단추 클릭 시 이메일의 HTML을 직접 편집할 수 있습니다 </li> 
    </ul> 이메일용 Creative Designer는 영어로만 제공됩니다.<br /> 자세한 내용은 <a href="../../designing/using/designing-content-in-adobe-campaign.md">자세한 설명서를</a> 참조하고 이 <a href="https://www.youtube.com/watch?time_continue=1&amp;v=5S_6A4fsfms">비디오를</a>시청하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 다국어 푸시 배달<br /> </td> 
   <td> 이메일 및 SMS 채널에도 이미 존재하는 단순한 다국어 인터페이스가 푸시 채널에 추가되어 고객의 원하는 언어와 상관없이 고객의 참여를 유도할 수 있습니다.<br /> 이 기능은 여러 지역에서 푸시 캠페인을 관리하고 사용자가 원하는 언어로 타깃팅하기를 원하는 고객을 위한 확장 가능하고 자동 솔루션을 제공합니다. 템플릿 스프레드시트를 통해 모든 언어 변형을 한 번의 클릭으로 단일 푸시 배달로 업로드할 수 있습니다. 그런 다음 Adobe Campaign은 사용자의 언어 기본 설정에 따라 자동 세분화를 수행하여 워크플로우와 보고를 단순화하여 불필요한 중복 항목을 줄일 수 있습니다.<br /> 자세한 내용은 <a href="../../channels/using/creating-a-multilingual-push-notification.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Use of Custom Resources in Transactional Messaging<br /> </td> 
   <td> 기본 필드 외에도 트랜잭션 메시징을 사용하면 맞춤형 리소스를 통해 메시지 내용을 더욱 멋지게 만들 수 있습니다.<br /> 예제:<br /> 
    <ul> 
     <li> 사용자 정의 필드를 조정 기준으로 활용하여 트랜잭션 메시지를 프로필에 일치 </li> 
     <li> 전체 프로파일, 서비스 및 연결된 데이터를 활용하여 트랜잭션 메시지 개인화 </li> 
    </ul> 자세한 내용은 <a href="../../administration/using/configuring-transactional-messaging.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 목록에서 5,000개가 넘는 레코드를 내보낼 수 없는 문제를 해결했습니다.
* 개인화 필드를 사용하여 명명된 파일로 데이터를 내보낼 때 발생하는 문제가 해결되었습니다.

_이메일, SMS 메시지 및 DM_

* 부분 크기가 바이트 대신 문자로 계산되었기 때문에 다중 부분 SMS가 잘리는 문제를 해결했습니다.
* Added an option which allows the **[!UICONTROL Delivered]** or **[!UICONTROL Bounces + Errors]** KPIs to be updated in real time after sending your delivery. 공급자로부터 받은 SR(상태 보고서)에서 직접 다시 계산됩니다.
* 배달 스케줄러의 달력 위젯 문제를 수정했습니다.
* 전송된 배달에서 두 번째로 대상을 열 때의 표시 문제를 수정했습니다.
* 지연된 전송 날짜가 있는 이메일 템플릿을 만들 때 시작 날짜를 요청하는 오류 메시지가 표시되는 문제를 해결했습니다.
* 게재 컨텐츠를 편집할 때 이미지 렌더링 문제가 발생하는 문제를 해결했습니다.
* 캠페인을 복제할 때 교정쇄 문제가 해결되었습니다.
* 워크플로에 배달을 추가한 후 내비게이션 막대를 통해 캠페인 템플릿에 액세스할 때 오류 메시지가 표시되는 문제를 해결했습니다.
* A/B 테스트 이메일의 우승자가 자동으로 선택되지 않도록 하여 이메일이 전송되지 않는 문제를 해결했습니다. 배달이 **[!UICONTROL retryInProgress]** 상태이면 이 동작이 발생할 수 있습니다.
* A/B 테스트 이메일의 매개 변수를 다시 열 때 오류 메시지가 표시되는 문제를 해결했습니다.

_대상 및 쿼리_

* Adobe Campaign Classic에서 Standard로 복제된 수신자에 대한 데이터에 액세스하고 쿼리를 설정하지 못하는 문제를 해결했습니다.
* 쿼리 편집기에서 [ **카운트] 또는 [미리 보기] 단추를 사용한 후 필터 유형** 필드를 사용할 때 발생하던 **문제를** 수정했습니다.

_워크플로우_

* 청구 **워크플로우는** 배달 준비 지연을 개선하기 위해 최적화되었습니다.
* 반복 배달 활동을 사용할 때 인구 데이터가 아웃바운드 전환에 표시되지 않는 문제를 해결했습니다.
* 데이터 **업데이트 활동 후 전환 시 거부 레코드가 표시되지 않는 문제를** 해결했습니다.
* deliverabilityUpdate **기술 워크플로가** 실패할 수 있는 문제를 수정했습니다.

_통합_

* 국제 문자가 Adobe Analytics으로 올바르게 전송되지 않는 문제를 해결했습니다.
* 이제 Experience Cloud 에셋 라이브러리의 이미지를 메시지에 삽입하려고 할 때 에셋을 빠르게 로드해야 합니다.
* 경우에 따라 자산 선택 창이 닫히지 않는 문제를 해결했습니다.
* 이제 데이터 소스 세부 정보에서 관련 워크플로우에 직접 액세스하여 워크플로우 상태를 확인할 수 있습니다.
* 이제 트리거 이벤트를 정의하거나 편집할 때 트리거 스키마를 직접 업데이트할 수 있습니다. 이러한 변경 사항으로 인해 더 이상 트리거를 게시 취소하고 다른 트리거를 만들 필요가 없습니다.

_트랜잭션 메시지_

* 배달 리소스가 확장되었을 때 트랜잭션 메시지 템플릿의 오류를 수정했습니다.
* 이제 트랜잭션 메시지를 삭제할 수 있습니다.

## 릴리스 18.2 - 2018년 2월 {#release-18-2---february-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Subscription - subscribe or unsubscribe a list of profiles to multiple services<br /> </td> 
   <td> 구독 <strong>서비스</strong> 워크플로우 활동을 통해 여러 서비스에 대한 프로필 목록을 구독 또는 구독 취소할 수 있습니다. 워크플로우에서 프로파일이 포함된 파일과 각 프로파일의 작업 유형 및 서비스를 가져옵니다. 구독 <strong>서비스</strong> 활동은 이 정보를 사용하고 모든 프로필 구독 및 구독 취소를 한 번에 동적으로 처리할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/subscription-services.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Enrichment activity - enrich data based on previous transitions<br /> </td> 
   <td> 새로운 <span class="uicontrol">데이터 연계</span> 강화 워크플로우 활동을 통해 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료할 수 있습니다. 프로파일을 타깃팅하는 경우 데이터 연계 강화 기능을 사용하면 데이터베이스에 저장되지 않은 추가 데이터(예: 가져온 파일에서 가져온 데이터)로 프로파일 정보를 강화할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/enrichment.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* Adobe Campaign 인터페이스의 상단 막대가 새로운 Experience Cloud 메뉴로 업데이트되었습니다.
* 솔루션 드롭다운 목록에 링크가 표시되지 않는 문제 **[!UICONTROL Offers]** 를 해결했습니다.

_이메일, SMS 메시지 및 DM_

* 배달 준비 단계가 개선되어 성능이 향상되었다.
* 일부 틈새 상황에서 추적 로그가 손상될 수 있는 몇 가지 문제를 수정했습니다.
* 배달 준비와 확인 사이에 연락처 날짜가 변경되었을 때 발생하는 연락처 날짜 업데이트 문제를 해결했습니다. 이제 준비 후 연락처 날짜를 변경하면 전송을 확인하기 전에 배달을 다시 준비해야 합니다. 자세한 [설명서를 참조하십시오](../../sending/using/preparing-the-send.md).

_푸시 알림_

* iOS 푸시 알림에서 일부 개인화 필드가 작동하지 않던 오류를 수정했습니다.
* 푸시 알림 대시보드에서 클릭 및 열기 비율을 0%로 표시하는 오류를 수정했습니다.

_보고서_

* 일부 브라우저에서 보고서 목록이 비어 있는 것으로 표시하는 오류를 해결했습니다.
* 만료 제한에 도달하기 직전에 **[!UICONTROL Report sharing]** 기술 워크플로우에서 발생한 오류를 수정했습니다.

_워크플로우_

* 드래그 앤 드롭 후 활동에 액세스할 수 없는 문제를 해결했습니다.
* 일부 상황에서 활동의 출력 전환 순서가 변경될 수 있는 문제를 **[!UICONTROL Segmentation]** 수정했습니다.
* 열거형 유형 필드가 포함된 대상을 읽을 때 이전에 워크플로우에서 저장된 오류가 해결되었습니다.
* 워크플로우에서 생성된 게재의 예약 속성을 정의할 때 옵션을 선택 해제해도 옵션이 선택된 상태로 유지되게 하는 문제를 수정했습니다. **[!UICONTROL Request confirmation before sending messages]**
* 이제 활동(DISTINCT 절)에서 탭에 있는 새로운 옵션을 통해 중복 행 자동 제거 **[!UICONTROL Query]** 를 비활성화할 수 **[!UICONTROL Additional data]** 있습니다. 성능상의 이유로 추가 요소(100개 이상)를 정의할 때 이 옵션을 비활성화하는 것이 좋습니다.

_통합_

* 구성 화면에 일부 개선 사항이 **[!UICONTROL Data sources]** 적용되었습니다.

_알려진 문제_

표시 문제 때문에 Internet Explorer 버전 11을 사용하지 않는 것이 좋습니다.

Campaign 인터페이스의 컨텍스트 도움말 링크를 사용할 때 일부 문제가 발생할 수 있습니다. 18.3에 수정될 예정입니다.

## 릴리스 18.1 - 2018년 1월 {#release-18-1---january-2018}

**새로운 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 피로 관리 보고<br /> </td> 
   <td> 피로 관리 보고는 피로 규칙이 보내기 전에 지정된 날짜 범위 내에 이메일, 푸시, SMS 및 DM 채널에서 보낸 배달에 미치는 영향을 표시하는 구성 가능한 전용 보고서입니다. 상충되는 모든 캠페인을 한 번에 신속하게 확인할 수 있다는 통찰력이 더해져, 마케터는 피로 규칙을 보다 효과적으로 설정하여 마케팅 캠페인을 계획하고 커뮤니케이션의 우선 순위를 정할 수 있습니다.<br /> 자세한 내용은 <a href="../../sending/using/fatigue-rules.md#viewing-the-fatigue-rule-summary-report">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 보고서 공유<br /> </td> 
   <td> 보고서 공유를 사용하면 자동화된 반복 기준을 포함하여 보고서를 Adobe Campaign 사용자와 이메일 첨부 파일로 공유할 수 있습니다. 반복되는 보고서를 받는 사용자는 각 이메일에 있는 전용 링크를 통해 이러한 커뮤니케이션의 가입을 취소할 수 있습니다.<br /> 자세한 내용은 <a href="../../reporting/using/reporting-interface.md#share-tab">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 새로운 기능 푸시<br /> </td> 
   <td> 푸시 메시지 미리 보기 - 푸시 알림 컨텐츠 편집기 내에서 iOS 및 Android 디바이스에서 푸시 알림을 미리 볼 수 있으므로, 배달을 테스트하거나 실행하기 전에 수신자가 보게 될 내용을 정확하게 확인할 수 있습니다.<br /> 자세한 내용은 <a href="../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification">세부 설명서</a>를 참조하십시오.<br /> 사용 가능한 콘텐츠 - 앱이 오랜 시간 동안 열리지 않으면 데이터가 오래될 수 있습니다. 이로 인해 사용자가 앱을 마지막으로 여는 순간 데이터를 업데이트하거나 교체해야 하므로 앱 사용이 지연될 수 있습니다. 사용 가능한 컨텐츠에 대한 지원이 추가되어 Adobe Campaign 사용자는 푸시 알림을 제공할 때 백그라운드에서 자신의 데이터를 새로 고침하여 사용자의 인앱 경험을 일관되게 유지하고 제어할 수 있습니다.<br /> 변경 가능한 컨텐츠 - 이제 Adobe Campaign 사용자는 변경 가능한 컨텐트에 대한 지원이 추가되어 모바일 앱 익스텐션을 활용하여 Adobe Campaign에서 전송된 푸시 알림의 내용 또는 프레젠테이션을 더욱 수정할 수 있습니다. 예를 들어, 사용자는 변경 가능한 컨텐츠를 활용하여 다음을 수행할 수 있습니다. <br /> 
    <ul> 
     <li> 암호화된 형식으로 전달된 데이터 암호 해독 </li> 
     <li> 이미지 또는 기타 미디어 파일을 다운로드하고 알림에 첨부 파일로 추가 </li> 
     <li> 알림의 본문 또는 제목 텍스트 변경 </li> 
     <li> 알림에 스레드 식별자 추가 </li> 
    </ul> 사용 가능한 컨텐츠 및 변경 가능한 컨텐츠에 대한 자세한 내용은 <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios">자세한 설명서를 참조하십시오</a>.<br /> <strong>경고:</strong> 푸시 알림에 대한 이러한 업데이트를 사용하려면 고객이 모바일 애플리케이션을 업그레이드해야 합니다. Refer to <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard/using/communication-channels/push-notifications/push-payload.html">this technote</a> for more information.<br /> </td> 
  </tr> 
  <tr> 
   <td> 시간대로 최적화된 전달<br /> </td> 
   <td> 이메일, SMS 및 푸시 알림이 모든 수신자의 시간대에서 특정 일/시간에 배달되도록 예약하면 여러 번 메시지를 설정하지 않고도 적시에 배달됩니다. <br /> 자세한 내용은 <a href="../../automating/using/scheduler.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> API 신호 활동을 트리거합니다.<br /> </td> 
   <td> 이제 Adobe Campaign Standard API에서 직접 워크플로우에 대한 신호 활동을 트리거할 수 있습니다.<br /> 자세한 내용은 <a href="/help/api/using/triggering-a-signal-activity.md">자세한 설명서를 참조하십시오</a> .<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 프로필 검색을 최적화하여 성능을 개선했습니다.
* 이제 기본 보안 그룹의 내부 식별자가 표준 사용자에 대해 읽기 전용 모드입니다.

_이메일, SMS 메시지 및 DM_

* 게재의 컨텐츠에 이모지를 삽입할 때 발생하는 표시 문제를 해결했습니다.
* 배달을 계속 에디션할 때 사용자가 전송 로그에 액세스할 수 있었던 문제를 수정했습니다.
* 이제 **[!UICONTROL Scheduler]** 활동에서 수신자의 시간대에 따라 배달을 보낼 수 있습니다.
* SMS:데이터베이스 **[!UICONTROL Store incoming MO]** 의 옵션이 외부 계정에 추가되었습니다. 이 확인란을 선택하면 들어오는 모든 SMS가 **inSMS** 테이블에 저장됩니다.
* SMS:이제 트랜잭션 템플릿 대신 이벤트가 이벤트에 연결됩니다.
* SMS:기본 SMTP 연결 시간 초과가 30초로 감소되었습니다.

_푸시 알림_

* 푸시 알림 배달이 중지되지 않는 오류를 해결했습니다.
* 푸시 알림 고급 옵션에 푸시 알림으로 응용 프로그램을 깨우는 옵션을 추가했습니다.
* 푸시 알림 미리 보기 비디오에 대한 일시 정지 단추를 추가했습니다.
* 푸시 알림 미리 보기는 이제 iPhone, Android, 태블릿 등 다양한 장치에서 사용할 수 있습니다.

_보고서_

* 비율이 100% 이상인 오류를 수정했습니다.
* 사용자가 CSV로 보고서를 다운로드할 수 없는 문제를 해결했습니다.
* 홈 페이지에 새 **[!UICONTROL Report]** 항목을 추가했습니다.

_워크플로우_

* 쿼리에 추가 데이터를 사용하고 공백이 포함된 별칭을 추가할 때 오류 메시지가 표시되는 문제를 해결했습니다. 영숫자가 아닌 문자는 이제 &quot;_&quot;로 대체됩니다.
* KPI 계산 기술 워크플로우가 일부 경우 기본적으로 중지될 수 있었던 문제를 수정했습니다.

_프로필 및 대상자_

* 대상 쿼리에 필터를 여러 개 추가할 때 발생하는 오류가 수정되었습니다.
* 프로필 사진을 변경할 때 발생하는 표시 문제를 수정했습니다.
* 쿼리의 모집단을 계산한 후 정확한 결과 수를 표시하는 도구 설명이 추가되었습니다.
* 사용자가 대상을 선택하거나 대상자 선택기 창을 닫지 못하는 문제를 해결했습니다.
* 표현식 편집기의 사용 가능한 함수 목록이 업데이트되었습니다. FormatCurrency **및** ConvertCurrency **** 함수가 제거되었습니다.

