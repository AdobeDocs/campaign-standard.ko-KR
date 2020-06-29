---
title: 관계를 사용한 데이터 조정
description: 다음 예에서는 파일의 구매 데이터를 사용하여 데이터베이스를 업데이트하는 워크플로우를 보여줍니다.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# 관계를 사용한 데이터 조정 {#reconciliation-relations}

다음 예에서는 파일의 구매 데이터를 사용하여 데이터베이스를 업데이트하는 워크플로우를 보여줍니다. 구매 데이터에는 클라이언트 이메일 및 제품 코드와 같은 다른 차원의 요소를 참조하는 데이터가 포함됩니다.

>[!NOTE]
>
>이 **예제에 사용된 트랜잭션** 및 **제품** 리소스는 기본적으로 Adobe Campaign 데이터베이스에 없습니다. 따라서 사용자 지정 리소스 기능을 사용하여 미리 [제작되었습니다](../../developing/using/data-model-concepts.md) . 가져온 파일 및 제품의 이메일 주소에 해당하는 프로필이 미리 데이터베이스에 로드되었습니다.

워크플로우는 다음 활동으로 구성됩니다.

![](assets/reconciliation_example1.png)

* 가져올 파일의 데이터를 [로드하여 검색하는 파일](../../automating/using/load-file.md) 로드 활동 가져온 파일에는 다음 데이터가 포함됩니다.

   * 거래 날짜
   * 클라이언트 이메일 주소
   * 구매한 제품 코드

   ```
   date;client;product
   2015-05-19 09:00:00;mail1@email.com;ZZ1
   2015-05-19 09:01:00;mail2@email.com;ZZ2
   2015-05-19 09:01:01;mail3@email.com;ZZ2
   2015-05-19 09:01:02;mail4@email.com;ZZ2
   2015-05-19 09:02:00;mail5@email.com;ZZ3
   2015-05-19 09:03:00;mail6@email.com;ZZ4
   2015-05-19 09:04:00;mail7@email.com;ZZ5
   2015-05-19 09:05:00;mail8@email.com;ZZ7
   2015-05-19 09:06:00;mail9@email.com;ZZ6
   ```

* 구매 데이터를 [데이터베이스 프로필과 제품에 바인딩하는 조정](../../automating/using/reconciliation.md) 활동입니다. 따라서 파일 데이터와 프로필 테이블 및 제품 테이블 간의 관계를 정의해야 합니다. 이 구성은 활동의 **[!UICONTROL Relations]** 탭에서 수행됩니다.

   * 프로파일과 관계 ****: 파일의 **클라이언트** 열은 **프로필** 차원의 **이메일** 필드에연결됩니다.
   * 제품 관련 **사항**: 파일의 **제품** 열은 **프로필** 차원의 **productCode** 필드에연결되어있습니다.
   연결된 차원의 외래 키를 참조하기 위해 인바운드 데이터에 열이 추가됩니다.

   ![](assets/reconciliation_example3.png)

* 데이터 [업데이트](../../automating/using/update-data.md) 작업을 사용하면 가져온 데이터를 사용하여 업데이트할 데이터베이스 필드를 정의할 수 있습니다. 데이터가 이전 활동에서 **거래** 차원에 속하는 것으로 이미 확인되었으므로 여기에서 **[!UICONTROL Directly using the targeting dimension]** 식별 옵션을 사용할 수 있습니다.

   업데이트할 필드를 자동으로 감지하는 옵션을 사용하면 이전 활동(프로필 및 제품)에 구성된 링크가 목록 목록에 추가됩니다 **[!UICONTROL Fields to update]**. 또한 거래 날짜에 해당하는 필드가 이 목록에 올바르게 추가되어 있는지 확인해야 합니다.

   ![](assets/reconciliation_example5.png)

   ![](assets/reconciliation_example4.png)
