---
solution: Campaign Standard
product: campaign
title: 매핑 정의
description: XDM(Experience Data Model) 필드에 Campaign Standard 필드를 매핑하는 방법을 알아봅니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 2729852365a2e74d2a603d95f75285fe54313e71
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%

---


# 매핑 정의 {#mapping-definition}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 사전 예고 없이 빈번하게 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

이 섹션에서는 Campaign Standard 필드를 XDM(경험 데이터 모델) 필드에 매핑하는 방법을 알아봅니다.

이 작업을 수행하려면 사전 요구 사항:

* 인터페이스를 사용하거나 XDM과 연결된 REST API를 사용하여 XDM 스키마 정의
* XDM 스키마 정의를 기반으로 데이터 집합 만들기

1. **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]**&#x200B;로 이동하여 **[!UICONTROL Data mappings]** 항목을 선택합니다.

1. **[!UICONTROL Create]**&#x200B;을 클릭하여 새 XDM 매핑을 시작합니다.

   ![](assets/aep_createmapping.png)

1. 필수 필드를 작성하고 다음을 선택합니다.

   * **타깃팅 차원**:매핑할 Campaign Standard 스키마입니다.
   * **데이터 세트**:adobe experience platform의 XDM 스키마에 연결된 데이터 패키지입니다.

>[!NOTE]
>
>일괄 처리를 실시간 고객 프로필 또는 ID 서비스로 인제스트하려면 데이터 세트에 실시간 고객 프로필](https://docs.adobe.com/content/help/en/experience-platform/rtcdp/intro/get-started.html)에 대해 [이(가) 활성화되어 있어야 합니다.
>
>선택한 데이터 세트가 이미 기존 데이터 매핑에서 사용되고 있는 경우 Adobe Experience Platform에서 데이터를 덮어쓸 수 있다는 경고가 표시됩니다. 동일한 데이터 세트를 사용하는 데이터맵에 일부 일반적인 받는 사람이 있는 경우 이러한 문제가 발생할 수 있습니다.

다음 화면은 Campaign Standard 스키마의 각 필드에 대해 새 매핑을 만들 수 있는 **[!UICONTROL Field mappings]** 섹션을 보여 줍니다.

![](assets/aep_fieldmappings.png)

**[!UICONTROL Create new field mapping]** 단추를 사용하면 XDM 스키마의 Campaign Standard 필드와 해당 필드 경로 표현식을 선택할 수 있습니다.

Adobe Campaign Standard 필드를 찾을 수 없는 경우 검색 필드를 사용하여 필드를 검색할 수 있습니다. 현재 검색은 계층에 열려 있는 필드에만 작동합니다.

![](assets/aep_mapfield.png)

Campaign Standard에 정의된 확장 리소스는 모든 기본 필드가 좋아요를 누른 상태로 매핑됩니다. XDM에서 _customer/default 확장명으로 정의됩니다.

![](assets/aep_fieldscusmapping.png)

API를 통해 XDM 확장을 사용자 정의하고 자체 확장 기능을 정의하여 매핑에 대한 보다 효과적인 제어를 할 수 있습니다.

XDM API에 대한 자세한 내용은 [스키마 레지스트리 API 자습서](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/api/getting-started.html)를 참조하십시오.

열거형 필드를 매핑하려면 표현식 편집기를 사용하여 XDM 값에 해당하는 각 열거형 값을 정의해야 합니다. 예를 들어 postalAdressfield를 다음과 같이 정의해야 합니다.

![](assets/aep_enummapping.png)

XDM 값이 XDM 스키마의 열거형으로 정의된 경우 **lif** 구문을 자동으로 대체할 기본 EXDM 함수를 사용할 수 있습니다.

![](assets/aep_enummappingexdm.png)

XDM 매핑을 편집하려면 해당 매핑을 열고 원하는 정보를 수정한 다음 저장합니다.

![](assets/aep_editmapping.png)

>[!IMPORTANT]
>
>현재 **[!UICONTROL Field mappings]** 섹션에서 값을 편집한 다음 필드 외부를 클릭하면 **[!UICONTROL Save]** 단추를 클릭하기 전까지 변경 내용이 인터페이스에 표시되지 않습니다. 이 동작은 **[!UICONTROL Field Mappings]**&#x200B;의 편집이 페이지에서 처음 편집되는 경우에만 발생합니다.
