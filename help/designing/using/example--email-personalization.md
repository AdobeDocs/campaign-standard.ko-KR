---
title: '" 예: 이메일 개인화 "'
seo-title: '" 예: 이메일 개인화 "'
description: '" 예: 이메일 개인화 "'
seo-description: 프로파일에 따라 다이내믹한 컨텐츠와 텍스트를 사용하여 이메일을 개인화하는 전체 예를 살펴보십시오.
page-status-flag: 정품 인증 안 함
uuid: 3 D 30213 C -474 F -4 E 5 F -8688-9260 EA 2 E 2583
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: 맞춤형 컨텐츠
discoiquuid: D 1 B 618 AC-A 842-41 E 8-9 BA 6-7 A 50 F 7315 B 02
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Example: Email personalization{#example-email-personalization}

이 예에서는 마케팅 서비스 팀의 구성원이 일부 클라이언트에게 특별 오퍼가 있음을 알리는 이메일을 만들었습니다. 팀원은 고객의 연령에 따라 이메일을 개인화하기로 결정했습니다. 18 세에서 27 세 사이의 클라이언트는 27 세 이상의 클라이언트가 받을 수 있는 이미지와 슬로건이 포함된 이메일을 받게 됩니다.

이메일은 다음과 같이 만들어집니다.

* 동적 컨텐츠가 이미지에 적용되고 이러한 동적 컨텐츠가 연령 범위에 따라 구성됩니다.

   ![](assets/delivery_content_43.png)

   Adding and configuring dynamic content is detailed in the [Defining dynamic content in an email](../../designing/using/defining-dynamic-content-in-an-email.md) section.

* 개인화 필드와 동적 컨텐츠가 텍스트에 적용됩니다. 프로필의 연령 범위에 따라 이메일은 프로필의 이름 또는 프로필의 제목과 성으로 시작합니다.

   ![](assets/delivery_content_44.png)

   Adding and configuring the personalization fields is detailed in the [Inserting a personalization field](../../designing/using/inserting-a-personalization-field.md) section.

## Configuring images {#configuring-images}

이 예에서 이미지에 적용된 동적 컨텐츠는 다음과 같이 구성됩니다.

**18-27 세 타깃팅:**

1. **[!UICONTROL Properties]** 팔레트에서 동적 콘텐츠를 선택하고 **[!UICONTROL Edit]** 버튼을 클릭합니다.

   ![](assets/delivery_content_48.png)

1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.

   ![](assets/delivery_content_49.png)

1. **크거나 같음** 연산자를 선택한 다음 **18** 를 입력하여 **18** 개 이상의 표현식을 만듭니다.

   ![](assets/delivery_content_50.png)

1. Add a new **[!UICONTROL Age]** condition.

   Select the **Less than or equal to** operator followed by 27 in the value field to create the **younger than 27** expression.

   ![](assets/delivery_content_51.png)

1. 변경 사항을 확인합니다.

**27 이전 이상의 프로필을 타깃팅하려면:**

1. 팔레트에서 동적 콘텐츠를 선택하고 편집합니다.
1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.
1. Add the **Greater than** operator followed by 27 in the value field to create the **older than 27** expression.

   ![](assets/delivery_content_52.png)

1. 변경 사항을 확인합니다.

동적 컨텐츠가 올바르게 구성됩니다.

## Configuring text {#configuring-text}

이 예에서, 텍스트에 적용된 동적 컨텐츠는 다음과 같이 구성됩니다.

**18-27 사이의 오래된 프로필을 타깃팅하려면:**

1. 원하는 구조 구성 요소를 선택하고 동적 컨텐트를 추가합니다.
1. 동적 컨텐츠를 편집하고 타깃팅 표현식을 구성합니다. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**.

   ![](assets/delivery_content_53.png)

1. In the list that appears, select the **[!UICONTROL First name]** field and confirm.

   ![](assets/delivery_content_54.png)

1. 개인화 필드는 선택한 다이내믹 컨텐츠에 완벽하게 삽입됩니다.

**27 이전 이상의 프로필을 타깃팅하려면:**

1. 원하는 구조 구성 요소를 선택하고 동적 컨텐트를 추가합니다.
1. 동적 컨텐츠를 편집하고 타깃팅 표현식을 구성합니다. Refer to [Configuring images](../../designing/using/example--email-personalization.md#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**.
1. Select **[!UICONTROL Title]** from the drop-down list.
1. Proceed similarly to add the **[!UICONTROL Last name]** field.

   ![](assets/delivery_content_56.png)

이제 개인화 필드를 선택한 동적 컨텐츠에 완벽하게 삽입해야 합니다.

## Previewing emails {#previewing-emails}

Previewing allows you to check that the personalization fields and the dynamic contents are configured correctly before sending the **[!UICONTROL Proofs]**. 미리 보기 중에 이메일 타겟에 해당하는 다른 테스트 프로필을 선택할 수 있습니다.

테스트 프로필이 없으면 기본적으로 표시되는 이메일은 다음과 같습니다.

![](assets/delivery_content_45.png)

이메일에 슬로건에 개인화 필드가 없고 기본 이미지가 사용됩니다.

첫 번째 테스트 프로필은 18 ~ 27 범위의 클라이언트에게 해당합니다. 이 프로필을 선택하면 다음 이메일이 표시됩니다.

![](assets/delivery_content_46.png)

18-27 년 이전 표현식 (특히 프로필 이름) 에 해당하는 개인화 필드가 올바르게 구성되며 이미지에 따라 이미지가 변경되었었습니다.

두 번째 프로필은 27 세 이상의 클라이언트에게 해당하고 다음 이메일을 생성합니다.

![](assets/delivery_content_47.png)

The image has changed thanks with the dynamic content, and the 슬로건이 이 타깃팅된 공개적으로 정의된 더 공식적인 슬로건이 되었습니다.

**관련 항목:**

* [대상자 만들기](../../audiences/using/creating-audiences.md)
* [보내기 준비](../../sending/using/preparing-the-send.md)

