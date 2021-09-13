---
title: 소스 및 대상 시작
description: Adobe Experience Platform 소스 및 대상에 대해 자세히 알아보십시오.
audience: integrating
content-type: reference
role: Data Architect
level: Intermediate
exl-id: ba6205fa-dbcf-497a-882f-f15c00f12e68
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 8%

---

# 소스 및 대상 시작 {#rtcdp}

## 소스 및 대상 정보

Adobe Experience Platform을 사용하면 Campaign Standard과 RTCDP(실시간 고객 데이터 플랫폼) Adobe 간에 데이터를 공유할 수 있습니다. 이를 통해 Campaign 워크플로우에서 Adobe Experience Platform 대상을 타깃팅한 다음, 전송, 열기 및 클릭과 같은 이러한 대상과 관련된 실시간 고객 데이터 플랫폼 Adobe으로 다시 보낼 수 있습니다.

* **대상**&#x200B;을 사용하여 Adobe Experience Platform의 대상을 Campaign Standard으로 수집할 수 있습니다. 이를 통해 마케팅 캠페인에 대해 알려진 데이터와 알 수 없는 데이터를 활성화할 수 있습니다.
* **Sources**&#x200B;를 사용하여 Campaign Standard 데이터(예: 전송, 열기, 클릭)를 Adobe Experience Platform으로 내보냅니다. 이를 통해 서로 다른 소스에서 수집한 데이터를 한 곳에 집중하여 더 많은 작업을 수행할 수 있습니다.


>[!IMPORTANT]
>
>이 통합을 수행하는 동안 Adobe Campaign 계약에 따라 SFTP 저장소 제한, 데이터베이스 저장소 제한 및 활성 프로필 제한을 기억하십시오.

실시간 고객 데이터 플랫폼, 대상 및 소스 Adobe에 대한 자세한 개요는 다음 페이지를 참조하십시오.

* [실시간 고객 데이터 플랫폼 Adobe](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)
* [대상 설명서](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)
* [소스 설명서](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html)

## Adobe Experience Platform과 Campaign Standard 연결

Adobe Experience Platform과 Campaign Standard 간에 데이터를 공유하려면 먼저 Adobe Campaign을 **대상**&#x200B;으로 연결하고, AWS S3 또는 Azure blob 저장 공간 위치를 Adobe 경험 플랫폼의 **소스**&#x200B;로 연결해야 합니다.

커넥터가 구성되면 워크플로우를 사용하여 데이터 가져오기를 설정하거나 Campaign Standard으로 내보낼 수 있습니다.

![](assets/rtcdp-schema.png)

이러한 가져오기 및 내보내기 프로세스를 설정하는 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.

* [Adobe Experience Platform 대상자를 Campaign으로 수집](../../integrating/using/ingest-aep-data.md)
* [Campaign에서 Adobe Experience Platform으로 데이터 내보내기](../../integrating/using/export-campaign-data.md)
