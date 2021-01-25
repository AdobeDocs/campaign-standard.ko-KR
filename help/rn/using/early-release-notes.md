---
solution: Campaign Standard
product: campaign
title: 조기 릴리스 노트
description: 조기 릴리스 노트
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
hide: true
hidefromtoc: true
translation-type: tm+mt
source-git-commit: 26b401e18629f794ab3c1a836a28369d2f8f9605
workflow-type: tm+mt
source-wordcount: '2599'
ht-degree: 3%

---


# 새 릴리스 {#new-release}

[릴리스 계획](../../rn/using/release-planning.md) |  [Campaign 컨트롤 패널 릴리스](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html) |  [설명서 업데이트](../../rn/using/documentation-updates.md) |  [최신 릴리스 노트](../../rn/using/release-notes.md)   [| 사용 중단된 기능](../../rn/using/deprecated-features.md)

이 페이지에서는 다음 Campaign Standard 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 설명합니다.

>[!CAUTION]
>
> 이 컨텐츠는 스테이지 환경 업그레이드 날짜까지 사전 통지 없이 변경될 수 있습니다. [릴리즈 계획 페이지](../../rn/using/release-planning.md)에서 자세한 내용을 살펴보십시오.


## 릴리스 21.1 - 2021년 2월 {#release-21-1---febuary-2021}

**새로운 기능**

<table> 
<thead> 
<tr> 
<th> <strong>이메일 피드백 서비스</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>EFS(Email Feedback Service)는 향상된 MTA에서 바로 이메일 피드백을 캡처하여 보고 정확도를 높이는 확장 가능한 서비스입니다.</p>
<ul>
<li>모든 이벤트 카테고리가 캡처됩니다.지연, 전달, 보내기, 가입 해지(링크, 목록), 피드백(스팸 불만, 비동기 이벤트).</li>
<li>전송/배달 지표의 계산은 정확도와 재활동을 개선하기 위해 향상된 MTA의 실시간 피드백을 기반으로 합니다.</li>
<li>EFS는 동기식 바운스 보고 지연의 문제를 해결하고 inMail 프로세스에서 로드의 80%를 제거합니다.</li>
</ul>
<p>이 기능은 <strong>개인 베타</strong>로 릴리스되며 향후 릴리스의 모든 고객이 점진적으로 사용할 수 있게 됩니다.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>향상된 Adobe Experience Manager 통합</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Experience Manager와의 캠페인 통합이 개선되었습니다.이제 Adobe Experience Manager에서 다국어 컨텐츠를 보다 손쉽게 가져올 수 있습니다. <p>
<p>Adobe Campaign Standard은 이제 Adobe Experience Manager 컨텐츠의 언어 변형을 자동으로 감지하고 벌크 변형 가져오기 및 생성을 허용하므로, 전문가가 Adobe Experience Manager 컨텐츠를 기반으로 다국어 캠페인을 만들기 위해 거쳐야 하는 단계 수를 대폭 간소화할 수 있습니다.</p>
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>통합된 Experience Cloud 인터페이스</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign 헤더 막대가 모든 Experience Cloud 제품 및 서비스에서 경험을 통합하고 개선하기 위해 변경되었습니다. 이러한 변경 사항은 다음과 같은 작업을 보다 쉽게 할 수 있도록 설계되었습니다.</p>
<ul>
<li>조직 간에 또는 다른 애플리케이션으로 손쉽게 전환할 수 있습니다.</li>
<li>향상된 사용자 도움말 - Experience League을 제품에 포함시키면 커뮤니티 포럼 결과와 더 많은 비디오 컨텐츠에 대한 검색 결과가 포함되므로 더 많은 컨텐츠에 손쉽게 액세스하여 애플리케이션을 최대한 활용할 수 있습니다. 또한 도움말 메뉴에 바로 피드백 메커니즘을 추가하여 문제를 보고하거나 아이디어를 공유할 수 있습니다.</li>
<li>향상된 알림 - 이제 알림 드롭다운에는 2개의 탭이 있습니다.한 가지 제품 알림과 더 많은 글로벌 제품 발표 관련 사항이 있습니다.</li>
</ul>
</td> 
</tr> 
</tbody> 
</table>

