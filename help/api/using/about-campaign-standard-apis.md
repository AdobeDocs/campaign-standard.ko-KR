---
title: Campaign Standard API 정보
description: Campaign Standard API에 대한 자세한 내용
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
source-git-commit: 27ca2116c49f9c23a56c178a3e3f7baf2f755c45

---


# Campaign Standard API 정보 {#about-campaign-standard-apis}

Campaign Standard API는 Adobe Campaign Standard에 대한 통합을 ******만들고 사용하는 기술 패널과 Adobe Campaign Standard를 연계하여 고유한 에코시스템을** 구축할 수 있도록 하기 위한 것입니다.

Adobe Campaign Standard API를 사용하면 다음 기능에 액세스할 수 있습니다.

<table>
<tr>
    <td valign="top">
        <a href="../../api/using/retrieving-profiles.md"><img width="60px" alt="조건" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/creating-a-service.md"><img width="60px" alt="조건" src="assets/icon_services.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="조건" src="assets/icon_customresources.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="조건" src="assets/icon_marketinghistory.svg"/></a>
    </td>
</tr>
<tr>
<td>프로필</td>
<td>서비스 및 구독</td>
<td>사용자 정의 리소스</td>
<td>마케팅 내역</td>
</tr>
<tr>
    <td valign="top">
        <a href="../../api/using/creating-a-privacy-request.md"><img width="60px" alt="조건" src="assets/icon_privacy.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/managing-transactional-messages.md"><img width="60px" alt="조건" src="assets/icon_transactionalmessage.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/controlling-a-workflow.md"><img width="60px" alt="조건" src="assets/icon_workflows.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/retrieving-an-organizational-unit.md"><img width="60px" alt="조건" src="assets/icon_units.svg"/></a>
    </td>
</tr>
<tr>
<td>개인 정보 관리</td>
<td>트랜잭션 메시지</td>
<td>워크플로우</td>
<td>조직 단위</td>
</td>
</table>

>[!NOTE]
>
>API 호출을 수행하기 전에 라이선스 계약에 해당하는 크기 제한 사항을 확인하십시오. For more on this, refer to [this page](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

Campaign Standard API를 사용하려면 Adobe I/O 계정이 필요합니다. 이 단계는 API 기능을 계속 진행하여 검색하기 위한 필수 첫 번째 단계입니다.
For more on this, refer to [this section](../../api/using/setting-up-api-access.md).

REST 인터페이스 및 JSON 페이로드와 함께 **표준 개념을** 사용하는 API를 제공합니다.

>[!NOTE]
>
>모든 예는 Postman과 연동되지만 즐겨 사용하는 REST 클라이언트를 자유롭게 사용할 수 있습니다.

모든 끝점은 API, 전체 API 참조, 코드 예제 및 빠른 시작 안내선을 조작하기 위해 알아야 하는 일반적인 개념과 함께 이 설명서에서 광범위하게 설명됩니다.

누락되었거나 잘못된 것 같으면 [커뮤니티에](https://help-forums.adobe.com/content/adobeforums/en/campaign-forum/adobe-campaign.html)문의하십시오.