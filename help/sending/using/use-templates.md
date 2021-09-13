---
title: 게재 템플릿 사용
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: '"게재 템플릿을 사용하면 대부분의 일반적인 활동에 대해 준비된 시나리오를 제공하여 효율성을 높일 수 있습니다."'
feature: Deliverability
role: User
level: Intermediate
exl-id: ca134a7f-9035-4885-b4cb-1170b6ec10cc
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 10%

---

# 템플릿 사용 {#use-templates}

게재 템플릿을 사용하면 대부분의 일반적인 활동 유형에 대해 준비된 시나리오를 제공하여 효율성을 높일 수 있습니다. 마케터는 템플릿을 사용하여 짧은 시간에 최소한의 사용자 지정으로 새 캠페인을 배포할 수 있습니다.

[이 섹션](../../start/using/marketing-activity-templates.md)에서 게재 템플릿에 대해 자세히 알아보십시오.

## 게재 템플릿 시작 {#gs-templates}

[게재 템플릿](../../start/using/marketing-activity-templates.md#creating-a-new-template)을(를) 사용하면 사용자의 요구 사항에 맞는 기술 및 기능 속성 세트를 정의하고 향후 게재에 다시 사용할 수 있습니다. 그런 다음 시간을 절약하고 필요한 경우 게재를 표준화할 수 있습니다.

Adobe Campaign에서 여러 브랜드를 관리하는 경우, 브랜드당 하나의 하위 도메인이 있는 것이 좋습니다. 예를 들어 은행은 각 지역 기관에 해당하는 여러 하위 도메인을 가질 수 있습니다. 블루뱅크 도메인은 은행@ny.bluebank.com, @ma.bluebank.com, @ca.bluebank.com 등이 될 수 있습니다. 하위 도메인당 하나의 게재 템플릿을 사용하면 각 브랜드에 대해 항상 올바른 사전 구성된 매개 변수를 사용할 수 있으므로 오류를 방지하고 시간을 절약할 수 있습니다.

**팁**: Campaign에서 구성 오류가 발생하지 않도록 새 템플릿을 만들지 않고 기본 템플릿을 복제하고 해당 속성을 변경하는 것이 좋습니다.

## 주소 구성

* 이메일을 전송하도록 허용하려면 보낸 사람의 주소가 필수입니다.

* 일부 ISP(Internet Service Providers)는 메시지를 수락하기 전에 보낸 사람 주소의 유효성을 검사합니다.

* 잘못 형성된 주소는 수신 서버에서 거부될 수 있습니다. 올바른 주소가 지정되었는지 확인해야 합니다.

* 주소는 발신자를 명시적으로 식별해야 합니다. 도메인은 자신이 소유하고 발신자에게 등록해야 합니다.

* Adobe은 게재 및 답글에 지정된 주소에 해당하는 이메일 계정을 만드는 것을 권장합니다. 메시징 시스템 관리자에게 문의하십시오.

이메일 템플릿 속성의 **[!UICONTROL Advanced parameters]** 섹션에서 **[!UICONTROL From (email address)]** 필드는 보낸 사람의 주소에 해당합니다.

![](assets/template-parameters.png)

주소 도메인은 사용자가 구성한 하위 도메인과 같아야 합니다.

**[!UICONTROL Reply to]** 필드는 회신에 사용되는 전자 메일 주소와 이름에 해당합니다.

**팁**  - Adobe은 브랜드 고객 지원 센터와 같은 기존 실제 주소를 사용하는 것이 좋습니다. 이 경우 수신자가 답글을 보내면 고객 지원 센터에서 이를 처리할 수 있습니다.

보낸 메시지 헤더에 나타날 보낸 사람의 이름을 변경하려면 전자 메일 디자이너 홈 페이지의 **[!UICONTROL Properties]** 탭(홈 아이콘을 통해 액세스 가능)으로 이동하여 **[!UICONTROL Default sender name]** 블록을 클릭합니다.

![](assets/template-content.png)

게재 열기 비율을 높이려면 브랜드 이름과 같이 수신자가 쉽게 식별할 수 있는 이름을 사용하는 것이 좋습니다.

**팁**  - 수신자의 경험을 더 향상시키기 위해 &quot;Emma from Megastore&quot;와 같은 개인 이름을 추가할 수 있습니다.

발신자 이름 개인화에 대한 자세한 내용은 [이메일 발신자](../../designing/using/subject-line.md#email-sender)를 참조하십시오.

## SMS 발신자 이름 개인화

SMS 템플릿 속성의 **고급 매개 변수** 섹션에서 **시작** 옵션을 사용하면 문자열을 사용하여 SMS 메시지 발신자의 이름을 개인화할 수 있습니다. 발신자명이란 수신자의 휴대전화에서 SMS 메시지를 보낸 사람으로 표시되는 이름입니다.

이 필드가 비어 있는 경우 외부 계정에서 제공하는 소스 번호가 표시됩니다. 소스 번호가 제공되지 않는 경우 짧은 코드가 사용됩니다. 자세한 내용은 [SMS 구성](../../administration/using/configuring-sms-channel.md)을 참조하십시오.

**팁**  - 국가의 발신자 주소 수정에 대한 법률을 확인합니다. 또한 SMS 서비스 공급자에게 문의하여 이 기능을 제공하는지 확인하십시오.

## 컨트롤 그룹 설정

게재를 전송하면 제외된 수신자의 동작을 게재를 받은 수신자와 비교할 수 있습니다. 그런 다음 캠페인의 효율성을 측정할 수 있습니다. 컨트롤 그룹 [이 섹션](../../sending/using/control-group.md)에 대해 자세히 알아보십시오.

## 유형화를 사용하여 필터 또는 제어 규칙을 적용합니다

유형화에는 메시지를 보내기 전에 분석 단계 동안 적용되는 확인 규칙이 포함됩니다.

템플릿 속성의 **[!UICONTROL Advanced parameters]** > **[!UICONTROL Preparation]** 섹션에서 필요에 따라 기본 유형화를 변경합니다.

예를 들어 아웃바운드 트래픽을 더 잘 제어하기 위해 하위 도메인당 하나의 친화성을 정의하고 친화성당 하나의 유형화를 만들어 사용할 수 있는 IP 주소를 정의할 수 있습니다. 인스턴스의 구성 파일에 관심도가 정의됩니다. Adobe Campaign 관리자에게 문의하십시오.

유형화에 대한 자세한 정보는 [이 섹션](../../sending/using/managing-typologies.md)을 참조하십시오.

## 템플릿에 브랜드 연결

브랜드 이미지(예: 브랜드 로고 또는 발신자 주소)와 관련된 전송된 이메일의 매개 변수는 Adobe Campaign에서 중앙에서 관리됩니다. 하나 또는 여러 브랜드를 만들어 게재 템플릿에 연결할 수 있습니다.

Adobe Campaign에서 브랜드 사용 및 구성에 대한 자세한 내용은 브랜딩 을 참조하십시오.

게재 템플릿에 지정된 브랜드를 표시하거나 변경하려면 템플릿의 속성 편집 단추를 선택하고 브랜드의 세부 사항으로 이동합니다.

![](assets/template-brand.png)

템플릿에 브랜드 연결에 대한 자세한 내용은 [이메일을 통해 브랜드 지정](../../administration/using/branding.md#assigning-a-brand-to-an-email)을 참조하십시오.

이 섹션](../../administration/using/branding.md#creating-a-brand)에서 브랜드 [을 만들고 구성하는 방법을 알아봅니다.
