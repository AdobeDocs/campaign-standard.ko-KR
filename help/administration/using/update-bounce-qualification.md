---
title: ISP 중단 후 바운스 자격 업데이트
description: ISP 중단 후 바운스 자격을 업데이트하는 방법을 알아봅니다.
audience: delivery
hidefromtoc: true
exl-id: b06e9009-70c7-459f-8a9f-d5b7020d662f
source-git-commit: f81b8a3b076a6e29b697f21ea4d99fa7d5b6788c
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 2%

---

# ISP 중단 후 바운스 자격 업데이트 {#update-bounce-qualification.md}

## 컨텍스트

ISP가 중단되는 경우 Campaign을 통해 보낸 이메일이 수신자에게 정상적으로 전달될 수 없습니다. 이러한 이메일은 바운스로 잘못 표시됩니다.

2020년 12월, Gmail의 글로벌 문제로 인해 유효한 Gmail 전자 메일 주소로 전송된 일부 전자 메일 메시지가 바운스 다음 응답과 함께 Gmail 서버에서 잘못된 전자 메일 주소로 잘못 하드 바운스되었습니다. *&quot;550-5.1.1 연결하려고 시도한 전자 메일 계정이 존재하지 않습니다.&quot;*

Google은 이 문제를 일으킨 Gmail 중단과 운영 중단이 12월 14일 오전 6시 55분에 시작되어 12월 15일 오후 6시 9분 EST에서 종료되었다고 밝혔습니다. 또한 데이터 분석에서는 12월 16일 오전 2시 6분 EST에서 Gmail 바운스의 매우 짧은 급증을 보여주었으며, 12월 15일 오후 2시~오후 6시 30분 EST 사이에 가장 많은 수가 발생했습니다.

>[!NOTE]
>
>[이 페이지](https://www.google.com/appsstatus#hl=en&amp;v=status)에서 Google Workspace 상태 대시보드를 확인할 수 있습니다.


표준 바운스 처리 논리에 따라 Adobe Campaign은 **[!UICONTROL Status]** 설정이 **[!UICONTROL Quarantine]**&#x200B;인 격리 목록에 이 수신자를 자동으로 추가했습니다. 이 문제를 해결하려면 야간 정리 워크플로우에서 해당 수신자를 찾아 제거하거나 **[!UICONTROL Status]**&#x200B;을(를) **[!UICONTROL Valid]**(으)로 변경하여 Campaign에서 격리 테이블을 업데이트해야 합니다.

이 Gmail 문제의 영향을 받은 수신자를 찾으려면 또는 다른 ISP에서 이 문제가 다시 발생하는 경우 아래 지침을 참조하십시오.

## 업데이트할 프로세스

격리 테이블에서 쿼리를 실행하여 중단의 영향을 받을 가능성이 있는 모든 Gmail(또는 기타 ISP) 수신자를 필터링하여 격리 목록에서 제거하고 향후 Campaign 이메일 게재에 포함할 수 있습니다.

인시던트의 일정에 따라, 아래는 이 쿼리에 대한 권장 지침입니다.

>[!IMPORTANT]
>
>이 날짜/시간은 동부 표준 시간대(EST)를 기반으로 합니다. 인스턴스의 시간대를 조정하십시오.

격리 목록의 **[!UICONTROL Error text]** 필드에 SMTP 바운스 응답 정보가 있는 캠페인 인스턴스의 경우:

* **오류 텍스트(격리 텍스트)**&#x200B;에 &quot;550-5.1.1 연결하려는 전자 메일 계정이 존재하지 않습니다&quot; 및 **오류 텍스트(격리 텍스트)**&#x200B;에 &quot;support.google.com&quot;이 **
* **2020년 12월 14일 오전 6시:55:이후 상태(@lastModified)** 업데이트
* **2020/12/16 오전 6시:00:이전 상태(@lastModified)** 업데이트

영향을 받는 받는 받는 받는 받는 사람 목록을 가지고 있으면 **[!UICONTROL Database cleanup]** 워크플로에 의해 격리 목록에서 제거될 수 있도록 해당 받는 사람을 **[!UICONTROL Valid]** 상태로 설정하거나 표에서 삭제할 수 있습니다.

**관련 항목:**
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [반송 메일 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)
