---
title: 이메일의 제목 줄 테스트
seo-title: 이메일의 제목 줄 테스트
description: 이메일의 제목 줄 테스트
seo-description: 이메일 디자이너에서 이메일의 제목 줄을 정의하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8b85bbad7458286252a2900ce730288f6e52442e

---

# 제목 테스트 {#testing-a-subject}

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
* **Subject length: This indicator lets you see if the current length of the subject is correct or whether it would need to be longer or shorter.**
* **색상 단어**:대상을 테스트할 때 녹색으로 강조 표시된 단어는 개방 비율 예측을 높이는 데 가장 큰 기여를 하는 단어입니다. 빨간색으로 강조 표시된 단어는 개방 비율 예측을 높이기 위해 가장 적게 기여하는 단어입니다. If you add or remove words in the subject, highlighted words will change.
* **Categories and word suggestions: Towards the lower part of the window, a number of relevant categories for the selected model are displayed.** These categories are sorted by order of importance and they allow you to see whether your subject contains words that are associated with it via a check symbol. Each category contains a set of suggested words that could be used in your subject to make it more relevant and increase the open rate. These words are the words that are used the most often in a given category.

>[!NOTE]
>
>Personalization fields and punctuation marks are stripped from the subject analysis. In the case of dynamic/conditional text, all variants are considered as one subject line.

![](assets/predictive_subject_line_example.png)

## Importing models {#importing-models}

By default, there is no model running on your Adobe Campaign server. There are two ways to get a model and activate the feature:

* You can train a local model from the data of your previous email messages:

   * 이미 Adobe Campaign을 사용하고 있는 경우 로컬 모델은 이미 보낸 메시지에 대해 자동으로 교육됩니다.
   * If you are new to Adobe Campaign, you can extract a CSV file from your previous system/ESP that contains 4 columns: date, subject, sent, opens. To do that, go to  &gt;  &gt;  &gt;  and follow the instructions provided on the successive screens. **[!UICONTROL Administration]****[!UICONTROL Channels]****[!UICONTROL Email]****[!UICONTROL Subject Line Import]** When the subject upload is complete, import a local model as described below. 로컬 모델은 업로드한 데이터로 자동 교육됩니다.
   * Adobe Campaign을 처음 사용하고 위에서 설명한 대로 CSV 파일을 가져올 수 없는 경우, 사전 교육 모델을 사용하거나 로컬 모델을 교육하는 데 필요한 배달 데이터가 시스템에 충분히 있을 때까지 기다릴 수 있습니다. 시스템은 현재 데이터 세트에 패턴을 인식하고 모델을 교육할 충분한 데이터가 포함되어 있는지 자동으로 판별합니다.

      >[!NOTE]
      >
      >고유한 모델을 교육하는 데 필요한 제목 줄은 정의되어 있지 않습니다. 교육하려면 분야별 대사를 다양하게 변형하여 복제하지 않아도 됩니다. 처리할 데이터가 충분하지 않으면 시스템에서 모델을 교육할 수 없습니다. 인스턴스에 대해 하나의 교육된 모델만 가질 수 있습니다.
   로컬 모델을 교육하려면 [여기에서](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) subjectLineTraining.xml을 다운로드하고 [패키지 가져오기](../../automating/using/managing-packages.md) 기능을 사용하여 Adobe Campaign 인스턴스에 업로드합니다. 기술 워크플로우가 자동으로 트레이닝을 수행합니다.

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