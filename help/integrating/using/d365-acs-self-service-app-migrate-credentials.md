---
title: Campaign-Dynamics 통합 앱 구성
description: Campaign-Dynamics 통합 앱을 구성하는 방법 알아보기
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: e0fb289a-6b6e-473d-80af-50f6d0d72af1
source-git-commit: abdcd3f9f7f709818dee794b4c830e486fefa290
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 1%

---

# 자격 증명을 JWT에서 OAuth로 서버 간 마이그레이션

서비스 계정(JWT) 자격 증명은 새 OAuth 서버 간 자격 증명을 위해 더 이상 사용되지 않습니다. 새 자격 증명을 사용하면 Adobe 애플리케이션을 보다 쉽게 유지 관리할 수 있습니다. 또한 정기적으로 인증서를 회전해야 하는 필요성을 없애고 표준 OAuth2 라이브러리를 사용하여 즉시 작동합니다.

서비스 계정(JWT) 자격 증명은 더 이상 사용되지 않는 것으로 표시되었지만, 2025년 1월 1일까지 계속 작동합니다. 따라서 2025년 1월 1일 이전에 새로운 OAuth 서버 간 자격 증명을 사용하려면 통합을 마이그레이션해야 합니다. 자세한 내용은 [사용 중단 타임라인](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/#deperecation-timelines)을 확인하세요.

## JWT에서 OAuth 서버 간 자격 증명으로 마이그레이션하는 단계

OAuth 서버 간 자격 증명으로의 마이그레이션은 애플리케이션에 대한 다운타임 없이 마이그레이션할 수 있는 간단한 프로세스입니다. 아래 단계에 따라 자격 증명을 마이그레이션할 수 있습니다.

1. [Adobe Developer Console](https://developer.adobe.com/console)에 로그인
2. 왼쪽의 필터링 메뉴에서 서비스 계정(JWT) 자격 증명 있음 옵션을 선택합니다. 이 방법으로 서비스 계정(JWT) 자격 증명이 있는 모든 프로젝트가 표시됩니다. 프로젝트 목록에서 마이그레이션할 프로젝트를 클릭합니다.

   ![](assets/JwtToOAuthMigration1.png)

3. 왼쪽 탐색에서 서비스 계정(JWT) 자격 증명 탭을 열고 마이그레이션 카드를 확인합니다. 마이그레이션 카드에서 **새 자격 증명 추가** 단추를 클릭하여 해당 OAuth 서버 간 자격 증명을 추가합니다. 프로젝트에 OAuth 서버 간 자격 증명을 추가하면 마이그레이션이 시작됩니다.
   ![](assets/JwtToOAuthMigration2.png)
4. 새 자격 증명 **OAuth 서버 간**&#x200B;이(가) 왼쪽 탐색에 추가됩니다.
   * 마이그레이션을 취소하려면 마이그레이션 취소 를 클릭합니다.
   * 새 자격 증명 OAuth 서버 간 작동 여부를 확인할 때까지 검토 및 삭제 단추를 클릭하지 마십시오.

     ![](assets/JwtToOAuthMigration3.png)

5. Microsoft Dynamics 365의 자격 증명을 Adobe Campaign Standard 앱으로 업데이트
   * 통합 앱에 로그인하고 설정 페이지로 이동합니다.
   * 인증 유형으로 OAuth를 선택합니다.
   * 새 OAuth 서버 간 자격 증명은 이전 서비스 계정(JWT) 자격 증명과 동일한 자격 증명을 사용하므로 대부분의 필드가 이미 채워집니다.
   * 클라이언트 ID 및 클라이언트 암호를 입력합니다. 이러한 속성은 Adobe Developer Console의 프로젝트에서 찾을 수 있습니다.
   * 저장 을 클릭하여 설정을 저장합니다.

     ![](assets/JwtToOAuthMigration4.png)

6. 새 자격 증명이 작동하는지 확인
   * 통합 앱에 로그인하고 워크플로우 페이지로 이동합니다.
   * 활성 워크플로우를 중지합니다. 워크플로우가 중지될 때까지 기다립니다.
   * 워크플로우를 시작합니다. 워크플로우가 실행 중 상태가 될 때까지 기다립니다.
   * 워크플로우를 몇 분 동안 모니터링하여 워크플로우가 올바르게 작동하는지 확인합니다. Adobe Campaign Standard 및 Microsoft Dynamics 365에서 데이터를 확인하여 데이터가 올바르게 동기화되고 있는지 확인할 수도 있습니다.

7. 마이그레이션을 완료하려면 JWT 자격 증명을 삭제하십시오.
   * [Adobe Developer Console](https://developer.adobe.com/console)에 로그인
   * 프로젝트를 클릭하고 마이그레이션한 프로젝트를 선택합니다.
   * 왼쪽 탐색에서 서비스 계정(JWT) 자격 증명 탭을 클릭합니다.
   * 검토 및 삭제 버튼을 클릭합니다.

     ![](assets/JwtToOAuthMigration5.png)
   * 마지막 액세스 또는 마지막으로 사용한 메뉴의 타임스탬프를 검토하여 통합 앱이 새 OAuth 자격 증명을 사용하여 액세스 토큰을 생성하고 있는지 또는 이전 JWT 자격 증명을 계속 사용하고 있는지 확인하십시오.

     ![](assets/JwtToOAuthMigration6.png)
   * 통합 앱에서 새 OAuth 자격 증명을 사용하고 있으며 JWT 자격 증명을 더 이상 사용하지 않는 것이 확인되면 **확인 및 계속** 버튼을 클릭하여 이전 자격 증명을 삭제하는 작업을 계속 진행하여 마이그레이션을 완료합니다.

     ![](assets/JwtToOAuthMigration7.png)
