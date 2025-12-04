---
title: Audience Manager 또는 People 핵심 서비스와 대상자 공유
description: 다양한 Adobe Experience Cloud 솔루션 내에서 대상을 가져오거나 내보내는 방법에 대해 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: People Core Service Integration
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: b0d063de-863c-42e7-98dd-c4c86da3281e
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 3%

---

# Audience Manager 또는 People 핵심 서비스와 대상자 공유{#sharing-audiences-with-audience-manager-or-people-core-service}

## 대상자 가져오기 {#importing-an-audience}

People 핵심 서비스 통합을 사용하면 기술 워크플로우를 통해 대상자를 Adobe Campaign으로 직접 가져와 데이터베이스를 보강할 수 있습니다. People 핵심 서비스의 대상 공유에 대한 자세한 내용은 이 [설명서](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=ko)를 참조하세요.

Adobe Campaign의 People 핵심 서비스에서 대상/세그먼트를 가져오는 작업은 IMS(Adobe ID을 통한 인증)를 통해 연결된 사용자만 **[!UICONTROL Audiences]** 메뉴에서 수행할 수 있습니다.

1. **[!UICONTROL Audiences]** 메뉴로 이동합니다.
1. 작업 표시줄에서 화면에 표시할 **[!UICONTROL Create]**&#x200B;을(를) 선택하여 대상자를 만듭니다.
1. 새 대상자의 레이블을 지정합니다.
1. 만들 대상이 People 핵심 서비스에서 가져온 대상임을 나타내려면 대상 **[!UICONTROL Type]**&#x200B;을(를) **[!UICONTROL Experience Cloud]**(으)로 설정하십시오.
1. **[!UICONTROL Name of the shared audience]** 필드에서 가져올 대상을 선택합니다. 세그먼트만 가져올 수 있습니다. 키-값 쌍, 트레이트 및 규칙을 포함한 세분화된 데이터는 지원되지 않습니다.

   ![](assets/aam_import_audience.png)

1. 해당 **[!UICONTROL Shared Data Source]**&#x200B;을(를) 선택하십시오.

   선택한 데이터 원본이 암호화 알고리즘을 사용하도록 구성된 경우 추가 옵션을 사용하면 **[!UICONTROL Force reconciliation with a profile]**&#x200B;할 수 있습니다. 데이터 원본의 **[!UICONTROL Channel]** 필드가 전자 메일 또는 모바일(SMS)으로 설정되어 있고 프로필 데이터를 활용하려면 이 옵션을 선택하십시오.

   **[!UICONTROL Force reconciliation with a profile]**&#x200B;을(를) 선택하지 않고 **[!UICONTROL Channel]**&#x200B;이(가) AMC 데이터 원본에서 전자 메일 또는 모바일(SMS)로 설정된 경우 암호화된 선언된 모든 ID의 암호가 해독됩니다. 모든 전자 메일 주소/휴대폰 번호 목록이 있는 **파일** 유형의 대상자가 만들어지거나 업데이트되었습니다. 이렇게 하면 이 통합을 통해 공유 대상을 가져오는 동안 해당 프로필이 Campaign에 없는 경우에도 이메일 주소/휴대폰 번호를 손실하지 않습니다. 워크플로우를 사용하여 수동으로 조정해야 하므로 이 유형의 대상자는 직접 사용할 수 없습니다.

