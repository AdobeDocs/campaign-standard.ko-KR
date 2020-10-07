---
title: 개인화된 콘텐츠 제작
seo-title: 개인화된 콘텐츠 제작
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 7%

---


# 개인화된 콘텐츠 제작 {#build-personalized-content}

메시지 내용을 디자인할 때 배달 실행을 방지할 수 있는 일반적인 문제를 방지하십시오. 대부분의 경우, 가능한 오류는 [개인화](../../designing/using/personalization.md), 기존 컨텐츠 [를](../../designing/using/using-existing-content.md) 사용할 때의 서식, HTML 컨텐츠 [를](../../designing/using/using-existing-content.md#converting-an-html-content) 변환할 때 발생할 수 있는 오류 [- 및](../../designing/using/images.md)이미지와 관련되어 있습니다.

## 개인화 최적화 {#optimize-personalization}

메시지 전달을 실행하지 못하도록 하고 받는 사람의 경험을 향상시킬 수 있는 일반적인 문제를 방지하기 위해 Adobe Campaign을 사용하면 메시지를 개인화할 수 있습니다.

Adobe Campaign 데이터베이스에 저장된 수신자 데이터를 사용하거나 추적, 랜딩 페이지, 구독 등을 통해 수집할 수 있습니다.
개인화 기본 사항은 [이 섹션에 나와 있습니다](../../designing/using/personalization.md).

메시지 컨텐츠가 개인화와 관련된 오류를 방지하도록 제대로 설계되었는지 확인하십시오.

표현식 편집기에서 정의된 조건에 따라 받는 사람에게 다른 컨텐츠를 표시하도록 동적 컨텐츠를 수동으로 추가할 수 있습니다. 동적 컨텐츠를 추가할 때는 선택한 조건을 충족하지 않는 수신자에 대해 항상 기본 변형을 그대로 두어야 합니다.
동적 컨텐츠에 대한 자세한 내용은 [이 섹션을 참조하십시오](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

**팁** - 다이내믹 컨텐츠가 올바르게 구성되었는지 확인하기 위해 다른 테스트 프로필로 이메일을 미리 봅니다.

## 최적화된 콘텐츠 제작 {#optimize-content}

이메일을 작성할 때 아래의 일반적인 모범 사례를 염두에 두십시오.

* 디자인 간소화

* 모바일 사용자를 염두에 두십시오

* 이미지 기반의 이메일 수신 방지

* 이메일 안전 글꼴 사용

* 특수 문자 인코딩

### 제목

개방률을 [높이기](../../designing/using/subject-line.md) 위해 주제 라인

* 너무 긴 과목은 피하세요. 최대 50자를 사용할 수 있습니다

* 스팸으로 간주될 수 있는 &quot;무료&quot; 또는 &quot;오퍼&quot;와 같은 반복적인 단어를 사용하지 마십시오

* 대문자 및 &quot;!&quot;, &quot; 저녁&quot;, &quot;\&quot;, &quot;$&quot;와 같은 특수 문자를 사용하지 마십시오.

### 미러 페이지

항상 미러 페이지 링크를 포함합니다. 이메일의 맨 위에 기본 위치가 있습니다. [자세히 알아보기](../../designing/using/personalization.md#adding-a-content-block)

### 구독 취소 링크

구독 취소 링크는 필수적입니다. 반드시 표시되고 유효해야 하며, 양식이 제대로 작동하는지 확인해야 합니다. 이 섹션 [에서 구독 취소 링크 가이드라인에 대해 학습합니다](../../designing/using/personalization.md#about-targeting-dimension).

기본적으로 메시지를 분석할 때 제어 유형 [규칙은](../../sending/using/control-rules.md) 옵트아웃 링크가 포함되었는지 여부를 확인하고 누락된 경우 경고를 생성합니다.

**팁**:사용자 오류는 항상 가능하므로 전송 때마다 옵트아웃 링크가 올바르게 작동하는지 확인합니다. 예를 들어 증거를 보낼 때 링크가 유효한지, 양식이 온라인인지, 이 수신자에게 더 이상 연락하지 않음 필드가 예로 변경되었는지 확인하십시오.

이 섹션 [에 옵트아웃 링크를 삽입하는 방법을 알아봅니다](../../designing/using/personalization.md#adding-a-content-block).

### 이메일 크기

성능 또는 전달 문제가 발생하지 않도록 하기 위해 권장되는 최대 이메일 크기는 약 **35KB입니다**.

이메일을 제한된 범위 내에서 유지하려면 다음을 고려하십시오.

* 중복 또는 사용하지 않는 스타일 제거

* 이메일 콘텐츠 중 일부를 랜딩 페이지로 이동

* 코드 축소

최종 전송 전에 변경 사항을 테스트하십시오

### SMS 길이

기본적으로 SMS의 글자 수는 GSM(이동통신 글로벌 시스템) 표준을 충족합니다. GSM 인코딩을 사용하는 SMS 메시지는 SMS당 160자, 또는 여러 부분으로 나누어 전송되는 메시지의 경우 153자로 제한됩니다.

변환은 GSM 표준에서 고려하지 않는 SMS 문자를 다른 문자로 바꾸는 작업입니다. SMS 메시지의 컨텐츠에 개인화 필드를 삽입하면 GSM 인코딩에 의해 고려되지 않는 문자가 도입될 수 있습니다. 해당 채널의 SMPP 채널 설정 탭에서 해당 상자를 선택하여 문자 교환을 인증할 수 있습니다 **[!UICONTROL External account]**.
이 섹션 [에서 자세히 알아보십시오](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

**팁**:

* SMS 메시지의 모든 문자를 그대로 유지하려면 적절한 이름을 바꾸지 마십시오. 음역을 활성화하지 마십시오.

* 그러나 GSM 표준으로 간주되지 않는 많은 문자가 SMS 메시지에 포함되어 있는 경우, 교역을 활성화하여 메시지 전송 비용을 제한합니다.

이 섹션 [에서 자세히 알아보십시오](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

### 반응형 이메일 디자인

반응형 디자인을 사용하면 이메일이 열려 있는 장치에 맞게 최적으로 렌더링됩니다.

* 웹 HTML이 아닌 반응형 이메일 HTML 사용

* 미리 보기 모드를 사용하여 가능한 한 많은 디바이스에서 렌더링을 테스트할 수 있습니다. 보내기 전에 [메시지를 미리](../../sending/using/previewing-messages.md) 보는 방법을 알아봅니다.

* Campaign Email Designer에는 모바일용 반응형 디자인 형식 템플릿이 포함되어 있습니다. 이 페이지 [에서 자세히 알아보십시오](../../designing/using/using-reusable-content.md#content-templates).

## 이미지 관리 {#manage-images}

이미지 사용에 대해서는 아래 지침을 따르십시오.

### 이미지 차단 방지

일부 이메일 클라이언트는 기본적으로 이미지를 차단하며, 일부 사용자는 데이터 사용을 위해 이미지를 차단하도록 설정을 변경합니다. 따라서 이미지를 다운로드하지 않으면 전체 메시지가 손실될 수 있습니다. 이를 방지하려면

* 콘텐츠와 이미지 및 텍스트의 균형을 맞출 수 있습니다. 이미지 기반의 이메일 전달

* 이미지에 텍스트를 포함해야 하는 경우 대체 및 제목 텍스트를 사용하여 메시지가 제대로 전달되는지 확인하십시오. 대체/제목 텍스트에 스타일을 지정하여 모양을 향상시킬 수 있습니다.

* 일부 이메일 클라이언트에서 지원하지 않는 배경 이미지는 사용하지 마십시오.

### 반응형 이미지 제작

반응형 이미지를 만들고 크기를 조정할 수 있습니다. 이렇게 하면 구축하는 데 시간이 더 걸리기 때문에 비용 측면에서 영향을 줄 수 있습니다.

### 절대 이미지 참조 사용

외부에서 액세스하려면 캠페인에 연결된 이메일 및 공개 리소스에 사용된 이미지가 외부에서 액세스 가능한 서버에 있어야 합니다.

## 메시지 미리 보기 {#preview-msg}

Adobe은 메시지를 미리 보고 개인화와 수신자가 전달을 어떻게 볼 수 있는지 확인하는 것이 좋습니다.

이메일 디자이너에서 이 **[!UICONTROL Preview]** 단추를 사용하여 수신자의 각 컨텐츠 렌더링을 볼 수 있습니다. 개인화 필드 및 컨텐츠 조건부 요소는 선택한 프로필에 대한 해당 정보로 대체됩니다. [자세히 알아보기](../../sending/using/previewing-messages.md)
