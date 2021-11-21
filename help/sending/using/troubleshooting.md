---
title: Adobe Campaign Standard의 게재 기능 문제 해결
description: Adobe Campaign Standard에서 게재 기능 문제가 발생할 때 수행할 작업을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 0470b986-c00a-4441-8621-82c7112a9953
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 1%

---

# 문제 해결{#troubleshooting}

게재 능력에 문제가 있습니까? 여기서 해결 방법을 찾을 수 있습니다.

## ISP에 대해 동일한 오류 메시지 {#same-error-for-an-isp}

**특정 ISP에 대해 항상 동일한 오류 메시지가 표시되는 이유는 무엇입니까?**

ISP에 대해 항상 동일한 오류 메시지가 표시되는 경우, 이메일 또는 IP가 ISP에서 오류로 감지되었을 수 있습니다. 다음 권장 사항을 수행합니다.
* 존재하지 않는 이메일 주소에 연결된 오류 중 많은 부분을 수신하는지 확인합니다(**사용자 알 수 없음** 실패).
* 가입 양식을 업데이트하여 입력한 도메인 이름의 오류를 검색합니다(예: gmaul.com 또는 yaho.com)
* 메시지가 스팸으로 선언되거나 메시지가 항상 차단된다는 오류가 표시되면 지난 12개월 동안 메시지 중 하나에서 열지 또는 클릭되지 않은 수신자를 대상에서 제외하십시오.

문제가 지속되면 커머셜, 게재 가능성 서비스 또는 Adobe Campaign 지원에 문의하십시오.

## 격리 차단 목록과 비교 {#denylist-versus-quarantine}

* **의 이메일 주소와 격리된 이메일 차단 목록 주소 간의 차이점은 무엇입니까?**

   * 상태 **[!UICONTROL On denylist]** 의 결과입니다. [피드백 루프](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#feedback-loops) (사용자가 메시지를 스팸으로 보고하는 경우)

   * 상태 **[!UICONTROL Quarantined]** 소프트 또는 하드 바운스의 결과입니다.
   자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)을 참조하십시오.

* **다른 격리 오류 이유는 무엇입니까?**

   다음은 10가지 가능한 이유입니다. 정의되지 않음, 사용자 알 수 없음, 잘못된 도메인,의 주소차단 목록, 거부, 오류 무시, 접근 불가, 계정 사용 안 함, 사서함 가득 참, 연결되지 않음.

   자세한 내용은 [격리 관리 이해](../../sending/using/understanding-quarantine-management.md).

## 에서 차단 목록 제거 {#removing-from-denylist}

* **받는 사람 중 한 명이 실수로에 차단 목록 추가되었습니다. 메시지를 다시 전송할 수 있도록 차단 목록에서 해당 메시지를 제거하려면 어떻게 합니까?**

   * 이동 **[!UICONTROL Administration > Channels > Quarantines > Addresses]**.
   * 해당 레코드의 세부 정보에서 **[!UICONTROL Status]** 필드 대상 **[!UICONTROL Valid]**.
   * 레코드를 저장합니다.

* **IP 중 하나가 중인지 확인하려면 어떻게 해야 차단 목록 합니까? 에서 IP를 제거하려면 어떻게 차단 목록 합니까?**

   IP 주소가 상태인지 확인하려면 차단 목록 다양한 웹 사이트를 사용하여 확인할 수 있습니다. 예를 들면 다음과 같습니다.
   * [MX 도구 상자](https://mxtoolbox.com/)
   * [내 IP 주소는 무엇입니까](https://whatismyipaddress.com)

   일반적으로 IP 주소 확인 결과는의 세부 정보와 IP 주소를 차단한 웹 사이트의 이름이 차단 목록 포함된 목록을 반환합니다.

   해당 링크를 클릭하면 웹 사이트 세부 사항에 액세스할 수 있습니다.

   그런 다음 해당 웹 사이트에 IP 주소를 추가한 웹 사이트의 삭제를 요청할 수 차단 목록 있습니다.

   >[!NOTE]
   >
   >삭제 프로세스는 웹 사이트에 따라 달라질 수 있습니다. 일부 사이트에서는 계정을 만들어야 하지만 다른 사이트에서는 IP 주소를 제공해야 합니다.
