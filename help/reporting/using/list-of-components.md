---
title: 구성 요소 목록
description: 여기에서 사용 가능한 모든 구성 요소 목록 찾기     동적 보고서와 해당 정의.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: 8980bf05-60a8-4360-a354-445e1faeb5b2
source-git-commit: dcfd4e2610cbf9d250359cab6ed43e8c97dd4536
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# 구성 요소 목록 {#list-of-components}

차원과 지표 간의 호환성에 대한 자세한 내용은 이 [테이블](/help/reporting/using/assets/dynamic_report_compatibility.pdf)을 참조하세요. 두 구성 요소가 호환되지 않으면 셀에 **없음** 값이 표시됩니다.

[![이미지](assets/dynamic_report_compatibility.png)](https://experienceleague.adobe.com/docs/campaign-standard/assets/dynamic_report_compatibility.pdf)

## 차원 {#dimensions}

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
   <td> 메시지를 열거나 클릭한 브라우저.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign<br /> </td> 
   <td> 캠페인의 레이블과 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구/군/시<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 도시입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 국가/지역<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 국가입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달<br /> </td> 
   <td> 게재 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 장치<br /> </td> 
   <td> 이메일/SMS/푸시 알림이 열리거나 보거나 클릭한 장치.<br /> </td> 
  </tr> 
  <tr> 
   <td> 실패 이유<br /> </td> 
   <td> 각 게재에 대해 바운스를 발생시키는 오류 유형(예: 사용자 알 수 없음, 잘못된 도메인 또는 사서함 가득 참).<br /> </td> 
  </tr> 
  <tr> 
   <td> 성별<br /> </td> 
   <td> 남성 또는 여성 등 수신자의 성별. 받는 사람의 프로필에서 성별 필드가 비어 있으면 값은 none이 됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 메시지 동작<br /> </td> 
   <td> 전달된 인앱 메시지에 대한 작업(예: 단추 1 또는 2에 대한 작업 또는 취소.<br /> </td> 
  </tr> 
  <tr> 
   <td> 메시지 유형<br /> </td> 
   <td> 게재에 사용되는 채널(예: 이메일, SMS, 푸시 알림 또는 인앱).<br /> </td> 
  </tr> 
  <tr> 
   <td> 모바일 앱 이름<br /> </td> 
   <td> 모바일 응용 프로그램 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 플랫폼<br /> </td> 
   <td> 메시지를 열고/보고/클릭한 장치의 플랫폼입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로필<br /> </td> 
   <td> 프로필 리소스 확장 중에 만들어진 기본 및 사용자 지정 프로필 필드를 다시 그룹화합니다. 자세한 내용은 이 <a href="../../developing/using/key-steps-to-add-a-resource.md">페이지</a> 또는 이 <a href="../../reporting/using/creating-a-custom-profile-dimension.md">예제</a>를 참조하세요.<br /> 프로필 필드에 연결된 사용자 지정 리소스가 게시되는 즉시 이 차원의 데이터를 검색합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 푸시 플랫폼<br /> </td> 
   <td> 푸시 알림을 연 장치의 플랫폼(예: iOS 또는 Android).<br /> </td> 
  </tr> 
  <tr> 
   <td> 받는 사람 도메인<br /> </td> 
   <td> 전자 메일을 여는 데 사용되는 도메인입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 반복 게재<br /> </td> 
   <td> 반복 게재의 레이블 및 ID입니다.<br /> </td> 
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
   <td> 추적 URL 범주<br /> </td> 
   <td> 추적 URL에 할당된 범주.<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL 레이블<br /> </td> 
   <td> 미러 페이지와 같이 URL에 지정된 레이블은 당사로 연락하거나 엽니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 게재<br /> </td> 
   <td> 트랜잭션 게재의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 변형<br /> </td> 
   <td> A/B 테스트 시 이메일 변형.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 지표 {#metrics}

아래 표는 보고서에 사용된 지표 목록과 게재 유형에 따라 해당 정의를 제공합니다.

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
   <td> 스팸 또는 정크 메일로 선언된 받는 사람의 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 차단 목록에 추가하다 속도<br /> </td> 
   <td> 차단 목록에 추가하다 게재 비율(<br />) </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류율<br /> </td> 
   <td> 보낸 전자 메일과 비교하여 반송된 전자 메일의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> 클릭 </td> 
   <td> 게재에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 게재 중 클릭 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 게재율<br /> </td> 
   <td> 성공적으로 보낸 메시지의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스<br /> </td> 
   <td> 잘못된 이메일 주소와 같은 총 영구 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스 비율<br /> </td> 
   <td> 영구 오류로 인해 실패한 게재의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지<br /> </td> 
   <td> 미러 페이지 링크를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지 속도<br /> </td> 
   <td> 총 게재 메시지와 비교한 미러 페이지 링크 클릭 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭수<br /> </td> 
   <td> 게재에서 오퍼를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭률<br /> </td> 
   <td> 오퍼 클릭률입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> 열기 </td> 
   <td> 메시지가 게재된 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열람률<br /> </td> 
   <td> 열린 메시지의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리<br /> </td> 
   <td> 반송되어 주소가 격리된 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리 비율<br /> </td> 
   <td> 보낸 메시지와 비교하여 격리한 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부됨<br /> </td> 
   <td> SMTP 서버에서 스팸으로 분류된 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부된 비율<br /> </td> 
   <td> 거부됨으로 표시된 메시지의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스<br /> </td> 
   <td> 전체 받은 편지함과 같은 총 임시 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스 비율<br /> </td> 
   <td> 일시적인 이유로 실패한 게재의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭수<br /> </td> 
   <td> 게재에서 콘텐츠를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기 수<br /> </td> 
   <td> 게재를 연 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 구독 취소<br /> </td> 
   <td> 구독 취소 링크를 클릭한 수신자 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소 비율<br /> </td> 
   <td> 배달된 메시지와 비교하여 고유한 구독 취소 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소됨<br /> </td> 
   <td> 구독 취소 링크를 클릭한 횟수입니다.<br /> </td> 
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
   <td> 바운스 + 오류<br /> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 중에 누적된 총 오류(예: MCPNS 또는 공급자의 오류)입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류율<br /> </td> 
   <td> 보낸 푸시 알림과 비교하여 반송된 푸시 알림의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> 클릭 </td> 
   <td> 푸시 알림이 디바이스에 전달되고 사용자가 클릭한 횟수. 사용자는 알림을 보고 싶었다가 푸시 열기 추적으로 이동되거나 알림을 해제했습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 푸시 알림과 상호 작용한 사용자의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 게재율<br /> </td> 
   <td> 푸시 알림이 성공적으로 전송된 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 푸시 알림이 디바이스에 전달되고 알림 센터에 그대로 남아 있는 횟수입니다. 대부분의 경우 노출 횟수는 게재된 횟수와 유사해야 합니다. 이렇게 하면 장치에서 메시지를 받아서 해당 정보를 다시 서버로 전달합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 보낸 총 푸시 알림 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> <br /> 열기 </td> 
   <td> 장치로 전달되고 사용자가 클릭하여 앱을 여는 총 푸시 알림 수입니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하면 푸시 클릭과 유사합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열람률<br /> </td> 
   <td> 열린 푸시 알림의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭수<br /> </td> 
   <td> 고유 사용자가 푸시 알림과 상호 작용하는 횟수(예: 알림 또는 단추 클릭 수)<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 받는 사람의 노출 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기 수<br /> </td> 
   <td> 게재를 연 수신자 수입니다.<br /> </td> 
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
   <td> 서비스 공급자가 장치로 배달한 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 트리거 기준이 충족되었는지 여부에 따라 수신자가 본 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭 수 <br /> </td> 
   <td> 단추 1 또는 단추 2를 클릭한 총 수신자 수.<br /> </td> 
  </tr> 
  <tr> 
   <td> 앱 내 클릭스루 비율<br /> </td> 
   <td> 단추 1 또는 단추 2를 클릭한 사용자의 백분율과 메시지를 본 사용자의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 해제<br /> </td> 
   <td> 받는 사람이 닫기 단추 또는 자동 취소를 클릭하여 해제한 총 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 삭제 비율<br /> </td> 
   <td> 수신자가 해제한 인앱 메시지의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 보낸 게재 프로세스의 일부로 Adobe Campaign에서 보낸 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 고유 수신자의 노출 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 인앱 클릭 수<br /> </td> 
   <td> 수신자가 단추 1 또는 단추 2를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유한 인앱 취소<br /> </td> 
   <td> 인앱 메시지를 거부한 시간 받는 사람 수입니다.<br /> </td> 
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
   <td> 나이: 붐 세대 1<br /> </td> 
   <td> 1946년부터 1954년까지 출생한 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 붐 세대 2<br /> </td> 
   <td> 1955년부터 1965년까지 출생한 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 18세부터 25<br /> </td> 
   <td> 18세에서 25세 사이의 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 26세부터 30<br /> </td> 
   <td> 26세에서 30세 사이의 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 31~40<br /> </td> 
   <td> 31세에서 40세 사이의 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 41~50<br /> </td> 
   <td> 41세에서 50세 사이의 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 세대 X<br /> </td> 
   <td> 1966년부터 1976년까지 출생한 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: Y세대(밀레니얼)<br /> </td> 
   <td> 1977년부터 1994년까지 출생한 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 세대 Z<br /> </td> 
   <td> 1995년부터 오늘까지 출생한 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령: 50<br />보다 큼 </td> 
   <td> 연령이 50세 이상인 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 나이: 25<br /> 미만 </td> 
   <td> 연령이 25.<br />세 미만인 수신자 </td> 
  </tr> 
  <tr> 
   <td> 연령: 30<br /> 미만 </td> 
   <td> 연령이 30.<br />세 미만인 수신자 </td> 
  </tr> 
  <tr> 
   <td> 나이: 40<br /> 미만 </td> 
   <td> 연령이 40.<br /> 미만인 수신자 </td> 
  </tr> 
  <tr> 
   <td> 연령: 50<br /> 미만 </td> 
   <td> 연령이 50.<br />세 미만인 수신자 </td> 
  </tr> 
  <tr> 
   <td> 수명: 자동 생성<br /> </td> 
   <td> 1945년 또는 그 이전에 태어난 수신자.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모든 방문<br /> </td> 
   <td> 모든 받는 사람<br /> </td> 
  </tr>
 </tbody> 
</table>
