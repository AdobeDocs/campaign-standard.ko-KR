---
title: URL에서 콘텐트 가져오기
seo-title: URL에서 콘텐트 가져오기
description: URL에서 콘텐트 가져오기
seo-description: 이메일을 만들 때 기존 URL에서 컨텐츠를 로드하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 7 Db 6 C 20 F -7004-4 FB 8-Add 9-362 EAB 3 D 2795
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 로딩 내용
discoiquuid: 738 B 7 C 8 A -88 EB -491 C-A 4 D 0-078 B 0959 B 973
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Importing content from a URL{#importing-content-from-a-url}

URL에서 컨텐츠를 가져오기 전에 아래 요구 사항을 따라야 합니다.

* 이 URL를 통해 컨텐츠를 공개적으로 사용할 수 있어야 합니다.
* For security reasons, only URLs beginning with **[!UICONTROL https]** are allowed.
* 모든 리소스 (이미지, CSS) 가 절대 링크와 HTTPS로 설정되어 있는지 확인합니다. 그렇지 않으면, 이메일을 보낸 후 미러 페이지가 리소스 없이 표시됩니다. 다음은 절대 링크 정의의 예입니다.

   ```
   <a href="https://www.mywebsite.com/images/myimage.png">
   ```

>[!NOTE]
>
>URL에서 컨텐츠를 로드하는 기능은 이메일 채널에서만 사용할 수 있습니다.

기존 콘텐트를 URL로 검색하려면 아래 단계를 따르십시오.

1. From the Email Designer home page, select the **[!UICONTROL Import from URL]** button.

   ![](assets/email_designer_importfromurl.png)

1. 컨텐츠를 검색할 URL를 정의합니다.
1. **[!UICONTROL Confirm]**&#x200B;을 클릭합니다.

**관련 항목:**

[URL](https://helpx.adobe.com/campaign/kt/acs/using/acs-email-designer-tutorial.html#Workingwithexistingcontent) 비디오에서 콘텐트 가져오기

## Retrieving content from a URL automatically at preparation time {#retrieving-content-from-a-url-automatically-at-preparation-time}

메시지 준비 중에 URL에서 콘텐트를 가져오면 이메일을 준비할 때마다 최신 HTML 콘텐츠를 가져올 수 있습니다. 이렇게 하면 반복되는 이메일의 컨텐츠가 항상 전송 시점에 최신 상태로 유지됩니다. 또한 이 기능을 사용하면 컨텐츠가 아직 준비되지 않았더라도 특정 날짜에 예약된 메시지를 만들 수 있습니다.

준비 시간에 컨텐츠를 검색하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Content imported during preparation]** 옵션을 선택합니다.

   ![](assets/email_designer_importfromurl2.png)

1. URL 컨텐츠는 편집기에 읽기 전용으로 표시됩니다.

   >[!CAUTION]
   >
   >이 단계에서는 컨텐츠 편집기의 HTML 표시를 고려해서는 안 됩니다. 준비 단계에서 검색됩니다.

1. To preview the URL content that has been retrieved, open the message once it is created then click the **[!UICONTROL Preview]** button.

컨텐츠가 검색되는 원격 URL를 개인화할 수 있습니다. 이렇게 하려면 아래 단계를 따르십시오.

1. Click the email label on top of the screen to acces the Email Designer **[!UICONTROL Properties]** tab.
1. **[!UICONTROL Remote URL]** 필드를 찾습니다.

   ![](assets/email_designer_importfromurl4.png)

1. 원하는 개인화 필드, 컨텐츠 블록 또는 동적 텍스트를 삽입합니다.

   The **[!UICONTROL Current date - YYYYMMDD]** content block, for example, enables you to insert the date of the day.

   >[!NOTE]
   >
   >The available personalization fields are linked to **Delivery** attributes only (email creation date, status, campaign label...).

