---
solution: Campaign Standard
product: campaign
title: 전자 메일 렌더링
description: 전자 메일 렌더링 기능을 살펴보십시오.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 85%

---


# 전자 메일 렌더링{#email-rendering}

**[!UICONTROL Send]** 버튼을 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 디바이스에서 최적의 방식으로 표시되는지 확인하십시오.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 수신되었을 수 있는 다른 컨텍스트에서 전송된 메시지를 미리 볼 수 있습니다.

Adobe Campaign에서 **전자 메일 렌더링을** 위해 사용할 수 있는 모바일, 메시징 및 웹 메일 클라이언트는 Litmus [웹 사이트](https://litmus.com/email-testing) (**모든 이메일 클라이언트 보기** 클릭)에 나열되어 있습니다.

## 전자 메일 렌더링 보고서 확인 {#checking-the-email-rendering-report}

전자 메일 게재를 만들고 타겟팅된 모집단과 해당 컨텐츠까지 정의했으면 아래 단계를 따르십시오.

1. **대상자**&#x200B;를 클릭하여 **[!UICONTROL Test profiles]** 탭에 액세스합니다.

   ![](assets/email_rendering_05.png)

1. 쿼리 편집기를 사용하여 **전자 메일 렌더링**&#x200B;을 위한 테스트 프로필과 같은 사용할 테스트 프로필을 정의합니다. [테스트 프로필 정보](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

   ![](assets/email_rendering_06.png)

1. 쿼리를 선택하고 확인한 다음 변경 내용을 저장합니다.
1. 작업 모음에서 **[!UICONTROL Test]** 버튼을 클릭합니다.

   ![](assets/email_rendering_07.png)

1. **[!UICONTROL Email rendering]** 옵션을 선택한 다음 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

   ![](assets/email_rendering_08.png)

   >[!NOTE]
   >
   >**[!UICONTROL Proof + Email rendering]** 옵션을 사용하면 증명 전송과 전자 메일 렌더링 기능을 동시에 사용할 수 있습니다. 증명된 수신인에 의해 메시지를 승인받을 수 있으며 동시에 타겟팅된 받은 편지함에 따라 메시지가 수신되는 방식을 테스트할 수 있습니다. 이 경우 테스트 프로필 증명을 선택해야 합니다. [테스트 프로필 정보](../../audiences/using/managing-test-profiles.md)를 참조하십시오.

   테스트 게재가 전송됩니다.

1. 메시지를 보낸 후 몇 분 후에 렌더링 미리 보기를 사용할 수 있습니다. 액세스하려면 **[!UICONTROL Summary]** 드롭다운 목록에서 **[!UICONTROL Proofs]**&#x200B;을(를) 선택합니다.

   ![](assets/email_rendering_03.png)

1. **[!UICONTROL Proofs]** 목록에서 **[!UICONTROL Access email rendering]**&#x200B;아이콘을 클릭합니다.

   ![](assets/email_rendering_04.png)

전용 전자 메일 렌더링 보고서가 표시됩니다. [전자 메일 렌더링 보고서 설명](#email-rendering-report-description)을 참조하십시오.

**관련 항목**:

* [전자 메일 만들기](../../channels/using/creating-an-email.md)
* [증명 보내기](../../sending/using/sending-proofs.md)
* [쿼리 편집기](../../automating/using/editing-queries.md#about-query-editor)

## 전자 메일 렌더링 보고서 설명 {#email-rendering-report-description}

이 보고서는 수신자에게 보여지는 전자 메일 주소를 표시합니다. 전자 메일 렌더링은 브라우저, 모바일 디바이스 또는 전자 메일 애플리케이션을 통해서와 같이 수신자가 전자 메일 게재를 여는 방법에 따라 다를 수 있습니다.

>[!NOTE]
>
>사용 가능한 렌더링 수는 사용권 계약에 나와 있습니다. **전자 메일 렌더링**&#x200B;이 활성화된 각 게재는 사용 가능한 렌더링(토큰으로 알려져 있음)을 하나씩 감소시킵니다.
>
>토큰은 각 개별 렌더링을 사용하며 전체 이메일 렌더링 보고서가 아닙니다. 즉,
>
>**받은 편지함 렌더링 보고서가 생성될 때마다** 메시징 클라이언트당 하나의 토큰을 공제합니다.Outlook 2000 렌더링을 위한 하나의 토큰, Outlook 렌더링을 위한 토큰, Apple Mail 렌더링을 위한 토큰.
>
>**동일한 전달의 경우**&#x200B;이메일 렌더링을 다시 생성하면 사용 가능한 토큰 수가 생성된 렌더링 수로 다시 감소합니다.


보고서 요약에는 받은 메시지, 원치 않는 메시지(스팸), 받지 못한 메시지 또는 수신 대기 중인 메시지 수가 나와 있습니다.

![](assets/inbox_rendering_report.png)

보고서는 **[!UICONTROL Mobile]**&#x200B;와(과) **[!UICONTROL Messaging clients]** 그리고 **[!UICONTROL Webmails]**&#x200B;의 세 부분으로 나뉘어져 있습니다. 보고서를 아래로 스크롤하여 이 세 가지 범주로 그룹화된 모든 렌더링을 표시합니다.

![](assets/inbox_rendering_report_3.png)

각 보고서에 대한 세부 정보를 보려면 해당 카드를 클릭합니다. 선택한 수신 방법에 대해 렌더링이 표시됩니다.

![](assets/inbox_rendering_report_2.png)

**[!UICONTROL Technical data]** 탭에서는 수신 및 캡처 날짜, 전자 메일의 전체 헤더와 같은 자세한 정보를 얻을 수 있습니다.
