---
title: 메시지 대시보드
seo-title: 메시지 대시보드
description: 메시지 대시보드
seo-description: 작업 표시줄 및 다양한 기능 블록을 포함하여 메시지 대시보드의 기능을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: 9 BB 44 EE 8-2 CF 6-43 CE -94 A 4-367 F 4 E 469713
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: About-communication-channels
discoiquuid: 90 A 78742-697 F -46 DA -8 C 54-108048 E 57 B 67
context-tags: 전달, 기본
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 25d997b2e5aa41e29e49ab047398b3db811bd6b6

---


# Message dashboard{#message-dashboard}

메시지 대시보드는 작업 모음으로 다시 그룹화된 작업 영역과 메시지 매개 변수를 설정하고 메시지를 전송할 수 있는 다양한 기능 블록으로 구성됩니다. 이러한 요소는 다음과 같습니다.

![](assets/delivery_dashboard_2.png)

## Gray bar {#gray-bar}

회색 막대는 메시지에 연결된 다양한 아이콘을 다시 그룹화합니다.

* **[!UICONTROL Summary]**: 메시지와 관련된 기본 정보를 표시하거나 숨깁니다.
* **[!UICONTROL Edit properties]**: 메시지의 [고급 매개 변수를 편집할](../../administration/using/configuring-email-channel.md#list-of-email-properties)수 있습니다.
* **[!UICONTROL Reports]**: 메시지와 관련된 보고서에 액세스할 수 있습니다.

**관련 항목:**

* [채널 구성](../../administration/using/about-channel-configuration.md)
* [보고서 액세스](../../reporting/using/about-dynamic-reports.md)

## Action bar {#action-bar}

작업 모음에는 메시지와 상호 작용할 수 있는 다른 아이콘이 있습니다.

![](assets/delivery_dashboard_4.png)

설정한 매개 변수와 진행 중인 매개 변수에 따라 특정 아이콘을 사용하지 못할 수 있습니다.

* **[!UICONTROL Show proofs]**: 전송된 증명 목록 (있는 경우) 를 표시하거나 숨깁니다. 이 단추는 문서를 보낸 후에만 활성화됩니다.

   For more on proofs, see [Managing test profiles and sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md).

* **[!UICONTROL Send a test]**: 사용할 승인 모드를 선택할 수 있습니다. **[!UICONTROL Email rendering]****[!UICONTROL Proof]** 를 입력합니다. For more on test profiles, see [Sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).

   이 단추는 테스트 프로필을 설정한 후에만 활성화됩니다.

   >[!NOTE]
   >
   >For an SMS message, there is no other choice: it is automatically a **[!UICONTROL Proof]**.

* **[!UICONTROL Prepare send]**: 전송을 준비합니다. **[!UICONTROL Deployment]** 블록이 나타나고 준비 결과가 표시됩니다. 이 단추는 대상을 입력한 후에만 나타납니다. 해당 단추를 사용하여 언제든지 준비를 중지할 수 있습니다.

   For more on message preparation, [Preparing the send](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Confirm send]**: 메시지 전송을 확인합니다. The sending statistics appear in the **[!UICONTROL Deployment]** block. 이 단추는 전송이 준비된 후에만 나타납니다. You can stop or pause the send at any time using the **Stop send** and **[!UICONTROL Pause]** buttons.

   For more on confirming sending, see [Sending messages](../../sending/using/confirming-the-send.md).

## Blocks {#blocks}

기본 화면은 다른 블록으로 구성됩니다. 블록 안쪽을 클릭하여 해당 매개 변수 화면에 액세스합니다.

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Deployment]**: 메시지 준비 또는 전송 진행 상황을 추적할 수 있습니다. 이 블록의 오른쪽 아래 섹션에 있는 단추를 클릭하여 전송 및 분석 로그에 액세스합니다. 이 블록은 전송이 준비된 후에만 나타납니다. 에 대한 자세한 내용을 살펴보십시오. See [Confirming send](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**: 테스트 프로필은 물론 메시지의 기본 Target를 설정할 수 있습니다. See [Creating audiences](../../audiences/using/creating-audiences.md).
* **[!UICONTROL Schedule]**: 메시지를 보낼 날짜를 지정할 수 있습니다. [예약을 참조하십시오](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Content]**: 메시지의 콘텐츠를 정의하고 미리 볼 수 있습니다. See [Defining content](../../designing/using/designing-content-in-adobe-campaign.md).

