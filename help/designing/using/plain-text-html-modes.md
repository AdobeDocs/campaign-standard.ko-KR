---
title: 일반 텍스트 및 HTML 모드
seo-title: 일반 텍스트 및 HTML 모드
description: 일반 텍스트 및 HTML 모드
seo-description: 일반 텍스트 및 HTML 모드 살펴보기
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
source-git-commit: 2045c69398902a8e942e20c70287d7f3e9570837

---


# 일반 텍스트 및 HTML 모드 {#plain-text-and-html-modes}

## 이메일의 텍스트 버전 생성 {#generating-a-text-version-of-the-email}

기본적으로 이메일 **[!UICONTROL Plain text]** 버전은 자동으로 생성되어 **[!UICONTROL Edit]** 버전과 동기화됩니다.

HTML 버전에 추가된 개인화 필드 및 컨텐츠 블록도 일반 텍스트 버전과 동기화됩니다.

>[!NOTE]
>
>일반 텍스트 버전에서 컨텐츠 블록을 사용하려면 HTML 코드가 포함되어 있지 않은지 확인하십시오.

HTML 버전과 다른 일반 텍스트 버전을 사용하려면 이메일 보기에서 **[!UICONTROL Sync with HTML]** 스위치를 클릭하여 이 동기화를 비활성화할 수 **[!UICONTROL Plain text]** 있습니다.

![](assets/email_designer_textversion.png)

그런 다음 일반 텍스트 버전을 원하는 대로 편집할 수 있습니다.

>[!NOTE]
>
>동기화가 비활성화되어 있는 동안 **[!UICONTROL Plain text]** 버전을 편집하는 경우 다음 번에 이 **[!UICONTROL Sync with HTML]** 옵션을 활성화하면 일반 텍스트 버전에서 수행한 모든 변경 사항이 HTML 버전으로 대체됩니다. 보기에서 변경한 내용은 **[!UICONTROL Plain text]** 보기에 반영되지 않습니다 **[!UICONTROL HTML]** .

## HTML 파섹 {#editing-an-email-content-source-in-html}

고급 사용자와 디버깅의 경우 HTML에서 직접 이메일 컨텐츠를 보고 편집할 수 있습니다.

이메일의 HTML 버전을 편집하는 방법에는 두 가지가 있습니다.

* &gt; **[!UICONTROL Edit]** 를 **[!UICONTROL HTML]** 선택하여 전체 이메일의 HTML 버전을 엽니다.

   ![](assets/email_designer_html1.png)

* WYSIWYG 인터페이스에서 요소를 선택하고 **[!UICONTROL Source code]** 아이콘을 클릭합니다.

   선택한 요소의 소스만 표시됩니다. 선택한 요소가 **[!UICONTROL HTML]** 컨텐츠 구성 요소인 경우 소스 코드를 편집할 수 있습니다. 다른 구성 요소는 읽기 전용 모드이지만 이메일의 전체 HTML 버전에서 계속 편집할 수 있습니다.

   ![](assets/email_designer_html2.png)

HTML을 수정하면 이메일의 응답성이 끊어집니다. 이 **[!UICONTROL Preview]** 단추를 사용하여 테스트하십시오. 메시지 [미리 보기를](../../sending/using/previewing-messages.md)참조하십시오.
