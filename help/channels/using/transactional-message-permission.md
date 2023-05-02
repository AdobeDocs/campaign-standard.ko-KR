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
ht-degree: 0%

---

# 트랜잭션 이벤트 개선 사항 {#transactional-event-improvements}

>[!AVAILABILITY]
>
>이러한 기능은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

현재 Adobe Campaign Standard에서 관리자 보안 그룹이 없는 사용자는 트랜잭션 이벤트에 액세스, 만들기 또는 게시할 수 없으므로 이벤트를 구성하고 게시해야 하지만 관리자 권한이 없는 비즈니스 사용자에게 문제가 발생합니다. 또한 트랜잭션 이벤트를 복제할 수는 없습니다.

트랜잭션 메시지 액세스 제어에 다음과 같은 개선 사항을 구현했습니다.

* 새로운 **[!UICONTROL Role]**, 호출됨 **MC 사용자**&#x200B;관리자가 아닌 사용자가 트랜잭션 이벤트 구성을 관리할 수 있도록 이 추가되었습니다. 다음 **MC 사용자** 역할은 이러한 사용자에게 트랜잭션 이벤트 및 메시지에 액세스, 만들기, 게시 및 게시 취소할 수 있는 기능을 제공합니다.

* 이제 실행 게재(즉, 트랜잭션 메시지가 다시 편집되어 게시될 때마다 또는 기본적으로 한 달에 한 번)가 **[!UICONTROL Organizational unit]** 이벤트를 만드는 사용자가 속한 보안 그룹의 **[!UICONTROL Organizational unit]** 의 **메시지 센터 에이전트(mcExec)** 보안 그룹

* **관리자** 이제 게시된 트랜잭션 이벤트와 **MC 사용자** 같은 역할을 제공함 **조직 단위** 계층 은 이벤트를 만든 사용자입니다.

## MC 사용자 역할 할당 {#assign-role}

을(를) 할당하려면 **MC 사용자** 보안 그룹에 대한 역할:

1. 새 만들기 **[!UICONTROL Security group]** 또는 기존 항목을 업데이트합니다. [자세히 알아보기](../../administration/using/managing-groups-and-users.md)

1. 클릭 **[!UICONTROL Create element]** 보안 그룹에 역할을 할당하려면 다음을 수행하십시오.

   ![](assets/event_access_1.png)

1. MC 사용자를 선택합니다 **[!UICONTROL Role]** 을(를) 클릭합니다. **[!UICONTROL Confirm]**.

   >[!IMPORTANT]
   >
   > 연산자에 MC 사용자 역할을 할당할 때 주의하여 이벤트를 게시 취소할 수 있는 기능을 제공합니다.

   ![](assets/event_access_2.png)

1. 구성이 완료되면 을(를) 클릭합니다. **[!UICONTROL Save]**.

이 항목에 연결된 사용자 **[!UICONTROL Security group]** 이제 트랜잭션 이벤트 및 메시지에 액세스하고, 만들고, 게시할 수 있습니다.

## MC 사용자 보안 그룹 할당 {#assign-group}

1. Admin Console에서 **제품** 탭.

1. 선택 **Adobe Campaign Standard** 그런 다음 인스턴스를 선택합니다.

1. 에서 **제품 프로필** 목록에서 을 선택합니다. **MC 사용자** 그룹에 속해 있어야 합니다.

1. 클릭 **사용자 추가** 및 이 제품 프로필에 추가할 프로필의 이름, 사용자 그룹 또는 이메일 주소를 입력합니다.

1. 추가한 후에는 **저장**.

여기에 추가된 사용자 **[!UICONTROL Security group]** 이제 트랜잭션 이벤트 및 메시지에 액세스하고, 만들고, 게시할 수 있습니다.

## 중복된 트랜잭션 이벤트 {#duplicate-transactional-events}

