---
title: 액세스 관리 기본 정보
description: 역할, 그룹 및 조직 단위를 사용하여 Adobe Campaign 연산자를 관리합니다.
page-status-flag: never-activated
uuid: 4f538452-cc67-4e03-9e2f-2d9eecc081c7
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: 54028f63-c9ca-4397-a079-e27e0cfdebf6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d0a0c59763af8babc9701206cc39fe41b98e0cd4
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---


# SyncWithLaunch 기술 워크플로우 FAQ {#syncwithlaunch-faq}

이 **[!UICONTROL Sync with Launch]** 워크플로우를 통해 모든 Adobe Launch 모바일 속성을 Adobe Campaign Standard으로 자동으로 가져올 수 있습니다.

자세한 내용은 이 [페이지를 참조하십시오](../../administration/using/technical-workflows.md).

>[!NOTE]
>
>Adobe 고객 지원 센터(직접 또는 Adobe 담당자를 통해)에 티켓을 제출하여 Campaign 인스턴스에서 **[!UICONTROL syncWithLaunch]** 기술 워크플로우를 활성화해야 합니다.

## (조직 단위 ALL의 비관리 [!DNL Launch] 로) 속성을 만들었습니다. 내 애플리케이션이 Adobe Campaign에서 구성 준비 상태에 있지만 해당 상태를 열거나 구성할 수 없습니다. {#configuring-property}

조직 구성 단위 ALL의 관리자만 Adobe Campaign Standard에서 모바일 애플리케이션을 구성할 수 있습니다. 구성한 후에는 지정된 조직 구성 단위의 사용자만 애플리케이션을 편집할 수 있습니다. 조직 구성 요소에 대한 자세한 내용은 이 [페이지를 참조하십시오](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 구성된 모바일 응용 프로그램을 편집할 수 없으며 모바일 응용 프로그램은 읽기 모드입니다. {#read-mode-mobile-app}

섹션에서 모바일 애플리케이션의 구성 요소를 **[!UICONTROL Access Authorization ]** 확인합니다. 지정된 조직 구성 단위의 사용자만 모바일 응용 프로그램을 편집할 수 있습니다.

조직 구성 요소에 대한 자세한 내용은 이 [페이지를 참조하십시오](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 조직 단위 ALL을 사용하는 관리자이지만 모바일 애플리케이션을 구성할 수 없습니다. {#org-unit-mobile}

조직 단위가 모두(ALL)로 설정된 관리자는 모바일 애플리케이션을 구성하려면 모든 모바일 속성 [!DNL Launch] 에 대한 권한이 있어야 합니다.

조직 구성 요소에 대한 자세한 내용은 이 [페이지를 참조하십시오](../../administration/using/organizational-units.md).

## 모바일 속성을 만들었지만 내 속성이 Adobe Campaign Standard에 표시되지 [!DNL Launch] 않습니다. {#visibility-mobile-property}

1. Adobe Campaign Standard 확장이 [!DNL Launch]

1. 인스턴스의 끝점이 확장자에 올바르게 구성되어 있는지 확인합니다.

1. &#39;Launch_URL_Campaign&#39; 또는 &#39;NmsServer_URL&#39;이 올바른지 확인하십시오.

1. 그런 다음 기술 워크플로우에서 [!DNL Launch] Adobe Campaign과 간의 동기화가 완료되었는지 **[!UICONTROL syncWithLaunch]** 확인하십시오.

## Adobe Campaign과 론치 간 동기화가 완료되었는지 확인하는 방법 {#sync-campaign-launch}

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;을 선택합니다.

1. 워크플로우를 **[!UICONTROL syncWithLaunch]** 엽니다.

1. 워크플로우가 오류 없이 끝났는지 확인합니다.

1. 워크플로우 동기화가 활성화되고 성공적으로 완료되었는지 로그를 확인합니다.

## Launch에서 구성된 모바일 응용 프로그램의 키를 재설정합니다. Launch에서 키를 다시 구성하는 방법 {#configuring-pkey}

1. Adobe Launch에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장명에 새 URL을 설정합니다.

1. 파일을 저장하고 Adobe Campaign과 워크플로우 간에 워크플로우를 동기화할 수 있습니다 [!DNL Launch].

1. 동기화가 완료되면 모바일 속성을 엽니다 [!DNL Launch].

1. PKey가 재설정된 Adobe Campaign Standard 확장자에서 올바른 URL을 설정합니다.

1. 저장하여 워크플로우 동기화를 다시 실행할 수 있습니다.

1. 그래야 속성이 Adobe Campaign의 **[!UICONTROL Ready to Configure]** 상태로 표시되고 구성할 수 있습니다.

## Adobe Campaign에서 모바일 속성을 구성하려고 합니다. Adobe Launch와 Adobe Campaign 간에 기술 워크플로우가 동기화되기를 기다려야 합니까?

워크플로우를 즉시 실행할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;을 선택합니다.

1. 워크플로우를 **[!UICONTROL syncWithLaunch]** 엽니다.

1. 활동을 **[!UICONTROL Scheduler]** 클릭하고 선택합니다 **[!UICONTROL Immediate execution]**.
