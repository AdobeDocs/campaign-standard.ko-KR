---
title: 활성 프로필
description: 고객 지표에 대한 전용 보고서에 액세스하고 캠페인 데이터베이스에서 활성 프로파일을 시각화할 수 있습니다.
page-status-flag: never-activated
uuid: ee8ac493-c297-49ca-aed4-3976d8a685a4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: e029213f-0b65-41b1-8adf-34fa813b0c70
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1147c4512b1485ae5d927a32970adcd41b540e7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# 활성 프로필{#active-profiles}

Adobe Campaign은 활성 프로필 수를 표시하는 보고서를 제공합니다. 이 보고서는 단지 유익할 뿐, 대금 청구에는 직접적인 영향을 주지 않습니다. 관리자만 아래 이 보고서에 액세스할 수 있습니다 **[!UICONTROL Administration > Customer metrics]**.

![](assets/audience_active_profiles1.png)

>[!NOTE]
>
>AWS에서 호스팅되고 빌드 10368의 Campaign Standard을 사용하는 경우 Campaign 컨트롤 패널에서 직접 인스턴스에 사용된 활성 프로필의 수를 모니터링할 수도 있습니다. For more on this, refer to the [Control Panel documentation](https://docs.adobe.com/content/help/en/control-panel/using/performance-monitoring/active-profiles-monitoring.html).
>
>활성 프로필 지표는 **마케팅 인스턴스에만 사용할 수 있으며 관련** 지표입니다. MID(mid 소싱) 및 RT(메시지 센터/실시간 메시징) 인스턴스를 의미하는 실행 인스턴스에는 적용되지 않으며 사용할 수 없습니다.


배달 준비 중 제외된 프로필(분류 규칙, 검역소, 제어 그룹)은 고려되지 않습니다. 여러 게재에서 타깃팅된 프로필은 한 번만 카운트됩니다. 보고서 하단에는 각 타깃팅 차원에 대한 활성 프로필 목록이 있습니다.

이 보고서는 **[!UICONTROL Billing]** 기술 워크플로우로 매월 생성됩니다. 여기에는 지난 12개월 롤링 기간 동안 타깃팅된 활성 프로필 수가 포함됩니다.

배달 준비 중 제외된 프로필(분류 규칙, 격리)은 고려되지 않습니다. 또한 여러 게재에서 타깃팅된 프로필은 한 번만 카운트됩니다.

![](assets/audience_active_profiles2.png)

보고서 하단에는 청구 워크플로우에 의해 처리된 활성 프로파일 목록이 표시됩니다.

* 소스에는 **[!UICONTROL NmsRecipient]** Campaign Standard 프로필의 정보를 사용하여 접촉한 모든 고객이 포함됩니다.

* 반면에 특정 정보(이메일 주소, 전화 번호)만 사용하여 타깃팅된 고객은 자신의 캠페인 프로필과 관련이 없는 **[!UICONTROL anonymous]** 소스로 이동됩니다.
