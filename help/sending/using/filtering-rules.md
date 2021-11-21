---
title: 필터링 규칙
description: 필터링 규칙을 사용하여 메시지 대상자를 세분화합니다.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
feature: Typology Rules
role: User
level: Intermediate
exl-id: 43e97f3c-ed82-4fcc-ac0d-fcee6a22da35
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 3%

---

# 필터링 규칙 {#filtering-rules}

Filtering rules allow you to exclude one part of the message target according to criteria defined in a query, such as quarantined profiles or profiles that have already been sent a certain number of emails.

## 기본 필터링 유형화 규칙 {#default-filtering-typology-rules}

The table below provides information about out-of-the-box filtering rules, as well as their related channels.

| 레이블 | 채널 | 설명 |
| ---------|----------|---------|
| **[!UICONTROL Address not specified]** | 모두 | 지정된 주소(이메일, 우편 주소 등)가 없는 대상 모집단을 제외합니다. )을 클릭하여 제품에서 사용할 수 있습니다. |
| **[!UICONTROL Address on denylist]** | 모두 | 에 있는 주소를 차단 목록 제외합니다. |
| **[!UICONTROL Duplicate]** | 모두 | 대상 모집단에 따라 중복을 제외합니다 **[!UICONTROL Address]** 필드. |
| **[!UICONTROL Exclude mobile applications]** | 모바일 애플리케이션 | 메시지에 정의된 모바일 애플리케이션과 일치하지 않는 앱 구독을 제외합니다. |
| **[!UICONTROL Exclude mobile applications for In-App]** | 인앱 | 메시지에 정의된 모바일 애플리케이션(인앱 템플릿)과 일치하지 않는 앱 구독을 제외합니다. |
| **[!UICONTROL Exclude mobile applications for In-App broadcast]** | 인앱 | 메시지에 정의된 모바일 애플리케이션과 일치하지 않는 앱 구독(인앱 브로드캐스트 템플릿)을 제외합니다 |
| **[!UICONTROL Exclude mobile applications for Push]** | 모바일 애플리케이션 | 메시지에 정의된 모바일 애플리케이션과 일치하지 않는 앱 구독(푸시용)을 제외합니다 |
| **[!UICONTROL Quarantined address]** | 모두 | 격리된 주소를 제외합니다. |
| **[!UICONTROL Target limited in size]** | 모두 | 대상에 대한 최대 게재 크기에 도달했는지 확인합니다. 배달 제한 옵션이 활성화된 DM 게재에 적용됩니다. |

Additionally to these default filtering rules, two exclusion rules are available:

* **[!UICONTROL Exclusion of addresses]** ( **[!UICONTROL addressExclusions]** )
* **[!UICONTROL Exclusion of domains]** ( **[!UICONTROL domainExclusions]** ).

During the email analysis, these rules compare the recipient email addresses with the forbidden addresses or domain names contained in an encrypted global suppression list managed in the deliverability instance. If there is a match, the message is not sent to that recipient.

악의적인 활동, 특히 Spamtrap을 차단 목록 사용하여에 추가되지 않기 위한 것입니다. 예를 들어, Spamtrap을 사용하여 웹 양식 중 하나를 구독하는 경우 확인 이메일이 자동으로 해당 Spamtrap로 전송되고 이로 인해 주소가 자동으로에 추가됩니다차단 목록.

>[!NOTE]
>
>전역 제외 목록에 포함된 주소 및 도메인 이름은 숨겨집니다. 제외된 수신자 수만 게재 분석 로그에 표시됩니다.

## 필터링 규칙 만들기 {#creating-a-filtering-rule}

필요에 따라 고유한 필터링 규칙을 만들 수 있습니다. 예를 들어 18세 미만의 구독자가 통신을 받지 않도록 뉴스레터의 대상 모집단을 필터링할 수 있습니다.

필터링 유형화 규칙을 만들려면 다음 단계를 수행합니다.

1. 새 유형화 규칙을 만듭니다. 유형화 규칙을 만드는 주요 단계는 [이 섹션](../../sending/using/managing-typology-rules.md).

1. 을(를) 선택합니다 **[!UICONTROL Filtering]** 규칙 유형을 선택한 다음, 원하는 채널을 지정합니다.

1. 에서 **[!UICONTROL Filtering criteria]** 탭에서 구독을 선택합니다 **[!UICONTROL Subscription]** 카테고리.

   ![](assets/typology_create-rule-subscription.png)

1. 에서 **[!UICONTROL Explorer]** 쿼리 편집기의 탭에서 을(를) 끌어서 놓습니다 **[!UICONTROL Subscriber]** 노드가 화면 주 부분에 있습니다.

   ![](assets/typology_create-rule-subscriber.png)

1. 을(를) 선택합니다 **[!UICONTROL Age]** 구독자의 나이가 18 이상이 되도록 필터링 조건을 정의하고 정의합니다.

   ![](assets/typology_create-rule-age.png)

1. 에서 **[!UICONTROL Typologies]** 탭에서 이 규칙을 유형화에 연결합니다.

   ![](assets/typology_create-rule-typology.png)

1. Make sure that the typology is selected in the delivery or delivery template that you want to use. 이 작업에 대한 자세한 정보는 [이 섹션](../../sending/using/managing-typologies.md#applying-typologies-to-messages)을 참조하십시오.

   ![](assets/typology_template.png)

이 규칙을 메시지에 사용할 때마다 미성년자로 간주되는 가입자는 자동으로 제외됩니다.

## Configuring filtering rules&#39; targeting context {#configuring-filtering-rules-targeting-context}

Campaign Standard을 통해  **타깃팅** 및 **필터링** 타겟팅하려는 데이터에 따라 사용할 차원입니다.

이렇게 하려면 유형화 규칙의 속성을 연 다음 **[!UICONTROL Advanced information]** 섹션을 참조하십시오.

기본적으로 필터링은 **[!UICONTROL Profiles]**. 예를 들어, 규칙이 모바일 애플리케이션을 타깃팅하는 경우 **[!UICONTROL Filtering dimension]** 을(를) (으)로 변경할 수 있습니다. **[!UICONTROL Subscriptions to an application]**.

![](assets/typology_rule-order_2.png)

## 필터링 규칙의 적용 제한 {#restricting-the-applicability-of-a-filtering-rule}

전송할 메시지에 따라 필터링 규칙의 적용을 제한할 수 있습니다.

1. In the typology rule&#39;s **[!UICONTROL Application criteria]** tab, uncheck the **[!UICONTROL Apply the rule on all deliveries]** option, which is enabled by default.

   ![](assets/typology_limit.png)

1. 쿼리 편집기를 사용하여 필터를 정의합니다. 예를 들어 지정된 단어로 시작하거나 ID에 특정 문자가 포함된 메시지에만 규칙을 적용할 수 있습니다.

   ![](assets/typology_limit-rule.png)

이 경우 규칙은 정의된 기준에 해당하는 메시지에만 적용됩니다.
