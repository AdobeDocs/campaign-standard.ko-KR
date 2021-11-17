---
title: 데이터 모델 변경 모니터링
description: Adobe Campaign 데이터 모델을 진단하는 방법을 알아봅니다.
audience: developing
content-type: reference
topic-tags: about-custom-resources
feature: Data Model
role: Developer
level: Experienced
exl-id: ced9a897-47e9-4128-84fb-35660c553cd4
source-git-commit: 5fef74296a4790102c75e609c270e52d5ead1d58
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 5%

---

# 데이터 모델 변경 모니터링{#monitoring-data-model-changes}

에서 **[!UICONTROL Diagnosis]** 메뉴에서 응용 프로그램에서 생성한 기술 객체를 확인하여 분석할 수 있습니다.

>[!NOTE]
>
>이 메뉴의 스크린은 읽기 전용입니다.

![](assets/diagnostic.png)

다음 유형의 객체를 볼 수 있습니다.

* 데이터 스키마
* 웹 페이지
* 필터
* 탐색
* 구성 요소
* 배치 작업

목록 구성을 변경할 수 있습니다.

* 열을 추가 및 제거할 수 있습니다.
* 열 이름을 정의할 수 있습니다.
* 목록에서 열의 표시 순서를 정의할 수 있습니다.
* 목록에서 값의 정렬 순서를 선택할 수 있습니다.

목록을 필터링할 수 있습니다.

* 기본 데이터 스키마, 웹 페이지, 필터 및 탐색 개체를 포함하거나 제외할 수 있습니다.
* 개체 이름을 기준으로 개체를 검색할 수 있습니다.
* 상태, 시작 날짜 및 종료 날짜에 따라 배치 작업을 필터링할 수 있습니다.

표시된 목록을 쉼표로 구분된 값으로 TXT 형식의 파일로 다운로드할 수 있습니다.

선택한 객체의 세부 정보를 볼 수 있습니다.

예를 들어 이 기능을 사용하여 기본 제공 필터의 필터링 기준을 볼 수 있습니다. 이 예는 기본 제공 필터의 필터링 기준에 대해 표시되는 코드를 보여줍니다.

```xml
<where displayFilter="Has clicked an offer">
  <condition boolOperator="AND" enabledIf="$(offer) != ''" expr="trackingLog" internalId="1" setOperator="EXISTS">
    <condition boolOperator="AND" expr="[url/offer] = $RestKey(offer)" internalId="2"/>
    <condition boolOperator="AND" expr="[@url-id] != 1" internalId="3"/>
  </condition>
</where>
```

![](assets/diagnosis_filter_criteria.png)