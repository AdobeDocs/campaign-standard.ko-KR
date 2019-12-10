---
title: Adobe Campaign Standard의 전달 문제 해결
description: Adobe Campaign Standard에서 전달 가능 문제가 발생하면 어떻게 해야 하는지 살펴보십시오.
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
source-git-commit: b2df5ca4d38e35f57815924ffbe0313dc1a22b29

---


# 문제 해결{#troubleshooting}

배달 문제가 발생했습니까? 여기에서 해결 방법을 찾을 수 있습니다.

**특정 ISP에 대해 항상 동일한 오류 메시지가 표시되는 이유는 무엇입니까?**

ISP에 대해 항상 동일한 오류 메시지가 표시되는 경우, ISP에서 사용자의 이메일 또는 IP가 오류로 감지되었을 수 있습니다. 다음 권장 사항을 실행합니다.
* 존재하지 않는 이메일 주소에 연결된 오류(사용자 알 수 없는&#x200B;**오류** )가 많은지 확인합니다.
* 가입 양식을 업데이트하여 입력한 도메인 이름의 오류를 검색합니다(예:gmaul.com 또는 yaho.com)을 참조하십시오.
* 메시지가 스팸으로 선언되거나 메시지가 지속적으로 차단되었다는 오류가 발생하는 경우, 타겟에서 지난 12개월 동안 메시지 중 하나를 열지 않았거나 클릭하지 않은 수신자를 제외하십시오.

문제가 지속되면 상업용 또는 배달 서비스 또는 Adobe Campaign 지원에 문의하십시오.

**블랙리스트에 추가된 이메일 주소와 격리된 이메일 주소 간의 차이점은 무엇입니까?**

상태는 피드백 루프의 **[!UICONTROL Blacklisted]** 결과입니다(사용자가 스팸으로 메시지를 보고하는 경우).

상태는 부드러운 또는 하드 바운스의 **[!UICONTROL Quarantined]** 결과입니다.

**다른 격리 오류 이유는 무엇입니까?**

다음과 같은 10가지 이유가 있습니다.정의되지 않음, 사용자 알 수 없음, 잘못된 도메인, 블랙리스트에 추가된 주소, 거부됨, 오류 무시, 접근 불가, 계정 비활성화, 전체, 연결되지 않음.

자세한 내용은 격리 [관리](../../sending/using/understanding-quarantine-management.md)이해를 참조하십시오.

**내 받는 사람 중 한 명이 실수로 블랙리스트에 올랐다. 메시지를 다시 보낼 수 있도록 블랙리스트를 해제하려면 어떻게 해야 합니까?**

* 로 **[!UICONTROL Administration > Channels > Quarantines > Addresses]**&#x200B;이동합니다.
* 해당 레코드의 세부 정보에서 **[!UICONTROL Status]** 필드 값을 로 설정합니다 **[!UICONTROL Valid]**.
* 레코드를 저장합니다.

**내 IP 중 하나가 블랙리스트에 추가되었는지 어떻게 알 수 있습니까? 내 IP의 블랙 리스트 해제는 어떻게 합니까?**

IP 주소가 블랙리스트에 추가되었는지 확인하려면 다양한 웹 사이트를 사용하여 확인할 수 있습니다.
* http://mxtoolbox.com/
* http://whatismyipaddress.com/blacklist-check
* http://www.blacklistalert.org/

일반적으로 IP 주소 확인 결과는 블랙 리스트의 세부 사항과 IP 주소를 블랙리스트에 올린 웹 사이트의 이름이 포함된 목록을 반환합니다.

링크를 클릭하면 웹 사이트 세부 정보에 액세스할 수 있습니다.

그런 다음 IP 주소를 블랙리스트에 올린 웹 사이트에서 웹 사이트를 삭제하도록 요청할 수 있습니다.

삭제 프로세스는 웹 사이트에 따라 다를 수 있습니다. 일부 사이트에서는 계정을 만들어야 하지만 다른 사이트에서는 IP 주소를 제공해야 합니다.
