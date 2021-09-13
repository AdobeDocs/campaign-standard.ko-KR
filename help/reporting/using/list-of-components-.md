---
title: '구성 요소 목록 '
description: 여기에서 사용 가능한 모든 구성 요소 목록을 확인하십시오     동적 보고서 및 정의를 참조하십시오.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: 8980bf05-60a8-4360-a354-445e1faeb5b2
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 1%

---

# 구성 요소 목록 {#list-of-components}

차원과 지표 간의 호환성에 대한 자세한 내용은 이 [표](/help/reporting/using/assets/dynamic_report_compatibility.pdf)를 참조하십시오. 두 구성 요소가 호환되지 않으면 **None** 값이 셀에 표시됩니다.

[![이미지](assets/dynamic_report_compatibility.png)](https://experienceleague.adobe.com/docs/campaign-standard/assets/dynamic_report_compatibility.pdf?lang=en)

## Dimension {#dimensions}

아래 표는 보고서에 사용된 차원 목록과 해당 정의를 제공합니다.

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 브라우저<br /> </td> 
   <td> 메시지를 열거나 클릭한 브라우저입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 캠페인<br /> </td> 
   <td> 캠페인의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> City<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 도시입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 국가/지역<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 국가입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 게재<br /> </td> 
   <td> 게재의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> Device<br /> </td> 
   <td> 전자 메일/SMS/푸시 알림이 열리거나 보거나 클릭한 장치입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 실패 이유<br /> </td> 
   <td> 각 게재에 대한 반송(예: 사용자 알 수 없음, 잘못된 도메인 또는 사서함이 가득 찬 오류 유형.<br />) </td> 
  </tr> 
  <tr> 
   <td> Gender<br /> </td> 
   <td> 수신자의 성별(예: 남성 또는 여성). 수신자 프로필에 성별 필드가 비어 있으면 값은 none이 됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 메시지 작업<br /> </td> 
   <td> 전달된 인앱 메시지에 대한 작업(예: 단추 1 또는 2의 작업 또는 취소).<br /> </td> 
  </tr> 
  <tr> 
   <td> 메시지 유형<br /> </td> 
   <td> 게재에 사용되는 채널(예: 이메일, SMS, 푸시 알림 또는 인앱)입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모바일 앱 이름<br /> </td> 
   <td> 모바일 응용 프로그램의 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 플랫폼<br /> </td> 
   <td> 메시지가 열리거나 보거나 클릭한 장치의 플랫폼입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로필<br /> </td> 
   <td> 프로필 리소스 확장 중에 만들어진 사용자 지정 프로필 필드와 기본 프로필을 다시 그룹화합니다. 자세한 내용은 이 <a href="../../developing/using/key-steps-to-add-a-resource.md">page</a> 또는 이 <a href="../../reporting/using/creating-a-custom-profile-dimension.md">예제</a>를 참조하십시오.<br /> 이 차원에 대한 데이터는 프로필 필드에 연결된 사용자 지정 리소스가 게시되는 즉시 검색됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 푸시 플랫폼<br /> </td> 
   <td> 푸시 알림이 열린 장치의 플랫폼(예: iOS 또는 Android)입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 받는 사람 도메인<br /> </td> 
   <td> 전자 메일을 여는 데 사용되는 도메인입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 반복 게재<br /> </td> 
   <td> 반복 배달의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 보낸 사람 도메인<br /> </td> 
   <td> 전자 메일을 보내는 데 사용되는 도메인입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 보낸 사람 IP<br /> </td> 
   <td> 전자 메일을 보내는 데 사용되는 IP입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 상태<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 상태입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL<br /> </td> 
   <td> 메시지에서 사용자가 클릭한 URL입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL 카테고리<br /> </td> 
   <td> 추적 URL에 지정된 카테고리입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL 레이블<br /> </td> 
   <td> 미러 페이지와 같이 URL에 지정된 레이블은 Adobe에 문의하거나 엽니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 게재<br /> </td> 
   <td> 트랜잭션 배달의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> Variant<br /> </td> 
   <td> A/B 테스트의 경우 전자 메일의 변형입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 지표 {#metrics}

아래 표는 보고서에 사용된 지표 목록과 배달 유형에 따라 해당 정의를 제공합니다.

### 이메일 및 SMS 지표 {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 차단 목록<br /> </td> 
   <td> 이메일을 스팸 또는 정크 메일로 선언한 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 차단 목록 속도<br /> </td> 
   <td> 게재에 표시된 차단 목록 게재의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 수 + 오류<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> 보낸 전자 메일에 비해 바운스된 전자 메일의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 게재 클릭 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전달된 비율<br /> </td> 
   <td> 성공적으로 보낸 메시지 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스<br /> </td> 
   <td> 잘못된 전자 메일 주소와 같은 총 영구 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스 비율<br /> </td> 
   <td> 영구 오류로 인해 실패한 게재의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지<br /> </td> 
   <td> 미러 페이지 링크를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지 속도<br /> </td> 
   <td> 미러 페이지 링크에 대한 클릭 비율(<br />)입니다. </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭<br /> </td> 
   <td> 게재에서 오퍼를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭률<br /> </td> 
   <td> 오퍼에 대한 클릭 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> 게재에서 메시지를 연 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기 비율<br /> </td> 
   <td> 열린 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리/전송<br /> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리<br /> </td> 
   <td> 바운스되어 주소가 격리된 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리 속도<br /> </td> 
   <td> 보낸 메시지와 비교하여 격리 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부됨<br /> </td> 
   <td> SMTP 서버로 스팸으로 분류된 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부된 비율<br /> </td> 
   <td> 거부됨으로 표시된 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스<br /> </td> 
   <td> 전체 받은 편지함과 같은 총 임시 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스 비율<br /> </td> 
   <td> 일시적인 이유로 인해 실패한 게재의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭 수<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> 게재를 연 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 구독 취소<br /> </td> 
   <td> 구독 취소 링크를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 가입 해지율<br /> </td> 
   <td> 전달된 메시지와 비교하여 고유한 구독 취소 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 가입 해지됨<br /> </td> 
   <td> 구독 취소 링크에 대한 클릭 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 푸시 알림 지표 {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 바운스 수 + 오류<br /> </td> 
   <td> MCPNS 또는 공급자의 오류 등 보낸 총 메시지 수와 관련하여 게재 중에 누적된 총 오류 수<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> 전송된 푸시 알림과 비교하여 바운스된 푸시 알림의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> 푸시 알림이 장치에 전달되고 사용자가 로그온한 횟수입니다. 사용자가 알림을 보려 했습니다. 알림을 본 후 푸시 열기 추적으로 이동되거나 해지됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 푸시 알림과 상호 작용한 사용자의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 푸시 알림 수와 관련하여 성공적으로 전송된 푸시 알림 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 전달된 비율<br /> </td> 
   <td> 푸시 알림을 성공적으로 보낸 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 푸시 알림이 장치에 전달되고 알림 센터에 그대로 남아 있는 횟수입니다. 대부분의 경우 노출 횟수 번호는 전달된 번호와 유사해야 합니다. 이렇게 하면 장치가 메시지를 수신하고 해당 정보를 서버에 다시 전달할 수 있습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리/전송<br /> </td> 
   <td> 보낸 총 푸시 알림 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> 장치에 배달되고 사용자가 클릭했던 총 푸시 알림 수로 인해 앱이 열립니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하고 푸시 클릭과 유사합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기 비율<br /> </td> 
   <td> 열린 푸시 알림의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭 수<br /> </td> 
   <td> 고유 사용자가 푸시 알림과 상호 작용하는 횟수(예: 알림 또는 단추를 클릭함)<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 수신자별 노출 횟수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> 게재를 연 받는 사람 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### 인앱 지표 {#in-app-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 서비스 공급자가 장치에 배달한 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 트리거 기준이 충족되었는지 여부에 따라 수신자가 본 인앱 메시지의 합계입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭 <br /> </td> 
   <td> 단추 1 또는 단추 2를 클릭한 총 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭스루 비율<br /> </td> 
   <td> 단추 1 또는 단추 2를 클릭한 사용자의 백분율과 메시지를 본 사용자의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 해임<br /> </td> 
   <td> 닫기 단추를 클릭하거나 자동 해지를 클릭하여 수신자가 해지한 총 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 해임률<br /> </td> 
   <td> 수신자가 해지한 인앱 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리/전송<br /> </td> 
   <td> 전송 전송 프로세스의 일부로 Adobe Campaign에서 전송된 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 고유한 수신자의 노출 횟수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유한 인앱 클릭<br /> </td> 
   <td> 받는 사람이 단추 1 또는 단추 2를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유한 인앱 취소<br /> </td> 
   <td> 인앱 메시지를 취소한 받는 사람 수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 세그먼트 {#segments}

아래 표는 보고서에 사용된 세그먼트 목록과 해당 정의를 제공합니다.

<table> 
 <thead> 
  <tr> 
   <th> 세그먼트<br /> </th> 
   <th> 정의<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 연령: 붐 세대 1<br /> </td> 
   <td> <br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 붐 세대 2<br /> </td> 
   <td> <br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 18~25<br /> </td> 
   <td> 수신자: 18세에서 25세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 26~30<br /> </td> 
   <td> 받는 사람: 26세에서 30세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 31~40<br /> </td> 
   <td> 받는 사람: 31세에서 40세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 41~50<br /> </td> 
   <td> 수신자: 41세에서 50세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 생성 X<br /> </td> 
   <td> <br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: Y 세대(밀레니얼)<br /> </td> 
   <td> 1977년부터 1994년까지 태어난 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 생성 Z<br /> </td> 
   <td> 1995년부터 오늘까지 출생한 받는 사람.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 50보다 큼<br /> </td> 
   <td> 나이가 50세 이상인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 25<br /> 미만 </td> 
   <td> 나이가 25세 미만인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 30<br /> 미만 </td> 
   <td> 연령이 30세 미만인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 40<br /> 미만 </td> 
   <td> 나이가 40세 미만인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 50<br /> 미만 </td> 
   <td> 나이가 50세 미만인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 자동 생성<br /> </td> 
   <td> 1945년 또는 그 이전에 태어난 받는 사람.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모든 방문<br /> </td> 
   <td> 모든 수신자<br /> </td> 
  </tr>
 </tbody> 
</table>
