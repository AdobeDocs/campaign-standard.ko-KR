---
solution: Campaign Standard
product: campaign
title: 적합한 대상 정의
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
translation-type: tm+mt
source-git-commit: a7300666587362048431d0bafacc317170b317aa
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 11%

---


# 적합한 대상 정의 {#define-the-right-audience}

타깃팅된 채우기가 핵심 요소입니다.목록을 주의 깊게 작성하고, 인기 있는 이메일 클라이언트 및 모바일 디바이스에서 이메일을 테스트하고, 이메일 목록이 최신 상태(알 수 없거나 오래된 주소 없음)인지 확인합니다. 또한 전체 확인 주기를 설정하는 데 도움이 되는 교정본을 보낼 수 있습니다.

이 섹션](../../audiences/using/selecting-an-audience-in-a-message.md)에서 타겟 모집단 [에 대해 자세히 알아보십시오.

## 올바른 대상자 {#target-the-right-audience}

콘텐츠를 준비하면 메시지를 받을 사람을 신중하게 정의해야 합니다.

성공적으로 전달하려면 가장 연관성 높은 개인화된 컨텐츠를 적합한 수신자에게 전송해야 합니다. Adobe Campaign을 사용하면 가장 정확한 타겟을 구축할 수 있습니다.이전 배달에서 링크를 클릭한 경우 연령, 현지화, 구매자, 구매자 등에 따라 받는 사람을 선택할 수 있습니다. Adobe Campaign을 사용하면 테스트 프로필, 제어 그룹 및 시드 주소를 정의하여 대상이 올바른지 확인할 수도 있습니다.

## 대상 매핑 {#target-mappings}

기본적으로 배달 템플릿은 **프로필**&#x200B;을(를) 대상으로 합니다. Adobe Campaign은 필요에 따라 변경할 수 있는 게재에 대한 다른 대상 매핑을 제공합니다.

이러한 매핑은 이 섹션](../../automating/using/query.md#targeting-dimensions-and-resources)에 [표시됩니다.

사용자 지정된 대상 매핑을 만들고 사용할 수도 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../administration/using/target-mappings-in-campaign.md)을 참조하십시오.

## 외부 데이터 {#external-data}

데이터베이스에 저장되지 않고 외부 파일에 저장된 수신자에게 전달할 수 있습니다. 이렇게 하려면 작업 과정을 설계하면 파일에서 데이터를 데이터베이스에 로드하여 연관된 대상을 만듭니다.  이 사용 사례](../../automating/using/use-case-calling-workflow.md)에서 [에 대해 자세히 알아보십시오. [매개 변수](../../automating/using/calling-a-workflow-with-external-parameters.md)가 있는 워크플로 호출을 참조하십시오.

## 구독자에게 {#send-to-subscribers} 보내기

뉴스레터 가입자에게 메시지를 보내려면 해당 정보 서비스에 가입자를 직접 타깃팅할 수 있습니다. 이 섹션](../../audiences/using/about-subscriptions.md)에서 [에 대해 자세히 알아보십시오.

**팁** - 워크플로우를 사용하여 뉴스레터 가입자를 대상으로 하는 목록 대상자를 만들 수 있습니다. 그런 다음 게재에서 이 대상자를 선택할 수 있습니다. 자세한 내용은 [목록 대상 만들기](../../audiences/using/creating-audiences.md#creating-list-audiences)를 참조하십시오.

## 교정본, 테스트 프로파일 및 제어 그룹 {#proofs-test-control-groups}

전달 내용을 테스트하려면 주 타겟으로 보내기 전에 교정본을 사용하십시오.
양식 및 메시지 내용의 유효성을 검사하므로 적절한 증명 수신자를 선택해야 합니다. 교정본을 전송하는 단계는 이 섹션](../../sending/using/sending-proofs.md)에 [표시됩니다.

이 섹션](../../audiences/using/managing-test-profiles.md)에서 테스트 프로필 [에 대해 자세히 알아보십시오.

[제어 그룹](../../sending/using/control-group.md)을 사용하여 대상의 일부를 제외하여 캠페인의 영향을 측정할 수 있습니다. 그러면 메시지를 받은 대상 모집단과 타겟팅되지 않은 연락처의 동작을 비교할 수 있습니다. 전송 로그를 기준으로 향후 캠페인에서 컨트롤 그룹을 타겟팅할 수도 있습니다.

## 주소 중복 제거 {#deduplicate-addresses}

타겟에 영향을 줄 수 있으므로 중복된 이메일 주소를 사용하지 않는 것이 중요합니다.

* 대상이 분할될 때 동일한 메시지를 두 번 이상 보낼 수 있습니다.

* 메시지를 받은 수신자가 구독을 취소하는 경우 중복된 프로필은 여전히 향후 메시지를 수신하게 됩니다.

중복 제거 주소는 전송 명성을 보호하고 안전한 격리 관리를 보장합니다.

이 사용 사례](../../automating/using/deduplicating-data-imported-file.md)에서 [에 대해 자세히 알아보십시오.
