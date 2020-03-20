---
title: 이메일의 제목란 테스트
description: 이메일 디자이너에서 이메일의 제목 줄을 정의하는 방법을 알아봅니다.
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
source-git-commit: 6f89b420f0f98c13da1bfff8f9b1b29e015aef89

---

# 이메일의 제목란 테스트 {#testing-a-subject}


## 예측 제목 라인 정보 {#about-predictive-subject-line}

이메일을 편집할 때 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다.

이 기능은 기본적으로 비활성화됩니다. 첫 번째 모델을 가져올 때 활성화됩니다. 모델은 해당 업계별 교육 데이터 세트의 결과입니다. 모델을 사용하면 시스템에서 새 제목 줄이 제출될 때 이메일 공개 비율을 예측할 수 있습니다.

>[!NOTE]
>
>이 기능은 이메일 메시지와 영어 내용만 포함하는 데이터베이스에 사용할 수 있습니다. 인스턴스에 다른 언어로 된 이메일이 포함되어 있으면 트레이닝된 모델이 일관되지 않고 잘못된 결과를 초래할 수 있습니다. 모델을 인스턴스에서 이미 사용할 수 있는 경우에만 제목을 테스트할 수 있는 옵션이 표시됩니다.

모델 가져오기에 대한 자세한 내용은 이 [섹션을](#importing-models)참조하십시오.

## 제목 줄 테스트 {#testing-subject-line}

제목 줄을 테스트하려면 아래 단계를 따르십시오.

1. 이메일을 만들거나 엽니다.
1. 컨텐츠를 열고 해당 입력 필드에 이메일 제목을 입력합니다.
1. 단추를 클릭하여 창에 액세스합니다. **[!UICONTROL Test subject]** **[!UICONTROL Test your subject line]** 여전히 이 창에서 제목을 편집할 수 있습니다.
1. 개방 비율 예측을 고려하도록 올바른 모델을 선택합니다. 각 모델은 특정 업계에 해당하는 몇 가지 모델을 사용할 수 있습니다. 모델 사용에 대한 자세한 내용은 이 [섹션을](#importing-models)참조하십시오.
1. 클릭 **[!UICONTROL Test]**.

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

* 이전 이메일 메시지의 데이터에서 로컬 모델을 교육할 수 있습니다.
* 특정 산업 분야(의료 등)에 맞는 미리 교육된 모델을 가져올 수 있습니다. 패키지 [가져오기](../../automating/using/managing-packages.md) 기능 사용.

### 로컬 모델 교육 {#training-local-model}

* 이미 Adobe Campaign을 사용하고 있는 경우 로컬 모델은 이미 보낸 메시지에 대해 자동으로 교육됩니다.
* Adobe Campaign을 처음 사용하는 경우 이전 시스템/ESP에서 4개의 열이 포함된 CSV 파일을 추출할 수 있습니다.날짜, 제목, 열기, 전송 이렇게 하려면 > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email]** > > **[!UICONTROL Subject Line Import]** 로 이동하여 연속 화면에 제공된 지침을 따르십시오. 제목 업로드가 완료되면 아래 설명된 대로 로컬 모델을 가져옵니다. 로컬 모델은 업로드한 데이터로 자동 교육됩니다.
* Adobe Campaign을 처음 사용하고 위에서 설명한 대로 CSV 파일을 가져올 수 없는 경우 [사전 교육 모델을](#pre-trained-models) 사용하거나 로컬 모델을 교육할 수 있는 전달 데이터가 시스템에 충분히 있을 때까지 기다릴 수 있습니다. 시스템은 현재 데이터 세트에 패턴을 인식하고 모델을 교육할 충분한 데이터가 포함되어 있는지 자동으로 판별합니다.

>[!NOTE]
>
>고유한 모델을 교육하는 데 필요한 제목 줄은 정의되어 있지 않습니다. 자세한 내용은 문제 [해결을 참조하십시오](#troubleshooting).
>
>인스턴스에 대해 하나의 교육된 모델만 가질 수 있습니다.

로컬 모델을 교육하려면
1. 여기서 subjectLineTraining.xml을 [다운로드하고](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) [패키지 가져오기](../../automating/using/managing-packages.md) 기능을 사용하여 Adobe Campaign 인스턴스에 업로드합니다. 기술 워크플로우가 자동으로 트레이닝을 수행합니다.
1. 모델을 처음 교육할 때 관리자는 > **[!UICONTROL SubjectLine Training workflow]** > **[!UICONTROL Administration]** 메뉴에서 **[!UICONTROL Application settings]** **[!UICONTROL Workflows]** 시작하도록 설정할 수 있습니다.
1. 모델이 업로드되고 교육되면 기능이 자동으로 활성화되고 메시지의 제목 필드 옆에 새로운 옵션이 나타납니다.
1. 그러면 기술 워크플로우는 매주 자동으로 모델을 교육합니다.

### 미리 교육된 모델 가져오기 {#pre-trained-models}

이러한 모델에 액세스하려면 [여기를](https://support.neolane.net/webApp/extranetLogin) 클릭하고 로 이동합니다 **[!UICONTROL Download Center]**. Adobe Campaign 인스턴스에 모델을 업로드하려면 [패키지 가져오기](../../automating/using/managing-packages.md) 기능을 사용합니다.

사용할 수 있는 모델은 다음과 같습니다.

* 화장품 업계:subjectInsightCosmetic.xml
* 슈퍼마켓 산업:subject 파섹
* 의료 업계:subjectInsightMedical.xml
* 교육 모델:subjectlineTraining.xml

이러한 모델은 교육받을 수 없습니다.

모델이 업로드되면 기능이 자동으로 활성화되고 메시지의 제목 줄 필드 옆에 새로운 옵션이 나타납니다.

>[!NOTE]
>
>숙련된 모델 가져오기 및 생성은 관리자만 수행할 수 있습니다.

## 문제 해결 {#troubleshooting}

예측 제목 줄은 사용자가 업로드한 모든 제목 라인을 개방 비율로 고려하는 기계 학습 프로세스입니다. 그러면 시스템에서 새 제목 줄이 제출될 때 이메일 공개 비율을 예측할 수 있습니다.

모델을 직접 교육하려면 모델 트레이닝에 사용되는 제목 줄 수에 관계 없이 제목 라인이 다양해야 하며 중복되지 않아야 합니다.

주제의 질은 필수적이다. 처리할 품질 데이터가 충분하지 않거나 이전 제목 라인이 너무 유사한 경우 시스템에서 모델을 교육할 수 없으며 오류 메시지가 나타날 수 있습니다. 이는 기존 레코드 집합에서 신뢰할 수 있는 예측 제안을 제공할 수 없음을 의미합니다.

이 경우 업로드하고 있는 데이터를 검토하고 모델 교육을 효율적으로 수행할 수 있도록 제목 라인이 다양한지 확인해야 합니다.

<!--Some clients have reported this issue: I have had the subject line training workflow running for about a year now.  It has trained on 883 records and I am still seeing the message "The existing dataset is not enough to generate a model."  I do get an error in the workflow every time it runs "XML-110009 Unable to find the element 'runwf' of path '/' (document with schema 'serverConf')".

For this, campaign takes the subject line as training data and tries to come up with significant enough model to predict open rate with 95% confidence.

The 400 subject line number is mention with at least and is only indicative, model generation will also depend on quality of these lines.

It may happen that even 10k subject lines don't lead to model generation if they are too similar.

It means that it can be case that you don't have enough subject lines to generate the model and it is giving this error.

If you are getting an error/warning message, it means that your existing set of records is not enough for the predictive subject module to give a high confidence suggestion.

Adobe recommends reviewing the data you are uploading as the similarity of the subject lines might be the issue.-->
