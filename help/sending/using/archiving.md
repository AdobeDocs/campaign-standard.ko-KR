---
title: Adobe Campaign Standard의 메시지 보관
description: 숨은 참조 이메일 주소를 사용하여 Adobe Campaign Standard으로 이메일을 보관하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 5%

---


# 이메일 숨은 참조를 통해 보관{#archiving-emails}

이메일 BCC를 통해 플랫폼에서 보낸 이메일 복사본을 유지하도록 Adobe Campaign을 구성할 수 있습니다.

특히, 조직에서 모든 아웃바운드 이메일 메시지를 규정 준수를 위해 보관해야 하는 경우 이 기능을 활성화할 수 있습니다. 지정한 숨은 참조 이메일 주소(배달 받는 사람에게 보이지 않음)로 보낸 해당 메시지의 숨겨진 사본을 정확하게 보낼 수 있습니다.

활성화되면 이메일 배달 템플릿의 옵션에서 이메일 숨은 참조 **[!UICONTROL Archive emails]** 를 활성화해야 합니다.

>[!NOTE]
>
>Adobe Campaign 자체는 보관된 파일을 관리하지 않습니다. 따라서 외부 시스템을 사용하여 처리 및 보관할 수 있는 전용 주소로 원하는 메시지를 보낼 수 있습니다.

## Recommendations 및 제한 사항 {#recommendations-and-limitations}

* 이 기능은 선택 사항입니다. 라이선스 계약을 확인하고 계정 관리자에게 문의하여 기능을 활성화하십시오.
* 선택한 BCC 주소는 자신을 위해 구성할 Adobe 팀에 제공해야 합니다.
* 숨은 참조 이메일 주소는 하나만 사용할 수 있습니다.
* 성공적으로 보낸 이메일만 고려됩니다. 바운스 수는 없습니다.
* 개인 정보 보호를 위해 BCC 이메일은 PII(개인 식별 정보)를 안전하게 저장할 수 있는 보관 시스템에서 처리해야 합니다.
* 새 배달 템플릿을 만들 때 옵션을 구입했더라도 기본적으로 이메일 숨은 참조 기능이 활성화되지 않습니다. 사용할 각 배달 템플릿에서 수동으로 활성화해야 합니다.

>[!NOTE]
>
>현재 고급 MTA로 업그레이드된 경우에도 보관된 이메일을 Adobe Campaign 고급 MTA로 보낼 수 없습니다.

## 이메일 보관 활성화 {#activating-email-archiving}

활성화된 이메일 BCC는 전용 옵션을 통해 [이메일 템플릿에서](../../start/using/marketing-activity-templates.md)활성화됩니다.

1. 리소스 **> 템플릿** **** > **배달 템플릿으로**&#x200B;이동합니다.
1. 기본 템플릿을 **[!UICONTROL Send via email]** 복제합니다.
1. 중복된 템플릿을 선택합니다.
1. Click the **[!UICONTROL Edit properties]** button to edit the template&#39;s properties.
1. 섹션을 **[!UICONTROL Send]** 확장합니다.
1. 이 템플릿을 기준으로 각 배달에 대해 보낸 모든 메시지 사본을 보관하려면 이 **[!UICONTROL Archive emails]** 상자를 선택합니다.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>BCC 주소로 보낸 이메일을 열고 클릭하는 경우 전송 분석에서 **[!UICONTROL Total opens]** 및 **[!UICONTROL Clicks]** 에서 계산되지 않을 수 있습니다.