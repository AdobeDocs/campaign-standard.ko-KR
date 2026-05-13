---
title: 동적 보고서 시작하기
description: 동적 보고서를 사용하여 변수 및 차원을 자유 형식 환경으로 드래그하여 놓고 캠페인의 성공을 분석합니다.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: fc3b28f3-63f6-4edc-923d-c7eb7925d1b7
TQID: https://experienceleague.adobe.com/L392oFEzYUkSajzO3Gi7gjWLmDrpbOhW24k1OXFmoRc
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616aid: c309ee4e-82e4-4f7e-b608-ef345678c34eid: c5474392-5419-4296-9e41-f6f4ce4f6e9b
subfeature_v2: id: ca3c1dd6-bdd2-41a9-bc5a-e35f5cca9e63
role_v2: id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 831
ht-degree: 10%

---

# 동적 보고서 시작하기 {#about-dynamic-reports}

Dynamic Reporting은 완전히 맞춤화가 가능한 실시간 보고서를 제공합니다. 이 기능은 프로필 데이터에 대한 액세스를 추가하여 열기 및 클릭과 같은 기능적 이메일 캠페인 데이터 외에도 성별, 도시, 연령과 같은 프로필 차원별로 인구통계 분석을 지원합니다. 끌어서 놓기 인터페이스에서 데이터를 살펴보고 가장 중요한 고객 세그먼트에 대한 이메일 캠페인의 성과를 확인하고 수신자에게 미치는 영향을 측정할 수 있습니다.

>[!NOTE]
>
>관리 권한이 있거나 조직 단위가 **모두**(으)로 설정된 사용자만 새 보고서를 만들거나 저장할 수 있습니다. 자세한 정보는 이 [섹션](../../administration/using/users-management.md)을 참조하십시오.

## 동적 보고서 액세스 {#accessing-dynamic-reports}

보고서에 액세스할 수 있는 권한은 다음과 같습니다.

* 홈페이지에서 상단 막대 또는 **[!UICONTROL Reports]** 카드에서 **[!UICONTROL Reports]** 탭을 선택하여 모든 게재에 대한 보고서에 액세스합니다.

  ![](assets/campaign_reports_access.png)

* 각 프로그램, 캠페인 및 메시지에서 **동적 보고서**&#x200B;를 클릭하여 **보고서** 단추를 클릭하여 게재와 관련된 보고서만 봅니다.

  ![](assets/campaign_reports_description.png)

특정 보고서는 정보를 수집하고 처리하는 데 걸리는 시간에 따라 배달 후 즉시 사용할 수 없습니다.

동적 보고서는 다음 두 가지 범주로 나뉩니다.

* **템플릿**, **다른 이름으로 저장** 옵션(**프로젝트 > 다른 이름으로 저장..**)을 사용하여 복사하여 수정할 수 있음 템플릿에서 사용할 수 있습니다.
* **보고서** 홈 페이지에서 **새 프로젝트 만들기** 단추를 클릭하여 직접 만들 수 있는 **사용자 지정 보고서**(파란색으로 식별됨).

>[!NOTE]
>
>데이터는 조직 단위에 따라 필터링됩니다.

![](assets/dynamic_report_overview.png)

## 동적 보고 사용 계약 {#dynamic-reporting-usage-agreement}

동적 보고 사용 계약의 목적은 데이터 처리에 대한 팝업 동의로 작동하는 것입니다. 기본적으로 계약은 표시만 되며 관리 권한이 할당된 사용자만 수락하거나 거부할 수 있습니다.

다음 세 가지 옵션을 사용할 수 있습니다.

* **[!UICONTROL Ask me later]**: **나중에 묻기**&#x200B;를 클릭하면 24시간 동안 창이 표시되지 않습니다. 계약에 동의하거나 동의하지 않을 때까지 프로필 차원이 보고서에 표시되지 않으며 고객의 개인 식별 정보가 수집 또는 전송되지 않습니다.
* **[!UICONTROL Accept]**: 이 계약에 동의하면 Adobe Campaign에서 고객의 개인 식별 정보를 수집하고 이를 보고 또는 데이터 센터로 전송하는 권한을 부여합니다.
* **[!UICONTROL Decline]**: 계약을 거부하면 프로필 차원이 보고서에 표시되지 않고 고객의 개인 식별 정보가 수집되거나 전송되지 않습니다. 이 경우 externalID는 계속 수집되고 최종 사용자를 식별하는 데 사용됩니다.

