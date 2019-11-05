---
title: 문제 해결
description: 리소스를 공유할 때 문제를 해결하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 1c764dd8-e09f-4e8e-9ccd-88ab3d714284
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 통합
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: c28e1d90-8074-4127-a6fc-ed39d69cdb19
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 문제 해결{#troubleshooting}

Audience Manager 또는 사람 핵심 서비스와의 통합을 사용하는 동안 오류가 발생할 수 있습니다.

이 경우 다음 요소가 올바르게 구성되어 있는지 확인하십시오.

* **외부 계정**

   &gt; **[!UICONTROL Administration]****[!UICONTROL Application settings]** &gt; **[!UICONTROL External accounts]**&#x200B;에서 다음 외부 S3 계정이 올바르게 구성되어 있는지 확인합니다. 언급된 S3 서버는 프로비저닝 중에 구성되어야 합니다.

   * **[!UICONTROL importSharedAudience]**:대상 가져오기 전용 S3 계정
   * **[!UICONTROL exportSharedAudience]**:대상 내보내기를 위한 S3 계정

* **공유 데이터 소스**

   &gt; **[!UICONTROL Administration]****[!UICONTROL Application settings]** &gt; **[!UICONTROL Shared Data Sources]**&#x200B;에서 공유 데이터 소스가 제대로 설정되어 있는지 확인합니다.

   **[!UICONTROL Priority]** 여러 데이터 소스가 정의된 경우 사용됩니다. 우선 순위는 정의된 순서대로 받은 별칭과 일치시키는 데 사용할 데이터 소스를 결정합니다. **[!UICONTROL Priority]** 은 트리거 구현에만 필요합니다.

   조정 키가 올바른지 확인하십시오. 대상을 내보내고 가져오는 데 사용되는 이 필드의 해시/암호화된 값입니다.

   선언된 ID를 해시하거나 암호화하는 경우 웹 사이트에서 동일한 매개 변수/암호화 알고리즘이 사용되는지 확인하십시오.

   하나의 암호화 알고리즘만 지원됩니다.키 크기가 128, 192 또는 256비트인 CBC 모드에서 PKCS 패딩이 있는 AES.

   AES 암호화 알고리즘을 선택한 경우 다음 추가 필드를 올바르게 설정해야 합니다.

   * **AES용** 암호화 키
   * **AES용** 암호화 IV(초기화 벡터)
   * **채널** (이메일/SMS/기타):이 필드를 사용하면 이메일 주소와 SMS 번호를 직접 해독할 수 있습니다. 조정 키가 채널 필드의 설정과 일치하는지 **확인합니다** . "기타"를 선택하면 특정 암호 해독 작업이 수행되지 않고 조정 키가 데이터를 조정하는 데 사용됩니다.
   기술 워크플로우가 중지되거나 일시 중지되어 Experience Cloud 대상이 공유되지 않을 수 있습니다. 데이터 소스의 **[!UICONTROL Import shared audience]** **[!UICONTROL Show ImportShared Audience workflow]** 옵션을 직접 클릭하여 워크플로우에 액세스합니다.

사람 코어 서비스를 통해 대상을 공유하거나 대상을 가져올 때 일부 데이터가 누락될 수 있습니다. ID('방문자 ID' 또는 '선언된 ID')가 프로필 차원과 조정될 수 있었던 레코드만 전송됩니다. Adobe Campaign에서 인식할 수 없는 사람 핵심 서비스 세그먼트의 ID는 가져올 수 없습니다.
