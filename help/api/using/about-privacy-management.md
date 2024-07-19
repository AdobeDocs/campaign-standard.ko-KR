---
title: 개인 정보 관리 기본 정보
description: API를 사용한 개인 정보 관리에 대해 자세히 알아보기
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
source-git-commit: 210289d44f0ad0ebf0b2654f6e9795adad7dd458
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# 개인 정보 관리 기본 정보 {#about-privacy-management}

Campaign Standard API는 GDPR 및 CCPA와 같은 개인 정보 보호 규정과 관련된 요청을 자동 처리할 수 있는 기능을 제공합니다.

수행할 수 있는 작업은 다음과 같습니다.

* 새 개인 정보 보호 요청 만들기,
* 개인 정보 보호 요청 모니터링,
* 개인 정보 데이터 파일 검색,
* 프로필의 CCPA 옵트아웃 상태를 관리합니다.

개인 정보 API 끝점은 **/privacy/privacyTool**&#x200B;입니다. PrivacyTool 리소스 설명 및 관련 필터는 리소스 메타데이터에서 사용할 수 있습니다. [메타데이터 메커니즘](../../api/using/metadata-mechanism.md)을 참조하십시오.

CCPA 옵트아웃은 **ccpaOptOut** 프로필 특성을 사용하여 관리됩니다.

Adobe Campaign Standard 및 개인 정보 보호 규정 준수에 대한 자세한 내용은 [전용 설명서](../../start/using/privacy-requests.md)를 참조하세요.
