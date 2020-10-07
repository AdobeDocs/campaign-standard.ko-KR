---
title: 데이터 가져오기 및 내보내기 기본 정보
description: Adobe Campaign에서 데이터를 가져오고 내보내는 다양한 방법에 대해 알아봅니다.
page-status-flag: never-activated
uuid: f6810364-555c-4b72-8a9c-4ae2fcb2ba63
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: 31215773-6c0c-48f1-9101-da0ea2a366da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 24%

---


# 데이터 가져오기 및 내보내기 기본 정보{#about-data-import-and-export}

비즈니스 요구 사항에 따라 Adobe Campaign에서 데이터를 가져오고 내보낼 수 있는 여러 가지 방법이 있습니다.

* **패키지**:패키지는 Adobe Campaign 인스턴스에서 다른 인스턴스로 구성 및 데이터 세트를 내보내고 가져올 수 있는 XML 파일입니다. 시스템 업데이트는 패키지 가져오기를 통해 수행됩니다.
* **목록**:모든 목록 화면을 구성하고 표시된 데이터를 별도의 파일로 내보낼 수 있습니다.
* **워크플로우**:파일에서 데이터를 가져와서 데이터베이스를 업데이트하거나 이메일을 전송하는 데 사용합니다. 파일로 내보낼 데이터를 선택할 수도 있습니다. 프로파일 가져오기와 같은 일반 업데이트를 자동화하는 가장 좋은 방법은 워크플로우입니다.

   * **[!UICONTROL Load file]** 활동을 통해 데이터를 Adobe Campaign에서 사용할 수 있도록 하나의 구조화된 양식으로 가져올 수 있습니다. 파일 로드 활동을 통한 데이터 가져오기는 일시적이며, 가져온 데이터를 Adobe Campaign 데이터베이스에 완전히 통합하려면 다른 활동이 필요합니다. 이 활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/load-file.md).
   * **[!UICONTROL Transfer file]** 활동을 사용하면 Adobe Campaign에서 파일을 받거나 보내고, 파일이 있는지 테스트하거나, 파일 목록을 만들 수 있습니다. 외부 소스에서 파일을 검색해야 하는 경우에 대비해 이 활동 **[!UICONTROL Load file]** 을 먼저 사용할 수 있습니다. 이 활동 사용 방법에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../automating/using/transfer-file.md).

가져오기 프로세스를 디자인할 때 요구 사항에 맞게 변경할 수 있는 워크플로우 템플릿을 사용하는 것이 가장 좋습니다. 데이터를 가져오기 위한 워크플로우 템플릿을 설정하는 방법에 대한 자세한 내용은 [이 사용 사례를 참조하십시오](../../automating/using/creating-import-workflow-templates.md).

또한 Adobe Campaign은 **가져오기 템플릿을 디자인하는 데 필요한 일반적인 가져오기를 간소화할 수 있는 방법을 제공합니다**. 가져오기 템플릿은 전용 화면을 통해 사용할 수 있는 특수 워크플로우 템플릿입니다. 일단 디자인한 후에는 가져오기를 수행하는 사용자가 파일을 업로드하여 간단히 볼 수 있습니다.

**관련 항목**:

* [가져오기 템플릿으로 데이터 가져오기](../../automating/using/importing-data-with-import-templates.md)
* [가져오기 템플릿 정의](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)
* [패키지 관리](../../automating/using/managing-packages.md)
