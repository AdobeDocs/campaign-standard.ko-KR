---
title: 문제 해결
seo-title: 문제 해결
description: 문제 해결
seo-description: 리소스를 공유할 때 문제를 해결하는 방법을 알아봅니다.
page-status-flag: 정품 인증 안 함
uuid: 1 c 764 dd 8-e 09 f -4 e 8 e -9 ccd -88 ab 3 d 714284
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 통합
content-type: 참조
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: C 28 E 1 D 90-8074-4127-A 6 FC-ED 39 D 69 CDB 19
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Troubleshooting{#troubleshooting}

Audience Manager 또는 People 핵심 서비스와의 통합을 사용하는 동안 오류가 발생할 수 있습니다.

이 경우 다음 요소가 올바르게 구성되어 있는지 확인하십시오.

* **외부 계정**

   In **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL External accounts]**, make sure that the following external S3 accounts are correctly configured. 언급된 S 3 서버가 프로비저닝 중에 구성되었어야 합니다.

   * **[!UICONTROL importSharedAudience]**: 고객 가져오기 전용 S 3 계정.
   * **[!UICONTROL exportSharedAudience]**: 대상 내보내기를 위한 S 3 계정.

* **Shared Data Sources**

   In **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Shared Data Sources]**, check that the shared data source is set properly.

   **[!UICONTROL Priority]** 는 여러 데이터 소스가 정의되어 있을 때 사용됩니다. 우선 순위는 정의된 순서로 받은 별칭과 일치시킬 데이터 소스를 결정합니다. **[!UICONTROL Priority]** 는 트리거 구현에만 필요합니다.

   조정 키가 올바른지 확인합니다. 대상을 내보내고 가져오는 데 사용되는 이 필드의 해시된/비밀번호화된 값입니다.

   선언된 ID의 해싱 또는 암호화의 경우 웹 사이트에서 동일한 매개 변수/암호화 알고리즘이 사용되는지 확인합니다.

   하나의 암호화 알고리즘만 지원됩니다. PKCS 패딩이 있는 128 비트, 192 비트 또는 256 비트의 키 크기를 갖는 CBC 모드의 AES 입니다.

   AES 암호화 알고리즘을 선택한 경우 다음 추가 필드를 올바르게 설정해야 합니다.

   * **AES 암호화 키**
   * **AES 용 암호화 IV** (초기화 벡터)
   * **채널** (이메일/SMS/기타): 이 필드를 사용하면 이메일 주소와 SMS 번호를 직접 해독할 수 있습니다. Make sure that the reconciliation key matches the setting of the **Channel** field. " 기타 "를 선택하면 이 특정 해독이 발생하지 않고 조정 키가 데이터를 조정하는 데 사용됩니다.
   Experience Cloud 대상은 기술 워크플로우가 중지되거나 일시 중지되었기 때문에 공유되지 않을 수 있습니다. Access the **[!UICONTROL Import shared audience]** workflow by clicking directly the **[!UICONTROL Show ImportShared Audience workflow]** option in your Data source.

사람 핵심 서비스를 통해 또는 대상을 가져올 때 대상을 공유할 때 일부 데이터가 누락될 수 있습니다. ID (' 방문자 ID'또는'선언된 ID ') 가 프로필 차원과 통합될 수 있었던 레코드만 전송됩니다. Adobe Campaign에서 인식할 수 없는 사람 핵심 서비스 세그먼트의 ID는 가져오지 않습니다.
