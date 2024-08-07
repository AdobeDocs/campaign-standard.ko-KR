---
title: 2017년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2017년 릴리스가 모두 나열되어 있습니다.
feature: Overview
role: User
level: Beginner
hidefromtoc: true
exl-id: 73a1ec49-fcbc-406b-9590-1ad20da9e73b
source-git-commit: bee4da592e0b3727949bc44c6e41b81d4e7e73d4
workflow-type: tm+mt
source-wordcount: '4572'
ht-degree: 3%

---

# 2017년 릴리스 정보{#release-notes}

## 릴리스 17.10 - 2017년 10월 {#release-17-10---october-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 피로도 관리<br /> </td> 
   <td> 피로도 관리를 사용하면 피로도 규칙을 만들어 프로필과의 과도한 커뮤니케이션을 관리할 수 있습니다. 피로도 규칙은 쉽게 작성할 수 있지만, 트랜잭션 메시지를 포함하여 여러 채널에서 메시지를 계산하거나, 특정 게재만 계산하거나, 특정 프로필에 규칙을 적용하는 등의 기능으로 매우 유연합니다.<br /> 자세한 내용은 <a href="../../sending/using/fatigue-rules.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 콘텐츠 만들기: URL<br />에서 가져오기 </td> 
   <td> URL에서 가져오기를 사용하면 웹 사이트에서 크리에이티브 콘텐츠를 빠르게 검색하여 배달할 이메일을 작성할 수 있습니다. 또한 타사에서 URL을 통해 직접 콘텐츠를 공유할 수 있게 하여 크리에이티브 프로세스를 간소화할 수 있습니다. 가져온 콘텐츠는 단일 게재의 일부나 템플릿 수준에서 유연하게 사용하여 워크플로우 기반 메시지든 트랜잭션 메시지든 관계없이 모든 관련 캠페인에 대한 브랜드 일관성을 보장하고, A/B 또는 다변량 테스트를 포함할 수 있습니다. URL에서 가져오기는 모든 링크를 자동으로 변환 및 추적하여 다이내믹 보고를 통해 이메일 성능을 모니터링합니다.<br /> 자세한 내용은 <a href="../../designing/using/using-existing-content.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 큰 압축 파일의 압축이 제대로 풀리지 않는 문제를 해결했습니다.
* 브랜드 관리 보안이 개선되었습니다. 브랜드 이름과 발신자 주소 수정은 이제 Adobe 기술 관리자용으로 예약되었습니다.
* 보안을 강화하기 위해 사용자 생성 컨텐츠(이미지, 미러 페이지, 랜딩 페이지 등) 더 이상 adobe.com 도메인에서 제공할 수 없습니다. 이제 브랜딩을 사용하여 고유한 도메인을 사용하여 이러한 리소스를 처리하는 것이 필수입니다.
* 마케팅 활동을 표시하고 필터링할 때 발생하는 인터페이스 문제를 수정했습니다.
* 구독 날짜 필드가 POST REST API 호출로 업데이트되지 않는 문제를 수정했습니다.

_전자 메일, SMS 메시지 및 DM_

* 메시지에서 목록 유형 대상자를 타깃팅하지 못하여 준비가 실패하는 문제를 해결했습니다.
* 다국어 이메일 게재 기능에 누락된 언어가 추가되었습니다.
* 이제 사용자가 콘텐츠를 수정하고 저장할 때 게재 대시보드에 표시되는 콘텐츠 썸네일이 자동으로 업데이트됩니다.
* 게재를 열 수 없는 시간대 관련 문제를 해결했습니다.

_푸시 알림_

* 푸시 알림 채널을 구성할 때 iOS용 푸시 공급자 플랫폼은 **apns** 및 Android **gcm**&#x200B;이어야 합니다.
* iOS 모바일 앱이 Adobe Campaign 인터페이스에 추가되지 않던 오류를 수정했습니다.
* 푸시 알림은 이제 GCM 및 FCM 지원 Android 모바일 애플리케이션 모두에서 지원됩니다.
* 푸시 알림 템플릿을 복제할 때 콘텐츠가 저장되지 않는 오류를 수정했습니다.
* 이제 모바일 애플리케이션 사용자의 데이터를 조정하여 Adobe Campaign 데이터베이스에서 프로필을 만들거나 업데이트할 수 있습니다.
* 이제 Adobe Campaign은 표준 푸시 알림보다 트랜잭션 푸시 알림 처리의 우선 순위를 지정합니다.

_보고서_

* 이메일 콘텐츠에 핫 클릭 비율이 표시되지 않는 문제를 해결했습니다.
* 바운스 대신 바운스로 계산된 하드 차단 목록 지표 문제를 수정했습니다.
* 요약 데이터에 음수 카운트가 표시되는 문제를 해결했습니다.
* 잘못된 연령 세그먼트의 프로필을 계산하는 문제를 해결했습니다.
* 소프트 및 하드 바운스 계산 공식이 변경되었습니다.

_워크플로_