**개선 사항**

* **Microsoft Dynamics 365** 와의 통합이 전용 셀프 서비스 통합 앱과 향상된 구현 프로세스를 통해 향상되었습니다. [자세히 알아보기](../../integrating/using/d365-acs-get-started.md)

* **트랜잭션 메시징 프로세스**&#x200B;에서 문제가 발생할 때 문제 해결을 용이하게 하기 위해 개선되었습니다. 이제 Adobe 기술 관리자는 프로세스를 다시 시작하지 않고도 모든 프로세스에 대한 추적을 사용할 수 있습니다.

* 이제 **프로필** 목록에서 다음 필드 중 하나를 기반으로 레코드를 검색할 수 있습니다.프로필 리소스를 확장할 때 고급 필터링에 추가된 이메일, 이름, 성 또는 사용자 정의 필드. 이 기능은 filterType 매개 변수를 사용하여 Campaign Standard API에서도 사용할 수 있습니다.

* 매개 변수가 **트랜잭션 메시징** 데이터베이스 풀링 프로세스를 실행하는 컨테이너 수로 조정되었습니다. 이렇게 하면 사용되는 모든 컨테이너에 걸쳐 로드를 균일하게 배포하고 최적의 성능에 도달할 수 있습니다.

* 이제 외부 매개 변수를 사용한 작업 흐름을 호출한 후 이벤트 변수를 사용하는 활동에서 새 **GetOption** 함수를 사용할 수 있습니다. 지정된 함수의 값을 반환할 수 있습니다.

* 새 옵션을 사용하면 워크플로우를 시작하기 전에 Campaign Standard에서 **시스템에서 실제 메모리** 가용성을 확인할 수 있습니다. 메모리 양이 너무 낮으면 시스템 메모리가 이 임계값에 도달할 때까지 워크플로 실행이 지연됩니다. 이로 인해 성능 저하를 방지하고 서비스 중단 위험을 줄일 수 있습니다. 서버 압력이 완화되면 워크플로우가 자동으로 다시 시작됩니다.  워크플로우 실행이 지연되는 경우 이 워크플로우의 활동 시간이 부족한 상태로 다시 예약하고 다시 시도하십시오. 이 옵션은 읽기 전용이므로 수정할 수 없습니다.

**기타 변경 사항**

* 롤링 시간당 컨텐츠 다운로드로 최대 100개까지 도달할 수 있는 메시지 준비 중 오류가 경고로 변경되었습니다. 이제 제한에 도달하면 경고가 표시되므로 배달을 진행할 수 있습니다.

* 트랜잭션 메시지 컨텐츠를 증가시키는 경우 프로필 테이블에서 데이터를 가져올 때 더 이상 링크가 검색되지 않으므로 메시지 준비 중 지연이 줄어들고 프로필 테이블에 정의된 잘못된 관계로 인해 빈 프로필 데이터가 표시되지 않습니다.

* 인스턴스 기술 구성이 안정성이 보장되도록 최적화되었습니다. (CAMP-45681)

* 세션 관리가 메모리를 최적화하기 위해 개선되었습니다. (CAMP-45901, CAMP-46767)

* 이제 **전송 파일** 활동이 업로드되거나 다운로드한 파일의 수를 포함하는 추가 변수(filesCount)를 생성합니다. (CAMP-45842)

* 이제 **SMS 커넥터**&#x200B;에서 각 메시지와 함께 여러 선택적 매개 변수를 보낼 수 있습니다.

* 이제 DATAMODEL 역할을 가진 사용자가 배달 로그 확장을 게시할 수 있습니다. (CAMP-46604)

