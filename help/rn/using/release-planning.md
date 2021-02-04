---
solution: Campaign Standard
product: campaign
title: Campaign Standard 릴리스 계획
description: 이 페이지에는 Adobe Campaign Standard의 향후 릴리스 목록이 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning
translation-type: tm+mt
source-git-commit: fb16fc4e24a4345d73e0b2a0ad58a78771a93b8a
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 94%

---


# 릴리스 계획 {#release-planning}

Adobe는 새로운 기능, 개선 사항 및 수정 사항을 추가하여 솔루션을 지속적으로 개선합니다.

모든 Adobe Campaign Standard 인스턴스는 새로운 릴리스마다 업그레이드됩니다. 업그레이드하기 위해 필요한 작업은 없습니다.

업그레이드는 두 단계로 배포됩니다. 먼저 Stage 인스턴스가 업그레이드되어 고객이 새로운 기능을 테스트하고 필요한 경우 구성을 변경할 수 있습니다. 그런 다음 프로덕션 인스턴스가 업그레이드됩니다.

모든 릴리스 날짜는 변경될 수 있습니다. 정기적으로 이 페이지를 방문하여 업데이트를 확인하는 것이 좋습니다.

**새로운 기능이 있습니다.** [Campaign Standard 릴리스 알림](http://amc-mkt-prod1-t.adobe-campaign.com/lp/LP25?service=%40rZ5cqp2DgNzrgz0alKPInakNbPSTeJYozZYnS7Wbs802u4GlISkHZX4omtK00nAU6xzZ6luEWQzr7kQ9pkCwJYumWkU)을 구독하면 받은 편지함에서 예정된 릴리스에 대한 세부 정보를 바로 확인할 수 있습니다.

## 릴리스 21.1 - 2월 릴리스 {#release-21-1-release}

아래의 표시된 기간 동안 환경 업데이트가 발생합니다. 정확한 날짜는 각 고객에게 이메일로 전달된다.

이 릴리스에 대한 자세한 내용은 스테이지 환경 업그레이드가 시작될 때 [릴리스 노트](../../rn/using/release-notes.md)에서 확인할 수 있습니다.

<table>
 <thead>
  <tr>
   <th> 환경<br /> </th>
   <th> 날짜<br /> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>단계<br /> </td>
   <td>2021년 2월 1일 - 10일<br /> </td>
  </tr>
  <tr>
   <td> 프로덕션<br /> </td>
   <td>2021년 2월 8일 - 17일<br /> </td>
  </tr>
 </tbody>
</table>

추가 질문 사항은 [Adobe Client Care](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.

## 질문 및 답변 {#questions-and-answers}

**질문: 어떤 영향이 있습니까?**

답변: 변경 사항은 관련 설명서에 대한 링크를 포함하여 [릴리스 정보](../../rn/using/release-notes.md)에 나열되어 있습니다. [더 이상 사용되지 않는 기능 및 제거된 기능 페이지](../../rn/using/deprecated-features.md)를 참조하는 것을 권장합니다. 이 페이지는 스테이징 환경 업그레이드 날짜에 새 릴리스에서 사용할 수 있습니다.

**질문: 유효성 검사 프로세스는 무엇입니까?**

답변: 스테이징 인스턴스가 업그레이드되면 프로세스 및 사용 사례가 이 새로운 버전에서 제대로 작동하는지 확인하고 문제가 발생하면 [Adobe Client Care](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 보고할 것을 권장합니다.

**질문: 업그레이드 프로세스 중에 인스턴스에 액세스할 수 있습니까?**

답변: 아니요. 인스턴스 업그레이드 중에는 몇 분 동안 데이터베이스에 액세스할 수 없습니다. 모든 프로세스가 자동으로 다시 시작됩니다.

**질문: 메시지가 계속 전송됩니까?**

답변: 아니요. 몇 분 동안 메시지가 전송되지 않습니다. 업그레이드가 완료되면 프로세스가 자동으로 다시 시작됩니다.

**질문: 워크플로우가 계속 실행되고 게재가 전송됩니까?**

답변: 아니요. 빌드 업그레이드 중에 워크플로우 서버와 MTA가 모두 중지됩니다. 즉, 워크플로우가 실행되지 않고 몇 분 동안 게재가 전송되지 않습니다. 조치할 필요가 없으며 인스턴스가 업그레이드되자마자 워크플로우가 다시 시작됩니다.

**질문: 업그레이드 중에도 메시지의 링크 추적이 계속 작동합니까?**

답변: 그렇습니다. 업그레이드 중에는 새 이메일을 보낼 수 없지만 이미 보낸 이메일에 포함된 링크 추적은 작동합니다.

**질문: 업그레이드가 완료되었음을 어떻게 알 수 있습니까?**

답변: Campaign에 로그인하면 최신 버전과 함께 릴리스 알림 팝업이 표시됩니다.

기타 문의 사항은 [Adobe Client Care](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
