---
solution: Campaign Standard
product: campaign
title: 캠페인 활성 프로필
description: 고객 지표 및 활성 프로파일에 액세스하는 방법 살펴보기
feature: 프로필
role: Business Practitioner
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
source-git-commit: d2fcf2ca22bb5fe3632280f922dfed0972f6eb09
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# 고객 지표 {#customer-metrics}

캠페인 기능 관리자는 **[!UICONTROL Administration > Customer metrics]**&#x200B;에서 **[!UICONTROL Customer metrics]** 보고서에 액세스할 수 있습니다.

![](assets/audience_active_profiles1.png)

이 보고서는 다음과 같이 표시됩니다.

* Experience Cloud ID
* IMS 조직 ID
* **활성 프로필 수**
* 인스턴스에서 사용할 수 있는 타깃팅 차원 목록

이 보고서는 매달 **[!UICONTROL Billing]** 기술 워크플로우에 의해 생성됩니다.

## 활성 프로필{#active-profiles}

계약에 따라 각 캠페인 인스턴스에는 특정 수의 활성 프로파일이 제공됩니다. 구입한 활성 프로파일 수에 대한 자세한 내용은 라이센스 계약을 참조하십시오.

>[!NOTE]
>
>관리자 사용자는 Campaign 컨트롤 패널에서 직접 인스턴스에 사용된 활성 프로필 수를 모니터링할 수도 있습니다. 자세한 내용은 [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html)를 참조하십시오.


&quot;프로필&quot;은 최종 고객, 잠재 고객 또는 리드를 나타내는 정보의 레코드입니다. 채널을 통해 지난 12개월 이내에 캠페인 배달에서 타깃팅된 프로필은 **활성**&#x200B;으로 간주됩니다. 배달 준비 동안(예: 유형 규칙 또는 격리 메커니즘에 의해) 제외된 프로파일도 고려되지 않습니다. 여러 게재에서 타깃팅된 프로필은 한 번만 카운트됩니다. 이 보고서는 단지 유익할 뿐이며, 대금 청구에 직접적인 영향을 주지 않습니다.

![](assets/audience_active_profiles2.png)

보고서 하단에는 각 타깃팅 차원에 대한 활성 프로필 목록이 표시됩니다. 지난 12개월 롤링 기간 동안 타깃팅된 활성 프로필 수를 표시합니다.

* **[!UICONTROL NmsRecipient]** 소스에는 Campaign Standard 프로필의 정보를 사용하여 연결된 모든 프로필이 포함되어 있습니다.

* 고객 **[!UICONTROL anonymous]** 소스는 캠페인 프로필과 관련이 없는 특정 정보(이메일 주소, 전화 번호)만 사용하여 타깃팅된 프로필 수를 표시합니다.
