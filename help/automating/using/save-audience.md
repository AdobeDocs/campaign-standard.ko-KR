---
title: 대상자 저장
description: 대상자 저장 활동을 통해 워크플로우에서 업스트림으로 계산한 모집단에서 기존 대상자를 업데이트하거나 새 대상자를 만들 수 있습니다.
page-status-flag: never-activated
uuid: 8babb173-fa59-44a7-a2a5-49f45ba6bf99
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 1f6bb048-7abd-499b-a4b0-187f9492dc47
context-tags: saveAudience,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 100%

---


# 대상자 저장{#save-audience}

## 설명 {#description}

![](assets/save_audience.png)

**[!UICONTROL Save audience]** 활동을 통해 워크플로우에서 업스트림으로 계산한 모집단에서 기존 대상자를 업데이트하거나 새 대상자를 만들 수 있습니다. 이 활동에서 만들거나 업데이트하는 대상자는 **목록** 또는 **파일** 대상자입니다. 이들은 애플리케이션 대상자 목록에 추가되고, **[!UICONTROL Audiences]** 메뉴를 통해 사용할 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Save audience]** 활동을 통해 만든 대상자가 추가 데이터로 보강된 경우, 이 데이터를 사용하여 독립 실행형 게재를 개인화할 수는 없습니다. 이 데이터는 워크플로우에서 실행되는 게재에서만 사용할 수 있습니다.

또한 이 활동을 통해 프로필을 Adobe Experience Cloud 대상자/세그먼트로 내보낼 수 있습니다. 내보내고 나면 다른 Adobe Experience Cloud 솔루션에서 이 대상자를 활용할 수 있습니다. 공유 대상자에 대한 자세한 내용은 [Campaign 및 People 핵심 서비스로 작업](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)을 참조하십시오.

## 사용의 컨텍스트 {#context-of-use}

**[!UICONTROL Save audience]** 활동은 기본적으로 모집단 그룹을 재사용 가능한 대상자로 전환하여 같은 워크플로우에서 계산되도록 하는 데 사용됩니다.

## 구성 {#configuration}

1. **[!UICONTROL Save audience]** 활동을 워크플로우에 드롭합니다.
1. 쿼리, 교집합, 결합 또는 제외 등 다른 타겟팅 활동 뒤에 연결합니다.
1. 활동을 선택한 다음 나타나는 빠른 작업에서 ![](assets/edit_darkgrey-24px.png) 버튼을 사용하여 활동을 엽니다.
1. 수행할 작업을 선택합니다.

   * **[!UICONTROL Update an existing audience]**: 기존 대상자를 선택하고 업데이트 유형을 선택합니다.

      * **[!UICONTROL Replace audience content with new data]**: 전체 대상자의 콘텐츠가 바뀝니다. 이전 데이터는 손실됩니다. 대상자 저장 활동의 인바운드 전환에서 수집한 데이터만 유지됩니다.
      * **[!UICONTROL Complete audience with new data]**: 이전 대상자 데이터가 유지되고 대상자 저장 활동의 인바운드 전환에서 수집한 데이터가 여기에 추가됩니다.
   * **[!UICONTROL Create then update an audience]**: 대상자의 이름을 입력하고 업데이트 유형을 선택합니다. 대상자가 아직 존재하지 않는 경우 새로 만들어집니다. 이미 존재하는 경우 선택한 모드에 따라 업데이트됩니다.

      * **[!UICONTROL Replace audience content with new data]**: 전체 대상자의 콘텐츠가 바뀝니다. 이전 데이터는 손실됩니다. 대상자 저장 활동의 인바운드 전환에서 수집한 데이터만 유지됩니다.

         경고: 이 옵션은 업데이트한 대상자의 대상자 유형과 타겟팅 차원을 지웁니다.

      * **[!UICONTROL Complete audience with new data]**: 이전 대상자 데이터가 유지되고 대상자 저장 활동의 인바운드 전환에서 수집한 데이터가 여기에 추가됩니다.

         경고: 업데이트한 대상자의 대상자 유형 또는 타겟팅 차원이 워크플로우의 현재 구성과 호환되지 않는 경우, 이 옵션을 사용하면 오류가 발생합니다. 예를 들어 쿼리에서 얻은 프로필로 파일 유형 대상자를 완성할 수는 없습니다.
   * **[!UICONTROL Create a new audience]**: 만들 대상자의 이름을 입력합니다. 대상자를 만든 시간과 날짜가 대상자 이름에 자동으로 추가됩니다. 이를 통해 워크플로우를 실행할 때마다 대상자가 고유해집니다.
   * **[!UICONTROL Share in Adobe Experience Cloud]**: 타겟팅한 프로필이 있고 대상자를 Adobe Experience Cloud로 내보내고 싶은 경우, 이 옵션을 선택한 뒤 기존 공유 대상자를 선택하거나 새 대상자를 만듭니다.

      또한 대상자에 포함된 데이터의 리소스에 해당하는 **[!UICONTROL Shared Data source]**&#x200B;을(를) 선택하여 데이터가 Adobe Experience Cloud에서 올바르게 조정되도록 합니다.

      이 옵션을 사용하면 공유 대상자가 **[!UICONTROL Audiences]** 메뉴의 Adobe Campaign 대상자 목록에 추가되지 않습니다.

      >[!NOTE]
      >
      >이 옵션은 관리자가 Adobe Experience Cloud 공유 대상자 기능을 구성한 경우에만 사용할 수 있습니다. 자세한 내용은 [Campaign 및 People 핵심 서비스로 작업](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)을 참조하십시오.

   업데이트 시 저장되거나 사용 가능한 대상자 유형은 워크플로우의 업스트림 활동에 따라 다릅니다.

   대상자를 저장할 때 대상자의 타겟팅 차원을 알 수 없는 경우(가져온 파일에서 수집한 경우 등), 해당 대상자는 **[!UICONTROL File]** 유형 대상자로 만들어지거나 업데이트됩니다.

   대상자를 저장할 때 저장된 대상자의 타겟팅 차원이 이미 정의되어 있는 경우(타겟팅에서나 쿼리 이후 수집한 경우 등), 해당 대상자는 **[!UICONTROL List]** 유형 대상자로 저장되거나 업데이트됩니다.

   **[!UICONTROL Audiences]** 메뉴를 통해 액세스할 수 있는 대상자 세부 사항 보기에서 저장한 대상자의 콘텐츠를 확인할 수 있습니다. 이 보기에서 사용할 수 있는 열은 워크플로우의 대상자 저장 활동의 인바운드 전환 열에 해당합니다. 가져온 파일의 열, 쿼리에서 추가한 데이터를 예로 들 수 있습니다.

1. 활동 구성을 확인하고 워크플로우를 저장합니다.

## 예제 {#example}

이 예제에서 정의한 워크플로우는 타겟팅을 통한 정기적 대상자 업데이트를 보여줍니다.

* 이 워크플로우는 **[!UICONTROL Scheduler]**&#x200B;을(를) 사용하여 한 달에 한 번 자동으로 실행됩니다.
* **[!UICONTROL Query]**&#x200B;을(를) 사용하여 사용 가능한 여러 애플리케이션 서비스를 구독하는 모든 프로필을 복구할 수 있습니다.
* **[!UICONTROL Save audience]** 활동은 마지막 워크플로우 실행 이후 서비스 구독을 취소한 프로필을 삭제하고 새로 구독한 프로필을 추가하여 대상자를 업데이트합니다.

![](assets/save_audience_example_1.png)

**[!UICONTROL Save audience]** 활동은 다음과 같이 구성됩니다.

![](assets/save_audience_example_2.png)

