---
title: 제목란 및 전자 메일 보낸 사람 정의
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

# 제목란 및 전자 메일 보낸 사람 정의{#defining-the-subject-line-of-an-email}

## 전자 메일의 제목 줄 정의 {#subject-line}

메시지 제목은 메시지를 준비하고 전송해야 합니다.

>[!NOTE]
>
>제목 줄이 비어 있으면 메시지 대시보드 및 이메일 디자이너에 경고가 표시됩니다.

1. 이메일 만들기.
1. 이동 **[!UICONTROL Properties]** 이메일 디자이너 홈페이지의 탭(홈 아이콘을 통해 액세스 가능).
1. 을 입력합니다. **[!UICONTROL Subject]** 섹션을 참조하십시오.

   ![](assets/email_designer_subject.png)

1. 해당 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 제목 줄에 추가할 수도 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md).

## 전자 메일 보낸 사람 정의 {#email-sender}

보낸 메시지 헤더에 표시될 발신자의 이름을 정의하려면 **[!UICONTROL Properties]** 이메일 디자이너 홈페이지의 탭(홈 아이콘을 통해 액세스 가능).

![](assets/delivery_content_edition16.png)

* 다음 **[!UICONTROL From: name]** 필드에서는 발신자명을 입력할 수 있습니다. 기본적으로 **발신자 이름** 블록은 필드에 자동으로 입력됩니다. 기본 발신자 이메일 주소와 발신자 이름은 **[!UICONTROL Brands]** 고급 메뉴 아래에 있는 Adobe Campaign 로고를 통해 액세스할 수 있습니다 **[!UICONTROL Administration > Instance settings > Brand configuration]** .

   을 클릭하여 발신자 이름을 변경할 수 있습니다. **발신자 이름** 차단. 그런 다음 필드를 편집할 수 있게 되고 사용할 이름을 입력할 수 있습니다.

   이 필드는 개인화할 수 있습니다. 이렇게 하려면 발신자 이름 아래의 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 추가할 수 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md).

* 다음 **[!UICONTROL From: email address]** 이 섹션에서 필드를 편집할 수 없습니다. 대시보드에서 전자 메일의 속성을 편집하여 변경할 수 있습니다. 자세한 내용은 [전자 메일 고급 매개 변수 목록](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>헤더 매개 변수는 비워 둘 수 없습니다. 전자 메일을 보낼 수 있도록 하려면 보낸 사람의 주소가 필수입니다(RFC 표준). Adobe Campaign은 입력한 이메일 주소 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
