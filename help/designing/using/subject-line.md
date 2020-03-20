---
title: 제목 줄 및 이메일 보낸 사람 정의
description: 이메일 디자이너에서 제목 줄 및 이메일 보낸 사람을 정의하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6f89b420f0f98c13da1bfff8f9b1b29e015aef89

---


# 제목 줄 및 이메일 보낸 사람 정의{#defining-the-subject-line-of-an-email}

## Defining the subject line of an email {#subject-line}

메시지 제목은 메시지를 준비하고 전송해야 합니다.

>[!NOTE]
>
>제목 줄이 비어 있으면 메시지 대시보드 및 이메일 디자이너에 경고가 표시됩니다.

1. 이메일을 만듭니다.
1. 이메일 디자이너 홈 페이지의 **[!UICONTROL Properties]** 탭으로 이동합니다(홈 아이콘을 통해 액세스 가능).
1. 섹션을 **[!UICONTROL Subject]** 채웁니다.

   ![](assets/email_designer_subject.png)

1. 해당 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 동적 컨텐츠를 제목 줄에 추가할 수도 있습니다. 자세한 내용은 개인화를 [참조하십시오](../../designing/using/personalization.md).
1. 이메일을 보내기 전에 다른 제목 줄을 시도해 볼 수 있습니다. 자세한 내용은 [이메일의](../../sending/using/testing-subject-line-email.md)제목 줄 테스트를 참조하십시오.

## 이메일의 이메일 보낸 사람 정의 {#email-sender}

보낸 메시지 헤더에 표시될 보낸 사람의 이름을 정의하려면, 이메일 디자이너 홈 페이지(홈 아이콘을 통해 액세스 가능)의 **[!UICONTROL Properties]** 탭으로 이동합니다.

![](assets/delivery_content_edition16.png)

* 이 **[!UICONTROL From: name]** 필드를 사용하면 발신자 이름을 입력할 수 있습니다. 기본적으로 필드에 기본 **보낸 사람 이름** 블록이 자동으로 입력됩니다. 기본 보낸 사람 이메일 주소와 보낸 사람 이름은 고급 메뉴 아래에 있는 Adobe Campaign 로고를 통해 **[!UICONTROL Brands]** 액세스할 수 있도록 **[!UICONTROL Administration > Instance settings > Brand configuration]** 정의됩니다.

   발신자 이름 **** 블록을 클릭하여 발신자 이름을 변경할 수 있습니다. 그런 다음 필드를 편집할 수 있으며 사용할 이름을 입력할 수 있습니다.

   이 필드는 개인화할 수 있습니다. 이렇게 하려면 발신자 이름 아래의 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 동적 컨텐츠를 추가할 수 있습니다. 자세한 내용은 개인화를 [참조하십시오](../../designing/using/personalization.md).

* 이 섹션에서 필드를 편집할 수 **[!UICONTROL From: email address]** 없습니다. 대시보드에서 이메일 속성을 편집하여 변경할 수 있습니다. 자세한 내용은 이메일 [고급 매개 변수](../../administration/using/configuring-email-channel.md#advanced-parameters)목록을 참조하십시오.

>[!NOTE]
>
>헤더 매개 변수는 비워 둘 수 없습니다. 보낸 사람의 주소는 RFC 표준(Email to Send)을 허용해야 합니다. Adobe Campaign은 입력한 이메일 주소 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 컨텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
