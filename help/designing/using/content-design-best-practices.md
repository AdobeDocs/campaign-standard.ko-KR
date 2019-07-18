---
title: 컨텐츠 디자인 모범 사례
seo-title: 컨텐츠 디자인 모범 사례
description: 컨텐츠 디자인 모범 사례
seo-description: 편집자의 최적 작업을 보장하기 위해 이러한 지침을 참조하십시오.
page-status-flag: 정품 인증 안 함
uuid: ad 74 f 49 d -999 f -4140-89 b 0-d 1 ead 8642 d 89
contentOwner: Sauviat
products: sg_ campaign/standard
audience: designing
content-type: 참조
topic-tags: About-content-design
discoiquuid: D 33 F 5 F 14-A 4 E 3-4327-BD 16-EB 3135 A 32076
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Content design best practices{#content-design-best-practices}

편집자의 최적의 작업을 위해서는 다음 지침을 따르는 것이 좋습니다.

* SCSS 스타일 시트는 지원되지 않습니다. HTML 콘텐츠가 포함된 ZIP 파일을 가져오는 경우 일반 CSS를 사용합니다.
* When editing **email content**:

   메시지를 보내기 전에 미리 볼 수 있습니다. Adobe Campaign 에서는 Litmus를 사용하여 이메일 렌더링을 테스트하는 방법을 제공합니다. For more on this, see [Email rendering](../../sending/using/email-rendering.md).

* When editing **landing page content**:

   * Adobe Campaign에서 HTML 페이지 템플릿을 가져오기 전에 템플릿이 열리고 다양한 브라우저에서 올바르게 표시되는지 확인하십시오.
   * HTML 페이지에 JavaScript 스크립트가 포함되어 있으면 편집기 외부에서 오류 없이 실행해야 합니다. 일반적으로 메시지 내용에서 스크립트를 사용하여 이메일 클라이언트에 의해 올바르게 처리되었는지 확인하십시오.
   * When building a template, we recommend adding a **'type'** attribute to  tags. 이 정보는 편집기에 의해 처리되며 사용자가 웹 애플리케이션을 구성할 때 양식 필드에 데이터베이스 필드를 연결할 수 있도록 도와줍니다.

      템플릿의 HTML 코드 예:

      ```
      <input id="email" type="email" name="email"/>
      ```

      The official list of 'type' attributes is available at the following address: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp)

More design and general best practices regarding messages are presented in the following Adobe Campaign step-by-step guide: [Delivery best practices with Adobe Campaign](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).
