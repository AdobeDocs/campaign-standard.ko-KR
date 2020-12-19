---
solution: Campaign Standard
product: campaign
title: Campaign 사용자 지정 리소스 및 Dynamics 365 사용자 지정 엔터티 매핑
description: Adobe Campaign Standard과 Microsoft Dynamics 365 간의 통합 컨텍스트에서 리소스와 개체를 매핑하는 방법을 살펴봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 9%

---


# 캠페인 리소스 및 Dynamics 365 개체 매핑

Adobe Campaign Standard과 Microsoft Dynamics 365 간의 통합 작업 중에 맞춤형 리소스와 맞춤형 엔티티를 매핑하는 방법을 살펴봅니다.

>[!CAUTION]
>
>이 기능은 제품의 일부로 기본 제공되지 않습니다. 구현하려면 Adobe Consulting 서비스가 필요합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

## 사전 요구 사항

[Microsoft Dynamics 365-Adobe Campaign Standard 통합](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)은 사용자 지정 개체를 지원하므로 Dynamics 365의 사용자 지정 엔터티가 Campaign의 해당 사용자 지정 리소스와 동기화될 수 있습니다.

사용자 지정 리소스의 새 데이터는 세그멘테이션 및 개인화를 비롯한 여러 용도로 사용할 수 있습니다.

통합은 연결된 테이블과 연결되지 않은 테이블을 모두 지원합니다. 연결은 최대 3개 수준(예: level1->level2->level3)까지 지원됩니다.

>[!CAUTION]
>
>캠페인 사용자 지정 리소스 레코드에 개인 정보가 포함되어 있는 경우 특정 권장 사항이 적용됩니다. 이 섹션](../../integrating/using/notices-and-recommendations-for-acs-and-ms-dynamics.md#privacy-linked-resources)에서 [에 대해 자세히 알아보십시오.

## 공지 사항

사용자 지정 엔티티 데이터 흐름을 구성할 때 다음을 알아야 합니다.

* Campaign 사용자 지정 리소스를 만들고 수정하는 것은 전문가 사용자에게만 수행해야 하는 중요한 작업입니다.
* 사용자 지정 엔터티 데이터 플로우의 경우 동기화된 사용자 지정 엔터티에 대해 Dynamics 365 내에서 변경 추적을 활성화해야 합니다.
* 통합의 병렬 처리로 인해 상위 레코드와 연결된 하위 레코드가 Dynamics 365에서 거의 같은 시간에 만들어지는 경우 새 하위 레코드를 부모 레코드 전에 Campaign에 기록할 수 있는 가능성이 약간 있습니다.

* 상위 및 하위가 **1 카디널리티 단순 링크** 옵션을 사용하여 캠페인 측에 연결된 경우, 상위 레코드가 Campaign에 도착할 때까지 하위 레코드는 숨겨지고 액세스할 수 없게 됩니다(UI 또는 API를 통해).

* (캠페인에서 **1 카디널리티 단순 링크**&#x200B;라고 가정함) Dynamics 365에서 하위 레코드가 업데이트되거나 삭제되고 상위 레코드가 캠페인에 표시되기 전에 해당 변경이 캠페인에 기록되면(그럴 가능성은 없지만 원격 가능성) 해당 업데이트 또는 삭제가 Campaign에서 처리되지 않고 오류가 발생합니다. 업데이트되는 경우 업데이트된 레코드를 동기화하려면 문제의 레코드를 Dynamics 365에서 다시 업데이트해야 합니다. 삭제의 경우 삭제 또는 업데이트에 필요한 Dynamics 365의 레코드가 더 이상 없으므로 해당 레코드를 캠페인 측에서 별도로 처리해야 합니다.

* 숨겨진 자식 레코드가 있고 액세스할 방법이 없는 경우에 발생하는 경우, 일시적으로 카디널리티 링크 유형을 **0 또는 1 카디널리티 단순 링크**&#x200B;로 변경하여 해당 레코드에 액세스할 수 있습니다.

캠페인 사용자 지정 리소스의 보다 포괄적인 개요는 이 섹션](../../developing/using/key-steps-to-add-a-resource.md)에서 [을 참조할 수 있습니다.
