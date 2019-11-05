---
title: 가져오기 템플릿 정의
description: 템플릿을 가져오면 필요한 설정을 줄이고 데이터를 보다 신속하게 가져올 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 651eb57c-adac-4e3e-b454-b39aea1f0484
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: 85d13147-fb31-446a-8476-f112c841fb82
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 가져오기 템플릿 정의{#defining-import-templates}

관리자는 가져오기 템플릿을 사용하여 특정 수의 기술 가져오기 구성을 미리 정의할 수 있습니다. 그런 다음 표준 사용자가 파일을 실행하고 업로드할 수 있도록 이러한 템플릿을 사용할 수 있습니다.

가져오기 템플릿은 기능 관리자가 정의하며 **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Import templates]** 메뉴에서 관리할 수 있습니다.

![](assets/import_template_list.png)

다음 세 가지 기본 읽기 전용 템플릿을 사용할 수 있습니다.

* **[!UICONTROL Update Direct mail quarantines and delivery logs]**:이 템플릿은 DM(Direct Mail)에 대한 검역과 배달 로그를 업데이트하는 새로운 가져오기의 기초로 사용할 수 있습니다. 템플릿의 워크플로우에는 다음 활동이 포함됩니다.
* **[!UICONTROL Import data]**:이 템플릿은 파일에서 데이터베이스에 데이터를 삽입하는 새 가져오기의 기초로 사용할 수 있습니다. 이 템플릿의 워크플로에는 다음 활동이 포함되어 있습니다.

   * **[!UICONTROL Load file]**:이 활동을 통해 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Update data]**:이 작업을 사용하면 데이터베이스의 파일에서 데이터를 삽입할 수 있습니다.

* **[!UICONTROL Import list]**:이 템플릿은 새 가져오기의 기초로 사용하여 파일의 데이터에서 목록 **유형** 대상을 만들 수 있습니다. 이 템플릿의 워크플로에는 다음 활동이 포함되어 있습니다.

   * **[!UICONTROL Load file]**:이 활동을 통해 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Reconciliation]**:이 활동을 사용하면 타깃팅 차원을 가져온 데이터에 연결할 수 있습니다. 그런 다음 목록 **유형 대상을** 만들 수 있습니다. 가져온 데이터의 타깃팅 차원을 알 수 없는 경우 대상은 파일 **유형입니다** . 차원 [및 리소스](../../automating/using/query.md#targeting-dimensions-and-resources)타깃팅을 참조하십시오.
   * **[!UICONTROL Save audience]**:이 활동을 사용하면 목록 유형 대상의 형태로 가져온 데이터를 저장할 **수** 있습니다. 저장된 대상의 이름은 사용자가 가져온 파일의 이름에 해당하며, 가져오기의 날짜 및 시간을 지정하는 접미사가 추가됩니다. 예:'profiles_20150406_151448'

이러한 기본 템플릿은 읽기 전용이며 표준 사용자는 볼 수 없습니다. 사용자가 사용할 수 있는 템플릿을 만들려면 다음 단계를 따르십시오.

1. 기본 템플릿을 복제합니다. 중복된 템플릿에는 세 개의 탭이 있습니다.

   * **[!UICONTROL Properties]**:가져오기 템플릿의 일반 매개 변수입니다. 이 탭에서는 템플릿을 활성화하고 샘플 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Workflow]**:워크플로우 가져오기 이 탭에서는 워크플로우 활동을 정의할 수 있습니다. 이러한 활동은 사용자가 수행한 간소화된 가져오기 작업 중에는 표시되지 않습니다.
   * **[!UICONTROL Executed imports]**:이 템플릿을 사용하여 수행한 가져오기 목록 이 템플릿을 사용하여 수행한 각 가져오기의 상태, 세부 사항 및 결과를 볼 수 있습니다. 이 목록에서 직접 워크플로우에 액세스할 수 있습니다(사용자에 대해 투명한 방식으로 수행).