아래 표에는 지역에 따라 이 계약에 동의한 후 발생한 사항이 표시됩니다.

|  | 동적 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 아메리카 및 APAC(아시아 태평양) | **사용 가능한 기능**. <br>미국 보고 센터에 푸시된 모든 기본 프로필(예: 도시, 국가/지역, 주, 성별 및 연령 기준 세그먼트) 및 사용자 지정 프로필 정보. 프로필 차원에 대한 자세한 정보는 이 [페이지](../../reporting/using/list-of-components.md)를 참조하세요. | **사용 가능한 기능**. <br>모든 기본 및 사용자 지정 프로필 필드와 Adobe Campaign Standard 이벤트 필드가 미국 데이터 센터에서 처리됩니다. |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한 기능**. <br>EMEA 보고 센터에 푸시된 모든 기본 제공(예: 도시, 국가/지역, 주, 성별 및 연령 기준 세그먼트) 및 사용자 지정 프로필 정보. 프로필 차원에 대한 자세한 정보는 이 [페이지](../../reporting/using/list-of-components.md)를 참조하세요. | **기능을 사용할 수 있습니다.** <br>EMEA 데이터 센터에서 처리된 기본 및 사용자 지정 프로필 필드와 Adobe Campaign Standard 이벤트 필드입니다. Adobe I/O 등록 데이터와 미국 데이터 센터에 전송되고 저장된 고객 최종 사용자 이벤트의 ID가 포함된 <br>**[!UICONTROL Control data]**. |

아래 표에는 지역에 따라 이 계약을 거절한 후 발생한 내용이 표시됩니다. 이 계약을 거부하더라도 게재 및 Microsoft Dynamics 365 통합에 대한 보고는 계속 사용할 수 있습니다.

| 지역 | 동적 보고 | Microsoft Dynamics 365 커넥터 |
|---|---|---|
| 아메리카 및 APAC(아시아 태평양) | **사용 가능한 기능**. <br> ExternalID를 제외하고 기본 및 사용자 정의 프로필 정보가 미국 보고 센터로 푸시되지 않습니다. | **사용 가능한 기능**. <br>외부 ID와 받는 사람 ID를 제외하고 기본 프로필 필드나 사용자 지정 프로필 필드를 미국 데이터 센터로 보내지 않습니다. <br>미러 페이지 ID를 제외하고 미국 데이터 센터에서 처리된 모든 Adobe Campaign Standard 이벤트 필드. <br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 이 [페이지](../../integrating/using/d365-acs-get-started.md)를 참조하세요. |
| EMEA(유럽 중동 및 아프리카) | **사용 가능한 기능**. <br>기본 및 사용자 지정 프로필 정보가 ExternalID를 제외하고 EMEA 보고 센터로 푸시되지 않았습니다. | **기능을 사용할 수 있습니다.** <br>외부 ID와 받는 사람 ID를 제외하고 기본 프로필 또는 사용자 지정 프로필 필드를 EMEA 데이터 센터로 보내지 않습니다. <br>미러 페이지 ID를 제외한 모든 Adobe Campaign Standard 이벤트 필드가 EMEA 데이터 센터에서 처리되었습니다. <br>**[!UICONTROL Control data]**- Adobe I/O 등록 데이터와 미국 데이터 센터에서 전송 및 저장된 고객 최종 사용자 이벤트의 ID가 들어 있습니다.<br>Microsoft Dynamics 365 통합에 대한 자세한 내용은 이 [페이지](../../integrating/using/d365-acs-get-started.md)를 참조하세요. |

이 선택은 최종적인 것이 아닙니다. **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**&#x200B;에서 **[!UICONTROL Enable PII data to be transferred to US region to use reporting on Profile data]**&#x200B;을(를) 선택하여 언제든지 변경할 수 있습니다.

값은 언제든지 변경할 수 있습니다. 값 1은 **[!UICONTROL Ask me later]**, 2 **[!UICONTROL Decline]** 및 3 **[!UICONTROL Accept]**&#x200B;에 해당합니다.

![](assets/pii_window_2.png)
