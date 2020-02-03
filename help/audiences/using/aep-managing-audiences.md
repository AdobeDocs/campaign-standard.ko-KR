---
title: 대상자 관리
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
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 19b22fa0780a0bf7c4b7a559270d7c8b32d89e38

---


# 대상자 관리 {#about-audiences}

>[!IMPORTANT]
>
>대상 서비스는 현재 베타 버전으로, 예고 없이 빈번한 업데이트가 적용될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

## 대상 액세스

Adobe Experience Platform 대상에 액세스하려면 Campaign Standard 홈 페이지에서 **[!UICONTROL Audiences]**카드를 선택하거나**[!UICONTROL Audiences]** 링크를 선택한 다음 **[!UICONTROL Adobe Experience Platform]**선택합니다.

![](assets/aep_audiences_access.png)

만들어진 모든 Adobe Experience Platform 고객이 표시됩니다. 원하는 대상을 찾는 데 도움이 되는 검색 막대와 필터를 사용할 수 있습니다.

![](assets/aep_audiences_list.png)

## 대상자 만들기

대상은 Adobe Experience Platform 고객 목록에서 직접 생성됩니다. 이렇게 하려면 다음 단계를 따르십시오.

1. 대상 목록으로 이동한 다음 **[!UICONTROL New audience]**단추를 클릭합니다.

   ![](assets/aep_audiences_creation_create.png)

1. 이제 통합 세그먼트 빌더가 작업 영역에 표시됩니다. Adobe Experience Platform의 데이터를 사용하여 세그먼트를 만들 수 있습니다. 이 데이터는 궁극적으로 고객을 형성하는 데 사용됩니다.

1. 오른쪽 창에서 세그먼트의 이름을 지정하고 설명을 입력합니다(선택 사항).

   ![](assets/aep_audiences_creation_edit_name.png)

1. 세그먼트를 성공적으로 만들려면 이 세그먼트의 마케팅 용도와 일치하는 **병합 정책을** 선택해야 합니다.

   설정 창에서 플랫폼 기본 병합 정책이 선택됩니다. 병합 정책에 대한 자세한 내용은 세그먼트 빌더 사용 안내서의 [전용 섹션을 참조하십시오](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md)

   ![](assets/aep_audiences_mergepolicy.png)

1. 대상에서 검색할 프로파일을 식별할 규칙을 정의합니다.

   이렇게 하려면 왼쪽 창에서 원하는 속성 및/또는 이벤트를 작업 영역으로 드래그하고 해당 규칙을 정의한 다음 **[!UICONTROL Create segment]**단추를 클릭하여 세그먼트를 저장합니다(통합 세그먼트 빌더[사용 참조](../../audiences/using/aep-using-segment-builder.md)).

   ![](assets/aep_audiences_creation_query.png)

이제 대상이 활성화될 준비가 되었습니다. 이를 캠페인의 타겟으로 사용할 수 있습니다(Adobe Experience Platform [대상](../../automating/using/aep-targeting-audiences.md)타깃팅 참조).

## 대상자 편집

대상을 편집하려면 대상을 열고 필요에 따라 통합 세그먼트 빌더 인터페이스에서 규칙을 수정합니다(통합 세그먼트 빌더 [사용 참조](../../audiences/using/aep-using-segment-builder.md)).

변경 사항이 완료되면 **[!UICONTROL Save segment]**단추를 클릭하여 대상을 업데이트합니다.

![](assets/aep_audiences_editing.png)
