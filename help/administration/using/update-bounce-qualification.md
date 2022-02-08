---
title: ISP 중단 후 바운스 자격 업데이트
description: ISP 중단 후 반송 조건을 업데이트하는 방법을 알아봅니다.
audience: delivery
hidefromtoc: true
exl-id: b06e9009-70c7-459f-8a9f-d5b7020d662f
source-git-commit: bfba6b156d020e8d2656239e713d2d24625bda54
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 4%

---

# ISP 중단 후 바운스 자격 업데이트 {#update-bounce-qualification.md}

최신 버전의 Campaign을 실행하지 않는 경우 이 섹션이 적용될 수 있습니다. Adobe Campaign 담당자에게 문의하십시오.

## 컨텍스트

ISP가 중단되는 경우, Campaign을 통해 전송된 이메일을 수신자에게 전달할 수 없습니다. 이 이메일은 반송 행위로 잘못 표시될 것입니다.

2020년 12월, Gmail의 글로벌 문제로 인해 유효한 Gmail 이메일 주소로 전송된 일부 이메일 메시지가 바운스 다음 응답이 있는 Gmail 서버에 의해 잘못된 이메일 주소로 잘못 바운스되었습니다. *&quot;550-5.1.1 연락하려는 이메일 계정이 없습니다.&quot;*

Google은 이 문제를 일으킨 Gmail의 정전과 혼란을 12월 14일 오전 6시 55분에 시작했고 12월 15일 동부시간 오후 6시 9분에 끝났다고 발표했습니다. Adobe의 데이터 분석은 또한 12월 16일 오전 2시 6분에 EST에서 Gmail 바운스의 매우 짧은 스파이크를 보여주었으며, 대부분은 12월 15일 오후 2시 ~ 오후 6시 30분 사이에 발생합니다.

>[!NOTE]
>
>에서 Google 작업 공간 상태 대시보드를 확인할 수 있습니다 [이 페이지](https://www.google.com/appsstatus#hl=en&amp;v=status).


표준 바운스 처리 논리에 따라 Adobe Campaign은 이러한 수신자를 **[!UICONTROL Status]** 설정 **[!UICONTROL Quarantine]**. 이 문제를 해결하려면 이러한 수신자를 찾아 제거하거나 수신자를 변경하여 Campaign에서 격리 테이블을 업데이트해야 합니다 **[!UICONTROL Status]** to **[!UICONTROL Valid]** 야간 정리 워크플로우가 해당 워크플로우가 제거합니다.

이 Gmail 문제의 영향을 받은 수신자를 찾거나 다른 ISP에서 이 문제가 다시 발생하는 경우 아래 지침을 참조하십시오.

## 업데이트할 프로세스

격리 테이블에서 쿼리를 실행하여 중단의 영향을 받을 수 있는 모든 Gmail(또는 기타 ISP) 수신자를 필터링하여 격리 목록에서 제거하고 향후 Campaign 이메일 게재에 포함할 수 있습니다.

사고 기간에 따라 이 쿼리에 대한 권장 지침은 아래에 나와 있습니다.

>[!IMPORTANT]
>
>이 날짜/시간은 동부 표준 시간대(EST)를 기반으로 합니다. 인스턴스의 시간대에 맞게 조정하십시오.

에서 SMTP 바운스 응답 정보가 있는 Campaign 인스턴스의 경우 **[!UICONTROL Error text]** 격리 목록 필드:

* **오류 텍스트(격리 텍스트)** 에는 &quot;550-5.1.1에 연결하려고 한 이메일 계정이 존재하지 않음&quot; AND가 포함되어 있습니다 **오류 텍스트(격리 텍스트)** contains &quot;support.google.com&quot; **
* **업데이트 상태(@lastModified)** 12/14/2020 6 이상:55:오전 00시
* **업데이트 상태(@lastModified)** 12/16/2020 6 이상:00:오전 00시

영향을 받는 수신자 목록이 있으면 해당 수신자를 다음 상태로 설정할 수 있습니다. **[!UICONTROL Valid]** 따라서 다음을 통해 격리 목록에서 제거됩니다 **[!UICONTROL Database cleanup]** 워크플로우나 테이블에서 삭제할 수도 있습니다.

**관련 항목:**
* [게재 실패 이해](../../sending/using/understanding-delivery-failures.md)
* [반송 메일 조건](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)
