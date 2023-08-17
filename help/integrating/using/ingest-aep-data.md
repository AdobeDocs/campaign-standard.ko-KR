---
title: Adobe Experience Platform 대상자를 Campaign으로 수집
description: Adobe Experience Platform 대상을 Campaign Standard으로 수집하는 방법에 대해 알아봅니다.
audience: integrating
content-type: reference
role: Data Architect
level: Intermediate
exl-id: 5c266c44-535b-4954-862d-74c83a6f6406
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 7%

---

# Adobe Experience Platform 대상자를 Campaign으로 수집 {#destinations}

Adobe Experience Platform 대상자를 Campaign에 수집하고 워크플로우에서 사용하려면 먼저 Adobe Campaign as a Adobe Experience Platform에 연결해야 합니다 **대상** 내보낼 세그먼트로 구성합니다.

대상이 구성되면 데이터가 스토리지 위치로 내보내지며, 이를 수집하려면 Campaign Standard에서 전용 워크플로우를 구축해야 합니다.

## Adobe Campaign을 대상으로 연결

Experience Platform Adobe에서 내보낸 세그먼트에 대한 저장소 위치를 선택하여 Adobe Campaign과의 연결을 구성합니다. 또한 이 단계를 통해 내보낼 세그먼트를 선택하고 포함할 추가 XDM 필드를 지정할 수 있습니다.

자세한 내용은 [대상 설명서](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email-marketing/adobe-campaign.html).

대상이 구성되면 Adobe Experience Platform은 사용자가 제공한 저장소 위치에 탭으로 구분된 .txt 또는 .csv 파일을 생성합니다. 이 작업은 24시간에 한 번 예약되고 수행됩니다.

이제 세그먼트를 Campaign에 수집하도록 Campaign Standard 워크플로우를 구성할 수 있습니다.

## Campaign Standard에서 가져오기 워크플로우 만들기

Campaign Standard이 대상으로 구성되면 Adobe Experience Platform에서 내보낸 파일을 가져올 수 있는 전용 워크플로우를 빌드해야 합니다.

이렇게 하려면 을(를) 추가하고 구성해야 합니다 **[!UICONTROL Transfer file]** 활동. 이 활동을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../../automating/using/transfer-file.md).

![](assets/rtcdp-transfer-file.png)

그런 다음 필요에 따라 워크플로우를 빌드할 수 있습니다(세그먼트 데이터를 사용하여 데이터베이스 업데이트, 세그먼트로 크로스 채널 게재 보내기 등)

예를 들어 아래 워크플로우는 매일 저장소 위치에서 파일을 다운로드한 다음 세그먼트 데이터로 Campaign 데이터베이스를 업데이트합니다.

![](assets/rtcdp-workflow.png)

데이터 관리 워크플로의 예는 [워크플로우 사용 사례](../../automating/using/about-workflow-use-cases.md#management) 섹션.

관련 항목:

* [데이터 관리 활동](../../automating/using/about-data-management-activities.md)
* [데이터 가져오기 및 내보내기 기본 정보](../../automating/using/about-data-import-and-export.md)
