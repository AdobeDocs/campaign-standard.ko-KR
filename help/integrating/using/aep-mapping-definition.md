---
title: 매핑 정의
description: Campaign Standard 필드를 XDM(Experience Data Model) 필드와 매핑하는 방법에 대해 알아봅니다.
audience: administration
content-type: reference
topic-tags: configuring-channels
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 6383ddbe-922a-4363-a1da-166cf717b0dd
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# 매핑 정의 {#mapping-definition}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객을 Azure(현재 북미 지역의 경우에만 베타 버전)에서 호스팅해야 합니다. 액세스하려면 Adobe 고객 지원 센터에 문의하십시오.

이 섹션에서는 Campaign Standard 필드를 XDM(Experience Data Model) 필드와 매핑하는 방법에 대해 알아봅니다.

이 작업을 수행하기 위한 사전 요구 사항은 다음과 같습니다.

* 인터페이스를 통하거나 XDM과 연결된 REST API를 사용하는 XDM 스키마 정의
* xdm 스키마 정의를 기반으로 한 데이터 세트 생성

1. 다음으로 이동 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** 및 선택 **[!UICONTROL Data mappings]** 입력.

1. 클릭 **[!UICONTROL Create]** 새 XDM 매핑을 시작합니다.

   ![](assets/aep_createmapping.png)

1. 필수 필드를 완료하고 다음을 선택합니다.

   * a **타겟팅 차원**: 매핑할 Campaign Standard 스키마
   * a **데이터 세트**: Adobe Experience Platform의 XDM 스키마와 연결된 데이터 패키지입니다.

>[!NOTE]
>
>배치를 Real-Time Customer Profile 또는 Identity Service에 수집하려면 데이터 세트가 다음과 같아야 합니다. [실시간 고객 프로필에 대해 활성화됨](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/intro/get-started.html).
>
>선택한 데이터 세트가 기존 데이터 매핑에서 이미 사용 중인 경우 Adobe Experience Platform에서 데이터를 덮어쓸 수 있다는 경고가 표시됩니다. 이 문제는 동일한 데이터 세트를 사용하는 데이터 매핑에 몇 가지 일반적인 수신자가 있을 때 발생할 수 있습니다.

다음 화면은 **[!UICONTROL Field mappings]** Campaign Standard 스키마의 각 필드에 대한 새 매핑을 만들 수 있는 섹션입니다.

![](assets/aep_fieldmappings.png)

다음 **[!UICONTROL Create new field mapping]** 버튼을 사용하면 XDM 스키마에서 Campaign Standard 필드 및 해당 필드 경로 표현식을 선택할 수 있습니다.

Adobe Campaign Standard 필드를 찾을 수 없는 경우 검색 필드를 사용하여 필드를 검색할 수 있습니다. 현재 검색은 계층 구조에 열려 있는 필드에 대해서만 작동합니다.

![](assets/aep_mapfield.png)

Campaign Standard에 정의된 확장 리소스는 모든 기본 필드를 좋아하도록 매핑됩니다. XDM에서 _customer/default 확장에 정의됩니다.

![](assets/aep_fieldscusmapping.png)

API를 통해 XDM 확장을 사용자 지정하고 매핑을 더 잘 제어할 수 있도록 고유한 확장을 정의할 수 있습니다.

다음을 참조하십시오 [스키마 레지스트리 API 튜토리얼](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html) xdm API에 대한 자세한 내용.

열거형 필드를 매핑하려면 표현식 편집기를 사용하여 XDM 값에 해당하는 각 열거형 값을 정의해야 합니다. 예를 들어 postaladdressfield를 다음과 같이 정의해야 합니다.

![](assets/aep_enummapping.png)

XDM 스키마에서 XDM 값이 열거형으로 정의된 경우 를 자동으로 대체하는 기본 EXDM 함수를 사용할 수 있습니다. **lif** 구문.

![](assets/aep_enummappingexdm.png)

XDM 매핑을 편집하려면 XDM을 열고 원하는 정보를 수정한 다음 저장합니다.

![](assets/aep_editmapping.png)

>[!IMPORTANT]
>
>현재로서는 의 값을 편집하는 경우 **[!UICONTROL Field mappings]** 섹션에서 필드 외부를 클릭한 다음 를 클릭할 때까지 변경 사항이 인터페이스에 표시되지 않습니다. **[!UICONTROL Save]** 단추를 클릭합니다. 이 동작은 편집이 있을 때 한 번만 발생합니다 **[!UICONTROL Field Mappings]** 는 페이지의 첫 번째 편집입니다.
