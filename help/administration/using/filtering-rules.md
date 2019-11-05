---
title: 필터링 규칙
description: 필터링 규칙을 사용하여 메시지 대상자를 세분화할 수 있습니다.
page-status-flag: 활성화 안 함
uuid: ed3eea62-3a47-4318-ae22-d82aa85748f
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 관리
content-type: reference
topic-tags: working-with-typical-rules
discoiquuid: 7ddaf36c-74e6-4501-b3eb-3d005aaa6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 필터링 규칙{#filtering-rules}

필터링 규칙을 사용하면 격리된 프로필 또는 특정 수의 이메일을 이미 보낸 프로필과 같이 쿼리에 정의된 기준에 따라 메시지 대상의 한 부분을 제외할 수 있습니다.

예를 들어 18세 미만의 구독자가 통신을 받지 않도록 뉴스레터 가입자를 필터링할 수 있습니다.

## 필터링 규칙 만들기 {#creating-a-filtering-rule}

1. 모든 통신 **채널에** 적용할 수 있는 필터링 유형 규칙을 만듭니다.

   ![](assets/typology_create-rule.png)

1. 탭의 **[!UICONTROL Filtering criteria]** 카테고리에서 가입을 선택합니다 **[!UICONTROL Subscription]** .

   ![](assets/typology_create-rule-subscription.png)

1. 쿼리 편집기의 **[!UICONTROL Explorer]** 탭에서 **[!UICONTROL Subscriber]** 노드를 화면 주 부분으로 드래그하여 놓습니다.

   ![](assets/typology_create-rule-subscriber.png)

1. 가입자의 나이가 18 이상이 되도록 **[!UICONTROL Age]** 필드를 선택하고 필터링 조건을 정의합니다.

   ![](assets/typology_create-rule-age.png)

1. 탭에서 이 규칙을 **[!UICONTROL Typologies]** 유형 분석에 연결합니다.

   ![](assets/typology_create-rule-typology.png)

1. 사용할 배달 템플릿에서 문제의 유형이 선택되어 있는지 확인합니다.

   ![](assets/typology_template.png)

   >[!NOTE]
   >
   >게재 템플릿에 액세스하려면 탐색 메뉴에서 **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** 를 선택합니다. 이 템플릿은 Adobe Campaign 로고를 통해 액세스할 수 있습니다.

이 규칙이 메시지에 사용될 때마다 미성년자로 간주되는 가입자는 자동으로 제외됩니다.

## 필터링 규칙의 적용 가능성 제한 {#restricting-the-applicability-of-a-filtering-rule}

보낼 메시지에 따라 필터링 규칙의 적용 가능성을 제한할 수 있습니다.

1. 분류 규칙의 **[!UICONTROL Application criteria]** 탭에서 기본적으로 활성화되는 **[!UICONTROL Apply the rule on all deliveries]** 옵션을 선택 해제합니다.

   ![](assets/typology_limit.png)

1. 쿼리 편집기를 사용하여 필터를 정의합니다. 예를 들어 레이블이 지정된 단어로 시작하거나 ID에 특정 문자가 포함된 메시지만 적용할 수 있습니다.

   ![](assets/typology_limit-rule.png)

이 경우 규칙은 정의된 기준에 해당하는 메시지만 적용됩니다.

## 기본 제공 가능성 제외 규칙 {#default-deliverability-exclusion-rules}

기본적으로 두 개의 필터링 규칙을 사용할 수 있습니다.( **[!UICONTROL Exclusion of addresses]** ) 및 **[!UICONTROL addressExclusions]** ( **[!UICONTROL Exclusion of domains]** **[!UICONTROL domainExclusions]** ). 이메일 분석 중에 이러한 규칙은 받는 사람 이메일 주소와 배달 가능성 인스턴스에서 관리되는 암호화된 전역 억제 목록에 포함된 금지된 주소 또는 도메인 이름을 비교합니다. 일치하는 메시지가 있으면 해당 받는 사람에게 메시지가 전송되지 않습니다.

이는 악성 활동, 특히 Spamtrap 사용으로 인해 블랙리스트에 추가되지 않도록 하기 위한 것입니다. 예를 들어 웹 양식 중 하나를 통해 구독하는 데 Spamtrap을 사용하는 경우 확인 이메일이 자동으로 해당 Spamtrap으로 전송되어 사용자의 주소가 자동으로 블랙리스트에 추가됩니다.

>[!NOTE]
>
>글로벌 억제 목록에 포함된 주소 및 도메인 이름은 숨겨집니다. 제외된 받는 사람 수만 배달 분석 로그에 표시됩니다.

