---
solution: Campaign Standard
product: campaign
title: 가져오기 템플릿으로 데이터 가져오기
description: 데이터를 수집하여 Campaign 데이터베이스를 제공하는 방법을 알아보십시오.
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 99%

---


# 가져오기 템플릿으로 데이터 가져오기{#importing-data-with-import-templates}

데이터를 가져오면 데이터를 수집하여 Campaign 데이터베이스를 제공할 수 있습니다.

[워크플로우](../../automating/using/get-started-workflows.md) 대신 Adobe Campaign은 관리자가 정의한 특정 유형의 가져오기를 사용자가 관리할 수 있도록 해주는 간소화된 가져오기 기능을 제공합니다.

운영 원칙은 다음과 같습니다. **관리자**&#x200B;가 가져오기 템플릿을 정의하고 관리합니다([가져오기 템플릿 정의](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates) 참조). 그리고 이러한 가져오기 템플릿은 **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Imports]** 메뉴 아래에 간소화된 보기가 있는 사용자가 사용할 수 있습니다.

따라서 이러한 사용자는 수행할 가져오기 유형을 선택하고 가져올 데이터가 있는 파일을 업로드하기만 하면 됩니다. 관리자가 정의한 워크플로우는 가져오기가 완료되면 그 결과에 대한 세부 정보에 액세스할 수 있는 사용자를 위해 투명하게 실행됩니다.

>[!NOTE]
>
>데이터 가져오기 기능은 **[!UICONTROL GENERIC IMPORT (import)]** 및 **[!UICONTROL WORKFLOW (workflow)]** 역할이 있는 사용자가 관리할 수 있습니다. 역할과 관련한 자세한 내용은 [이 섹션](../../administration/using/list-of-roles.md)을 참조하십시오.

가져오기는 실행된 템플릿, 실행 날짜 및 실행 상태에 따라 필터링할 수 있습니다.

1. 가져오기 개요에서 **[!UICONTROL Create]** 버튼을 클릭합니다. 마법사가 열립니다.
1. 수행할 가져오기 유형을 선택합니다. 가져오기 유형은 사용 가능한 가져오기 템플릿에 해당합니다.
1. 필요한 경우 템플릿에 연결된 샘플 파일을 컴퓨터에 다운로드하여 가져올 파일의 데이터 유형을 확인합니다.
1. 마법사에서 가져올 데이터가 포함된 파일을 다운로드합니다.
1. 가져오기를 시작합니다. 마법사가 닫히고 사용된 템플릿으로 수행된 가져오기 목록으로 돌아갑니다.
1. 페이지를 새로 고침하고 방금 수행한 가져오기를 선택하여 실행 세부 사항을 확인합니다.

   ![](assets/simplified_import1.png)

이제 가져오기 실행에 대한 세부 사항을 사용할 수 있습니다. 가져온 파일 및 거부된 데이터(가져오지 않은 데이터)가 포함된 파일은 모두 컴퓨터에 다운로드할 수 있습니다.

## 가져오기 템플릿 설정 {#setting-up-import-templates}

관리자는 가져오기 템플릿으로 특정한 수의 기술 가져오기 구성을 미리 정의할 수 있습니다. 그 다음 표준 사용자가 이 템플릿을 사용하여 파일을 실행 및 업로드할 수 있습니다.

가져오기 템플릿은 기능 관리자가 정의하며 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Import templates]** 메뉴에서 관리할 수 있습니다.

![](assets/import_template_list.png)

다음 세 가지 기본 읽기 전용 템플릿을 사용할 수 있습니다.

* **[!UICONTROL Update Direct mail quarantines and delivery logs]**: 이 템플릿은 격리와 DM의 게재 로그를 업데이트하는 새 가져오기의 토대 역할을 합니다. 이 템플릿의 워크플로우에는 다음 활동이 포함됩니다.
* **[!UICONTROL Import data]**: 이 템플릿은 파일의 데이터를 데이터베이스에 삽입하는 새 가져오기의 토대 역할을 합니다. 이 템플릿의 워크플로우에는 다음 활동이 포함됩니다.

   * **[!UICONTROL Load file]**: 이 활동을 사용하면 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Update data]**: 이 활동을 사용하면 파일의 데이터를 데이터베이스에 삽입할 수 있습니다.

* **[!UICONTROL Import list]**: 이 템플릿은 파일의 데이터에서 **목록** 유형 대상자를 만드는 새 가져오기의 토대 역할을 합니다. 이 템플릿의 워크플로우에는 다음 활동이 포함됩니다.

   * **[!UICONTROL Load file]**: 이 활동을 사용하면 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Reconciliation]**: 이 활동을 사용하면 타겟팅 차원을 가져온 데이터에 연결할 수 있습니다. 이를 통해 **목록** 유형 대상자를 만들 수 있습니다. 가져온 데이터의 타겟팅 차원을 알 수 없는 경우 이 대상자는 **파일** 유형이 됩니다. [타겟팅 차원 및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)를 참조하십시오.
   * **[!UICONTROL Save audience]**: 이 활동을 사용하면 가져온 데이터를 **목록** 유형 대상자의 형태로 저장할 수 있습니다. 저장되는 대상자의 이름은 사용자가 가져온 파일의 이름에 해당하며, 가져온 날짜 및 시간을 표시하는 접미사가 추가됩니다. &#39;profiles_20150406_151448&#39;을 예로 들 수 있습니다.

