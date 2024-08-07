---
title: 랜딩 페이지 템플릿
description: 랜딩 페이지 템플릿에 대해 자세히 알아봅니다.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
feature: Landing Pages
role: User
level: Intermediate
exl-id: 29d1badf-9ce3-470c-9bdc-169586d2e943
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 94%

---

# 랜딩 페이지 템플릿 기본 정보 {#landing-page-templates}

Campaign에는 다음과 같은 기본 제공 랜딩 페이지 템플릿이 포함되어 있습니다.

* **[!UICONTROL Acquisition]**: 랜딩 페이지의 기본 템플릿으로 Campaign 데이터베이스에서 데이터를 캡처하고 업데이트할 수 있습니다.
* **[!UICONTROL Subscription]**: 이 템플릿은 서비스 구독을 제공하는 데 사용해야 합니다.
* **[!UICONTROL Unsubscription]**: 이 템플릿은 구독자에게 전송된 이메일에서 서비스에 연결될 수 있으며 구독자가 이 서비스의 구독을 취소하도록 허용합니다.
* **[!UICONTROL Denylist]**: 이 템플릿은 Campaign에서 더 이상 프로필에 연락하지 않으려는 경우에 사용해야 합니다. 차단 목록에 추가하다 관리에 대한 자세한 정보는 [Campaign의 옵트인 정보](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)를 참조하세요.

템플릿은 새 랜딩 페이지를 만들 때 기본적으로 제안됩니다.

![](assets/lp_creation_1.png)

랜딩 페이지 템플릿에 액세스하려면 왼쪽 상단의 Adobe Campaign 로고를 클릭하고 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Landing page templates]**&#x200B;을(를) 선택합니다.

>[!NOTE]
>
>기본 제공 템플릿을 복제하여 자신만의 템플릿을 만드는 것이 좋습니다. 일부 매개 변수는 랜딩 페이지 템플릿에서만 설정할 수 있으며 랜딩 페이지에서 직접 수정할 수 없습니다.

템플릿을 작성할 때 태그에 **&#39;type&#39;** 속성을 추가하는 것이 좋습니다. 이 정보는 편집기에서 처리되고 사용자가 웹 애플리케이션을 구성할 때 데이터베이스 필드를 양식 필드에 연결하는 데 도움이 됩니다.

템플릿의 HTML 코드 예제:

```
<input id="email" type="email" name="email"/>
```

&#39;type&#39; 속성의 공식 목록은 다음 주소에서 사용할 수 있습니다. [https://www.w3schools.com/tags/att_input_type.asp](https://www.w3schools.com/tags/att_input_type.asp)
