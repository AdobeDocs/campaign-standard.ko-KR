---
title: Adobe Campaign Standard의 전달성 문제 해결
description: Adobe Campaign Standard에서 전달성 문제가 발생할 때 수행할 작업에 대해 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 0470b986-c00a-4441-8621-82c7112a9953
source-git-commit: 449187bba167f9ce00e644d44a124b36030ba001
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 문제 해결{#troubleshooting}

전달에 문제가 있습니까? 여기에서 해결책을 찾을 수 있습니다.

## ISP에 대해 동일한 오류 메시지 {#same-error-for-an-isp}

**특정 ISP에 대해 항상 동일한 오류 메시지가 표시되는 이유는 무엇입니까?**

ISP에 대해 항상 동일한 오류 메시지가 표시되는 경우 ISP에서 이메일이나 IP가 잘못된 것으로 감지되었을 수 있습니다. 다음 권장 사항을 수행합니다.

* 존재하지 않는 전자 메일 주소에 연결된 오류가 많이 수신되는지 확인합니다(**사용자 알 수 없음**&#x200B;개 오류).
* 가입 양식을 업데이트하여 입력한 도메인 이름의 오류를 감지합니다(예: gmaul.com 또는 yaho.com).
* 메시지가 스팸으로 선언되거나 메시지가 계속 차단된다는 오류가 표시되면 지난 12개월 동안 메시지 중 하나를 열거나 클릭하지 않은 수신자를 대상에서 제외해 보십시오.

문제가 지속되면 상업용 또는 게재 기능 서비스 또는 Adobe Campaign 지원 센터에 문의하십시오.

## 차단 목록에 추가하다 격리 대 격리 {#denylist-versus-quarantine}

* 차단 목록에 추가하다 **전자 메일 주소와 격리된 전자 메일 주소의 차이점은 무엇입니까?**

   * **[!UICONTROL On denylist]** 상태는 [피드백 루프](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html?lang=ko#feedback-loops)의 결과입니다(사용자가 메시지를 스팸으로 보고할 때).

   * 상태 **[!UICONTROL Quarantined]**&#x200B;은(는) 소프트 또는 하드 바운스의 결과입니다.

  자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)을 참조하십시오.

* **다른 격리 오류 이유는 무엇을 의미합니까?**

  정의되지 않음, 사용자 알 수 없음, 잘못된 도메인, 주소 차단 목록에 추가하다, 거부, 오류 무시, 연결할 수 없음, 계정 사용 안 함 사서함 가득 참, 연결되지 않음 등 10가지 가능한 이유가 있습니다.

  자세한 내용은 [격리 관리 이해](../../sending/using/understanding-quarantine-management.md)를 참조하십시오.

## 차단 목록 제거 {#removing-from-denylist}

* **받는 사람 중 한 명이 실수로 차단 목록에 추가되었습니다. 메시지를 다시 보낼 수 있도록 차단 목록에 추가하다에서 어떻게 제거할 수 있습니까?**

   * **[!UICONTROL Administration > Channels > Quarantines > Addresses]**(으)로 이동합니다.
   * 해당 레코드의 세부 정보에서 **[!UICONTROL Status]** 필드의 값을 **[!UICONTROL Valid]**(으)로 설정합니다.
   * 레코드를 저장합니다.

* **내 IP 중 하나가 차단 목록에 추가하다에 있는지 어떻게 확인할 수 있습니까? 차단 목록에 추가하다에서 IP를 제거하려면 어떻게 해야 합니까?**

  IP 주소가 차단 목록에 추가하다에 있는지 확인하려면 다음과 같이 다양한 웹 사이트를 사용하여 확인할 수 있습니다.
   * [MX 도구 상자](https://mxtoolbox.com/)
   * [내 IP 주소](https://whatismyipaddress.com)

  일반적으로 IP 주소 검사 결과는 차단 목록에 추가하다 웹 사이트의 세부 정보와 IP 주소를 차단한 이름이 포함된 목록을 반환합니다.

  해당 링크를 클릭하면 웹 사이트 세부 정보에 액세스할 수 있습니다.

  그런 다음 IP 주소를 차단 목록에 추가하다에 추가한 웹 사이트에서 웹 사이트를 삭제할 것을 요청할 수 있습니다.

  >[!NOTE]
  >
  >상장 폐지 절차는 웹 사이트에 따라 다를 수 있습니다. 일부 사이트에서는 계정을 만들어야 하지만 다른 사이트에서는 IP 주소를 제공해야 합니다.