을 사용하는 사용자 **관리자** 보안 그룹<!--([Functional administrators](../../administration/using/users-management.md#functional-administrators)?)--> 이제 이벤트가 발생한 경우 이벤트 구성을 복제할 수 있습니다 **게시됨**.

또한 관리자가 아닌 사용자가 **MC 사용자** 이제 역할은 이벤트 구성에 액세스할 수 있지만 중복에 대한 권한은 **조직 단위** 그들은 속한 사람들이다. 현재 사용자와 이벤트를 만든 사용자가 동일한 조직 단위 계층에 속하는 경우 중복을 수행할 수 있습니다.

예를 들어 &#39;France Sales&#39; 조직 단위에 속하는 사용자가 이벤트 구성을 만드는 경우:

* 조직 단위가 &#39;Paris Sales&#39;인 다른 사용자는 &#39;Paris Sales&#39;가 &#39;France Sales&#39; 조직 단위에 속하기 때문에 이 이벤트를 복제할 수 있습니다.

* 그러나 조직단위가 샌프란시스코 판매인 사용자는 이를 수행할 수 없다. 샌프란시스코 매출부는 프랑스 영업 조직과는 별개인 미국 판매 조직부에 있기 때문이다.

이벤트 구성을 복제하려면 아래 단계를 따르십시오.

1. 을(를) 클릭합니다. **Adobe** 왼쪽 상단 모서리에서 로고를 선택한 다음 **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**.

1. 마우스를 선택한 게시된 이벤트 구성 위로 가져간 후 **[!UICONTROL Duplicate element]** 버튼을 클릭합니다.

   ![](assets/message-center_duplicate-button.png)

   >[!CAUTION]
   >
   >게시되지 않은 이벤트 구성은 복제할 수 없습니다. [자세히 알아보기](publishing-transactional-event.md)

1. 복제한 이벤트가 자동으로 표시됩니다. 여기에는 원래 이벤트에 대해 정의한 구성과 동일하지만 **[!UICONTROL Draft]** 상태.

   ![](assets/message-center_duplicated-draft-event.png)

1. 해당 트랜잭션 메시지가 자동으로 만들어집니다. 액세스하려면 다음 위치로 이동하십시오. **[!UICONTROL Transactional messages]** > **[!UICONTROL Transactional messages]**.

   ![](assets/message-center_duplicated-message.png)

1. 새로 복제한 메시지를 엽니다. 원본 메시지에 대해 정의한 것과 동일한 디자인이 포함되어 있지만 **[!UICONTROL Draft]** 원래 트랜잭션 메시지가 게시되었더라도 상태로 유지됩니다.

   ![](assets/message-center_duplicated-draft-message.png)

1. 이제 이 메시지를 편집하고 개인화할 수 있습니다. 자세한 내용은 [트랜잭션 메시지 편집](../../channels/using/editing-transactional-message.md).

## 영향 {#impacts}

아래 표는 이러한 개선 사항의 영향을 간략하게 설명합니다.

| 개체 | 이 변경 전 | 이 변경 후 |
|:-: | :--: | :-:|
| 트랜잭션 이벤트 | 내의 사용자만 **관리자** 보안 그룹은 이벤트를 만들고 게시할 수 있습니다. | 다음 **MC 사용자** 역할을 사용하면 이벤트를 만들고 게시할 수 있습니다. |
| 트랜잭션 메시지 | 트랜잭션 메시지는 **조직 단위** 의 **메시지 센터 에이전트(mcExec)** 보안 그룹 | 트랜잭션 메시지는 **조직 단위** 트랜잭션 이벤트/메시지를 만드는 사용자가 속한 보안 그룹의 이름입니다. |
| 실행 게재 | 실행 게재는 **조직 단위** 의 **메시지 센터 에이전트(mcExec)** 보안 그룹 | 실행 게재는 **조직 단위** 트랜잭션 이벤트/메시지를 만드는 사용자가 속한 보안 그룹의 이름입니다. |
| 게시된 트랜잭션 이벤트 | 사용자는 복제할 수 없습니다. | <ul><li>을 사용하는 사용자 **관리자** 보안 그룹이 게시된 이벤트를 복제할 수 있습니다.</li> <li>을 사용하는 사용자 **MC 사용자** 게시된 이벤트가 같은 경우 역할이 복제 가능 **조직 단위** 계층 은 이벤트를 만든 사용자입니다.</li></ul> |


<!--Transactional Message Templates| Transactional Message templates are set to the Organizational unit **All**. | Transaction Message Template will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.-->