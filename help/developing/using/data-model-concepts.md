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
translation-type: ht
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401
workflow-type: ht
source-wordcount: '207'
ht-degree: 100%

---


# 데이터 모델 기본 개념{#data-model-concepts}

Adobe Campaign은 사전 정의된 데이터 모델을 제공합니다. 기존 리소스에 새 리소스 또는 확장을 추가할 수 있는 [관리자](../../administration/using/users-management.md#functional-administrators)가 이 데이터 모델을 수정할 수 있습니다.

>[!CAUTION]
>
>리소스를 만들고 수정하는 작업은 전문가 사용자만이 수행해야 하는 중요한 작업입니다.

Adobe Campaign 로고를 통해 액세스할 수 있는 **[!UICONTROL Administration]** > **[!UICONTROL Development]** 메뉴를 사용하면 **사용자 지정 리소스**&#x200B;를 관리하고 **게시**&#x200B;하며 **진단 도구에 액세스**&#x200B;할 수 있습니다.

Adobe Campaign에서 사용하는 데이터는 다양한 리소스를 통해 정의됩니다. 제공되는 **데이터 템플릿을 보강**&#x200B;하기 위해 구매 또는 제품 표 등 사용자 지정 리소스를 만들 수 있습니다.

기본 제공 리소스(예: 캠페인, 이메일 또는 대상자)는 수정할 수 없습니다. 그러나 사용자 지정 리소스를 확장하여 새 필드를 추가할 수 있습니다.

확장 필드는 기본 제공 필드와 충돌하지 않도록 접두사가 붙어 생성됩니다.

>[!NOTE]
>
>[이 페이지](../../developing/using/datamodel-introduction.md)에서 기본 제공 리소스에 대한 데이터 모델 표시를 확인할 수 있습니다.

또한 만든 리소스에 해당하는 화면에서 [내비게이션을 구성](configuring-the-screen-definition.md)할 수도 있습니다.

사용자 정의 리소스를 **내보내기 및 가져오기**&#x200B;할 수 있습니다. 예를 들면 개발 환경에서 프로덕션 환경으로 가져오거나 내보낼 수 있습니다. 자세한 내용은 이 [단계별 사용 사례](../../automating/using/exporting-importing-custom-resources.md)를 참조하십시오.
