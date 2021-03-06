---
title: 링크 추가
description: 이메일 디자이너에서 링크를 관리하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Intermediate
exl-id: d1714101-bad0-40c1-8d60-90469d033197
source-git-commit: 146dfea38bd456a5d9200b0632d4aa279b10a7b9
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 2%

---

# 링크 추가 {#links}

## 링크 삽입 {#inserting-a-link}

편집기를 사용하면 HTML 컨텐츠 요소에 링크를 삽입하여 이메일 또는 랜딩 페이지를 개인화할 수 있습니다.

링크를 임의의 페이지 요소에 삽입할 수 있습니다. 이미지, 단어, 단어 그룹, 텍스트 블록 등

>[!NOTE]
>
>아래 이미지는 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md) 이메일.

1. 요소를 선택하고 를 클릭합니다 **[!UICONTROL Insert link]** 상황별 도구 모음

   ![](assets/des_insert_link.png)

1. 만들 링크 유형을 선택합니다.

   * **외부 링크**: 외부 URL에 대한 링크를 삽입합니다.

      URL에 대한 개인화를 정의할 수 있습니다. 자세한 내용은 [URL 개인화](personalization.md#personalizing-urls).

   * **랜딩 페이지**: Adobe Campaign 랜딩 페이지에 대한 액세스 권한을 제공합니다.
   * **구독 링크**: Adobe Campaign 서비스에 가입할 링크를 삽입합니다.
   * **구독 취소 링크**: Adobe Campaign 서비스에서 가입을 해지할 링크를 삽입합니다.
   * **작업을 정의하는 링크**: 랜딩 페이지의 요소를 클릭할 때 작업을 정의합니다.

      >[!NOTE]
      >
      >이 유형의 링크는 랜딩 페이지에만 사용할 수 있습니다.

1. 수신자에게 표시되는 텍스트를 수정할 수 있습니다.
1. 사용자가 링크를 클릭할 때(예: 새 창 열기) 브라우저 동작을 설정할 수 있습니다.

   >[!NOTE]
   >
   >브라우저 동작을 정의하면 랜딩 페이지에만 적용됩니다.

1. 변경 내용을 저장합니다.

링크가 만들어져도 설정 창에서 수정할 수 있습니다. 연필 아이콘을 클릭하여 매개 변수를 편집합니다.

![](assets/des_link_edit.png)

을(를) 사용하여 이메일을 편집할 때 [이메일 디자이너](../../designing/using/designing-content-in-adobe-campaign.md)를 채울 경우 이메일에 포함된 모든 URL을 나열하는 테이블에서 만든 링크에 쉽게 액세스하고 수정할 수 있습니다. 이 목록을 사용하면 중앙 집중식 보기를 사용하고 이메일 콘텐츠에서 각 URL을 찾을 수 있습니다. 액세스하려면 다음을 참조하십시오 [추적된 URL 정보](#about-tracked-urls).

![](assets/des_link_list.png)

>[!NOTE]
>
>과 같은 개인화된 URL **미러 페이지 URL** 또는 **구독 취소** 이 목록에서 링크를 수정할 수 없습니다. 다른 모든 링크는 편집할 수 있습니다.

**관련 항목**:

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)

## 추적된 URL 정보 {#about-tracked-urls}

Adobe Campaign을 사용하면 수신자가 이메일에 포함된 URL을 클릭할 때 받는 사람의 동작을 추적할 수 있습니다. 추적에 대한 자세한 내용은 [이 섹션](../../sending/using/tracking-messages.md#about-tracking)을 참조하십시오.

다음 **[!UICONTROL Links]** 작업 표시줄의 아이콘은 추적할 컨텐츠의 모든 URL 목록을 자동으로 표시합니다.

![](assets/des_links.png)

>[!NOTE]
>
>추적은 기본적으로 활성화됩니다. 이 기능은 Adobe Campaign에서 추적이 활성화된 경우 이메일에만 사용할 수 있습니다. 추적 매개 변수에 대한 자세한 내용은 [이 섹션](../../administration/using/configuring-email-channel.md#tracking-parameters).

이 목록에서 각 링크의 URL, 카테고리, 레이블 및 추적 유형을 수정할 수 있습니다. 링크를 편집하려면 해당 연필 아이콘을 클릭합니다.

![](assets/des_links_tracking.png)

추적된 각 URL에 대해 추적 모드를 다음 값 중 하나로 설정할 수 있습니다.

* **추적됨**: 이 URL에서 추적을 활성화합니다.
* **미러 페이지**: 는 이 URL이 미러 페이지 URL인 것으로 간주합니다.
* **절대 안 함**: 이 URL의 추적을 활성화하지 않습니다. 이 정보는 저장됩니다. url이 향후 메시지에 다시 표시되면 해당 추적은 자동으로 비활성화됩니다.
* **옵트아웃**: 은 이 URL을 옵트아웃 또는 구독 취소 URL로 간주합니다.

![](assets/des_link_tracking_type.png)

각 URL에 대한 추적을 비활성화하거나 활성화할 수도 있습니다.

>[!NOTE]
>
>기본적으로 Adobe Campaign에서 를 제외한 모든 컨텐츠 URL이 추적됩니다 **미러 페이지 URL** 및 **구독 취소** 링크를 클릭합니다.

를 편집하여 URL을 다시 그룹화할 수 있습니다 **[!UICONTROL Category]** 필드에 입력할 수 있습니다. 이러한 카테고리는 다음과 같이 보고서를 표시할 수 있습니다 [URL 및 클릭 스트림](../../reporting/using/urls-and-click-streams.md).

![](assets/des_link_tracking_category.png)

보고서를 작성할 때, **[!UICONTROL Components]** 탭, 선택 **[!UICONTROL Dimension]** 및 목록 아래로 스크롤하여 추적 구성 요소에 액세스합니다. 예를 들어 끌어서 놓습니다 **[!UICONTROL Tracking URL Category]** 를 작업 공간으로 가져온 후 클릭한 각 URL의 추적 카테고리에 따라 결과를 표시합니다.

![](assets/des_link_tracking_report.png)

사용자 지정 보고서 작성에 대한 자세한 내용은 [이 섹션](../../reporting/using/about-dynamic-reports.md).
