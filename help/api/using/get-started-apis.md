---
title: Campaign Standard API 시작
description: Adobe Campaign과 다양한 기술의 통합을 통해 고유한 에코시스템을 구축할 수 있습니다.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4ae70ca95cb282a694c41361d859b19385db5673
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 93%

---


# Campaign Standard API 시작 {#get-started-apis}

Campaign Standard API는 사용자가 사용하는 기술 패널과 Adobe Campaign Standard을 연결하여 Adobe Campaign Standard를 위한 **통합을 만들고** **고유한 에코시스템을 구축**&#x200B;할 수 있도록 해줍니다.

Adobe Campaign Standard API를 사용하면 다음 기능에 액세스할 수 있습니다.

<table><tr>
 <td valign="top"><a href="../../api/using/retrieving-profiles.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a><p><a href="../../api/using/retrieving-profiles.md">프로필</a></p></td>
<td valign="top"><a href="../../api/using/creating-a-service.md"><img width="60px" alt="조건" src="assets/icon_services.svg"/></a><p><a href="../../api/using/creating-a-service.md">서비스 및 구독</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="조건" src="assets/icon_customresources.svg"/></a><p><a href="../../api/using/interacting-with-custom-resources.md">사용자 정의 리소스</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="조건" src="assets/icon_marketinghistory.svg"/></a><p><a href="../../api/using/interacting-with-marketing-history.md">마케팅 기록</a></p></td>
</tr>
<tr>
<td valign="top"><a href="../../api/using/creating-a-privacy-request.md"><img width="60px" alt="조건" src="assets/icon_privacy.svg"/></a><p><a href="../../api/using/creating-a-privacy-request.md">개인 정보 관리</a></p></td>
<td valign="top"><a href="../../api/using/managing-transactional-messages.md"><img width="60px" alt="조건" src="assets/icon_transactionalmessage.svg"/></a><p><a href="../../api/using/managing-transactional-messages.md">트랜잭션 메시지 </a></p></td>
<td valign="top"><a href="../../api/using/controlling-a-workflow.md"><img width="60px" alt="조건" src="assets/icon_workflows.svg"/></a><p><a href="../../api/using/controlling-a-workflow.md">워크플로우</a></p></td>
<td valign="top"><a href="../../api/using/retrieving-an-organizational-unit.md"><img width="60px" alt="조건" src="assets/icon_units.svg"/></a><p><a href="../../api/using/retrieving-an-organizational-unit.md">조직 단위</a></p></td>
</tr></table>

>[!NOTE]
>
>API 호출을 수행하기 전에 라이선스 계약에 해당하는 크기 제한 사항을 확인하십시오. 자세한 정보는 이 [페이지](https://helpx.adobe.com/kr/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers)를 참조하십시오.

Campaign Standard API를 사용하려면 Adobe I/O 계정이 필요합니다. 이는 API 기능을 앞으로 나아가고 검색하기 위한 필수 첫 단계입니다.
이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/setting-up-api-access.md)을 참조하십시오.

Adobe가 제공하는 API는 REST 인터페이스 및 JSON 페이로드와 함께 **표준 개념**&#x200B;을 사용합니다.

>[!NOTE]
>
>모든 예는 Postman과 함께 작동하지만 좋아하는 REST 클라이언트를 자유롭게 사용할 수 있습니다.

모든 엔드포인트는 API, 전체 API 참조, 코드 예제 및 빠른 시작 안내서를 조작할 때 알아야 하는 일반적인 개념과 함께 이 설명서에서 광범위하게 설명됩니다.

누락되었거나 잘못된 것 같은 경우에는 [커뮤니티](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)에 문의하십시오.
