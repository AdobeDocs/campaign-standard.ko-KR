---
solution: Campaign Standard
product: campaign
title: 제목란 및 전자 메일 보낸 사람 정의
description: 이메일 디자이너에서 제목란과 이메일 발신자를 정의하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: 이메일 디자인
role: User
level: Beginner
exl-id: 22112517-40f7-4966-84bf-40794e5d0f79
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 2%

---

# 제목란 및 전자 메일 보낸 사람 정의{#defining-the-subject-line-of-an-email}

## 전자 메일의 제목 줄 정의 {#subject-line}

메시지 제목은 메시지를 준비하고 전송해야 합니다.

>[!NOTE]
>
>제목 줄이 비어 있으면 메시지 대시보드 및 이메일 디자이너에 경고가 표시됩니다.

1. 이메일 만들기.
1. 전자 메일 디자이너 홈 페이지의 **[!UICONTROL Properties]** 탭으로 이동합니다(홈 아이콘을 통해 액세스 가능).
1. **[!UICONTROL Subject]** 섹션을 입력합니다.

   ![](assets/email_designer_subject.png)

1. 해당 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 제목 줄에 추가할 수도 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md)를 참조하십시오.

## 전자 메일 보낸 사람 정의 {#email-sender}

보낸 메시지 헤더에 표시되는 발신자의 이름을 정의하려면 이메일 디자이너 홈 페이지의 **[!UICONTROL Properties]** 탭으로 이동합니다(홈 아이콘을 통해 액세스할 수 있음).

![](assets/delivery_content_edition16.png)

* **[!UICONTROL From: name]** 필드에서는 발신자 이름을 입력할 수 있습니다. 기본적으로 필드에 기본 **보낸 사람 이름** 블록이 자동으로 입력됩니다. 기본 발신자 이메일 주소 및 발신자 이름은 고급 메뉴 **[!UICONTROL Administration > Instance settings > Brand configuration]** 아래의 Adobe Campaign 로고를 통해 액세스할 수 있는 **[!UICONTROL Brands]**&#x200B;에 정의되어 있습니다.

   **보낸 사람 이름** 블록을 클릭하여 보낸 사람 이름을 변경할 수 있습니다. 그런 다음 필드를 편집할 수 있게 되고 사용할 이름을 입력할 수 있습니다.

   이 필드는 개인화할 수 있습니다. 이렇게 하려면 발신자 이름 아래의 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 다이내믹 콘텐츠를 추가할 수 있습니다. 자세한 내용은 [개인화](../../designing/using/personalization.md)를 참조하십시오.

* **[!UICONTROL From: email address]** 필드는 이 섹션에서 편집할 수 없습니다. 대시보드에서 전자 메일의 속성을 편집하여 변경할 수 있습니다. 자세한 내용은 [전자 메일 고급 매개 변수 목록](../../administration/using/configuring-email-channel.md#advanced-parameters)을 참조하십시오.

>[!NOTE]
>
>헤더 매개 변수는 비워 둘 수 없습니다. 전자 메일을 보낼 수 있도록 하려면 보낸 사람의 주소가 필수입니다(RFC 표준). Adobe Campaign은 입력한 이메일 주소 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 콘텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
