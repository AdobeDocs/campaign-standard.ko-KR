---
title: Adobe Campaign 통합을 통해 이메일 디자인
description: 이메일 디자이너에서 Adobe Campaign 통합을 통해 이메일을 디자인하는 방법을 알아봅니다.
audience: designing
content-type: reference
topic-tags: editing-email-content
feature: Email Design
role: User
level: Intermediate
exl-id: d5c72f69-68a2-4523-956f-f265ae79b470
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 8%

---

# 멀티 솔루션 이메일 디자인 {#multi-solution-email-design}

Adobe Campaign에서는 여러 이메일 작성 옵션을 제공합니다. Dreamweaver 등의 솔루션을 사용하여 이메일 콘텐츠를 편집하고 이메일 디자이너에서 응답형 메시지를 만들 수 있습니다. Adobe Campaign Standard에서 Adobe Experience Manager으로 콘텐츠를 이메일로 보내고 이메일에서 사용할 수도 있습니다.

## Dreamweaver에서 컨텐츠 편집 {#editing-content-in-dreamweaver}

Dreamweaver과 Adobe Campaign Standard 통합을 사용하면 Dreamweaver 인터페이스에서 이메일의 컨텐츠를 편집할 수 있습니다. 반응형 이메일 콘텐츠를 디자인하고 개발할 수 있는 Dreamweaver의 강력한 인터페이스에 액세스할 수 있습니다.

* **양방향 동기화**

   한 제품에서 편집이 수행될 때마다 다른 제품에서 실시간으로 업데이트됩니다. Dreamweaver에서 텍스트 색상을 변경하려는 경우 편집하는 즉시 텍스트 색상이 Campaign에서 라이브로 적용됩니다. 또한 Dreamweaver 또는 Campaign에서 코드를 선택하는 경우 줄 번호가 동일하므로 두 제품 간에 선택 사항이 유지되므로 코드에서 특정 항목을 찾을 때 매우 유용합니다.

* **Dreamweaver를 통해 로컬 이미지를 Adobe Campaign에 업로드**

   Dreamweaver 내에서 이메일을 만들거나 편집할 때 데스크탑 또는 로컬 시스템에서 이미지를 선택하면 됩니다. Dreamweaver에서는 항상 이 작업을 수행할 수 있었지만 Dreamweaver 및 Campaign이 연결되면 로컬 파일이 Adobe Campaign 서버에 즉시 업로드됩니다. 컨텐츠 변경 사항으로 이미지를 수동으로 업로드할 필요가 없습니다. 또한 최신 이미지가 항상 Campaign에서 활성화되도록 합니다.

* **Dreamweaver에서 Campaign 개인화 추가**

   이메일 개발자의 경우 더 이상 다음과 같은 텍스트를 추가할 필요가 없습니다 `[[FIRSTNAME_PLACEHOLDER]]` 또한 데이터 모델 테이블의 구문을 검색할 수도 없습니다. Dreamweaver의 캠페인 도구 모음은 Campaign 인스턴스의 데이터 모델에 직접 연결됩니다. 즉, 이름 과 주소 등 개인화에 필요한 모든 데이터를 가져올 수 있습니다. Campaign 내에서 콘텐츠 블록을 만든 경우 이를 Dreamweaver에 직접 가져올 수도 있습니다.

