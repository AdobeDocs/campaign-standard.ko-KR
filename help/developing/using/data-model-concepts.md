---
title: 데이터 모델 기본 개념
description: Adobe Campaign 데이터 모델과 수정 방법에 대해 알아봅니다.
page-status-flag: never-activated
uuid: cacd563f-6936-4b3e-83e3-5d4ae31d44e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 4e0468da-3052-4ce5-8174-45aba1f5c4ed
context-tags: cusResource,overview;eventCusResource,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1deeead4ad311fd3ba3a5e9d27a67d3a1dadf3d2

---


# 데이터 모델 기본 개념{#data-model-concepts}

Adobe Campaign은 사전 정의된 데이터 모델과 함께 제공됩니다. 이 데이터 모델은 기존 리소스에 새 리소스 또는 확장을 추가할 수 있는 [관리자가](../../administration/using/users-management.md#functional-administrators) 수정할 수 있습니다.

>[!CAUTION]
>
>리소스를 만들고 수정하는 작업은 전문가 사용자만 수행해야 하는 민감한 작업입니다.

Adobe Campaign 로고를 통해 액세스하는 **[!UICONTROL Administration]**> 메뉴를 사용하면**[!UICONTROL Development]** 사용자 지정 리소스를 **관리하고****게시하며** 진단 도구에 **액세스할 수**&#x200B;있습니다.

Adobe Campaign에서 사용하는 데이터는 다른 리소스를 통해 정의됩니다. 구매 또는 제품 테이블과 같은 사용자 지정 리소스를 만들어 제공되는 데이터 템플릿을 **** 보완할 수 있습니다.

기본 리소스(캠페인, 이메일 또는 대상 등)는 수정할 수 없습니다. 그러나 사용자 지정 리소스를 확장하여 새 필드를 추가할 수 있습니다.

확장 필드는 기본 필드와 충돌하지 않도록 접두사로 생성됩니다.

>[!NOTE]
>
>기본 리소스에 대한 데이터 모델 표현을 [여기에서](../../developing/using/datamodel-introduction.md)찾을 수 있습니다.

생성된 리소스에 해당하는 화면에서 내비게이션을 **** 구성할 수도 있습니다.

개발 환경에서 프로덕션 환경으로 사용자 정의 리소스를 **내보내고 가져올** 수 있습니다. 자세한 내용은 이 [단계별 사용 사례를](../../automating/using/exporting-importing-custom-resources.md)참조하십시오.
