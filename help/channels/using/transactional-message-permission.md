---
title: 트랜잭션 메시지 권한
description: 트랜잭션 이벤트에 연결된 권한에 대해 알아봅니다.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
hide: true
hidefromtoc: true
feature: Transactional Messaging
role: User
level: Intermediate
source-git-commit: d7e0912dd7d19a1f5dd2172235f28a40e130cac1
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# 트랜잭션 메시지 권한 {#transactional-message-permission}

현재 Adobe Campaign Standard에서 관리자 보안 그룹이 없는 사용자는 이벤트에 액세스, 만들기 또는 게시할 수 없으므로 이벤트를 구성하고 게시해야 하지만 관리자 권한이 없는 비즈니스 사용자에게 문제가 발생합니다.

트랜잭션 메시지 액세스 제어에 다음과 같은 개선 사항을 구현했습니다.

* 새로운 **[!UICONTROL Role]**, 호출됨 **MC 사용자**&#x200B;관리자가 아닌 사용자가 트랜잭션 이벤트를 관리할 수 있도록 이 추가되었습니다. 다음 **MC 사용자** 역할은 이러한 사용자에게 트랜잭션 이벤트 및 메시지에 액세스, 만들기, 게시 및 게시 취소할 수 있는 기능을 제공합니다.

* 이제 하위 게재가 **[!UICONTROL Organizational unit]** 메시지 템플릿을 만드는 사용자가 속한 보안 그룹의 **[!UICONTROL Organizational unit]** 의 **메시지 센터 에이전트(mcExec)** 보안 그룹

* 기본값 **메시지 센터 실행(mcExec)** 트랜잭션 메시지 하위 게재를 수집하는 캠페인이 이제 조직 단위로 설정됩니다 **모두** 모든 사용자가 하위 게재 보고서를 볼 수 있도록 허용.

을(를) 할당하려면 **MC 사용자** 역할:

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

아래 표에서는 이 기능이 액세스 제어에 미치는 영향에 대해 설명합니다.

| 개체 | 이 변경 전 | 이 변경 후 |
|:-: | :--: | :-:|
| 메시지 센터 실행(mcExec) 캠페인 | **메시지 센터 실행(mcExec)** 캠페인이 **메시지 센터 에이전트(mcExec)** 보안 그룹 | **메시지 센터 실행(mcExec)** 캠페인이 조직 단위로 설정되어 있습니다. **모두** 모든 하위 게재를 이 캠페인과 연결할 수 있도록 합니다.</br> 모든 사용자는 하위 게재 보고서를 볼 수 있지만 게재 컨텐츠에 대한 읽기 전용 액세스 권한만 갖게 됩니다. |
| 하위 게재 | 하위 게재는 **조직 단위** 의 **메시지 센터 에이전트(mcExec)** 보안 그룹 | 하위 게재는 **조직 단위** 메시지 템플릿을 만드는 사용자가 속한 보안 그룹의 이름입니다. |
| 메시지 템플릿 | 메시지 템플릿은 **조직 단위** 의&#x200B;**메시지 센터 에이전트(mcExec)** 보안 그룹 | 메시지 템플릿이 **조직 단위** 메시지 템플릿을 만드는 사용자가 속한 보안 그룹의 이름입니다. |
| 트랜잭션 이벤트 | 내의 사용자만 **관리자** 보안 그룹은 이벤트를 만들고 게시할 수 있습니다. | 다음 **MC 사용자** 역할을 사용하면 이벤트를 만들고 게시할 수 있습니다. |
| 트랜잭션 메시지 템플릿 | 트랜잭션 메시지 템플릿은 조직 단위로 설정됩니다 **모두**. | 트랜잭션 메시지 템플릿이 **조직 단위** 메시지 템플릿을 만드는 사용자가 속한 보안 그룹의 이름입니다. |