* 활동에서 열을 수동으로 추가하고 제거한 후 오류가 발생할 수 있는 **[!UICONTROL Load file]** 활동의 문제를 해결했습니다.
* **[!UICONTROL deliverabilityUpdate]** 기술 워크플로우가 서버 시간으로 오전 2시에 실행되도록 예약되었습니다.
* 내보내기 역할 없이 목록 내보내기를 수행할 수 있었던 보안 문제를 해결했습니다.
* **[!UICONTROL Reconciliation]** 활동 문제를 해결했습니다.
* **[!UICONTROL File Transfer]** 활동에서 와일드카드 문자를 사용하는 문제를 해결했습니다.

_프로필 및 대상자_

* 일부 특정 경우에 쿼리의 조건이 올바르게 고려되지 않아 잘못된 결과가 발생하는 문제를 해결했습니다.
* 준비되었지만 전송 및 만료된 적이 없는 메시지에서 프로필을 타겟팅한 경우 프로필에 액세스하지 못하는 문제를 해결했습니다.

_통합_

* 트리거에 대해 만들어진 일부 데이터 소스가 올바르게 표시되고 선택되지 않는 문제를 해결했습니다.

_사용자 정의 리소스_

* 목록 화면에서 데이터 없이 사용자 지정 리소스 행을 표시할 수 있는 문제를 해결했습니다.
* &#39;False&#39; 값이 있는 부울 유형 필드가 사용자 지정 리소스에 표시되지 않는 문제를 해결했습니다.

## 릴리스 17.9 - 2017년 9월 {#release-17-9---september-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 전자 메일 서식 파일 라이브러리<br /> </td> 
   <td> 아스트로(Astro)와 페더(Feather)라는 두 가지 아름다운 테마로 디자인된 18가지의 새롭고 반응형 템플릿을 소개합니다. 사용자 정의 가능한 이러한 템플릿은 산업에 관계없이 사용할 수 있으며 즉시 사용할 수 있습니다. 템플릿에는 다양한 사용 사례에 대한 콘텐츠가 포함되어 있어 이메일 마케팅 캠페인을 보다 빠르고 효율적이며 아름답게 설계하고 전달할 수 있습니다.<br /> 자세한 내용은 <a href="../../designing/using/using-reusable-content.md#content-templates">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 프로필 데이터를 사용한 다이내믹 보고<br /> </td> 
   <td> Dynamic Reporting은 완전히 맞춤화가 가능하고 실시간 비즈니스 보고서를 제공합니다. 이 릴리스에서는 다이내믹 보고의 강력한 개선 사항이 프로필 데이터에 대한 액세스를 추가하여 열기 및 클릭과 같은 실용적인 이메일 캠페인 데이터 외에도 성별, 도시, 우편번호 및 연령 등의 프로필 차원별 인구 통계 분석을 활성화합니다. 사용하기 쉬운 동일한 드래그 앤 드롭 인터페이스를 사용하여 가장 중요한 고객 세그먼트에 대해 이메일 캠페인이 수행된 방식을 결정하는 것이 그 어느 때보다 쉽습니다.<br /> 자세한 내용은 <a href="../../reporting/using/about-dynamic-reports.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 원본 및 날짜가 <br />인 대량 구독 </td> 
   <td> 향상된 이 일괄 구독 기능을 통해 이제 워크플로우의 구독 서비스 활동을 통해 Adobe Campaign Standard 데이터베이스에 구독 정보(원본 및 날짜)를 직접 저장할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/subscription-services.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 일부 고객은 자신의 레코드를 식별하는 고유 키를 관리하지 않으므로 Adobe Campaign Standard에서 가져온 ID를 활용할 수 있어야 합니다. 이 ID(**ACS ID**)를 내보내고 데이터를 업데이트하는 동안 조정 키로 사용할 수 있습니다. 자세한 내용은 [세부 설명서](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)를 참조하세요.
* FTP 프로토콜은 더 이상 사용되지 않습니다. 이제 SFTP를 대신 사용해야 합니다. 기존 구현을 차단하지 않기 위해 FTP의 기존 구성은 이전과 동일하게 작동하지만 새 활동에 대해서는 옵션이 표시되지 않습니다.

_전자 메일, SMS 메시지 및 DM_

* 이제 게재 경고 알림에서 사용할 새 경고 기준을 만들 수 있습니다. 자세한 내용은 [세부 설명서](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion)를 참조하세요.
* 게재 경고 알림의 새로운 디자인과 게재 경고 대시보드 사용자 경험이 개선되었습니다.
* 이제 라우팅 외부 계정을 사용하지 않도록 설정하면 영향을 받는 게재(전자 메일, SMS 및 푸시)에 경고가 표시되고 **미리 보기** 단추가 이러한 게재에서 숨겨집니다.
* 제목 줄에 동적 텍스트가 활성화된 경우 이메일 콘텐츠에서 A/B 테스트의 미리 보기에 오류가 발생하는 문제를 해결했습니다.

_트랜잭션 메시지_

