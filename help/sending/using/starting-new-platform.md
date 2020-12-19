---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard으로 새 플랫폼 시작
description: Adobe Campaign Standard을 사용하여 도메인 및 IP 주소 명성을 유지하면서 새로운 플랫폼을 설정하는 방법을 알아봅니다.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 2%

---


# 새 플랫폼 시작{#starting-new-platform}

도메인과 IP 주소 평판 유지 관리가 중요합니다. 다음은 새 플랫폼을 설정하는 방법에 대한 몇 가지 조언입니다.

새 플랫폼에서 이메일을 보내는 것은 사용 내역이 없고 명성도 없기 때문에(보낸 IP가 이 용도로 사용되지 않은 경우) 민감한 단계입니다. ISP는 이메일을 보내는 데 전혀 사용되지 않은 IP 주소를 의심하기 때문에 갑자기 대량의 이메일 트래픽을 전송하기 시작합니다. 실제로 스팸은 감지하기 전에 &quot;알 수 없는&quot; IP 주소(에 추가되지 않은 주소)를 사용하여 가장 많은 메시지 수를 차단 목록 전송합니다.

제작 단계가 시작될 때 출력 측면에서 운영 속도에 도달하는 것을 기대할 수 없습니다. 또한, ISP가 보내는 주소를 막고 나머지 시작 단계를 심각하게 훼손할 수 있으므로 이 속도로 메시지를 전송하지 않아야 합니다.

플랫폼을 시작하는 것은 처음 주소 목록을 사용할 때 자주 발생하여 완전히 자격이 없을 수 있습니다. 잘못된 주소 또는 허니포트 주소로 보내는 경우 플랫폼의 이름이 낮아지는 데 도움이 됩니다.
* 잘못된 주소 목록이 있는 경우 처음 보내기 전에 검역표(**[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** > **[!UICONTROL Addresses]**)로 가져오는 것이 좋습니다. 자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform)을 참조하십시오.
* 동일한 경우 잘못된 주소를 요청하려는 경우, 플랫폼의 이름이 설정되고 시간이 지남에 따라 잘못된 주소의 사용을 &quot;희석하기&quot;하기 위해 비트별로 비트 전송되면 이 작업을 수행하는 것이 훨씬 좋습니다.

시작할 때 따라야 할 원칙을 요약하려면:
* **Adobe** 에서 보낸 이메일 캠페인과 관련된 캠페인과 함께 작동하도록 전용 하위 도메인을 구성합니다.
* **잘못된/비활성 주소를 격리 테이블로**  가져옵니다(이 정보가 있는 경우).
* **전달** 범위 제한(기술 설정:mtachilds 수 제한).
* **전송된 볼륨을 점진적으로 증가시킵니다**.처음부터 전체 데이터베이스를 대상으로 하지 않고 전송할 때마다 목록의 일부를 추가로 추가하십시오. 따라서 유효하지 않은 주소의 전체 비율을 줄이면서 각 단계에서 볼륨을 증가시킬 수 있습니다.
* **정기적으로** 메시지 보내기:산발적으로 대형 캠페인보다는 정기적으로 작은 샷을 보내는 것이 좋습니다.
* **배달 보고서를 자세히 모니터링합니다**.오류 표시기가 높으면 기술 설정이 잘못 구성되었음을 의미합니다.
