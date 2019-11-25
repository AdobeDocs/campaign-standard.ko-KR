---
title: 끝점
description: API 끝점에 대한 자세한 내용을 살펴보십시오.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 554bf4a441a0fb4daea3c5eddd95b0197ca12ae6

---


# 끝점 {#endpoints}

Adobe Campaign REST API에 사용할 수 있는 끝점:

* **/profileAndServices**:즉시 사용 가능한 필드와 상호 작용 이 끝점에서 확장 필드에 액세스할 수 없습니다.
* **/profileAndServicesExt**:프로필 또는 서비스 사용자 지정 리소스 확장 중에 추가된 사용자 정의 필드와 상호 작용합니다. For more on custom resources, refer to [this section](../../api/using/custom-resources.md).
* **/&lt;transactionalAPI&gt;**:트랜잭션 메시지 API와 상호 작용(API 끝점의 이름은 인스턴스 구성에 따라 다름) For more on this, refer to [this section](../../api/using/managing-transactional-messages.md).
* **/workflow/execution**:워크플로우와 인터랙션 For more on this, refer to [this section](../../api/using/managing-workflows.md).
* **/privacy/privacy도구**:개인정보 보호 API와 상호 작용하여 개인 정보 보호 요청의 자동 프로세스를 허용합니다. For more on this, refer to [this section](../../api/using/privacy-management.md).
* **/history**:프로파일의 마케팅 내역을 검색합니다. Campaign의 통합 고객 프로파일에 대한 자세한 내용은 Campaign [설명서를](https://helpx.adobe.com/campaign/standard/audiences/using/integrated-customer-profile.html)참조하십시오.

profileAndServices 및 profileAndServicesExt API에 사용할 수 있는 기본 **리소스는** 기본적으로 **다음과** 같습니다.

* **/profile**:campaign 데이터베이스의 프로필과 상호 작용합니다. 서비스에 프로필을 추가하려면 **/서비스** 끝점을 사용합니다. Campaign의 프로필에 대한 자세한 내용은 Campaign [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/audiences/using/about-profiles.html).
* **/service**:구독 서비스를 관리합니다. Campaign의 서비스에 대한 자세한 내용은 Campaign [설명서를 참조하십시오](https://helpx.adobe.com/campaign/standard/audiences/using/creating-a-service.html).

>[!NOTE]
>
>확장 또는 생성된 기타 모든 리소스는 ProfileAndServicesExt API를 통해서만 사용할 **수** 있습니다. 액세스 가능하려면 프로필 **리소스에** 연결되어 있어야 합니다.
