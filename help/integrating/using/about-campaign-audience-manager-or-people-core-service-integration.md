---
title: Campaign-Audience Manager 또는 People 핵심 서비스 통합 기본 정보
description: Audience Manager / 사람 핵심 서비스 통합을 통해 다양한 Adobe Experience Cloud 솔루션 내에서 대상 또는 세그먼트를 공유할 수 있습니다.
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
ht-degree: 22%

---

# Campaign-Audience Manager 또는 People 핵심 서비스 통합 기본 정보{#about-campaign-audience-manager-or-people-core-service-integration}

>[!CAUTION]
>
>교환된 데이터에 따라 Adobe Campaign에서 수입하는 대상자는 법적 제한을 받을 수 있습니다.

Adobe Campaign을 사용하면 대상자/세그먼트를 다른 Adobe Experience Cloud 애플리케이션과 교환하고 공유할 수 있습니다. 통합 중 **Adobe Campaign** 포함 **사용자 핵심 서비스** (또한으로 알려짐) **프로필 및 대상자 핵심 서비스**) 또는 Adobe Audience Manager을 사용하여 다음을 수행할 수 있습니다.

* 다양한 Adobe Experience Cloud 솔루션의 대상/세그먼트를 Adobe Campaign으로 가져옵니다. 대상에서 대상을 가져올 수 있습니다. **[!UICONTROL Audiences]** Adobe Campaign의 메뉴입니다.
* 대상을 공유 대상/세그먼트로 내보냅니다. 이러한 대상자는 사용하고 있는 여러 Adobe Experience Cloud 솔루션에서 사용할 수 있습니다. 대상자는 워크플로우에서 활동을 타겟팅한 후 을 사용하여 내보낼 수 있습니다. **[!UICONTROL Save audience]** 활동.

통합은 두 가지 유형의 Adobe Experience Cloud ID를 지원합니다.

* **방문자 ID**: 이 유형의 ID를 사용하면 Adobe Experience Cloud 방문자와 Adobe Campaign 프로필을 조정할 수 있습니다. Adobe IMS를 통해 연결이 활성화되는 즉시 Marketing Cloud 방문자 ID 서비스 가 활성화되고, 이는 Adobe Campaign에서 사용하는 영구 쿠키를 대체합니다. 이렇게 하면 방문자를 식별한 다음 프로필에 연결할 수 있습니다.
   <br>방문자 ID는 Adobe Campaign을 통해 전송된 이메일에서 프로필이 클릭되는 즉시 프로필에 연결됩니다.
   * 프로필에 이미 방문자 ID가 있는 경우 프로필의 브라우저 데이터를 사용하여 Adobe Campaign에서 복구하고 프로필을 방문자 ID에 자동으로 연결할 수 있습니다.
   * 방문자 ID가 없으면 새 ID가 만들어집니다. 이 방문자 ID는 프로필 추적 로그에 저장됩니다.

   그러면 이 ID는 동일한 CNAME을 사용하는 다른 Adobe Marketing Cloud 애플리케이션에서 인식됩니다.

* **선언된 ID**: 이 유형의 ID를 사용하면 모든 유형의 데이터를 Adobe Campaign 데이터베이스의 요소와 조정할 수 있습니다. Adobe Campaign에서는 사전 정의된 조정 키로 표시됩니다. 데이터를 교환할 때 Adobe Campaign 데이터베이스 식별자는 해시됩니다. 그런 다음 이러한 해시된 ID는 가져오기 또는 내보내기와 관련된 Adobe Marketing Cloud 대상의 해시된 ID와 비교됩니다.
   <br>이 통합은 일반 선언 ID, 해시된 선언 ID 및 암호화된 선언 ID를 지원합니다.

   >[!NOTE]
   >
   >선언된 ID 데이터 소스는 People 핵심 서비스 통합에도 사용할 수 있습니다.
   >
   >People 핵심 서비스 통합을 사용 중이고 Audience Manager 통합을 추가하려면 Adobe Audience Manager 컨설턴트의 도움이 필요합니다. 도움을 통해 Adobe Audience Manage 컨텍스트에서 선언 ID 데이터 소스를 사용하여 전환할 때 수집된 모든 ID 동기화를 손실되지 않도록 할 수 있습니다.


   암호화를 사용하면 암호화 알고리즘을 지정하여 선언된 ID를 사용하여 데이터 소스(예: PII)에서 암호화된 데이터를 공유할 수 있습니다.

   예를 들어 암호화된 이메일 주소 또는 SMS 번호를 해독하는 기능을 사용하면 Adobe Campaign 데이터베이스에 해당 프로필이 없는 경우에도 트리거된 메시지를 사용자에게 보낼 수 있습니다.

다음 다이어그램은 이 통합이 작동하는 방식을 자세히 설명합니다. 여기서 AAM은 Adobe Audience Manager을 나타내고 ACS는 Adobe Campaign Standard을 나타냅니다.

![](assets/aam_diagram.png)
