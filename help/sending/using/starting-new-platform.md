---
title: Adobe Campaign Standard에서 새로운 플랫폼 시작
description: Adobe Campaign Standard에서 도메인 및 IP 주소 명성을 유지하면서 새로운 플랫폼을 설정하는 방법을 살펴볼 수 있습니다.
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
source-git-commit: 1f15e28bed22e3defb29f16875fcf4c07f4af5a3
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 2%

---


# 새 플랫폼 시작{#starting-new-platform}

도메인 및 IP 주소 평판 유지 관리가 중요합니다. 다음은 새 플랫폼을 설정하는 몇 가지 조언입니다.

새로운 플랫폼에서 이메일을 보내는 것은 플랫폼이 사용 내역이 없고 명성도 없기 때문에(전송 IP가 이 용도로 사용되지 않은 경우) 민감한 단계입니다. ISP는 원래 이메일을 보내는 데 전혀 사용되지 않은 IP 주소를 의심하기 때문에 갑자기 많은 양의 이메일 트래픽이 전송되기 시작합니다. 실제로 스팸은 검색하기 전에 &quot;알 수 없는&quot; IP 주소(이전에 차단 목록에 추가된 한 번도 없는 주소)를 사용하여 가장 많은 수의 메시지를 전송합니다.

제작 단계에서 출력 측면에서 운영 속도에 도달하는 것은 기대할 수 없습니다. 또한, ISP가 전송 주소를 막고 나머지 시작 단계를 심각하게 훼손할 수 있으므로 이러한 속도로 메시지를 전송하지 마십시오.

플랫폼 시작은 처음 주소 목록을 사용할 때 일어나며, 이것은 완전히 검증되지 않을 수 있습니다. 잘못된 주소 또는 허니포트 주소로 보내면 플랫폼의 명성이 낮아집니다.
* 잘못된 주소 목록이 있는 경우 처음 보내기 전에 검역 표(**[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** > **[!UICONTROL Addresses]**)로 가져오는 것이 좋습니다. 자세한 내용은 이 [섹션](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform)을 참조하십시오.
* 동일한 경우 잘못된 주소를 요청하려는 경우, 플랫폼의 이름이 설정되고 시간이 지남에 따라 잘못된 주소의 사용을 &quot;희석시키기&quot;위해 비트별로 비트 단위로 설정되면 이 방법을 사용하는 것이 더 좋습니다.

시작할 때 따라야 할 원칙을 요약하려면:
* **Adobe에서 보낸 이메일 캠페인에만 해당하는 전용 하위** 도메인을 Adobe에 위임합니다.
* **잘못된/비활성 주소를 검역 테이블로** 가져옵니다(이 정보가 있는 경우).
* **전달 처리량** 비율 제한(기술 설정:일치 수 제한).
* **전송된 볼륨을 점진적으로 증가시킵니다**.처음부터 전체 데이터베이스를 대상으로 하지 않고 전송할 때마다 목록의 일부를 추가로 추가하십시오. 따라서 각 단계에서 볼륨을 증가시키고 잘못된 주소의 전체 속도를 줄일 수 있습니다.
* **정기적으로**&#x200B;메시지 전송:산발적으로 대형 캠페인보다는 작은 샷을 정기적으로 보내는 것이 좋다.
* **배달 보고서를 자세히 모니터링합니다**.오류 표시기가 높으면 기술 설정이 잘못 구성되었음을 의미합니다.
