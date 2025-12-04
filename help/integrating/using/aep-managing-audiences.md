---
title: Adobe Experience Platform 대상자 관리
description: Campaign Standard 내에서 Adobe Experience Platform을 관리하는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 2f6c5cc6-0634-4418-a2ee-e1c133d9cbd2
hide: true
hidefromtoc: true
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Adobe Experience Platform 대상자 관리 {#about-audiences}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타 버전이며, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

## Adobe Experience Platform 대상자 액세스

Adobe Experience Platform 세그먼트 빌더에 액세스하려면 Campaign Standard 홈 페이지의 **[!UICONTROL Audiences]** 카드(또는 헤더의 **[!UICONTROL Audiences]** 링크)로 이동한 다음 **[!UICONTROL Adobe Experience Platform]** 환경을 선택하십시오.

![](assets/aep_audiences_access.png)

먼저 기존 Adobe Experience Platform 세그먼트에 액세스하여 추가 편집할 수 있는 Adobe Experience Platform 세그먼트 목록 페이지로 이동합니다.

원하는 Adobe Experience Platform 세그먼트를 찾는 데 도움이 되는 검색 창과 필터를 사용할 수 있습니다.

![](assets/aep_audiences_list.png)

## Adobe Experience Platform 대상자 만들기

Campaign Standard에서 직접 Adobe Experience Platform 대상자를 만들려면 다음 단계를 수행하십시오.

1. Adobe Experience Platform 세그먼트 목록 페이지에서 오른쪽 모서리에 있는 **[!UICONTROL New audience]** 단추를 클릭합니다.

   ![](assets/aep_audiences_creation_create.png)

1. 이제 세그먼트 빌더가 작업 공간에 표시됩니다. 이를 통해 최종적으로 대상자를 만드는 데 사용될 Adobe Experience Platform의 데이터를 사용하여 세그먼트를 작성할 수 있습니다.

1. 오른쪽 창에서 세그먼트 이름을 지정하고 설명을 입력합니다(선택 사항).

   ![](assets/aep_audiences_creation_edit_name.png)

1. 세그먼트를 만들려면 이 세그먼트에 대한 마케팅 목적에 일치하는 **병합 정책**&#x200B;을(를) 선택해야 합니다.

   설정 창에서 플랫폼 기본 병합 정책을 선택합니다. 병합 정책에 대한 자세한 내용은 [세그먼트 빌더 사용 안내서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)의 전용 섹션을 참조하십시오.

   ![](assets/aep_audiences_mergepolicy.png)

1. 대상자에서 검색할 프로필을 식별하는 규칙을 정의합니다.

   이렇게 하려면 왼쪽 창에서 작업 영역으로 원하는 특성 및/또는 이벤트를 끌어서 해당 규칙을 정의한 다음 **[!UICONTROL Create segment]** 단추를 클릭하여 세그먼트를 저장합니다([세그먼트 빌더 사용](../../integrating/using/aep-using-segment-builder.md) 참조).

   ![](assets/aep_audiences_creation_query.png)

이제 대상을 활성화할 준비가 되었습니다. 캠페인의 대상으로 사용할 수 있습니다([Adobe Experience Platform 대상 타기팅](../../integrating/using/aep-targeting-audiences.md) 참조).

## 대상자 편집

대상자를 편집하려면 대상자를 열고 필요에 따라 세그먼트 빌더 인터페이스 내에서 규칙을 수정하십시오([세그먼트 빌더 사용](../../integrating/using/aep-using-segment-builder.md) 참조).

변경이 완료되면 **[!UICONTROL Save segment]** 단추를 클릭하여 대상자를 업데이트합니다.

![](assets/aep_audiences_editing.png)
