---
title: 역할 목록
description: 사용자에게 지정할 수 있는 역할 목록을 확인합니다.
page-status-flag: never-activated
uuid: 128aaf9b-9b7d-49f3-9e1f-72e79a29baa0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: ceaa3c94-9e1a-4271-b443-b00b4068929f
context-tags: role,overview;role,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 395791e69d0c4c8a888829539338e338387294de
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# 역할 목록{#list-of-roles}

기본적으로 Adobe Campaign은 사용자 및 사용자 그룹에 할당된 단일 인증을 정의할 수 있는 일련의 역할을 제공합니다.

조직의 구성 단위와 결합된 역할은 사용자에게 인터페이스에 대한 필터링된 보기를 제공하고 다양한 기능에 대한 액세스를 정의합니다.

여기에 대한 자세한 내용은 선택한 인증에 따라 인터페이스에서 사용할 수 있는 기능에 대한 [세부 정보를 제공하는 역할 및 권한 테이블을](/help/administration/using/assets/acs_rights.pdf)참조하십시오.

[![이미지](assets/user_management_3.png)](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/users-and-security/assets/acs_rights.pdf)

역할은 **[!UICONTROL Administration > Users & Security > Roles]** 메뉴에서 관리할 수 있습니다.

기본 권한은 다음과 같습니다.

* **[!UICONTROL Administration]**: 범용 관리 권한
* **[!UICONTROL Datamodel]**: 발행물을 실행하고 맞춤형 리소스를 제작할 수 있습니다.
* **[!UICONTROL Generic import]**: 데이터에 대한 일반 가져오기를 실행할 수 있습니다. 이를 수행하려면 역할을 역할에 **[!UICONTROL Generic import]** 연결해야 **[!UICONTROL Workflow]** 합니다.
* **[!UICONTROL Prepare deliveries]**: 게재를 생성, 수정, 준비 및 삭제할 권리. 이 역할을 가진 사용자는 배달을 준비할 수 있지만 보낼 수는 없습니다.
* **[!UICONTROL Start deliveries]**: 전달 생성, 수정, 준비, 전송 및 삭제할 수 있는 권한
* **[!UICONTROL Workflow]**: 워크플로우 실행을 관리할 권한(시작, 중지, 일시 중지 등) 이 역할을 가진 사용자는 워크플로우에서도 배달을 보낼 수 없습니다.

**관련 항목:**

* [액세스 관리 기본 정보](../../administration/using/about-access-management.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)
