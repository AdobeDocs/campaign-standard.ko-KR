---
title: 데이터 가져오기 및 내보내기 기본 정보
description: Adobe Campaign을 사용하여 데이터를 가져오고 내보내는 다양한 방법에 대해 알아봅니다.
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
feature: Workflows
role: Data Architect
level: Experienced
exl-id: 208e8629-c3e2-4f36-bae7-46ffc3f56a1b
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 12%

---

# 데이터 가져오기 및 내보내기 기본 정보{#about-data-import-and-export}

비즈니스 요구 사항에 따라 Adobe Campaign을 사용하여 데이터를 가져오고 내보내는 몇 가지 방법이 있습니다.

* **패키지**: 패키지는 Adobe Campaign 인스턴스에서 다른 인스턴스로 구성 및 데이터 세트를 내보내고 가져올 수 있는 XML 파일입니다. 시스템 업데이트는 패키지 가져오기를 통해서도 수행됩니다.
* **목록**: 모든 목록 화면을 구성하고 표시된 데이터를 별도의 파일로 내보낼 수 있습니다.
* **워크플로**: 파일에서 데이터를 가져와 데이터베이스를 업데이트하거나 이메일을 보낼 수 있습니다. 파일로 내보낼 데이터를 선택할 수도 있습니다. 워크플로우는 프로필 가져오기와 같은 정기적인 업데이트를 자동화하는 가장 좋은 방법입니다.

   * **[!UICONTROL Load file]** 활동을 통해 데이터를 Adobe Campaign에서 사용할 수 있도록 하나의 구조화된 양식으로 가져올 수 있습니다. 데이터를 일시적으로 가져오고 이를 Adobe Campaign 데이터베이스에 완전히 통합하려면 다른 활동이 필요합니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../../automating/using/load-file.md).
   * 다음 **[!UICONTROL Transfer file]** 활동을 사용하면 Adobe Campaign에서 파일을 받거나 보내고, 파일이 있는지 테스트하거나, 파일 목록을 만들 수 있습니다. 다음 작업 전에 이 활동을 사용할 수 있습니다. **[!UICONTROL Load file]** 외부 소스에서 파일을 검색해야 하는 경우. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../../automating/using/transfer-file.md).

가져오기 프로세스를 디자인할 때는 필요에 맞게 조정할 수 있는 워크플로우 템플릿을 사용하는 것이 좋습니다. 데이터를 가져오기 위한 워크플로우 템플릿 설정 방법에 대한 자세한 내용은 을 참조하십시오. [이 사용 사례](../../automating/using/creating-import-workflow-templates.md).

Adobe Campaign은 또한 디자인에서 이루어지는 일반 가져오기를 수행하는 간단한 방법을 제공합니다 **템플릿 가져오기**. 가져오기 템플릿은 전용 화면을 통해 사용할 수 있는 전문 워크플로 템플릿입니다. 디자인한 후에는 가져오기를 수행하는 사용자가 단순화된 보기에서 가져올 파일을 업로드하기만 하면 됩니다.

**관련 항목**:

* [가져오기 템플릿으로 데이터 가져오기](../../automating/using/importing-data-with-import-templates.md)
* [가져오기 템플릿 정의](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)
* [패키지 관리](../../automating/using/managing-packages.md)