1. 탭에서 템플릿 이름을 변경하고 설명을 추가합니다. **[!UICONTROL Properties]** 템플릿을 사용할 수 있으면 사용자가 설명을 볼 수 있습니다.

   ![](assets/simplified_import_model1.png)

1. 탭으로 **[!UICONTROL Workflow]** 이동합니다. 여기에서 필요에 따라 새 활동을 추가하여 기본적으로 제공되는 워크플로우를 강화할 수 있습니다.

   워크플로우 활동을 구성하는 방법에 대한 자세한 내용은 다음 섹션에 설명된 사용 사례를 참조하십시오.예 [:워크플로우 템플릿](../../automating/using/importing-data.md#example--import-workflow-template)가져오기 이 사용 사례는 Adobe Campaign 데이터베이스의 CRM에서 가져오는 데 다시 사용할 수 있는 워크플로우를 설정하는 데 도움이 됩니다.

1. 워크플로우의 구성을 올바로 고려하도록 템플릿을 저장합니다.
1. 탭에서 샘플 파일을 **[!UICONTROL Properties]** 업로드합니다. 업로드된 파일에는 향후 가져오기 또는 샘플 데이터에 필요한 열만 있을 수 있습니다. 샘플 파일의 데이터를 사용하면 워크플로우가 정의된 후 간소화된 가져오기를 테스트할 수 있습니다.

   ![](assets/import_template_sample.png)

   그러면 템플릿을 사용하여 가져오기를 수행하는 사용자가 이 샘플 파일을 사용할 수 있습니다. 예를 들어 가져올 데이터로 내용을 채우는 등 컴퓨터에 다운로드할 수 있습니다. 샘플 파일을 추가할 때 이 문제를 고려해야 합니다.

1. 템플릿을 저장합니다. 이제 샘플 파일을 고려합니다. 언제든지 컴퓨터에 다운로드하여 컨텐츠를 확인하거나 **[!UICONTROL Drop a new sample file]** 옵션을 선택하여 수정할 수 있습니다.

   ![](assets/simplified_import_model2.png)

1. 탭으로 돌아가서 **[!UICONTROL Workflow]** **[!UICONTROL Load file]** 활동을 열어 이전 단계에서 업로드된 샘플 파일의 열 구성을 확인하고 조정합니다.
1. 워크플로우를 시작하여 가져오기를 테스트합니다. 5단계에서 업로드된 샘플 파일은 **데이터를** 포함해야 합니다.

   그런 다음 샘플 파일의 데이터를 실제로 가져옵니다. 사용된 데이터가 작고 허구인지 확인하여 데이터베이스가 손상되지 않았는지 확인하십시오.

1. 작업 표시줄에서 사용할 수 있는 워크플로우 실행 로그로 이동합니다. 오류가 발생하면 활동이 올바르게 구성되었는지 확인하십시오.

   ![](assets/simplified_import_model3.png)

1. 탭에서 을 **[!UICONTROL Properties]** 로 **[!UICONTROL Import template status]** **[!UICONTROL Available]**&#x200B;설정한 다음 템플릿을 저장합니다. 이 템플릿 사용을 중지하려면 을 **[!UICONTROL Import template status]** 다음으로 설정할 수 **[!UICONTROL Archived]**&#x200B;있습니다.

템플릿 워크플로우는 샘플 파일을 다시 업로드하고 **[!UICONTROL Load file]** 구성을 확인하여 수정할 수 있습니다.

이제 사용자가 가져오기 템플릿을 사용할 수 있으며 파일을 업로드하는 데 사용할 수 있습니다.

**관련 항목:**

* [워크플로우](../../automating/using/discovering-workflows.md)
* [데이터 가져오기](../../automating/using/importing-data.md)
* [예:워크플로우 템플릿 가져오기](../../automating/using/importing-data.md#example--import-workflow-template)

