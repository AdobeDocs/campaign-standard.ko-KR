---
title: 'Adobe Campaign 통합을 통해 이메일 디자인 '
description: 이메일 디자이너의 Adobe Campaign 통합을 통해 이메일을 디자인하는 방법을 살펴볼 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 디자인
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---

# 멀티 솔루션 이메일 디자인 {#multi-solution-email-design}

## Dreamweaver에서 컨텐츠 편집 {#editing-content-in-dreamweaver}

Dreamweaver와 Adobe Campaign Standard의 통합을 통해 Dreamweaver 인터페이스에서 이메일의 컨텐츠를 편집할 수 있습니다. Dreamweaver의 강력한 인터페이스를 사용하여 반응형 이메일 컨텐츠를 디자인하고 개발할 수 있습니다.

* **양방향 동기화**

   한 제품에서 편집이 수행될 때마다 다른 제품에서 실시간으로 업데이트됩니다. Dreamweaver에서 텍스트 색상을 변경하려는 경우 편집과 동시에 텍스트 색상이 Campaign에 적용됩니다. 또한 Dreamweaver 또는 Campaign에서 코드를 선택하면 라인 번호가 동일하므로 선택한 항목이 두 제품 사이에 그대로 유지되므로 코드에서 특정 항목을 찾을 때 매우 유용합니다.

* **Dreamweaver를 통해 Adobe Campaign에 로컬 이미지 업로드**

   Dreamweaver에서 이메일을 만들거나 편집할 때 데스크탑 또는 로컬 시스템에서 이미지를 선택하면 됩니다. Dreamweaver에서는 항상 이렇게 할 수 있었지만 Dreamweaver 및 Campaign이 연결되면 로컬 파일이 Adobe Campaign 서버에 즉시 업로드됩니다.컨텐츠를 변경할 때 수동으로 이미지를 업로드할 필요가 없습니다. 또한 최신 이미지가 항상 Campaign에서 라이브되도록 합니다.

* **Dreamweaver에서 캠페인 개인화 추가**

   이메일 개발자의 경우 더 이상 데이터 모델 표의 구문과 같은 텍스트를 추가하거나 찾을 필요가 `[[FIRSTNAME_PLACEHOLDER]]` 없습니다. Dreamweaver의 캠페인 도구 모음은 캠페인 인스턴스의 데이터 모델에 직접 연결됩니다. 즉, 이름과 주소 등 개인화에 필요한 모든 데이터를 가져올 수 있습니다. Campaign 내에서 컨텐츠 블록을 만든 경우 Dreamweaver로 직접 가져올 수도 있습니다.

이 기능은 [여기에서](https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html)액세스할 수 있는 Dreamweaver 문서에서 자세히 설명합니다. 데모 [비디오도](https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html) 제공됩니다.

## Experience Manager에서 콘텐츠 편집 {#editing-content-in-experience-manager}

이메일 컨텐츠는 Adobe Experience Manager에서 편집한 다음 Adobe Campaign Standard에서 하나 또는 여러 개의 이메일 메시지에 사용할 수 있습니다. 이 [문서를](../../integrating/using/integrating-with-experience-manager.md)참조하십시오.

## 이메일 디자인 옵션 비교 {#email-design-options-comparison}

Adobe Campaign은 다양한 이메일 작성 옵션을 제공합니다. 아래 표는 각 기능에 대한 주요 가능성, 이점 및 제한 사항을 보여줍니다.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> Email Designer<br /> </th> 
   <th> Adobe Experience Manager<br /> </th> 
   <th> Dreamweaver<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <strong>빈 이메일 시작</strong><br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원됨<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HTML 작성</strong><br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
   <td> 지원됨<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HTML 업데이트</strong><br /> </td> 
   <td> HTML 구성 요소 내에서만<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
   <td> 지원됨<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>기본 개인화</strong><br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원됨<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>고급 개인화</strong><br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>증명/미리 보기</strong><br /> </td> 
   <td> 지원됨<br /> </td> 
   <td> 캠페인에서 AEM<br /> Proof에서 미리 보기<br /> </td> 
   <td> 캠페인에서 미리 보기 및 증명<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>제품 목록</strong><br /> </td> 
   <td> 이메일 트랜잭션 메시지에서 지원<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>이점</strong><br /> </td> 
   <td> 
     - 드래그 앤 드롭 경험을<br/>통한 간편한 이메일 제작 - 기존 컨텐츠 편집기와<br/>유사한 기능 - 조각을 사용한 재사용 가능한 컨텐츠
  </td> 
   <td> 
     - 이메일에서<br/>웹 사이트의 에셋 재사용 - 이메일 컨텐츠에서 Adobe Experience Manager 활용
    </td> 
   <td> 
    - 개발자가 직접 이메일을<br/>코딩할 수 있는 기능 - 양방향 동기화<br/>- Dreamweaver에서 오프라인으로 편집하고 나중에<br/>동기화 - Dreamweaver를 통해 Adobe Campaign에 이미지 업로드
  </td> 
  </tr> 
  <tr> 
   <td> <strong>제한 사항</strong><br /> </td> 
   <td> 
     - 조각<br/>내에 조건부 컨텐츠 없음 - Experience Manager 조각 사용을 할 수 없습니다.
  </td> 
   <td> 
     - 구현하기<br/>어려운 고급 개인화 - Adobe Campaign에서 테스트를 전송해야 함
  </td> 
   <td> 동적 콘텐츠가 지원되지 않음<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>고객</strong><br /> </td> 
   <td> 드래그 앤 드롭 기능과 함께 HTML 구성 요소를 유연하게 사용하려는 마케터<br /> </td> 
   <td> 마케터는 이미 Adobe Experience Manager를 사용하여 개인화를 거의 하지 않고 표준 이메일 템플릿을 사용하고 있습니다.<br /> </td> 
   <td> 이메일 컨텐츠를 코딩하고 Adobe Campaign과 직접 통합하려는 개발자<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>자세한 내용</strong><br /> </td> 
   <td> 이메일 <a href="../../designing/using/overview.md">디자이너 정보 보기</a><br /> </td> 
   <td> See <a href="../../integrating/using/integrating-with-experience-manager.md">Integrating with Experience Manager</a><br /> </td> 
   <td> Dreamweaver <a href="https://helpx.adobe.com/dreamweaver/using/working-with-dreamweaver-and-campaign.html">및 Campaign</a> 보기 및 이 <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html">비디오 보기</a><br /> </td> 
  </tr> 
 </tbody> 
</table>
