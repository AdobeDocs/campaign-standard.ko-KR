---
solution: Campaign Standard
product: campaign
title: 문제 해결
description: 리소스를 공유할 때 문제를 해결하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: 트리거
role: 데이터 아키텍트
level: 중간
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 1%

---


# 문제 해결{#troubleshooting}

Audience Manager 또는 사람 핵심 서비스와의 통합을 사용하는 동안 오류가 발생할 수 있습니다.

이 경우 다음 요소가 올바르게 구성되어 있는지 확인하십시오.

* **외부 계정**

   **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL External accounts]**&#x200B;에서 다음 외부 S3 계정이 올바르게 구성되어 있는지 확인합니다. 프로비저닝 중에 언급된 S3 서버를 구성해야 합니다.

   * **[!UICONTROL importSharedAudience]**:대상 가져오기 전용 S3 계정.
   * **[!UICONTROL exportSharedAudience]**:대상 내보내기를 위한 S3 계정입니다.

* **공유 데이터 소스**

   **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;에서 공유 데이터 소스가 제대로 설정되어 있는지 확인합니다.

   **[!UICONTROL Priority]** 여러 데이터 소스가 정의된 경우 사용됩니다. 우선 순위는 정의된 순서로 받은 별칭과 일치하는 데이터 소스를 결정합니다. **[!UICONTROL Priority]** 은 트리거 구현에만 필요합니다.

   조정 키가 올바른지 확인하십시오. 대상을 내보내고 가져오는 데 사용되는 이 필드의 해시/암호화된 값입니다.

   선언된 ID를 해시 또는 암호화하는 경우 웹 사이트에 동일한 매개 변수/암호화 알고리즘이 사용되는지 확인하십시오.

   하나의 암호화 알고리즘만 지원됩니다.키 크기가 128, 192 또는 256비트인 CBC 모드에서 PKCS 패딩이 있는 AES.

   AES 암호화 알고리즘을 선택한 경우 다음 추가 필드를 올바르게 설정해야 합니다.

   * **AES** 용 암호화 키
   * **AES용 암호화 IV** (초기화 벡터)
   * **채널** (이메일/SMS/기타):이 필드를 사용하면 이메일 주소와 SMS 번호를 직접 해독할 수 있습니다. 조정 키가 **채널** 필드의 설정과 일치하는지 확인합니다. &quot;기타&quot;를 선택하면 이 특정 암호 해독 작업이 발생하지 않으며 조정 키를 사용하여 데이터를 조정합니다.

   기술 작업 과정이 중지되거나 일시 중지되어 Experience Cloud 대상을 공유할 수 없습니다. 데이터 소스에서 **[!UICONTROL Show ImportShared Audience workflow]** 옵션을 직접 클릭하여 **[!UICONTROL Import shared audience]** 작업 과정에 액세스합니다.

사람 핵심 서비스를 통해 대상을 공유하거나 대상을 가져올 때 일부 데이터가 누락될 수 있습니다. ID(&#39;방문자 ID&#39; 또는 &#39;선언된 ID&#39;)를 프로필 차원과 조정할 수 있는 레코드만 전송됩니다. Adobe Campaign에서 인식하지 못하는 사람 핵심 서비스 세그먼트의 ID는 가져오지 않습니다.
