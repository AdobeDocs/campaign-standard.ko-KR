---
title: 매핑 활성화
description: 데이터 매핑을 활성화하는 방법 살펴보기
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c2ed4b3c85ceef3b604a8f68d924c7e5d9fad900

---


# 매핑 활성화 {#mapping-activation}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector는 현재 베타 버전이며, 사전 예고 없이 자주 업데이트될 수 있습니다. 이러한 기능에 액세스하려면 고객이 Azure(현재 북미 전용 베타 버전)에서 호스팅되어야 합니다. 액세스 권한을 원하는 경우 Adobe 고객 지원 센터에 문의하십시오.

매핑 정의가 완료되면 매핑을 게시할 수 있습니다. 배포 단계 후에 Campaign Standard와 Adobe Experience Platform 간의 데이터 복제가 자동으로 시작됩니다. 언제든지 **[!UICONTROL Stop]** 버튼을 클릭하여 복제를 중지할 수 있습니다.

매핑 수정 사항에 따라 모든 레코드를 Adobe Experience Platform으로 재전송하도록 선택할 수 있습니다.

![](assets/aep_publishmapping.png)

배포 타일에서 게시 로그에 액세스하고 로그를 내보낼 수 있습니다.

![](assets/aep_publog.png)

탭에서 게시된 **[!UICONTROL Export jobs]** 매핑에 대한 내보내기 작업을 모니터링할 수 있습니다.

![](assets/aep_jobstatus.png)

모든 데이터 내보내기 작업을 모니터링하려면 **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Platform]** > **[!UICONTROL Status of data export to platform]** 메뉴로 이동합니다.

![](assets/aep_statusmapping.png)

데이터 수집 작업 상태:

* **[!UICONTROL Created]**: 데이터 수집 작업이 만들어지고 데이터 수집이 진행 중입니다.
* **[!UICONTROL Failed]**: 데이터 수집 작업이 실패했습니다. 이유 필드는 실패 이유를 설명합니다. 실패가 일시적으로 또는 영구적일 수 있습니다. 일시적인 오류가 발생하는 경우 구성된 간격 후에 새 통합 작업이 만들어집니다. 문제 해결을 위한 첫 번째 단계로, 사용자는 실패 이유 필드를 확인할 수 있습니다. 이유가 사용자를 Adobe Experience Platform UI로 리디렉션하는 경우, 사용자는 Adobe Experience Platform에 로그인하여 데이터 세트에 있는 일괄 처리 상태를 확인하여 정확한 실패 원인을 파악할 수 있습니다.
* **[!UICONTROL Uploaded]**: 일괄 처리는 Adobe Experience Platform에서 처음 생성되며 데이터를 일괄 처리로 인제스트됩니다. 배치 ID 필드는 Adobe Experience Platform에서 배치에 대한 배치 ID를 표시합니다. 또한 Adobe Experience Platform에서는 일괄 처리에 대한 게시물 유효성 검사를 수행합니다. Adobe Experience Platform에서 게시물 유효성 검사 단계를 완료할 때까지 일괄 처리가 업로드됨으로 표시됩니다. 업로드 후 Adobe Experience Platform에서 일괄 처리 상태를 계속 폴링합니다. 일괄 처리는 Adobe Experience Platform의 실패 또는 성공 상태 게시물 확인에서 이동할 수 있습니다.
* **[!UICONTROL Success]**: Adobe Experience Platform에 일괄 처리가 업로드되면 구성된 간격 후에 작업 상태(플랫폼의 게시 유효성 검사)가 확인됩니다. &#39;성공&#39; 상태는 Adobe Experience Platform에서 데이터를 성공적으로 수집했음을 나타냅니다.
