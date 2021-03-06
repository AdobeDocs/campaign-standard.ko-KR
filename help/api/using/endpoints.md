---
title: 엔드포인트
description: API 종단점에 대해 자세히 알아보십시오 .
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 9f6d3da6-374d-47f5-bc8f-b31b19cbb5ca
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 10%

---

# 엔드포인트 {#endpoints}

Adobe Campaign REST API에 사용할 수 있는 엔드포인트:

* **/profileAndServices**: 즉시 사용 가능한 필드와 상호 작용할 수 있습니다. 이 끝점에서 확장 필드에 액세스할 수 없습니다.
* **/profileAndServicesExt**: 은 프로필 또는 서비스 사용자 지정 리소스 확장 중에 추가된 사용자 지정 필드와 상호 작용합니다. 사용자 지정 리소스에 대한 자세한 내용은 [이 섹션](../../api/using/custom-resources.md).
* **/&lt;transactionalapi>**: 트랜잭션 메시지 API와 상호 작용(트랜잭션 메시지 API 엔드포인트의 이름은 인스턴스 구성에 따라 다릅니다.) 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/managing-transactional-messages.md)을 참조하십시오.
* **/workflow/execution**: 워크플로우와 상호 작용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/controlling-a-workflow.md)을 참조하십시오.
* **/privacy/privacyTool**: 개인 정보 보호 API와 상호 작용하여 개인 정보 보호 요청의 자동 프로세스를 허용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/creating-a-privacy-request.md)을 참조하십시오.
* **/history**: 프로필의 마케팅 내역을 검색합니다. Campaign의 통합 고객 프로필에 대한 자세한 내용은 [Campaign 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/integrated-customer-profile.html).

기본적으로 **profileAndServices** 및 **profileAndServicesExt** API는 다음과 같습니다.

* **/profile**: campaign 데이터베이스의 프로필과 상호 작용합니다. 서비스에 프로필을 추가하려면 **/service** 엔드포인트. Campaign의 프로필에 대한 자세한 내용은 [Campaign 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/about-profiles.html).
* **/service**: 구독 서비스를 관리합니다. Campaign의 서비스에 대한 자세한 내용은 [Campaign 설명서](https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html).

>[!NOTE]
>
>확장 또는 생성된 기타 모든 리소스는 **ProfileAndServicesExt** API만 해당. 와 연결되어 있어야 합니다 **프로필** 액세스 가능한 리소스
