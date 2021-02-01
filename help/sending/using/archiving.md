---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard에서 메시지 보관
description: 숨은 참조 이메일 주소를 사용하여 Adobe Campaign Standard으로 이메일을 보관하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
translation-type: tm+mt
source-git-commit: 0f057375e5cd63605af460f08cd39bed00435184
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 5%

---


# 이메일 숨은 참조를 통해 보관{#archiving-emails}

이메일 BCC를 통해 플랫폼에서 보낸 이메일 복사본을 유지하도록 Adobe Campaign을 구성할 수 있습니다.

특히, 조직에서 규정을 준수하기 위해 모든 아웃바운드 이메일 메시지를 보관해야 하는 경우 이 기능을 활성화할 수 있습니다. 이 도구를 사용하면 지정해야 하는 숨은 참조 이메일 주소(배달 받는 사람에게 보이지 않음)로 보낸 해당 메시지의 숨겨진 복사본을 정확히 보낼 수 있습니다.

활성화되면 이메일 배달 템플릿의 **[!UICONTROL Archive emails]** 옵션에서 이메일 BCC를 활성화해야 합니다.

>[!NOTE]
>
>Adobe Campaign 자체에서는 보관된 파일을 관리하지 않습니다. 외부 시스템을 사용하여 처리하고 보관할 수 있는 전용 주소로 원하는 메시지를 보낼 수 있습니다.

## Recommendations 및 제한 사항 {#recommendations-and-limitations}

* 이 기능은 선택 사항입니다. 라이선스 계약을 확인하고 계정 관리자에게 문의하여 기능을 활성화하십시오.
* 선택한 BCC 주소는 해당 주소를 구성할 Adobe 팀에 제공해야 합니다.
* 숨은 참조 이메일 주소는 하나만 사용할 수 있습니다.
* 전송된 이메일만 고려됩니다. 바운스 수가 없습니다.
* 개인 정보를 보호하기 위해 BCC 이메일은 안전한 개인 식별 정보(PII)를 저장할 수 있는 보관 시스템에 의해 처리되어야 합니다.
* 새 배달 템플릿을 만들 때 옵션을 구입했더라도 이메일 숨은 참조(Email BCC)는 기본적으로 활성화되지 않습니다. 사용할 각 배달 템플릿에서 수동으로 활성화해야 합니다.

>[!NOTE]
>
>현재 보관된 이메일은 Adobe Campaign Enhanced MTA로 보낼 수 없습니다.

## 전자 메일 보관 {#activating-email-archiving} 활성화

활성화된 이메일 BCC는 전용 옵션을 통해 [이메일 템플릿](../../start/using/marketing-activity-templates.md)에서 활성화됩니다.

1. **리소스** > **템플릿** > **배달 템플릿**&#x200B;으로 이동합니다.
1. 기본 **[!UICONTROL Send via email]** 템플릿을 복제합니다.
1. 복제된 템플릿을 선택합니다.
1. **[!UICONTROL Edit properties]** 단추를 클릭하여 템플릿의 속성을 편집합니다.
1. **[!UICONTROL Send]** 섹션을 확장합니다.
1. 이 템플릿을 기준으로 각 배달에 대해 보낸 모든 메시지의 복사본을 보관하려면 **[!UICONTROL Archive emails]** 상자를 선택합니다.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>BCC 주소로 보낸 이메일을 열고 클릭하는 경우, 전송 분석의 **[!UICONTROL Total opens]** 및 **[!UICONTROL Clicks]**&#x200B;에 있는 사항을 고려하여 일부 계산 오류가 발생할 수 있습니다.