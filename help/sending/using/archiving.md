---
title: Adobe Campaign Standard에서 메시지 보관
description: BCC 이메일 주소를 사용하여 Adobe Campaign Standard으로 이메일을 보관하는 방법에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
feature: Performance Monitoring
role: User
level: Intermediate
exl-id: 7bf380d7-195e-413d-b14e-85e78b07ba8b
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 5%

---

# 이메일 숨은 참조를 통해 보관{#archiving-emails}

이메일 BCC를 통해 플랫폼에서 전송된 이메일 사본을 유지하도록 Adobe Campaign을 구성할 수 있습니다.

특히 규정 준수를 위해 모든 아웃바운드 이메일 메시지를 보관해야 하는 경우 이 기능을 활성화할 수 있습니다. 이를 통해 사용자가 지정해야 하는 BCC 이메일 주소(게재 수신자에게는 보이지 않음)로 보낸 해당 메시지의 정확한 숨겨진 사본을 보낼 수 있습니다.

사용하도록 설정하면 전자 메일 게재 템플릿의 **[!UICONTROL Archive emails]** 옵션에서 전자 메일 BCC를 활성화해야 합니다.

>[!NOTE]
>
>Adobe Campaign 자체는 보관된 파일을 관리하지 않습니다. 원하는 메시지를 외부 시스템을 사용하여 처리하고 보관할 수 있는 전용 주소로 전송할 수 있습니다.

## Recommendations 및 제한 사항 {#recommendations-and-limitations}

* 이 기능은 선택 사항입니다. 라이선스 계약을 확인하고 계정 관리자에게 문의하여 기능을 활성화하십시오.
* 선택한 BCC 주소를 구성할 Adobe 팀에 제공해야 합니다.
* 숨은 참조 이메일 주소는 하나만 사용할 수 있습니다.
* 성공적으로 전송된 이메일만 고려됩니다. 바운스 수는 없습니다.
* 개인정보 보호를 위해 BCC 이메일은 PII(개인 식별 정보)를 안전하게 저장할 수 있는 보관 시스템에 의해 처리되어야 합니다.
* 새 게재 템플릿을 만들 때 옵션을 구입한 경우에도 이메일 BCC는 기본적으로 활성화되지 않습니다. 사용할 각 게재 템플릿에서 수동으로 활성화해야 합니다.

>[!NOTE]
>
>현재 보관된 이메일은 단순 SMTP 릴레이를 사용하는 기존 보관 모듈에 의해 계속 전송됩니다.

## 전자 메일 보관 활성화 중 {#activating-email-archiving}

활성화하면 전용 옵션을 통해 [이메일 템플릿](../../start/using/marketing-activity-templates.md)에서 이메일 BCC가 활성화됩니다.

1. **리소스** > **템플릿** > **게재 템플릿**(으)로 이동합니다.
1. 기본 제공 **[!UICONTROL Send via email]** 템플릿을 복제합니다.
1. 복제된 템플릿을 선택합니다.
1. 템플릿의 속성을 편집하려면 **[!UICONTROL Edit properties]** 단추를 클릭하십시오.
1. **[!UICONTROL Send]** 섹션을 확장합니다.
1. 이 템플릿을 기반으로 각 게재의 보낸 모든 메시지 복사본을 유지하려면 **[!UICONTROL Archive emails]** 상자를 선택하세요.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>BCC 주소로 전송된 전자 메일을 열고 클릭스루하는 경우 전송 분석의 **[!UICONTROL Total opens]** 및 **[!UICONTROL Clicks]**&#x200B;에서 이 값이 고려되며, 이로 인해 일부 계산 착오가 발생할 수 있습니다.
