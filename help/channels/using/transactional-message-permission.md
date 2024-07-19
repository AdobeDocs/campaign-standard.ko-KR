---
title: 트랜잭션 메시지 권한
description: 트랜잭션 이벤트에 연결된 권한에 대해 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 995da330-6c86-444b-86b2-61d887f37db4
source-git-commit: 7247fe596494690ac0676196fbb72c6139aeb0c7
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 1%

---

# 트랜잭션 이벤트 개선 사항 {#transactional-event-improvements}

>[!AVAILABILITY]
>
>이러한 기능은 현재 조직 집합(제한된 가용성)에서만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하세요.

현재 Adobe Campaign Standard에서 관리자 보안 그룹이 없는 사용자는 트랜잭션 이벤트에 액세스, 만들기 또는 게시할 수 없으므로 이벤트를 구성하고 게시해야 하지만 관리자 권한이 없는 비즈니스 사용자에게 문제가 발생합니다. 또한 트랜잭션 이벤트를 복제할 수 없습니다.

다음과 같은 트랜잭션 메시지 액세스 제어 개선 사항을 구현했습니다.

* 관리자가 아닌 사용자가 트랜잭션 이벤트 구성을 관리할 수 있도록 **MC 사용자**&#x200B;라는 새 **[!UICONTROL Role]**&#x200B;을(를) 추가했습니다. **MC 사용자** 역할을 통해 이러한 사용자에게 트랜잭션 이벤트 및 메시지에 액세스하고, 만들고, 게시하고, 게시를 취소할 수 있는 권한을 부여합니다.

* 이제 실행 게재(즉, 트랜잭션 메시지를 편집하고 다시 게시할 때마다 또는 기본적으로 한 달에 한 번 만들어지는 기술 메시지)가 **메시지 센터 에이전트(mcExec)** 보안 그룹의 **[!UICONTROL Organizational unit]**(으)로 제한되지 않고 이벤트를 만드는 사용자가 속한 보안 그룹의 **[!UICONTROL Organizational unit]**(으)로 설정됩니다.

* **관리자**&#x200B;는 이벤트를 만든 사용자와 동일한 **조직 단위** 계층 구조에 있는 경우 게시된 트랜잭션 이벤트와 **MC 사용자** 역할을 가진 사용자를 복제할 수 있습니다.

## MC 사용자 역할 할당 {#assign-role}

보안 그룹에 **MC 사용자** 역할을 할당하려면 다음을 수행하십시오.

1. 새 **[!UICONTROL Security group]**&#x200B;을(를) 만들거나 기존 을(를) 업데이트하세요. [자세히 알아보기](../../administration/using/managing-groups-and-users.md).

1. 보안 그룹에 역할을 할당하려면 **[!UICONTROL Create element]**&#x200B;을(를) 클릭하십시오.

   ![](assets/event_access_1.png)

1. MC 사용자 **[!UICONTROL Role]**&#x200B;을(를) 선택하고 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

   >[!IMPORTANT]
   >
   > 운영자에게 MC 사용자 역할을 할당하면 이벤트를 게시 취소할 수 있으므로 주의해서 진행하십시오.

   ![](assets/event_access_2.png)

1. 구성이 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

이제 이 **[!UICONTROL Security group]**&#x200B;에 연결된 사용자가 트랜잭션 이벤트 및 메시지에 액세스하고 메시지를 만들고 게시할 수 있습니다.

## MC 사용자 보안 그룹 할당 {#assign-group}

1. Admin Console에서 **제품** 탭을 선택합니다.

1. **Adobe Campaign Standard**&#x200B;을(를) 선택한 다음 인스턴스를 선택합니다.

1. **제품 프로필** 목록에서 **MC 사용자** 그룹을 선택합니다.

1. **사용자 추가**&#x200B;를 클릭하고 이 제품 프로필에 추가하려는 프로필의 이름, 사용자 그룹 또는 전자 메일 주소를 입력합니다.

1. 추가한 후에는 **저장**&#x200B;을 클릭하세요.

이 **[!UICONTROL Security group]**&#x200B;에 추가된 사용자는 이제 트랜잭션 이벤트 및 메시지에 액세스하고 메시지를 만들고 게시할 수 있습니다.

## 중복 트랜잭션 이벤트 {#duplicate-transactional-events}

이제 이벤트가 **게시**&#x200B;된 경우 **관리자** 보안 그룹<!--([Functional administrators](../../administration/using/users-management.md#functional-administrators)?)-->이(가) 있는 사용자가 이벤트 구성을 복제할 수 있습니다.

