---
solution: Campaign Standard
product: campaign
title: Launch 기술 워크플로우와 동기화 FAQ
description: Launch technical workflow에 대한 일반적인 질문입니다.
audience: administration
content-type: reference
topic-tags: users-and-security
feature: Instance Settings
role: Administrator
level: Experienced
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# Adobe 실행 동기화 FAQ {#syncwithlaunch-faq}

전용 기술 작업 과정을 통해 Adobe Launch 모바일 속성을 Adobe Campaign Standard으로 가져올 수 있습니다. **[!UICONTROL Sync with Launch]** 자세한 내용은 이 [페이지](../../administration/using/technical-workflows.md)를 참조하십시오.

아래 섹션에는 이 동기화에 대한 일반적인 질문이 나와 있습니다.

## [!DNL Launch](조직 단위 ALL의 관리자가 아닌 속성)에 속성을 만들었습니다. 내 애플리케이션이 Adobe Campaign에서 구성 준비 상태에 있지만 해당 상태를 열거나 구성할 수 없습니다.{#configuring-property}

조직 구성 단위 ALL의 관리자만 Adobe Campaign Standard에서 모바일 애플리케이션을 구성할 수 있습니다. 구성한 후에는 지정된 조직 단위의 사용자만
응용 프로그램. 조직 단위에 대한 자세한 내용은 이 [페이지](../../administration/using/organizational-units.md)를 참조하십시오.

## Adobe Campaign Standard에서 구성된 모바일 응용 프로그램을 편집할 수 없으며 모바일 응용 프로그램은 읽기 모드에만 있습니다.{#read-mode-mobile-app}

**[!UICONTROL Access Authorization]** 섹션에서 모바일 애플리케이션의 조직 단위를 확인합니다. 지정된 조직 구성 단위 사용자만 모바일 응용 프로그램을 편집할 수 있습니다.

조직 단위에 대한 자세한 내용은 이 [페이지](../../administration/using/organizational-units.md)를 참조하십시오.

## Adobe Campaign Standard에서 조직 단위 ALL을 사용하는 관리자이지만 모바일 애플리케이션을 구성할 수 없습니다.{#org-unit-mobile}

조직 단위가 ALL으로 설정된 관리자는 모바일 응용 프로그램을 구성하려면 [!DNL Launch]의 모든 모바일 속성에 대한 권한을 가져야 합니다.

조직 단위에 대한 자세한 내용은 이 [페이지](../../administration/using/organizational-units.md)를 참조하십시오.

## [!DNL Launch]에 모바일 속성을 만들었지만 내 속성은 Adobe Campaign Standard에 표시되지 않습니다.{#visibility-mobile-property}

1. Adobe Campaign Standard 확장이 [!DNL Launch]의 모바일 속성에 설치되어 있는지 확인합니다.

1. 인스턴스의 끝점이 확장자에 올바르게 구성되어 있는지 확인합니다.

1. &#39;Launch_URL_Campaign&#39; 또는 &#39;NmsServer_URL&#39;이 올바른지 확인하십시오.

1. 그런 다음 [!DNL Launch] 및 Adobe Campaign 간의 동기화가 **[!UICONTROL syncWithLaunch]** 기술 워크플로와 함께 완료되었는지 확인하십시오.

## Adobe Campaign과 Launch 간의 동기화가 완료되었는지 확인하는 방법{#sync-campaign-launch}

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;를 선택합니다.

1. **[!UICONTROL syncWithLaunch]** 작업 과정을 엽니다.

1. 워크플로우가 오류 없이 끝났는지 확인합니다.

1. 워크플로 동기화가 활성화되고 성공적으로 완료되었는지 로그를 확인합니다.

## Launch에서 구성된 모바일 애플리케이션에 대한 키를 재설정합니다. Launch에서 키를 다시 재구성하는 방법{#configuring-pkey}

1. Adobe Launch에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장 프로그램에 새 URL을 설정합니다.

1. 저장하고 Adobe Campaign과 [!DNL Launch] 간의 워크플로우가 동기화되도록 합니다.

1. 동기화가 완료되면 [!DNL Launch]에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장에서 올바른 URL을 설정합니다.

1. 저장하고 워크플로우 동기화를 다시 실행할 수 있습니다.

1. 이 경우에만 속성이 Adobe Campaign의 **[!UICONTROL Ready to Configure]** 상태에 나타나며 이제 구성할 수 있습니다.

## Adobe Campaign에서 모바일 속성을 구성하려고 합니다. Adobe Launch와 Adobe Campaign 간에 동기화되는 기술 워크플로우를 기다려야 합니까?

워크플로우를 즉시 실행할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;를 선택합니다.

1. **[!UICONTROL syncWithLaunch]** 작업 과정을 엽니다.

1. **[!UICONTROL Scheduler]** 활동을 클릭하고 **[!UICONTROL Immediate execution]**&#x200B;을 선택합니다.
