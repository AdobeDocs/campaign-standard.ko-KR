---
title: 캠페인 활성 프로필
description: 고객 지표 및 활성 프로필에 액세스하는 방법 알아보기
feature: Profiles
role: User
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
source-git-commit: 0ae2501b5c3ecf6dc9562bb53b5354c52aff7323
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# 활성 프로필{#active-profiles}

**[!UICONTROL Customer metrics]** 보고서에서 활성 프로필 세부 정보에 액세스할 수 있습니다. 이 보고서는 Campaign 기능 관리자만 사용할 수 있습니다. 이 보고서에 액세스하려면 [사용자 인터페이스](../../start/using/interface-description.md#advanced-menu)의 왼쪽 상단에 있는 Adobe Campaign 아이콘을 클릭하고 **[!UICONTROL Administration > Customer metrics]**(으)로 이동하십시오.

![](assets/audience_customer_metrics.png)

이 보고서는 **[!UICONTROL Billing]** 기술 워크플로우에서 매월 생성되며 **활성 프로필**&#x200B;의 수를 표시합니다. [이 페이지](../../administration/using/technical-workflows.md)에서 기술 워크플로우에 대해 자세히 알아보세요.

&quot;프로필&quot;은 최종 고객, 잠재 고객 또는 잠재 고객을 나타내는 정보 레코드입니다. 지난 12개월 내에 모든 채널을 통해 Campaign 게재의 타겟이 된 프로필은 **활성**(으)로 간주됩니다.

계약에 따라 각 Campaign 인스턴스에는 특정 수의 활성 프로필이 제공됩니다. 구입한 활성 프로필 수에 대한 자세한 내용은 라이선스 계약을 참조하십시오.

![](assets/audience_active_profiles_list.png)



* 게재를 준비하는 동안 제외된 프로필(예: 유형화 규칙 또는 격리 메커니즘에 의해)은 고려되지 않습니다.

* 트랜잭션 메시지 수신자는 활성 프로필에 계산됩니다.

* 여러 게재에서 타겟팅한 프로필은 한 번만 카운트됩니다.

* 이 보고서는 정보용일 뿐이며, 청구에 직접적인 영향을 주지 않습니다.

페이지 하단에 타겟팅 차원이 각 타겟팅의 프로필 수와 함께 나열됩니다. 트랜잭션 메시지 수신자는 **익명** 차원에 연결되어 있습니다.

>[!NOTE]
>
>관리 사용자는 Campaign 컨트롤 패널에서 직접 인스턴스에 사용된 활성 프로필 수를 모니터링할 수도 있습니다. 자세한 내용은 [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html?lang=ko)를 참조하세요.
>