이 기능은 Dreamweaver 설명서에서 액세스 가능한 세부 사항으로 설명되어 있습니다 [여기](https://helpx.adobe.com/kr/dreamweaver/using/working-with-dreamweaver-and-campaign.html).

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

## Experience Manager에서 컨텐츠 편집 {#editing-content-in-experience-manager}

이메일 콘텐츠는 Experience Manager에서 편집한 다음 Adobe Campaign Standard에서 한 개 또는 여러 개의 이메일 메시지에 사용할 수 있습니다. 을(를) 참조하십시오. [이 문서](../../integrating/using/integrating-with-experience-manager.md).

## 제품 목록 {#product-listing}

>[!CONTEXTUALHELP]
>id="ac_product_listing"
>title="제품 목록 사용"
>abstract="제품 목록을 사용하여 데이터 컬렉션을 참조하고 이메일 콘텐츠에 표시할 수 있습니다."

제품 목록을 사용하면 이메일 콘텐츠에서 하나 이상의 데이터 컬렉션을 참조할 수 있습니다. 이러한 목록은 트랜잭션 전자 메일에 사용할 수 있습니다. 이 기능에 대한 전용 섹션을 사용할 수 있습니다 [여기](../../designing/using/using-product-listings.md).

## 이메일 디자인 옵션 비교 {#email-design-options-comparison}

Adobe Campaign에서는 여러 이메일 작성 옵션을 제공합니다. 아래 표에는 각 솔루션의 주요 가능성, 이점 및 제한 사항이 나와 있습니다.

<table> 
 <thead> 
  <tr> 
   <th> </th> 
   <th> 이메일 디자이너<br /> </th> 
   <th> Experience Manager<br /> </th> 
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
   <td> <strong>쓰기 HTML</strong><br /> </td> 
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
   <td> AEM에서 미리 보기<br /> Campaign의 증명<br /> </td> 
   <td> Campaign에서 미리 보기 및 증명<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>제품 목록</strong><br /> </td> 
   <td> 전자 메일 트랜잭션 메시지에서 지원됨<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
   <td> 지원되지 않음<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>이점</strong><br /> </td> 
   <td> 
     <p>- 드래그 앤 드롭 경험을 통해 손쉽게 이메일 구축</p>
     <p>- 기존 콘텐츠 편집기와 유사한 기능</p>
     <p>- 조각을 사용한 재사용 가능한 콘텐츠</p>
  </td> 
   <td> 
     <p>- 이메일에서 웹 사이트의 자산 재사용</p>
     <p>- 이메일 콘텐츠에서 Experience Manager의 강력한 활용</p>
    </td> 
   <td> 
    <p>- 개발자가 직접 이메일을 코딩하는 기능</p>
    <p>- 양방향 동기화</p>
    <p>- Dreamweaver에서 오프라인으로 편집하고 나중에 동기화</p>
    <p>- Dreamweaver을 통해 Adobe Campaign에 이미지 업로드</p>
  </td> 
  </tr> 
  <tr> 
   <td> <strong>제한 사항</strong><br /> </td> 
   <td> 
     <p>- 조각 내에 조건부 콘텐츠 없음</p>
     <p>- Experience Manager 조각을 사용할 수 없습니다.</p>
  </td> 
   <td> 
     <p>- 고급 개인화를 구현하기 어려움</p>
     <p>- Adobe Campaign에서 테스트 보내기 필요</p>
  </td> 
   <td> 동적 콘텐츠가 지원되지 않음<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>대상자</strong><br /> </td> 
   <td> 드래그 앤 드롭 기능과 함께 HTML 구성 요소를 사용할 수 있도록 유연성을 유지하려는 마케터<br /> </td> 
   <td> 마케터는 개인화가 거의 없는 표준 이메일 템플릿을 사용하려는 Experience Manager을 이미 사용하고 있습니다<br /> </td> 
   <td> 이메일 콘텐츠를 코딩하고 Adobe Campaign과 직접 통합하려는 개발자<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>추가 정보</strong><br /> </td> 
   <td> 자세한 내용은 <a href="../../designing/using/designing-content-in-adobe-campaign.md">이메일 디자이너 정보</a>.<br /> </td> 
   <td> 자세한 내용은 <a href="../../integrating/using/integrating-with-experience-manager.md">Experience Manager과 통합</a>.<br /> </td> 
   <td> 자세한 내용은 <a href="https://helpx.adobe.com/kr/dreamweaver/using/working-with-dreamweaver-and-campaign.html">Dreamweaver 및 캠페인</a> 이걸 보고 <a href="#video">비디오</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 튜토리얼 비디오 {#video}

이 비디오에서는 Dreamweaver을 사용하여 Adobe Campaign Standard용 컨텐츠를 만들고 편집하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/23121?quality=12&captions=eng)

추가 Campaign Standard 방법 비디오를 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko).
