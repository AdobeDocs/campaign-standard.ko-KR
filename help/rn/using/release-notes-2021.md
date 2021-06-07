---
solution: Campaign Standard
product: campaign
title: 2021년 릴리스 정보
description: 이 페이지에는 Adobe Campaign Standard의 2021년 릴리스가 모두 나열되어 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: 개요
role: Business Practitioner
level: Beginner
exl-id: b6cf7152-2200-43d7-8d0a-d65752bb2c9b
source-git-commit: 21820131ef4ef13782a416535b170f260ab5efea
workflow-type: tm+mt
source-wordcount: '2538'
ht-degree: 95%

---

# 릴리스 정보 2021년{#release-notes-2021}

[릴리스 계획](../../rn/using/release-planning.md) | [Campaign 컨트롤 패널 릴리스](https://docs.adobe.com/content/help/ko-KR/control-panel/using/release-notes.html) | [설명서 업데이트](../../rn/using/documentation-updates.md) | [이전 릴리스 정보](../../rn/using/release-notes-2020.md) | [더 이상 사용되지 않는 기능](../../rn/using/deprecated-features.md)

## 릴리스 21.1 - 2021년 2월 {#release-21-1---february-2021}

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
<p>EFS(이메일 피드백 서비스)는 Enhanced MTA의 피드백을 바로 캡처하여 보고 정확도를 향상하는 확장 가능한 서비스입니다. 이 기능은 개인 베타 버전으로 출시되며 모든 고객은 향후 릴리스에서 점진적으로 사용할 수 있습니다.</p>
<ul>
<li>이제 완벽하고 정밀한 보고를 위해 모든 카테고리의 피드백을 캡처합니다.</li>
<li><b>전달됨</b> 표시기의 계산은 정확도 및 재활동 향상을 위해 Enhanced MTA의 실시간 피드백을 기반으로 합니다.</li>
<li>EFS는 동기식 소프트 바운스 보고로 지연되는 문제를 해결합니다.</li>
</ul>
<p>자세한 내용은 <a href="../../sending/using/confirming-the-send.md">세부 설명서</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Adobe Experience Manager 통합 개선 사항</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Experience Manager와 Campaign의 통합을 개선했습니다. 이제 Adobe Experience Manager에서 다국어 콘텐츠를 보다 손쉽게 가져올 수 있습니다. <p>
<p>Adobe Campaign Standard는 이제 Adobe Experience Manager 콘텐츠의 언어 변형을 자동으로 감지하고 일괄 변형 가져오기 및 생성을 허용하므로, 전문가가 Adobe Experience Manager 콘텐츠를 기반으로 다국어 캠페인을 만들기 위해 거쳐야 하는 단계를 대폭 간소화할 수 있습니다.</p>
<p>자세한 내용은 <a href="../../integrating/using/creating-multilingual-email-aem.md">세부 설명서</a>를 참조하십시오.
</p>
</td> 
</tr> 
</tbody> 
</table>

<!--
<table> 
<thead> 
<tr> 
<th> <strong>Unified Experience Cloud interface</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign header bar has been changed to unify and improve your experience across all Experience Cloud products and services. These changes are designed to make your life easier, including:</p>
<ul>
<li>Easier switching between your organizations or to a different application.</li>
<li>Improved User Help – Bringing the Experience League into the product, search results also include results from community forums and more video content, giving you easier access to more content to help get the most out of the application. We've also added a feedback mechanism right in the Help menu, making it easier to report issues or share your ideas.</li>
<li>Improved Notifications – Notifications drop-down now has two tabs: one for your own product notifications, and one for more global product announcements.</li>
</ul>
<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>
<p>NOTE: This change will be progressively rolled out to all customer environments between Feb 10 and March 1st.
</p>
</td> 
</tr> 
</tbody> 
</table>
-->

**개선 사항**

* **Microsoft Dynamics 365 통합**&#x200B;을 개선했습니다. 셀프 서비스 전용 통합 앱과 향상된 구현 프로세스를 추가했습니다. [자세히 알아보기](../../integrating/using/d365-acs-get-started.md)

* 트랜잭션 메시지 프로세스에서 문제가 발생할 때 쉽게 해결하도록 개선되었습니다. 이제 Adobe 기술 관리자는 프로세스를 다시 시작하지 않고도 모든 프로세스를 추적할 수 있습니다.

* 이제 **프로필** 목록에서 다음 필드 중 하나를 기반으로 레코드를 검색할 수 있습니다. 이메일, 이름, 성 또는 사용자 정의 필드는 프로필 리소스를 확장할 때 고급 필터링에 추가되었습니다. 이 기능은 filterType 매개 변수를 사용하여 Campaign Standard API에서도 사용할 수 있습니다. [자세히 알아보기](../../audiences/using/integrated-customer-profile.md)

* 매개 변수는 트랜잭션 메시지의 데이터베이스 풀링 프로세스를 실행하는 컨테이너 수로 조정했습니다. 이렇게 하면 사용되는 모든 컨테이너로 로드를 균일하게 분산하고 최적의 성능을 발휘할 수 있습니다.

* 이제 외부 매개 변수로 워크플로우를 호출한 후 이벤트 변수를 사용하는 활동에서 새 **GetOption** 함수를 사용할 수 있습니다. 이를 통해 지정된 함수의 값을 반환할 수 있습니다. [자세히 알아보기](../../automating/using/customizing-workflow-external-parameters.md)

* 새 옵션을 사용하면 워크플로우를 시작하기 전에 Campaign Standard에서 시스템의 사용 가능한 **실제 메모리를 확인**&#x200B;할 수 있습니다. 메모리의 양이 너무 낮으면 시스템 메모리가 이 임계값에 도달할 때까지 워크플로우 실행이 지연됩니다. 이를 통해 성능 저하를 방지하고 작동 중단 위험을 줄일 수 있습니다. 서버에 대한 로드가 줄고 메모리가 증가하면 워크플로우가 자동으로 다시 시작됩니다. 이 옵션은 읽기 전용이며 수정할 수 없습니다. [자세히 알아보기](../../automating/using/best-practices-workflows.md#execution)

* 기존 SDK v4 모바일 애플리케이션에서 **Adobe Experience Platform Mobile SDK**&#x200B;로 보다 쉽게 마이그레이션할 수 있는 새로운 프로세스가 Adobe Campaign Standard에서 제공됩니다. [이 페이지](../../administration/using/sdkv4-migration.md)를 참조하십시오.

**기타 변경 사항**

* 롤링 시간당 최대 100개의 콘텐츠 다운로드 제한에 도달할 때 메시지 준비 중 오류가 경고로 변경되었습니다. 이제 제한에 도달하면 경고가 표시되므로 게재를 진행할 수 있습니다.

* 트랜잭션 메시지 콘텐츠를 보강하는 경우 프로필 테이블에서 데이터를 가져올 때 더 이상 링크가 검색되지 않으므로 메시지 준비 중 지연이 줄어들고 프로필 테이블에 정의된 잘못된 관계로 인한 빈 프로필 데이터가 표시되지 않습니다.

* 인스턴스 기술 구성이 안정성이 보장되도록 최적화되었습니다. (CAMP-45681)

* 세션 관리가 메모리를 최적화하기 위해 개선되었습니다. (CAMP-45901, CAMP-46767)

* 이제 **전송 파일** 활동은 업로드되거나 다운로드한 파일의 수를 포함하는 추가 변수(filesCount)를 생성합니다. (CAMP-45842) [자세히 알아보기](../../automating/using/transfer-file.md#output-variables)

* 이제 SMS 커넥터는 각 메시지와 함께 여러 선택적 매개 변수를 보낼 수 있습니다. [자세히 알아보기](../../administration/using/sms-protocol.md)

* 이제 DATAMODEL 역할을 가진 사용자는 게재 로그 확장을 게시할 수 있습니다. (CAMP-46604)

* 더 이상 존재하지 않는 사용자 지정 리소스를 타겟팅하는 리소스를 게시하려고 할 때 표시되는 오류 메시지가 더욱 명확하게 표시됩니다. (CAMP-46893)

* 다음 언어가 **기본 설정 언어** 목록에 추가되었습니다. 인도네시아어 - 인도네시아(id), 영어 - 스웨덴(en-se), 영어 - 아시아 태평양(en-ap), 영어 - 일본(en-jp), 스페인어 - 라틴 아메리카(es-la). (CAMP-46351)

* 이제 랜딩 페이지를 테스트할 때 프로필 선택을 위한 선택기가 시간 초과를 방지하기 위해 프로필 대신 profileBase 리소스를 사용합니다.

* SMPP 로그 포맷이 개선되었습니다.

* Adobe Campaign Classic API와 일치하기 위해 cryptString 및 decryptString JS 함수에 대한 선택적 매개 변수가 추가되었습니다.

* 게재 준비 로그의 경고 또는 오류 메시지가 개선되었습니다.

* Adobe IMS(Identity Management Service)에 연결을 시도할 때 오류 로그가 개선되었습니다.

* 이제 다이내믹 보고에서 검색 창을 사용하여 **게재** 및 **Campaign** 차원을 추가로 필터링할 수 있습니다.

* 이제 트랜잭션 SMS 메시지 유효성 날짜는 트랜잭션 메시지 API의 만료 매개 변수에 대해 설정된 값으로 정의할 수 있습니다. (CAMP-36600)

* 다이내믹 보고에서는 **게재 요약** 기본 제공 보고서에 구독 취소 비율 지표에 대한 잘못된 데이터가 표시되었습니다. 이 문제를 해결하기 위해 **고유 구독 취소**&#x200B;라는 새 지표가 추가되었습니다. (CAMP-46445)

**패치**

* 특정 프로세스로 인해 게재가 매우 느리게 실행되는 문제를 해결했습니다. 몇 개의 매개 변수에 대해 잘못된 단위(예: 초 대신 밀리초)가 정의되었기 때문이었습니다.

* Mobile SDK에서 deliveryID/MessageID가 null이 아니라는 조건을 기준으로 공개 추적 요청을 전송하던 문제를 해결했습니다. 이로 인해 추적이 비활성화된 게재에 대해 404 오류가 발생합니다. 이제 게재의 추적 상태에 대한 정보가 포함된 추가 변수(acsDeliveryTracking)가 페이로드에서 전송됩니다. 이 변수는 설정된 추적 상태에 따라 2개의 값을 설정하거나 해제할 수 있습니다. [자세히 알아보기](../../administration/using/push-tracking.md)

* 한 번 실행되고 임시 리소스를 활용하는 **중복 제거** 활동을 복사하여 붙여넣을 때 발생할 수 있는 워크플로우의 문제를 해결했습니다. 중복되면 활동 리소스가 자동으로 비어 있게 설정되므로 워크플로우의 다른 활동에서 문제가 발생합니다. 붙여넣으면 이제 활동의 리소스는 워크플로우에서 나중에 오류를 트리거하지 않고 가능한 한 빨리 오류를 트리거하기 위해 동일하게 유지됩니다. (CAMP-46903)

* 새 [target 매핑](../../administration/using/target-mappings-in-campaign.md)을 도입하여 트랜잭션 푸시 알림 타겟팅 프로필을 전송할 때 게재 분석이 실패하는 문제를 해결했습니다.**프로필 - Push**&#x200B;에 대한 실시간 이벤트(*mapRtEventAppSubRcp*). [프로필 기반 트랜잭션 푸시 알림](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile)에 대한 게재, 제외 및 추적 로그는 이제 *broadLogAppSubRcp*, *excludeLogAppSubRcp* 및 *trackingLogAppSubRcp* 테이블에 저장됩니다.

   >[!IMPORTANT]
   >
   >이러한 변경으로 인해 기존 프로필 기반 푸시 트랜잭션 알림을 사용하는 경우(Adobe Campaign 21.1로 업그레이드하기 전에 생성됨) 대상 매핑을 새 프로필에 업데이트하고 메시지를 다시 게시하는 것이 좋습니다. 여기](../../channels/using/transactional-push-notifications.md#change-target-mapping)에서 자세한 [단계를 참조하십시오. 이전 대상 매핑 **프로필 - 실시간 이벤트**(*mapRtEventRcp*)를 사용하면 게재 준비 시간이 길어지고 성능이 저하될 수 있습니다.

* 5,000개의 행이 표시되었을 때 게재 보고서가 실행되지 않던 문제를 해결했습니다.
* 게재 템플릿이 수정된 후 변형 B의 콘텐츠가 업데이트되지 않는 A/B 테스트 문제를 해결했습니다. (CAMP-45235)
* 트랜잭션 메시지 프로세스가 중단되어 메시지가 전송되지 않던 문제를 해결했습니다.
* 내부 링크를 클릭한 후 탐색 문제가 발생하는 문제를 해결했습니다(예: 증명 요약 화면에서 상위 게재에 액세스할 때).
* 게재를 만들 때 사용 가능한 모든 Experience Manager 콘텐츠 템플릿이 표시되지 않던 문제를 해결했습니다. (CAMP-45990)
* **Reason** 열을 추가 데이터 탭에 추가한 후 게재 로그에 오류 메시지가 표시되지 않는 워크플로우의 문제를 해결했습니다. (CAMP-45139)
* 두 앱 구독 호출의 Marketing Cloud ID가 동일한 경우 발생하던 문제를 해결했습니다(&#39;복제 키 값이 고유 제한 위반&#39; 오류).
* 대량의 **쿼리** 및 **대상자 읽기** 활동이 포함된 워크플로우로 활동을 끌어다 놓을 때 성능 저하를 초래할 수 있는 문제를 수정했습니다. (CAMP-44511)
* 리디렉션 정보가 추적 서버로 업로드되지 않도록 트랜잭션 메시지 준비 끝에 발생할 수 있는 오류를 수정했습니다.
* 워크플로우 리소스를 사용자 지정한 후 가져오기 템플릿을 열거나 이전의 가져오기 작업을 열려고 할 때 오류 메시지가 표시될 수 있는 문제를 해결했습니다. (CAMP-46183)
* 동적 대상 이름으로 구성된 경우 **대상자 읽기** 활동이 실행되지 않는 문제를 해결했습니다. (CAMP-46047)
* **목록 내보내기** 단추가 표시되지 않는 문제를 해결했습니다.
* **보고 합계** 워크플로우의 실패를 초래할 수 있는 문제를 해결했습니다. (CAMP-45979)
* 사용자 지정 복합 키(텍스트/날짜 다이내믹 콘텐츠)로 사용자 지정 리소스를 만들 때 발생하는 문제를 해결했습니다.
* 쿼리 전환 데이터가 표시되지 않는 문제를 해결했습니다. (CAMP-45669)
* 사용자 지정 리소스 게시와 관련된 메모리 사용량 문제를 해결했습니다.
* 특정 날짜에 전송되도록 게재를 구성할 때 발생하는 문제를 수정했습니다. 게재가 확인되면 즉시 발송되도록 설정된 경우, 게재 준비가 실패하고 처음에 지정된 날짜를 여전히 고려했습니다. (CAMP-44107)
* 트랜잭션 템플릿이 열리지 않는 문제를 해결했습니다. (CAMP-47181)
* 허용되는 문자열 크기를 초과하는 이름의 유형화 및 유형화 규칙이 중복될 수 있는 트랜잭션 메시지 게시 프로세스의 문제를 해결했습니다. (CAMP-47104)
* 입력 매개 변수가 존재하지 않는 레코드를 반환할 때 발생하는 **외부 API** 활동의 문제를 해결했습니다. (CAMP-47023)
* SMPP 커넥터가 다시 연결되지 않는 문제를 해결했습니다.
* 이름에 점이 포함된 파일을 다운로드할 때 **파일 전송** 활동에서 발생하는 문제를 해결했습니다. 점 다음에 오는 문자는 파일의 확장자로 간주되었습니다. (CAMP-46624)
* 데이터베이스 풀링을 수행할 수 없어 트랜잭션 메시지가 라우터 큐에 멈추는 문제를 해결했습니다.
* 취소된 게재 로그가 전송되지 않도록 하지 못했던 오류를 수정했습니다. 
* **AND-join** 활동을 사용할 때 워크플로우가 실패하던 문제를 해결했습니다. 처음 유선 전환을 시각적으로 표시하더라도 활동은 기본 설정을 해당 전환으로 연결된 마지막 전환으로 자동으로 변경했습니다. (CAMP-46900)
* 격리된 주소가 상태가 [유효함]으로 잘못 설정되어 격리되지 않는 문제를 해결했습니다.
* 개인화된 필드에 특수 문자가 포함되어 있는 경우 해당 필드가 표시되지 않는 문제를 해결했습니다. (CAMP-46805)
* 프로필에 대한 특정 자세히 보기를 표시하지 못하는 문제를 해결했습니다. 이 문제는 프로필 리소스가 **개인화된 필드 추가 섹션** 옵션이 활성화된 사용자 지정 필드로 확장되는 경우에 발생했습니다.
* 트랜잭션 이벤트를 전송할 때 오류 코드 500을 반환할 수 있는 문제를 해결했습니다. (CAMP-46811)
* 이메일 예약 보고서를 수신하지 못하는 문제를 해결했습니다. (CAMP-46891)
* 1개의 카디널리티 단순 링크를 사용하여 사용자 지정 리소스를 프로필 리소스에 연결할 때 발생하는 문제를 해결했습니다. 사용자 지정 리소스 필드가 비어 있는 프로필에 액세스할 때 이제 빈 목록 대신 오류 메시지가 표시됩니다.
* 대체할 프로필을 선택할 때 페이지가 게재 프로필을 로드하지 못하는 워크플로우에서 프로필 대체를 사용할 때 발생하는 문제를 해결했습니다. (CAMP-46522)
* **데이터베이스 정리** 기술 워크플로에서 다음과 같은 오류로 인해 만료된 게재 작업테이블을 삭제하려고 했던 회귀 문제를 해결했습니다. (CAMP-46536)

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* 사용자 지정 리소스에 대해 사용자 지정 필터를 사용할 때 몇 가지 사례에서 발생하는 다음과 같은 오류를 수정했습니다. (CAMP-46509)

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* **푸시 알림 준비**&#x200B;가 완료되는 데 시간이 너무 오래 걸리는 문제를 해결했습니다. 이는 일시적인 작업 테이블에 색인이 누락되었기 때문이었습니다.
* 사용자 지정 리소스와 프로필 리소스 간의 관계가 이미 정의된 경우 워크플로우의 **조정** 활동에서 **조정 차원** 옵션을 사용 시 발생할 수 있는 오류를 수정했습니다.
* **조정** 또는 **데이터 보강** 활동을 통해 링크를 추가할 때 발생하는 문제를 해결했습니다. 선택한 링크가 출력 변환에 표시되지 않았습니다.
* 워크플로우에서 되풀이하는 게재와 함께 **세분화** 활동을 사용할 때 게재를 잘못된 대상자에게 보내는 문제를 해결했습니다. (CAMP-46275, CAMP-46470)
* 다이내믹 보고를 위한 사용자 지정 프로필 차원을 만들기 위해 프로필 리소스를 확장하려고 할 때 사용자 지정 리소스 게시가 실패하는 오류를 수정했습니다. (CAMP-46266)
* 파일 가져오기 테이블에 링크를 추가할 때 발생하는 오류를 수정했습니다. **데이터 보강** 활동을 **파일 가져오기** 활동에 추가한 후 이전에 구성된 링크가 사라졌습니다. (CAMP-46557)
* 저장 시 **세부 사항** 구성 화면의 표시 순서가 변경된 프로필 데이터에 연결된 사용자 지정 리소스를 사용할 때 발생하는 문제를 해결했습니다. (CAMP-46312)
* 사용자 지정 게재 매핑을 기반으로 하는 게재로 인해 다이내믹 보고에서 데이터를 표시하지 않는 문제를 해결했습니다.
* 워크플로우 **쿼리** 활동에서 잘못된 리소스 타겟이 있는 컬렉션을 선택할 수 없는 오류를 수정했습니다.
* InMail 프로세스에서 하드 바운스의 유효성을 잘못 확인할 수 있는 문제를 해결했습니다.
* 링크 오류로 인해 프로필 화면을 열 때 발생하는 오류를 수정했습니다.
* 정리 워크플로우에서 GDPR 데이터를 삭제하지 못하는 문제를 해결했습니다.
* 이메일 게재 예약 매개 변수에서 키보드로 예약 구성을 수동으로 업데이트할 때 발생하는 오류를 수정했습니다.
* 조직 단위의 잘못된 매개 변수로 인해 프로필을 편집할 수 없는 문제를 수정했습니다.
* 게재 템플릿에 설정되어 있더라도 **서비스** 확장 필드를 비우고 **이메일 속성**&#x200B;에 설정할 수 없는 문제를 수정했습니다.
* 증명을 처리하는 데 더 오래 걸릴 수 있는 문제를 수정했습니다. (CAMP-45048)
* 프로필 개요 화면에서 열을 정렬하지 못하는 문제를 해결했습니다.
* Azure에서 중국어 문자가 포함된 이메일의 변형이 발생할 수 있는 미리 보기 생성 문제를 해결했습니다. (CAMP-47152)
* Gmail 계정에서 받은 추적 이벤트 필터링으로 인해 Gmail에 대해 잘못된 공개 비율을 초래할 수 있는 Campaign 20.4에 도입된 회귀 문제를 해결했습니다. (CAMP-46504)
* HTML 콘텐츠를 트랜잭션 메시지 템플릿으로 가져올 수 없는 문제를 해결했습니다. (CAMP-47318)
* **이메일 렌더링 보고서**&#x200B;에서 렌더링 표시를 느리게 할 수 있는 문제를 해결했습니다. (CAMP-46226)
* 화면 정의에서 목록 유형 요소로 구성된 사용자 지정 리소스를 게시하지 못하는 문제를 해결했습니다. (CAMP-47217)
* 이메일 콘텐츠의 맨 위에 배치할 때 줄 디바이더 **Microsoft Outlook**&#x200B;에서 올바르게 렌더링되지 않는 이메일 디자이너의 문제를 해결했습니다. (CAMP-46294)
* **Adobe Analytics** 기술 워크플로우로 KPI 조정이 중단되는 문제를 해결했습니다. (CAMP-46576)
* 콘텐츠 블록을 삽입할 때 조각이 검색 상자에 자동으로 표시되지 않는 **이메일 디자이너**&#x200B;의 문제를 해결했습니다. (CAMP-44205)
* 조각에 이모지를 사용할 때 보낸 이메일에 원하지 않는 문자가 표시되던 **이메일 디자이너**&#x200B;의 문제를 해결했습니다. (CAMP-46621)
* 콘텐츠에서 행 높이 추가 및 이미지 왜곡을 초래하는 디바이더 구성 요소에 영향을 미치는 **이메일 디자이너**&#x200B;에서 20.4에 도입된 회귀 문제를 해결했습니다. (CAMP-46663)
* 메시지를 Outlook 사서함에 보낼 때 **이메일 디자이너**&#x200B;의 오른쪽 또는 왼쪽에 정렬되었더라도 기본 제공 단추를 중앙에 그대로 유지하는 문제를 해결했습니다. (CAMP-46466)
* **이메일 디자이너** 미리 보기에서 프로필을 검색할 때 테스트 프로필 목록이 새로 고침되지 않는 문제를 해결했습니다. (CAMP-45265)
* **이메일 디자이너** 미리 보기에서 프로필을 검색할 때 사용자 지정 테스트 프로필이 목록에 표시되지 않는 문제를 해결했습니다. (CAMP-45589)
* **게재 요약 보고서**&#x200B;에서 트렌드 그래픽을 생성할 때 일치하지 않는 날짜가 표시되는 문제를 해결했습니다. (CAMP-45521)