---
solution: Campaign Standard
product: campaign
title: 추적된 URL 서명 문제
description: 추적된 URL 서명 문제
translation-type: ht
source-git-commit: 830c003e36cec41e5cf480f66812900312609e9f
workflow-type: ht
source-wordcount: '199'
ht-degree: 100%

---


# 추적된 URL 서명 문제 {#tracked-urls}

최근 변경 사항에 따라 Campaign에서 보낸 추적된 URL이 실패할 수 있습니다. 일부 회사에는 링크에 영향을 주고 URL 서명 메커니즘을 변경할 수 있는 특정 보안 도구가 있으므로 일부 사서함은 다른 사서함보다 더 큰 영향을 받을 수 있습니다.

그 결과 Adobe은 링크 추적을 위해 서명 메커니즘을 비활성화하기로 했습니다. 이 절차에서는 모든 추적 링크를 수정합니다.

구독 취소 링크는 다른 모든 링크와 마찬가지로 실패할 수 있으며, 빈도는 호스트에 따라 다르지만 1% 미만입니다.

**영향을 받습니까?**

이메일 링크 추적에 대한 서명 메커니즘이 2020년 10월에 [Campaign Standard 20.4](release-notes-2020.md#release-20-4---october-2020)으로 도입되었으며 모든 고객에 대해 기본적으로 활성화되어 있기 때문에 일부 Campaign Standard 사용자는 영향을 받습니다.

**업데이트 방법**

Adobe에서 잠시 후 구성을 업데이트하기 위해 사용자와 함께 작업할 예정입니다. 업그레이드 타임라인이 포함된 이메일 알림을 받게 됩니다.

**어떤 영향이 있습니까?**

유지 관리에는 최대 25분 다운타임이 필요하며 이 기간 동안 모든 게재, 추적 링크 및 API 호출이 작동하지 않습니다.

업데이트가 완료되면 모든 링크가 예상대로 작동합니다.

>[!NOTE]
>
>이러한 변경 사항에 대한 질문이 있으면 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html)에 문의하십시오.

