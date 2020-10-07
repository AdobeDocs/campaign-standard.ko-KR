---
title: 이메일 제목란 테스트
description: 이메일 디자이너에서 이메일의 제목 줄을 정의하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 1%

---

# 이메일 제목란 테스트 {#testing-a-subject}


## 예측 제목 라인 정보 {#about-predictive-subject-line}

이메일을 편집할 때 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다.

이 기능은 기본적으로 비활성화됩니다. 첫 번째 모델을 가져올 때 활성화됩니다. 모델은 특정 업계에만 적용되는 교육 데이터 세트의 결과입니다. 모델을 사용하면 시스템에서 새로운 제목 라인이 제출될 때 이메일 공개 비율을 예측할 수 있습니다.

>[!NOTE]
>
>이 기능은 이메일 메시지와 영어 내용만 포함된 데이터베이스에 사용할 수 있습니다. 인스턴스에 다른 언어로 된 이메일이 포함되어 있으면 트레이닝된 모델이 일치하지 않고 잘못된 결과를 초래할 수 있습니다. 모델을 인스턴스에서 이미 사용할 수 있는 경우에만 제목을 테스트할 수 있는 옵션이 표시됩니다.

For more on importing models, see this [section](#importing-models).

## 제목 라인 테스트 {#testing-subject-line}

제목 줄을 테스트하려면 아래 단계를 따르십시오.

1. 이메일을 만들거나 엽니다.
1. 컨텐츠를 열고 해당 입력 필드에 이메일 제목을 입력합니다.
1. Click the **[!UICONTROL Test subject]** button to access the **[!UICONTROL Test your subject line]** window. 이 창에서도 제목을 편집할 수 있습니다.
1. 열림 비율 예측을 고려하여 고려할 올바른 모델을 선택합니다. 각 모델은 특정 산업에 해당하는 여러 모델을 사용할 수 있습니다. For more on using models, see this [section](#importing-models).
1. **[!UICONTROL Test]**&#x200B;을(를) 클릭합니다.

그러면 주제가 분석됩니다.

>[!NOTE]
>
>제목 줄이 너무 짧은 경우 분석할 수 없으며 오류 메시지가 표시됩니다.

몇 가지 지표가 계산되고 도구 세트가 표시되므로 다음과 같은 작업을 수행할 수 있습니다.

* **예상 개설 비율**:이 차트에는 현재 제목에 해당하는 이메일에 대해 예상할 수 있는 개방 비율의 개념이 표시됩니다.
* **제목 길이**:이 표시기를 사용하면 피사체의 현재 길이가 정확한지 또는 길어야 하는지 여부를 확인할 수 있습니다.
* **색상 단어**:대상을 테스트할 때 녹색으로 강조 표시된 단어는 개방률 예측을 높이는 데 가장 도움이 되는 단어입니다. 빨간색으로 강조된 단어는 개방률 예측을 높이기 위해 가장 적게 기여하는 단어이다. 제목에 단어를 추가하거나 제거하면 강조 표시된 단어가 변경됩니다.
* **카테고리 및 단어 제안**:창 하단에는 선택한 모델에 대한 다양한 관련 카테고리가 표시됩니다. 이러한 카테고리는 중요도의 순서로 정렬되며, 피사체에 확인 기호를 통해 연결된 단어가 포함되어 있는지 여부를 확인할 수 있습니다. 각 부문에는 제목에 사용할 수 있는 제안된 단어 세트가 포함되어 있어 보다 관련성이 높고 개방률을 높일 수 있습니다. 이러한 단어는 특정 카테고리에서 가장 자주 사용되는 단어입니다.

>[!NOTE]
>
>개인화 필드 및 구두점 표시는 대상 분석에서 제거됩니다. 동적/조건부 텍스트의 경우 모든 변형이 하나의 제목 줄로 간주됩니다.

![](assets/predictive_subject_line_example.png)

## 모델 가져오기 {#importing-models}

기본적으로 Adobe Campaign 서버에서 실행 중인 모델이 없습니다. 두 가지 방법으로 모델을 가져오고 기능을 활성화할 수 있습니다.

* 이전 이메일 메시지의 데이터에서 로컬 모델을 교육할 수 있습니다.
* 특정 산업 분야(의료 등)에만 해당되는 사전 교육된 모델을 가져올 수 있습니다. 패키지 [가져오기](../../automating/using/managing-packages.md) 기능 사용

### 로컬 모델 교육 {#training-local-model}

* 이미 Adobe Campaign을 사용하고 있는 경우 해당 로컬 모델은 이미 전송한 메시지에 대해 자동으로 교육을 받게 됩니다.
* Adobe Campaign을 처음 사용하는 경우 이전 시스템/ESP에서 4개의 열이 포함된 CSV 파일을 추출할 수 있습니다.date, subject, opens, sent. 이렇게 하려면 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > **[!UICONTROL Subject Line Import]** 로 이동하여 연속적인 화면에 제공된 지침을 따릅니다. 제목 업로드가 완료되면 아래 설명된 대로 로컬 모델을 가져옵니다. 로컬 모델은 업로드한 데이터로 자동 교육됩니다.
* Adobe Campaign을 처음 사용하고 위에서 설명한 대로 CSV 파일을 가져올 수 없는 경우 [사전 교육을 받은 모델을](#pre-trained-models) 사용하거나 로컬 모델을 교육하는 데 필요한 배달 데이터가 시스템에 충분할 때까지 기다릴 수 있습니다. 시스템은 현재 데이터 세트에 패턴을 인식하고 모델을 교육할 충분한 데이터가 포함되어 있는지 여부를 자동으로 결정합니다.

>[!NOTE]
>
>고유한 모델을 교육하는 데 필요한 제목 줄의 개수는 정의되어 있지 않습니다. For more on this, see [Troubleshooting](#troubleshooting).
>
>인스턴스에 대해 하나의 교육된 모델만 가질 수 있습니다.

로컬 모델을 교육하려면
1. 여기에서 subjectLineTraining.xml을 [다운로드하고](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html) [패키지 가져오기](../../automating/using/managing-packages.md) 기능을 사용하여 Adobe Campaign 인스턴스에 업로드합니다. 기술 워크플로우는 자동으로 교육을 수행합니다.
1. 모델을 처음 교육할 때 관리자가 > **[!UICONTROL SubjectLine Training workflow]** > **[!UICONTROL Administration]** 메뉴에서 **[!UICONTROL Application settings]** **[!UICONTROL Workflows]** 를 강제로 시작할 수 있습니다.
1. 모델이 업로드되고 교육되면 기능이 자동으로 활성화되고 메시지 제목 필드 옆에 새로운 옵션이 나타납니다.
1. 그러면 기술 워크플로우는 매주 자동으로 모델을 교육합니다.

### 미리 교육된 모델 가져오기 {#pre-trained-models}

이러한 모델에 액세스하려면 [여기를 클릭하십시오](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html). 패키지 [가져오기](../../automating/using/managing-packages.md) 기능을 사용하여 모델을 Adobe Campaign 인스턴스에 업로드합니다.

사용할 수 있는 모델은 다음과 같습니다.

* 화장품 업계:subjectInsightCosmetic.xml
* 슈퍼마켓 산업:subjectInsightSupermarket.xml
* 의료 업계:subjectInsightMedical.xml
* 트레이닝 모델:subjectlineTraining.xml

이러한 모델들은 교육받을 수 없다.

모델이 업로드되면 기능이 자동으로 활성화되고 메시지 제목 필드 옆에 새로운 옵션이 나타납니다.

>[!NOTE]
>
>교육된 모델 가져오기 및 생성은 관리자만 수행할 수 있습니다.

## 문제 해결 {#troubleshooting}

예측 제목 라인은 사용자가 업로드한 모든 제목 라인을 해당 개설 비율로 고려하는 기계 학습 프로세스입니다. 이를 통해 시스템은 새로운 제목 라인이 제출되면 이메일의 공개 비율을 예측할 수 있습니다.

모델을 직접 교육하려면 모델 교육에 사용되는 제목 줄 수에 관계없이 제목 라인이 다양해야 하며 중복되지 않아야 합니다.

주제 자료의 질은 필수적이다. 처리할 품질 데이터가 충분하지 않거나 이전 제목 라인이 너무 유사한 경우 시스템에서 모델을 교육할 수 없으며 오류 메시지가 나타날 수 있습니다. 이는 기존 레코드 세트에서 신뢰할 수 있는 예측 제안을 제공하지 않는다는 것을 의미합니다.

이 경우 업로드하고 있는 데이터를 검토하고 모델 교육을 효율적으로 수행할 수 있도록 제목 라인이 충분히 변경되었는지 확인해야 합니다.

<!--Some clients have reported this issue: I have had the subject line training workflow running for about a year now.  It has trained on 883 records and I am still seeing the message "The existing dataset is not enough to generate a model."  I do get an error in the workflow every time it runs "XML-110009 Unable to find the element 'runwf' of path '/' (document with schema 'serverConf')".

For this, campaign takes the subject line as training data and tries to come up with significant enough model to predict open rate with 95% confidence.

The 400 subject line number is mention with at least and is only indicative, model generation will also depend on quality of these lines.

It may happen that even 10k subject lines don't lead to model generation if they are too similar.

It means that it can be case that you don't have enough subject lines to generate the model and it is giving this error.

If you are getting an error/warning message, it means that your existing set of records is not enough for the predictive subject module to give a high confidence suggestion.

Adobe recommends reviewing the data you are uploading as the similarity of the subject lines might be the issue.-->
