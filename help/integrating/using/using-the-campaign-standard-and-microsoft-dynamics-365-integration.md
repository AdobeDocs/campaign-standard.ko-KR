---
solution: Campaign Standard
product: campaign
title: Microsoft Dynamics 365 통합 사용
description: Campaign Standard 통합과 함께 Microsoft Dynamics 365를 사용하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---


# Microsoft Dynamics 365 통합 사용

이 통합이 수행하는 몇 가지 작업이 있습니다.

* **수신**:

   * Dynamics 365의 **연락처**&#x200B;를 Campaign으로 가져오기

   * **사용자 지정 엔티티**:Dynamics 365에서 Campaign으로 사용자 지정 테이블을 가져옵니다. 이 섹션](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md)에서 [에 대해 자세히 알아보십시오.

* **수신**:ACS에서 D365로 이메일 마케팅 이벤트 가져오기(이메일 전송, 열기, 클릭, 바운스)

* **옵트아웃**:양방향 동기화 옵트아웃 상태(예:)

데이터 흐름에 대한 자세한 내용은 이 섹션](#data-flows)에서 [을 참조하십시오.

## Adobe Campaign Standard 사용자 경험

Dynamics 365에서 담당자가 생성 또는 수정되거나(활성화된 경우 삭제됨) Campaign으로 전송됩니다.  이러한 연락처는 캠페인의 프로필 화면에 표시되며 마케팅 캠페인에서 타깃팅될 수 있습니다.  아래의 프로필 화면을 참조하십시오.

![](assets/MSdynamicsACS-usage1.png)

옵트아웃 속성이 Campaign에서 수정되면, Campaign-to-Dynamics 365 또는 양방향 옵트아웃 구성을 선택하고 해당 특정 속성이 올바르게 매핑되어 있으면 Dynamics 365에 반영됩니다.

## Microsoft Dynamics 365 사용자 경험

예를 들어 다음 이메일 마케팅 이벤트가 캠페인에서 Dynamics 365로 전송되고 Dynamics 365 타임라인 보기에 사용자 지정 활동으로 표시됩니다.

* Adobe Campaign 이메일 보내기

* Adobe Campaign 이메일 열기

* Adobe Campaign 이메일 URL 클릭

* Adobe Campaign 이메일 바운스

연락처의 타임라인을 보려면 Dynamics 365 드롭다운 메뉴에서 판매 허브를 클릭하여 연락처 목록으로 이동합니다.  그런 다음 왼쪽 메뉴 모음에서 [연락처]를 클릭하고 연락처를 선택합니다.

>[!NOTE]
>
>이러한 이벤트를 보려면 AppSource의 Adobe Campaign for Dynamics 365 앱을 Dynamics 365 인스턴스에 설치해야 합니다.

아래에서 &quot;Dynamics 사용자&quot;에 대한 연락처 화면의 스냅숏을 볼 수 있습니다.  타임라인 보기에서는 Dynamics 사용자가 캠페인 이름 &quot;2019LoymentCamp&quot; 및 배달 이름 &quot;DM190&quot;과 연결된 이메일을 전송했음을 알 수 있습니다.  Dynamics 사용자가 이메일을 열고 이메일에서 URL을 클릭했습니다.이 두 작업 모두 아래 표시 이벤트를 만들었습니다.  오른쪽 모퉁이를 보면 관계 도우미(RA) 카드가 표시됩니다.현재, 여기에는 클릭한 URL에 대한 후속 작업을 수행하는 작업이 포함되어 있습니다.

![](assets/do-not-localize/MSdynamicsACS-usage4.png)

Dynamics 사용자에 대한 타임라인 보기에 대한 자세한 내용은 아래를 참조하십시오.

![](assets/do-not-localize/MSdynamicsACS-usage5.png)

아래는 RA(Relationship Assistant) 카드의 가까운 부분입니다.  AppSource 앱에는 Adobe 이메일 URL 클릭 이벤트를 보는 워크플로우가 포함되어 있습니다.  이 이벤트가 발생하면 작업을 만들고 기한을 설정합니다.  이렇게 하면 작업이 RA 카드에 표시되어 추가 가시성을 제공할 수 있습니다.  잘못된 이메일 주소를 조정하는 작업을 추가하여 Adobe 이메일 바운스 이벤트에 대한 유사한 워크플로우가 있습니다.  이러한 워크플로우는 솔루션에서 끌 수 있습니다.

![](assets/do-not-localize/MSdynamicsACS-usage6.png)

전송 이벤트의 제목을 클릭하면 아래 양식과 유사한 양식이 표시됩니다.  열린 이벤트와 바운스 이벤트에 대한 양식은 유사합니다.

![](assets/do-not-localize/mirror_page_url_send.png)

이메일 URL 클릭 이벤트에 대한 양식은 클릭한 URL에 대한 추가 속성을 추가합니다.

![](assets/do-not-localize/mirror_page_url_click.png)

다음은 속성 목록과 설명입니다.

* 제목:행사 대상;이메일 배달의 캠페인 ID 및 배달 ID로 구성됨

* 소유자:사후 제공 단계에서 생성된 응용 프로그램 사용자

* 관련:연락처 이름

* 캠페인 이름:Campaign Standard의 캠페인 ID

* 배달 이름:Campaign Standard의 배달 ID

* 보낸 날짜/열린 날짜/클릭한 날짜/바운스된 날짜:이벤트를 만든 날짜/시간

* 추적 URL:클릭한 URL

* 페이지 URL 미러:보낸/연/클릭한/반송된 이메일의 미러 페이지에 대한 URL

>[!NOTE]
>
>이메일 미러 페이지의 만료 기간은 해당 캠페인 이메일 채널 활동의 구성 화면에서 수정할 수 있습니다([유효성 기간 매개 변수](../../administration/using/configuring-email-channel.md#validity-period-parameters) 참조).

>[!NOTE]
>
>옵트아웃의 경우, 옵트아웃 속성이 Dynamics 365에서 수정되면 Dynamics 365에서 캠페인에 로의 옵트아웃 또는 양방향 옵트아웃 구성을 선택하고 해당 특정 속성이 올바르게 매핑되는 경우 캠페인에 반영됩니다.

## 데이터 흐름 {#data-flows}

### 연락처 및 사용자 지정 개체 수신

새 레코드와 업데이트된(활성화된 경우 삭제됨) 레코드는 Dynamics 365 연락처 테이블에서 캠페인 프로필 테이블로 전송됩니다.

테이블 매핑을 구성하여 Dynamics 365 테이블 속성을 캠페인 테이블 속성에 매핑할 수 있습니다. 필요에 따라 특성을 추가/제거하도록 테이블 매핑을 수정할 수 있습니다.

데이터 흐름의 초기 실행은 &quot;비활성&quot;으로 표시된 레코드를 포함하여 매핑된 모든 레코드를 전송하도록 설계되었습니다.이후 통합은 증분 업데이트만 처리합니다. 이에 대한 예외는 필터가 구성된 경우입니다.기본 속성 기반 필터링 규칙을 구성하여 캠페인에 동기화할 레코드를 결정할 수 있습니다.

속성 값을 다른 값(예: &quot;#00FF00&quot;의 경우 &quot;green&quot;, &quot;1의 경우 &quot;F&quot;)으로 대체하도록 기본 대체 규칙을 구성할 수 있습니다.

레코드 볼륨에 따라, 초기 데이터 전송을 위해 캠페인 SFTP 저장소를 사용해야 할 수 있습니다.  &quot;초기 데이터 전송&quot;에 대한 섹션을 참조하십시오.

연락처 수신이 작동하려면 Dynamics 365 연락처 특성 contactId로 캠페인 프로필 테이블 특성 externalId를 채워야 합니다. 캠페인 사용자 지정 엔터티도 Dynamics 365 고유 ID 속성으로 채워야 합니다.하지만 이 속성은 모든 Campaign 사용자 지정 개체 속성에 저장할 수 있습니다(즉, externalId일 필요가 없습니다).

>[!NOTE]
>
>사용자 지정 엔터티 입맞춤의 경우 동기화된 사용자 지정 엔터티에 대해 Dynamics 365 내에서 변경 추적을 활성화해야 합니다.

### 이메일 마케팅 이벤트 흐름

이메일 마케팅 이벤트는 Campaign에서 Dynamics 365로 전송되어 타임라인 보기에 표시됩니다.

지원되는 마케팅 이벤트 유형:
* 보내기 - 수신자에게 보낸 이메일
* 열기 - 수신자가 연 이메일
* 클릭 - 수신자가 클릭한 이메일 내 URL
* 바운스 - 수신자에게 이메일 보내기에서 하드 바운스가 발생했습니다.

다음 이벤트 속성이 D365 내에 표시됩니다.
* 마케팅 캠페인 이름
* 이메일 배달 이름
* 타임스탬프
* 이메일 미러 페이지 URL
* 클릭한 URL(클릭 이벤트만)

이메일 마케팅 이벤트는 유형별로 활성화/비활성화할 수 있으므로 선택한 이벤트 유형만 Dynamics 365에 전달됩니다.

### 옵트아웃 흐름

옵트아웃(예:) 값차단 목록은 시스템 간에 동기화됩니다.가입 시 선택할 수 있는 옵션은 다음과 같습니다.
* Dynamics 365는 옵트아웃을 위한 진실의 근원입니다.옵트아웃 속성은 Dynamics 365에서 Campaign Standard으로 한 방향으로 동기화됩니다.
* Campaign Standard은 옵트아웃의 근원이다.옵트아웃 속성은 Campaign Standard에서 Dynamics 365로 한 방향으로 동기화됩니다.
* Dynamics 365 AND Campaign Standard은 둘 다 진실의 원천입니다.옵트아웃 속성은 Campaign Standard과 Dynamics 365 간에 양방향 동기화됩니다.

또는 시스템 간의 옵트아웃 동기화를 관리하는 별도의 프로세스가 있는 경우 통합의 옵트아웃 데이터 흐름을 비활성화할 수 있습니다.

비즈니스 요구 사항은 회사 간에 다를 수 있으므로 고객이 옵트아웃 흐름 매핑을 지정해야 합니다.  캠페인 측에서는 OTB 옵트아웃 속성만 옵트아웃 매핑에 사용할 수 있습니다.
* 차단 목록
* denyListEmail
* denyListFax
* denyListMobile
* denyListPhone
* denyListPostalMail
* denyListPushnotification
* ccpaOptOut

Dynamics 365에서는 대부분의 옵트아웃 필드에 &quot;doot&quot; 접두어가 있습니다.그러나 데이터 유형이 호환하는 경우 옵트아웃 용도로 다른 속성을 사용할 수도 있습니다.

### 초기 데이터 전송

500k 레코드가 넘는 Dynamics 365개의 표를 캠페인 작업 과정을 통해 가져올 캠페인 SFTP 스토리지로 내보내야 합니다.

초기 데이터 전송은 파일 기반의 데이터 전송으로, 데이터 전송 후 통합은 증분 업데이트에 API를 사용합니다.
