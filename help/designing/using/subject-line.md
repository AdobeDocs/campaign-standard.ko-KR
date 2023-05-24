---
title: 제목란 및 이메일 발신자 정의
description: 이메일 디자이너에서 제목란과 이메일 발신자를 정의하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Beginner
exl-id: 22112517-40f7-4966-84bf-40794e5d0f79
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 2%

---

# 제목란 및 이메일 발신자 정의{#defining-the-subject-line-of-an-email}

## 이메일의 제목란 정의 {#subject-line}

메시지 제목은 메시지를 준비하고 보내는 데 필수입니다.

>[!NOTE]
>
>제목 줄이 비어 있으면 메시지 대시보드와 이메일 디자이너에 경고가 표시됩니다.

1. 이메일 만들기.
1. 이동 **[!UICONTROL Properties]** 이메일 디자이너 홈 페이지의 탭(홈 아이콘을 통해 액세스 가능).
1. 다음을 입력합니다. **[!UICONTROL Subject]** 섹션.

   ![](assets/email_designer_subject.png)

1. 해당 아이콘을 클릭하여 제목 줄에 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 추가할 수도 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md).

## 이메일의 이메일 발신자 정의 {#email-sender}

보낸 메시지의 헤더에 나타나는 보낸 사람의 이름을 정의하려면 **[!UICONTROL Properties]** 이메일 디자이너 홈 페이지의 탭(홈 아이콘을 통해 액세스 가능).

![](assets/delivery_content_edition16.png)

* 다음 **[!UICONTROL From: name]** 필드에서는 발신자 이름을 입력할 수 있습니다. 기본적으로 **보낸 사람 이름** 블록은 필드에 자동으로 입력됩니다. 기본 발신자 이메일 주소 및 발신자 이름은에 정의되어 있습니다. **[!UICONTROL Brands]** 고급 메뉴 아래의 Adobe Campaign 로고를 통해 액세스할 수 있습니다 **[!UICONTROL Administration > Instance settings > Brand configuration]** .

   다음을 클릭하여 발신자 이름을 변경할 수 있습니다. **보낸 사람 이름** 차단합니다. 그러면 필드를 편집할 수 있고 사용할 이름을 입력할 수 있습니다.

   이 필드는 개인화할 수 있습니다. 이렇게 하려면 보낸 사람 이름 아래의 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 추가할 수 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md).

* 다음 **[!UICONTROL From: email address]** 필드는 이 섹션에서 편집할 수 없습니다. 대시보드에서 이메일의 속성을 편집하여 변경할 수 있습니다. 자세한 내용은 [이메일 고급 매개 변수 목록](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>헤더 매개 변수는 비워 둘 수 없습니다. 이메일을 보낼 수 있도록 하려면 발신자 주소가 필요합니다(RFC 표준). Adobe Campaign은 입력한 이메일 주소의 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