1. 대상을 만들려면 을(를) 확인합니다.

   그러면 기술 워크플로우를 통해 대상자를 가져옵니다. 이 ID(&#39;방문자 ID&#39; 또는 &#39;선언된 ID&#39;)를 프로필 차원과 조정할 수 있는 레코드로 구성됩니다. Adobe Campaign에서 인식하지 못하는 사람 핵심 서비스 세그먼트의 ID는 가져오지 않습니다.

이제 대상을 Adobe Campaign 데이터베이스로 가져옵니다. People 핵심 서비스 또는 Audience Manager에서 직접 세그먼트를 가져오는 경우 가져오기 프로세스를 동기화하는 데 24~36시간이 소요됩니다. 이 기간이 지나면 Adobe Campaign에서 새 대상을 찾아 사용할 수 있습니다.

>[!NOTE]
>
>Adobe Analytics에서 Adobe Campaign으로 대상을 가져오는 경우 먼저 이러한 대상을 People Core Service 또는 Audience Manager에서 공유해야 합니다. 이 프로세스는 12~24시간 걸리며, Campaign과의 24~36시간 동기화에 추가해야 합니다. 이 경우 대상 공유 기간은 최대 60시간일 수 있습니다. People 핵심 서비스 및 Audience Manager의 Adobe Analytics 대상 공유에 대한 자세한 내용은 이 [설명서](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=ko)를 참조하십시오.

## 대상자 내보내기 {#exporting-an-audience}

워크플로우와 **[!UICONTROL Save audience]** 활동을 사용하여 대상을 Adobe Campaign에서 Audience Manager 또는 People 핵심 서비스로 내보낼 수 있습니다.

새 워크플로우에서 IMS(Adobe ID을 통한 인증)를 통해 연결된 사용자만 수행할 수 있습니다.

1. 프로그램, 캠페인 또는 마케팅 활동 목록에서 새 워크플로우를 만듭니다.
1. 사용 가능한 여러 활동을 사용하여 프로필 세트를 타깃팅합니다.
1. 타겟팅 후 **[!UICONTROL Save audience]** 활동을 워크플로우로 끌어서 놓은 다음 엽니다.
1. **[!UICONTROL Share in Adobe Experience Cloud]**&#x200B;을(를) 선택합니다.

   ![](assets/aam_save_audience_activity.png)

1. **[!UICONTROL Shared audience]** 필드를 사용하여 대상자를 지정하십시오. 열리는 창에서 기존 대상을 선택하거나 새 대상을 만들 수 있습니다.

   * 기존 대상자를 선택하면 새 레코드만 대상자에 추가됩니다.
   * 프로필 목록을 새 대상자로 내보내려면 **[!UICONTROL Segment name]** 필드를 완료한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭한 후 새로 만든 대상자를 선택하십시오.

   ![](assets/aam_save_audience_segment_picker.png)

   조정하고 교환하려면 레코드에 Adobe Experience Cloud ID(&#39;방문자 ID&#39; 또는 &#39;선언된 ID&#39;)가 있어야 합니다. 조정되지 않은 레코드는 대상자를 가져오거나 내보낼 때 무시됩니다.

1. 마치려면 화면 오른쪽 상단에 있는 확인 표시를 클릭합니다.
1. 해당 **[!UICONTROL Shared Data Source]**&#x200B;을(를) 선택하십시오.
1. 내보내기한 프로필을 사용하려면 **[!UICONTROL Generate an outbound transition]** 상자를 선택합니다. 조정할 수 있는 프로필만 내보냅니다.
1. 활동의 구성을 확인하고 워크플로우를 저장합니다.
1. 워크플로우를 시작하여 대상자를 내보냅니다. Adobe Campaign과 People 핵심 서비스 간 동기화는 몇 시간 정도 소요될 수 있습니다

Adobe Campaign과 People 핵심 서비스 간 동기화는 24-36시간이 소요됩니다. 이 기간이 지나면 People 핵심 서비스에서 새 대상자를 찾아 다른 Adobe Experience Cloud 솔루션에서 다시 사용할 수 있습니다. Adobe People 핵심 서비스에서 Adobe Campaign 공유 대상을 사용하는 방법에 대한 자세한 내용은 이 [설명서](https://experienceleague.adobe.com/docs/core-services/interface/audiences/t-audience-create.html?lang=ko)를 참조하십시오.

**관련 항목:**

* [워크플로](../../automating/using/get-started-workflows.md)
* [대상자](../../audiences/using/about-audiences.md)
