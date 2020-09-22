---
title: Adobe Campaign Standard의 전달 문제 해결
description: Adobe Campaign Standard에서 발생하는 전달 문제
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 331769e7f1c1c30e3b7ff340252052c5aaa2eac9
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# 문제 해결{#troubleshooting}

배달 문제가 발생했습니까? 여기에서 해결 방법을 찾을 수 있습니다.

## ISP에 대해 동일한 오류 메시지 {#same-error-for-an-isp}

**특정 ISP에 대해 항상 동일한 오류 메시지가 표시되는 이유는 무엇입니까?**

ISP에 대해 항상 동일한 오류 메시지가 표시되는 경우, ISP에서 오류 메시지가 감지되었을 수 있습니다. 다음 권장 사항을 수행합니다.
* 존재하지 않는 이메일 주소(**사용자 알 수 없는** 실패)로 연결된 오류가 매우 많은지 확인합니다.
* 입력한 도메인 이름의 오류를 감지하도록 구독 양식을 업데이트합니다(예:gmaul.com 또는 yaho.com)을 참조하십시오.
* 메시지가 스팸으로 선언되거나 메시지가 지속적으로 차단된다는 오류가 발생하는 경우 타겟에서 지난 12개월 동안 메시지 중 하나를 열거나 클릭하지 않은 수신자를 제외해 보십시오.

문제가 지속되면 상업용, 배달 서비스 또는 Adobe Campaign 지원에 문의하십시오.

## 차단 목록 대 검역 {#denylist-versus-quarantine}

* **에 게시된 이메일 주소와 격리된 이메일 주소차단 목록의 차이점은 무엇입니까?**

   * 상태 **[!UICONTROL On denylist]** 는 피드백 루프의 결과입니다(사용자가 스팸으로 보고하면).

   * 상태 **[!UICONTROL Quarantined]** 는 부드러운 또는 하드 바운스의 결과입니다.
   자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)을 참조하십시오.

* **다른 검역 오류 이유는 무엇입니까?**

   다음과 같은 10가지 이유가 있습니다.정의되지 않음, 사용자 알 수 없음, 잘못된 도메인,차단 목록의 주소, 거부, 오류 무시, 접근 불가, 계정 비활성화, 사서함 꽉 참, 연결되지 않음.

   For more on this, see [Understanding quarantine management](../../sending/using/understanding-quarantine-management.md).

## 에서 차단 목록 제거 {#removing-from-denylist}

* **수신인 중 한 명이 실수로에 차단 목록 추가되었다. 메시지를 다시 보낼 수 있도록차단 목록에서 해당 메시지를 어떻게 제거합니까?**

   * 로 **[!UICONTROL Administration > Channels > Quarantines > Addresses]**&#x200B;이동합니다.
   * 해당 레코드의 세부 정보에서 필드 값을 로 **[!UICONTROL Status]** 설정합니다 **[!UICONTROL Valid]**.
   * 기록을 저장합니다.

* **내 IP 중 하나가에 차단 목록 있는지 어떻게 알 수 있습니까? 에서 IP를 어떻게 차단 목록 제거합니까?**

   IP 주소가차단 목록에 있는지 확인하려면 다양한 웹 사이트를 사용하여 다음과 같이 확인할 수 있습니다.
   * [MX 도구 상자](https://mxtoolbox.com/)
   * [내 IP 주소](https://whatismyipaddress.com)

   일반적으로 IP 주소 확인 결과는에 대한 세부 차단 목록 정보와 IP 주소를 차단하는 웹 사이트의 이름이 포함된 목록을 반환합니다.

   해당 링크를 클릭하면 웹 사이트 세부 정보에 액세스할 수 있습니다.

   그런 다음 IP 주소를 해당에 추가한 웹 사이트에서 웹 사이트를 삭제하도록 요청할 수 차단 목록 있습니다.

   >[!NOTE]
   >
   >상장폐지 프로세스는 웹 사이트에 따라 다를 수 있습니다. 일부 사이트에서는 계정을 만들어야 하지만 다른 사이트에서는 IP 주소를 제공해야 합니다.
