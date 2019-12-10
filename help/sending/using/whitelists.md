---
title: Adobe Campaign Standard의 화이트리스트
description: Adobe Campaign Standard를 사용하여 화이트리스트를 최적화하는 방법을 살펴보십시오.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44049443f8028ed26089ee0d49944ebac6a62111

---


# 화이트 리스트{#whitelists}

기본 인터넷 서비스 제공업체(ISP)와 웹 메일 제공업체는 인식된 이메일 메시지 전송자의 화이트 리스트를 관리합니다. Adobe Campaign을 사용하면 최고의 화이트리스트에 대한 인증을 받을 수 있습니다.

이메일 허용 목록은 이메일 차단 프로그램이 메시지를 수신할 수 있도록 허용하는 이메일 주소 또는 도메인 이름 목록입니다.

두 가지 유형의 화이트 리스트가 있습니다.
* 비상업적 화이트 리스트
* 상업용 화이트 리스트

## 비상업적 화이트 리스트 {#non-commercial-whitelists}

이러한 화이트 리스트가 수락하려면, 발신자는 기술 확인을 기반으로 한 일련의 테스트를 통과해야 합니다(이메일 서버는 공개 릴레이가 아니어야 하지만 정적 IP가 있어야 함). 인프라 또는 해당 활동(배달 빈도, 볼륨, 불만 수).

보낸 사람이 이러한 규칙 중 하나를 따르지 않으면 허용 목록에서 삭제될 수 있습니다. Adobe Campaign **이메일 배달** 기능 패키지에서 Adobe Campaign은 비기업 화이트리스트에 대한 인증 프로세스를 위한 전문 컨설팅 서비스를 제공합니다.

## 상업용 화이트 리스트 {#commercial-whitelists}

상업용 화이트 리스트는 발신자가 스팸 방지 필터를 모두 우회하거나 시스템에 들어올 때 점차적으로 포인트를 할당할 수 있는 시스템을 기반으로 합니다. 이러한 유료 허용 목록(CPT 또는 연간 기준)은 반환 경로 보낸 사람 점수와 같은 시스템에서 제공됩니다.

ISP 파섹 따라서 발신자는 전달 보증을 통해 메시지를 보낼 때 더욱 자신감을 가질 수 있습니다. 일부 화이트 리스트는 이미지를 열고 링크를 활성화할 수도 있습니다.

화이트리스트에 나타나는 것은 모든 이메일 캠페인에 대한 부인할 수 없는 자산입니다. Adobe Campaign **이메일 배달** 기능 패키지에서 Adobe Campaign은 CSA 및 반환 경로 보낸 사람 점수와 같은 상업용 화이트 리스트 인증 서비스를 제공합니다.