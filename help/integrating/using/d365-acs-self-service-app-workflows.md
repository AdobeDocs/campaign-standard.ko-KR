---
title: 통합 애플리케이션 워크플로우
description: Campaign 및 Dynamics 통합 워크플로우
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 51f07f08-5d57-4c4c-aff2-d03e5956ec6f
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# 캠페인 - Microsoft Dynamics 365 통합 워크플로우

다음 **[!UICONTROL Workflows]** 페이지에는 기술 워크플로우 및 해당 상태가 나열됩니다.

통합 애플리케이션은 다음 세 가지 워크플로우와 함께 제공됩니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows.png)

**Microsoft Dynamics 365에서 Campaign으로**
* 보내기 *연락처* Microsoft Dynamics 365에서 Adobe Campaign으로
* *사용자 지정 엔티티*: Microsoft Dynamics 365에서 Adobe Campaign으로 사용자 지정 테이블을 가져옵니다. [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#data-flows)
* 이것을 라고 합니다 **수신** (Microsoft Dynamics 365에서 Adobe Campaign으로 데이터 수신 참조)

**Campaign에서 Microsoft Dynamics 365로**
* Adobe Campaign Standard의 이메일 마케팅 이벤트가 Dynamics 365로 전송됩니다(이메일 전송, 열기, 클릭, 바운스). [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#email-marketing-event-flow)
* 이것을 라고 합니다 **송신** (Adobe Campaign에서 Microsoft Dynamics 365로의 데이터 송신 참조)

**옵트인/옵트아웃**

옵트아웃 상태(예:)는 Microsoft Dynamics 365에서 Adobe Campaign으로 또는 Adobe Campaign에서 Microsoft Dynamics 365로 동기화할 수 있습니다차단 목록. 데이터는 양방향(즉, 양방향으로 데이터 흐름)으로 동기화될 수도 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf)

>[!IMPORTANT]
>
>를 중지하는 것이 좋습니다 **Microsoft Dynamics 365에서 Campaign으로** Adobe Campaign Standard 또는 Microsoft Dynamics 365에 변경 사항을 게시하기 전 워크플로우입니다. 이러한 변경 사항에는 현재 통합에서 사용 중인 리소스/엔티티(및 관련 필드), 링크, 식별자 열 등에 대한 업데이트가 포함됩니다. 설정하지 않으면 데이터 손실이 발생하고/또는 워크플로우가 예기치 않게 중지될 수 있습니다.

## 워크플로우 백로그

이 통합 애플리케이션은 먼저 데이터를 읽은 다음 대상에 데이터를 기록합니다. 다음 **[!UICONTROL Backlog]** 열은 큐에 있고 쓰기 대기 중인 레코드 수를 나타냅니다. 이 값은 처리할 대량의 데이터가 있을 때 증가할 것으로 예상됩니다(예: 통합을 처음 실행하고 데이터 재재생 등).

>[!NOTE]
>Microsoft Dynamics 365 및/또는 Campaign 레코드가 업데이트되지 않는 경우 먼저 대상에 기록되기를 기다리는 레코드 수가 많은지 확인해야 합니다.

## 워크플로우 상태 {#workflow-status}

다음 **[!UICONTROL Status]** 열은 워크플로우와 연관된 백그라운드 프로세스의 상태를 나타냅니다. 가능한 값은 다음과 같습니다.

* **실행 중**: 프로세스가 현재 실행 중이며 데이터를 동기화해야 합니다.
* **중지됨**: 프로세스가 현재 실행 중이 아니므로 데이터를 동기화해서는 안 됩니다.
* **시작**: 워크플로우 프로세스를 시작하도록 요청했습니다. 애플리케이션이 이 워크플로우와 연관된 데이터를 아직 동기화하지 않았지만 몇 분 후에(그런 다음 상태가 표시될 때) **실행 중**)
* **실패**: 워크플로우 프로세스가 실행 중이지만 오류가 발생하여 이 프로세스에서 복구할 수 없습니다.

## 사용 가능한 작업

가능한 작업은 아래에 나열되어 있습니다.

* **편집**: 연필 아이콘을 클릭하면 워크플로우를 업데이트할 수 있는 다른 페이지로 이동합니다. 변경한 내용은 워크플로우를 중지한 다음 다시 시작할 때까지 적용되지 않습니다.

* **시작**: 시작 단추를 사용하면 중지된 워크플로우를 시작할 수 있습니다. 이 단추는 워크플로우와 연관된 프로세스가 현재 중지된 경우에만 나타납니다. 프로세스가 먼저 &quot;시작&quot;으로 변경된 다음 &quot;실행 중&quot;으로 변경됩니다. 워크플로우가 &quot;실행 중&quot; 상태가 될 때까지 워크플로우와 연관된 데이터가 동기화를 시작하지 않습니다.

   시작 버튼은 토글 단추입니다. 워크플로우 프로세스가 이미 시작된 경우에는 버튼이 로 변경됩니다 **정지** 버튼을 클릭합니다.

* **정지**: A **정지** 버튼은 실행 중인 워크플로우를 중지할 것을 요청합니다. 이 단추는 워크플로우와 연관된 프로세스가 현재 실행 중인 경우에만 나타납니다.

워크플로우를 편집하면 워크플로우를 중지하고 를 클릭하기 전까지 업데이트가 실행 중인 프로세스의 규칙에 즉시 통합되지 않습니다. **시작** 버튼을 클릭합니다. 그러면 업데이트가 실행 중인 프로세스에 통합됩니다(프로세스가 **실행 중** state).

에 경고 표시가 추가됩니다 **정지** (a) 워크플로우를 업데이트했지만 (b) 이 워크플로우의 중지/시작을 수행하지 않은 경우를 알리는 단추입니다.

![](assets/do-not-localize/d365-to-acs-icon-stop-with-changes.png)
