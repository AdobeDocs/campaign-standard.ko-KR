---
solution: Campaign Standard
product: campaign
title: Adobe Experience Manager에서 이메일 콘텐츠 만들기.
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 콘텐츠를 제작하고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---


# Adobe Experience Manager 컨텐츠를 Adobe Campaign 이메일로 가져오기 {#creating-email-aem}

이 문서를 사용하면 Adobe Experience Manager에서 이메일 컨텐츠를 만들고 관리하는 방법을 학습하고 마케팅 캠페인에 사용할 수 있도록 이메일을 Adobe Campaign Standard으로 가져옵니다.

전제 조건은 다음과 같습니다.

* 통합을 위해 구성된 AEM 인스턴스에 액세스합니다.
* 통합에 대해 구성된 Adobe Campaign 인스턴스에 액세스합니다.
* AEM 컨텐츠를 수신하도록 구성된 Adobe Campaign 이메일 템플릿입니다.

## Adobe Experience Manager에서 이메일 액세스 {#email-content-aem}

Adobe Experience Manager 작성 인스턴스에 로그인하고 사이트를 탐색하여 이메일 콘텐츠가 포함된 폴더에 액세스합니다.

>[!VIDEO](https://video.tv.adobe.com/v/29996)

## Creating new email content in Adobe Experience Manager {#creating-email-content-aem}

Adobe Campaign 전용 템플릿 몇 개를 사용할 수 있습니다. 이 템플릿에는 Adobe Campaign에서 지원하는 사전 정의된 구성 요소가 포함되어 있으므로 이러한 템플릿 중 하나를 사용해야 합니다.

기본적으로 사전 정의된 두 개의 템플릿을 사용하여 Adobe Campaign용 이메일 컨텐츠를 만들 수 있습니다.

* **[!UICONTROL Adobe Campaign Email]**:이 템플릿에는 개인화할 수 있는 표준 컨텐츠가 포함되어 있습니다. Adobe Campaign 이메일(AC6.1)과 Adobe Campaign 이메일(ACS) 중에서 선택할 수 있습니다.
* **[!UICONTROL Importer Page]**:이 템플릿을 사용하면 개인화할 수 있는 컨텐츠가 포함된 HTML 파일이 포함된 ZIP 파일을 가져올 수 있습니다.

1. Adobe Experience Manager에서 새 컨텐츠를 만듭니다 **[!UICONTROL Page]**.

1. 템플릿을 **[!UICONTROL Adobe Campaign Email]** 선택합니다. 자세한 내용은 다음 비디오를 참조하십시오.
   >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. 새 이메일 컨텐츠를 엽니다.

1. 에서 **[!UICONTROL Page properties]**&#x200B;로 **[!UICONTROL Adobe Campaign]** 설정합니다 **[!UICONTROL Cloud Service Configuration]**. 이렇게 하면 컨텐츠와 Adobe Campaign 인스턴스 간에 통신이 가능합니다.

   자세한 내용은 다음 비디오를 참조하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/29999)

## 이메일 편집 및 보내기 {#editing-email-aem}

구성 요소 및 자산을 추가하여 이메일 컨텐츠를 편집할 수 있습니다. 개인화 필드는 Adobe Campaign에서 수신자의 데이터를 기반으로 보다 관련성 높은 메시지를 전달하는 데 사용할 수 있습니다.

Adobe Experience Manager에서 이메일 컨텐츠를 만들려면

1. 사이드 킥의 **[!UICONTROL Plain text]** > **[!UICONTROL Page properties]** 탭에 액세스하여 제목뿐만 아니라 이메일 **[!UICONTROL Email]** 버전을 편집합니다.

1. 구성 요소 **[!UICONTROL Personalization fields]** 를 **[!UICONTROL Text & Personalization]** 통해 추가합니다. 각 구성 요소는 특정 사용에 해당합니다.이미지 삽입, 개인화 추가 등

   자세한 내용은 다음 비디오를 참조하십시오.
   >[!VIDEO](https://video.tv.adobe.com/v/29998)

1. 탭에서 **[!UICONTROL Workflow]** 유효성 검사 **[!UICONTROL Approve for Adobe Campaign]** 워크플로우를 선택합니다. 승인되지 않은 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

1. 컨텐츠 및 전송 매개 변수가 정의되면 Adobe Campaign Standard에서 이메일을 승인, 준비 및 전송할 수 있습니다.

   자세한 내용은 다음 비디오를 참조하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/23721)
