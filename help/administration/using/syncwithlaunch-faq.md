---
title: Launch 기술 워크플로우 FAQ와 동기화
description: Adobe Launch 기술 워크플로우에 대한 일반적인 질문
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: aaaceb3a-5e54-47da-9be4-b70747282830
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# Adobe Experience Platform 동기화의 태그 FAQ {#syncwithlaunch-faq}

다음을 통해 태그 모바일 속성을 Adobe Campaign Standard으로 가져올 수 있습니다. **[!UICONTROL Sync with Launch]** 전용 기술 워크플로우입니다. 자세한 내용은 다음을 참조하십시오. [페이지](../../administration/using/technical-workflows.md)

아래 섹션에는 이 동기화에 대한 일반적인 질문이 나와 있습니다.

## 태그 속성(조직 단위 ALL의 관리자가 아닌 사용자)을 만들었습니다. 내 애플리케이션은 Adobe Campaign에서 구성 준비 상태이지만 열거나 구성할 수 없습니다. {#configuring-property}

조직 단위 ALL의 관리자만 Adobe Campaign Standard에서 모바일 애플리케이션을 구성할 수 있습니다. 구성이 완료되면 할당된 조직 단위의 사용자만 애플리케이션을 편집할 수 있습니다. 조직 단위에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 구성된 모바일 애플리케이션을 편집할 수 없고 모바일 애플리케이션이 읽기 모드에만 있습니다. {#read-mode-mobile-app}

에서 모바일 애플리케이션의 조직 구성 단위를 확인합니다. **[!UICONTROL Access Authorization]** 섹션. 할당된 조직 단위의 사용자만 모바일 애플리케이션을 편집할 수 있습니다.

조직 단위에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../administration/using/organizational-units.md).

## Adobe Campaign Standard에서 조직 단위 ALL을 사용하는 관리자이지만 모바일 애플리케이션을 구성할 수 없습니다. {#org-unit-mobile}

조직 단위가 ALL로 설정된 관리자는 모바일 애플리케이션을 구성할 수 있는 모든 태그 모바일 속성에 대한 권한이 있어야 합니다.

조직 단위에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../administration/using/organizational-units.md).

## 태그 모바일 속성을 만들었지만 내 속성이 Adobe Campaign Standard에 표시되지 않습니다. {#visibility-mobile-property}

1. Adobe Campaign Standard 확장이 데이터 수집 UI의 모바일 속성에 설치되었는지 확인합니다.

1. 인스턴스의 끝점이 확장에 올바르게 구성되었는지 확인합니다.

1. &#39;Launch_URL_Campaign&#39; 또는 &#39;NmsServer_URL&#39;이 올바른지 확인하십시오.

1. 그런 다음 동기화가 완료되었는지 확인합니다. **[!UICONTROL syncWithLaunch]** 기술 워크플로우입니다.

## Adobe Experience Platform의 Adobe Campaign과 태그 간의 동기화가 완료되었는지 확인하는 방법 {#sync-campaign-launch}

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**.

1. 를 엽니다. **[!UICONTROL syncWithLaunch]** 워크플로입니다.

1. 워크플로우가 오류 없이 종료되었는지 확인합니다.

1. 워크플로우 동기화가 활성화되고 성공적으로 완료되었는지 로그에서 확인합니다.

## 구성된 태그 모바일 애플리케이션에 대한 pkey를 재설정했습니다. 데이터 수집 UI에서 pkey를 다시 구성하는 방법 {#configuring-pkey}

1. 데이터 수집 UI에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장에서 새 URL을 설정합니다.

1. 저장하고 워크플로우를 동기화합니다.

1. 동기화가 완료되면 데이터 수집 UI의에서 모바일 속성을 엽니다.

1. PKey가 재설정된 Adobe Campaign Standard 확장에서 올바른 URL을 설정하십시오.

1. 저장하고 워크플로우 동기화를 다시 실행합니다.

1. 이 후에만 속성이에 표시됩니다. **[!UICONTROL Ready to Configure]** Adobe Campaign의 상태이며, 이제 구성할 수 있습니다.

## Adobe Campaign에서 모바일 속성을 구성하려고 합니다. 기술 워크플로우가 Adobe Experience Platform과 Adobe Campaign의 태그 간에 동기화될 때까지 기다려야 합니까?

워크플로우를 즉시 실행할 수 있습니다.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**.

1. 를 엽니다. **[!UICONTROL syncWithLaunch]** 워크플로입니다.

1. 을(를) 클릭합니다 **[!UICONTROL Scheduler]** 활동 및 선택 **[!UICONTROL Immediate execution]**.
