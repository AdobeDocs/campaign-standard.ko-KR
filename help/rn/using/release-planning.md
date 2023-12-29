---
title: Campaign Standard 릴리스 계획
description: 이 페이지에는 Adobe Campaign Standard의 향후 릴리스 목록이 있습니다.
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning
feature: Overview
role: User
level: Beginner
exl-id: 1f48d4da-5622-4fab-af87-fcce0e40ade1
source-git-commit: 311fdf000333c03cb3b21fc6fea786251ced045f
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 100%

---

# 릴리스 계획 {#release-planning}

Adobe는 새로운 기능, 개선 사항 및 수정 사항을 추가하여 솔루션을 지속적으로 개선합니다.

모든 Adobe Campaign Standard 인스턴스는 새로운 릴리스마다 업그레이드됩니다. 업그레이드하기 위해 필요한 작업은 없습니다.

업그레이드는 두 단계로 배포됩니다. 먼저 Stage 인스턴스가 업그레이드되어 고객이 새로운 기능을 테스트하고 필요한 경우 구성을 변경할 수 있습니다. 그런 다음 프로덕션 인스턴스가 업그레이드됩니다.

모든 릴리스 날짜는 변경될 수 있습니다. 업데이트를 확인하려면 이 페이지를 정기적으로 방문하십시오. 아래에 표시된 기간 동안 환경이 연속적으로 업데이트됩니다. 정확한 날짜는 각 고객에게 이메일로 전달됩니다.

## 릴리스 24.1 - 2024년 겨울 릴리스 {#release-24-1-release}

이 릴리스에 대한 자세한 내용은 스테이징 환경 업그레이드가 시작되기 일주일 전에 [릴리스 정보](release-notes.md)에서 확인할 수 있습니다.

<table>
 <thead>
  <tr>
   <th> 환경 </th>
   <th> 날짜 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>단계 </td>
   <td>2024년 1월 16일 - 2월 13일 </td>
  </tr>
  <tr>
   <td>프로덕션 </td>
   <td>2024년 1월 23일 - 2월 20일 </td>
  </tr>
 </tbody>
</table>


## 릴리스 23.2 - 2023년 가을 제한 릴리스 {#release-23-2-release}


>[!AVAILABILITY]
>
>이 릴리스는 일부 조직에만 적용될 수 있습니다(제한 공개). 자세한 내용은 Adobe 담당자에게 문의하세요.

이 릴리스에 대한 자세한 내용은 [릴리스 정보](release-notes.md)를 참조하십시오.

<table>
 <thead>
  <tr>
   <th> 환경 </th>
   <th> 날짜 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>단계 </td>
   <td>2023년 10월 3~9일 </td>
  </tr>
  <tr>
   <td>프로덕션 </td>
   <td>2023년 10월 12~18일 </td>
  </tr>
 </tbody>
</table>

추가 질문은 [Adobe 클라이언트 지원 센터](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.

## 질문 및 답변 {#questions-and-answers}

**질문: 어떤 영향이 있습니까?**

답변: 변경 사항은 관련 설명서에 대한 링크를 포함하여 [릴리스 정보](../../rn/using/release-notes.md)에 나열되어 있습니다. [더 이상 사용되지 않는 기능 및 제거된 기능 페이지](../../rn/using/deprecated-features.md)를 참조하는 것을 권장합니다. 이 페이지는 스테이징 환경 업그레이드 날짜에 새 릴리스에서 사용할 수 있습니다.

**질문: 유효성 검사 프로세스는 무엇입니까?**

답변: 스테이징 인스턴스가 업그레이드되면 프로세스 및 사용 사례가 이 새로운 버전에서 제대로 작동하는지 확인하고 문제가 발생하면 [Adobe Client Care](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 보고할 것을 권장합니다.

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

기타 문의 사항은 [Adobe Client Care](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
