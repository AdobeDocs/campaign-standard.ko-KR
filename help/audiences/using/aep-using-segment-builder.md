---
solution: Campaign Standard
product: campaign
title: 세그먼트 빌더 사용
description: 세그먼트 빌더를 사용하여 대상을 만드는 방법을 알아봅니다.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 4%

---


# 세그먼트 빌더 사용 {#using-the-segment-builder}

>[!IMPORTANT]
>
>대상 대상 서비스는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스 권한을 원하는 경우 Adobe 고객 지원 센터에 문의하십시오.

세그먼트 빌더를 사용하면 [실시간 고객 프로필에서 오는 데이터를 기반으로 규칙을 정의하여 대상을 만들 수 있습니다](https://docs.adobe.com/content/help/ko-KR/experience-platform/profile/home.html).

이 섹션에서는 세그먼트를 작성할 때 글로벌 개념을 설명합니다. 세그먼트 빌더 자체에 대한 자세한 내용은 [세그먼트 빌더 사용자 안내서를 참조하십시오](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

세그먼트 빌더 인터페이스는 다음과 같이 구성됩니다.

* 왼쪽 창에는 원하는 필드를 세그먼트 빌더 작업 공간으로 드래그하여 놓아 세그먼트를 만드는 데 사용할 수 있는 모든 속성, 이벤트 및 대상이 제공됩니다.
* 가운데 영역에서는 사용 가능한 필드에서 규칙을 정의하고 결합하여 세그먼트를 만드는 작업 공간을 제공합니다.
* 헤더와 오른쪽 창에는 세그먼트의 속성(예: 세그먼트의 이름, 설명 및 예상 적격한 프로필)이 표시됩니다.

![](assets/aep_audiences_interface.png)

## 세그먼트 작성

세그먼트를 만들려면 다음 단계를 수행하십시오.

이제 작업 공간에 세그먼트 빌더가 표시됩니다. 이 플러그인을 사용하면 궁극적으로 고객을 만드는 데 사용할 Adobe Experience Platform 데이터를 사용하여 세그먼트를 만들 수 있습니다.

1. 세그먼트 이름을 지정한 다음 설명을 입력합니다(선택 사항).

   ![](assets/aep_audiences_creation_edit_name.png)

1. 설정 창에서 원하는 병합 정책을 선택했는지 확인합니다.

   병합 정책에 대한 자세한 내용은 세그먼트 빌더 사용 안내서의 [전용 섹션을 참조하십시오](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

   ![](assets/aep_audiences_mergepolicy.png)

1. 왼쪽 창에서 원하는 필드를 찾아 가운데 작업 영역으로 드래그합니다.

   ![](assets/aep_audiences_dragfield.png)

1. 드래그된 필드에 해당하는 규칙을 구성합니다.

   ![](assets/aep_audiences_configure_rules.png)

1. **[!UICONTROL Create segment]** 버튼을 클릭합니다.

## 세그먼트에 적합한 필드 찾기

왼쪽 창에는 규칙을 구성하는 데 사용할 수 있는 모든 속성, 이벤트 및 대상이 나열됩니다.

나열된 필드는 회사에서 캡처한 속성이며 XDM( [Experience Data Model) 시스템을 통해 사용할 수 있게 되었습니다](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/home.html).

필드는 탭으로 구성됩니다.

* **[!UICONTROL Attributes]**:Adobe Campaign 데이터베이스 및/또는 Adobe Experience Platform에서 가져올 수 있는 기존 프로필 속성입니다. 프로필에는 첨부된 정적 정보(예: 이메일 주소, 거주 국가, 충성도 프로그램 상태 등)를 나타냅니다.

   ![](assets/aep_audiences_attributestab.png)

* **[!UICONTROL Events]**:&quot;2주 동안 두 번 주문했던 사람&quot;과 같이 회사의 고객 접점과 약간의 상호 작용을 가진 소비자를 식별하는 활동입니다. Adobe Analytics에서 스트리밍하거나 타사 ETL 툴을 사용하여 Adobe Experience Platform으로 직접 유입할 수 있습니다.

   ![](assets/aep_audiences_eventstab.png)

>[!NOTE]
>
>**다중 엔티티 세그먼테이션을** 사용하면 제품, 스토어 또는 기타 비프로필 클래스에 따라 추가 데이터로 프로필 데이터를 확장할 수 있습니다. 연결되면 추가 클래스의 데이터를 프로필 스키마가 기본인 것처럼 사용할 수 있습니다.
>
>자세한 내용은 [전용 설명서](https://docs.adobe.com/content/help/en/experience-platform/segmentation/multi-entity-segmentation.html)를 참조하십시오.

기본적으로 세그먼트 빌더에는 데이터가 이미 있는 필드가 표시됩니다. 데이터가 없는 필드를 포함하여 전체 스키마를 표시하려면 설정에서 **[!UICONTROL Show full XDM schema]** 옵션을 활성화합니다.

![](assets/aep_audiences_populatedfields.png)

각 필드 끝에 있는 기호는 속성에 대한 추가 정보와 속성 사용 방법을 제공합니다.

![](assets/aep_audiences_isymbol.png)

## 세그먼트에 대한 규칙 정의

>[!NOTE]
>
>아래 섹션은 규칙 정의에 대한 전역 정보를 제공합니다. 자세한 내용은 세그먼트 빌더 [사용자 안내서를 참조하십시오](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

규칙을 빌드하려면 다음 단계를 따르십시오.

1. 왼쪽 창에서 규칙의 기준이 되는 속성이나 이벤트를 반영하는 필드를 찾습니다.

1. 필드를 가운데 작업 영역으로 드래그한 다음 원하는 세그먼트 정의에 따라 구성합니다. 이렇게 하려면 몇 개의 문자열 및 날짜/시간 함수를 사용할 수 있습니다.

   아래 예에서 규칙은 &quot;남성&quot;과 같은 성별을 가진 모든 프로필을 대상으로 합니다.

   ![](assets/aep_audiences_malegender.png)

   세그먼트에 해당하는 예상 모집단은 섹션에서 자동으로 다시 **[!UICONTROL Segment Properties]** 계산됩니다.

1. 이 **[!UICONTROL View Profiles]** 단추를 사용하면 규칙에 해당하는 처음 20개의 레코드를 미리 볼 수 있으므로 빠르게 세그먼트의 유효성을 확인할 수 있습니다.

   ![](assets/aep_audiences_samplepreview.png)

   원하는 만큼 추가 규칙을 추가하여 올바른 프로파일을 타깃팅할 수 있습니다.

   컨테이너에 규칙을 추가하면 AND 논리 연산자가 있는 기존 규칙에 해당 규칙이 추가됩니다. 필요한 경우 논리 연산자를 클릭하여 수정합니다.

   ![](assets/aep_audiences_andoperator.png)

두 규칙이 함께 연결되면 컨테이너가 만들어집니다.

## 필드 비교

세그먼트 빌더를 사용하면 두 필드를 비교하여 규칙을 정의할 수 있습니다. 예를 들어 자신의 집 주소가 직장 주소와는 다른 우편번호에 있는 여성의 경우

이렇게 하려면 다음 단계를 수행합니다.

1. 비교할 첫 번째 필드(예: 집 주소 우편 번호)를 가운데 작업 영역으로 드래그합니다.

   ![](assets/aep_audiences_comparing_1.png)

1. 첫 번째 필드와 비교할 두 번째 필드(예: 직장 주소 우편 번호)를 선택합니다.

   상자의 첫 번째 필드와 동일한 컨테이너에 있는 가운데 작업 영역으로 **[!UICONTROL Drop here to compare operands]** 드래그합니다.

   ![](assets/aep_audiences_comparing_2.png)

1. 원하는 대로 두 필드 사이에 연산자를 구성합니다. 이 예에서는 세그먼트가 회사 주소와 다른 홈 주소를 가진 프로필을 타깃팅하기를 바랍니다.

   ![](assets/aep_audiences_comparing_3.png)

이제 규칙이 구성되고 대상으로 활성화할 준비가 되었습니다.