기본 템플릿은 읽기 전용이며 표준 사용자에게는 보이지 않습니다. 사용자가 사용할 수 있는 템플릿을 만들려면 다음 단계를 수행하십시오.

1. 기본 템플릿을 복제합니다. 복제한 템플릿에는 세 개의 탭이 있습니다.

   * **[!UICONTROL Properties]**: 가져오기 템플릿의 일반 매개 변수입니다. 이 탭에서는 템플릿을 활성화하고 샘플 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Workflow]**: 가져오기 워크플로우입니다. 이 탭에서는 워크플로우 활동을 정의할 수 있습니다. 이 활동은 사용자가 수행하는 간소화된 가져오기 작업 중에는 보이지 않습니다.
   * **[!UICONTROL Executed imports]**: 이 템플릿을 사용하여 수행한 가져오기 목록입니다. 이 템플릿을 사용하여 수행한 각 가져오기의 상태, 세부 사항 및 결과를 볼 수 있습니다. 이 목록에서 직접 워크플로우(사용자용으로 투명하게 수행)에 액세스할 수 있습니다.

1. **[!UICONTROL Properties]** 탭에서 템플릿 이름을 변경하고 설명을 추가합니다. 템플릿을 사용할 수 있을 경우 사용자가 설명을 볼 수 있습니다.

   ![](assets/simplified_import_model1.png)

1. **[!UICONTROL Workflow]** 탭으로 이동합니다. 여기에서는 기본적으로 제공되는 워크플로우에 필요에 따라 새 활동을 추가하여 보강할 수 있습니다.

   워크플로우 활동을 구성하는 방법에 대한 자세한 내용은 [예제: 가져오기 워크플로우 템플릿](../../automating/using/creating-import-workflow-templates.md) 섹션에 설명된 사용 사례를 참조하십시오. 이 사용 사례는 Adobe Campaign 데이터베이스의 CRM에 있는 프로필을 가져올 때 다시 사용할 수 있는 워크플로우를 설정하는 데 도움이 됩니다.

1. 워크플로우의 구성을 올바르게 고려할 수 있도록 템플릿을 저장합니다.
1. **[!UICONTROL Properties]** 탭에서 샘플 파일을 업로드합니다. 업로드하는 파일에는 향후 가져오기 또는 샘플 데이터에 필요한 열만 포함할 수 있습니다. 워크플로우를 정의한 후 샘플 파일의 데이터를 사용해 간소화된 가져오기를 테스트할 수 있습니다.

   ![](assets/import_template_sample.png)

   그 이후 템플릿으로 가져오기를 수행하는 사용자가 이 샘플 파일을 사용할 수 있습니다. 예를 들어 컴퓨터에 다운로드하여 가져올 데이터로 입력할 수 있습니다. 샘플 파일을 추가할 때는 이를 고려해야 합니다.

1. 템플릿을 저장합니다. 이제 샘플 파일이 고려됩니다. 언제든지 컴퓨터에 다운로드하여 콘텐츠를 확인하거나 **[!UICONTROL Drop a new sample file]** 옵션을 선택하여 수정할 수 있습니다.

   ![](assets/simplified_import_model2.png)

1. **[!UICONTROL Workflow]** 탭으로 돌아가서 **[!UICONTROL Load file]** 활동을 열고 앞 단계에서 업로드한 샘플 파일의 열 구성을 확인 및 조정합니다.
1. 워크플로우를 시작하여 가져오기를 테스트합니다. **5**&#x200B;단계에서 업로드하는 샘플 파일에는 데이터가 있어야 합니다.

   그런 다음 샘플 파일의 데이터를 실제로 가져옵니다. 데이터베이스가 손상되지 않도록 용량이 작은 가상 데이터를 사용해야 합니다.

1. 작업 표시줄을 통해 워크플로우 실행 로그로 이동합니다. 오류가 발생했을 경우 활동이 올바르게 구성되었는지 확인합니다.

   ![](assets/simplified_import_model3.png)

1. **[!UICONTROL Properties]** 탭에서 **[!UICONTROL Import template status]**&#x200B;을(를) **[!UICONTROL Available]**(으)로 설정한 다음 템플릿을 저장합니다. 이 템플릿 사용을 중단하려면 **[!UICONTROL Import template status]**&#x200B;을(를) **[!UICONTROL Archived]**(으)로 설정할 수 있습니다.

템플릿 워크플로우를 수정하려면 샘플 파일을 다시 업로드하고 **[!UICONTROL Load file]** 구성을 확인합니다.

이제 사용자가 가져오기 템플릿을 사용하여 파일을 업로드할 수 있습니다.

**관련 항목:**

* [워크플로우](../../automating/using/get-started-workflows.md)
* [예제: 가져오기 워크플로우 템플릿](../../automating/using/creating-import-workflow-templates.md)
