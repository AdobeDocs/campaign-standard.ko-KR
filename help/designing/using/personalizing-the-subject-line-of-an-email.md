---
title: 이메일의 제목 맞춤화
seo-title: 이메일의 제목 맞춤화
description: 이메일의 제목 맞춤화
seo-description: 이메일의 제목을 개인화하고 다른 제목 라인을 사용해 볼 수 있으며 열람률을 예측할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 345 B 5 F 4 B -8 E 2 C -4 F 8 E-BCE 7-0 E 9 B 40 A 44932
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 맞춤형 컨텐츠
discoiquuid: F 7 A 5 E 935-54 CF -422 E -8459-27221409 A 200
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 782a5f89b0361f1cbe59c9b353ca90dec90c3906

---


# 이메일의 제목 맞춤화{#personalizing-the-subject-line-of-an-email}

## 이메일 제목 개인화 {#personalizing-an-email-subject}

메시지 제목은 메시지를 준비하고 보내는 것이 필수적입니다.

>[!NOTE]
>
>제목 라인이 비어 있으면 메시지 대시보드와 이메일 디자이너에 경고가 표시됩니다.

이메일 제목을 구성하려면 홈 아이콘을 통해 액세스 가능한 이메일 디자이너 홈 페이지의 **[!UICONTROL Properties]** 탭으로 이동하여 **[!UICONTROL Subject]** 섹션을 채웁니다.

![](assets/email_designer_subject.png)

해당 아이콘을 클릭하여 개인화 필드, 컨텐츠 블록 및 동적 컨텐트를 제목 줄에 추가할 수도 있습니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/inserting-a-personalization-field.md)
* [컨텐츠 블록 추가](../../designing/using/adding-a-content-block.md)
* [이메일에서 동적 컨텐츠 정의](../../designing/using/defining-dynamic-content-in-an-email.md)

## 예측 제목 라인 {#predictive-subject-line}

이메일을 편집할 때 다른 제목 선을 시험해 보고 보내기 전에 열린 비율을 예측할 수 있습니다.

이 기능은 기본적으로 비활성화되어 있습니다. 첫 번째 모델을 가져올 때 활성화됩니다. 모델은 해당 산업 관련 교육 데이터 세트의 결과입니다. 모델을 사용하면 시스템이 새 제목 행을 제출할 때 이메일의 공개 비율을 예측할 수 있습니다.

>[!NOTE]
>
>이 기능은 이메일 메시지와 영어 컨텐츠만 포함된 데이터베이스에 사용할 수 있습니다. 교육 모델은 일관성이 없고 인스턴스에 다른 언어로 이메일이 포함된 경우 잘못된 결과가 표시됩니다. 제목을 테스트할 수 있는 옵션은 인스턴스에서 모델을 이미 사용할 수 있는 경우에만 표시됩니다.

### 피사체 테스트 {#testing-a-subject}

제목 라인을 테스트하려면 다음을 수행하십시오.

1. 이메일을 만들거나 엽니다.
1. 콘텐트를 열고 해당 입력 필드에 이메일의 제목을 입력합니다.
1. **[!UICONTROL Test subject]** 단추를 클릭하여 **[!UICONTROL Test your subject line]** 창에 액세스합니다. 여전히 이 창에서 피사체를 편집할 수 있습니다.
1. 개방 비율 예측을 고려하려면 올바른 모델을 선택합니다. 특정 업종에 해당하는 여러 모델이 제공됩니다.
1. **[!UICONTROL Test]**&#x200B;을 클릭합니다.

그러면 주제가 분석됩니다.

>[!NOTE]
>
>제목 줄이 너무 짧으면 분석할 수 없으며 오류 메시지가 표시됩니다.

다음과 같이 여러 개의 표시기가 계산되고 도구 세트가 표시됩니다.

* **예상 개방 비율**: 이 차트는 현재 제목으로 이메일에 대해 예상할 수 있는 공개 비율에 대한 아이디어를 제공합니다.
* **제목 길이**: 이 표시기를 사용하면 피사체의 현재 길이가 올바른지 또는 길거나 짧아야 하는지를 확인할 수 있습니다.
* **색상 단어**: 제목을 테스트할 때 녹색으로 강조 표시된 단어는 개방 비율 예측을 높이는 데 가장 많이 기여하는 단어입니다. 빨간색으로 강조 표시된 단어는 개방 비율 예측을 증가시키기 위해 가장 적게 기여하는 단어입니다. 제목에서 단어를 추가하거나 제거하면 강조 표시된 단어가 바뀝니다.
* **카테고리 및 단어 제안**: 창의 아랫부분으로, 선택한 모델에 대한 많은 관련 카테고리가 표시됩니다. 이러한 카테고리는 중요도 순으로 정렬되며, 이를 통해 확인 기호를 통해 제목에 연관된 단어가 포함되어 있는지 확인할 수 있습니다. 각 카테고리에는 제목에 사용할 수 있는 제안 단어 세트가 포함되어 있어 이를 관련성을 높이고 비율을 높일 수 있습니다. 이러한 단어는 해당 카테고리에서 가장 자주 사용되는 단어입니다.

