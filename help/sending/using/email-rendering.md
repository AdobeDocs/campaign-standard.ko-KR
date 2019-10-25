---
title: 이메일 렌더링
seo-title: 이메일 렌더링
description: 이메일 렌더링
seo-description: 이메일 렌더링 기능을 살펴보십시오.
page-status-flag: 활성화 안 함
uuid: c423e237-ad39-4797-ac3a-4320894a8f99
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 보내기
content-type: reference
topic-tags: preparing and-testing-messages
discoiquuid: 2b5b13c8-2e51-4985-a161-c1d7f0fc32b4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 51d80fc9c683e39b9d08ba7d36b76b71a9dd1e8c

---


# 이메일 렌더링{#email-rendering}

이 **[!UICONTROL Send]** 단추를 누르기 전에 메시지가 다양한 웹 클라이언트, 웹 메일 및 장치에서 최적의 방식으로 표시되는지 확인하십시오.

이를 위해 Adobe Campaign은 렌더링을 캡처하여 전용 보고서에서 사용할 수 있도록 합니다. 이렇게 하면 메시지를 수신할 수 있는 다른 컨텍스트에서 메시지를 미리 볼 수 있습니다.

Adobe Campaign에서 이메일 렌더링에 **** 사용할 수 있는 모바일, 메시징 및 웹 메일 클라이언트는 리트머스 [웹](https://litmus.com/email-testing) 사이트에 **표시됩니다(모든 이메일 클라이언트**&#x200B;보기 클릭).

## 이메일 렌더링 보고서 확인 {#checking-the-email-rendering-report}

이메일 배달을 만들고 해당 컨텐츠와 타깃팅된 인구를 정의했으면 아래 단계를 따르십시오.

1. 대상을 **클릭하여** 탭에 액세스합니다 **[!UICONTROL Test profiles]** .

   ![](assets/email_rendering_05.png)

1. 쿼리 편집기를 사용하여 이메일 렌더링을 **위한 테스트 프로필을 포함하여 사용할 테스트 프로필을** 정의합니다. 테스트 [프로필](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles)정보를 참조하십시오.

   ![](assets/email_rendering_06.png)

1. 쿼리를 확인하고 변경한 내용을 저장합니다.
1. 작업 표시줄에서 **[!UICONTROL Test]** 단추를 클릭합니다.

   ![](assets/email_rendering_07.png)

1. 옵션을 **[!UICONTROL Email rendering]** 선택한 다음 을 클릭합니다 **[!UICONTROL OK]**.

   ![](assets/email_rendering_08.png)

   >[!NOTE]
   >
   >이 **[!UICONTROL Proof + Email rendering]** 옵션을 사용하면 증명 자료를 보내고 이메일 렌더링 기능을 동시에 사용할 수 있습니다. 메시지를 인증된 수신자가 승인하도록 할 수 있으며 동시에 타깃팅된 받은 편지함에 따라 메시지가 수신되는 방식을 테스트할 수 있습니다. 이 경우 증명 테스트 프로필도 선택해야 합니다. 테스트 [프로필](../../sending/using/managing-test-profiles-and-sending-proofs.md#about-test-profiles)정보를 참조하십시오.

   테스트 배달이 전송됩니다.

1. 메시지를 보낸 후 몇 분 후에 렌더링 축소판을 사용할 수 있습니다. 액세스 권한을 부여하려면 **[!UICONTROL Proofs]** 드롭다운 **[!UICONTROL Summary]** 목록에서 선택합니다.

   ![](assets/email_rendering_03.png)

1. 목록에서 **[!UICONTROL Proofs]** 아이콘을 클릭합니다 **[!UICONTROL Access email rendering]** .

   ![](assets/email_rendering_04.png)

전용 이메일 렌더링 보고서가 표시됩니다. 이메일 [렌더링 보고서 설명을](#email-rendering-report-description)참조하십시오.

**관련 항목**:

* [이메일 만들기](../../channels/using/creating-an-email.md)
* [테스트 프로파일 관리 및 증명 전송](../../sending/using/managing-test-profiles-and-sending-proofs.md)
* [쿼리 편집기](../../automating/using/editing-queries.md#about-query-editor)

## 이메일 렌더링 보고서 설명 {#email-rendering-report-description}

이 보고서는 받는 사람에게 나타나는 이메일 제목을 표시합니다. 이메일 렌더링은 수신자가 이메일 배달을 여는 방법에 따라 다를 수 있습니다.브라우저, 모바일 디바이스 또는 이메일 애플리케이션을 통해

>[!NOTE]
>
>사용 가능한 렌더링 수는 라이센스 계약에 나와 있습니다. 이메일 렌더링을 **활성화한 각 전달은 사용 가능한 렌더링** (토큰이라고 함)을 하나씩 감소시킵니다. 리트머스 클라이언트인 경우 자체 리트머스 계정을 사용하여 Adobe Campaign에서 이메일 렌더링을 프로비저닝하고 사용할 수 있습니다. 자세한 내용은 Adobe 계정 담당자에게 문의하십시오.

보고서 요약에는 받은 메시지, 원치 않는 메시지(스팸), 받은 메시지 또는 수신 대기 중인 메시지 수가 표시됩니다.

![](assets/inbox_rendering_report.png)

보고서는 다음 세 부분으로 나뉘어져 있습니다. **[!UICONTROL Mobile]**&#x200B;및 **[!UICONTROL Messaging clients]**&#x200B;를 **[!UICONTROL Webmails]**&#x200B;참조하십시오. 보고서를 아래로 스크롤하여 이 세 가지 카테고리로 그룹화된 모든 렌더링을 표시합니다.

![](assets/inbox_rendering_report_3.png)

각 보고서에 대한 세부 정보를 보려면 해당 카드를 클릭합니다. 선택한 수신 방법에 대해 렌더링이 표시됩니다.

![](assets/inbox_rendering_report_2.png)

이 **[!UICONTROL Technical data]** 탭에서는 수신 및 캡처 날짜, 이메일의 전체 헤더와 같은 자세한 정보를 얻을 수 있습니다.
