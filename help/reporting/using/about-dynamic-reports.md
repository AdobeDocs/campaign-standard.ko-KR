---
title: 동적 보고서 시작
description: 동적 보고서를 사용하여 변수 및 차원을 자유 형식 환경으로 끌어서 놓고 캠페인의 성공을 분석합니다.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: fc3b28f3-63f6-4edc-923d-c7eb7925d1b7
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 5%

---

# 동적 보고서 시작 {#about-dynamic-reports}

동적 보고는 사용자 정의 가능하고 실시간 보고서를 제공합니다. 프로필 데이터에 대한 액세스를 추가하여 열림 및 클릭과 같은 실용적인 이메일 캠페인 데이터 외에도 성별, 도시 및 연령 등의 프로필 차원별 인구 통계 분석을 지원합니다. 끌어서 놓기 인터페이스에서 데이터를 살펴보고 가장 중요한 고객 세그먼트에 대한 이메일 캠페인의 성과를 확인하고 수신자에게 미치는 영향을 측정할 수 있습니다.

>[!NOTE]
>
>관리 권한이 있거나 조직 단위가 **모두**&#x200B;로 설정된 사용자만 새 보고서를 만들거나 저장할 수 있습니다. 자세한 정보는 이 [섹션](../../administration/using/users-management.md)을 참조하십시오.

## 동적 보고서 액세스 {#accessing-dynamic-reports}

보고서에 액세스할 수 있는 항목:

* 맨 위 막대에서 **[!UICONTROL Reports]** 탭 또는 **[!UICONTROL Reports]** 카드를 선택하여 홈 페이지에서 모든 게재에 대한 보고서에 액세스합니다.

   ![](assets/campaign_reports_access.png)

* 각 프로그램, 캠페인 및 메시지에서 **Reports** 단추에서 **동적 보고서**&#x200B;를 클릭하여 게재와 관련된 보고서만 봅니다.

   ![](assets/campaign_reports_description.png)

특정 보고서는 게재 후 정보를 수집 및 처리하는 데 걸리는 시간에 따라 즉시 사용할 수 없습니다.

동적 보고서는 다음 두 가지 카테고리로 분류됩니다.

* **템플릿** - 다른 이름으로  **저장 옵션(** 프로젝트 > 다른 이름으로 **저장)을 사용하여 복사하여 수정할 수 있습니다.**)을 클릭하여 제품에서 사용할 수 있습니다.
* **사용자 지정 보고서** (파란색으로 식별됨)이며, Reporthome 페이지에서  **새** 프로젝트 만들기 단추를 클릭하여 직접 만들 수  **** 있습니다.

>[!NOTE]
>
>데이터는 조직 단위에 따라 필터링됩니다.

![](assets/dynamic_report_overview.png)

## 동적 보고 사용 계약 {#dynamic-reporting-usage-agreement}

동적 보고 사용 계약의 목적은 데이터 처리에 대한 팝업 동의로 작동하는 것입니다. 기본적으로 계약은 만 표시되며 관리 권한이 있는 사용자만이 수락하거나 거부할 수 있습니다.

다음 세 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL Ask me later]**: 나중에  **묻기를** 클릭하면 창이 24시간 동안 표시되지 않습니다. 계약에 동의하거나 거부하기 전까지 프로필 차원은 보고서에 표시되지 않으며 고객의 개인 식별 정보는 수집되거나 전송되지 않습니다.
* **[!UICONTROL Accept]**: 이 계약에 동의하면 Adobe Campaign에서 고객의 개인 식별 정보를 수집하고 이를 보고 또는 데이터 센터로 전송할 수 있도록 권한을 부여합니다.
* **[!UICONTROL Decline]**: 계약을 거절하면 프로필 차원이 보고서에 표시되지 않고 고객의 개인 식별 정보가 수집되거나 전송되지 않습니다. 이 경우 externalID는 여전히 수집되고 최종 사용자를 식별하는 데 사용됩니다.