* 더 이상 존재하지 않는 사용자 지정 리소스를 타깃팅하는 리소스를 게시하려고 할 때 표시되는 오류 메시지가 더 이상 명확하지 않습니다. (CAMP-46893)

* 다음 언어가 **기본 언어** 목록에 추가되었습니다.인도네시아 - 인도네시아(id), 영어 - 스웨덴(en-se), 영어 - 아시아 태평양(en-ap), 영어 - 일본어(en-jp), 스페인어 - 라틴 아메리카(es-la). (CAMP-46351)

* 이제 랜딩 페이지를 테스트할 때 프로필 선택을 위한 선택기가 시간 초과를 방지하기 위해 프로필 대신 profileBase 리소스를 사용합니다.

* SMPP 로그 형식이 개선되었습니다.

* Adobe Campaign Classic API와 일치하도록 cryptString 및 decryptString JS 함수에 대한 선택적 매개 변수가 추가되었습니다.

* 배달 준비 로그의 경고 또는 오류 메시지가 개선되었습니다.

* IMS(Adobe Identity Management Service)에 연결하려고 할 때 오류 로그가 개선되었습니다.

* 이제 **동적 보고**&#x200B;의 검색 막대를 사용하여 게재 및 캠페인 차원을 추가로 필터링할 수 있습니다.

* 이제 거래 SMS 메시지 유효성 날짜는 **트랜잭션 메시지 API**&#x200B;의 만료 매개 변수에 대해 설정된 값으로 정의할 수 있습니다. (CAMP-36600)

* 동적 보고에서 **배달 요약** 내장 보고서에 가입되지 않은 비율 지표에 대한 잘못된 데이터가 표시되었습니다. 이 문제를 해결하기 위해 **고유 구독 취소**&#x200B;라는 새 지표가 추가되었습니다. (CAMP-46445)

**패치**

