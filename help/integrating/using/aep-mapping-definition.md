---
title: 매핑 정의
description: XDM(Experience Data Model) 필드에 Campaign Standard 필드를 매핑하는 방법을 알아봅니다.
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
>Adobe Experience Platform Data Connector는 현재 베타 버전으로, 예고 없이 자주 업데이트될 수 있습니다. 고객은 이러한 기능에 액세스하려면 Azure에서 호스팅(현재 북미 전용 베타 버전)해야 합니다. 액세스하려면 고객 지원 센터에 문의하십시오.

이 섹션에서는 Campaign Standard 필드를 XDM(Experience Data Model) 필드에 매핑하는 방법을 알아봅니다.

이 작업을 수행하려면 전제 조건이 다음과 같습니다.

* 인터페이스를 통해 또는 XDM과 연결된 REST API를 사용하여 XDM 스키마 정의
* XDM 스키마 정의를 기반으로 데이터 세트 생성

1. **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** 로 이동하여 **[!UICONTROL Data mappings]** 항목을 선택합니다.

1. 새 XDM 매핑을 시작하려면 **[!UICONTROL Create]** 를 클릭하십시오.

   ![](assets/aep_createmapping.png)

1. 필수 필드를 작성하고 다음을 선택합니다.

   * **타겟팅 차원**: 매핑할 Campaign Standard 스키마입니다
   * **데이터 세트**: Adobe Experience Platform의 XDM 스키마와 연결된 데이터 패키지입니다.

>[!NOTE]
>
>실시간 고객 프로필 또는 ID 서비스에 일괄 처리를 수집하려면 데이터 세트에 실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/intro/get-started.html)에 대해 [이 활성화되어 있어야 합니다.
>
>선택한 데이터 세트가 이미 기존 데이터 매핑에서 사용되고 있는 경우 Adobe Experience Platform에서 데이터를 덮어쓸 수 있다는 경고가 표시됩니다. 동일한 데이터 세트를 사용하는 데이터 매핑에 일부 일반적인 수신자가 있는 경우 이러한 문제가 발생할 수 있습니다.

다음 화면에는 Campaign Standard 스키마의 각 필드에 대해 새 매핑을 생성할 수 있는 **[!UICONTROL Field mappings]** 섹션이 표시됩니다.

![](assets/aep_fieldmappings.png)

**[!UICONTROL Create new field mapping]** 버튼을 사용하면 XDM 스키마에서 Campaign Standard 필드와 해당 필드 경로 표현식을 선택할 수 있습니다.

Adobe Campaign Standard 필드를 찾을 수 없는 경우 검색 필드를 사용하여 필드를 검색할 수 있습니다. 현재 검색은 계층에서 열려 있는 필드에만 작동합니다.

![](assets/aep_mapfield.png)

Campaign Standard에 정의된 확장 리소스는 모든 기본 필드가 매핑됩니다. XDM에서 _customer/default 확장에 정의됩니다.

![](assets/aep_fieldscusmapping.png)

API를 통해 XDM 확장을 사용자 지정하고 고유한 확장을 정의할 수 있으므로 매핑에 대한 개선된 제어를 수행할 수 있습니다.

XDM API에 대한 자세한 내용은 [스키마 레지스트리 API 자습서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)를 참조하십시오.

열거형 필드를 매핑하려면 표현식 편집기를 사용하여 XDM 값에 해당하는 각 열거형 값을 정의해야 합니다. 예를 들어 postaladdressfield를 다음과 같이 정의해야 합니다.

![](assets/aep_enummapping.png)

XDM 값이 XDM 스키마에서 열거형으로 정의된 경우 **lif** 구문을 자동으로 바꾸는 기본 EXDM 함수를 사용할 수 있습니다.

![](assets/aep_enummappingexdm.png)

XDM 매핑을 편집하려면 해당 매핑을 열고 원하는 정보를 수정한 후 저장합니다.

![](assets/aep_editmapping.png)

>[!IMPORTANT]
>
>현재 **[!UICONTROL Field mappings]** 섹션에서 값을 편집한 다음 필드 바깥쪽을 클릭하면 **[!UICONTROL Save]** 버튼을 클릭하기 전까지 변경 사항이 인터페이스에 표시되지 않습니다. 이 동작은 **[!UICONTROL Field Mappings]**&#x200B;의 편집이 페이지의 첫 번째 편집인 경우에만 발생합니다.