아래 표에는 해당 지역에 따라 이 계약에 동의하면 수행되는 작업이 표시됩니다.

|  | 동적 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 미국 및 APAC(아시아 태평양) | **사용 가능한** 기능입니다. <br>미국 보고 센터로 푸시된 모든 기본 제공(예: 도시, 국가/지역, 주, 성별 및 세그먼트) 및 사용자 지정 프로필 정보. 프로필 차원에 대한 자세한 내용은 이 [page](../../reporting/using/list-of-components-.md)을 참조하십시오 | **사용 가능한** 기능입니다. <br>모든 기본 및 사용자 지정 프로필 필드와 Adobe Campaign Standard 이벤트 필드는 미국 데이터 센터에서 처리됩니다. |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한** 기능입니다. <br>EMEA 보고 센터로 푸시된 모든 기본 제공(예: 도시, 국가/지역, 주, 성별 및 세그먼트) 및 사용자 지정 프로필 정보. 프로필 차원에 대한 자세한 내용은 이 [page](../../reporting/using/list-of-components-.md)을 참조하십시오 | **기능 사용 가능.** <br>EMEA 데이터 센터에서 처리된 모든 기본 제공 및 사용자 지정 프로필 필드와 Adobe Campaign Standard 이벤트 필드입니다. <br>**[!UICONTROL Control data]**에는 Adobe I/O 등록 데이터와 미국 데이터 센터에 전송되어 저장되는 고객 최종 사용자 이벤트의 ID가 포함되어 있습니다. |

아래 표에는 해당 지역에 따라 이 계약을 거부한 후 발생하는 사항이 표시됩니다. 이 계약을 거절하더라도 게재 및 Microsoft Dynamics 365 통합에 대한 보고를 계속 사용할 수 있습니다.

| 지역 | 동적 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 미국 및 APAC(아시아 태평양) | **사용 가능한** 기능입니다. <br> ExternalID를 제외하고 미국 보고 센터로 푸시된 기본 및 사용자 지정 프로필 정보가 없습니다. | **사용 가능한** 기능입니다. <br>외부 ID 및 수신자 ID를 제외하고 미국 데이터 센터로 전송된 기본 또는 사용자 지정 프로필 필드가 없습니다. <br>미러 페이지 ID를 제외하고 미국 데이터 센터에서 처리된 모든 Adobe Campaign Standard 이벤트 필드입니다. <br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 이  [페이지](../../integrating/using/d365-acs-get-started.md)를 참조하십시오. |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한** 기능입니다. <br>ExternalID를 제외하고 EMEA 보고 센터로 푸시된 기본 및 사용자 지정 프로필 정보가 없습니다. | **기능 사용 가능.** <br>외부 ID 및 수신자 ID를 제외하고 EMEA 데이터 센터로 전송된 기본 또는 사용자 지정 프로필 필드가 없습니다. <br>미러 페이지 ID를 제외하고 EMEA 데이터 센터에서 처리된 모든 Adobe Campaign Standard 이벤트 필드입니다.  <br>**[!UICONTROL Control data]**에는 Adobe I/O 등록 데이터와 미국 데이터 센터에 전송되어 저장되는 고객 최종 사용자 이벤트의 ID가 포함되어 있습니다.<br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 이  [페이지](../../integrating/using/d365-acs-get-started.md)를 참조하십시오. |

이 선택 사항은 최종적이지 않으므로 항상 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**&#x200B;에서 **[!UICONTROL Enable PII data to be transferred to US region to use reporting on Profile data]**&#x200B;을 선택하여 변경할 수 있습니다.

값은 언제든지 변경할 수 있습니다. 값 1은 **[!UICONTROL Ask me later]**, 2 **[!UICONTROL Decline]** 및 3 **[!UICONTROL Accept]**&#x200B;에 해당합니다.

![](assets/pii_window_2.png)
