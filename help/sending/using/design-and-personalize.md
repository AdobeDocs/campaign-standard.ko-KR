---
title: 개인화된 콘텐츠 작성
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: 메시지 콘텐츠를 디자인하고 게재를 실행하지 못하도록 할 수 있는 일반적인 문제를 방지하는 방법을 알아봅니다. 
feature: Deliverability
role: User
level: Intermediate
exl-id: 938989c9-ef19-4297-9b8b-c38eb1cec1f0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 7%

---

# 개인화된 콘텐츠 작성 {#build-personalized-content}

메시지 콘텐츠를 디자인할 때 게재를 실행하지 못하도록 할 수 있는 일반적인 문제를 방지하십시오. 대부분의 경우 가능한 오류는 [개인화](../../designing/using/personalization.md), 서식 [기존 콘텐츠 사용](../../designing/using/using-existing-content.md) - 및 [HTML 컨텐츠 변환](../../designing/using/using-existing-content.md#converting-an-html-content) - 및 [이미지](../../designing/using/images.md).

## 개인화 최적화 {#optimize-personalization}

게재를 실행하지 못하도록 하는 일반적인 문제를 방지하고 수신자의 경험을 향상시키기 위해 Adobe Campaign에서 메시지를 개인화할 수 있습니다.

Adobe Campaign 데이터베이스에 저장된 수신자의 데이터를 사용하거나 추적, 랜딩 페이지, 구독 등을 통해 수집할 수 있습니다.
개인화 기본 사항은 [이 섹션](../../designing/using/personalization.md).

일반적으로 개인화와 관련된 오류를 방지하기 위해 메시지 콘텐츠가 제대로 디자인되었는지 확인하십시오.

동적 콘텐츠를 수동으로 추가하여 표현식 편집기에 정의된 조건에 따라 수신자에게 다른 콘텐츠를 표시할 수 있습니다. 동적 콘텐츠를 추가할 때는 선택한 조건을 충족하지 않는 수신자에 대해 항상 기본 변형을 남겨두어야 합니다.
동적 콘텐츠에 대한 자세한 내용은 [이 섹션](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

**팁** - 다른 테스트 프로필로 이메일을 미리 보고 다이내믹 콘텐츠가 올바르게 구성되었는지 확인합니다.

## 최적화된 컨텐츠 작성 {#optimize-content}

이메일을 작성할 때는 아래에 일반적인 모범 사례를 기억하십시오.

* 간편한 디자인 유지

* 모바일 사용자 주의

* 완전히 이미지 기반 이메일을 사용하지 마십시오

* 전자 메일 안전 글꼴 사용

* 특수 문자 인코딩

### 제목 줄

작업 [제목 줄](../../designing/using/subject-line.md) 공개 비율을 개선하려면

* 너무 긴 과목은 피하세요. 최대 50자를 사용할 수 있습니다

* 스팸으로 간주될 수 있는 &quot;무료&quot; 또는 &quot;오퍼&quot;와 같은 반복 단어를 사용하지 마십시오

* 대문자와 &quot;!&quot;, &quot;£&quot;, &quot; uuid&quot;, &quot;$&quot;와 같은 특수 문자를 사용하지 마십시오

### 미러 페이지

항상 미러 페이지 링크를 포함합니다. 기본 위치는 이메일의 맨 위에 있습니다. [자세히 알아보기](../../designing/using/personalization.md#adding-a-content-block)

### 구독 취소 링크

구독 취소 링크는 필수입니다. 이 변수는 표시적이고 유효해야 하며 양식이 작동해야 합니다. 구독 취소 링크 지침 학습 [이 섹션](../../designing/using/personalization.md#about-targeting-dimension).

기본적으로 메시지를 분석하면 컨트롤이 표시됩니다 [유형화 규칙](../../sending/using/control-rules.md) 옵트아웃 링크가 포함되었는지 확인하고 누락된 경우 경고를 생성합니다.

**팁**: 인간 오류가 항상 가능하므로 보낼 때마다 옵트아웃 링크가 올바르게 작동하는지 확인하십시오. 예를 들어 증명을 보낼 때 링크가 유효한지, 양식이 온라인 상태이고, 이 수신자 필드에 더 이상 연락하지 않음 필드가 예로 변경되었는지 확인하십시오.

옵트아웃 링크를 삽입하는 방법 알아보기 [이 섹션](../../designing/using/personalization.md#adding-a-content-block).

### 전자 메일 크기 {#email-size}

성능 또는 게재 가능성 문제를 방지하기 위해 이메일의 권장 최대 크기는 거의 입니다 **35KB**.

전자 메일을 한도에 따라 유지하려면 다음을 고려하십시오.

* 중복 또는 사용하지 않은 스타일 제거

* 전자 메일 콘텐츠 일부를 [랜딩 페이지](../../channels/using/getting-started-with-landing-pages.md)

* 코드 축소

최종 전송 전에 변경 사항을 테스트해야 합니다.

Adobe Campaign에서 이메일의 기본 최대 크기가 **100MB**. <!--This limit enables to prevent any error that could indefinitely increase the size of an email, which can lead to a system crash.-->

제한에 도달하면 제한을 초과하는 메시지가 실패하여 게재 로그에 오류 메시지가 표시됩니다. 동일한 게재의 다른 메시지는 영향을 받지 않습니다. 이 경우 이메일 템플릿의 동적 부분 또는 게재에서 사용하는 콘텐츠 조각을 조정해야 합니다. <!--If you need assistance, or if you have any question or request about the **[!UICONTROL Maximum message size]** option, reach out to your Adobe contact.-->

Adobe은 최대 메시지 크기 기본값을 유지하는 것이 좋습니다. 그러나 이 값은 **[!UICONTROL Maximum message size]** 옵션, 사용 **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** 메뉴, 기준 [기능 관리자](../../administration/using/users-management.md#functional-administrators) 전용.

>[!IMPORTANT]
>
>이 값을 0으로 설정하면 제한이 적용되지 않습니다.

### SMS 길이

기본적으로 SMS의 글자 수는 GSM(이동통신 글로벌 시스템) 표준을 충족합니다. GSM 인코딩을 사용하는 SMS 메시지는 SMS당 160자, 또는 여러 부분으로 나누어 전송되는 메시지의 경우 153자로 제한됩니다.

변환은 GSM 표준에서 고려하지 않는 SMS 문자를 다른 문자로 바꾸는 작업입니다. SMS 메시지의 콘텐츠에 개인화 필드를 삽입하면 GSM 인코딩에서 고려하지 않는 문자가 들어갈 수 있습니다. 해당 채널의 SMPP 채널 설정 탭에서 해당 상자를 선택하여 문자 변환을 승인할 수 있습니다 **[!UICONTROL External account]**.
추가 정보 [이 섹션](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

**팁**:

* SMS 메시지의 모든 문자를 그대로 유지하려는 경우, 예를 들어 적절한 이름을 변경하지 마십시오. 음역을 활성화하지 마십시오.

* 그러나 GSM 표준에서 고려하지 않는 문자가 많이 포함된 SMS 메시지에는 음역을 활성화하여 메시지 전송 비용을 제한합니다.

추가 정보 [이 섹션](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

### 반응형 이메일 디자인

응답형 디자인은 이메일이 열려 있는 장치에 대해 최적으로 렌더링되도록 합니다.

* 웹 HTML이 아닌 응답형 이메일 HTML 사용

* 미리 보기 모드를 사용하고 증명을 보내 가능한 한 많은 장치에서 렌더링을 테스트합니다. 방법 알아보기 [메시지 미리 보기](../../sending/using/previewing-messages.md) 보내기 전.

* Campaign 이메일 디자이너는 모바일용 반응형 디자인 형식 템플릿을 제공합니다. [이 페이지](../../designing/using/using-reusable-content.md#content-templates)에서 자세히 알아보십시오.

## 이미지 관리 {#manage-images}

이미지 사용에 대해서는 아래 지침을 따르십시오.

### 이미지 차단

일부 이메일 클라이언트는 기본적으로 이미지를 차단하며, 일부 사용자는 데이터 사용을 위해 이미지를 차단하도록 설정을 변경합니다. 따라서 이미지를 다운로드하지 않으면 전체 메시지가 손실될 수 있습니다. 이를 방지하려면 다음을 수행하십시오.

* 컨텐츠와 이미지 및 텍스트의 균형을 맞춥니다. 완전히 이미지 기반 이메일을 사용하지 마십시오.

* 이미지에 텍스트를 포함해야 하는 경우 대체 및 제목 텍스트를 사용하여 메시지가 전달되는지 확인하십시오. 대체/제목 텍스트 스타일을 지정하여 모양을 개선합니다.

* 일부 이메일 클라이언트는 배경 이미지를 지원하지 않으므로 배경 이미지를 사용하지 마십시오.

### 반응형 이미지 만들기

이미지를 반응시키고 크기를 조정할 수 있도록 합니다. 이렇게 하면 빌드하는 데 시간이 오래 걸려 비용이 발생할 수 있습니다.

### 절대 이미지 참조 사용

외부에서 액세스하려면 캠페인에 연결된 이메일 및 공개 리소스에 사용된 이미지가 외부에서 액세스할 수 있는 서버에 있어야 합니다.

## 메시지 미리 보기 {#preview-msg}

Adobe은 메시지를 미리 보고 개인화와 수신자가 게재를 볼 수 있는 방법을 확인하는 것을 권장합니다.

이메일 디자이너에서 **[!UICONTROL Preview]** 버튼을 사용하면 수신자에 대한 각 컨텐츠 렌더링을 볼 수 있습니다. 개인화 필드 및 콘텐츠의 조건부 요소는 선택한 프로필에 대한 해당 정보로 대체됩니다. [자세히 알아보기](../../sending/using/previewing-messages.md)
