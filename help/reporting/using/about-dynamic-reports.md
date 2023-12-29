---
title: 동적 보고서 시작
description: 동적 보고서를 사용하여 변수 및 차원을 자유 형식 환경으로 드래그하여 놓고 캠페인의 성공을 분석합니다.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: fc3b28f3-63f6-4edc-923d-c7eb7925d1b7
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 2%

---

# 동적 보고서 시작 {#about-dynamic-reports}

Dynamic Reporting은 완전히 맞춤화가 가능한 실시간 보고서를 제공합니다. 프로필 데이터에 대한 액세스를 추가하여 열기 및 클릭과 같은 실용적인 이메일 캠페인 데이터 외에도 성별, 도시 및 연령 등의 프로필 차원별 인구 통계 분석을 활성화합니다. 드래그 앤 드롭 인터페이스에서 데이터를 탐색하고, 가장 중요한 고객 세그먼트에 대한 이메일 캠페인의 성과를 확인하고 수신자에게 미치는 영향을 측정할 수 있습니다.

>[!NOTE]
>
>관리 권한이 있거나 조직 단위가 로 설정된 사용자만 **모두** 새 보고서를 만들거나 저장할 수 있습니다. 자세한 정보는 이 [섹션](../../administration/using/users-management.md)을 참조하십시오.

## 동적 보고서 액세스 {#accessing-dynamic-reports}

보고서에 액세스할 수 있는 권한은 다음과 같습니다.

* 을(를) 선택하여 홈페이지에서 **[!UICONTROL Reports]** 상단 막대의 탭 또는 **[!UICONTROL Reports]** 모든 게재에 대한 보고서에 액세스하기 위한 카드.

  ![](assets/campaign_reports_access.png)

* 각 프로그램, 캠페인 및 메시지의 **보고서** 클릭하여 표시되는 단추 **동적 보고서** 게재와 관련된 보고서만 볼 수 있습니다.

  ![](assets/campaign_reports_description.png)

특정 보고서는 정보를 수집하고 처리하는 데 걸리는 시간에 따라 배달 후 즉시 사용할 수 없습니다.

동적 보고서는 다음 두 가지 범주로 나뉩니다.

* **템플릿**, 다음을 사용하여 복사하여 수정할 수 있음 **다른 이름으로 저장** 옵션(**프로젝트 > 다른 이름으로 저장..**)을 클릭하여 제품에서 사용할 수 있습니다.
* **사용자 정의 보고서** (파란색으로 표시됨) - 다음을 클릭하여 직접 만들 수 있음 **새 프로젝트 만들기** 단추 **보고서** 홈 페이지입니다.

>[!NOTE]
>
>데이터는 조직 단위에 따라 필터링됩니다.

![](assets/dynamic_report_overview.png)

## 동적 보고 사용 계약 {#dynamic-reporting-usage-agreement}

동적 보고 사용 계약의 목적은 데이터 처리에 대한 팝업 동의로 작동하는 것입니다. 기본적으로 계약은 표시만 되며 관리 권한이 할당된 사용자만 수락하거나 거부할 수 있습니다.

다음 세 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL Ask me later]**: 다음을 클릭: **나중에 묻기**, 창이 24시간 동안 표시되지 않습니다. 계약에 동의하거나 동의하지 않을 때까지 프로필 차원이 보고서에 표시되지 않으며 고객의 개인 식별 정보가 수집 또는 전송되지 않습니다.
* **[!UICONTROL Accept]**: 이 계약에 동의함으로써 귀하는 Adobe Campaign이 고객의 개인 식별 정보를 수집하고 이를 보고 또는 데이터 센터로 전송하도록 승인합니다.
* **[!UICONTROL Decline]**: 계약을 거부하면 프로필 차원이 보고서에 표시되지 않고 고객의 개인 식별 정보가 수집 또는 전송되지 않습니다. 이 경우 externalID는 계속 수집되고 최종 사용자를 식별하는 데 사용됩니다.

아래 표에는 지역에 따라 이 계약에 동의한 후 발생한 사항이 표시됩니다.

|  | 다이내믹 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 아메리카 및 APAC(아시아 태평양) | **사용 가능한 기능**. <br>미국 보고 센터에 푸시된 모든 기본 프로필(즉, 도시, 국가/지역, 주, 성별 및 연령 기준 세그먼트) 및 사용자 정의 프로필 정보. 프로필 차원에 대한 자세한 내용은 다음을 참조하십시오. [페이지](../../reporting/using/list-of-components-.md) | **사용 가능한 기능**. <br>모든 기본 및 사용자 정의 프로필 필드와 Adobe Campaign Standard 이벤트 필드는 미국 데이터 센터에서 처리됩니다. |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한 기능**. <br>즉시 사용 가능한 모든 정보(예: 도시, 국가/지역, 주, 성별 및 연령 기준 세그먼트) 및 사용자 정의 프로필 정보가 EMEA 보고 센터에 푸시됩니다. 프로필 차원에 대한 자세한 내용은 다음을 참조하십시오. [페이지](../../reporting/using/list-of-components-.md) | **기능을 사용할 수 있습니다.** <br>EMEA 데이터 센터에서 처리된 기본 및 사용자 지정 프로필 필드와 Adobe Campaign Standard 이벤트 필드. <br>**[!UICONTROL Control data]**미국 데이터 센터에 전송되고 저장된 고객 최종 사용자 이벤트의 Adobe I/O 등록 데이터 및 ID가 들어 있습니다. |

아래 표에는 지역에 따라 이 계약을 거절한 후 발생한 내용이 표시됩니다. 이 계약을 거부하더라도 게재 및 Microsoft Dynamics 365 통합에 대한 보고를 계속 사용할 수 있습니다.

| 지역 | 다이내믹 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 아메리카 및 APAC(아시아 태평양) | **사용 가능한 기능**. <br> ExternalID를 제외하고 기본 및 사용자 정의 프로필 정보가 미국 보고 센터로 푸시되지 않습니다. | **사용 가능한 기능**. <br>외부 ID 및 수신자 ID를 제외하고 기본 제공 또는 사용자 지정 프로필 필드가 미국 데이터 센터로 전송되지 않습니다. <br>미러 페이지 ID를 제외하고 미국 데이터 센터에서 처리된 모든 Adobe Campaign Standard 이벤트 필드. <br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../integrating/using/d365-acs-get-started.md). |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한 기능**. <br>ExternalID를 제외하고 기본 및 사용자 정의 프로필 정보가 EMEA 보고 센터로 푸시되지 않습니다. | **기능을 사용할 수 있습니다.** <br>외부 ID 및 수신자 ID를 제외하고 EMEA 데이터 센터로 전송된 바로 사용 가능한 또는 사용자 지정 프로필 필드가 없습니다. <br>미러 페이지 ID를 제외하고 EMEA 데이터 센터에서 처리된 모든 Adobe Campaign Standard 이벤트 필드.  <br>**[!UICONTROL Control data]**미국 데이터 센터에 전송되고 저장된 고객 최종 사용자 이벤트의 Adobe I/O 등록 데이터 및 ID가 들어 있습니다.<br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../integrating/using/d365-acs-get-started.md). |

이 선택은 최종적인 것이 아닙니다. 언제든지 을 선택하여 변경할 수 있습니다. **[!UICONTROL Enable PII data to be transferred to US region to use reporting on Profile data]** 위치: **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**.

값은 언제든지 변경할 수 있습니다. 값 1은 **[!UICONTROL Ask me later]**, 2 **[!UICONTROL Decline]** 및 3 **[!UICONTROL Accept]**.

![](assets/pii_window_2.png)
