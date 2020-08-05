---
title: Launch 기술 워크플로우와 동기화 FAQ
description: Launch 기술 워크플로우에 대한 일반적인 질문입니다.
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
source-git-commit: 95a7397092f6e07c84967d90908469f630f7a170
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# Adobe 실행 동기화 FAQ {#syncwithlaunch-faq}

전용 기술 워크플로우를 통해 Adobe Launch 모바일 속성을 Adobe Campaign Standard으로 가져올 수 **[!UICONTROL Sync with Launch]** 있습니다. For more information, refer to this [page](../../administration/using/technical-workflows.md)

아래 섹션에는 이 동기화에 대한 일반적인 질문이 나와 있습니다.

>[!NOTE]
>
>You will need to submit a ticket to Adobe Customer Care (either directly or through your Adobe contact) to have the **[!UICONTROL syncWithLaunch]** technical workflow enabled in your Campaign instance.

## (조직 단위 ALL의 비관리 [!DNL Launch] 로) 속성을 만들었습니다. 내 애플리케이션이 Adobe Campaign에서 구성 준비 상태에 있지만 해당 상태를 열거나 구성할 수 없습니다. {#configuring-property}

조직 구성 단위 ALL의 관리자만 Adobe Campaign Standard에서 모바일 애플리케이션을 구성할 수 있습니다. 구성한 후에는 지정된 조직 구성 단위의 사용자만 애플리케이션을 편집할 수 있습니다. For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 구성된 모바일 응용 프로그램을 편집할 수 없으며 모바일 응용 프로그램은 읽기 모드입니다. {#read-mode-mobile-app}

섹션에서 모바일 애플리케이션의 구성 요소를 **[!UICONTROL Access Authorization ]** 확인합니다. 지정된 조직 구성 단위의 사용자만 모바일 응용 프로그램을 편집할 수 있습니다.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 조직 구성 단위 ALL을 담당하는 관리자이지만 모바일 애플리케이션을 구성할 수 없습니다. {#org-unit-mobile}

조직 단위가 모두(ALL)로 설정된 관리자는 모바일 애플리케이션을 구성하려면 모든 모바일 속성 [!DNL Launch] 에 대한 권한이 있어야 합니다.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## 모바일 속성을 만들었지만 내 속성이 Adobe Campaign Standard에서 보이지 [!DNL Launch] 않습니다. {#visibility-mobile-property}

1. Adobe Campaign Standard 확장이 모바일 속성에 설치되어 있는지 확인하십시오 [!DNL Launch].

1. 인스턴스의 끝점이 확장자에 올바르게 구성되어 있는지 확인합니다.

1. &#39;Launch_URL_Campaign&#39; 또는 &#39;NmsServer_URL&#39;이 올바른지 확인하십시오.

1. 그런 다음 [!DNL Launch] 와 Adobe Campaign 간의 동기화가 **[!UICONTROL syncWithLaunch]** 기술 워크플로우로 완료되었는지 확인하십시오.

## Adobe Campaign과 론치 간 동기화가 완료되었는지 확인하는 방법 {#sync-campaign-launch}

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;를 선택합니다.

1. 워크플로우를 **[!UICONTROL syncWithLaunch]** 엽니다.

1. 워크플로우가 오류 없이 끝났는지 확인합니다.

1. 워크플로우 동기화가 활성화되고 성공적으로 완료되었는지 로그를 확인합니다.

## Launch에서 구성된 모바일 응용 프로그램의 키를 재설정합니다. Launch에서 키를 다시 구성하는 방법 {#configuring-pkey}

1. Adobe 론치에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장 프로그램에 새 URL을 설정합니다.

1. 파일을 저장하고 Adobe Campaign과 간에 워크플로우를 동기화할 수 있습니다 [!DNL Launch].

1. 동기화가 완료되면 모바일 속성을 엽니다 [!DNL Launch].

1. PKey가 재설정된 Adobe Campaign Standard 확장 프로그램에서 올바른 URL을 설정합니다.

1. 저장하여 워크플로우 동기화를 다시 실행할 수 있습니다.

1. 이 경우에만 속성이 Adobe Campaign의 **[!UICONTROL Ready to Configure]** 상태로 나타나고 이제 구성할 수 있습니다.

## Adobe Campaign에서 모바일 속성을 구성하고 싶습니다. Adobe Launch와 Adobe Campaign 간에 기술 워크플로우가 동기화되기를 기다려야 합니까?

워크플로우를 즉시 실행할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;를 선택합니다.

1. 워크플로우를 **[!UICONTROL syncWithLaunch]** 엽니다.

1. Click on the **[!UICONTROL Scheduler]** activity and select **[!UICONTROL Immediate execution]**.
