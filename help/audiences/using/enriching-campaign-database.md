---
title: 데이터베이스 강화
description: 데이터베이스를 보강하는 다양한 방법에 대해 알아봅니다.
audience: start
content-type: reference
topic-tags: about-adobe-campaign
feature: Profiles
role: User
level: Intermediate
exl-id: 9c55a8b3-034e-4319-8a88-7b59e83fa458
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 3%

---

# 데이터베이스 강화{#enriching-the-database}

Campaign Standard은 마케팅 데이터베이스를 확장하는 데 도움이 되는 몇 가지 도구를 제공합니다. 이 섹션에서는 Campaign에 데이터를 주입하는 데 사용할 수 있는 다양한 방법과 전용 설명서에 대한 참조를 자세히 설명합니다.

## 워크플로우를 통해 데이터 가져오기 {#importing-data-through-workflows}

워크플로우에서는 [[!UICONTROL Data management]](../../automating/using/about-data-management-activities.md) 활동을 사용하여 데이터를 수집하고 Campaign 데이터베이스로 가져올 수 있습니다.

워크플로우를 통해 데이터를 가져올 때 일반적인 정보 및 모범 사례는 [이 섹션](../../automating/using/about-data-import-and-export.md)에 나와 있습니다.

또한 템플릿을 설정하여 데이터를 가져올 수도 있습니다. 가져오기 템플릿을 사용하는 것은 구조가 동일한 파일을 정기적으로 가져와야 하는 경우에 가장 좋습니다.

다음과 같은 두 가지 유형의 템플릿을 설정할 수 있습니다.

* **워크플로우 템플릿**: 미리 구성된 워크플로우로서 필요에 따라 한 번 설정하고 데이터를 가져오고 데이터베이스를 업데이트할 때마다 다시 사용할 수 있습니다.

   데이터를 가져오는 워크플로우 템플릿의 예는 [이 섹션](../../automating/using/creating-import-workflow-templates.md)에 자세히 설명되어 있습니다.

* **데이터 템플릿 가져오기**: 워크플로우 템플릿과 마찬가지로 워크플로우를 기반으로 하는 템플릿이며 데이터베이스를 업데이트하기 위해 파일을 업로드하도록 설정됩니다. 구성이 완료되면 **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** 메뉴 아래에 간소화된 보기가 있는 사용자가 사용할 수 있습니다.

   데이터 템플릿 가져오기에 대한 자세한 내용은 [전용 설명서](../../automating/using/importing-data-with-import-templates.md)를 참조하십시오.

## 랜딩 페이지에서 데이터 수집 {#collecting-data-from-landing-pages}

랜딩 페이지는 데이터를 수집하고 데이터베이스에서 기존 정보를 만들거나 업데이트하는 데 사용할 수 있는 웹 양식입니다.

원칙은 다음과 같습니다.

* 입력 필드를 추가하여 데이터(이름, 성, 이메일 등)를 수집하여 랜딩 페이지를 만들고 디자인합니다.
* 각 입력 필드를 데이터베이스의 해당 필드에 매핑합니다.
* 랜딩 페이지를 웹 사이트를 통해 또는 메시지에 대한 직접 링크를 통해 온라인으로 사용할 수 있도록 합니다.

랜딩 페이지에 대한 자세한 내용은 [전용 설명서](../../channels/using/getting-started-with-landing-pages.md)를 참조하십시오.

## Microsoft Dynamics 365에서 프로필 동기화

Microsoft Dynamics 365와 Campaign Standard 통합을 통해 연락처 데이터를 Microsoft Dynamics 365에서 Campaign 데이터베이스로 전달할 수 있습니다.
그런 다음 이러한 연락처는 프로필 목록에 표시되며 마케팅 캠페인에서 타겟팅할 수 있습니다.

이 통합에 대한 자세한 내용은 [전용 설명서](../../integrating/using/d365-acs-get-started.md)를 참조하십시오.

>[!NOTE]
>
>Campaign Standard-Microsoft Dynamics 365 커넥터는 현재 제한된 사용 가능 상태이며 문서에 자세히 설명된 몇 가지 제한 사항을 따라야 합니다.

## API 호출을 통해 데이터 가져오기

Campaign Standard API를 사용하면 프로필 또는 서비스의 만들기, 업데이트 또는 삭제와 같은 데이터베이스를 업데이트하는 작업을 수행할 수 있습니다.

API 사용 방법에 대한 자세한 내용은 [전용 설명서](../../api/using/get-started-apis.md)를 참조하십시오.

>[!IMPORTANT]
>
>API 호출을 통해 프로필을 대량 만들거나 업데이트하기 전에 라이선스 계약에 해당하는 크기 제한 사항을 확인하십시오. 자세한 정보는 이 [페이지](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers)를 참조하십시오.
