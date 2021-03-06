---
title: Campaign-Audience Manager 또는 People 핵심 서비스 통합 기본 정보
description: Audience Manager/사용자 핵심 서비스 통합을 사용하여 다른 Adobe Experience Cloud 솔루션 내에서 대상 또는 세그먼트를 공유할 수 있습니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: e8b96c66-82f7-4adb-88b2-b7e0f7c4a96f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 7%

---

# Campaign-Audience Manager 또는 People 핵심 서비스 통합 기본 정보{#about-campaign-audience-manager-or-people-core-service-integration}

>[!CAUTION]
>
>교환된 데이터에 따라 Adobe Campaign에서 대상을 가져오는 것은 법적 제한을 받을 수 있습니다.

Adobe Campaign을 사용하면 다양한 Adobe Experience Cloud 애플리케이션과 대상/세그먼트를 교환하고 공유할 수 있습니다. 통합 **Adobe Campaign** with **사용자 핵심 서비스** ( **프로필 및 대상 핵심 서비스**) 또는 Adobe Audience Manager을 통해 다음을 수행할 수 있습니다.

* 다양한 Adobe Experience Cloud 솔루션의 대상/세그먼트를 Adobe Campaign에 가져올 수 있습니다. 대상을 **[!UICONTROL Audiences]** 메뉴의 Adobe Campaign.
* 대상을 공유 대상/세그먼트로 내보냅니다. 이러한 대상은 사용하는 다양한 Adobe Experience Cloud 솔루션에서 사용할 수 있습니다. 워크플로우에서 타겟팅 활동을 수행한 후, **[!UICONTROL Save audience]** 활동.

통합은 다음과 같은 두 가지 유형의 Adobe Experience Cloud ID를 지원합니다.

* **방문자 ID**: 이 유형의 ID를 사용하면 Adobe Experience Cloud 방문자와 Adobe Campaign 프로필을 조정할 수 있습니다. Adobe IMS를 통해 연결이 활성화되면 바로 Adobe Campaign에서 사용하는 영구 쿠키를 대체하는 Marketing Cloud 방문자 ID 서비스 가 활성화됩니다. 방문자를 식별한 다음 프로필에 연결할 수 있습니다.
   <br>방문자 ID는 프로필이 Adobe Campaign을 통해 보낸 이메일을 클릭하는 즉시 프로필에 연결됩니다.
   * 프로필에 이미 방문자 ID가 있는 경우 해당 프로필의 브라우저 데이터를 사용하여 Adobe Campaign에서 프로필을 복구하고 방문자 ID에 자동으로 연결할 수 있습니다.
   * 방문자 ID가 없으면 새 ID가 만들어집니다. 이 방문자 ID는 프로필 추적 로그에 저장됩니다.

   그러면 ID가 동일한 CNAME의 다른 Adobe Marketing Cloud 애플리케이션에서 인식됩니다.

* **선언된 ID**: 이 유형의 ID를 사용하면 모든 유형의 데이터를 Adobe Campaign 데이터베이스의 요소로 조정할 수 있습니다. 이 키는 Adobe Campaign에 사전 정의된 조정 키로 표시됩니다. 데이터를 교환할 때 Adobe Campaign 데이터베이스 식별자가 해시됩니다. 그러면 이러한 해시된 ID는 가져오기 또는 내보내기에 포함된 Adobe Marketing Cloud 대상자의 해시된 ID와 비교됩니다.
   <br>이 통합은 선언된 일반 ID, 해시된 선언 ID 및 암호화된 선언 ID를 지원합니다.

   >[!NOTE]
   >
   >선언된 ID 데이터 소스는 People 핵심 서비스 통합에도 사용할 수 있습니다.
   >
   >People 핵심 서비스 통합을 사용하고 있으며 Audience Manager 통합을 추가하려면 Adobe Audience Manager 컨텍스트에서 선언된 ID 데이터 소스를 사용하여 전환할 때 수집된 모든 ID 동기화를 유실하지 않도록 Adobe Audience Manager 컨설턴트의 도움이 필요합니다.


   암호화를 사용하면 암호화 알고리즘을 지정하여 선언된 ID를 사용하여 데이터 소스(예: PII)에서 암호화된 데이터를 공유할 수 있습니다.

   예를 들어 암호화된 이메일 주소 또는 SMS 번호를 해독하는 기능을 사용하면 해당 프로필이 Adobe Campaign 데이터베이스에 없더라도 사용자에게 트리거된 메시지를 보낼 수 있습니다.

다음 다이어그램은 이 통합이 작동하는 방식을 자세히 설명합니다. 여기서는 AAM이 Adobe Audience Manager과 Adobe Campaign Standard의 ACS를 의미합니다.

![](assets/aam_diagram.png)
