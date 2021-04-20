---
solution: Campaign Standard
product: campaign
title: 엔드포인트
description: API 끝점에 대해 자세히 알아보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 10%

---


# 엔드포인트 {#endpoints}

Adobe Campaign REST API에 사용할 수 있는 끝점:

* **/profileAndServices**:즉시 사용 가능한 필드와 상호 작용합니다. 이 끝점에서 확장 필드에 액세스할 수 없습니다.
* **/profileAndServicesExt**:프로필 또는 서비스 사용자 지정 리소스 확장 중에 추가된 사용자 정의 필드와 상호 작용합니다. 사용자 지정 리소스에 대한 자세한 내용은 [이 섹션](../../api/using/custom-resources.md)을 참조하십시오.
* **/&lt;transactionalapi>**:트랜잭션 메시지 API와 상호 작용(트랜잭션 메시지 API 끝점의 이름은 인스턴스 구성에 따라 다릅니다.) 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/managing-transactional-messages.md)을 참조하십시오.
* **/workflow/execution**:워크플로우와 인터랙션 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/controlling-a-workflow.md)을 참조하십시오.
* **/privacy/privacy도구**:개인정보 보호 API와 상호 작용하여 개인정보 보호 요청의 자동 프로세스를 허용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/creating-a-privacy-request.md)을 참조하십시오.
* **/history**:프로파일의 마케팅 내역을 검색합니다. Campaign의 통합 고객 프로파일에 대한 자세한 내용은 [캠페인 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/integrated-customer-profile.html)를 참조하십시오.

기본적으로 **profileAndServices** 및 **profileAndServicesExt** API에 사용할 수 있는 기본 리소스는 다음과 같습니다.

* **/profile**:Campaign 데이터베이스의 프로필과 상호 작용합니다. 서비스에 프로필을 추가하려면 **/service** 끝점을 사용합니다. 캠페인의 프로필에 대한 자세한 내용은 [캠페인 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/about-profiles.html)를 참조하십시오.
* **/service**:구독 서비스를 관리합니다. 캠페인의 서비스에 대한 자세한 내용은 [캠페인 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html)를 참조하십시오.

>[!NOTE]
>
>확장되거나 만들어진 다른 모든 리소스는 **ProfileAndServicesExt** API를 통해서만 사용할 수 있습니다. 액세스할 수 있으려면 **프로필** 리소스에 연결해야 합니다.
