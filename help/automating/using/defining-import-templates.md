---
title: 가져오기 템플릿 정의
seo-title: 가져오기 템플릿 정의
description: 가져오기 템플릿 정의
seo-description: 템플릿을 가져올 수 있으므로 필요한 설정을 줄이고 데이터를 보다 빠르게 가져올 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 651 EB 57 C-ADAC -4 E 3 E-B 454-B 39 AEA 1 F 0484
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: 85 d 13147-FB 31-446 a -8476-F 112 C 841 FB 82
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 36727e82d3aa73add6116fa2916752ff0e407d9d

---


# Defining import templates{#defining-import-templates}

템플릿 가져오기 기능을 사용하면 관리자는 특정 수의 기술 가져오기 구성을 미리 정의할 수 있습니다. 그런 다음 표준 사용자는 이러한 템플릿을 사용하여 파일을 수행하고 업로드할 수 있습니다.

An import template is defined by the functional administrator and can be managed under the **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Import templates]** menu.

![](assets/import_template_list.png)

세 가지 기본 읽기 전용 템플릿을 사용할 수 있습니다.

* **[!UICONTROL Update Direct mail quarantines and delivery logs]**: 이 템플릿은 직접 메일을 위한 쿼리와 배달 로그를 업데이트하는 새 가져오기의 기초로 사용할 수 있습니다. 템플릿 워크플로우는 다음 활동을 포함합니다.
* **[!UICONTROL Import data]**: 이 템플릿은 파일의 데이터를 데이터베이스에 삽입하는 새 가져오기의 기초로 사용할 수 있습니다. 이 템플릿의 워크플로우는 다음 활동을 포함합니다.

   * **[!UICONTROL Load file]**: 이 활동에서는 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Update data]**: 이 활동을 통해 데이터베이스에 있는 파일의 데이터를 삽입할 수 있습니다.

* **[!UICONTROL Import list]**: 이 템플릿은 새 가져오기의 기초로 사용되어 파일의 데이터에서 **목록** 유형 대상을 만들 수 있습니다. 이 템플릿의 워크플로우는 다음 활동을 포함합니다.

   * **[!UICONTROL Load file]**: 이 활동에서는 Adobe Campaign 서버에 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Reconciliation]**: 이 활동을 통해 타깃팅 차원을 가져온 데이터에 연결할 수 있습니다. This then allows you to create a **List** type audience. If the targeting dimension of the imported data is not known, the audience is **File** type. See [Targeting dimensions and resources](../../automating/using/query.md#targeting-dimensions-and-resources).
   * **[!UICONTROL Save audience]**: 이 활동을 통해 **목록** 유형 대상의 양식으로 가져온 데이터를 저장할 수 있습니다. 저장된 대상의 이름은 사용자가 가져온 파일의 이름과 일치하며, 가져오기의 날짜 및 시간을 지정하는 접미사가 추가됩니다. 예를 들면 다음과 같습니다. ' profiles_ 20150406_ 151448 ' 를 참조하십시오.

이러한 기본 템플릿은 읽기 전용이며 표준 사용자에게는 표시되지 않습니다. 사용자가 사용할 수 있는 템플릿을 만들려면 다음 단계를 수행하십시오.

1. 기본 템플릿을 복제합니다. 복제된 템플릿에는 다음 세 가지 탭이 있습니다.

   * **[!UICONTROL Properties]**: 가져오기 템플릿의 일반 매개 변수. 이 탭에서는 템플릿을 활성화하고 샘플 파일을 업로드할 수 있습니다.
   * **[!UICONTROL Workflow]**: 가져오기 워크플로우를 참조하십시오. 이 탭에서는 워크플로우 활동을 정의할 수 있습니다. 사용자가 수행한 간소화된 가져오는 동안에는 이러한 활동이 표시되지 않습니다.
   * **[!UICONTROL Executed imports]**: 이 템플릿을 사용하여 수행한 가져오기 목록입니다. 이 템플릿을 사용하여 수행한 각 가져오기의 상태, 세부 사항 및 결과를 볼 수 있습니다. 이 목록에서 작업 과정 (사용자의 투명한 방법으로 수행) 에 직접 액세스할 수 있습니다.

1. **[!UICONTROL Properties]** 탭에서 템플릿의 이름을 변경하고 설명을 추가합니다. 템플릿을 사용할 수 있으면 사용자는 설명을 볼 수 있습니다.

   ![](assets/simplified_import_model1.png)

1. **[!UICONTROL Workflow]** 탭으로 이동합니다. 여기서 필요에 따라 새 활동을 추가하여 기본적으로 제공되는 워크플로우를 강화할 수 있습니다.

   For more on how to configure the workflow activities, refer to the use case describe in this section: [Example: Import workflow template](../../automating/using/importing-data.md#example--import-workflow-template). 이 사용 사례는 Adobe Campaign 데이터베이스의 CRM에서 가져온 프로필을 가져오는 데 재사용할 수 있는 워크플로우를 설정하는 데 유용합니다.

1. 워크플로우의 구성이 제대로 고려되도록 템플릿을 저장합니다.
1. Upload a sample file from the **[!UICONTROL Properties]** tab. 업로드된 파일에는 향후 가져오기 또는 샘플 데이터에 필요한 열만 있을 수 있습니다. 샘플 파일의 데이터를 사용하면 워크플로우가 정의된 후 간소화된 가져오기를 테스트할 수 있습니다.

   ![](assets/import_template_sample.png)

   이 샘플 파일은 템플릿을 사용하여 사용자가 가져오기를 수행하는 데 사용할 수 있습니다. 예를 들어 데이터를 가져올 때 데이터를 채울 수 있습니다. 샘플 파일을 추가할 때는 반드시 고려하십시오.

1. 템플릿을 저장합니다. 이제 샘플 파일이 고려됩니다. At any moment you can download it to your computer to check the content, or modify it by checking the **[!UICONTROL Drop a new sample file]** option.

   ![](assets/simplified_import_model2.png)

1. **[!UICONTROL Workflow]** 탭으로 돌아가서 **[!UICONTROL Load file]** 활동을 열어 이전 단계에서 업로드된 샘플 파일의 열 구성을 확인하고 조정합니다.
1. 워크플로우를 시작하여 가져오기를 테스트합니다. The sample file uploaded at step **5** has to contain data.

   그런 다음 샘플 파일의 데이터를 진정으로 가져옵니다. 데이터베이스가 손상되지 않도록 반드시 사용되는 데이터가 작고 사실적인지 확인하십시오.

1. 작업 표시줄에서 사용할 수 있는 워크플로우 실행 로그로 이동합니다. 오류가 발생하면 활동이 올바르게 구성되어 있는지 확인하십시오.

   ![](assets/simplified_import_model3.png)

1. **[!UICONTROL Properties]** 탭에서 대상을 **[!UICONTROL Import template status]** 설정한 **[!UICONTROL Available]**&#x200B;다음 템플릿을 저장합니다. To stop using this template, you can set the **[!UICONTROL Import template status]** to **[!UICONTROL Archived]**.

The template workflow can be modified by re-uploading the sample file and checking the **[!UICONTROL Load file]** configuration.

이제 사용자가 가져오기 템플릿을 사용할 수 있으며 파일을 업로드할 때 사용할 수 있습니다.

**관련 항목:**

* [워크플로우](../../automating/using/discovering-workflows.md)
* [데이터 가져오기](../../automating/using/importing-data.md)
* [예: 워크플로우 템플릿 가져오기](../../automating/using/importing-data.md#example--import-workflow-template)

