---
title: Adobe Experience Manager에서 이메일 콘텐츠 만들기.
description: Adobe Experience Manager 통합을 통해 AEM에서 직접 콘텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 72b99864-d9d9-4cf4-be06-dc5719a2e4f2
source-git-commit: 579404ddc128e25cc7f8f93dfec30663c7cf754e
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 2%

---

# Adobe Experience Manager 콘텐츠를 Adobe Campaign 이메일로 가져오기 {#creating-email-aem}

이 문서를 사용하면 Adobe Experience Manager에서 이메일 콘텐츠를 만들고 관리한 다음 이메일에서 Adobe Campaign Standard으로 가져와서 마케팅 캠페인에 사용하는 방법을 배웁니다.

전제 조건은 다음과 같습니다.

* 통합을 위해 구성된 AEM 인스턴스에 대한 액세스 권한.
* 통합을 위해 구성된 Adobe Campaign 인스턴스에 대한 액세스.
* AEM 콘텐츠를 수신하도록 구성된 Adobe Campaign 이메일 템플릿.

## Adobe Experience Manager에서 이메일 액세스 {#email-content-aem}

Adobe Experience Manager 제작 인스턴스에 로그인하고 사이트를 탐색하여 이메일 콘텐츠가 포함된 폴더에 액세스합니다.

>[!VIDEO](https://video.tv.adobe.com/v/29996)

## Adobe Experience Manager에서 새 이메일 콘텐츠 만들기 {#creating-email-content-aem}

Adobe Campaign과 관련된 몇 가지 템플릿을 사용할 수 있습니다. Adobe Campaign에서 지원하는 사전 정의된 구성 요소가 포함되어 있으므로 이러한 템플릿 중 하나를 사용해야 합니다.

기본적으로 사전 정의된 두 개의 템플릿을 사용하여 Adobe Campaign용 이메일 콘텐츠를 만들 수 있습니다.

* **[!UICONTROL Adobe Campaign Email]**: 이 템플릿에는 개인화할 수 있는 표준 콘텐츠가 포함되어 있습니다. Adobe Campaign 이메일(AC6.1)과 Adobe Campaign 이메일(ACS) 중에서 선택할 수 있습니다.
* **[!UICONTROL Importer Page]**: 이 템플릿을 사용하면 HTML 파일이 포함된 ZIP 파일을 개인화할 수 있는 콘텐츠와 함께 가져올 수 있습니다.

1. Adobe Experience Manager에서 새로 만들기 **[!UICONTROL Page]**.

1. 다음 항목 선택 **[!UICONTROL Adobe Campaign Email]** 템플릿. 자세한 단계는 다음 비디오를 참조하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/29997)

1. 새 이메일 콘텐츠를 엽니다.

1. 다음에서 **[!UICONTROL Page properties]**, 설정됨 **[!UICONTROL Adobe Campaign]** (으)로 **[!UICONTROL Cloud Service Configuration]**. 이를 통해 콘텐츠와 Adobe Campaign 인스턴스 간에 통신할 수 있습니다.

   자세한 내용은 다음 비디오를 시청하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/29999)

## 이메일 편집 및 보내기 {#editing-email-aem}

구성 요소 및 에셋을 추가하여 이메일 콘텐츠를 편집할 수 있습니다. 개인화 필드를 사용하여 Adobe Campaign의 수신자 데이터를 기반으로 더 연관성 높은 메시지를 전달할 수 있습니다.

Adobe Experience Manager에서 이메일 콘텐츠를 만들려면 다음 작업을 수행하십시오.

1. 제목과 을 편집합니다. **[!UICONTROL Plain text]** 에 액세스하여 이메일 버전 **[!UICONTROL Page properties]** > **[!UICONTROL Email]** 사이드 킥의 탭입니다.

1. 추가 **[!UICONTROL Personalization fields]** 다음을 통해 **[!UICONTROL Text & Personalization]** 구성 요소. 각 구성 요소는 이미지 삽입, 개인화 추가 등의 특정 용도에 해당합니다.

   자세한 내용은 다음 비디오를 시청하십시오.

   >[!VIDEO](https://video.tv.adobe.com/v/29998)

1. 다음에서 **[!UICONTROL Workflow]** 탭에서 **[!UICONTROL Approve for Adobe Campaign]** 유효성 검사 워크플로우. 승인되지 않은 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

Adobe Campaign Standard에서 이메일을 보내려면

1. 콘텐츠 및 전송 매개 변수가 정의되면 Adobe Campaign Standard에서 AEM 관련 이메일 템플릿을 기반으로 이메일을 만듭니다.

+++ AEM 관련 템플릿에 대해 자세히 알아보십시오.

   1. 고급 메뉴에서 **[!UICONTROL Resources]** `>` **[!UICONTROL Templates]** `>` **[!UICONTROL Delivery templates]**.

      ![](assets/aem_templates_1.png)

   1. 게재 템플릿 중 하나를 복제하거나 선택합니다.

   1. 다음에서 **[!UICONTROL Properties]** 템플릿의 **[!UICONTROL Content]** 드롭다운, 선택 **[!UICONTROL Adobe Experience Manager as Content mode]** 그런 다음 Adobe Experience Manager 계정을 만듭니다.

      ![](assets/aem_templates_2.png)

+++

   ![](assets/aem_send_1.png)

1. 전자 메일 속성을 입력하고 **[!UICONTROL Create]** AEM 컨텐츠를 선택할 수 있습니다.

1. 액세스 **[!UICONTROL Content]** 차단합니다.

   ![](assets/aem_send_2.png)

1. 다음에서 **[!UICONTROL Use Adobe Experience Manager content]** 메뉴, 클릭 **[!UICONTROL Link AEM content]**.

   그런 다음 이메일에 사용할 콘텐츠를 선택합니다.

   ![](assets/aem_send_3.png)

1. 대시보드를 통해 대상 대상 및 실행 일정과 같은 추가 매개 변수를 지정하여 이메일을 추가로 사용자 지정합니다. 구성하고 나면 이제 이메일 게재를 보낼 수 있습니다. [자세히 알아보기](../../sending/using/confirming-the-send.md)

