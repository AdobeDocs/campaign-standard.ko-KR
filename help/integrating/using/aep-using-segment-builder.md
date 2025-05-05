---
title: 세그먼트 빌더 사용
description: 세그먼트 빌더를 사용하여 대상자를 만드는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 9a6c542e-10ed-4e77-abb3-36324e1cb38f
hide: true
hidefromtoc: true
source-git-commit: 110f3ccb5865e70c78e18485b4ff4ba7a648af3f
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 3%

---

# 세그먼트 빌더 사용 {#using-the-segment-builder}

>[!IMPORTANT]
>
>Audience Destinations 서비스는 현재 베타 버전이며, 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

세그먼트 빌더를 사용하면 [실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko)에서 가져온 데이터를 기반으로 규칙을 정의하여 대상을 작성할 수 있습니다.

이 섹션에서는 세그먼트를 작성할 때의 글로벌 개념을 설명합니다. 세그먼트 빌더 자체에 대한 자세한 내용은 [세그먼트 빌더 사용 안내서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko)를 참조하세요.

세그먼트 빌더 인터페이스는 다음과 같이 구성됩니다.

* 왼쪽 창은 원하는 필드를 세그먼트 빌더 작업 영역으로 끌어다 놓아 세그먼트를 만드는 데 사용할 수 있는 모든 속성, 이벤트 및 대상을 제공합니다.
* 가운데 영역은 사용 가능한 필드에서 규칙을 정의하고 결합하여 세그먼트를 작성할 수 있는 작업 공간을 제공합니다.
* 머리글 및 오른쪽 창에는 세그먼트의 속성(예: 세그먼트의 이름, 설명 및 예상 적격 프로필)이 표시됩니다.

![](assets/aep_audiences_interface.png)

## 세그먼트 작성

세그먼트를 작성하려면 다음 단계를 따르십시오.

이제 세그먼트 빌더가 작업 공간에 표시됩니다. 이를 통해 최종적으로 대상자를 만드는 데 사용될 Adobe Experience Platform의 데이터를 사용하여 세그먼트를 작성할 수 있습니다.

1. 세그먼트 이름을 지정한 다음 설명을 입력합니다(선택 사항).

   ![](assets/aep_audiences_creation_edit_name.png)

1. 설정 창에서 원하는 병합 정책이 선택되어 있는지 확인합니다.

   병합 정책에 대한 자세한 내용은 [세그먼트 빌더 사용 안내서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko)의 전용 섹션을 참조하십시오.

   ![](assets/aep_audiences_mergepolicy.png)

1. 왼쪽 창에서 원하는 필드를 찾아 중앙 작업 영역으로 끌어서 놓습니다.

   ![](assets/aep_audiences_dragfield.png)

1. 끌어온 필드에 해당하는 규칙을 구성합니다.

   ![](assets/aep_audiences_configure_rules.png)

1. **[!UICONTROL Create segment]** 버튼을 클릭합니다.

## 세그먼트에 대한 적합한 필드 찾기

왼쪽 창에는 규칙을 구성하는 데 사용할 수 있는 모든 속성, 이벤트 및 대상이 나열됩니다.

나열된 필드는 회사에서 캡처한 특성이며 [XDM(Experience Data Model) 시스템](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)을 통해 사용할 수 있게 되었습니다.

필드는 탭으로 구성됩니다.

* **[!UICONTROL Attributes]**: Adobe Campaign 데이터베이스 및/또는 Adobe Experience Platform에서 가져올 수 있는 기존 프로필 특성입니다. 프로필에 첨부된 정적 정보(예: 이메일 주소, 거주 국가, 로열티 프로그램 상태 등)를 나타냅니다.

  ![](assets/aep_audiences_attributestab.png)

* **[!UICONTROL Events]**: &quot;2주 동안 두 번 주문한 사람&quot;과 같이 회사의 고객 접점과 일부 상호 작용한 소비자를 식별하는 활동. Adobe Analytics에서 스트리밍하거나 서드파티 ETL 도구를 사용하여 Adobe Experience Platform으로 직접 수집할 수 있습니다.

  ![](assets/aep_audiences_eventstab.png)

