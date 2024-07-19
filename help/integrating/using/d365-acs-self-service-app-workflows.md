---
title: 통합 애플리케이션 워크플로
description: Campaign과 Dynamics 통합 워크플로
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 51f07f08-5d57-4c4c-aff2-d03e5956ec6f
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Campaign - Microsoft Dynamics 365 통합 워크플로

**[!UICONTROL Workflows]** 페이지에 기술 워크플로우와 해당 상태가 나열됩니다.

통합 애플리케이션은 다음 세 가지 워크플로우와 함께 제공됩니다.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows.png)

Campaign에 대한 **Microsoft Dynamics 365**
* Microsoft Dynamics 365에서 Adobe Campaign으로 *연락처* 보내기
* *사용자 지정 엔터티*: Microsoft Dynamics 365에서 Adobe Campaign으로 사용자 지정 테이블을 가져옵니다. [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#data-flows)
* 이를 **수신**(Microsoft Dynamics 365에서 Adobe Campaign으로의 데이터 수신 참조)이라고도 합니다

Microsoft Dynamics 365에 대한 **캠페인**
* Adobe Campaign Standard의 이메일 마케팅 이벤트는 Dynamics 365로 전송됩니다(이메일 전송, 열기, 클릭, 바운스). [자세히 알아보기](../../integrating/using/d365-acs-using-the-integration.md#email-marketing-event-flow)
* 이를 **이그레스**(Adobe Campaign에서 Microsoft Dynamics 365로의 데이터 이그레스 참조)라고도 합니다

**옵트인/옵트아웃**

옵트아웃 상태(예: Adobe Campaign)는 Microsoft Dynamics 365에서 차단 목록에 추가하다으로 또는 Adobe Campaign에서 Microsoft Dynamics 365로 동기화할 수 있습니다. 데이터는 또한 양방향으로 동기화(즉, 양방향으로 데이터 흐름)될 수 있다. [자세히 알아보기](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!IMPORTANT]
>
>Adobe Campaign Standard 또는 Microsoft Dynamics 365에 변경 내용을 게시하기 전에 **Microsoft Dynamics 365에서 Campaign**&#x200B;으로 워크플로를 중지하는 것이 좋습니다. 이러한 변경 사항에는 현재 통합에서 사용 중인 리소스/엔티티(및 관련 필드), 링크, 식별자 열 등에 대한 업데이트가 포함됩니다. 이렇게 하지 않으면 데이터가 손실되거나 워크플로우가 예기치 않게 중지될 수 있습니다.

## 워크플로 백로그

이 통합 애플리케이션은 먼저 데이터를 읽은 다음 데이터를 대상에 기록합니다. **[!UICONTROL Backlog]** 열은 큐에 올라가 쓰기 대기 중인 레코드 수를 나타냅니다. 처리할 데이터가 많으면(예: 통합을 처음 실행 중이거나 데이터를 재실행 중인 경우 등) 이 값은 증가할 것으로 예상됩니다.

>[!NOTE]
>Microsoft Dynamics 365 및/또는 Campaign 레코드가 업데이트되지 않는 경우 먼저 대상에 쓰기 대기 중인 레코드가 많은지 확인해야 합니다.
>

## 워크플로 상태 {#workflow-status}

**[!UICONTROL Status]** 열은 워크플로와 연결된 백그라운드 프로세스의 상태를 나타냅니다. 가능한 값:

* **실행 중**: 프로세스가 현재 실행 중이므로 데이터를 동기화해야 합니다.
* **STOPPED**: 프로세스가 현재 실행되고 있지 않으므로 데이터를 동기화해서는 안 됩니다.
* **시작**: 워크플로 프로세스를 시작하도록 요청했습니다. 응용 프로그램이 아직 이 워크플로와 연결된 데이터 동기화를 시작하지 않았지만 몇 분 후에(**RUNNING** 상태가 표시될 때) 시작될 것으로 예상됩니다.
* **실패**: 워크플로 프로세스가 실행 중이지만 오류가 발생하여 이 프로세스에서 복구할 수 없습니다.

## 사용 가능한 작업

가능한 작업은 아래에 나와 있습니다.

* **편집**: 연필 아이콘을 클릭하면 워크플로우를 업데이트할 수 있는 다른 페이지로 이동합니다. 변경 사항은 워크플로우를 중지한 다음 다시 시작할 때까지 적용되지 않습니다.

* **시작**: 시작 단추는 중지된 워크플로의 시작을 요청합니다. 이 단추는 워크플로와 연결된 프로세스가 현재 중지된 경우에만 나타납니다. 프로세스는 먼저 &quot;시작&quot;으로 변경된 다음 &quot;실행&quot;으로 변경됩니다. 워크플로우가 &quot;실행 중&quot; 상태가 될 때까지 워크플로우와 연결된 데이터가 동기화를 시작하지 않습니다.

  시작 버튼은 토글(toggle)입니다. 워크플로 프로세스가 이미 시작된 경우 단추가 **중지** 단추로 변경됩니다.

* **중지**: **중지** 단추는 실행 중인 워크플로의 중지를 요청합니다. 이 단추는 워크플로와 연결된 프로세스가 현재 실행 중인 경우에만 나타납니다.

워크플로를 편집할 때 워크플로를 중지하고 **시작** 단추를 클릭하기 전까지는 업데이트가 실행 중인 프로세스 규칙에 즉시 통합되지 않습니다. 그런 다음 업데이트가 실행 중인 프로세스에 통합됩니다(프로세스가 **RUNNING** 상태로 돌아간 후).

**중지** 단추에 경고 표시가 추가되어 (a) 워크플로우를 업데이트했지만 (b) 이 워크플로우의 중지/시작을 완료하지 않은 경우 알려줍니다.

![](assets/do-not-localize/d365-to-acs-icon-stop-with-changes.png)
