---
title: 역할 목록
description: 사용자에게 지정할 수 있는 역할 목록을 확인합니다.
page-status-flag: 활성화 안 함
uuid: 128aaf9b-9b7d-49f3-9e1f-72e79a29baa0
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 관리
content-type: reference
topic-tags: 사용자 및 보안
discoiquuid: ceaa3c94-9e1a-4271-b443-b00b4068929f
context-tags: 역할,개요;역할,기본
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c321545b2f5fdc3ed43b9b943601008ff31fba6a

---


# 역할 목록{#list-of-roles}

기본적으로 Adobe Campaign은 사용자 및 사용자 그룹에 할당된 단일 인증을 정의할 수 있는 일련의 역할을 제공합니다. 조직의 구성 단위와 결합되어 역할을 통해 사용자는 인터페이스에 대한 필터링된 뷰를 볼 수 있고 다른 기능에 대한 액세스를 정의할 수 있습니다. 자세한 내용은 역할 및 [권한 테이블을](/help/administration/using/assets/acs_rights.pdf)참조하십시오.

![](assets/user_management_3.png)

역할은 **[!UICONTROL Administration > Users & Security > Roles]** 메뉴에서 관리할 수 있습니다.

기본 권한은 다음과 같습니다.

* **[!UICONTROL Administration]**:일반 관리 권한
* **[!UICONTROL Datamodel]**:발행물을 실행하고 맞춤형 리소스를 제작할 수 있습니다.
* **[!UICONTROL Export]**:데이터를 내보낼 수 있습니다.
* **[!UICONTROL Generic import]**:데이터에 대한 일반 가져오기를 실행할 수 있습니다. 이를 수행하려면 역할을 역할에 **[!UICONTROL Generic import]** 연결해야 합니다 **[!UICONTROL Workflow]** .
* **[!UICONTROL Prepare deliveries]**:게재를 생성, 수정, 준비 및 삭제할 수 있는 권한 이 역할을 가진 사용자는 배달을 준비할 수 있지만 보낼 수는 없습니다.
* **[!UICONTROL Start deliveries]**:전달을 생성, 수정, 준비, 전송 및 삭제할 수 있는 권한
* **[!UICONTROL Workflow]**:워크플로우를 생성, 수정, 시작 및 삭제할 수 있습니다. 이 역할을 가진 사용자는 워크플로우에서도 배달을 보낼 수 없습니다.

>[!CAUTION]
>
>이 **[!UICONTROL Deliverability]**, **[!UICONTROL Command execution]**, **[!UICONTROL Export]**&#x200B;및 **[!UICONTROL File access]** **[!UICONTROL Message Center push]** 역할은 Adobe 관리자의 내부용입니다. 사용자에게 허용되어서는 안 됩니다.

**관련 항목:**

* [액세스 관리 기본 정보](../../administration/using/about-access-management.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)

