---
title: 매핑 활성화
description: 데이터 매핑을 활성화하는 방법 알아보기
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: d7ca0de6-7f7b-4e31-877c-909d962c5f53
hide: true
hidefromtoc: true
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# 매핑 활성화 {#mapping-activation}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

매핑 정의가 완료되면 매핑을 게시할 수 있습니다. 배포 단계 후에 Campaign Standard과 Adobe Experience Platform 간의 데이터 복제가 자동으로 시작됩니다. 언제든지 **[!UICONTROL Stop]** 단추를 클릭하여 복제를 중지할 수 있습니다.

매핑 수정 사항에 따라 모든 레코드를 Adobe Experience Platform에 다시 전송하도록 선택할 수 있습니다.

![](assets/aep_publishmapping.png)

배포 타일에서 게시 로그 및 내보내기 로그에 액세스할 수 있습니다.

![](assets/aep_publog.png)

**[!UICONTROL Export jobs]** 탭에서 게시된 매핑의 내보내기 작업을 모니터링할 수 있습니다.

![](assets/aep_jobstatus.png)

모든 데이터 내보내기 작업을 모니터링하려면 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** 메뉴로 이동하십시오.

![](assets/aep_statusmapping.png)

데이터 수집 작업 상태는 다음과 같습니다.

* **[!UICONTROL Created]**: 데이터 수집 작업이 만들어지고 데이터 수집이 진행 중입니다.
* **[!UICONTROL Failed]**: 데이터 수집 작업이 실패했습니다. 사유 필드는 실패 이유를 설명합니다. 실패는 일시적이거나 영구적일 수 있습니다. 일시적인 오류의 경우 구성된 간격 후에 새 수집 작업이 생성됩니다. 문제 해결을 위한 첫 번째 단계로 사용자는 실패의 원인 필드를 확인할 수 있습니다. 원인이 사용자를 Adobe Experience Platform UI로 리디렉션하는 경우 사용자는 Adobe Experience Platform에 로그인하고 데이터 세트에서 배치 상태를 확인하여 정확한 실패 이유를 확인할 수 있습니다.
* **[!UICONTROL Uploaded]**: 먼저 Adobe Experience Platform에서 일괄 처리가 만들어지고 데이터가 일괄 처리로 수집됩니다. 배치 ID 필드는 Adobe Experience Platform에서 배치에 대한 배치 ID를 보여줍니다. Adobe Experience Platform은 배치에 대한 사후 유효성 검사도 수행합니다. 배치는 먼저 Adobe Experience Platform이 사후 유효성 검사 단계를 완료할 때까지 업로드된 것으로 표시됩니다. 작업은 업로드 후 배치 상태에 대해 Adobe Experience Platform을 계속 폴링합니다. 배치는 Adobe Experience Platform에서 실패 또는 성공 상태 사후 유효성 검사로 이동할 수 있습니다.
* **[!UICONTROL Success]**: 일괄 처리를 Adobe Experience Platform에 업로드한 후 구성된 간격 후에 작업 상태(플랫폼에서 유효성 검사 후)를 확인합니다. &#39;성공&#39; 상태에서 Adobe Experience Platform의 성공적인 데이터 수집을 확인했습니다.

경우에 따라 매핑을 게시할 때 아래에 유효성 검사 오류가 표시될 수 있습니다.

![](assets/aep_datamapping_ccpa.png)

이 문제는 사용 중인 XDM 스키마가 개인 정보 관리와 관련된 최신 XDM 필드로 업데이트되지 않았으며 더 이상 사용되지 않는 &quot;ccpa&quot; XDM 필드를 포함할 때 발생합니다.

XDM 스키마를 업데이트하려면 다음 단계를 따르십시오.

1. XDM 매핑 페이지에 있는 링크를 사용하여 Adobe Experience Platform의 데이터 세트로 이동합니다.

1. XDM 스키마로 이동합니다.

1. **[!UICONTROL Profile Privacy]** mixin을 스키마에 추가합니다.

   ![](assets/aep_datamapping_privacyfield.png)

1. 스키마를 저장한 다음 매핑 게시를 다시 시도하십시오. 이제 발행물이 전달됩니다.

   ![](assets/aep_save_mapping.png)
