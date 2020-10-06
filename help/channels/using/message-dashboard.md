---
title: 메시지 대시보드
description: 작업 표시줄과 다양한 기능 블록을 비롯하여 메시지 대시보드가 무엇으로 구성되어 있는지 확인합니다.
page-status-flag: never-activated
uuid: 9bb44ee8-2cf6-43ce-94a4-367f4e469713
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: about-communication-channels
discoiquuid: 90a78742-697f-46da-8c54-108048e57b67
context-tags: delivery,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9c812b0b622b82ba7aa382f04edb7a2a3f717cd4
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 4%

---


# 메시지 대시보드{#message-dashboard}

메시지 대시보드는 메시지 매개 변수를 설정하고 전송할 수 있도록 해주는 작업 막대와 다양한 기능 블록으로 재그룹화된 다양한 아이콘으로 구성된 작업 공간입니다. 이러한 요소는 향후 제공됩니다.

![](assets/delivery_dashboard_2.png)

## 회색 막대 {#gray-bar}

회색 막대는 메시지에 연결된 다양한 아이콘을 다시 그룹화합니다.

* **[!UICONTROL Summary]**:메시지에 대한 기본 정보를 표시하거나 숨깁니다.
* **[!UICONTROL Edit properties]**:메시지의 [고급 매개 변수를 편집할 수 있습니다](../../administration/using/configuring-email-channel.md#list-of-email-properties).
* **[!UICONTROL Reports]**:는 메시지와 관련된 보고서에 액세스할 수 있도록 해줍니다.

**관련 항목:**

* [채널 구성](../../administration/using/about-channel-configuration.md)
* [보고서 액세스](../../reporting/using/about-dynamic-reports.md)

## 작업 표시줄 {#action-bar}

작업 표시줄에는 메시지와 상호 작용할 수 있도록 해주는 다른 아이콘이 있습니다.

![](assets/delivery_dashboard_4.png)

설정된 매개 변수와 진행 상태에 따라 특정 아이콘을 사용할 수 없을 수도 있습니다.

* **[!UICONTROL Show proofs]**:전송된 증명 목록이 있는 경우 표시/숨기기 이 단추는 교정본을 보낸 경우에만 활성화됩니다.

   교정에 대한 자세한 내용은 증거 [전송 을 참조하십시오](../../sending/using/sending-proofs.md).

* **[!UICONTROL Send a test]**:사용할 승인 모드를 선택할 수 있습니다. **[!UICONTROL Email rendering]** (이메일만 해당) **[!UICONTROL Proof]** 또는 둘 다. 테스트 프로파일에 대한 자세한 내용은 증명 [보내기를 참조하십시오](../../sending/using/sending-proofs.md). 이 단추는 테스트 프로필을 만든 후에만 활성화됩니다.

* **[!UICONTROL Prepare send]**:전송을 준비하기 시작합니다. 블록이 **[!UICONTROL Deployment]** 나타나고 준비 결과가 표시됩니다. 이 단추는 타겟을 입력한 경우에만 나타납니다. 해당 단추를 사용하여 언제든지 준비를 중지할 수 있습니다. For more on message preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Confirm send]**:메시지 보내기를 확인합니다. 전송 통계가 **[!UICONTROL Deployment]** 블록에 나타납니다. 이 단추는 전송을 준비한 후에만 나타납니다. 전송 **중지** 및 **[!UICONTROL Pause]** 단추를 사용하여 언제든지 전송을 중지하거나 일시 중지할 수 있습니다. 전송 확인에 대한 자세한 내용은 메시지 [보내기를 참조하십시오](../../sending/using/confirming-the-send.md).

## 블록 {#blocks}

메인 스크린은 다른 블록으로 구성되어 있다. 블록 내부를 클릭하여 해당 매개 변수 화면에 액세스합니다.

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Deployment]**:메시지 준비 또는 전송 진행 상태를 추적할 수 있습니다. 이 블록의 오른쪽 아래에 있는 단추를 클릭하여 보내기 및 분석 로그에 액세스합니다. 이 블록은 전송을 준비한 경우에만 나타납니다. 자세한 내용 See [Confirming send](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**:테스트 프로필뿐만 아니라 메시지의 주 타겟을 설정할 수 있습니다. [대상자 만들기](../../audiences/using/creating-audiences.md)를 참조하십시오.
* **[!UICONTROL Schedule]**:메시지를 보낼 날짜를 지정할 수 있습니다. 예약을 [참조하십시오](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Content]**:메시지 내용을 정의하고 미리 볼 수 있습니다. See [Key steps to send a message](../../channels/using/key-steps-to-send-a-message.md).

## 경고 {#warnings}

경우에 따라 메시지 대시보드 위쪽에 있는 노란색 배너에 경고가 표시될 수 있습니다.

![](assets/delivery_dashboard_warnings.png)

아래는 표시할 수 있는 메시지 목록입니다.

* *&quot;이 이메일에 대해 SMTP 테스트 모드 옵션을 사용할 수 있습니다.메시지가 전송되지 않습니다.&quot;*

   자세한 내용은 [이 섹션](../../administration/using/configuring-email-channel.md#smtp-test-mode)을 참조하십시오.

* *&quot;라우팅 외부 계정을 사용할 수 없습니다.&quot;*

   자세한 내용은 [외부 계정을 참조하십시오](../../administration/using/external-accounts.md).

* *&quot;현재 IP 친화성을 전송 프로세스에서 처리하지 않으므로 메시지를 보낼 수 없습니다.&quot;*

   이 메시지가 표시되면 IP 친화성 정의 수준 또는 전송 프로세스 수준에서 문제가 발생합니다. Adobe 관리자에게 문의하십시오.

* *&quot;이는 즉시 사용 가능한 트랜잭션 메시지 템플릿입니다. 수정하려는 경우 복제하여 복사본에서 작업해야 합니다.&quot;*

   기본적으로 제공되는 트랜잭션 메시지 템플릿 중 일부는 내장된 랜딩 페이지 템플릿입니다. 자세한 내용은 [이 섹션](../../channels/using/landing-page-templates.md)을 참조하십시오.

* *&quot;이 메시지는 기술적 트랜잭션 메시지 템플릿입니다. 수정하거나 게시할 수 없습니다.&quot;*

   이 경고는 편집할 수 없는 빈 트랜잭션 메시지 템플릿에 표시됩니다. For more on transactional messages, see [this section](../../channels/using/getting-started-with-transactional-msg.md).
