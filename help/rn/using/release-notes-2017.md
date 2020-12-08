---
solution: Campaign Standard
product: campaign
title: 2017년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2017년 릴리스가 모두 나열되어 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
translation-type: tm+mt
source-git-commit: a51943e4da04f5d19aaecdfcf956f5c4f3d804c8
workflow-type: tm+mt
source-wordcount: '4627'
ht-degree: 8%

---


# 2017년 릴리스 정보{#release-notes}

Adobe Campaign Standard의 2017 특정 릴리스를 찾고 계십니까?

각 릴리스에는 새로운 기능과 패치가 포함되어 있습니다. 해당 콘텐츠를 보려면 릴리스를 클릭하십시오.

Adobe Campaign Standard에 대한 최신 [설명서 업데이트](../../rn/using/documentation-updates.md)를 봅니다. 최신 릴리스를 원하는 경우 이 [페이지](../../rn/using/release-notes.md)를 참조하십시오.

## 릴리스 17.10 - 2017년 10월 {#release-17-10---october-2017}

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
   <td> 피로 관리<br /> </td> 
   <td> 피로 관리를 사용하면 피로 규칙을 만들어 프로필과의 과도한 커뮤니케이션을 관리할 수 있습니다. 피로 규칙은 쉽게 만들어지지만, 여러 채널(트랜잭션 메시지 포함)에서 메시지 카운트, 특정 전달 횟수 계산, 특정 프로필에 규칙 적용 등의 기능을 사용하면 매우 유연합니다.<br /> 자세한 내용은 <a href="../../sending/using/fatigue-rules.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 콘텐츠 제작:URL<br />에서 가져오기 </td> 
   <td> URL에서 가져오기를 사용하면 웹 사이트에서 크리에이티브 컨텐츠를 빠르게 검색하여 모든 배달에 사용할 이메일을 작성할 수 있습니다. 또한 제3자가 URL을 통해 직접 컨텐츠를 공유할 수 있도록 함으로써 크리에이티브 프로세스를 간소화할 수 있습니다. 가져온 컨텐츠는 단일 전달의 일부로 또는 템플릿 수준에서 유연하게 사용할 수 있으므로 워크플로우 기반 메시지나 트랜잭션 메시지 등 모든 관련 캠페인에 대한 브랜드 일관성을 보장하며 A/B 또는 다변량 테스트를 포함할 수 있습니다. URL에서 가져오기를 사용하면 모든 링크를 자동으로 변환하고 추적하여 Dynamic Reporting을 통해 이메일 성과를 모니터링합니다.<br /> 자세한 내용은 <a href="../../designing/using/using-existing-content.md#importing-content-from-a-url">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 큰 zip 파일의 압축이 올바르게 풀리지 않는 문제를 해결했습니다.
* 브랜드 관리의 보안이 개선되었습니다. 이제 Adobe 기술 관리자를 위해 브랜드 이름과 보낸 사람 주소 수정이 예약되었습니다.
* 보안을 개선하기 위해 사용자가 생성한 컨텐츠(이미지, 미러 페이지, 랜딩 페이지 등)를 adobe.com 도메인에서 더 이상 제공되지 않습니다. 이제 브랜딩 사용을 통해 자신의 도메인을 사용하여 이러한 리소스를 처리해야 합니다.
* 마케팅 활동을 표시하고 필터링할 때의 인터페이스 문제를 수정했습니다.
* 구독 날짜 필드가 POST Rest API 호출로 업데이트되지 않는 문제를 해결했습니다.

_이메일, SMS 메시지 및 DM_

* 메시지의 목록 유형 대상을 타깃팅하지 못하게 하여 준비가 실패했던 문제를 수정했습니다.
* 다국어 이메일 전달 기능에 추가된 언어가 없습니다.
* 이제 사용자가 컨텐츠를 수정하고 저장할 때 배달 대시보드에 표시되는 컨텐츠 축소판이 자동으로 업데이트됩니다.
* 배달을 열 수 없는 표준 시간대 관련 문제를 수정했습니다.

_푸시 알림_

* 푸시 알림 채널을 구성할 때 iOS용 푸시 공급자 플랫폼은 **apns**&#x200B;이고 Android **gcm**&#x200B;의 경우 이어야 합니다.
* iOS 모바일 앱이 Adobe Campaign 인터페이스에 추가되지 않던 문제를 수정했습니다.
* 이제 GCM 및 FCM이 활성화된 Android 모바일 응용 프로그램에서 푸시 알림이 지원됩니다.
* 푸시 알림 템플릿을 복제할 때 컨텐츠가 저장되지 않는 오류를 해결했습니다.
* 이제 모바일 애플리케이션 사용자의 데이터를 중재하여 Adobe Campaign 데이터베이스에서 프로파일을 만들거나 업데이트할 수 있습니다.
* 이제 Adobe Campaign은 표준 푸시 알림보다 트랜잭션 푸시 알림 처리를 우선 순위 지정합니다.

_보고서_

* 이메일 컨텐츠에 핫 클릭 비율이 표시되지 않던 문제를 수정했습니다.
* 바운스 대신 하드 바운스로 계산되는 지표 차단 목록 문제를 해결했습니다.
* 요약 데이터에 부정 카운트가 표시되는 문제를 해결했습니다.
* 잘못된 연령 세그먼트에서 프로필을 카운트했던 문제를 수정했습니다.
* 소프트 및 하드 바운스 계산 공식이 변경되었습니다.

