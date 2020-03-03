---
title: Adobe Experience Manager에서 이메일 콘텐츠 만들기.
description: Adobe Experience Manager 통합을 통해 AEM에서 바로 컨텐츠를 제작하고 나중에 Adobe Campaign에서 사용할 수 있습니다.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9efce905cd767013a22afb2a4d642e42b6616ef1

---


# Adobe Experience Manager 콘텐츠를 Adobe Campaign 이메일로 가져오기 {#creating-email-aem}

이 문서를 사용하면 Adobe Experience Manager에서 이메일 컨텐츠를 만들고 관리하는 방법을 배웁니다. 그런 다음 Adobe Campaign Standard로 이메일을 가져와 마케팅 캠페인에 사용합니다.

사전 요구 사항은 다음과 같습니다.

* 통합을 위해 구성된 AEM 인스턴스에 대한 액세스
* 통합을 위해 구성된 Adobe Campaign 인스턴스에 액세스합니다.
* AEM 컨텐츠를 수신하도록 구성된 Adobe Campaign 이메일 템플릿입니다.

## Adobe Experience Manager에서 이메일 액세스 {#email-content-aem}

Adobe Experience Manager 제작 인스턴스에 로그인하고 사이트를 탐색하여 이메일 콘텐츠가 포함된 폴더에 액세스합니다.

>[!VIDEO](https://images-tv.adobe.com/mpcv3/2674d459-d57b-413b-9d34-9fd941666023_1575035768.854x480at800_h264.mp4)

## Creating new email content in Adobe Experience Manager {#creating-email-content-aem}

Adobe Campaign과 관련된 몇 가지 템플릿을 사용할 수 있습니다. Adobe Campaign에서 지원하는 사전 정의된 구성 요소가 포함되어 있으므로 이러한 템플릿 중 하나를 사용해야 합니다.

기본적으로 사전 정의된 두 개의 템플릿을 사용하여 Adobe Campaign의 이메일 컨텐츠를 만들 수 있습니다.

* **[!UICONTROL Adobe Campaign Email]**:이 템플릿에는 개인화할 수 있는 표준 컨텐츠가 포함되어 있습니다. Adobe Campaign 이메일(AC6.1)과 Adobe Campaign 이메일(ACS) 중에서 선택할 수 있습니다.
* **[!UICONTROL Importer Page]**:이 템플릿을 사용하면 개인화할 수 있는 컨텐츠가 포함된 HTML 파일을 압축 파일로 가져올 수 있습니다.

1. Adobe Experience Manager에서 새 항목을 만듭니다 **[!UICONTROL Page]**.

1. 템플릿을 **[!UICONTROL Adobe Campaign Email]** 선택합니다. 자세한 내용은 다음 비디오를 참조하십시오.
   >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. 새 이메일 컨텐츠를 엽니다.

1. 에서 **[!UICONTROL Page properties]**&#x200B;로 **[!UICONTROL Adobe Campaign]** 설정합니다 **[!UICONTROL Cloud Service Configuration]**. 이렇게 하면 콘텐츠와 Adobe Campaign 인스턴스 간의 통신이 가능합니다.

   자세한 내용은 다음 비디오를 참조하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/29999)

## 이메일 편집 및 보내기 {#editing-email-aem}

구성 요소와 자산을 추가하여 이메일 컨텐츠를 편집할 수 있습니다. 개인화 필드는 Adobe Campaign에서 수신자의 데이터를 기반으로 보다 연관성 높은 메시지를 전달하는 데 사용할 수 있습니다.

Adobe Experience Manager에서 이메일 컨텐츠를 만들려면

1. 사이드 킥의 **[!UICONTROL Plain text]** > **[!UICONTROL Page properties]** 탭에 액세스하여 제목뿐만 아니라 이메일 **[!UICONTROL Email]** 버전을 편집합니다.

1. 구성 **[!UICONTROL Personalization fields]** 요소를 통해 **[!UICONTROL Text & Personalization]** 추가합니다. 각 구성 요소는 특정 사용에 해당합니다.이미지 삽입, 개인화 추가 등

   자세한 내용은 다음 비디오를 참조하십시오.
   >[!VIDEO](https://video.tv.adobe.com/v/29998)

1. 탭에서 **[!UICONTROL Workflow]** **[!UICONTROL Approve for Adobe Campaign]** 유효성 검사 워크플로우를 선택합니다. 승인되지 않은 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

1. 컨텐츠 및 전송 매개 변수가 정의되면 Adobe Campaign Standard에서 이메일을 승인, 준비 및 전송할 수 있습니다.

   자세한 내용은 다음 비디오를 참조하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/23721)
