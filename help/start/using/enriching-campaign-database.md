---
title: 데이터베이스 강화
seo-title: 데이터베이스 강화
description: 데이터베이스 강화
seo-description: 데이터베이스를 보강하는 다양한 방법에 대해 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 71f53808-0309-49f6-a4ee-3446eac9758a
contentOwner: 여우원숭이
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: about-adobe-campaign
discoiquuid: d8c8a318-9433-4aec-b378-fd0beb50e9fb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8b4cf35fcbdee436ce3f9fa4aeb1b1fdd8609f50

---


# 데이터베이스 강화{#enriching-the-database}

Campaign Standard는 마케팅 데이터베이스를 확장하는 데 도움이 되는 몇 가지 도구를 제공합니다. 이 섹션에서는 전용 문서에 대한 참조와 함께 데이터를 Campaign에 주입하는 데 사용할 수 있는 다양한 방법에 대해 자세히 설명합니다.

## 워크플로우를 통해 데이터 가져오기 {#importing-data-through-workflows}

워크플로우를 사용하면 [**[!UICONTROL Data management]**](../../automating/using/about-data-management-activities.md) 활동을 사용하여 데이터를 수집하고 Campaign 데이터베이스로 가져올 수 있습니다.

워크플로우를 통해 데이터를 가져올 때의 일반 정보 및 우수 사례가 [이 섹션에](../../automating/using/importing-data.md)설명되어 있습니다.

또한 템플릿을 설정하여 데이터를 가져올 수 있습니다. 가져오기 템플릿을 사용하면 구조가 동일한 파일을 정기적으로 가져와야 하는 경우 가장 좋은 방법입니다.

두 가지 유형의 템플릿을 설정할 수 있습니다.

* **워크플로우 템플릿**:이러한 워크플로우는 필요에 따라 한 번 설정할 수 있고 데이터를 가져오고 데이터베이스를 업데이트할 때마다 재사용할 수 있는 미리 구성된 워크플로우입니다.

   데이터를 가져오는 워크플로우 템플릿의 예는 [이 섹션에](../../automating/using/importing-data.md#example--import-workflow-template)자세히 설명되어 있습니다.

* **데이터 템플릿**&#x200B;가져오기:워크플로우 템플릿과 마찬가지로 데이터베이스를 업데이트하기 위해 파일을 업로드하도록 설정된 워크플로우를 기반으로 하는 템플릿입니다. 구성이 완료되면 **[!UICONTROL Profile & audiences]** / **[!UICONTROL Imports]** 메뉴 아래에 간소화된 보기를 사용하는 사용자가 사용할 수 있습니다.

   데이터 템플릿 가져오기에 대한 자세한 내용은 [전용 설명서를](../../automating/using/importing-data-with-import-templates.md)참조하십시오.

## 랜딩 페이지에서 데이터 수집 {#collecting-data-from-landing-pages}

랜딩 페이지는 데이터를 수집하고 데이터베이스에 기존 정보를 만들거나 업데이트하는 데 사용할 수 있는 웹 양식입니다.

원칙은 다음과 같습니다.

* 입력 필드를 추가하여 데이터(이름, 성, 이메일 등)를 수집하여 랜딩 페이지를 만들고 디자인합니다.
* 각 입력 필드를 데이터베이스의 해당 필드에 매핑합니다.
* 랜딩 페이지를 웹 사이트를 통해 또는 메시지에 대한 직접 링크를 통해 온라인으로 사용할 수 있도록 합니다.

랜딩 페이지에 대한 자세한 내용은 [전용 설명서를](../../channels/using/about-landing-pages.md)참조하십시오.

## Microsoft Dynamics 365에서 프로필 동기화

Microsoft Dynamics 365와 Campaign Standard의 통합을 통해 Microsoft Dynamics 365의 연락처 데이터를 Campaign 데이터베이스로 전달할 수 있습니다.
그런 다음 이러한 연락처가 **[!UICONTROL Profiles]** 목록에 표시되며 마케팅 캠페인에서 타깃팅될 수 있습니다.

이 통합에 대한 자세한 내용은 [전용 설명서를](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html)참조하십시오.

>[!NOTE]
>
>Campaign Standard-Microsoft Dynamics 365 커넥터는 현재 제한된 가용성에 있으며 설명서에 자세히 나와 있는 몇 가지 제한 사항을 따릅니다.

## API 호출을 통해 데이터 가져오기

Campaign Standard API를 사용하면 프로필 또는 서비스의 생성, 업데이트 또는 삭제와 같은 데이터베이스를 업데이트하는 작업을 수행할 수 있습니다.

API를 사용하는 방법에 대한 자세한 내용은 [전용 설명서를](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)참조하십시오.

>[!CAUTION]
>
>API 호출을 통해 프로파일 대량 생성 또는 업데이트를 수행하기 전에 라이센스 계약에 해당하는 크기 제한을 확인하십시오. For more on this, refer to [this page](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).
