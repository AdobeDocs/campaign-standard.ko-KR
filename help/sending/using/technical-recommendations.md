---
solution: Campaign Standard
product: campaign
title: Adobe Campaign Standard을 위한 기술 추천 제공
description: Adobe Campaign Standard을 통한 제공 능력을 개선하기 위한 몇 가지 기술적인 권장 사항에 대해 살펴보십시오.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# 기술 추천{#technical-recommendations}

배달률을 향상시키는 데 사용할 수 있는 몇 가지 기법, 구성 및 도구는 아래에 나와 있습니다. 주요 기술 용어에 대한 몇 가지 정의는 다음과 같습니다.

**DNS** 반전:Adobe Campaign은 IP 주소에 대해 역 DNS가 제공되었는지 그리고 이것이 IP를 올바르게 가리키는지 확인합니다.

**MX** 규칙은 캠페인 MTA(메시지 전송 에이전트)가 각 개별 이메일 도메인 또는 ISP(예: hotmail.com, comcast.net)로 이메일을 보내는 속도를 제어하는 데 사용됩니다. 이러한 규칙은 일반적으로 ISP가 게시한 제한을 기반으로 합니다(예: 각 SMTP 연결당 20개 이상의 메시지가 포함되지 않음).

**TLS** (전송 계층 보안)는 두 이메일 서버 간의 연결을 보호하고 대상 받는 사람 이외의 다른 사람이 이메일 컨텐츠를 읽지 못하도록 보호하는 데 사용할 수 있는 암호화 프로토콜입니다.

**SPF** (Sender Policy Framework)는 도메인 소유자가 해당 도메인을 대신하여 이메일을 보낼 수 있는 이메일 서버를 지정할 수 있도록 하는 이메일 인증 표준입니다. 이 표준은 이메일의 &quot;반환 경로&quot; 헤더에 있는 도메인을 사용합니다(&quot;편지 봉투 보낸 사람&quot; 주소라고도 함).

**DKIM** (Domain Keys Identified Mail) 인증은 SPF의 후속 개념이며 받는 이메일 서버가 메시지를 전송했다고 주장하는 사람 또는 엔티티가 메시지를 실제로 보냈는지, 메시지 컨텐츠가 원래 전송(및 DKIM &quot;signed&quot;)된 시간 및 수신될 때까지 변경되었는지 여부를 확인하는 공개 키 암호화를 사용합니다. 이 표준은 일반적으로 &quot;보낸 사람&quot; 또는 &quot;보낸 사람&quot; 헤더의 도메인을 사용합니다.

**DMARC** (도메인 기반 메시지 인증, 보고 및 준수)는 최신 이메일 인증 양식이며, SPF 및 DKIM 인증을 통해 이메일 전달 여부를 확인합니다. DMARC는 매우 중요한 두 가지 방법으로 독특하고 강력합니다.
* 적합성 - 발신자가 인증하지 못한 메시지(예: 승인하지 않음)를 ISP에 지시할 수 있도록 해줍니다.
* 보고 - &quot;보낸 사람&quot; 도메인 및 각 항목에 사용되는 IP 주소와 함께 DMARC 인증에 실패한 모든 메시지를 표시하는 자세한 보고서를 전송자에게 제공합니다. 이를 통해 회사는 인증이 실패하고 있고 일부 유형의 &quot;수정&quot;(예: SPF 레코드에 IP 주소 추가) 및 이메일 도메인에서 피싱 시도 소인과 출현을 필요로 하는 정당한 이메일을 식별할 수 있습니다.

DMARC는 250ok로 생성된 보고서를 활용할 수 있습니다.

**SMTP** (Simple mail transfer protocol)는 이메일 전송을 위한 인터넷 표준입니다.

**전용 IP**:Adobe은 명성을 구축하고 전달 성능을 최적화하기 위해 각 고객에게 구현 IP를 제공하는 전용 IP 전략을 제공합니다.
