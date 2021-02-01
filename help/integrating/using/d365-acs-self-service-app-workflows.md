---
title: 통합 애플리케이션 워크플로우
description: 캠페인 및 Dynamics 통합 워크플로우
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: efa30d7ed4a0caf929da6f485681078318849cda
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---


# 캠페인 - Microsoft Dynamics 365 통합 워크플로우

**[!UICONTROL Workflows]** 페이지에는 기술 워크플로우와 해당 상태가 나열됩니다.

통합 애플리케이션에는 3개의 워크플로우가 포함되어 있습니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows.png)

**Microsoft Dynamics 365에서 Campaign으로 전환**
* Microsoft Dynamics 365에서 Adobe Campaign으로 *연락처* 보내기
* *사용자 지정 엔티티*:Microsoft Dynamics 365에서 Adobe Campaign으로 사용자 정의 표를 가져올 수 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#data-flows)
* 이 이름은 **Ingress**(Microsoft Dynamics 365에서 Adobe Campaign으로 데이터 수신 참조)이라고도 합니다.

**Microsoft Dynamics 365로 캠페인 전환**
* Adobe Campaign Standard의 이메일 마케팅 이벤트가 Dynamics 365로 전송됩니다(이메일 전송, 열기, 클릭, 바운스). [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#email-marketing-event-flow)
* 이 이름은 **Egress**(Adobe Campaign에서 Microsoft Dynamics 365로 데이터 송신 참조)이라고도 합니다.

**옵트인/옵트아웃**

옵트아웃 상태(예:)는 Microsoft Dynamics 365에서 Adobe Campaign으로 또는 Adobe Campaign에서 Microsoft Dynamics 365로 동기화할 수 있습니다차단 목록. 데이터는 양방향(즉, 두 방향으로 데이터 흐름)으로 동기화될 수도 있습니다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf)

>[!IMPORTANT]
>
>Adobe Campaign Standard 또는 Microsoft Dynamics 365에 변경 내용을 게시하기 전에 **Microsoft Dynamics 365에서 Campaign** 작업 과정을 중지하는 것이 좋습니다. 이러한 변경 사항에는 현재 통합에서 사용 중인 리소스/개체(및 관련 필드), 링크, 식별자 열 등에 대한 업데이트가 포함됩니다. 이렇게 하지 않으면 데이터 손실 및/또는 워크플로우가 예기치 않게 중지될 수 있습니다.

## 워크플로우 백로그

이 통합 응용 프로그램은 먼저 데이터를 읽은 다음 대상에 데이터를 씁니다. **[!UICONTROL Backlog]** 열은 큐에 올라가 있고 쓰기를 기다리고 있는 레코드 수를 나타냅니다. 처리할 대량의 데이터가 있을 때 이 값이 증가할 것으로 예상됩니다(예: 처음으로 통합을 실행하고 있거나 데이터를 다시 재생하고 있는 경우 등).

>[!NOTE]
>Microsoft Dynamics 365 및/또는 Campaign 레코드가 업데이트되지 않는 경우 먼저 대상에 기록되기를 기다리는 레코드 수가 많은지 확인해야 합니다.


## 워크플로 상태 {#workflow-status}

**[!UICONTROL Status]** 열은 워크플로우와 연관된 백그라운드 프로세스의 상태를 나타냅니다. 가능한 값은 다음과 같습니다.

* **실행**:프로세스가 현재 실행 중이며 데이터를 동기화해야 합니다.
* **중지됨**:프로세스가 현재 실행되고 있지 않으므로 데이터를 동기화해서는 안 됩니다.
* **시작**:워크플로우 프로세스를 시작하도록 요청했습니다. 응용 프로그램이 이 워크플로와 연결된 데이터를 아직 동기화하지 않았지만 몇 분 후에 동기화될 것으로 예상할 수 있습니다(그런 다음 **RUNNING** 상태가 표시됩니다).
* **실패**:워크플로 프로세스가 실행 중이지만 오류가 발생하여 이 프로세스에서 복구할 수 없습니다.

## 사용 가능한 작업

가능한 작업이 아래에 나열되어 있습니다.

* **편집**:연필 아이콘을 클릭하면 워크플로우를 업데이트할 수 있는 다른 페이지로 이동합니다. 변경 사항은 워크플로우를 중지한 다음 다시 시작해야 적용됩니다.

* **시작**:시작 단추를 사용하여 중지된 워크플로우를 시작할 수 있습니다. 이 단추는 워크플로우와 연관된 프로세스가 현재 중지된 경우에만 나타납니다. 프로세스는 먼저 &quot;시작&quot;으로 변경된 다음 &quot;실행&quot;으로 변경됩니다. 워크플로우가 &quot;실행 중&quot; 상태가 될 때까지 워크플로와 연관된 데이터가 동기화를 시작하지 않습니다.

   시작 단추는 전환입니다. 워크플로 프로세스가 이미 시작된 경우 단추가 **중지** 단추로 바뀝니다.

* **중지**:정지  **** 단추를 사용하여 실행 중인 작업 흐름을 중지할 것을 요청합니다. 이 단추는 워크플로우와 연관된 프로세스가 현재 실행 중인 경우에만 나타납니다.

워크플로우를 편집하면 워크플로우를 중지한 다음 **시작** 단추를 클릭할 때까지 업데이트가 실행 중인 프로세스의 규칙에 즉시 통합되지 않습니다. 그런 다음 업데이트 내용이 실행 프로세스에 통합됩니다(프로세스가 **RUNNING** 상태로 돌아오면).

작업 과정을 업데이트했지만 (b) 이 작업 과정의 중지/시작을 수행하지 않은 경우 알려 주는 경고 표시가 **중지** 단추에 추가됩니다.

![](assets/do-not-localize/d365-to-acs-icon-stop-with-changes.png)