* 특정 프로세스로 인해 배달이 매우 느리게 실행되는 문제를 해결했습니다. 몇 개의 매개 변수에 대해 잘못된 단위(예: 초 대신 밀리초)가 정의되었기 때문입니다.
* 한 번 실행되어 임시 리소스를 활용하는 **데이터 중복 제거** 활동을 복사하여 붙여넣을 때 발생할 수 있는 워크플로우의 문제를 해결했습니다. 중복되면 활동 리소스가 자동으로 비어 있게 설정되므로 워크플로우의 다른 활동에서 문제가 발생합니다. 붙여넣기가 완료되면, 이제 활동의 리소스가 동일하게 유지됩니다. 이 경우 워크플로우에서 나중에 오류를 트리거하지 않고 가능한 한 빨리 오류가 트리거됩니다. (CAMP-46903)
* Mobile SDK에서 deliveryID/MessageID가 null이 아닌 조건을 기준으로 공개 추적 요청을 전송하던 문제가 해결되었습니다. 이렇게 하면 추적 기능이 비활성화된 배달에 대해 404 오류가 발생합니다. 이제 게재의 추적 상태에 대한 정보가 포함된 추가 변수(acsDeliveryTracking)가 페이로드에서 전송됩니다. 이 변수는 설정된 추적 상태에 따라 2개의 값을 설정하거나 해제할 수 있습니다.
* 5,000개의 행이 표시되었을 때 배달 보고서가 실행되지 않던 문제를 수정했습니다.
* 배달 템플릿이 수정된 후 변형 B의 컨텐츠가 업데이트되지 않는 A/B 테스트 문제를 수정했습니다. (CAMP-45235)
* 트랜잭션 메시징 프로세스가 중단되어 메시지가 전송되지 않던 문제를 수정했습니다.
* 프로필 대상 차원을 사용하여 트랜잭션 푸시 메시지를 전송할 때 배달 분석이 실패하는 문제를 해결했습니다. 이제 새 게재 매핑 (mapRtEventAppSubRcp)을 트랜잭션 푸시 메시지 타겟팅 프로필에 사용할 수 있습니다. 이러한 게재에 대한 게재, 제외 및 추적 로그는 이제 broadLogAppSubRcp, excludeLogAppSubRcp 및 trackingLogAppSubRcp 테이블에서 사용할 수 있습니다.
* 내부 링크를 클릭한 후 탐색 문제가 발생하는 문제를 해결했습니다(예: 증명 요약 화면에서 상위 배달에 액세스할 때).
* 배달을 만들 때 사용 가능한 모든 Experience Manager 컨텐츠 템플릿이 표시되지 않던 문제를 수정했습니다. (CAMP-45990)
* **Reason** 열을 추가 데이터 탭에 추가한 후 배달 로그에 오류 메시지가 표시되지 않는 워크플로우의 문제를 해결했습니다. (CAMP-45139)
* 두 앱 구독 호출의 Marketing Cloud ID가 동일한 경우(&#39;중복된 키 값이 고유 제약 조건&#39; 오류를 위반함) 발생하던 문제가 해결되었습니다.
* 대량의 **쿼리** 및 **대상자 읽기** 활동이 포함된 워크플로우로 활동을 끌어다 놓을 때 성능 저하를 초래할 수 있는 문제를 수정했습니다. (CAMP-44511)
* 리디렉션 정보가 추적 서버로 업로드되지 않도록, 트랜잭션 메시지 준비 끝에 발생할 수 있는 오류를 수정했습니다.
* 워크플로우 리소스를 사용자 정의한 후 가져오기 템플릿을 열거나 가져오기 작업 이전의 가져오기 작업을 열려고 할 때 오류 메시지를 표시할 수 있는 문제를 수정했습니다. (CAMP-46183)
* 동적 대상 이름으로 구성된 경우 **대상자 읽기** 활동이 실행되지 않는 문제를 해결했습니다. (CAMP-46047)
* **목록 내보내기** 단추가 표시되지 않는 문제를 해결했습니다.
* **보고 집계** 작업 과정의 실패를 초래할 수 있는 문제를 수정했습니다. (CAMP-45979)
* 사용자 지정 합성 키(텍스트/날짜 동적 내용)로 사용자 지정 리소스를 만들 때 발생하는 문제를 수정했습니다.
* 쿼리 전환 데이터가 표시되지 않는 문제를 해결했습니다. (CAMP-45669)
* 사용자 지정 리소스 게시와 관련된 메모리 사용 문제가 해결되었습니다.
* 특정 날짜에 전송되도록 배달을 구성할 때 발생하는 문제를 수정했습니다. 납품이 확인되면 즉시 발송되도록 설정된 경우, 납품을 준비하지 못했고 처음에 지정된 날짜를 고려했습니다. (CAMP-44107)
* 트랜잭션 템플릿이 열리지 않는 문제가 해결되었습니다. (CAMP-47181)
* 허용되는 문자열 크기를 초과하는 이름의 유형 및 유형 분류 규칙이 중복될 수 있는 트랜잭션 메시지 게시 프로세스의 문제를 수정했습니다. (CAMP-47104)
* 입력 매개 변수가 존재하지 않는 레코드를 반환할 때 발생하는 **외부 API** 활동의 문제를 수정했습니다. (CAMP-47023)
* SMPP 커넥터가 다시 연결되지 않는 문제를 해결했습니다.
* 이름에 점이 포함된 파일을 다운로드할 때 **파일 전송** 작업에서 발생하는 문제가 해결되었습니다. 점 다음에 오는 문자는 파일의 확장자로 간주되었습니다. (CAMP-46624)
* 데이터베이스 풀링을 수행할 수 없어 트랜잭션 메시지가 라우터 큐에 고정되는 문제를 해결했습니다.
* 취소된 배달 로그가 전송되지 않도록 하지 못했던 오류가 수정되었습니다.
* **AND-join** 활동을 사용할 때 워크플로우가 실패하던 문제를 수정했습니다. 처음 유선 전환을 시각적으로 표시하더라도 활동이 기본 설정을 해당 전환으로 연결된 마지막 전환으로 자동으로 변경했습니다. (CAMP-46900)
* 격리된 주소가 상태가 [유효함]으로 잘못 설정되어 격리되지 않는 문제를 해결했습니다.
* 개인화된 필드에 특수 문자가 포함되어 있는 경우 해당 필드가 표시되지 않는 문제를 해결했습니다. (CAMP-46805)
* 프로필에 대한 특정 세부 보기를 표시하지 못하는 문제를 해결했습니다. 이 문제는 프로필 리소스가 **개인화된 필드 추가 섹션** 옵션이 활성화된 사용자 정의 필드로 확장되는 경우에 발생했습니다.
* 트랜잭션 이벤트를 전송할 때 오류 코드 500을 반환할 수 있는 문제를 수정했습니다. (CAMP-46811)
* 이메일 예약된 보고서를 수신하지 못하는 문제를 수정했습니다. (CAMP-46891)
* 1개의 카디널리티 단순 링크를 사용하여 사용자 지정 리소스를 프로필 리소스에 연결할 때 발생하는 문제가 수정되었습니다. 사용자 지정 리소스 필드가 비어 있는 프로파일에 액세스할 때 이제 빈 목록 대신 오류 메시지가 표시됩니다.
* 대체할 프로필을 선택할 때 페이지가 배달 프로필을 로드하지 못하는 워크플로우에서 프로필 대체를 사용할 때 발생하는 문제를 수정했습니다. (CAMP-46522)
* **데이터베이스 정리** 기술 워크플로에서 다음 오류로 인해 만료된 배달 작업 테이블을 삭제하려고 했던 회귀 문제를 수정했습니다.(CAMP-46536)

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* 사용자 지정 리소스에 대해 사용자 지정 필터를 사용할 때 가끔씩 발생하는 다음 오류를 수정했습니다.(CAMP-46509)

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* 푸시 알림 준비를 완료하는 데 시간이 너무 오래 걸리는 문제가 해결되었습니다. 일시적인 작업 테이블에 색인이 누락되었기 때문입니다.
* 사용자 지정 리소스와 프로필 리소스 사이에 관계가 이미 정의된 경우 워크플로우의 **조정** 활동에서 **Dimension을 사용하여** 옵션을 조정할 때 발생할 수 있는 오류가 수정되었습니다.
* **조정** 또는 **데이터 연계 강화** 활동을 통해 링크를 추가할 때 발생하는 문제가 해결되었습니다. 선택한 링크가 출력 변환에 표시되지 않았습니다.
* 워크플로우에서 반복적인 게재와 함께 **세그멘테이션** 활동을 사용할 때 배달을 잘못된 대상자에게 보내는 문제를 수정했습니다. (CAMP-46275, CAMP-46470)
* 동적 보고를 위한 사용자 지정 프로필 차원을 만들기 위해 프로필 리소스를 확장하려고 할 때 사용자 지정 리소스 게시가 실패하는 오류를 수정했습니다. (CAMP-46266)
* 파일 가져오기 테이블에 링크를 추가할 때 발생하는 오류를 수정했습니다. **Enrichment** 활동을 **파일 가져오기** 활동에 추가한 후 이전에 구성된 링크가 사라졌습니다. (CAMP-46557)
* 저장 시 세부 사항 구성 화면의 표시 순서가 변경된 프로필 데이터에 연결된 사용자 지정 리소스를 사용할 때 발생하는 문제를 수정했습니다. (CAMP-46312)
* 사용자 지정 배달 매핑을 기반으로 하는 배달로 인해 동적 보고에서 데이터를 표시하지 않는 문제를 해결했습니다.
* 워크플로우 쿼리 활동에서 잘못된 리소스 대상이 있는 컬렉션을 선택할 수 없는 오류를 수정했습니다.
* InMail 프로세스에서 하드 바운스의 유효성을 잘못 확인할 수 있는 문제를 수정했습니다.
* 링크 오류로 인해 프로필 화면을 열 때 발생하는 오류가 수정되었습니다.
* 정리 워크플로우에서 GDPR 데이터를 삭제하지 못하는 문제를 해결했습니다.
* 예약 구성이 이메일 배달 예약 매개 변수의 문자 키보드로 수동으로 업데이트되는 오류가 수정되었습니다.
* 조직 단위의 잘못된 매개 변수로 인해 프로필을 편집할 수 없는 문제를 수정했습니다.
* 서비스 확장 필드가 비어 있고 이메일 속성이 배달 템플릿에서 설정되었더라도 설정할 수 없는 문제를 해결했습니다.
* 교정본을 처리하는 데 더 오래 걸릴 수 있는 문제를 수정했습니다. (CAMP-45048)
* 프로필 개요 화면에서 열을 정렬하지 못하는 문제를 수정했습니다.
* Azure에서 중국어 문자가 포함된 이메일 변형이 발생할 수 있는 축소판 생성 문제를 수정했습니다. (CAMP-47152)
* Gmail 계정에서 받은 추적 이벤트 필터링으로 인해 Gmail에 대해 잘못된 개방 비율을 초래할 수 있는 20.4에 도입된 회귀 문제를 수정했습니다. (CAMP-46504)
* HTML 콘텐츠를 트랜잭션 메시지 템플릿으로 가져올 수 없는 문제를 수정했습니다. (CAMP-47318)
* 이메일 렌더링 보고서의 렌더링 표시 속도를 저하할 수 있는 문제를 수정했습니다. (CAMP-46226)
* 화면 정의에 목록 유형 요소로 구성된 사용자 지정 리소스를 게시하지 못하는 문제를 해결했습니다. (CAMP-47217)
* 이메일 콘텐츠 맨 위에 놓을 때 Microsoft Outlook에서 줄 분할자가 올바르게 렌더링되지 않는 이메일 디자이너의 문제를 해결했습니다. (CAMP-46294)
* Adobe Analytics 기술 워크플로우와의 KPI 조정 문제가 해결되었습니다. (CAMP-46576)
* 콘텐츠 블록을 삽입할 때 검색 상자에 조각이 자동으로 표시되지 않던 이메일 디자이너의 문제를 수정했습니다. (CAMP-44205)
* 조각에 emojis를 사용할 때 보낸 이메일에 원하지 않는 문자가 표시되는 이메일 디자이너의 문제를 해결했습니다. (CAMP-46621)
* 분할자 구성 요소에 영향을 주는 이메일 디자이너에서 20.4에 도입된 회귀 기능을 통해 컨텐츠의 행 높이 및 이미지 왜곡이 추가되었습니다. (CAMP-46663)
* 메시지를 Outlook 사서함에 보낼 때 이메일 디자이너에서 이 단추가 오른쪽 또는 왼쪽으로 정렬되었음에도 불구하고 기본 단추 단추가 가운데에 있도록 하는 문제를 해결했습니다. (CAMP-46466)
* 이메일 디자이너 미리 보기에서 프로필을 검색할 때 테스트 프로필 목록이 새로 고침되지 않는 문제를 해결했습니다. (CAMP-45265)
* 이메일 디자이너 미리 보기에서 프로필을 검색할 때 사용자 지정 테스트 프로필이 목록에 표시되지 않는 문제를 해결했습니다. (CAMP-45589)
* 배달 요약 보고서에서 트렌드 그래픽을 생성할 때 일치하지 않는 날짜가 표시되는 문제를 해결했습니다. (CAMP-45521)