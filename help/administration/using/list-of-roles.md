---
title: 역할 목록
seo-title: 역할 목록
description: 역할 목록
seo-description: 사용자에게 할당할 수 있는 역할 목록을 확인합니다.
page-status-flag: 정품 인증 안 함
uuid: 128 AAF 9 B -9 B 7 D -49 F 3-9 E 1 F -72 E 79 A 29 BAA 0
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: 사용자 및 보안
discoiquuid: CEAA 3 C 94-9 E 1 A -4271-B 443-B 00 B 4068929 F
context-tags: 역할, 개요; 역할, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# List of roles{#list-of-roles}

기본적으로 Adobe Campaign 에서는 사용자 및 사용자 그룹에 할당된 일회성 인증을 정의할 수 있는 일련의 역할을 제공합니다. 조직 단위와 결합된 역할은 사용자에게 인터페이스의 필터링된 보기를 제공하고 다른 기능에 대한 액세스 권한을 정의합니다. For more on this, refer to the [Roles and permissions table](https://docs.campaign.adobe.com/doc/standard/en/Technotes/AdobeCampaign-ACSRights.pdf).

![](assets/user_management_3.png)

Roles can be managed from the **[!UICONTROL Administration > Users & Security > Roles]** menu.

기본 권리는 다음과 같습니다.

* **[!UICONTROL Administration]**: 일반 관리 권한.
* **[!UICONTROL Datamodel]**: 발행물을 실행하고 사용자 지정 리소스를 만드는 권한.
* **[!UICONTROL Export]**: 데이터 내보내기 권한.
* **[!UICONTROL Generic import]**: 데이터에 대한 일반 가져오기를 실행하는 권한. For this to work, you need to link the **[!UICONTROL Generic import]** role to the **[!UICONTROL Workflow]** role.
* **[!UICONTROL Prepare deliveries]**: 제작 준비, 편집, 전달 준비 및 증거 자료 전송
* **[!UICONTROL Start deliveries]**: 이전에 준비된 배달을 확인할 권리.
* **[!UICONTROL Workflow]**: 워크플로우 사용 권한.

>[!CAUTION]
>
>배달 가능성 역할은 Adobe 관리자에게만 사용됩니다. 사용자에게 부여되면 안 됩니다.

**관련 항목:**

* [액세스 관리 정보](../../administration/using/about-access-management.md)
* [그룹 및 사용자 관리](../../administration/using/managing-groups-and-users.md)

