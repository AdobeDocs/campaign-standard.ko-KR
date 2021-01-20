---
solution: Campaign Standard
product: campaign
title: Campaign Standard API의 장점?
description: Campaign Standard API 및 API 사용에 대한 자세한 내용을 살펴보십시오.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 9eca72e744524cf201d998abd9acf718fdaca0f8
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 3%

---


# Campaign Standard API의 장점 {#why-using-campaign-standard-apis}

Adobe Campaign Standard은 기존 시스템이 캠페인 플랫폼과 통합되므로 실시간으로 실제 문제를 해결할 수 있는 API를 제공합니다.

등록 페이지 또는 옵트아웃 페이지와 같은 공개 웹 사이트는 프로필 정보를 저장하기 위해 백엔드 시스템에 연결해야 합니다. Adobe Campaign과 같은 백엔드 시스템은 프로필 데이터를 인제스트하여 사용자 정의 작업을 수행할 수 있는 유연성과 능력을 갖추고 있습니다.

다음은 몇 가지 예입니다.

* 잠재 고객 온라인 등록
* 기존 고객 프로파일 및 마케팅 커뮤니케이션 환경 설정 관리
* 이벤트 기반 트랜잭션 통신 트리거 - 주문 확인, 예약 일정, 암호 재설정 등
* 장바구니에 담긴 이메일 커뮤니케이션도 포기

등록 랜딩 페이지는 고객이나 잠재 고객이 자신의 이름과 이메일 주소를 등록할 수 있는 방법을 제공합니다. Campaign Standard은 프로파일 정보와 환경 설정을 캡처한 후 고객의 관심사에 따라 개인화된 메시지를 보낼 수 있습니다.

이러한 템플릿은 아래 요소로 만들어집니다.

1. 캠페인 API 리스너가 있는 등록 양식입니다.

   ![대체 텍스트](assets/apis_uc1.png)

1. 확인란을 기반으로 할 사용자 지정 작업. &quot;특별 혜택 이메일&quot;을 선택하면 일반적인 등록 과정과 비교하여 선물 쿠폰이 있는 다른 사용자 정의 메일이 전송됩니다.

   ![대체 텍스트](assets/apis_uc2.png)

1. 프로필은 이메일의 &quot;세부 정보 업데이트&quot; 링크를 클릭한 후 세부 사항을 변경할 수 있습니다. 그러면 &quot;프로필 및 환경 설정 세부 사항 업데이트&quot; 페이지가 표시됩니다. 작업을 수행하려면 프로필 세부 사항(Pkey)이 캠페인 서버로 전달되고 프로필이 검색되고 표시됩니다. 프로파일이 &quot;업데이트&quot; 버튼을 클릭하면 정보가 PATCH 명령을 통해 시스템에 업데이트됩니다.

   ![대체 텍스트](assets/apis_uc3.png)

요청 컬렉션은 Campaign Standard API 요청에 익숙해지는 데 도움이 됩니다. JSON 형식의 이 컬렉션은 일반적인 사용 사례를 나타내는 미리 디자인된 API 요청을 제공합니다.

아래 단계에서는 컬렉션을 가져와 사용하여 Campaign Standard 데이터베이스에 프로파일을 만드는 단계별 사용 사례를 설명합니다.

>[!NOTE]
>
>예를 들면 Postman이 사용됩니다. 그러나 좋아하는 REST 클라이언트를 자유롭게 사용할 수 있습니다.

1. 여기에서 [여기](https://helpx.adobe.com/content/dam/help/en/campaign/kb/working-with-acs-api/_jcr_content/main-pars/download_section/download-1/KB_postman_collection.json.zip)를 클릭하여 JSON 컬렉션을 다운로드합니다.

1. Postman을 열고 **파일** / **가져오기** 메뉴를 선택합니다.

1. 다운로드한 파일을 창으로 드래그하여 놓습니다. 미리 디자인된 API 요청이 표시되고 사용할 준비가 됩니다.

   ![대체 텍스트](assets/postman_collection.png)

1. **프로필** 요청 만들기를 선택한 다음 POST 요청과 **헤더** 탭을 사용자 고유의 정보로 업데이트합니다(&lt;ORGANIZATION>, &lt;API_KEY>, &lt;ACCESS_TOKEN>). 이 작업에 대한 자세한 정보는 [이 섹션](../../api/using/setting-up-api-access.md)을 참조하십시오.

   ![대체 텍스트](assets/postman_uc1.png)

1. 새 프로필에 추가할 정보를 **본문** 탭에 입력한 다음 **보내기** 단추를 클릭하여 요청을 실행합니다.

   ![대체 텍스트](assets/postman_uc2.png)

1. 객체를 만든 후 기본 키(PKey)가 해당 객체에 연결됩니다. 다른 속성은 물론 응답 응답에서도 볼 수 있습니다.

   ![대체 텍스트](assets/postman_uc3.png)

1. Campaign Standard 인스턴스를 열고 페이로드의 모든 정보와 함께 프로필이 만들어졌는지 확인합니다.

   ![대체 텍스트](assets/postman_uc4.png)
