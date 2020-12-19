---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard의 전달 문제 해결
description: Adobe Campaign Standard에서 전달 가능성 문제가 발생할 때 어떻게 해야 하는지 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# 문제 해결{#troubleshooting}

배달할 수 없는 문제가 발생합니까? 여기에서 해결 방법을 찾을 수 있습니다.

## ISP {#same-error-for-an-isp}에 대한 동일한 오류 메시지

**특정 ISP에 대해 항상 동일한 오류 메시지가 표시되는 이유는 무엇입니까?**

ISP에 대해 항상 동일한 오류 메시지가 표시되는 경우, 이메일 또는 IP가 ISP에 의해 오류로 감지되었을 수 있습니다. 다음 권장 사항을 수행합니다.
* 존재하지 않는 이메일 주소(**사용자 알 수 없음** 실패)에 연결된 실패 중 상당 부분을 받았는지 확인합니다.
* 입력한 도메인 이름의 오류를 감지하도록 구독 양식을 업데이트합니다(예:gamaul.com 또는 yaho.com)을 참조하십시오.
* 메시지가 스팸으로 선언되거나 메시지가 지속적으로 차단된다는 오류가 발견되면 대상에서 지난 12개월 동안 메시지 중 하나를 열거나 클릭하지 않은 수신자를 제외해 보십시오.

문제가 지속되면 상업용, 배달 가능성 서비스 또는 Adobe Campaign 지원에 문의하십시오.

## 격리 차단 목록 대비 {#denylist-versus-quarantine}

* **에 게시된 이메일 주소와 격리된 이메일 차단 목록 주소 간의 차이점은 무엇입니까?**

   * 상태 **[!UICONTROL On denylist]**&#x200B;은 피드백 루프(사용자가 스팸으로 메시지를 보고하는 경우)의 결과입니다.

   * 상태 **[!UICONTROL Quarantined]**&#x200B;은(는) 소프트 바운스의 결과입니다.
   자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)을 참조하십시오.

* **다른 격리 오류 이유는 무엇입니까?**

   다음과 같은 10가지 이유가 있습니다.정의되지 않음, 사용자 알 수 없음, 잘못된 도메인,차단 목록의 주소, 거부됨, 오류 무시, 접근 불가, 계정 비활성화, 사서함 가득 참, 연결되지 않음.

   자세한 내용은 [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)를 참조하십시오.

## {#removing-from-denylist}차단 목록에서 제거 중

* **수신인 중 한 명이 실수로에 차단 목록 추가되었다. 메시지를 다시 보낼 수 있도록차단 목록에서 해당 메시지를 어떻게 제거합니까?**

   * **[!UICONTROL Administration > Channels > Quarantines > Addresses]**&#x200B;으로 이동합니다.
   * 해당 레코드의 세부 정보에서 **[!UICONTROL Status]** 필드의 값을 **[!UICONTROL Valid]**&#x200B;로 설정합니다.
   * 레코드를 저장합니다.

* **내 IP 중 하나가에 있는지 어떻게 알 수 차단 목록 있습니까? 내 IP를에서 어떻게 차단 목록 제거합니까?**

   IP 주소가차단 목록에 있는지 확인하려면 다양한 웹 사이트를 사용하여 다음과 같이 확인할 수 있습니다.
   * [MX 도구 상자](https://mxtoolbox.com/)
   * [내 IP 주소](https://whatismyipaddress.com)

   일반적으로 IP 주소 확인 결과는의 세부 정보와 IP 주소를 차단 목록 차단하는 웹 사이트의 이름이 포함된 목록을 반환합니다.

   해당 링크를 클릭하면 웹 사이트 세부 정보에 액세스할 수 있습니다.

   그런 다음 IP 주소를에 추가한 웹 사이트에서 웹 사이트를 삭제하도록 요청할 수 차단 목록 있습니다.

   >[!NOTE]
   >
   >삭제 프로세스는 웹 사이트에 따라 다를 수 있습니다. 일부 사이트에서는 계정을 만들어야 하지만 다른 사이트에서는 IP 주소를 제공해야 합니다.
