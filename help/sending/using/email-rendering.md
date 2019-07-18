---
title: 이메일 렌더링
seo-title: 이메일 렌더링
description: 이메일 렌더링
seo-description: 이메일 렌더링 기능을 살펴보십시오.
page-status-flag: 정품 인증 안 함
uuid: C 423 E 237-AD 39-4797-AC 3 A -4320894 A 8 F 99
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 전송
content-type: 참조
topic-tags: preparing-and-testing-messages
discoiquuid: 2 B 5 B 13 C 8-2 E 51-4985-A 161-C 1 D 7 F 0 FC 32 B 4
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Email rendering{#email-rendering}

**[!UICONTROL Send]** 단추를 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방법으로 표시되는지 확인합니다.

이를 위해 Adobe Campaign는 렌더링을 캡처하여 전용 보고서에서 사용할 수 있게 합니다. 이렇게 하면 전송된 메시지를 수신할 수 있는 다른 컨텍스트에서 미리 볼 수 있습니다.

The mobile, messaging and webmail clients available for **Email rendering** in Adobe Campaign are listed on the Litmus [website](https://litmus.com/email-testing) (click **View all email clients**).

## Checking the Email rendering report {#checking-the-email-rendering-report}

이메일 배달을 만들고 타깃팅된 모집단을 정의했으면 아래 단계를 따르십시오.

1. **대상을** 클릭하여 **[!UICONTROL Test profiles]** 탭에 액세스합니다.

   ![](assets/email_rendering_05.png)

1. Use the query editor to define the test profiles that you want to use, including the test profiles that are for **Email rendering** use. See [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

   ![](assets/email_rendering_06.png)

1. 쿼리를 확인하고 확인한 다음 변경 사항을 저장합니다.
1. Click the **[!UICONTROL Test]** button in the action bar.

   ![](assets/email_rendering_07.png)

1. Select the **[!UICONTROL Email rendering]** option then click **[!UICONTROL OK]**.

   ![](assets/email_rendering_08.png)

   >[!NOTE]
   >
   >**[!UICONTROL Proof + Email rendering]** 이 옵션을 사용하면 증거 자료를 전송하고 이메일 렌더링 기능을 동시에 사용할 수 있습니다. 증명 받는 사람이 메시지를 승인하고 동시에 받은 받은 편지함에 따라 메시지가 수신될 방법을 테스트할 수 있습니다. 이 경우, 증명 테스트 프로필을 선택해야 합니다. See [About test profiles](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles).

   테스트 배달이 전송됩니다.

1. 렌더링 축소판은 메시지를 전송한 후 몇 분 후에 사용할 수 있습니다. To access them, select **[!UICONTROL Proofs]** in the **[!UICONTROL Summary]** drop-down list.

   ![](assets/email_rendering_03.png)

1. **[!UICONTROL Proofs]** 목록에서 **[!UICONTROL Access email rendering]** 아이콘을 클릭합니다.

   ![](assets/email_rendering_04.png)

전용 이메일 렌더링 보고서가 표시됩니다. [이메일 렌더링 보고서 설명을 참조하십시오](../../sending/using/email-rendering.md#email-rendering-report-description).

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [테스트 프로파일 관리 및 증명 전송](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [쿼리 편집기](../../automating/using/editing-queries.md#about-query-editor)

## Email rendering report description {#email-rendering-report-description}

이 보고서는 받는 사람에게 나타나는 이메일 렌더링을 보여줍니다. 이메일 렌더링은 수신자가 이메일 배달을 여는 방법에 따라 다를 수 있습니다. 브라우저, 모바일 디바이스 또는 이메일 애플리케이션을 통해

>[!NOTE]
>
>사용 가능한 렌더링 개수는 라이센스 계약에 나와 있습니다. **이메일 렌더링** 기능을 사용할 때마다 사용 가능한 렌더링 (토큰으로 알려져 있음) 이 하나씩 줄어듭니다. Litmus 클라이언트인 경우 자신만의 Litmus 계정을 사용하여 Adobe Campaign에서 이메일 렌더링을 프로비저닝하고 사용할 수 있습니다. 자세한 내용은 Adobe 계정 담당자에게 문의하십시오.

보고서 요약은 수신, 원하지 않는 (스팸), 수신 안 함 또는 수신을 대기 중인 메시지의 수를 나타냅니다.

![](assets/inbox_rendering_report.png)

The report is divided into three parts: **[!UICONTROL Mobile]**, **[!UICONTROL Messaging clients]**, and **[!UICONTROL Webmails]**. 보고서 아래로 스크롤하여 이 세 가지 카테고리로 그룹화된 모든 렌더링을 표시합니다.

![](assets/inbox_rendering_report_3.png)

각 보고서에 대한 세부 정보를 얻으려면 해당 카드를 클릭합니다. 선택한 수신 방법에 대해 렌더링이 표시됩니다.

![](assets/inbox_rendering_report_2.png)

**[!UICONTROL Technical data]** 이 탭에서는 수신 및 캡처 날짜, 이메일의 전체 헤더 등의 추가 정보를 얻을 수 있습니다.
