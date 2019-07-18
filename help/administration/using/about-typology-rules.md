---
title: 유형 규칙 정보
seo-title: 유형 규칙 정보
description: 유형 규칙 정보
seo-description: Adobe Campaign에서 유형 분석 규칙이 작동하는 방식을 살펴볼 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: A 98 EBC 36-172 D -4 F 46-B 6 EE-B 2636 A 1007 C 9
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 관리
content-type: 참조
topic-tags: working-with-tyatype-rules
discoiquuid: 2590 d 94 c -51 ef -4 c 0 f-b 1 ec-c 2837 e 94 da 40
context-tags: tyatype, 개요; Tyatype gyrule, main; Tyatype 규칙, 개요
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# About typology rules{#about-typology-rules}

유형 유형은 Target, 컨텐츠 및 다음 요소의 구성을 검증할 수 있는 메시지 분석 단계 중에 실행되는 규칙 세트입니다. 주제, URL, 이미지, 구독 취소 링크, 증빙 크기 등은

Adobe Campaign에서 각 메시지에는 유형 분석에 대한 링크가 포함되어 있습니다. This link is defined in the advanced parameters of the delivery template's properties (for more on this, refer to the [Preparation](../../administration/using/configuring-email-channel.md#preparation) section).

>[!NOTE]
>
>각 메시지에는 하나의 유형만 할당할 수 있습니다.

For each typology, the **[!UICONTROL Typology rules]** section lists the set of rules for this typology.

![](assets/typology_typo-rule-list.png)

## Managing typologies {#managing-typologies}

애플리케이션에서 기본적으로 여러 유형의 유형이 제공됩니다. 필요에 따라 고유한 유형을 만들거나 기존 유형을 수정할 수 있습니다.

1. Access the **[!UICONTROL List of typologies]** from the **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Typologies]** menu.
1. 유형 유형을 선택하여 내용과 속성을 수정하거나 새 속성을 만듭니다.

   ![](assets/typology_list.png)

1. 유형 유형을 정의합니다. 유형유형은 표준 또는 필터링 유형일 수 있습니다.
1. **[!UICONTROL Add an element]** 단추를 사용하여 필요한 유형 지정 규칙을 추가하거나 사용하지 않을 유형을 제거합니다.

   주어진 유형에 대한 규칙이 적용되는 순서를 수정할 수 있습니다. 이렇게 하려면 요소를 이동하여 화면에 나타나는 순서를 수정합니다. 그러면 실행 순서에 해당하는 숫자가 자동으로 다시 계산됩니다. The rule application mode is presented in the [Typology rules execution order](../../administration/using/about-typology-rules.md#typology-rules-execution-order) section.

   이 화면에 표시되는 규칙은 읽기 전용 모드로 액세스할 수 있습니다.

유형을 사용할 준비가 되었습니다. 메시지 속성 또는 메시지 템플릿 속성에서 선택할 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL IP affinity]** 이 필드에서 구성에 따라 친화성을 관리할 수 있습니다. 이것은 인스턴스의 구성 파일에 정의됩니다. 친화성을 사용하려면 관리자에게 문의하십시오.

## Typology rules {#typology-rules}

유형 규칙은 메시지 준비 중에 적용되는 비즈니스 규칙입니다. 메시지를 유효하고 품질 기준을 충족하는지 확인하는 데 사용됩니다. 또한 대상 대상의 각 구성원이 메시지를 받을 수 있는지 여부도 확인합니다.

Typology rules are available under the **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Typologies]** &gt; **[!UICONTROL Typology rules]** menu.

두 가지 유형의 규칙이 있습니다.

* **필터링** 규칙: 이미 지정된 수의 이메일 또는 이미 전송된 프로필과 같이 쿼리에 정의된 기준에 따라 메시지 타겟의 한 부분을 제외시킬 수 있도록 해줍니다. See [Filtering rules](../../administration/using/filtering-rules.md).
* **피로** 규칙: 요청되지 않도록 프로필당 최대 메시지 수를 정의할 수 있습니다. [피로 규칙을 참조하십시오](../../administration/using/fatigue-rules.md).
* **제어** 규칙: 문자 표시, SMS 메시지 크기, 주소 형식 등 메시지가 전송되기 전에 사용자가 메시지의 유효성을 확인하고 품질을 확인할 수 있도록 합니다. [제어 규칙을 참조하십시오](../../administration/using/control-rules.md).

유형 유형은 하나의 채널에만 적용하거나 모든 채널에 적용할 수 있습니다.

![](assets/typology_channel.png)

In the **[!UICONTROL Properties]** of a typology rule, you can set its execution order. 여러 규칙을 적용해야 하는 경우 각 규칙의 실행 순서에 따라 먼저 처리할 규칙이 결정됩니다. For more on this, refer to the [Typology rules execution order](../../administration/using/about-typology-rules.md#typology-rules-execution-order) section.

![](assets/typology_rule-active.png)

A typology rule can be deactivated through its **[!UICONTROL Properties]** if you do not want the rule to be applied at the moment that the messages concerned by the rule are analyzed.

![](assets/typology_rule-order.png)

**[!UICONTROL Targeting context]** 카테고리에서는 타깃팅할 데이터에 따라 **타깃팅 차원** 및 **필터링 차원을** 선택할 수 있습니다.

By default, filtering is carried out on the **[!UICONTROL Profiles]**. For example, if the rule is aimed at a mobile application, the **[!UICONTROL Filtering dimension]** can be changed to **[!UICONTROL Subscriptions to an application]**.

![](assets/typology_rule-order_2.png)

>[!NOTE]
>
>제어 규칙의 컨텐츠는 수정할 수 없으므로 기본적으로 사용되는 규칙을 필터링합니다.

## Typology rules execution order {#typology-rules-execution-order}

유형 지정 규칙은 타깃팅, 분석 및 메시지 개인화 단계 중에 지정된 순서로 실행됩니다.

표준 작업 모드에서는 규칙이 다음 시퀀스에 적용됩니다.

1. 타깃팅 시작 시 적용되는 경우 규칙 제어
1. 필터링 규칙:

   * 주소 자격 조건에 대한 기본 애플리케이션 규칙: 정의된 주소/확인되지 않은 주소/블랙리스트에 추가된 주소/격리된 주소/주소 품질.
   * 사용자가 정의한 필터링 규칙.

1. 타깃팅 끝에 적용되는 경우 규칙 제어
1. 개인화 시작 시 적용되는 규칙을 제어합니다.
1. 개인화 끝에 적용되는 경우 규칙 제어

하지만 각 유형마다 동일한 유형의 규칙 실행 순서를 조정할 수 있습니다. 실제로 동일한 메시지 처리 단계 동안 여러 규칙을 실행할 때 적용되는 순서를 선택할 수 있습니다.

예를 들어, 실행 순서가 숫자 20에 위치하는 필터링 규칙은 실행 순서가 숫자 30에 위치한 필터링 규칙 전에 실행됩니다.
