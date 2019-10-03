---
title: Testing the subject line of an email
seo-title: Testing the subject line of an email
description: Testing the subject line of an email
seo-description: Discover how to define the subject line of an email in the Email Designer.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3fc0d9d7e90a31ffb34efc33d6f5c148ba5aac90

---

# 이메일의 제목 줄 테스트 {#testing-a-subject}

제목 줄을 테스트하려면 아래 단계를 따르십시오.

1. 이메일을 만들거나 엽니다.
1. 컨텐츠를 열고 해당 입력 필드에 이메일 제목을 입력합니다.
1. 단추를 클릭하여 창에 액세스합니다. **[!UICONTROL Test subject]** **[!UICONTROL Test your subject line]** 여전히 이 창에서 제목을 편집할 수 있습니다.
1. 개방 비율 예측을 고려하도록 올바른 모델을 선택합니다. 각 모델은 특정 업계에 해당하는 몇 가지 모델을 사용할 수 있습니다.
1. Click **[!UICONTROL Test]**.

그러면 해당 주제를 분석합니다.

>[!NOTE]
>
>제목 줄이 너무 짧으면 분석할 수 없으며 오류 메시지가 표시됩니다.

몇 가지 지표가 계산되고 도구 세트가 표시되므로 다음과 같은 작업을 할 수 있습니다.

* **예상 개설 비율**:이 차트는 현재 주제와 함께 이메일에 대해 예상할 수 있는 공개 비율을 보여줍니다.
* **제목 길이**:이 표시기를 사용하면 피사체의 현재 길이가 올바른지 또는 길이가 길어야 하는지 또는 짧아야 하는지 여부를 확인할 수 있습니다.
* **색상 단어**:대상을 테스트할 때 녹색으로 강조 표시된 단어는 개방 비율 예측을 높이는 데 가장 큰 기여를 하는 단어입니다. 빨간색으로 강조 표시된 단어는 개방 비율 예측을 높이기 위해 가장 적게 기여하는 단어입니다. 제목에서 단어를 추가하거나 제거하면 강조 표시된 단어가 변경됩니다.
* **카테고리 및 단어 제안**:창의 아래쪽에 선택한 모델에 대한 여러 관련 카테고리가 표시됩니다. 이러한 카테고리는 중요도 순으로 정렬되며 제목에 확인 기호를 통해 연결된 단어가 포함되어 있는지 여부를 확인할 수 있습니다. 각 카테고리에는 제목에 사용할 수 있는 제안된 단어 집합이 포함되어 있어 관련성이 더 높고 공개 비율을 높일 수 있습니다. 이러한 단어는 특정 카테고리에서 가장 자주 사용되는 단어입니다.

>[!NOTE]
>
>개인화 필드 및 구두점은 제목 분석에서 제거됩니다. 동적/조건부 텍스트의 경우 모든 변형이 하나의 제목 줄로 간주됩니다.

![](assets/predictive_subject_line_example.png)

## 모델 가져오기 {#importing-models}

기본적으로 Adobe Campaign 서버에서 실행 중인 모델이 없습니다. 모델을 가져오고 기능을 활성화하는 방법은 두 가지가 있습니다.

* You can train a local model from the data of your previous email messages:

   * If you are already using Adobe Campaign, the local model will be automatically trained on the messages that you have already sent.
   * If you are new to Adobe Campaign, you can extract a CSV file from your previous system/ESP that contains 4 columns: date, subject, sent, opens. To do that, go to  &gt;  &gt;  &gt;  and follow the instructions provided on the successive screens. **[!UICONTROL Administration]****[!UICONTROL Channels]****[!UICONTROL Email]****[!UICONTROL Subject Line Import]** When the subject upload is complete, import a local model as described below. 로컬 모델은 업로드한 데이터로 자동 교육됩니다.
   * If you are new to Adobe Campaign and cannot get a CSV file as described above, you can use a pre-trained model or wait until you have enough delivery data in your system to train a local model. The system will automatically determine whether your current data set contains enough data to recognize patterns and to train the model.

      >[!NOTE]
      >
      >There is no defined number of subject lines needed to train your own model. 교육하려면 분야별 대사를 다양하게 변형하여 복제하지 않아도 됩니다. If there is not enough data to process, the system will not be able to train the model. You can only have one trained model on your instance.
   To train a local model, download the subjectLineTraining.xml from here and use the package import feature to upload it to your Adobe Campaign instance. [](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter)[](../../automating/using/managing-packages.md) 기술 워크플로우가 자동으로 트레이닝을 수행합니다.

   모델을 처음 교육할 때 관리자는 &gt; **[!UICONTROL SubjectLine Training workflow]** &gt; **[!UICONTROL Administration]** 메뉴에서 **[!UICONTROL Application settings]** **[!UICONTROL Workflows]** 시작하도록 설정할 수 있습니다.

   모델이 업로드되고 교육되면 기능이 자동으로 활성화되고 메시지의 제목 필드 옆에 새로운 옵션이 나타납니다.

   그러면 기술 워크플로우는 매주 자동으로 모델을 교육합니다.

* 특정 산업 분야(의료 등)에 맞는 미리 교육된 모델을 가져올 수 있습니다. 패키지 [가져오기](../../automating/using/managing-packages.md) 기능 사용. 이러한 모델은 [여기에서](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) 이용할 수 있으며 교육을 받을 수 없습니다.

   모델이 업로드되면 기능이 자동으로 활성화되고 메시지의 제목 줄 필드 옆에 새로운 옵션이 나타납니다.

>[!NOTE]
>
>숙련된 모델 가져오기 및 생성은 관리자만 수행할 수 있습니다.

사용할 수 있는 모델은 다음과 같습니다.

* 화장품 업계:subjectInsightCosmetic.xml
* 슈퍼마켓 산업:subject 파섹
* 의료 업계:subjectInsightMedical.xml
* 교육 모델:subjectlineTraining.xml
