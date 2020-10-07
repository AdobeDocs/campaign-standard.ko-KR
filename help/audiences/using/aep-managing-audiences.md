---
title: Adobe Experience Platform 대상자 관리
description: Campaign Standard에서 Adobe Experience Platform을 관리하는 방법을 살펴보십시오.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 3%

---


# Adobe Experience Platform 대상자 관리 {#about-audiences}

>[!IMPORTANT]
>
>대상 대상 서비스는 현재 베타 버전이며 예고 없이 수시로 업데이트됩니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스 권한을 원하는 경우 Adobe 고객 지원 센터에 문의하십시오.

## Adobe Experience Platform 대상 액세스

Adobe Experience Platform 세그먼트 빌더에 액세스하려면 Campaign Standard 홈 페이지(또는 헤더의 **[!UICONTROL Audiences]** 링크)의 **[!UICONTROL Audiences]** 카드로 이동한 다음 **[!UICONTROL Adobe Experience Platform]** 환경을 선택합니다.

![](assets/aep_audiences_access.png)

먼저 Adobe Experience Platform 세그먼트 목록 페이지로 이동합니다. 이 페이지에서 기존 Adobe Experience Platform 세그먼트를 더 자세히 편집할 수 있습니다.

검색 막대와 필터를 사용하여 원하는 Adobe Experience Platform 세그먼트를 찾을 수 있습니다.

![](assets/aep_audiences_list.png)

## Adobe Experience Platform 대상 만들기

Campaign Standard에서 직접 Adobe Experience Platform 대상을 만들려면 다음 단계를 수행하십시오.

1. Adobe Experience Platform 세그먼트 목록 페이지에서 오른쪽 모서리에 있는 **[!UICONTROL New audience]** 단추를 클릭합니다.

   ![](assets/aep_audiences_creation_create.png)

1. 이제 작업 공간에 세그먼트 빌더가 표시됩니다. 이 플러그인을 사용하면 궁극적으로 고객을 만드는 데 사용할 Adobe Experience Platform 데이터를 사용하여 세그먼트를 만들 수 있습니다.

1. 오른쪽 창에서 세그먼트의 이름을 지정하고 설명을 입력합니다(선택 사항).

   ![](assets/aep_audiences_creation_edit_name.png)

1. 세그먼트를 성공적으로 만들려면 이 세그먼트의 마케팅 목적과 일치하는 **병합 정책을** 선택해야 합니다.

   설정 창에서 플랫폼 기본 병합 정책이 선택됩니다. 병합 정책에 대한 자세한 내용은 세그먼트 빌더 사용 안내서의 [전용 섹션을 참조하십시오](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

   ![](assets/aep_audiences_mergepolicy.png)

1. 대상에서 검색할 프로파일을 식별하는 규칙을 정의합니다.

   이렇게 하려면 왼쪽 창에서 원하는 속성 및/또는 이벤트를 작업 영역으로 드래그하고 해당 규칙을 정의한 다음 **[!UICONTROL Create segment]** 단추를 클릭하여 세그먼트를 저장합니다(세그먼트 빌더 사용 [참조](../../audiences/using/aep-using-segment-builder.md)).

   ![](assets/aep_audiences_creation_query.png)

이제 대상이 활성화될 준비가 되었습니다. 이 대상을 캠페인에 대한 타겟으로 사용할 수 있습니다(Adobe Experience Platform 대상 [타깃팅 참조](../../automating/using/aep-targeting-audiences.md)).

## 대상자 편집

대상을 편집하려면 대상을 열고 세그먼트 빌더 인터페이스 내에서 필요에 따라 규칙 [을 수정합니다(세그먼트 빌더 사용 참조](../../audiences/using/aep-using-segment-builder.md)).

변경 사항이 완료되면 **[!UICONTROL Save segment]** 단추를 클릭하여 대상을 업데이트합니다.

![](assets/aep_audiences_editing.png)
