---
title: 랜딩 페이지 템플릿
description: 랜딩 페이지 템플릿에 대해 자세히 알아보십시오.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 012546e109b085b7ed968bcefa8f76482656ae0d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# 랜딩 페이지 템플릿 기본 정보 {#landing-page-templates}

Campaign에는 다음과 같은 내장 랜딩 페이지 템플릿이 포함되어 있습니다.

* **[!UICONTROL Acquisition]**: 이것은 Campaign 데이터베이스에서 데이터를 캡처하고 업데이트할 수 있는 랜딩 페이지의 기본 템플릿입니다.
* **[!UICONTROL Subscription]**: 이 템플릿은 서비스에 대한 구독을 제공하는 데 사용해야 합니다.
* **[!UICONTROL Unsubscription]**: 이 템플릿은 가입자에게 서비스 구독을 취소할 수 있도록 하는 이메일에서 연결할 수 있습니다.
* **[!UICONTROL Block list]**: 이 템플릿은 더 이상 Campaign에서 프로필로 연결하지 않을 때 사용해야 합니다. 차단 목록 관리에 대한 자세한 내용은 캠페인 [에서 옵트인 및 옵트아웃 정보를 참조하십시오](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

이러한 템플릿은 새 랜딩 페이지를 만들 때 기본적으로 제안됩니다.

![](assets/lp_creation_1.png)

랜딩 페이지 템플릿에 액세스하려면 왼쪽 위 모서리에 있는 Adobe Campaign 로고를 클릭하고 **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Landing page templates]**&#x200B;를 선택합니다.

>[!NOTE]
>
>내장된 템플릿을 복제하여 고유한 템플릿을 만드는 것이 좋습니다. 일부 매개 변수는 랜딩 페이지 템플릿에서만 설정할 수 있으며 랜딩 페이지에서 직접 수정할 수 없습니다.

템플릿을 작성할 때는 태그에 **&#39;type&#39;** 속성을 추가하는 것이 좋습니다. 이 정보는 편집자가 처리하고 웹 응용 프로그램을 구성할 때 데이터베이스 필드를 양식 필드에 연결하는 데 도움이 됩니다.

템플릿의 HTML 코드 예:

```
<input id="email" type="email" name="email"/>
```

&#39;type&#39; 속성의 공식 목록은 다음 주소로 사용할 수 있습니다. [https://www.w3schools.com/tags/att_input_type.asp](https://www.w3schools.com/tags/att_input_type.asp)