---
title: DM 기본 정보
description: Adobe Campaign에서 DM 채널의 주요 특성을 살펴볼 수 있습니다.
page-status-flag: never-activated
uuid: 24add992-2efe-4b73-81c9-cda3e921ab16
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: e1fbf39c-9c30-493c-8322-9c71e18ce98c
context-tags: delivery,directMailContent,back;deliveryCreation,wizard
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: efb1f14e0094e200d186423f98bfad65d25cfab2

---


# DM 기본 정보{#about-direct-mail}

DM은 DM 제공업체가 요구하는 파일을 개인화하고 생성할 수 있는 오프라인 채널입니다. 고객 여정의 온라인 및 오프라인 채널을 혼합할 수 있습니다.

>[!NOTE]
>
>이 기능은 선택 사항입니다. 사용권 계약을 확인하십시오. DM을 사용하려면 **[!UICONTROL Export]** 역할이 필요합니다. 관리자에게 문의하십시오.

온라인 채널을 통해 메시지(이메일, SMS, 모바일 앱 전달 등)를 만들 수 있습니다. Adobe Campaign에서 바로 고객에게 보낼 수 있습니다. 오프라인 채널에서는 다릅니다. Direct Mail 배달을 준비하면 Adobe Campaign은 타깃팅된 모든 프로필 및 선택한 연락처 정보(예: 우편 주소)를 포함하는 파일을 생성합니다. 그러면 이 파일을 다이렉트 메일 제공업체에 보낼 수 있습니다. 이 제공자는 실제 전송을 처리합니다.

다음 섹션에서는 DM(One-Shot Direct Mail) 배달을 만들고 생성하는 방법에 대해 설명합니다. 또한 워크플로우에 직접 메일 활동을 포함하여 온라인 및 오프라인 채널을 결합하는 캠페인을 구성할 수도 있습니다. 자세한 내용은 워크플로우 [안내서를 참조하십시오](../../automating/using/workflow-data-and-processes.md) .

Adobe Campaign의 사용자 프로세스는 다음과 같습니다.

1. 배달 만들기
1. 대상자 선택
1. 컨텐츠 정의
1. 연락처 날짜 설정
1. 파일 생성

## Recommendations {#recommendations}

### DM 공급자 {#direct-mail-providers}

우선 다이렉트 메일 제공업체에 연락하여 추천을 수집해야 합니다. 추출 파일에 포함시켜야 하는 프로필 정보를 확인하여 개인화하여 고객에게 보낼 수 있습니다. 예를 들어, 이름과 성, 우편 주소, 프로모션 코드 등이 있습니다. 이러한 필드는 DM 컨텐츠의 추출 [정의](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) 탭에서 추가할 필드입니다.

프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택했는지 확인합니다. 이 옵션을 활성화하면 프로필이 대상에 추가됩니다. 준비 단계 동안 유형 지정 규칙에 의해 제외되지 않습니다(DM [만들기](../../channels/using/creating-the-direct-mail.md)참조). 프로필을 가져오는 동안 이 필드를 업데이트하는 것을 잊지 마십시오.

![](assets/direct_mail_22.png)

### 우편 주소 {#postal-addresses}

추출 파일에 포함할 필드를 추가하면 **[!UICONTROL Location]** 노드에서 우편 주소 필드를 사용할 수 있습니다.

Adobe Campaign은 가장 일반적인 우편 주소 정규화를 따르는 미리 정의된 계산된 필드 세트를 제공합니다. 이 필드는 **[!UICONTROL Postal address]** 노드에서 사용할 수 있습니다.

주소는 기본적으로 최대 6개의 줄을 포함할 수 있습니다.첫 번째 계산된 필드(**[!UICONTROL Line 1]** 이름과 성 포함, 다음 줄에는 우편 주소(도로 등)가 들어 있으며, 마지막 줄에는 우편 번호 및 우편 번호 및 시/도가 포함되어 있습니다.

![](assets/direct_mail_23.png)