또한 **MC 사용자** 역할을 가진 관리자가 아닌 사용자는 이제 이벤트 구성에 액세스할 수 있지만 복제할 권한은 해당 사용자가 속한 **조직 단위**&#x200B;에 의해 결정됩니다. 현재 사용자와 이벤트를 만든 사용자가 동일한 조직 단위 계층에 속하는 경우 중복이 허용됩니다.

예를 들어 &#39;프랑스 판매&#39; 조직 단위에 속하는 사용자가 이벤트 구성을 만드는 경우:

* 조직 단위가 &#39;Paris Sales&#39;인 다른 사용자는 이 이벤트를 복제할 수 있습니다. &#39;Paris Sales&#39;는 &#39;France Sales&#39; 조직 단위의 일부이기 때문입니다.

* 단, 조직 단위가 &#39;샌프란시스코 영업&#39;인 사용자는 &#39;샌프란시스코 영업&#39;이 &#39;프랑스 영업&#39; 조직 단위와 별개인 &#39;미국 영업&#39; 조직 단위 아래에 있으므로 이 작업을 수행할 수 없습니다.

이벤트 구성을 복제하려면 아래 단계를 따르십시오.

1. 왼쪽 상단 모서리에서 **Adobe** 로고를 클릭한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**&#x200B;을(를) 선택합니다.

1. 선택한 게시된 이벤트 구성 위에 마우스를 놓고 **[!UICONTROL Duplicate element]** 단추를 선택합니다.

   ![](assets/message-center_duplicate-button.png)

   >[!CAUTION]
   >
   >게시되지 않은 이벤트 구성은 복제할 수 없습니다. [자세히 알아보기](publishing-transactional-event.md)

1. 복제된 이벤트가 자동으로 표시됩니다. 원본 이벤트에 대해 정의한 구성과 동일한 구성이 포함되어 있지만 **[!UICONTROL Draft]** 상태입니다.

   ![](assets/message-center_duplicated-draft-event.png)

1. 해당 트랜잭션 메시지가 자동으로 만들어집니다. 액세스하려면 **[!UICONTROL Transactional messages]** > **[!UICONTROL Transactional messages]**(으)로 이동하십시오.

   ![](assets/message-center_duplicated-message.png)

1. 새로 복제된 메시지를 엽니다. 원본 메시지에 대해 정의한 디자인과 동일한 디자인이 포함되어 있지만 원본 트랜잭션 메시지가 게시된 경우에도 **[!UICONTROL Draft]** 상태가 있습니다.

   ![](assets/message-center_duplicated-draft-message.png)

1. 이제 이 메시지를 편집하고 개인화할 수 있습니다. [트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md)을 참조하세요.

## 영향 {#impacts}

아래 표는 이러한 개선 사항의 영향을 간략하게 설명합니다.

| 오브젝트 | 이 변경 전 | 이 변경 후 |
|:-: | :--: | :-:|
| 트랜잭션 이벤트 | **관리자** 보안 그룹 내의 사용자만 이벤트를 만들고 게시할 수 있습니다. | **MC 사용자** 역할을 사용하면 이벤트를 만들고 게시할 수 있습니다. |
| 트랜잭션 메시지 | 트랜잭션 메시지가 **메시지 센터 에이전트(mcExec)** 보안 그룹의 **조직 단위**(으)로 설정되어 있습니다. | 트랜잭션 메시지는 트랜잭션 이벤트/메시지를 만드는 사용자가 속한 보안 그룹의 **조직 단위**(으)로 설정됩니다. |
| 실행 게재 | 실행 게재가 **메시지 센터 에이전트(mcExec)** 보안 그룹의 **조직 단위**(으)로 설정됩니다. | 실행 게재는 트랜잭션 이벤트/메시지를 만드는 사용자가 속한 보안 그룹의 **조직 단위**(으)로 설정됩니다. |
| 게시된 트랜잭션 이벤트 | 어떤 사용자도 복제할 수 없습니다. | <ul><li>**관리자** 보안 그룹을 가진 사용자는 게시된 이벤트를 복제할 수 있습니다.</li> <li>**MC 사용자** 역할을 가진 사용자는 이벤트를 만든 사용자와 동일한 **조직 단위** 계층에 있는 경우 게시된 이벤트를 복제할 수 있습니다.</li></ul> |


<!--Transactional Message Templates| Transactional Message templates are set to the Organizational unit **All**. | Transaction Message Template will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.-->