---
title: ISP 중단 후 바운스 자격 업데이트
description: ISP 중단 후 반송 조건을 업데이트하는 방법을 알아봅니다.
audience: delivery
content-type: reference
topic-tags: monitoring-deliveries
hidefromtoc: true
exl-id: b06e9009-70c7-459f-8a9f-d5b7020d662f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 4%

---

# ISP 중단 후 바운스 자격 업데이트 {#update-bounce-qualification.md}

최신 버전의 Campaign을 실행하지 않는 경우 이 섹션이 적용될 수 있습니다. Adobe Campaign 담당자에게 문의하십시오.

## 컨텍스트

ISP가 중단되는 경우, Campaign을 통해 전송된 이메일을 수신자에게 전달할 수 없습니다. 이 이메일은 반송 행위로 잘못 표시될 것입니다.

2020년 12월, Gmail의 글로벌 문제로 인해 유효한 Gmail 이메일 주소로 전송된 일부 이메일 메시지가 바운스 다음 응답이 있는 Gmail 서버에 의해 잘못된 이메일 주소로 잘못 바운스되었습니다. *&quot;550-5.1.1 연결하려는 전자 메일 계정이 없습니다.&quot;*

Google은 이 문제를 일으킨 Gmail의 정전과 혼란을 12월 14일 오전 6시 55분에 시작했고 12월 15일 동부시간 오후 6시 9분에 끝났다고 밝혔습니다. Adobe의 데이터 분석은 또한 12월 16일 오전 2시 6분에 EST에서 Gmail 바운스의 매우 짧은 스파이크를 보여주었으며, 대부분은 12월 15일 오후 2시 ~ 오후 6시 30분 사이에 발생합니다.

>[!NOTE]
>
>[이 페이지에서 Google 작업 공간 상태 대시보드를 확인할 수 있습니다](https://www.google.com/appsstatus#hl=en&amp;v=status).


표준 바운스 처리 논리에 따라 Adobe Campaign은 **[!UICONTROL Quarantine]** 의 **[!UICONTROL Status]** 설정을 사용하여 이러한 수신자를 격리 목록에 자동으로 추가했습니다. 이 문제를 해결하려면 야간 정리 워크플로우가 제거할 수 있도록 이러한 수신자를 찾아 제거하거나 **[!UICONTROL Status]** 을 **[!UICONTROL Valid]**(으)로 변경하여 Campaign에서 격리 테이블을 업데이트해야 합니다.

이 Gmail 문제의 영향을 받은 수신자를 찾거나 다른 ISP에서 이 문제가 다시 발생하는 경우 아래 지침을 참조하십시오.

## 업데이트할 프로세스

격리 테이블에서 쿼리를 실행하여 중단의 영향을 받을 수 있는 모든 Gmail(또는 기타 ISP) 수신자를 필터링하여 격리 목록에서 제거하고 향후 Campaign 이메일 게재에 포함할 수 있습니다.

사고 기간에 따라 이 쿼리에 대한 권장 지침은 아래에 나와 있습니다.

>[!IMPORTANT]
>
>이 날짜/시간은 동부 표준 시간대(EST)를 기반으로 합니다. 인스턴스의 시간대에 맞게 조정하십시오.

격리 목록의 **[!UICONTROL Error text]** 필드에 SMTP 바운스 응답 정보가 있는 Campaign 인스턴스의 경우:

* **오류 텍스트(격리 텍스트)** 에 &quot;550-5.1.1에 연결하려는 전자 메일 계정이 없습니다.&quot; AND  **오류 텍스트(격리 텍스트)** 에 &quot;support.google.com&quot; **
* **12/14/2020 6** 00AM 이후:55:의 업데이트 상태(@lastModified)
* **12/16/2020 6** 00AM 이전:00:에 상태 업데이트(@lastModified)

영향을 받는 수신자 목록이 있으면 **[!UICONTROL Valid]** 상태로 설정하여 **[!UICONTROL Database cleanup]** 워크플로에 의해 격리 목록에서 제거하거나 테이블에서 삭제할 수 있습니다.

**관련 항목:**
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [반송 메일 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)
