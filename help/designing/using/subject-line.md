---
title: 제목 줄 및 이메일 보낸 사람 정의
seo-title: 제목 줄 및 이메일 보낸 사람 정의
description: 제목 줄 및 이메일 보낸 사람 정의
seo-description: 이메일 디자이너에서 제목 줄 및 이메일 보낸 사람을 정의하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 디자인
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5847c89b97ede8b03e75d1d90f31c88ed5c8a84e

---


# Defining the subject line and the sender of an email{#defining-the-subject-line-of-an-email}

메시지 제목은 메시지를 준비하고 전송해야 합니다.

>[!NOTE]
>
>If the subject line is empty, a warning is displayed in the message dashboard and in the Email Designer.

To configure the email subject, go the  tab of the Email Designer home page (accessible through the home icon) and fill in the  section.**[!UICONTROL Properties]****[!UICONTROL Subject]**

**To define the subject line of an email:**

1. Create an email.
1. 홈 페이지를 닫습니다.
1. Go the  tab of the Email Designer home page (accessible through the home icon) and fill in the  section.**[!UICONTROL Properties]****[!UICONTROL Subject]**

![](assets/email_designer_subject.png)

You can also add personalization fields, content blocks and dynamic content to the subject line by clicking the corresponding icons.

**Related topics:**

* [Inserting a personalization field](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 컨텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)

## 예측 제목 줄 {#predictive-subject-line}

이메일을 편집할 때 다른 제목 줄을 시도해 보고 보내기 전에 공개 비율을 예측할 수 있습니다.

이 기능은 기본적으로 비활성화됩니다. 첫 번째 모델을 가져올 때 활성화됩니다. 모델은 해당 업계별 교육 데이터 세트의 결과입니다. 모델을 사용하면 시스템에서 새 제목 줄이 제출될 때 이메일 공개 비율을 예측할 수 있습니다.

>[!NOTE]
>
>이 기능은 이메일 메시지와 영어 내용만 포함하는 데이터베이스에 사용할 수 있습니다. 인스턴스에 다른 언어로 된 이메일이 포함되어 있으면 트레이닝된 모델이 일관되지 않고 잘못된 결과를 초래할 수 있습니다. 모델을 인스턴스에서 이미 사용할 수 있는 경우에만 제목을 테스트할 수 있는 옵션이 표시됩니다.

**관련 항목**

* [이메일의 제목 줄 테스트](../../sending/using/testing-subject-line-email.md)

## 이메일 보낸 사람 {#email-sender}

보낸 메시지 헤더에 표시될 보낸 사람의 이름을 정의하려면, 이메일 디자이너 홈 페이지(홈 아이콘을 통해 액세스 가능)의 **[!UICONTROL Properties]** 탭으로 이동합니다.

![](assets/delivery_content_edition16.png)

* The  field allows you to enter the sender name. **[!UICONTROL From: name]** By default, the default Sender name block is automatically entered in the field. **** Adobe Campaign refers to the email channel configuration (from the advanced menu  via the Adobe Campaign logo) to designate this sender.**[!UICONTROL Administration > Channels > Email > Email accounts]**

   발신자 이름 **** 블록을 클릭하여 발신자 이름을 변경할 수 있습니다. 그런 다음 필드를 편집할 수 있으며 사용할 이름을 입력할 수 있습니다.

   This field can be personalized. 이렇게 하려면 발신자 이름 아래의 아이콘을 클릭하여 개인화 필드, 콘텐츠 블록 및 동적 컨텐츠를 추가할 수 있습니다.

* 이 섹션에서 필드를 편집할 수 **[!UICONTROL From: email address]** 없습니다. 대시보드에서 이메일 속성을 편집하여 변경할 수 있습니다. 자세한 내용은 이메일 [고급 매개 변수](../../administration/using/configuring-email-channel.md#advanced-parameters)목록을 참조하십시오.

>[!NOTE]
>
>헤더 매개 변수는 비워 둘 수 없습니다. 보낸 사람의 주소는 RFC 표준(Email to Send)을 허용해야 합니다. Adobe Campaign은 입력한 이메일 주소 구문을 확인합니다.

**관련 항목:**

* [개인화 필드 삽입](../../designing/using/personalization.md#inserting-a-personalization-field)
* [콘텐츠 블록 추가](../../designing/using/personalization.md#adding-a-content-block)
* [이메일에서 동적 컨텐츠 정의](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)