>[!NOTE]
>
>**다중 엔터티 세분화**&#x200B;을(를) 사용하면 제품, 스토어 또는 기타 비프로필 클래스를 기반으로 추가 데이터로 프로필 데이터를 확장할 수 있습니다. 연결되면 추가 클래스의 데이터를 프로필 스키마의 네이티브인 것처럼 사용할 수 있게 됩니다.
>
>자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/multi-entity-segmentation.html?lang=ko)를 참조하십시오.

기본적으로 세그먼트 빌더는 데이터가 이미 있는 필드를 표시합니다. 데이터가 없는 필드를 포함하여 전체 스키마를 표시하려면 설정에서 **[!UICONTROL Show full XDM schema]** 옵션을 활성화하십시오.

![](assets/aep_audiences_populatedfields.png)

각 필드의 끝에 있는 기호는 속성 및 속성 사용 방법에 대한 추가 정보를 제공합니다.

![](assets/aep_audiences_isymbol.png)

## 세그먼트에 대한 규칙 정의

>[!NOTE]
>
>아래 섹션에서는 규칙 정의에 대한 전역 정보를 제공합니다. 자세한 내용은 [세그먼트 빌더 사용 안내서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko)를 참조하세요.

규칙을 작성하려면 다음 단계를 수행합니다.

1. 왼쪽 창에서 규칙의 기준이 될 속성 또는 이벤트를 반영하는 필드를 찾습니다.

1. 필드를 중앙 작업 영역으로 끌어온 다음 원하는 세그먼트 정의에 따라 구성합니다. 이를 위해 몇 가지 문자열 및 날짜/시간 함수를 사용할 수 있습니다.

   아래 예에서, 규칙은 &quot;남성&quot;과 같은 성별을 가진 모든 프로필을 타겟팅합니다.

   ![](assets/aep_audiences_malegender.png)

   세그먼트에 해당하는 예상 모집단은 **[!UICONTROL Segment Properties]** 섹션에서 자동으로 다시 계산됩니다.

1. **[!UICONTROL View Profiles]** 단추를 사용하면 규칙에 해당하는 처음 20개의 레코드를 미리 볼 수 있으므로 세그먼트를 빠르게 확인할 수 있습니다.

   ![](assets/aep_audiences_samplepreview.png)

   올바른 프로필을 타겟팅하기 위해 원하는 만큼 추가 규칙을 추가할 수 있습니다.

   컨테이너에 규칙을 추가하면 AND 논리 연산자로 기존 규칙에 추가됩니다. 필요한 경우 논리 연산자를 클릭하여 수정합니다.

   ![](assets/aep_audiences_andoperator.png)

함께 연결되면 두 규칙이 컨테이너를 형성합니다.

## 필드 비교

세그먼트 빌더를 사용하면 두 필드를 비교하여 규칙을 정의할 수 있습니다. 예를 들어 집 주소가 회사 주소와 다른 우편번호에 있는 여성

이렇게 하려면 다음 단계를 수행합니다.

1. 비교하려는 첫 번째 필드(예: 홈 주소 우편 번호)를 중앙 작업 영역으로 끌어서 놓습니다.

   ![](assets/aep_audiences_comparing_1.png)

1. 첫 번째 필드와 비교할 두 번째 필드(예: 회사 주소 우편 번호)를 선택합니다.

   **[!UICONTROL Drop here to compare operands]** 상자의 첫 번째 필드와 같은 컨테이너에서 가운데 작업 영역으로 끌어서 놓습니다.

   ![](assets/aep_audiences_comparing_2.png)

1. 원하는 대로 두 필드 사이에 연산자를 구성합니다. 이 예에서는 세그먼트가 회사 주소와 다른 홈 주소를 사용하는 프로필을 타겟팅하려고 합니다.

   ![](assets/aep_audiences_comparing_3.png)

이제 규칙이 구성되었으며 대상으로 활성화할 준비가 되었습니다.