>[!NOTE]
>
>개인화 필드와 구두점은 주제 분석에서 제거됩니다. 동적/조건부 텍스트의 경우 모든 변형이 하나의 제목 라인으로 간주됩니다.

![](assets/predictive_subject_line_example.png)

### 모델 가져오기 {#importing-models}

기본적으로 Adobe Campaign 서버에서 실행 중인 모델은 없습니다. 모델을 가져오고 기능을 활성화하는 방법에는 두 가지가 있습니다.

* 이전 이메일 메시지의 데이터에서 로컬 모델을 트레이닝할 수 있습니다.

   * 이미 Adobe Campaign를 사용하고 있는 경우 이미 보낸 메시지에 대해 로컬 모델이 자동으로 트레이닝됩니다.
   * Adobe Campaign를 처음 사용하는 경우 4 개의 열이 포함된 이전 시스템/ESP에서 CSV 파일을 추출할 수 있습니다. 날짜, 제목, 전송됨. 이렇게 하려면 **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Email]** &gt; **[!UICONTROL Subject Line Import]** 를 클릭하고 연속된 화면에 제공된 지침을 따르십시오. 주제 업로드가 완료되면 아래 설명된 대로 로컬 모델을 가져옵니다. 로컬 모델은 업로드한 데이터로 자동으로 트레이닝됩니다.
   * Adobe Campaign를 처음 사용하고 위에서 설명한 CSV 파일을 가져올 수 없는 경우 사전 훈련된 모델을 사용하거나 시스템에 있는 배달 데이터가 충분히 있을 때까지 기다렸다가 해당 지역의 모델을 교육할 수 있습니다. 시스템은 현재 데이터 세트에 패턴을 인식하고 모델을 트레이닝할 충분한 데이터가 포함되어 있는지 자동으로 결정합니다.

      >[!NOTE]
      >
      >자신의 모델을 교육하는 데 필요한 제목 줄의 수는 정해져 있지 않습니다. 트레이닝을 하려면 제목 라인이 다양해야 하며 중복되지 않아야 합니다. 처리할 데이터가 충분하지 않으면 시스템은 모델을 트레이닝할 수 없게 됩니다. 인스턴스에는 교육 모델이 하나만 있을 수 있습니다.
   로컬 모델을 트레이닝하려면 [여기에서](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) subjectLineTraining.xml를 다운로드하고 [패키지 가져오기](../../automating/using/managing-packages.md) 기능을 사용하여 Adobe Campaign 인스턴스에 업로드합니다. 기술 워크플로우는 자동으로 교육을 수행합니다.

   모델을 처음 트레이닝할 때 관리자는 **[!UICONTROL SubjectLine Training workflow]****[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]****[!UICONTROL Workflows]** &gt; 메뉴에서 강제로 시작할 수 있습니다.

   모델이 업로드되고 트레이닝되면 기능이 자동으로 활성화되고 메시지의 제목 라인 필드 옆에 새로운 옵션이 나타납니다.

   그러면 기술 워크플로우에서 매주 모델을 자동으로 교육할 수 있습니다.

* 특정 업계 (의료 등) 에 특화된 사전 교육을 받은 모델을 가져올 수 있습니다. [패키지 가져오기](../../automating/using/managing-packages.md) 기능 사용을 참조하십시오. 이러한 모델은 여기에서 사용할 수 있으며 [교육을](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) 받을 수 없습니다.

   모델이 업로드되면 기능이 자동으로 활성화되고 메시지의 제목 라인 필드 옆에 새로운 옵션이 나타납니다.

>[!NOTE]
>
>교육 모델을 가져오고 생성하는 작업은 관리자만 수행할 수 있습니다.

사용할 수 있는 모델은 다음과 같습니다.

* 화장품 산업: subjectInsightCosmetic.xml
* 슈퍼마켓 업계: subjectInsightSupermarket.xml
* 의료 업계: subjectInsightMedical.xml
* Model to Train: Subjectlinetraining. xml를 참조하십시오.

**관련 항목:**

* [Adobe Sensei 예측으로 제목 최적화](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Createcompellingcontenttailoredtoeveryindividual)