_워크플로우_

* 활동에서 열을 수동으로 추가 및 제거한 후 오류가 발생할 수 있는 **[!UICONTROL Load file]** 활동 문제를 수정했습니다.
* 이제 **[!UICONTROL deliverabilityUpdate]** 기술 워크플로우는 서버 시간으로 오전 2시에 실행되도록 예약되었습니다.
* 내보내기 역할 없이 목록 내보내기를 수행할 수 있었던 보안 문제를 수정했습니다.
* **[!UICONTROL Reconciliation]** 활동 문제가 해결되었습니다.
* **[!UICONTROL File Transfer]** 활동에서 와일드카드 문자를 사용하는 문제가 해결되었습니다.

_프로필 및 대상자_

* 일부 특정 경우에 쿼리 조건이 올바로 고려되지 않아 오류가 발생하는 문제를 수정했습니다.
* 미리 준비했지만 전송되거나 만료되지 않은 메시지에서 프로필이 타깃팅된 경우 프로필에 액세스하지 못하게 하는 문제가 해결되었습니다.

_통합_

* 트리거를 위해 만든 일부 데이터 소스가 올바르게 표시되고 선택되지 않는 문제를 해결했습니다.

_사용자 정의 리소스_

* 데이터 없이 사용자 지정 리소스 행을 표시할 수 있는 목록 화면에서 발생하는 문제를 수정했습니다.
* 사용자 지정 리소스에 &#39;False&#39; 값이 있는 부울 형식 필드가 표시되지 않는 문제를 해결했습니다.

## 릴리스 17.9 - 2017년 9월 {#release-17-9---september-2017}

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
   <td> 이메일 템플릿 라이브러리<br /> </td> 
   <td> 아톰과 페더 등 두 가지 아름다운 테마로 디자인된 18개의 새로운 반응형 템플릿을 소개합니다. 이러한 사용자 정의 가능한 템플릿은 업계에 상관없이 즉시 사용할 수 있습니다. 템플릿에는 이메일 마케팅 캠페인을 보다 빠르고 효율적이며 아름답게 디자인하고 전달하기 위한 다양한 활용 사례를 위한 컨텐츠가 포함되어 있습니다.<br /> 자세한 내용은 <a href="../../designing/using/using-reusable-content.md#content-templates">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로필 데이터를 사용한 동적 보고<br /> </td> 
   <td> 동적 보고는 완벽하게 사용자 정의 가능하고 실시간 비즈니스 보고서를 제공합니다. 이번 릴리스에서는 동적 보고에 대한 강력한 향상된 기능이 프로필 데이터에 대한 액세스를 추가함으로써 열림 및 클릭과 같은 실용적인 이메일 캠페인 데이터 외에도 성별, 도시, 우편 번호 및 연령 등의 프로필 차원별 인구 통계 분석을 가능하게 합니다. 사용이 간편한 동일한 드래그 앤 드롭 인터페이스에서 가장 중요한 고객 세그먼트에 대해 이메일 캠페인을 수행하는 방법을 확인하는 것이 한결 수월해졌습니다.<br /> 자세한 내용은 <a href="../../reporting/using/about-dynamic-reports.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 출처 및 날짜가 있는 대량 가입<br /> </td> 
   <td> 이 대량 가입 개선 사항을 통해 이제 워크플로우의 가입 서비스 활동을 통해 Adobe Campaign Standard 데이터베이스에 가입 정보(출처 및 날짜)를 직접 저장할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/subscription-services.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 일부 고객은 고유한 키를 관리하지 않아 자신의 레코드를 식별하지 못하므로 Adobe Campaign Standard에서 제공하는 ID를 활용할 수 있어야 합니다. 이 ID(**ACS ID**)는 내보내거나 데이터를 업데이트하는 동안 조정 키로 사용할 수 있습니다. 자세한 내용은 [세부 설명서](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)를 참조하십시오.
* FTP 프로토콜은 더 이상 사용되지 않습니다. 이제 SFTP를 대신 사용해야 합니다. 기존 구현을 차단하지 않기 위해 FTP의 기존 구성은 이전과 같이 작동하지만 새 활동에 대해서는 옵션이 표시되지 않습니다.

_이메일, SMS 메시지 및 DM_

* 이제 전달 알림 시 사용할 수 있는 새 경고 기준을 만들 수 있습니다. 자세한 내용은 [세부 설명서](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion)를 참조하십시오.
* 전달 알림 알림에는 새로운 디자인이 적용되며 전달 알림 대시보드 사용자 경험이 향상되었습니다.
* 라우팅 외부 계정이 비활성화되면 영향을 받는 배달(이메일, SMS 및 푸시)에 경고가 표시되고 **미리 보기** 단추가 이러한 배달에서 숨겨집니다.
* 제목 줄에서 동적 텍스트를 활성화했을 때 이메일 컨텐츠에서 A/B 테스트 미리 보기에 오류가 발생했던 문제를 수정했습니다.

_트랜잭션 메시지_

