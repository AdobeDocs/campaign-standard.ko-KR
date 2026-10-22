---
title: Campaign Standard API 시작
description: Campaign과 다양한 기술의 통합을 통해 고유한 에코시스템을 빌드할 수 있습니다.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: c6968252-a012-4029-bbb8-66f4f693e99b
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: f5407121-8933-4ac3-8e06-a9b692a4e88a
    internal-label: Campaign Standard
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
    internal-label: APIs
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: bb37e2bfbc52de1b0cc03f0f8e03985caff5e5b0
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 100%
---
# Campaign Standard API 시작 {#get-started-apis}

Campaign Standard API는 사용자가 사용하는 기술 패널과 Adobe Campaign Standard을 연결하여 Adobe Campaign Standard를 위한 **통합을 만들고** **고유한 에코시스템을 구축**&#x200B;할 수 있도록 해줍니다.

Adobe Campaign Standard API를 사용하면 다음 기능에 액세스할 수 있습니다.

<table style="table-layout:fixed; margin-top: 0px; margin-bottom: 0px;">
<tbody><tr style="border: 0;background-color: #FFFFFF;">
<td valign="top"><a href="../../api/using/retrieving-profiles.md"><img width="50px" alt="조건" src="assets/icon_profile.svg"/></a><p><a href="../../api/using/retrieving-profiles.md">프로필</a></p></td>
<td valign="top"><a href="../../api/using/creating-a-service.md"><img width="50px" alt="조건" src="assets/icon_services.svg"/></a><p><a href="../../api/using/creating-a-service.md">서비스 및 구독</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-custom-resources.md"><img width="50px" alt="조건" src="assets/icon_customresources.svg"/></a><p><a href="../../api/using/interacting-with-custom-resources.md">사용자 정의 리소스</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-marketing-history.md"><img width="50px" alt="조건" src="assets/icon_marketinghistory.svg"/></a><p><a href="../../api/using/interacting-with-marketing-history.md">마케팅 기록</a></p></td>
</tr>
<tr style="border: 0;background-color: #FFFFFF;">
<td valign="top"><a href="../../api/using/creating-a-privacy-request.md"><img width="50px" alt="조건" src="assets/icon_privacy.svg"/></a><p><a href="../../api/using/creating-a-privacy-request.md">개인 정보 보호 관리</a></p></td>
<td valign="top"><a href="../../api/using/managing-transactional-messages.md"><img width="50px" alt="조건" src="assets/icon_transactionalmessage.svg"/></a><p><a href="../../api/using/managing-transactional-messages.md">트랜잭션 메시지</a></p></td>
<td valign="top"><a href="../../api/using/controlling-a-workflow.md"><img width="50px" alt="조건" src="assets/icon_workflows.svg"/></a><p><a href="../../api/using/controlling-a-workflow.md">워크플로</a></p></td>
<td valign="top"><a href="../../api/using/retrieving-an-organizational-unit.md"><img width="50px" alt="조건" src="assets/icon_units.svg"/></a><p><a href="../../api/using/retrieving-an-organizational-unit.md">조직 단위</a></p></td>
</tr></tbody></table>

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
