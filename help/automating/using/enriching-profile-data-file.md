---
title: 파일에 포함된 데이터로 프로필 데이터 강화
description: 이 예에서는 파일에 포함된 구매 데이터를 사용하여 프로필 데이터를 향상시키는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 8c1693ef-1312-422c-b05d-263553113f8f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: f67c1caf-3284-4c34-a5b0-8654a95640ae
context-tags: enrichment,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---


# 파일에 포함된 데이터로 프로필 데이터 강화 {#enriching-profile-data-with-data-contained-in-a-file}

이 예에서는 파일에 포함된 구매 데이터를 사용하여 프로필 데이터를 향상시키는 방법을 보여 줍니다.여기서 구매 데이터는 타사 시스템에 저장되어 있습니다. 각 프로파일은 파일에 여러 개의 구매를 저장할 수 있습니다. 워크플로우의 최종 목표는 두 개 이상의 항목을 구매한 대상 프로필로 이메일을 보내 충성도에 대한 감사를 표시하는 것입니다.

워크플로우는 다음과 같이 구성됩니다.

![](assets/enrichment_example_workflow.png)

* 메시지를 받을 프로필을 [타깃팅하는 쿼리](../../automating/using/query.md) 활동입니다.
* 구매 데이터를 [로드하는 파일](../../automating/using/load-file.md) 로드 활동. 예:

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2017;dannymars@example.com;TV;799
   aze124;28/05/2017;dannymars@example.com;Headphones;8
   aze125;31/07/2017;john.smith@example.com;Headphones;8
   aze126;14/12/2017;john.smith@example.com;Plastic Cover;4
   aze127;02/01/2018;dannymars@example.com;Case Cover;79
   aze128;04/03/2017;clara.smith@example.com;Phone;149
   ```

   이 예제 파일을 사용하면 이메일 주소를 사용하여 데이터를 데이터베이스 프로필과 조정합니다. 이 문서에 설명된 대로 고유 ID를 활성화할 수도 [있습니다](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).

* 파일에서 로드한 트랜잭션 데이터와 [에서 선택한 프로필 간에 링크를 만드는](../../automating/using/enrichment.md) 데이터 **[!UICONTROL Query]**&#x200B;농축활동. 링크는 활동의 **[!UICONTROL Advanced relations]** 탭에 정의됩니다. 링크는 **[!UICONTROL Load file]** 활동에서 들어오는 전환을 기반으로 합니다. 프로필 리소스의 &quot;이메일&quot; 필드와 가져온 파일의 &quot;고객&quot; 열을 조정 기준으로 사용합니다.

   ![](assets/enrichment_example_workflow2.png)

   링크가 만들어지면 두 세트의 **[!UICONTROL Additional data]** 가 추가됩니다.

   * 각 프로파일의 마지막 2개 트랜잭션에 해당하는 두 개의 라인 수집. 이 컬렉션의 제품 이름, 거래 날짜 및 제품 가격이 추가 데이터로 추가됩니다. 데이터에 내림차순 정렬이 적용됩니다. 컬렉션을 만들려면 탭에서 **[!UICONTROL Additional data]** 다음을 수행하십시오.

      활동의 탭에서 이전에 정의된 링크를 **[!UICONTROL Advanced relations]** 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      검색할 줄 수 **[!UICONTROL Collection]** 를 확인하고 지정합니다(이 예에서는 2개). 이 화면에서 컬렉션의 **[!UICONTROL Alias]** 및 **[!UICONTROL Label]** 를 사용자 지정할 수 있습니다. 이러한 값은 이 컬렉션을 참조할 때 워크플로우의 다음 활동에서 볼 수 있습니다.

      ![](assets/enrichment_example_workflow4.png)

      컬렉션 **[!UICONTROL Data]** 을 유지하려면 최종 전달에 사용할 열을 선택합니다.

      ![](assets/enrichment_example_workflow6.png)

      거래 날짜에 내림차순 정렬을 적용하여 최신 트랜잭션을 검색합니다.

      ![](assets/enrichment_example_workflow7.png)

   * 각 프로필에 대한 총 트랜잭션 수를 계산하는 집계입니다. 이 집계는 나중에 두 개 이상의 트랜잭션을 기록한 프로파일을 필터링하는 데 사용됩니다. 합계를 생성하려면 탭에서 다음을 **[!UICONTROL Additional data]** 수행합니다.

      활동의 탭에서 이전에 정의된 링크를 **[!UICONTROL Advanced relations]** 선택합니다.

      ![](assets/enrichment_example_workflow3.png)

      선택합니다 **[!UICONTROL Aggregate]**.

      ![](assets/enrichment_example_workflow8.png)

      유지할 **[!UICONTROL Data]** 방법은 모두 **계산 합계를** 정의합니다. 필요한 경우 사용자 지정 별칭을 지정하여 다음 활동에서 더 빠르게 찾습니다.

      ![](assets/enrichment_example_workflow9.png)

* 하나 [이상의 트랜잭션을 기록한 초기 대상의 프로파일을 검색하는 세그먼테이션](../../automating/using/segmentation.md) 활동 트랜잭션이 하나만 있는 프로필은 제외됩니다. 이를 위해 이전에 정의한 합계에서 세그멘테이션의 쿼리가 수행됩니다.

   ![](assets/enrichment_example_workflow5.png)

* 에 정의된 추가 데이터를 사용하여 프로필에서 수행한 두 개의 마지막 구매 [를 동적으로 검색하는 이메일 배달](../../automating/using/email-delivery.md) **[!UICONTROL Enrichment]** 활동. 개인화 필드를 추가할 때 추가 데이터( **TargetData)** 노드에서 추가 데이터를 찾을 수 있습니다.

   ![](assets/enrichment_example_workflow10.png)

**관련 항목:**

* [외부 데이터로 고객 프로파일 강화](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Managedatatofuelengagingexperiences)