* 이제 트랜잭션 메시지를 보낸 후 3일 등의 후속 메시지를 보낼 시기를 정의할 수 있습니다. 자세한 내용은 [세부 설명서](../../channels/using/follow-up-messages.md#sending-a-follow-up-message)를 참조하십시오.
* 이제 이벤트에 연결된 트랜잭션 메시지를 보낼 날짜를 정의할 수 있습니다.
* 수신 및 처리된 이벤트에 연결된 프로필을 삭제한 후 후속 메시지가 포함된 워크플로우를 실행할 때 SQL 오류가 발생하는 문제를 수정했습니다.
* 이벤트에 연결된 프로필을 삭제할 수 없는 오류가 수정되었습니다.
* 추적된 링크의 리디렉션이 작동하지 않는 문제를 해결했습니다.
* 이메일 또는 SMS 메시지의 특정 링크에 대한 추적을 비활성화하지 못하는 문제를 해결했습니다.

_보고서_

* **핫 클릭** 보고서가 개선되었습니다. 또한, 이제 게재에서 정의된 각 조건부 컨텐츠에 따라 핫 클릭을 표시할 수 있고 반복되는 게재나 트랜잭션 메시지의 각 실행에 대한 핫 클릭을 표시할 수 있습니다. 자세한 내용은 [세부 설명서](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion)를 참조하십시오.
* 격리 지표가 올바른 데이터를 검색하지 못하는 문제를 해결했습니다.
* 달력 위젯에 새로운 사전 설정 타임프레임이 추가되었습니다.
* [동적 보고서 지표](../../reporting/using/indicator-calculation.md) 및 [캠페인의 KPI](../../sending/using/confirming-the-send.md)(보낸 메시지 대시보드에 표시됨)가 보다 일관성 있게 정렬되었습니다.
* 이론적 7에서 파이프라인이 충돌을 야기할 수 있는 문제를 해결했습니다.

_워크플로우_

* 가져온 파일 보존 기능이 작동하지 않는 문제를 해결했습니다.

_통합_

* 이제 eVar 및 이벤트가 분석 및 캠페인 통합에 대해 지원됩니다.
* 중단된 장바구니의 컨텐츠가 포함된 이메일을 보낼 때 장바구니에서 제거된 요소에 대한 페이로드 매개 변수는 선택 사항입니다.

_프로필 및 대상자_

* 이제 Adobe Campaign에서 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 단지 유익할 뿐, 대금 청구에는 직접적인 영향을 주지 않습니다. 자세한 내용은 [세부 설명서](../../audiences/using/active-profiles.md)를 참조하십시오.
* 프로필 및 서비스 API를 사용할 때 프로필이 서비스에 가입되지 않던 문제를 수정했습니다.

## 릴리스 17.7 - 2017년 7월 {#release-17-7---july-2017}

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
   <td> 다국어 이메일 및 SMS 배달<br /> </td> 
   <td> 고객이 선호하는 언어를 자동으로 세분화하여 하나의 전달 방식을 통해 다국어 이메일 및 SMS 전달을 정의하고 실행할 수 있습니다. 언어 및 개인 수준에 대한 모든 게재의 성과를 보고합니다.<br /> 점점 더 많은 기업이 국내외에서 성장하면서 여러 언어로 컨텐츠를 전달하는 데 어려움을 겪고 있습니다. 이와 같이 로컬라이즈된 메시지 전달 과정을 간소화하는 것은 다국적 기업을 위한 효과적인 고객 커뮤니케이션 전략의 핵심입니다.여러 언어를 사용하는 국가의 기업고객이 거주하는 위치에 상관없이 고객의 컨텐츠를 언어 수준으로 개인화하고자 하는 기업 자세한 내용은 <a href="../../channels/using/creating-a-multilingual-email.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign 알림<br /> </td> 
   <td> Adobe Campaign Standard에서 바로 중요한 시스템 활동에 대한 알림을 받을 수 있습니다. 예를 들어 진행 중인 게재의 진행 상황이나 워크플로우가 잘못된 경우 알림을 받게 됩니다.<br /> 실시간 알림은 관련 이해 관계자에게 정보를 제공하고 사용자에게 애플리케이션 내에서 활동 알림에 즉시 대응할 수 있는 기능을 제공합니다. 팀은 민첩성, 효율성 및 원활한 캠페인 실행을 보장합니다. 자세한 내용은 <a href="../../administration/using/sending-internal-notifications.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달 경고<br /> </td> 
   <td> Adobe Campaign은 Adobe Campaign Standard에서 바로 알림을 볼 수 있을 뿐만 아니라 중요한 시스템 활동에 대한 사용자 또는 외부 이해 관계자에게 이메일 알림을 트리거하는 이메일 경고 시스템도 제공합니다. 사용자 정의 가능한 알림 및 대시보드를 만들고 관리 및 수신하여 전달 성공이나 실패를 추적할 수 있습니다.<br /> Adobe Campaign 전달 알림은 이메일 및 대시보드를 통해 회사의 Adobe Campaign 관련 모든 사용자에게 전달 진행 상태를 자동으로 알려 효율성을 높입니다. 자세한 내용은 <a href="../../sending/using/receiving-alerts-when-failures-happen.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 데이터 소스의 암호화된 등록 ID<br /> </td> 
   <td> 암호화된 연락처 정보(이메일 주소 또는 전화 번호)를 선언된 ID로 사용하여 Campaign에서 기존 프로필 없이도 이메일 및 SMS 트리거를 보낼 수 있습니다. 암호화된 등록 ID는 Adobe Campaign Standard에서 디코딩할 수 있으므로, Campaign은 이전에 알 수 없는 연락처가 포함된 다른 Experience Cloud 솔루션에서 대상을 수신할 때 새로운 마케팅 가능 프로파일을 만들 수 있습니다.<br /> 이메일 및 SMS를 통해 실시간으로 Target 고객과 알려지지 않은 잠재 고객을 확보하고 기존 고객층의 충성도를 높이고 신규 고객을 확보할 수 있습니다. 잠재 고객이 인증을 받고 Adobe Campaign에서 이러한 통찰력을 활용할 경우 Adobe Audience Manager*에서 자사 쿠키 데이터를 최대한 활용할 수 있습니다. <br /> *Adobe Audience Manager은 필수입니다. 자세한 내용은 <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign에서 Analytics로 KPI 공유<br /> </td> 
   <td> 캠페인 데이터를 Adobe Analytics과 공유하여 전환을 통한 다른 마케팅 및 광고 활동과 함께 Campaign의 이메일 마케팅 지표를 측정하여 사전 및 사후 클릭 행동을 통합할 수 있습니다.<br /> 전체 성과를 직접 추적하고 Analytics에서 외부 프로그램과의 시너지 효과를 확인할 수 있습니다. 통합 보기에서 얻은 학습을 캠페인에 다시 적용하십시오.궁극적으로 개방, 클릭률 및 전환율을 개선하여 매출 및 전체 캠페인 성과를 높일 수 있습니다. <br /> Adobe Analytics이 필요합니다. 자세한 내용은 <a href="../../integrating/using/about-campaign-analytics-integration.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> DM 채널 - 보낸 사람에게 돌아가기<br /> </td> 
   <td> 이제 보낸 사람에게 돌아가기 정보가 포함된 DM 공급자와의 일반 파일 교환이 지원됩니다. 이 개선 사항을 통해 향후 통신에서 해당 우편 주소를 제외할 수 있습니다.<br /> 이를 통해 마케터는 잘못된 주소로 통지를 받고 다른 채널을 통해 고객과 교류하거나 우편 주소를 업데이트하도록 권장할 수 있습니다. 따라서 마케터가 잘못된 주소로 메일을 보내지 않으므로 마케팅 비용이 낭비되는 횟수가 줄어듭니다. <br /> 다이렉트 메일은 추가 채널로 사용할 수 있습니다. 자세한 내용은 <a href="../../channels/using/return-to-sender.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* 모든 사용자 내보내기 목록을 허용하는 문제를 수정했습니다. 이제 **[!UICONTROL Export]** 역할을 가진 사용자만 사용할 수 있습니다.

_이메일, SMS 메시지 및 DM_

* **To deliver** 표시기를 SMS 배달용으로 0으로 설정하는 **updateDeliveryExecInfo** 워크플로 문제를 수정했습니다.
* 이제 배달 템플릿 속성의 **고급 매개 변수**&#x200B;에서 **라우팅** 드롭다운 목록에는 템플릿 메시지 유형에 해당하는 외부 계정만 표시됩니다. 예를 들어 이메일 배달 템플릿은 이메일 외부 계정만 표시합니다.
* 테스트 프로필에 대해 정의된 **[!UICONTROL Text]** 기본 이메일 형식 문제를 수정했습니다.
* 게재의 예약 정의 화면에서 기본 시간대를 선택할 때 Javascript 오류가 발생하던 문제를 수정했습니다.
* 전송 로그에 트랩이 표시되지 않던 문제를 수정했습니다.
* 이제 배달 만들기 마법사의 템플릿 선택 화면에서 후속 및 A/B 테스트 템플릿이 기본적으로 숨겨집니다. 자세한 내용은 [자세한 문서](../../channels/using/creating-an-email.md)를 참조하십시오.
* 모든 사용자가 배달을 보낼 수 있는 문제를 수정했습니다. 이제 **[!UICONTROL Start deliveries]** 역할을 가진 사용자만 사용할 수 있습니다. 자세한 내용은 [자세한 문서](../../sending/using/confirming-the-send.md)를 참조하십시오.

_푸시 알림_

* 보고할 수 없는 **캠페인 추적 끝점** URL과 관련된 문제를 수정했습니다.
* 푸시 알림 제목이 Android 장치에 표시되지 않던 문제를 수정했습니다.
* 푸시 알림에 제목만 포함된 경우(메시지 본문에 아무 것도 없는 경우) iOS 장치에 푸시 알림이 표시되지 않던 문제를 수정했습니다.
* 게재 시 미디어 첨부 URL을 추적해야 하는 문제를 해결했습니다. 이로 인해 비디오 및 그림이 전달에 포함되지 않았습니다. 이제 미디어 첨부 파일 URL 유형의 URL 추적은 푸시 알림에 대해 기본적으로 비활성화됩니다.

_보고서_

* 차트와 테이블 간에 값이 다르게 나타나는 문제를 수정했습니다.
* 푸시 알림 값이 이메일 값으로 표시되는 문제를 수정했습니다.
* 캠페인 외부에서 배달을 만들 때 값을 알 수 없음을 표시하는 문제를 해결했습니다.
* SMS 보고서 데이터를 모바일 애플리케이션 데이터로 표시하는 문제를 수정했습니다.

_워크플로우_

* 이제 워크플로우 로그(기간 및 텍스트 검색)를 필터링할 수 있습니다. 자세한 내용은 [자세한 문서](../../automating/using/monitoring-workflow-execution.md)를 참조하십시오.
* 이제 전송 전에 확인을 비활성화하기 위해 워크플로우 배달에서 옵션을 사용할 수 있습니다.
* 반복 게재 생성 마법사에서 아웃바운드 전환을 설정하지 못하는 문제를 해결했습니다.
* 값이 많은 사용자 지정 리소스 필드를 기반으로 하는 워크플로 쿼리 활동을 사용할 때 발생하던 문제가 해결되었습니다.

## 릴리스 17.5 - 2017년 5월 {#release-17-5---may-2017}

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
   <td> DM<br /> </td> 
   <td> 디지털 장벽을 넘어 Adobe Campaign Standard의 첫 오프라인 채널인 DM을 통해 물리적 세계에 연결할 수 있습니다. 이 기능을 사용하면 크로스채널 캠페인의 일부로 DM 제공업체가 요구하는 파일을 개인화하고 생성할 수 있습니다. DM을 활용하여 고객의 재참여를 유도하거나 고객을 앱, 웹 사이트 또는 스토어로 유도할 수 있는 매력적인 촉매로 고객 경험을 향상시킬 수 있습니다.<br /> 자세한 내용은 <a href="../../channels/using/about-direct-mail.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 이메일 BCC<br /> </td> 
   <td> 이메일 BCC를 사용하면 개별 받는 사람에게 보낸 고유한 이메일 메시지를 저장할 수 있으므로 해당 메시지를 브랜드에서 보관할 수 있습니다. 모든 이메일에 숨은 참조 이메일 주소를 추가하면 Adobe Campaign Standard 고객은 이 기능을 사용하여 각 이메일의 정확한 사본을 보관할 수 있습니다. 이는 금융 서비스 업계의 일반적인 법적 요구 사항이며 고객 서비스 센터에서 실시간으로 분쟁을 해결하는 데 도움이 됩니다.<br /> 자세한 내용은 <a href="../../sending/using/archiving.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_인터페이스 업데이트_

* 상단 막대에서 **[!UICONTROL Timeline]** 링크가 제거되고 **[!UICONTROL Programs & Campaigns]** 링크로 대체되었습니다.

_이메일 및 SMS 메시지_

* **[!UICONTROL Retry in progress]** 배달 상태에 대해 잘못된 색상을 표시하는 문제를 수정했습니다. 그 색깔은 파란색이 아니라 회색이다.

_워크플로우_

* **[!UICONTROL Transfer file]** 활동에서 수행할 작업을 변경할 때 발생하는 문제를 수정했습니다.

_보고서_

* **[!UICONTROL Spam]** 및 **[!UICONTROL Spam rate]** 표시기 계산이 변경되었습니다.
* 보다 정확한 결과를 위해 **[!UICONTROL Bounce]** 지표가 개선되었습니다.

_푸시 알림_

* 프로필의 마케팅 내역에서 푸시 이벤트를 클릭할 수 없는 문제를 해결했습니다.
* 워크플로우에서 푸시 알림 사용이 개선되었습니다.

## 릴리스 17.4 - 2017년 4월 {#release-17-4---april-2017}

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
   <td> Creative SDK<br />의 향상된 이미지 에디션 기능 </td> 
   <td> 이제 이메일이나 랜딩 페이지를 편집할 때 컨텐츠 편집기에서 바로 이미지를 향상시킬 수 있는 Creative SDK 기반의 완벽한 기능을 이용할 수 있습니다.<br /> 이 기능은 추가 Creative Cloud 솔루션을 획득할 필요가 없습니다.<br /> 자세한 내용은 <a href="../../designing/using/images.md#modifying-images-with-the-adobe-creative-sdk">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 푸시 알림<br /> </td> 
   <td> 모바일 응용 프로그램 채널이 Adobe Campaign의 트랜잭션 메시징 기능에 추가되었습니다. 이제 트랜잭션 메시지에 대해 세 개의 채널이 지원됩니다.이메일, SMS 및 푸시 알림<br /> 자세한 내용은 <a href="../../channels/using/transactional-push-notifications.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 반복 푸시 알림<br /> </td> 
   <td> 이제 워크플로우에서 반복되는 푸시 알림을 구성할 수 있습니다. 고객이 주별 미리 알림과 같은 정기 업데이트를 기대하는 경우 새로운 컨텐츠 또는 프로모션을 확인할 수 있는 반복 푸시 알림을 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/push-notification-delivery.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service (S3) 커넥터<br /> </td> 
   <td> 이제 Amazon Simple Storage Service (S3) 커넥터를 사용하여 데이터를 Adobe Campaign으로 가져오거나 내보낼 수 있습니다. 워크플로우 활동에서 설정할 수 있습니다. 구성은 외부 계정에서 수행됩니다.<br /> 자세한 내용은 <a href="../../administration/using/external-accounts.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver 통합 live<br /> </td> 
   <td> Adobe Campaign과 Dreamweaver의 통합이 지금 생방송이다. 현재 이 제품은 공식적으로 최근 출시된 Dreamweaver 버전(17.0.2)과 연동됩니다.<br /> 이를 위해서는 다음 위치에서 Adobe Campaign 통합 익스텐션을 설치해야 합니다. <a href="https://adobe.ly/acdw_addon">https://adobe.ly/acdw_</a><br /> addon자세한 내용은 이  <a href="https://docs.adobe.com/content/help/ko-KR/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html">비디오를 참조하십시오</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_플랫폼_

* 메모리 사용 문제가 해결되었습니다.

_이메일 및 SMS 메시지_

* 메시지를 미리 볼 때 콘텐츠가 최신 변경 사항과 제대로 동기화되지 않는 문제가 해결되었습니다.
* MX 또는 도메인 이메일 처리 규칙을 만들거나 삭제할 수 없는 문제를 해결했습니다.
* 여러 별칭으로 이메일을 보내지 못하는 문제를 해결했습니다.
* 배달 전송 로그에 트랩 배달 로그가 표시되지 않는 문제를 해결했습니다.
* 컨텐츠에 URL이 없는 게재의 추적된 URL을 표시할 때 오류가 발생하던 문제를 수정했습니다.
* 보낸 메시지에 이미지의 크기 속성이 올바르게 적용되지 않는 문제를 해결했습니다.

_트랜잭션 메시지_

* 트랜잭션 메시지 템플릿에서 rtEventHistoId 필드가 더 이상 개인화 필드로 노출되지 않습니다.

_랜딩 페이지_

* 랜딩 페이지에 사용되는 **[!UICONTROL by email]** 필터를 최적화하여 새 가입자를 데이터베이스 프로필로 조정합니다.
* 양식 구성에서 부울 필드를 사용할 때 확인란 대신 무료 텍스트 입력 내용을 표시하는 문제를 해결했습니다.
* 랜딩 페이지 축소판을 생성할 수 없는 문제를 해결했습니다.

_워크플로우_

* **[!UICONTROL End]** 또는 **[!UICONTROL External Signal]** 활동(Safari에만 해당)을 편집할 때 발생하는 표시 오류를 수정했습니다.
* 잘못된 대상이 포함된 **[!UICONTROL Read Audience]** 활동을 편집할 때 표시되는 오류 메시지를 개선했습니다.
* 구독 활동을 실행할 때 SQL 오류가 발생하던 문제를 수정했습니다.

_통합_

* 관심 영역 데이터:위치 가입자를 계산할 때 발생하는 오류가 수정되었습니다.

_대상 및 쿼리_

* 쿼리 편집기의 컬렉션에서 합계 및 평균 집계가 사용되지 않는 문제를 해결했습니다.
* 필터 리소스를 변경한 후 쿼리 편집기가 다시 로드되지 않는 문제를 해결했습니다.

_보고서_

* 테이블에서 여러 행을 선택할 때 개방 비율 지표가 올바르게 계산되지 않는 문제를 해결했습니다.
* 지표만 정수 값으로 표시하는 오류를 수정했습니다. 이제 지표를 소수 단위로 표시할 수 있습니다.

_푸시 알림_

* MCPNS에서 만들지 못한 모바일 앱에 연결된 Android 응용 프로그램을 만들 때 오류 메시지가 표시되지 않는 문제가 해결되었습니다.
* 사용자가 자동 알림에 사운드를 추가할 수 있었던 문제를 수정했습니다.

## 릴리스 17.2 - 2017년 3월 {#release-17-2---march-2017}

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
   <td> 동적 보고<br /> </td> 
   <td> 동적 보고는 완전히 사용자 정의 가능한 실시간 비즈니스 보고서의 새로운 세대를 제공합니다. 시각적인 동적 피벗 테이블 및 그래픽을 기반으로, 이 기능을 사용하면 변수 및 차원을 드래그하여 놓아 마케팅 캠페인의 효율성과 효과를 분석할 수 있습니다. 또한 동적 보고를 사용하면 고유한 비즈니스 보고서를 처음부터 만들고 나중에 사용할 수 있도록 저장할 수 있습니다.<br /> 자세한 내용은 <a href="../../reporting/using/about-dynamic-reports.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dreamweaver 통합(랩)<br /> </td> 
   <td> 이제 Adobe Campaign과 Dreamweaver의 통합을 통해 Adobe 솔루션을 사용하여 이메일 캠페인을 만드는 통합 프로세스를 경험할 수 있습니다.<br /> Dreamweaver에서 Adobe Campaign 이메일을 편집하고 두 솔루션 간에 컨텐츠를 완벽하게 동기화할 수 있습니다.<br /> 초기 릴리스의 경우 통합을 "Labs" 기능으로 사용할 수 있으며 Dreamweaver 시험판 베타에서만 작동합니다. 정품 인증을 받으려면 AC-DW-integration@adobe.com으로 문의하십시오.<br /> 자세한 내용은 이  <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/email-designer/dreamweaver-integration.html">비디오를 참조하십시오</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> 수동 전송 시간 최적화<br /> </td> 
   <td> 이제 배달 수준에서 또는 워크플로우를 사용하여 수신자당 사용자 지정 전송 시간을 수동으로 정의할 수 있습니다. <br /> 두 가지 새로운 옵션을 사용할 수 있습니다.  <br /> 
    <ul> 
     <li> 모든 수신자는 시간대를 고려하여 메시지를 수신합니다. </li> 
     <li> 각 수신자는 공식에 의해 정의된 계산된 날짜와 시간에 메시지를 받습니다. </li> 
    </ul> 자세한 내용은 <a href="../../sending/using/optimizing-the-sending-time.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 푸시 알림 새로운 기능<br /> </td> 
   <td> 푸시 알림 채널은 다음과 같은 몇 가지 새로운 기능으로 개선되었습니다.<br /> 
    <ul> 
     <li> 새로운 작성 인터페이스 </li> 
     <li> 자동 알림 </li> 
     <li> 인터랙티브한 푸시 </li> 
     <li> 리치 컨텐츠 지원 </li> 
     <li> 페이로드 크기 계산기 </li> 
    </ul> 자세한 내용은 <a href="../../channels/using/about-push-notifications.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:새 신호 활동<br /> </td> 
   <td> 새 <span class="uicontrol">Signal</span> 활동을 사용하여 다른 워크플로우의 워크플로우를 트리거합니다.<br /> 이제 다른 워크플로우에서 워크플로우를 시작할 수 있으므로 보다 복잡한 고객 여정을 지원할 수 있습니다. 고객 여정을 모니터링하고 문제가 있을 경우 대응할 수 있습니다.<br /> 몇 가지 워크플로우 활동이 업데이트되었습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">미달 </span> 활동:새 탭에서는 이 활동이 실행된 후 트리거할 워크플로우를 지정할 수 있습니다. </li> 
     <li> <span class="uicontrol">데이터 </span> 활동 업데이트:새로운 빈 아웃바운드 전환을 사용하여 다른 워크플로우를 트리거하는  <strong></strong> Endactivity를 추가합니다. 빈 아웃바운드 전환은 데이터를 포함하지 않으며 시스템에서 불필요한 공간을 사용하지 않습니다. </li> 
    </ul> 자세한 내용은 <a href="../../automating/using/external-signal.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 워크플로우:새로운 대상 활동 읽기<br /> </td> 
   <td> 하나의 활동에서 손쉽게 선택하고 조정할 수 있는 기존 고객으로 타깃팅 프로세스를 시작할 수 있습니다.<br /> 자세한 내용은 <a href="../../automating/using/read-audience.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 관심 영역 데이터<br /> </td> 
   <td> 관심 영역 데이터는 Adobe Campaign과 모바일용 Adobe Analytics을 통합합니다. 브랜드는 사용자가 브랜드의 앱을 열 때 사용자의 모바일 위치(<strong>관심 영역</strong>)에서 데이터를 수집할 수 있습니다. 이를 통해 브랜드는 Adobe Campaign 워크플로우를 활용하여 사용자의 위치를 기반으로 개인화된 메시지를 보낼 수 있습니다. 이 채널은 Mobile 코어 서비스의 SDK를 활용합니다.<br /> 이 기능을 사용하려면 유료 솔루션인 Analytics for Mobile이 필요합니다.<br /> 자세한 내용은 <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> REST API<br /> </td> 
   <td> 이제 모든 수준에서 프로필 또는 서비스 리소스에 연결된 리소스를 API에서 사용할 수 있습니다.<br /> 자세한 내용은 <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* 이제 배달 로그를 내보낼 때 프로필 데이터를 추가할 수 있습니다.

_이메일 및 SMS 메시지_

* **[!UICONTROL Request confirmation before sending messages]** 옵션이 선택을 취소하고 배달을 저장한 후에도 선택된 상태로 유지되는 문제를 수정했습니다.
* 거래 이메일의 게시 취소를 방지할 수 있는 문제를 수정했습니다.
* 배달을 미리 보기 전에 최신 변경 사항과 컨텐츠를 제대로 동기화할 수 없는 문제가 해결되었습니다.

_랜딩 페이지_

* 사용자가 랜딩 페이지의 내용을 클릭할 때 편집되지 않던 오류를 수정했습니다.

_워크플로우_

* **[!UICONTROL Load file]** 활동의 거부 전환 콘텐츠를 읽지 못하는 문제를 해결했습니다.
* **[!UICONTROL Load file]** 활동을 구성할 때 교환된 열이 제대로 고려되지 않는 문제를 해결했습니다.

## 릴리스 17.1 - 2017년 1월 {#release-17-1---january-2017}

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
   <td> 외부 보고용 로그 내보내기<br /> </td> 
   <td> 배달 로그 및 추적 로그와 같은 로그를 내보내 원하는 보고 또는 BI 툴에서 처리할 수 있습니다. 증분 쿼리가 있는 간단한 워크플로우를 사용하여 새 로그의 일반적인 내보내기를 자동화할 수 있습니다.<br /> 리소스 선택기에서 사용할 수 있는 로그 리소스 외에도 증분 쿼리 및 파일  <a href="../../automating/using/incremental-query.md">추출 </a> 활동이  <a href="../../automating/using/extract-file.md"> </a> 향상되었습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">이제 증분 </span> 쿼리를 통해 날짜 필드를 사용하여 새 데이터나 업데이트된 데이터를 검색할 수 있습니다. 이전에는 마지막 실행 이후 업데이트된 경우에도 이전 처형의 모든 결과가 자동으로 제외되었습니다. </li> 
     <li> <span class="uicontrol">이제 추출 </span> 파일에서 ID 대신 열거형 값에 대한 레이블을 내보낼 수 있습니다. </li> 
    </ul> 이러한 활동은 모든 지역 및 조직 단위에 대한 액세스 권한이 있는 관리자가 사용할 수 있습니다.<br /> 로그 내보내기에 대한 자세한 내용은  <a href="../../automating/using/exporting-logs.md">자세한 설명서를 참조하십시오</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지에 대한 마케팅 기능<br /> </td> 
   <td> 이제 마케터는 고객 마케팅 프로필을 기반으로 트랜잭션 메시지를 보낼 수 있습니다. 이를 통해 다음과 같은 작업을 수행할 수 있습니다.<br /> 
    <ul> 
     <li> <span class="uicontrol">주소와 같은 차단 목록 마케팅 유형 규칙을 적용합니다.</span> </li> 
     <li> 메시지에 구독 취소 링크를 포함합니다. </li> 
     <li> 트랜잭션 메시지를 글로벌 게재 보고서에 추가합니다. </li> 
     <li> 트랜잭션 메시지를 고객 여정에 활용합니다. </li> 
    </ul> 자세한 내용은 <a href="../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities">세부 설명서</a>를 참조하십시오.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 메시지 API<br /> </td> 
   <td> 이제 <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">adobe.io</a>를 통해 트랜잭션 메시지 API를 사용할 수 있으므로 사용하고 모니터링하기가 더 쉽습니다.<br /> 
    <ul> 
     <li> adobe.io 플랫폼 보고 및 모니터링 기능을 활용할 수 있습니다. </li> 
     <li> 이제 IP 허용 목록에 추가 대신 adobe.io 토큰 기반 인증을 사용하여 인증이 수행되므로 보안 프로세스가 더욱 간소화됩니다. </li> 
     <li> 모든 API는 이제 단일 플랫폼에 통합되어 있으므로 프로필 및 서비스 API를 이미 지원하는 경우 트랜잭션 메시징 기능을 통합에 추가하는 것이 한결 수월해졌습니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**패치**

_일반_

* **[!UICONTROL Access authorization]** 옵션이 랜딩 페이지 속성으로 돌아왔습니다.
* 올바른 이미지 대신 이전 이미지가 렌더링되는 문제를 수정했습니다. 배달 또는 랜딩 페이지의 컨텐츠 정의에서 소스 이미지가 업데이트된 경우 이 문제가 발생했습니다.
* 사용자가 기존 SFTP 외부 계정의 특정 필드를 편집할 수 없는 문제를 해결했습니다.
* 여러 UI 문제가 해결되었습니다. 예를 들어, 사용자는 이제 UI에 문제가 발생하지 않고 프로필 속성을 편집하고 수정 사항을 저장할 수 있습니다.

_이메일 및 SMS 메시지_

* HTML 콘텐츠가 포함된 배달 템플릿과 관련된

_푸시 알림_

* 애플리케이션에서 Adobe Campaign 서버로 포스트백을 보낼 수 없는 문제를 수정했습니다.
* Android에 대해 **[!UICONTROL Play a sound]** 및 **[!UICONTROL Custom fields]**&#x200B;을(를) 고려하지 않았던 문제를 수정했습니다.
* Emojis에 사용되는 유니코드 문자에 추가 이스케이프 문자가 추가되었을 수 있는 문제를 수정했습니다.
* 가입자의 등록 토큰이에 차단 목록 추가되면 해당 상태가 Adobe Campaign에 있는 애플리케이션의 가입자 목록에서 즉시 업데이트됩니다.

_워크플로우_

* 이벤트 리소스(예: rtEvent)에 대한 쿼리 미리 보기가 되지 않았던 문제를 수정했습니다.
* 이제 **[!UICONTROL Load file]** 활동에서 생성된 거부 파일을 아웃바운드 전환 중에 검색하여 다음 활동에서 처리할 수 있습니다. 예를 들어 **[!UICONTROL Transfer file]**&#x200B;을(를) 사용하여 SFTP 서버를 통해 거부 파일을 업로드합니다.
* **[!UICONTROL Segmentation]**&#x200B;의 **[!UICONTROL General]** 탭에서 **[!UICONTROL Temporary resource]**&#x200B;을 선택한 경우 사용자가 세그먼트 모집단을 제한하지 못했던 문제를 수정했습니다.
* **[!UICONTROL Scheduler]** 10분마다 한 번 이상 워크플로우를 트리거하도록 활동을 설정할 수 없습니다.
* **[!UICONTROL Use common columns]**&#x200B;이(가) **[!UICONTROL Union]** 활동에서 제대로 작동하지 않던 문제를 수정했습니다.

_통합_

* Adobe Campaign에서 이벤트 트리거를 배포할 때 오류가 발생하던 문제를 수정했습니다. 이 오류는 &quot;30일 후 반환 가능성&quot; 메타데이터가 Adobe Marketing Cloud의 포기 트리거에 추가되었을 때 발생했습니다.
* 사람 핵심 서비스에서 대상을 가져올 때 기술 워크플로가 Target Dimension 필드를 지우는 문제를 해결했습니다. 이후 쿼리는 가져온 대상을 검색할 수 없습니다.
* **[!UICONTROL Share in Adobe Marketing Cloud]** 옵션을 선택하면 워크플로우의 **[!UICONTROL Save audience]** 활동이 실패했을 수 있는 문제를 수정했습니다.

