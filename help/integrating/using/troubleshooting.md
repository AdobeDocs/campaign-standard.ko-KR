---
title: 문제 해결
description: 리소스를 공유할 때 문제를 해결하는 방법을 알아봅니다.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 5882ada6-dff4-4fd1-a433-0eb31570f73c
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---

# 문제 해결{#troubleshooting}

Audience Manager 또는 사용자 핵심 서비스와의 통합을 사용하는 동안 오류가 발생할 수 있습니다.

이 경우 다음 요소가 올바르게 구성되어 있는지 확인하십시오.

* **외부 계정**

   in **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL External accounts]**&#x200B;다음 외부 S3 계정이 올바르게 구성되었는지 확인합니다. 언급된 S3 서버는 프로비저닝 중에 구성했어야 합니다.

   * **[!UICONTROL importSharedAudience]**: 대상 가져오기에 전용 S3 계정입니다.
   * **[!UICONTROL exportSharedAudience]**: 대상 내보내기를 위한 S3 계정입니다.

* **공유 데이터 소스**

   in **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Shared Data Sources]**&#x200B;공유 데이터 소스가 제대로 설정되었는지 확인합니다.

   **[!UICONTROL Priority]** 여러 데이터 소스가 정의되어 있을 때에 사용됩니다. 우선 순위는 정의된 순서로 받은 별칭과 일치시키는 데 사용할 데이터 소스를 결정합니다. **[!UICONTROL Priority]** 은 트리거 구현에만 필요합니다.

   조정 키가 올바른지 확인합니다. 대상자를 내보내고 가져오는 데 사용되는 이 필드의 해시/암호화 값입니다.

   선언된 ID를 해싱하거나 암호화하는 경우 웹 사이트에서 동일한 매개 변수/암호화 알고리즘이 사용되는지 확인합니다.

   하나의 암호화 알고리즘만 지원됩니다. 키 크기가 128, 192 또는 256비트인 CBC 모드에서 PKCS 패딩과 함께 AES입니다.

   AES 암호화 알고리즘을 선택한 경우 다음 추가 필드를 올바르게 설정해야 합니다.

   * **암호화 키** AES용
   * **암호화 IV** (AES용 초기화 벡터)
   * **채널** (이메일/SMS/기타): 이 필드에서는 이메일 주소와 SMS 번호를 직접 해독할 수 있습니다. 조정 키가 **채널** 필드. &quot;기타&quot;를 선택하면 이 특정 암호 해독이 발생하지 않고 조정 키를 사용하여 데이터를 조정합니다.

   기술 워크플로우가 중지되었거나 일시 중지되었으므로 Experience Cloud 대상을 공유하지 않을 수 있습니다. 액세스 권한 **[!UICONTROL Import shared audience]** 직접 클릭하여 워크플로우 **[!UICONTROL Show ImportShared Audience workflow]** 옵션을 선택합니다.

People 핵심 서비스를 통해 대상을 공유하거나 대상을 가져올 때 일부 데이터가 누락될 수 있습니다. 프로필 차원과 조정할 수 있는 ID(&#39;방문자 ID&#39; 또는 &#39;선언된 ID&#39;)의 레코드만 전송됩니다. Adobe Campaign에서 인식하지 못하는 사람 핵심 서비스 세그먼트의 ID는 가져올 수 없습니다.
