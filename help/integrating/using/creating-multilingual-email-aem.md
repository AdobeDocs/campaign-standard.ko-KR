---
title: Adobe Experience Manager 통합으로 다국어 이메일 만들기.
description: Adobe Experience Manager 통합을 통해 AEM에서 직접 콘텐츠를 만들고 나중에 Adobe Campaign에서 사용할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 0f66fe2b-22b1-49d7-a080-29b00941a2cc
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 5%

---

# Adobe Experience Manager 통합으로 다국어 이메일 만들기 {#creating-multilingual-email-aem}

이 문서에서는 Adobe Experience Manager 콘텐츠 및 언어 사본을 사용하여 다국어 이메일을 만드는 방법을 알아봅니다.

전제 조건은 다음과 같습니다.

* 통합을 위해 구성된 AEM 인스턴스에 대한 액세스 권한.
* 통합을 위해 구성된 Adobe Campaign 인스턴스에 대한 액세스.
* AEM 콘텐츠를 수신하도록 구성된 Adobe Campaign 다국어 이메일 템플릿입니다.

## Adobe Experience Manager에서 새 이메일 콘텐츠 만들기 {#creating-email-content-aem}

1. Adobe Experience Manager 홈페이지에서 을 선택합니다. **[!UICONTROL Site]**.

   ![](assets/aem_acs_1.png)

1. 페이지를 만들 폴더를 선택하고 **[!UICONTROL Create]** 그러면 **[!UICONTROL Page]**. 여기에서는 기본 언어가 되는 en_us 폴더에 페이지를 만듭니다.

   ![](assets/aem_acs_2.png)

1. 다음 항목 선택 **[!UICONTROL Adobe Campaign Email (ACS)]** 템플릿.

1. 전자 메일 속성을 입력하고 **[!UICONTROL Create]**.

   ![](assets/aem_acs_3.png)

