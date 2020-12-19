---
solution: Campaign Standard
product: campaign
title: DM 기본 정보
description: Adobe Campaign DM 채널의 주요 특성을 알아봅니다.
audience: channels
content-type: reference
topic-tags: direct-mail
context-tags: delivery,directMailContent,back;deliveryCreation,wizard
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 98%

---


# DM 기본 정보{#about-direct-mail}

DM은 다이렉트 메일 공급자가 요구하는 파일을 개인화하고 생성할 수 있는 오프라인 채널입니다. DM을 통해 고객 여정의 온오프라인 채널을 혼합하여 운영할 수 있습니다.

>[!NOTE]
>
>이 기능은 선택 사항입니다. 사용권 계약을 확인하십시오. DM을 사용하려면 **[!UICONTROL Export]** 역할이 필요합니다. 관리자에게 문의하십시오.

온라인 채널을 통해 메시지(이메일, SMS, 모바일 앱 게재 등)를 만들고 Adobe Campaign에서 바로 대상자에게 보낼 수 있습니다. 하지만 오프라인 채널에서는 다릅니다. Adobe Campaign은 DM 게재 준비 시 타겟팅 프로필과 선택한 연락처 정보(예를 들면 우편 주소)가 있는 파일을 생성합니다. 그러면 이 파일을 DM 공급자에게 보내어 실제 전송을 처리하도록 할 수 있습니다.

다음 섹션에서는 일회성 DM 게재를 만들고 생성하는 방법에 대해 설명합니다. 또한 워크플로우에 DM 활동을 포함시켜 온라인 및 오프라인 채널을 결합하는 캠페인을 구성할 수도 있습니다. 자세한 내용은 [워크플로우](../../automating/using/get-started-workflows.md) 안내서를 참조하십시오.

Adobe Campaign의 사용자 프로세스는 다음과 같습니다.

1. 게재 만들기
1. 대상자 선택
1. 콘텐츠 정의
1. 연락 날짜 설정
1. 파일 생성

**관련 항목:**

* [사용 사례:이메일 및 DM 배달 연결](../../automating/using/coupling-email-direct-mail.md)

## 추천 {#recommendations}

### DM 공급자 {#direct-mail-providers}

우선 DM 공급자에게 연락하여 추천을 받아야 합니다. 통신을 개인화하여 대상자에게 보내려면 추출 파일에 어떤 프로필 정보를 포함해야 하는지를 확인합니다. 예를 들어 이름과 성, 우편 주소, 프로모션 코드 등이 필요할 있습니다. 여기에 해당하는 필드를 DM 콘텐츠의 [추출 정의](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) 탭에 추가합니다.

프로필 정보에 있는 **[!UICONTROL Address specified]** 상자를 선택했는지 확인하십시오. 이 옵션을 활성화하면 프로필이 타겟에 추가됩니다. 이 옵션을 활성화하지 않은 경우 준비 단계에서 유형화 규칙에 의해 프로필을 제외합니다([DM 만들기](../../channels/using/creating-the-direct-mail.md) 참조). 프로필을 가져올 때 이 필드를 업데이트하는 것을 잊지 마십시오.

![](assets/direct_mail_22.png)

### 우편 주소 {#postal-addresses}

추출 파일에 포함할 필드를 추가할 때, **[!UICONTROL Location]** 노드에서 우편 주소 필드를 사용할 수 있습니다. 

Adobe Campaign은 사전 정의 및 계산된 필드 세트를 제공합니다. 이는 가장 많이 쓰이는 우편 주소 표준에 따릅니다. 이 필드는 **[!UICONTROL Postal address]** 노드에서 사용할 수 있습니다.

주소는 기본적으로 최대 6줄을 포함할 수 있습니다. 첫 번째 계산 필드(**[!UICONTROL Line 1]**)에는 이름과 성, 두 번째 줄에는 우편 주소(도로명 등), 마지막 줄에는 우편 번호 및 구/군/시가 들어갑니다.

![](assets/direct_mail_23.png)