* 이제 트랜잭션 메시지를 보낸 후 3일 후와 같이 후속 메시지를 보낼 시기를 정의할 수 있습니다. 자세한 내용은 [세부 설명서](../../channels/using/follow-up-messages.md#sending-a-follow-up-message)를 참조하세요.
* 이제 이벤트에 연결된 트랜잭션 메시지를 보내야 하는 시작 날짜를 정의할 수 있습니다.
* 수신 및 처리된 이벤트에 연결된 프로필을 삭제한 후 후속 메시지가 포함된 워크플로우를 실행할 때 SQL 오류가 발생하는 문제를 해결했습니다.
* 이벤트에 연결된 프로필을 삭제할 수 없는 오류를 수정했습니다.
* 추적된 링크의 리디렉션이 작동하지 않는 문제를 해결했습니다.
* 이메일 또는 SMS 메시지에서 특정 링크에 대한 추적을 비활성화할 수 없는 문제를 해결했습니다.

_보고서_

* **핫 클릭** 보고서가 개선되었습니다. 또한 게재에 정의된 각 조건부 콘텐츠에 따라 핫 클릭을 표시하고 반복 게재 또는 트랜잭션 메시지의 각 실행에 대한 핫 클릭을 표시할 수 있습니다. 자세한 내용은 [세부 설명서](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion)를 참조하세요.
* 격리 지표가 올바른 데이터를 검색하지 못하는 문제를 해결했습니다.
* 달력 위젯에 사전 설정된 새 시간대가 추가되었습니다.
* 보다 일관성을 위해 [동적 보고서 지표](../../reporting/using/indicator-calculation.md) 및 [캠페인의 KPI](../../sending/using/confirming-the-send.md)(보낸 메시지의 대시보드에 표시됨)가 정렬되었습니다.
* Pipelined to crash on debian 7을 충돌을 야기할 수 있는 문제를 해결했습니다.

_워크플로_

* 가져온 파일 보존이 작동하지 않는 문제를 해결했습니다.

_통합_

* 이제 eVar 및 이벤트가 Analytics &amp; Campaign 통합에 대해 지원됩니다.
* 포기한 장바구니의 콘텐츠가 포함된 이메일을 보낼 때 장바구니에서 제거된 요소의 페이로드 매개 변수는 이제 선택 사항입니다.

_프로필 및 대상자_

* 이제 Adobe Campaign에서 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 정보용일 뿐이며, 청구에 직접적인 영향을 주지 않습니다. 자세한 내용은 [세부 설명서](../../audiences/using/active-profiles.md)를 참조하세요.
* 프로필 및 서비스 API를 사용할 때 프로필이 서비스를 구독할 수 없는 문제를 해결했습니다.

## 릴리스 17.7 - 2017년 7월 {#release-17-7---july-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 다국어 이메일 및 SMS 게재<br /> </td> 
   <td> 자동으로 세그먼트화된 고객의 선호 언어를 기반으로 하는 단일 게재를 통해 다국어 이메일 및 SMS 게재를 정의하고 실행할 수 있습니다. 언어 및 개인 수준에 대한 모든 게재의 성과를 보고합니다.<br /> 점점 더 많은 기업이 국내외에서 성장함에 따라 여러 언어로 콘텐츠를 전달해야 하는 어려움에 직면해 있습니다. 이와 같이 현지화된 메시지 전달을 간소화하는 것은 다국적 기업, 여러 언어를 사용하는 국가의 회사, 고객이 거주하는 지역에 상관없이 언어 수준에서 콘텐츠를 추가로 개인화하려는 회사를 위한 효과적인 고객 커뮤니케이션 전략의 핵심 부분입니다. 자세한 내용은 <a href="../../channels/using/creating-a-multilingual-email.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign 알림<br /> </td> 
   <td> Adobe Campaign Standard 내에서 직접 중요한 시스템 활동에 대한 알림을 받습니다. 예를 들어 진행 중인 게재의 진행 상황 또는 워크플로가 오류인 경우 알림을 받게 됩니다.<br /> 실시간 알림은 관련 이해 당사자에게 정보를 제공하고 애플리케이션 내에서 활동 알림을 즉시 직접 처리할 수 있는 기능을 사용자에게 제공합니다. 팀의 결과는 캠페인의 고급 민첩성, 효율성 및 더 원활한 실행입니다. 자세한 내용은 <a href="../../administration/using/sending-internal-notifications.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 게재 경고<br /> </td> 
   <td> 이제 Adobe Campaign에서는 Adobe Campaign Standard에서 직접 알림을 볼 수 있을 뿐만 아니라 중요한 시스템 활동의 사용자 또는 외부 관련자에게 이메일 경고를 트리거하는 이메일 경고 시스템도 제공합니다. 맞춤형 경고 및 대시보드를 생성, 관리 및 수신하여 게재 성공 또는 실패를 추적합니다.<br /> Adobe Campaign 게재 알림은 회사에 있는 모든 관련 Adobe Campaign 사용자에게 이메일 및 대시보드를 통해 게재 실행 상태에 대한 자동 알림을 제공하므로 효율성을 높입니다. 자세한 내용은 <a href="../../sending/using/receiving-alerts-when-failures-happen.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 데이터 원본 <br />의 암호화된 선언 ID </td> 
   <td> 암호화된 연락처 정보(이메일 주소 또는 전화번호)를 선언된 ID로 사용하여 Campaign에서 기존 프로필을 사용하지 않고 이메일 및 SMS 트리거를 보냅니다. 암호화된 선언 ID는 Adobe Campaign Standard에서 디코딩할 수 있으므로 Campaign은 이전에 알 수 없는 연락처가 포함된 다른 Experience Cloud 솔루션에서 대상을 받을 때 새로운 마케팅 가능한 프로필을 만들 수 있습니다.<br />은(는) 이메일 및 SMS를 통해 실시간으로 고객과 알 수 없는 잠재 고객을 타겟팅하여 기존 고객 기반의 충성도를 개선하고 새 고객을 각각 확보합니다. 잠재 고객이 Adobe Audience Manager에서 해당 인사이트를 인증하고 활용하면 자사 쿠키 데이터(Adobe Campaign*에서)를 최대한 활용할 수 있습니다. <br /> *Adobe Audience Manager이 필요합니다. 자세한 내용은 <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> Campaign에서 Analytics로 KPI 공유<br /> </td> 
   <td> Adobe Analytics과 캠페인 데이터를 공유하여 전환을 통한 다른 마케팅 및 광고 노력과 함께 Campaign의 이메일 마케팅 지표를 측정함으로써 사전 및 사후 클릭 행동을 통합합니다.<br /> 전체 성능을 직접 추적하고 Analytics의 외부 프로그램으로 시너지 효과를 확인합니다. 이 통합된 보기의 학습을 캠페인에 다시 적용하여, 궁극적으로 개방형, 클릭스루 및 전환율을 개선하여 매출과 전체 캠페인 성과를 높일 수 있습니다. <br /> Adobe Analytics이 필요합니다. 자세한 내용은 <a href="../../integrating/using/about-campaign-analytics-integration.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 다이렉트 메일 채널 - 발신자<br />에게 반송 </td> 
   <td> 이제 발신자에게 반송 정보를 통합하는 DM 공급자와의 플랫 파일 교환이 지원됩니다. DM 채널의 향상된 기능을 통해 해당 우편 주소를 향후 통신에서 제외할 수 있습니다.<br /> 이렇게 하면 마케터가 잘못된 주소를 통보받고 다른 채널을 통해 고객과 교류하거나 우편 주소를 업데이트하도록 유도할 수 있습니다. 또한 마케터가 잘못된 주소로 메일을 보내지 않으므로 마케팅 비용 낭비를 줄일 수 있습니다. <br /> DM을 추가 기능 채널로 사용할 수 있습니다. 자세한 내용은 <a href="../../channels/using/return-to-sender.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* 사용자가 목록을 내보낼 수 있는 문제를 해결했습니다. 이제 **[!UICONTROL Export]** 역할을 가진 사용자만 허용됩니다.

_전자 메일, SMS 메시지 및 DM_

* SMS 게재에 대해 **게재할** 표시기를 0으로 설정하는 **updateDeliveryExecInfo** 워크플로 문제를 해결했습니다.
* 이제 게재 템플릿 속성의 **고급 매개 변수**&#x200B;에서 **라우팅** 드롭다운 목록에 템플릿 메시지 유형에 해당하는 외부 계정만 표시됩니다. 예를 들어 이메일 게재 템플릿에는 이메일 외부 계정만 표시됩니다.
* 테스트 프로필에 대해 정의된 **[!UICONTROL Text]** 기본 전자 메일 형식 문제를 해결했습니다.
* 게재의 일정 정의 화면에서 기본 시간대를 선택할 때에서 Javascript 오류가 발생하는 문제를 수정했습니다.
* 전송 로그에 트랩이 표시되지 않는 문제를 해결했습니다.
* 게재 만들기 마법사의 템플릿 선택 화면에서 후속 및 A/B 테스트 템플릿은 이제 기본적으로 숨겨집니다. 자세한 내용은 [자세한 설명서](../../channels/using/creating-an-email.md)를 참조하세요.
* 모든 사용자가 게재를 보낼 수 있는 문제를 해결했습니다. 이제 **[!UICONTROL Start deliveries]** 역할을 가진 사용자만 허용됩니다. 자세한 내용은 [자세한 설명서](../../sending/using/confirming-the-send.md)를 참조하세요.

_푸시 알림_

* **Campaign 추적 끝점** URL에서 보고를 할 수 없는 문제를 해결했습니다.
* 푸시 알림 제목이 Android 디바이스에 표시되지 않는 문제를 해결했습니다.
* 푸시 알림에 제목만 포함되고 메시지 본문에 아무 것도 포함되지 않은 경우 푸시 알림이 iOS 디바이스에 표시되지 않는 문제를 해결했습니다.
* 게재에서 미디어 첨부 파일 URL을 추적하여 비디오와 사진을 게재에 포함할 수 없는 문제를 해결했습니다. 이제 푸시 알림에 대해 mediaAttachmentURL 유형의 URL 추적이 기본적으로 비활성화됩니다.

_보고서_

* 차트와 테이블 간에 값이 다르게 표시되는 문제가 수정되었습니다.
* 푸시 알림 값을 이메일 값으로 표시하는 문제를 해결했습니다.
* 캠페인 외부에서 게재를 만들 때 값을 알 수 없음으로 표시하는 문제를 해결했습니다.
* SMS 보고서 데이터를 모바일 애플리케이션 데이터로 표시하는 문제를 수정했습니다.

_워크플로_

* 이제 워크플로우 로그(기간 및 텍스트 검색)를 필터링할 수 있습니다. 자세한 내용은 [자세한 설명서](../../automating/using/monitoring-workflow-execution.md)를 참조하세요.
* 이제 전송 전에 확인을 비활성화하는 옵션을 워크플로우 게재에서 사용할 수 있습니다.
* 반복 게재 만들기 마법사에서 아웃바운드 전환을 설정할 수 없는 문제를 수정했습니다.
* 값이 많은 열거형으로 사용자 지정 리소스 필드를 기반으로 하는 워크플로우 쿼리 활동을 사용할 때 발생하는 문제를 해결했습니다

## 릴리스 17.5 - 2017년 5월 {#release-17-5---may-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> DM<br /> </td> 
   <td> Adobe Campaign Standard의 첫 번째 오프라인 채널인 DM을 통해 디지털 장벽을 깨고 물리적 세계로 연결합니다. 이 기능을 사용하면 DM 공급자가 크로스 채널 캠페인의 일부로 필요로 하는 파일을 개인화하고 생성할 수 있습니다. Dm을 활용하여 고객을 다시 참여시키거나 고객을 앱, 웹 사이트 또는 스토어로 유도하는 강력한 촉각 접점으로 고객 경험을 향상시키십시오.<br /> 자세한 내용은 <a href="../../channels/using/about-direct-mail.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 이메일 BCC<br /> </td> 
   <td> 이메일 BCC를 사용하면 개별 수신자에게 전송된 고유한 이메일 메시지를 저장할 수 있으므로 브랜드가 해당 메시지를 보관할 수 있습니다. Adobe Campaign Standard 고객은 모든 이메일에 BCC 이메일 주소를 추가하여 이 기능을 통해 각 이메일의 정확한 사본을 보관할 수 있습니다. 이는 금융 서비스 업계에서 일반적으로 요구되는 법적 요구 사항이며 고객 서비스 센터에서 실시간으로 갈등을 해결하는 데 도움이 됩니다.<br /> 자세한 내용은 <a href="../../sending/using/archiving.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_인터페이스 업데이트_

* 상단 표시줄에서 **[!UICONTROL Timeline]** 링크가 제거되고 **[!UICONTROL Programs & Campaigns]** 링크로 대체되었습니다.

_전자 메일 및 SMS 메시지_

* **[!UICONTROL Retry in progress]** 게재 상태에 대해 잘못된 색상을 표시하는 문제를 해결했습니다. 그 색깔은 파란색이 아니라 회색이었습니다.

_워크플로_

* **[!UICONTROL Transfer file]** 활동에서 수행할 작업을 변경할 때 발생하는 문제를 해결했습니다.

_보고서_

* **[!UICONTROL Spam]** 및 **[!UICONTROL Spam rate]** 표시기 계산이 변경되었습니다.
* 더 정확한 결과를 위해 **[!UICONTROL Bounce]** 지표가 개선되었습니다.

_푸시 알림_

* 프로필의 마케팅 기록에서 푸시 이벤트를 클릭할 수 없는 문제를 수정했습니다.
* 워크플로우에서 푸시 알림 사용이 개선되었습니다.

## 릴리스 17.4 - 2017년 4월 {#release-17-4---april-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Creative SDK의 이미지 편집 기능 향상<br /> </td> 
   <td> 이제 Creative SDK에서 제공하는 전체 기능 세트에 액세스하여 이메일 또는 랜딩 페이지를 편집할 때 콘텐츠 편집기에서 직접 이미지를 개선할 수 있습니다.<br /> 이 기능을 사용하려면 추가 Creative Cloud 솔루션을 가져올 필요가 없습니다.<br /> 자세한 내용은 <a href="../../designing/using/images.md#modifying-images-with-the-adobe-creative-sdk">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 푸시 알림<br /> </td> 
   <td> Adobe Campaign의 트랜잭션 메시지 기능에 모바일 애플리케이션 채널이 추가되었습니다. 트랜잭션 메시지에 대해 이메일, SMS 및 푸시 알림의 세 가지 채널이 지원됩니다.<br /> 자세한 내용은 <a href="../../channels/using/transactional-push-notifications.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 되풀이하는 푸시 알림<br /> </td> 
   <td> 이제 워크플로우에서 반복 푸시 알림을 구성할 수 있습니다. 고객이 새 콘텐츠 또는 프로모션을 확인하기 위해 주별 미리 알림과 같은 정기 업데이트를 기대하는 상황에서 반복 푸시 알림을 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/push-notification-delivery.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service(S3) 커넥터<br /> </td> 
   <td> 이제 Amazon Simple Storage Service(S3) 커넥터를 사용하여 데이터를 Adobe Campaign으로 가져오거나 내보낼 수 있습니다. 워크플로우 활동에서 설정할 수 있습니다. 구성은 외부 계정에서 수행됩니다.<br /> 자세한 내용은 <a href="../../administration/using/external-accounts.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver 통합 live<br /> </td> 
   <td> 이제 Adobe Campaign과 Dreamweaver 간의 통합이 라이브 상태가 되었습니다. 이제 Dreamweaver의 공식 마지막 릴리스 버전(17.0.2)과 함께 작동합니다.<br /> Adobe Campaign Integration Extension을 설치해야 합니다. 자세한 정보는 이 <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=ko">비디오</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 메모리 소모 문제를 해결했습니다.

_전자 메일 및 SMS 메시지_

* 메시지를 미리 볼 때 콘텐츠를 최신 변경 사항과 제대로 동기화할 수 없는 문제가 해결되었습니다.
* MX 또는 도메인 전자 메일 처리 규칙이 생성되거나 삭제되지 않는 문제를 해결했습니다.
* 여러 별칭이 있는 이메일을 보내지 못하는 문제를 해결했습니다.
* 트랩 게재 로그가 게재의 전송 로그에 표시되지 않는 문제를 해결했습니다.
* 콘텐츠에 URL이 없는 게재의 추적된 URL을 표시할 때 오류가 발생하는 문제를 해결했습니다.
* 보낸 메시지에서 이미지의 크기 특성이 올바르게 적용되지 않는 문제를 해결했습니다.

_트랜잭션 메시지_

* rtEventHistoId 필드가 트랜잭션 메시지 템플릿의 개인화 필드로 더 이상 노출되지 않습니다.

_랜딩 페이지_

* 랜딩 페이지에 사용되는 **[!UICONTROL by email]** 필터를 최적화하여 새 구독자를 데이터베이스 프로필과 조정합니다.
* 양식 구성에서 부울 필드를 사용할 때 확인란 대신 자유 텍스트 입력을 표시하는 문제를 해결했습니다.
* 랜딩 페이지 썸네일이 생성되지 않던 문제를 수정했습니다.

_워크플로_

* **[!UICONTROL End]** 또는 **[!UICONTROL External Signal]** 활동을 편집할 때 발생하는 표시 오류를 해결했습니다(Safari에서만).
* 잘못된 대상이 포함된 **[!UICONTROL Read Audience]** 활동을 편집할 때 표시되는 오류 메시지가 개선되었습니다.
* 구독 활동을 실행할 때 SQL 오류가 발생할 수 있는 문제를 수정했습니다.

_통합_

* 관심 영역 데이터: 위치 구독자를 계산할 때 발생하는 오류를 해결했습니다.

_대상 및 쿼리_

* 합계 및 평균 합계가 쿼리 편집기의 컬렉션에서 사용되지 않는 문제를 해결했습니다.
* 필터 리소스를 변경한 후 쿼리 편집기를 다시 로드할 수 없는 문제를 해결했습니다.

_보고서_

* 표에서 여러 행을 선택할 때 열람률 지표가 올바르게 계산되지 않는 문제를 해결했습니다.
* 지표만 정수 값으로 표시하는 오류를 수정했습니다. 이제 지표를 소수점과 함께 표시할 수 있습니다.

_푸시 알림_

* MCPNS에서 만들지 못한 모바일 앱에 연결된 Android 애플리케이션을 만들 때 오류 메시지가 표시되지 않던 문제를 수정했습니다.
* 사용자가 자동 알림에 사운드를 추가할 수 있는 문제를 해결했습니다.

## 릴리스 17.2 - 2017년 3월 {#release-17-2---march-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 동적 보고<br /> </td> 
   <td> Dynamic Reporting은 완전히 맞춤화가 가능한 새로운 세대의 실시간 비즈니스 보고서를 제공합니다. 이 기능을 사용하면 시각적 동적 피벗 테이블 및 그래픽을 기반으로 변수와 차원을 끌어서 놓아 마케팅 캠페인의 효율성과 효율성을 분석할 수 있습니다. 또한 동적 보고를 사용하면 비즈니스 보고서를 처음부터 직접 작성하고 나중에 사용할 수 있도록 저장할 수 있습니다.<br /> 자세한 내용은 <a href="../../reporting/using/about-dynamic-reports.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver 통합(Labs)<br /> </td> 
   <td> 이제 Adobe Campaign 및 Dreamweaver 통합을 통해 Adobe 솔루션을 사용하여 이메일 캠페인을 만들기 위한 통합 프로세스를 사용할 수 있습니다.<br /> Dreamweaver에서 Adobe Campaign 이메일을 편집하고 두 솔루션 간에 콘텐츠를 원활하게 동기화할 수 있습니다.<br /> 초기 릴리스의 경우 통합은 "Labs" 기능으로 사용할 수 있으며 Dreamweaver 프리릴리스 Beta에서만 작동합니다. 정품 인증을 받으려면 AC-DW-integration@adobe.com에 문의하십시오.<br /> 자세한 내용은 이 <a href="https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=ko">비디오</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 수동 전송 시간 최적화<br /> </td> 
   <td> 이제 게재 수준에서 또는 워크플로우를 사용하여 수신자당 사용자 지정 전송 시간을 수동으로 정의할 수 있습니다. <br /> 두 가지 새로운 옵션을 사용할 수 있습니다. <br /> 
    <ul> 
     <li> 모든 수신자는 시간대를 고려하여 메시지를 수신합니다. </li> 
     <li> 각 수신자는 수식으로 정의된 계산된 날짜 및 시간에 메시지를 수신합니다. </li> 
    </ul> 자세한 내용은 <a href="../../sending/using/optimizing-the-sending-time.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 푸시 알림 새로운 기능<br /> </td> 
   <td> 푸시 알림 채널이 다음과 같은 몇 가지 새로운 기능을 사용하여 향상되었습니다. <br /> 
    <ul> 
     <li> 새로운 작성 인터페이스 </li> 
     <li> 자동 알림 </li> 
     <li> 대화형 푸시 </li> 
     <li> 다양한 콘텐츠 지원 </li> 
     <li> 페이로드 크기 계산기 </li> 
    </ul> 자세한 내용은 <a href="../../channels/using/about-push-notifications.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 워크플로우: 새 신호 활동<br /> </td> 
   <td> 새 <span class="uicontrol">신호</span> 활동을 사용하여 다른 워크플로우에서 워크플로우를 트리거합니다.<br /> 이제 하나의 워크플로우를 다른 워크플로우에서 시작할 수 있으므로 보다 복잡한 고객 여정을 지원할 수 있습니다. 고객 여정을 보다 잘 모니터링하고 문제가 있을 경우 대응할 수 있습니다.<br /> 여러 워크플로우 활동이 업데이트되었습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">종료</span> 활동: 새 탭에서 이 활동이 실행된 후에 트리거할 워크플로우를 지정할 수 있습니다. </li> 
     <li> <span class="uicontrol">데이터 업데이트</span> 활동: 새로운 빈 아웃바운드 전환을 사용하여 다른 워크플로우를 트리거하는 <strong>End</strong> 활동을 추가합니다. 빈 아웃바운드 전환은 데이터를 전달하지 않으며, 시스템에서 불필요한 공간을 사용하지 않습니다. </li> 
    </ul> 자세한 내용은 <a href="../../automating/using/external-signal.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 워크플로우: 새로운 대상자 읽기 활동<br /> </td> 
   <td> 한 활동에서 쉽게 선택하고 세분화할 수 있는 기존 대상자로 타깃팅 프로세스를 시작합니다.<br /> 자세한 내용은 <a href="../../automating/using/read-audience.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 관심 영역 데이터<br /> </td> 
   <td> 관심 영역 데이터는 Adobe Campaign을 모바일용 Adobe Analytics과 통합합니다. 브랜드는 사용자가 브랜드의 앱을 열 때 사용자의 모바일 위치(<strong>관심 영역</strong>)에서 데이터를 수집할 수 있습니다. 이를 통해 브랜드는 Adobe Campaign 워크플로우를 활용하여 사용자의 위치를 기반으로 개인화된 메시지를 보낼 수 있습니다. 이 채널은 Mobile Core 서비스의 SDK를 활용합니다.<br /> 이 기능을 사용하려면 유료 솔루션인 Analytics for Mobile이 필요합니다.<br /> 자세한 내용은 <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> REST API<br /> </td> 
   <td> 이제 프로필 또는 서비스 리소스에 모든 수준에서 연결된 리소스를 API에서 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* 이제 게재 로그를 내보낼 때 프로필 데이터를 추가할 수 있습니다.

_전자 메일 및 SMS 메시지_

* 선택을 취소하고 게재를 저장한 후에도 **[!UICONTROL Request confirmation before sending messages]** 옵션이 선택된 상태로 유지되는 문제를 해결했습니다.
* 트랜잭션 전자 메일의 게시를 취소할 수 없는 문제를 해결했습니다.
* 게재를 미리 보기 전에 콘텐츠를 최신 변경 사항과 제대로 동기화할 수 없는 문제가 해결되었습니다.

_랜딩 페이지_

* 사용자가 랜딩 페이지의 콘텐츠를 클릭할 때 편집할 수 없는 오류를 수정했습니다.

_워크플로_

* **[!UICONTROL Load file]** 활동의 거부 전환 콘텐츠를 읽지 못하는 문제를 해결했습니다.
* **[!UICONTROL Load file]** 활동을 구성할 때 스왑된 열이 제대로 고려되지 않는 문제를 해결했습니다.

## 릴리스 17.1 - 2017년 1월 {#release-17-1---january-2017}

**새 기능**

<table> 
 <thead> 
  <tr> 
   <th> 기능<br /> </th> 
   <th> 설명<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 외부 보고에 대한 로그 내보내기<br /> </td> 
   <td> 게재 및 추적 로그와 같은 로그를 내보내 원하는 보고 또는 BI 도구에서 처리합니다. 증분 쿼리와 함께 간단한 워크플로우를 사용하여 새 로그의 정기적인 내보내기를 자동화할 수 있습니다.<br /> 리소스 선택기에서 로그 리소스를 사용할 수 있을 뿐만 아니라 <a href="../../automating/using/incremental-query.md">증분 쿼리</a> 및 <a href="../../automating/using/extract-file.md">파일 추출</a> 활동에 대한 기능이 향상되었습니다.<br /> 
    <ul> 
     <li> 이제 <span class="uicontrol">증분 쿼리</span>를 통해 날짜 필드를 사용하여 새 데이터나 업데이트된 데이터를 검색할 수 있습니다. 이전에는 마지막 실행 이후 업데이트된 경우에도 이전 실행의 모든 결과가 자동으로 제외되었습니다. </li> 
     <li> <span class="uicontrol">파일 추출</span>에서 이제 ID 대신 열거형 값에 대한 레이블을 내보낼 수 있습니다. </li> 
    </ul> 이러한 활동은 모든 지역 및 조직 단위에 액세스할 수 있는 관리자가 사용할 수 있습니다.<br /> 로그 내보내기에 대한 자세한 내용은 <a href="../../automating/using/exporting-logs.md">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지를 위한 마케팅 기능<br /> </td> 
   <td> 이제 마케터는 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다. 이렇게 하면 다음과 같은 작업을 수행할 수 있습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">차단 목록에 주소 지정</span> 과 같은 마케팅 토폴로지 규칙을 적용합니다. </li> 
     <li> 메시지에 구독 취소 링크를 포함합니다. </li> 
     <li> 트랜잭션 메시지를 글로벌 게재 보고서에 추가합니다. </li> 
     <li> 트랜잭션 메시지를 고객 여정에 활용합니다. </li> 
    </ul> 자세한 내용은 <a href="../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities">자세한 설명서</a>.<br />를 참조하세요. </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지 API<br /> </td> 
   <td> 이제 트랜잭션 메시지 API를 사용할 수 있으므로 사용 및 모니터링이 더 쉬워집니다.<br /> 
    <ul> 
     <li> Adobe Developer 플랫폼 보고 및 모니터링 기능을 활용할 수 있습니다. </li> 
     <li> 이제 IP 허용 목록에 추가 대신 adobe.io 토큰 기반 인증을 사용하여 인증이 수행되므로 보안 프로세스가 더 간단해집니다. </li> 
     <li> 이제 모든 API가 단일 플랫폼에서 통합되므로 프로필 및 서비스 API를 이미 지원하는 경우 그 어느 때보다 간단하게 통합에 트랜잭션 메시지 기능을 추가할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* **[!UICONTROL Access authorization]** 옵션이 랜딩 페이지 속성으로 돌아왔습니다.
* 올바른 이미지 대신 이전 이미지가 렌더링되는 문제를 해결했습니다. 이 문제는 소스 이미지가 게재 또는 랜딩 페이지의 콘텐츠 정의에서 업데이트된 경우에 발생했습니다.
* 사용자가 기존 SFTP 외부 계정의 특정 필드를 편집할 수 없는 문제를 해결했습니다.
* 여러 UI 문제가 해결되었습니다. 예를 들어 사용자는 이제 UI에 문제가 발생하지 않고 프로필 속성을 편집하고 수정 사항을 저장할 수 있습니다.

_전자 메일 및 SMS 메시지_

* 을(를) 포함하는 HTML 컨텐츠가 있는 게재 템플릿과 관련된 문제를 해결했습니다.

_푸시 알림_

* 애플리케이션에서 Adobe Campaign 서버로 포스트백하지 못하는 문제를 해결했습니다.
* Android에서 **[!UICONTROL Play a sound]** 및 **[!UICONTROL Custom fields]**&#x200B;을(를) 고려하지 못했을 수 있는 문제를 해결했습니다.
* 추가 이스케이프 문자가 이모지에 사용된 유니코드 문자에 추가되었을 수 있는 문제를 해결했습니다.
* 가입자 등록 토큰이 차단 목록에 추가하다에 추가되면 해당 상태가 이제 애플리케이션의 Adobe Campaign 가입자 목록에서 즉시 업데이트됩니다.

_워크플로_

* 이벤트 리소스(예: rtEvent)의 쿼리 미리보기를 방지할 수 있는 문제를 수정했습니다.
* **[!UICONTROL Load file]** 활동에서 생성된 거부 파일은 이제 아웃바운드 전환에서 검색하고 다음 활동에서 처리할 수 있습니다. 예를 들어 **[!UICONTROL Transfer file]** 을(를) 사용하여 SFTP 서버를 통해 거부 파일을 업로드합니다.
* **[!UICONTROL Segmentation]**&#x200B;의 **[!UICONTROL General]** 탭에서 **[!UICONTROL Temporary resource]**&#x200B;을(를) 선택한 경우 사용자가 세그먼트의 모집단을 제한할 수 없는 문제를 해결했습니다.
* 10분마다 두 번 이상 워크플로우를 트리거하도록 **[!UICONTROL Scheduler]** 활동을 설정할 수 없습니다.
* **[!UICONTROL Union]** 활동에서 **[!UICONTROL Use common columns]**&#x200B;이(가) 제대로 작동하지 않는 문제를 해결했습니다.

_통합_

* Adobe Campaign에서 이벤트 트리거를 배포할 때 오류가 발생했을 수 있는 문제를 해결했습니다. 이 오류는 &quot;30일 후에 반환될 가능성&quot; 메타데이터를 Adobe Marketing Cloud의 포기 트리거에 추가할 때 발생했습니다.
* People 핵심 서비스에서 대상을 가져올 때 기술 워크플로우가 Target Dimension 필드를 지우는 문제를 해결했습니다. 후속 쿼리에서 가져온 대상자를 검색할 수 없습니다.
* **[!UICONTROL Share in Adobe Marketing Cloud]** 옵션을 선택한 경우 워크플로우의 **[!UICONTROL Save audience]** 활동이 실패하는 문제를 해결했습니다.
