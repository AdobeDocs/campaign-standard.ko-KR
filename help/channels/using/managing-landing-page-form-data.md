---
title: 랜딩 페이지 양식 데이터 관리
description: 랜딩 페이지 양식 데이터를 관리하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 5b222ea2-6628-457f-a618-bfc0e5eb93dd
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 899c7152-f415-4df9-b4b4-5ff3470a4e32
context-tags: landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8c24e048c698f7ad699e83a753c114fcfd25f6a0

---


# 랜딩 페이지 양식 데이터 관리{#managing-landing-page-form-data}

## 랜딩 페이지 양식 데이터 속성 변경{#changing-a-landing-page-form-data-properties}

데이터베이스 필드를 입력 영역, 라디오 단추 또는 확인란 유형 블록에 연결할 수 있습니다. 이렇게 하려면 블록을 선택하고 팔레트에 을 **[!UICONTROL Form data]** 입력합니다.

![](assets/delivery_content_9.png)

* 필드 **입력** 영역을 사용하면 양식 필드에 연결할 데이터베이스 필드를 선택할 수 있습니다.
* 필수 **옵션을** 사용하면 사용자가 필드에 입력한 경우에만 페이지의 제출을 승인할 수 있습니다. 필수 필드를 채우지 않으면 오류 메시지가 나타납니다.

## 양식 필드 매핑 {#mapping-form-fields}

입력 필드는 Campaign 데이터베이스에 데이터를 저장하거나 업데이트하는 데 사용됩니다. 이렇게 하려면 데이터베이스 필드를 입력 영역, 라디오 단추 또는 확인란 유형 블록과 연결해야 합니다. 이렇게 하려면:

1. 랜딩 페이지에서 블록을 선택합니다.
1. 팔레트에서 **[!UICONTROL Form data]** 부품을 완료합니다.

   ![](assets/editing_lp_content_4.png)

1. 선택 영역의 양식 필드에 연결할 데이터베이스 필드를 **[!UICONTROL Field]** 선택합니다. 랜딩 페이지는 프로파일과 매핑만 할 수 **있습니다**.

1. 필요한 경우 **[!UICONTROL Mandatory]** 옵션을 선택합니다. 사용자가 이 필드를 완료한 경우에만 페이지를 제출할 수 있습니다. 필수 필드가 완료되지 않으면 사용자가 페이지의 유효성을 검사할 때 오류 메시지가 나타납니다.

1. 선택 영역(예: **[!UICONTROL Text]**&#x200B;선택 영역 **[!UICONTROL Number]**&#x200B;또는 **[!UICONTROL Date]** **[!UICONTROL HTML type of the field]** 선택 영역)을 선택하여 필드 유형을 정의합니다.
필수를 선택하는 **[!UICONTROL Checkbox]**&#x200B;경우 필수가 **[!UICONTROL Field]** 되어 있는지 확인합니다.

>[!NOTE]
>
>기본 제공 랜딩 페이지의 기본 필드는 미리 구성되어 있습니다. 필요에 따라 수정할 수 있습니다.

## 데이터 저장 및 조정{#data-storage-and-reconciliation}

데이터 조정 매개 변수를 사용하면 랜딩 페이지에 입력된 데이터가 사용자가 제출한 후 관리되는 방식을 정의할 수 있습니다.

이렇게 하려면:

1. 랜딩 페이지 대시보드의 ![](assets/edit_darkgrey-24px.png) 아이콘을 통해 액세스한 랜딩 페이지 속성을 편집하고 **[!UICONTROL Job]** 매개 변수를 표시합니다.

   ![](assets/lp_parameters_4.png)

1. 다음을 **[!UICONTROL Reconciliation key]**&#x200B;선택합니다.이러한 데이터베이스 필드(예:이메일, 이름, 성)은 방문자에게 Adobe Campaign 데이터베이스에 이미 알려진 프로필이 있는지 여부를 확인하는 데 사용됩니다. 그러면 정의된 업데이트 전략 매개 변수에 따라 프로파일을 업데이트하거나 생성할 수 있습니다.
1. 다음을 **[!UICONTROL Form parameter mapping]**&#x200B;정의합니다.이 섹션에서는 랜딩 페이지 필드 매개 변수와 조정 키에 사용되는 매개 변수를 매핑할 수 있습니다.
1. 다음을 **[!UICONTROL Update strategy]**&#x200B;선택합니다.조정 키가 기존 데이터베이스 프로필을 복구하는 경우 양식에 입력한 데이터로 이 프로필을 업데이트하도록 선택하거나 이 업데이트를 방지할 수 있습니다.
