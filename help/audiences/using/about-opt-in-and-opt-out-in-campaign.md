---
title: Campaign의 옵트인 및 옵트아웃 기본 정보
description: 옵트아웃(또는 블랙 리스트)으로 인해 프로필이 더 이상 특정 채널에서 배달이나 배달로 타깃팅되지 않습니다.
page-status-flag: 활성화 안 함
uuid: 501d9485-976b-4de7-b242-6886f2814c6c
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: 옵트인 및 옵트아웃 프로세스 이해
discoiquuid: 2f26ec22-0809-4541-b2a1-e84ff868ba6e
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Campaign의 옵트인 및 옵트아웃 기본 정보{#about-opt-in-and-opt-out-in-campaign}

옵트아웃(또는 블랙 리스트)으로 인해 프로필이 더 이상 특정 채널에서 배달이나 배달로 타깃팅되지 않습니다.

프로필에 옵트인 또는 옵트아웃 기능을 제공하려면 전용 랜딩 페이지를 만들어야 합니다. 자세한 내용은 옵트인 및 옵트아웃 [랜딩 페이지](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages)설정을 참조하십시오.

연산자가 수동으로 프로파일을 옵트인하거나 아웃할 수도 있습니다. 자세한 내용은 [프로필에서](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#managing-opt-in-and-opt-out-from-a-profile)옵트인 및 옵트아웃 관리를 참조하십시오.

배달 속도를 높이기 위해 배달 분석 중에 옵트아웃 프로필이 자동으로 제외됩니다(오류 비율은 배달 속도에 상당한 영향을 줍니다).

>[!NOTE]
>
>옵트아웃은 **이메일 주소**&#x200B;또는 **전화 번호와** 연결된 검역과 **달리 프로필에 적용됩니다**. 따라서 프로필을 선택 해제하면 프로필과 연결된 모든 주소가 게재에서 제외됩니다. 사용자가 데이터베이스에 두 개의 프로필이 있을 경우 프로필 중 하나만 옵트아웃되므로 여전히 게재 대상으로 지정됩니다. 그의 모든 첩이 제외되도록, 그것을 검역소에 넣어라. For more on this, refer to [this page](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).

서비스 구독에 대한 자세한 내용은 [이 페이지를](../../audiences/using/about-subscriptions.md)참조하십시오.