1. 새 이메일 콘텐츠를 열고 필요에 따라 개인화합니다. 자세한 정보는 이 [페이지](../../integrating/using/creating-email-experience-manager.md#editing-email-aem)를 참조하십시오.

   ![](assets/aem_acs_4.png)

1. 다음에서 **[!UICONTROL Workflow]** 탭에서 **[!UICONTROL Approve for Adobe Campaign]** 유효성 검사 워크플로우. 승인되지 않은 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

   ![](assets/aem_acs_7.png)

1. 클릭 **[!UICONTROL Complete]** 그러면 **[!UICONTROL Newsletter review]** 다음에서 **[!UICONTROL Complete work item]** 창.

1. **[!UICONTROL Complete]**&#x200B;을(를) 클릭한 뒤 **[!UICONTROL Newsletter approval]**&#x200B;을(를) 클릭합니다. 콘텐츠 및 전송 매개 변수가 정의되면 Adobe Campaign Standard에서 이메일 승인, 준비 및 전송을 진행할 수 있습니다.

   ![](assets/aem_acs_8.png)

## 언어 사본 만들기 {#creating-language-copies}

이메일 콘텐츠를 디자인한 후에는 이제 변형으로 Adobe Campaign Standard과 동기화할 언어 사본을 만들어야 합니다.

1. 앞에서 만든 페이지를 선택하고 **[!UICONTROL Create]** 그러면 **[!UICONTROL Language Copy]**.

   ![](assets/aem_acs_5.png)

1. 선택한 언어로 번역될 이전에 만든 이메일 콘텐츠를 선택한 다음 을(를) 클릭합니다. **[!UICONTROL Next]**.

   ![](assets/aem_acs_6.png)

1. 다음에서 **[!UICONTROL Target language(s)]** 드롭다운에서 콘텐츠를 번역할 언어를 선택한 다음 **[!UICONTROL Next]**.

   ![](assets/aem_acs_9.png)

1. **[!UICONTROL Create]**&#x200B;를 클릭합니다.

이제 언어 사본이 생성되었으므로 선택한 언어에 따라 콘텐츠를 편집할 수 있습니다.

>[!CAUTION]
>
>모든 언어 사본은 **[!UICONTROL Approve for Adobe Campaign]** 유효성 검사 워크플로우. 승인되지 않은 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

![](assets/aem_acs_11.png)

## Adobe Campaign Standard에서 다국어 콘텐츠 만들기 {#multilingual-acs}

1. Adobe Campaign Standard 홈페이지에서 **[!UICONTROL Create an email]**.

   ![](assets/aem_acs_12.png)

1. Adobe Experience Manager 콘텐츠를 수신하도록 구성된 Adobe Campaign 다국어 이메일 템플릿을 선택합니다. Adobe Experience Manager 인스턴스에 연결된 템플릿을 만드는 방법에 대한 자세한 내용은 다음을 참조하십시오. [페이지](../../integrating/using/configure-experience-manager.md#config-acs).

   >[!NOTE]
   >
   >이 경우 기본 제공 템플릿을 복제해야 합니다 **[!UICONTROL Multilingual email (mailMultiLang)]** 다국어 이메일을 보낼 수 있습니다.

   ![](assets/aem_acs_13.png)

1. 다음을 입력합니다. **[!UICONTROL Properties]** 및 **[!UICONTROL Audience]** 이메일 및 클릭 **[!UICONTROL Create]**.

1. 다음에서 **[!UICONTROL Edit properties]**&#x200B;에서 Adobe Experience Manager 계정이 올바르게 설정되었는지 확인합니다. **[!UICONTROL Content]** 드롭다운.

   ![](assets/aem_acs_20.png)

1. **[!UICONTROL Language copy creation]**&#x200B;를 클릭합니다.

   ![](assets/aem_acs_16.png)

1. 이전에 만든 Adobe Experience Manager 콘텐츠를 선택하고 **[!UICONTROL Confirm]**. 여기에 표시된 Adobe Experience Manager 콘텐츠는 유효성이 확인된 콘텐츠만 해당되며 콘텐츠에서 필터링될 수 있습니다 **[!UICONTROL Label]** 및 **[!UICONTROL Path]**.

   >[!NOTE]
   >
   >선택한 언어 사본은 기본값으로 설정되며 나중에 **[!UICONTROL Content variant]** 차단합니다.

   ![](assets/aem_acs_17.png)

1. 클릭 **[!UICONTROL Create variants]** 을 클릭하여 다국어 콘텐츠를 연결합니다. 그러면 Adobe Campaign Standard에서 다른 언어 사본을 이 콘텐츠에 자동으로 연결합니다. 생성된 변형의 레이블 및 코드 언어는 Adobe Experience Manager에서 선택한 변형과 동일합니다.

   ![](assets/aem_acs_18.png)

1. 다음을 클릭합니다. **[!UICONTROL Content variant]** 필요한 경우 기본 변형을 변경하려면 차단을 클릭하고 **[!UICONTROL Confirm]**.

   ![](assets/aem_acs_19.png)

1. 콘텐츠 또는 변형이 Adobe Experience Manager에서 업데이트된 경우 Adobe Campaign Standard에서 이를 **[!UICONTROL Refresh AEM contents]** 단추를 클릭합니다.

1. 이제 이메일을 보낼 준비가 되었습니다. 자세한 내용은 다음을 참조하십시오. [페이지](../../sending/using/get-started-sending-messages.md).

   >[!NOTE]
   >
   >승인되지 않은 AEM 콘텐츠를 사용하는 경우 Adobe Campaign에서 이메일을 보낼 수 없습니다.

대상자는 다음에 따라 이메일을 받게 됩니다. **[!UICONTROL Preferred languages]** 설정 **[!UICONTROL Profiles]**. 프로필 및 기본 언어를 편집하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [페이지](../../audiences/using/editing-profiles.md).
