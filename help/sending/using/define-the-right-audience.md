---
title: 적합한 대상자 정의
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: "콘텐츠를 준비한 후에는 메시지를 받을 사용자를 신중하게 정의하는 방법에 대해 알아보십시오."
feature: Deliverability
role: User
level: Intermediate
exl-id: 1e06fd9d-e850-4856-8f7b-b581dbe157df
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 11%

---

# 적합한 대상자 정의 {#define-the-right-audience}

타겟팅된 모집단은 중요합니다. 목록을 신중하게 작성하고, 인기 있는 이메일 클라이언트 및 모바일 디바이스에서 이메일을 테스트하고, 이메일 목록이 최신 상태인지 확인합니다(알 수 없거나 오래된 주소는 없음). 전체 유효성 검사 주기를 설정하는 데 도움이 되는 증명을 보낼 수도 있습니다.

대상 모집단 [에 대한 자세한 내용은 이 섹션](../../audiences/using/selecting-an-audience-in-a-message.md)을 참조하세요.

## 적합한 대상 타기팅 {#target-the-right-audience}

콘텐츠를 준비한 후에는 메시지를 받을 사용자를 신중하게 정의해야 합니다.

게재를 성공적으로 수행하려면 가장 관련성이 높은 개인화된 콘텐츠를 적절한 수신자에게 전송해야 합니다. Adobe Campaign을 사용하면 가장 정확한 대상을 작성할 수 있습니다. 이전 게재에서 링크를 클릭한 경우 나이, 현지화, 구입한 항목 등에 따라 수신자를 선택할 수 있습니다. Adobe Campaign을 사용하면 테스트 프로필, 컨트롤 그룹 및 시드 주소를 정의하여 타겟이 올바른지 확인할 수도 있습니다.

## 대상 매핑 {#target-mappings}

기본적으로 게재 템플릿은 **프로필**&#x200B;을(를) 대상으로 합니다. Adobe Campaign은 게재에 대한 다른 타겟 매핑을 제공하며, 필요에 따라 변경할 수 있습니다.

이 매핑은 [이 섹션](../../automating/using/query.md#targeting-dimensions-and-resources)에 표시됩니다.

사용자 지정된 대상 매핑을 만들고 사용할 수도 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../administration/using/target-mappings-in-campaign.md)을 참조하십시오.

## 외부 데이터 {#external-data}

데이터베이스에 저장되지 않고 외부 파일에 저장된 수신자에게 전달할 수 있습니다. 이를 위해 워크플로를 디자인하면 파일에서 데이터베이스에 데이터를 로드하고 관련 대상을 만듭니다.  [이 사용 사례](../../automating/using/use-case-calling-workflow.md)에서 자세히 알아보세요. [매개 변수로 워크플로우 호출](../../automating/using/calling-a-workflow-with-external-parameters.md)도 참조하세요.

## 구독자에게 보내기 {#send-to-subscribers}

뉴스레터 가입자에게 메시지를 보내려면 해당 정보 서비스의 가입자를 직접 타겟팅할 수 있습니다. 자세한 내용은 [이 섹션](../../audiences/using/about-subscriptions.md)을 참조하세요.

**팁** - 워크플로우를 사용하여 뉴스레터 구독자를 타겟팅하는 목록 대상자를 만들 수 있습니다. 그런 다음 게재에서 이 대상을 선택할 수 있습니다. 자세한 내용은 [목록 대상자 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)를 참조하십시오.

## 증명, 테스트 프로필 및 컨트롤 그룹 {#proofs-test-control-groups}

게재를 테스트하려면 주요 타겟에게 보내기 전에 증명을 사용하십시오.
적절한 증명 수신자를 선택해야 합니다. 메시지 양식 및 내용의 유효성을 검사하기 때문입니다. 증명을 보내는 단계는 [이 섹션](../../sending/using/sending-proofs.md)에 표시됩니다.

테스트 프로필 [에 대한 자세한 내용은 이 섹션](../../audiences/using/managing-test-profiles.md)을 참조하세요.

[컨트롤 그룹](../../sending/using/control-group.md)을 사용하여 대상의 일부를 제외하여 캠페인의 영향을 측정할 수 있습니다. 그러면 메시지를 받은 대상 모집단과 타겟팅되지 않은 연락처의 동작을 비교할 수 있습니다. 전송 로그를 기준으로 향후 캠페인에서 컨트롤 그룹을 타겟팅할 수도 있습니다.

## 주소 중복 제거 {#deduplicate-addresses}

중복 이메일 주소는 타겟에 영향을 줄 수 있으므로 피하는 것이 중요합니다.

* 대상이 분할될 때 동일한 메시지를 두 번 이상 보낼 수 있습니다.

* 메시지를 받은 후 수신자가 구독을 취소해도 중복 프로필은 향후 메시지를 계속 수신합니다.

주소 중복을 제거하면 전송 평판이 보호되며 격리도 잘 관리됩니다.

[이 사용 사례](../../automating/using/deduplicating-data-imported-file.md)에서 자세히 알아보세요.
