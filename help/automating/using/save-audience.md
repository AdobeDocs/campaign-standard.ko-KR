---
title: 대상자 저장
description: 대상자 저장 활동을 사용하면 기존 대상을 업데이트하거나 워크플로우에서 업스트림 모집단에서 새 대상자를 만들 수 있습니다.
page-status-flag: 활성화 안 함
uuid: 8bb173-fa59-44a7-a2a5-49f45ba6bf99
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 자동화
content-type: reference
topic-tags: 타깃팅 활동
discoiquuid: 1f6bb048-7abd-499b-a4b0-187f9492dc47
context-tags: saveAudience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 대상자 저장{#save-audience}

## 설명 {#description}

![](assets/save_audience.png)

이 **[!UICONTROL Save audience]** 활동을 사용하면 기존 대상을 업데이트하거나 워크플로에서 업스트림 계산된 모집단에서 새 대상자를 만들 수 있습니다. 이 활동에서 만들거나 업데이트한 대상은 **목록** 또는 파일 **대상입니다** . 애플리케이션 대상 목록에 추가되고 **[!UICONTROL Audiences]** 메뉴를 통해 사용할 수 있습니다.

>[!NOTE]
>
>활동을 통해 생성된 대상이 추가 데이터로 증가된 경우 이러한 데이터를 사용하여 독립 실행형 **[!UICONTROL Save audience]** 제공을 개인화할 수 없습니다. 워크플로우에서 실행되는 전달에서만 사용할 수 있습니다.

또한 이 활동을 통해 프로파일을 Adobe Experience Cloud 대상/세그먼트로 내보낼 수 있습니다. 그러면 다른 Adobe Experience Cloud 솔루션에서 이러한 고객을 활용할 수 있습니다. 공유 대상에 대한 자세한 내용은 캠페인 및 [사용자 코어 서비스 작업을 참조하십시오](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).

## 사용 상황 {#context-of-use}

이 **[!UICONTROL Save audience]** 활동은 기본적으로 다시 사용할 수 있는 대상으로 변환하여 동일한 워크플로우에서 인구 그룹을 계산하게 하는 데 사용됩니다.

## 구성 {#configuration}

1. 워크플로우에 **[!UICONTROL Save audience]** 활동 삽입
1. 쿼리, 교차, 조합 또는 제외와 같은 다른 타깃팅 활동 뒤에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업의 ![](assets/edit_darkgrey-24px.png) 단추를 사용하여 엽니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Update an existing audience]**:기존 대상자를 선택하고 업데이트 유형을 선택합니다.

      * **[!UICONTROL Replace audience content with new data]**:전체 대상 컨텐츠가 대체됩니다. 이전 데이터가 손실됩니다. 대상 저장 활동의 인바운드 전환의 데이터만 유지됩니다.
      * **[!UICONTROL Complete audience with new data]**:이전 대상 데이터는 유지되고 대상 저장 활동의 인바운드 전환의 데이터가 여기에 추가됩니다.
   * **[!UICONTROL Create then update an audience]**:대상자 이름을 입력하고 업데이트 유형을 선택합니다. 대상이 아직 없는 경우 만들어집니다. 이미 존재하는 경우 선택한 모드에 따라 업데이트됩니다.

      * **[!UICONTROL Replace audience content with new data]**:전체 대상 컨텐츠가 대체됩니다. 이전 데이터가 손실됩니다. 대상 저장 활동의 인바운드 전환의 데이터만 유지됩니다.

         경고, 이 옵션은 업데이트된 대상의 대상 유형과 타깃팅 차원을 지웁니다.

      * **[!UICONTROL Complete audience with new data]**:이전 대상 데이터는 유지되고 대상 저장 활동의 인바운드 전환의 데이터가 여기에 추가됩니다.

         경고: 업데이트된 대상의 대상 유형 또는 타깃팅 차원이 워크플로우의 현재 구성과 호환되지 않는 경우 이 옵션을 사용하면 오류가 발생합니다. 예를 들어 쿼리에서 얻은 프로필로 파일 유형 대상을 완료할 수 없습니다.
   * **[!UICONTROL Create a new audience]**:만들 대상의 이름을 입력합니다. 대상이 만들어지는 시간과 날짜는 대상 이름에 자동으로 추가됩니다. 그러면 워크플로우가 실행될 때마다 대상이 고유하게 설정됩니다.
   * **[!UICONTROL Share in Adobe Experience Cloud]**:타깃팅된 프로필을 보유하고 있고 대상을 Adobe Experience Cloud로 내보내려는 경우 이 옵션을 선택한 다음 기존 공유 대상을 선택하거나 새 대상을 만듭니다.

      또한 데이터가 Adobe Experience Cloud에서 올바르게 조정되도록 대상에 포함된 데이터의 리소스에 해당하는 **[!UICONTROL Shared Data source]** 항목을 선택합니다.

      이 옵션을 사용하면 공유 대상이 **[!UICONTROL Audiences]** 메뉴를 통해 사용할 수 있는 Adobe Campaign 대상 목록에 추가되지 않습니다.

      >[!NOTE]
      >
      >이 옵션은 관리자가 Adobe Experience Cloud의 공유 대상 기능을 구성한 경우에만 사용할 수 있습니다. 자세한 내용은 캠페인 및 [사용자 코어 서비스 작업을 참조하십시오](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md).
   업데이트 중에 저장되거나 사용할 수 있는 대상의 유형은 워크플로우의 업스트림에 배치된 활동에 따라 달라집니다.

   대상을 저장할 때 대상의 타깃팅 차원을 알 수 없는 경우(예: 가져온 파일의 경우) 대상이 **[!UICONTROL File]** 유형 대상으로 생성되거나 업데이트됩니다.

   저장된 대상의 타깃팅 차원이 저장될 때(예: 타깃팅에서 나온 경우 쿼리 후 등) 이미 정의된 경우, 대상이 **[!UICONTROL List]** 유형 대상으로 저장되거나 갱신됩니다.

   그런 다음 저장된 대상의 컨텐츠를 대상의 세부 사항 보기에서 사용할 수 있으며, **[!UICONTROL Audiences]** 메뉴에서 액세스할 수 있습니다. 이 보기에서 사용할 수 있는 열은 워크플로우의 대상 저장 활동의 인바운드 전환 열에 해당합니다. 예:가져온 파일의 열, 쿼리에서 추가된 추가 데이터.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예 {#example}

이 예제에서 정의된 워크플로우는 타깃팅에서 일반적인 대상 업데이트를 보여줍니다.

* 한 달에 한 번 자동으로 **[!UICONTROL Scheduler]**&#x200B;실행됩니다.
* 를 사용하여 사용 가능한 다른 응용 프로그램 서비스에 가입한 모든 프로필을 복구할 **[!UICONTROL Query]** 수 있습니다.
* 이 **[!UICONTROL Save audience]** 활동은 마지막 워크플로우 실행 이후 서비스에서 구독되지 않은 프로필을 삭제하고 새로 가입된 프로필을 추가하여 대상을 업데이트합니다.

![](assets/save_audience_example_1.png)

활동은 다음과 같이 구성됩니다. **[!UICONTROL Save audience]**

![](assets/save_audience_example_2.png)

