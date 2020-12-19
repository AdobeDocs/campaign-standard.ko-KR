---
solution: Campaign Standard
product: campaign
title: 외부 신호 및 데이터 가져오기
description: 다음 예제에서는 데이터 가져오기에 사용되는 외부 신호 활동을 보여 줍니다.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: signal,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 79%

---


# 외부 신호 및 데이터 가져오기 {#external-signal-data-import}

다음 예제는 일반적인 사용 사례에서 **[!UICONTROL External signal]** 활동을 보여줍니다. 데이터 가져오기는 소스 워크플로우에서 수행됩니다. 가져오기가 완료되고 데이터베이스가 업데이트되면 두 번째 워크플로우가 트리거됩니다. 이 두 번째 워크플로우는 가져온 데이터에 대한 집계를 업데이트하는 데 사용됩니다.

소스 워크플로우는 다음과 같이 표시됩니다.

* [파일 로드](../../automating/using/load-file.md) 활동은 새 구매 데이터가 포함된 파일을 업로드합니다. 구매 데이터가 기본적으로 데이터 마트에 없으므로 이에 따라 [데이터베이스가 확장](../../developing/using/data-model-concepts.md)되었습니다.

   예제:

   ```
   tcode;tdate;customer;product;tamount
   aze123;21/05/2015;dannymars@example.com;A2;799
   aze124;28/05/2015;dannymars@example.com;A7;8
   aze125;31/07/2015;john.smith@example.com;A7;8
   aze126;14/12/2015;john.smith@example.com;A10;4
   aze127;02/01/2016;dannymars@example.com;A3;79
   aze128;04/03/2016;clara.smith@example.com;A8;149
   ```

* [조정](../../automating/using/reconciliation.md) 활동은 가져온 데이터와 데이터베이스 사이에 링크를 만들어 트랜잭션 데이터가 프로필과 제품에 적절하게 연결되도록 합니다.
* [데이터 업데이트](../../automating/using/update-data.md) 활동은 수신 데이터로 데이터베이스의 트랜잭션 리소스를 삽입하고 업데이트합니다.
* [End](../../automating/using/start-and-end.md) 활동은 집계를 업데이트하는 데 사용되는 대상 워크플로우를 트리거합니다.

![](assets/signal_example_source1.png)

대상 워크플로우는 다음과 같이 표시됩니다.

* [외부 신호](../../automating/using/external-signal.md) 활동은 소스 워크플로우가 성공적으로 완료될 때까지 기다립니다.
* [쿼리](../../automating/using/query.md#enriching-data) 활동은 프로필을 타겟팅하고 마지막 구매 날짜를 검색하기 위해 컬렉션 집합으로 프로필을 보강합니다.
* [데이터 업데이트](../../automating/using/update-data.md) 활동은 전용 사용자 지정 필드에 추가 데이터를 저장합니다. 프로필 리소스가 **마지막 구매 날짜** 필드를 추가하도록 확장되었습니다.

![](assets/signal_example_source2.png)
