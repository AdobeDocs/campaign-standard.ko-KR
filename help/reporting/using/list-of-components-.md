---
solution: Campaign Standard
product: campaign
title: '구성 요소 목록 '
description: 여기에서 사용 가능한 모든 구성 요소 목록을 확인하십시오.     동적 보고서 및 해당 정의
audience: reporting
content-type: reference
topic-tags: about-reporting
translation-type: tm+mt
source-git-commit: 6fffc6a3574c71c01f1e07ff4e6e6aa194479079
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 1%

---


# 구성 요소 목록 {#list-of-components}

차원과 지표 간 호환성에 대한 자세한 내용은 이 [표](/help/reporting/using/assets/dynamic_report_compatibility.pdf)를 참조하십시오. 두 구성 요소가 호환되지 않으면 셀에 **None** 값이 표시됩니다.

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
   <td> 구/군/시<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 구/군/시입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 국가/지역<br /> </td> 
   <td> 받는 사람의 프로필에 등록된 국가.<br /> </td> 
  </tr> 
  <tr> 
   <td> 게재<br /> </td> 
   <td> 배달의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 장치<br /> </td> 
   <td> 이메일/SMS/푸시 알림을 연/본/클릭한 장치<br /> </td> 
  </tr> 
  <tr> 
   <td> 실패 이유<br /> </td> 
   <td> 각 배달에 대한 바운스 수를 발생시킨 오류 유형(예: 사용자를 알 수 없거나 잘못된 도메인 또는 사서함이 가득 찼습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 성별<br /> </td> 
   <td> 수신자의 성별(예: 남성 또는 여성) 받는 사람 프로필에 성별 필드가 비어 있으면 값이 none이 됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 메시지 작업<br /> </td> 
   <td> 배달된 인앱 메시지에 대한 작업(예: 단추 1 또는 2에 대한 작업 또는 취소).<br /> </td> 
  </tr> 
  <tr> 
   <td> 메시지 유형<br /> </td> 
   <td> 이메일, SMS, 푸시 알림 또는 In-App과 같은 전달에 사용되는 채널입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모바일 앱 이름<br /> </td> 
   <td> 모바일 응용 프로그램 이름<br /> </td> 
  </tr> 
  <tr> 
   <td> 플랫폼<br /> </td> 
   <td> 메시지를 연/본/클릭한 장치의 플랫폼.<br /> </td> 
  </tr> 
  <tr> 
   <td> 프로필<br /> </td> 
   <td> 프로필 리소스 확장 중에 만들어진 기본 및 사용자 지정 프로필 필드를 재그룹화합니다. 자세한 내용은 이 <a href="../../developing/using/key-steps-to-add-a-resource.md">page</a> 또는 이 <a href="../../reporting/using/creating-a-custom-profile-dimension.md">example</a>을 참조하십시오.<br /> 프로필 필드에 연결된 사용자 지정 리소스가 게시되는 즉시 이 차원의 데이터가 검색됩니다.<br /> </td> 
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
   <td> 되풀이 배달의 레이블 및 ID입니다.<br /> </td> 
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
   <td> 사용자가 메시지에서 클릭한 URL.<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL 범주<br /> </td> 
   <td> 추적 URL에 할당된 카테고리<br /> </td> 
  </tr> 
  <tr> 
   <td> 추적 URL 레이블<br /> </td> 
   <td> 미러 페이지와 같은 URL에 지정된 레이블에 연락하거나 엽니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 트랜잭션 배달<br /> </td> 
   <td> 트랜잭션 배달의 레이블 및 ID입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 변형<br /> </td> 
   <td> A/B 테스트의 경우 이메일의 변수입니다.<br /> </td> 
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
   <td> 설정 차단 목록<br /> </td> 
   <td> 이메일을 스팸 또는 정크 메일로 선언한 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 차단 목록 비율<br /> </td> 
   <td> 에 표시된 배달 차단 목록 비율<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 수 + 오류<br /> </td> 
   <td> 배달된 총 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류.<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> 보낸 이메일과 비교하여 바운스된 이메일의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> 배달에서 콘텐츠를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 배달에서 클릭하는 비율<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달율<br /> </td> 
   <td> 성공적으로 보낸 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스<br /> </td> 
   <td> 잘못된 이메일 주소와 같은 총 영구 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 하드 바운스 비율<br /> </td> 
   <td> 영구 오류로 인해 실패한 배달 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지<br /> </td> 
   <td> 미러 페이지 링크를 클릭한 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 미러 페이지 속도<br /> </td> 
   <td> 미러 페이지 링크에 대한 클릭 수와 총 배달 메시지 수의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭<br /> </td> 
   <td> 배달에서 오퍼를 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 오퍼 클릭률<br /> </td> 
   <td> 오퍼에 대한 클릭 비율<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> 배달에서 메시지를 연 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 여는 속도<br /> </td> 
   <td> 연 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 배달에 대한 총 전송 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 격리<br /> </td> 
   <td> 바운스되어 주소의 검역을 일으킨 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 검역률<br /> </td> 
   <td> 보낸 메시지와 비교하여 검역량의 백분율<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부됨<br /> </td> 
   <td> SMTP 서버로 스팸으로 분류된 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 거부된 속도<br /> </td> 
   <td> 거부됨으로 표시된 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스<br /> </td> 
   <td> 전체 받은 편지함과 같은 총 임시 오류 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 소프트 바운스 비율<br /> </td> 
   <td> 일시적인 이유로 실패한 배달의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> 배달에서 콘텐츠를 클릭한 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> 배달을 연 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소 비율<br /> </td> 
   <td> 수신자별 구독 취소 백분율과 배달된 메시지 비교<br /> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소<br /> </td> 
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
   <td> MCPNS 또는 공급자의 오류와 같이 전송 중에 누적된 총 오류 수<br /> </td> 
  </tr> 
  <tr> 
   <td> 바운스 + 오류 비율<br /> </td> 
   <td> 전송된 푸시 알림과 비교하여 바운스된 푸시 알림의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭<br /> </td> 
   <td> 푸시 알림이 장치에 배달되고 사용자가 클릭한 횟수입니다. 사용자가 알림을 보려고 했습니다. 이 알림은 푸시 열기 추적으로 이동되거나 해제됩니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 비율<br /> </td> 
   <td> 푸시 알림과 상호 작용한 사용자의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달됨<br /> </td> 
   <td> 보낸 푸시 알림의 총 수와 관련하여 성공적으로 보낸 푸시 알림 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 배달율<br /> </td> 
   <td> 푸시 알림을 성공적으로 전송한 비율(<br />) </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 푸시 알림이 장치에 배달되고 알림 센터에 손상되지 않은 상태로 남아 있는 횟수입니다. 대부분의 경우 노출 횟수는 배달된 번호와 비슷해야 합니다. 이렇게 하면 장치가 메시지를 받고 해당 정보를 다시 서버로 전달합니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 보낸 총 푸시 알림 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 열기<br /> </td> 
   <td> 장치에 배달되고 사용자가 클릭한 총 푸시 알림 수로, 앱을 엽니다. 이 동작은 푸시 클릭과 비슷하지만 알림이 해제된 경우 푸시 열기가 트리거되지 않습니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 여는 속도<br /> </td> 
   <td> 열린 푸시 알림의 비율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 클릭<br /> </td> 
   <td> 고유 사용자가 푸시 알림과 상호 작용하는 횟수(예: 알림 또는 단추를 클릭)<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 받는 사람의 노출 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 열기<br /> </td> 
   <td> 배달을 연 받는 사람 수입니다.<br /> </td> 
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
   <td> 서비스 공급자가 장치로 배달한 인앱 메시지의 총 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 노출 횟수<br /> </td> 
   <td> 트리거 기준이 충족되었는지 여부에 따라 받는 사람이 보는 인앱 메시지의 합계입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭 <br /> </td> 
   <td> 단추 1 또는 단추 2에서 클릭한 총 받는 사람 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 클릭스루 비율<br /> </td> 
   <td> 단추 1 또는 단추 2를 클릭한 사용자의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 해지<br /> </td> 
   <td> 닫기 단추 또는 자동 해지를 클릭하여 받는 사람이 해지한 총 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 인앱 기각률<br /> </td> 
   <td> 받는 사람이 해지한 인앱 메시지의 백분율입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 처리됨/전송됨<br /> </td> 
   <td> 전송 프로세스의 일부로 Adobe Campaign에서 보낸 총 인앱 메시지 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 노출 횟수<br /> </td> 
   <td> 고유 받는 사람의 노출 수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 인앱 클릭<br /> </td> 
   <td> 받는 사람이 단추 1 또는 단추 2에서 클릭한 횟수입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 고유 인앱 해지<br /> </td> 
   <td> 받는 사람이 인앱 메시지를 취소한 횟수입니다.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 세그먼트 {#segments}

>[!NOTE]
>
>기본적으로 **[!UICONTROL Exclude proof]** 세그먼트는 이미 보고서를 필터링하도록 선택되었지만 필요한 경우 변경할 수 있습니다.

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
   <td> 연령:붐 세대 1<br /> </td> 
   <td> 1946년생부터 1954년생입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:붐 세대 2<br /> </td> 
   <td> 1955년생부터 1965년생입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:18부터 25까지<br /> </td> 
   <td> 받는 사람: 18세에서 25세<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:26부터 30까지<br /> </td> 
   <td> 받는 사람: 26세에서 30세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:31부터 40까지<br /> </td> 
   <td> 받는 사람: 31세에서 40세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:41부터 50까지<br /> </td> 
   <td> 수신자: 41세에서 50세.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:생성 X<br /> </td> 
   <td> 1966~1976년생으로 받는 사람<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:Y 세대(밀레니엄 세대)<br /> </td> 
   <td> 1977년생부터 1994년생입니다.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:생성 Z<br /> </td> 
   <td> 1995년부터 오늘까지.<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:50보다 큼<br /> </td> 
   <td> 연령이 50세 이상인 받는 사람<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:25개 미만<br /> </td> 
   <td> 연령이 25세 미만인 수신자<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:30개 미만<br /> </td> 
   <td> 연령이 30세 미만인 받는 사람<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:40개 미만<br /> </td> 
   <td> 연령이 40세 미만인 받는 사람<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:50개 미만<br /> </td> 
   <td> 연령이 50세 미만인 받는 사람<br /> </td> 
  </tr> 
  <tr> 
   <td> 연령:자동 생성<br /> </td> 
   <td> 1945년 또는 그 이전에 태어난 받는 사람.<br /> </td> 
  </tr> 
  <tr> 
   <td> 모든 방문<br /> </td> 
   <td> 모든 받는 사람<br /> </td> 
  </tr> 
    <tr> 
   <td> 증명 제외<br /> </td> 
   <td> 보고서에서 교정본 제외<br /> </td> 
  </tr> 
 </tbody> 
</table>

