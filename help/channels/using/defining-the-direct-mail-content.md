---
title: DM 컨텐츠 정의
seo-title: DM 컨텐츠 정의
description: DM 컨텐츠 정의
seo-description: 다이렉트 메일 배달에 사용할 컨텐츠를 정의하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: c1234c06-4d22-46d7-ad1b-3c88660f9b06
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 채널
content-type: reference
topic-tags: 다이렉트 메일
discoiquuid: 9e73d6b5-41b4-474b-a880-a0cd5999c2d1
context-tags: delivery,directMailContent,뒤로
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 781904d58f520987e978ad5d1cdc9e34871ca876

---


# DM 컨텐츠 정의{#defining-the-direct-mail-content}

작성 마법사의 마지막 화면에서 또는 배달 대시보드의 컨텐츠 **섹션을 클릭하여 컨텐츠를** 정의할 수 있습니다.

![](assets/direct_mail_6.png)

정의 **[!UICONTROL Content]** 화면은 다이렉트 메일 채널에만 적용됩니다. 4개의 탭으로 나뉘어집니다. **[!UICONTROL Extraction]**&#x200B;및 **[!UICONTROL File structure]****[!UICONTROL Header]** 를 **[!UICONTROL Footer]**&#x200B;참조하십시오.

![](assets/direct_mail_11.png)

## 추출 정의 {#defining-the-extraction}

1. 먼저 추출 파일의 이름을 정의합니다. 필드 오른쪽의 단추를 클릭하고 원하는 레이블을 **[!UICONTROL Output file]** 입력합니다. 개인화 필드, 콘텐츠 블록 및 동적 텍스트를 사용할 수 있습니다(컨텐츠 [정의 참조](../../designing/using/personalization.md#example-email-personalization)). 예를 들어 배달 ID 또는 추출 날짜를 사용하여 레이블을 완료할 수 있습니다.

   ![](assets/direct_mail_12.png)

1. 출력 열을 추가하려면 **[!UICONTROL +]** 또는 **[!UICONTROL Add an element]** 단추를 클릭합니다. 를 **[!UICONTROL Output columns]** 사용하면 출력 파일로 내보낼 프로필 정보(열)를 정의할 수 있습니다.

   >[!CAUTION]
   >
   >이 정보는 다이렉트 메일 제공업체에 필수이므로 프로필에 우편 주소를 포함해야 합니다. 또한 프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택했는지 확인하십시오. 권장 사항을 [참조하십시오](../../channels/using/about-direct-mail.md#recommendations).

   ![](assets/direct_mail_13.png)

1. 필요한 만큼 열을 만듭니다. 표현식과 레이블을 클릭하여 열을 편집할 수 있습니다.

>[!NOTE]
>
>출력 열 정의에 대한 자세한 내용은 Extract 파일 [](../../automating/using/extract-file.md) 워크플로우 활동 섹션을 참조하십시오.

## 파일 구조 정의 {#defining-the-file-structure}

파일 **구조** 탭에서는 내보낼 파일의 출력, 날짜 및 번호 형식을 구성할 수 있습니다.

![](assets/direct_mail_14.png)

>[!NOTE]
>
>사용 가능한 옵션은 Extract 파일 [](../../automating/using/extract-file.md) 워크플로우 활동 섹션에서 자세히 설명합니다.

## 머리글 및 바닥글 정의 {#defining-the-header-and-footer}

경우에 따라 추출 파일의 시작 또는 끝 부분에 정보를 추가해야 할 수 있습니다. 이렇게 하려면 **[!UICONTROL Header]** 구성 화면의 **[!UICONTROL Footer]** 및 **[!UICONTROL Content]** 탭을 사용합니다.

![](assets/direct_mail_7.png)

예를 들어 다이렉트 메일 공급자의 경우 파일 헤더에 발신자 정보를 포함할 수 있습니다. 바닥글과 헤더를 배달 컨텍스트에서 사용할 수 있는 정보로 개인화할 수 있습니다. 컨텐츠 [정의를](../../designing/using/personalization.md#example-email-personalization)참조하십시오.

보낸 사람 주소는 DM 속성 **[!UICONTROL Send]** 섹션 또는 템플릿 수준에서 정의됩니다.

![](assets/direct_mail_24.png)

