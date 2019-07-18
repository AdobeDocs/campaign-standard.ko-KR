---
title: 이메일에서 동적 컨텐츠 정의
seo-title: 이메일에서 동적 컨텐츠 정의
description: 이메일에서 동적 컨텐츠 정의
seo-description: 다음 단계에 따라 Adobe Campaign 표현식 편집기를 통해 정의된 조건에 따라 이메일에서 동적으로 다른 컨텐츠를 표시합니다.
page-status-flag: 정품 인증 안 함
uuid: B 1 C 5013 F -3201-4239-8202-511 A 6902 D 604
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: defining-conditional-content
discoiquuid: D 0 D 009 A 5-6022-433 E-ACDF -2 B 51 A 243 A 5 C 9
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Defining dynamic content in an email{#defining-dynamic-content-in-an-email}

이메일에서 표현식 편집기를 통해 정의된 조건에 따라 수신자에게 동적으로 표시되는 다양한 컨텐츠를 정의할 수 있습니다. 예를 들어 동일한 이메일에서 각 프로필에 연령 범위에 따라 다른 메시지를 받도록 할 수 있습니다.

Defining dynamic content is different from [defining visibility conditions](../../designing/using/defining-a-visibility-condition.md).

1. 조각, 구성 요소 또는 요소를 선택합니다. 이 예에서는 이미지를 선택합니다.
1. Click the **[!UICONTROL Dynamic content]** icon from the contextual toolbar.

   ![](assets/dynamic_content_2.png)

   The **[!UICONTROL Dynamic content]** section appears in the palette on the left.

   ![](assets/dynamic_content_3.png)

   기본적으로 이 섹션에는 다음 두 가지 요소가 포함됩니다. 기본 변형 및 새 변형.

   >[!NOTE]
   >
   >콘텐츠는 항상 기본 변형을 가져야 합니다. 삭제할 수 없습니다.

1. **[!UICONTROL Edit]** 단추를 클릭하여 첫 번째 대체 변형에 대한 표시 조건을 정의합니다.

   ![](assets/dynamic_content_4.png)

1. 레이블을 지정하고 조건으로 설정할 필드를 선택합니다. For example, from the **[!UICONTROL General]** node, select the **[!UICONTROL Age]** field

   ![](assets/dynamic_content_5.png)

1. 필터링 조건을 설정합니다. 예를 들어 18 세에서 25 세 사이의 연령대에게 다른 콘텐츠를 표시할 수 있습니다.

   ![](assets/dynamic_content_6.png)

1. 모든 조건이 설정되면 조건이 적용될 순서를 정의하고 변경 내용을 저장합니다.

   ![](assets/dynamic_content_7.png)

   컨텐츠가 [위에서 아래로] 순으로 팔레트에 표시됩니다. For more on priorities, refer to [this section](../../designing/using/defining-dynamic-content-in-an-email.md#order-of-priority).

1. 방금 정의한 변형에 대한 새 이미지를 업로드합니다.

   ![](assets/dynamic_content_8.png)

   18 세에서 25 세 사이의 수신자는 새 이미지를 보게 됩니다.

   ![](assets/dynamic_content_10.png)

1. Click **[!UICONTROL Add a condition]** to add a new content and its linked rule.

   ![](assets/dynamic_content_9.png)

   예를 들어, 26 ~ 35 세 연령대에게 표시할 다른 이미지를 추가할 수 있습니다.

1. 이메일의 다른 요소도 동적으로 표시되므로 유사하게 진행하십시오. 텍스트, 단추, 조각 등이 될 수 있습니다. 변경 내용을 저장합니다.

>[!CAUTION]
>
>메시지를 준비한 후 발송하기 전에 인증서를 사용하여 테스트합니다. 이렇게 하지 않으면 일부 오류가 감지되지 않고 이메일을 보내지 못할 수 있습니다.

**관련 항목:**

* [증거 자료 전송](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs)
* [고급 표현식 편집](../../automating/using/editing-queries.md#about-query-editor)

## Order of priority {#order-of-priority}

표현식 편집기에서 동적 컨텐츠를 정의할 때 우선 순위는 다음과 같습니다.

1. You define two different dynamic contents with **two different conditions**, for example:

   **조건 1:** 프로필의 성관계는 남성입니다.

   **조건 2:** 프로필은 20 ~ 30 세 연령대입니다.

   ![](assets/delivery_content_61.png)

   데이터베이스의 일부 프로필은 두 가지 조건에 해당되지만, 하나의 동적 컨텐츠가 포함된 하나의 이메일만 전송될 수 있습니다.

1. 따라서 동적 컨텐츠에 대한 우선 순위를 정의해야 합니다. A condition with an order of priority of **1** (and therefore the corresponding dynamic content) will be sent to a profile even if another condition whose priority order is **2** or **3** is also met by this profile.

   ![](assets/delivery_content_62.png)

동적 컨텐츠당 우선 순위를 하나만 정의할 수 있습니다.
