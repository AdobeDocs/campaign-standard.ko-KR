---
title: 데이터베이스 구조 업데이트
description: Adobe Campaign 데이터베이스를 업데이트하는 방법을 알아봅니다.
page-status-flag: 활성화 안 함
uuid: 6c802f4f-d298-4ca4-acdb-09f2ad3865b9
contentOwner: 자우비
products: SG_CAMPAIGN/STANDARD
audience: 개발
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 2448b126-66b8-4608-aa6c-8028fb1902a4
context-tags: deploy,main;eventCusResource,개요
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# 데이터베이스 구조 업데이트{#updating-the-database-structure}

데이터 모델을 효과적으로 수정하고 이를 사용할 수 있으려면 데이터베이스 구조를 업데이트해야 합니다.

>[!NOTE]
>
>사용자 정의 리소스는 Adobe에서 수행한 자동 업데이트 중에 자동으로 새로 고쳐집니다.

## 사용자 지정 리소스 게시 {#publishing-a-custom-resource}

리소스에 대해 수행된 변경 사항을 적용하려면 데이터베이스 업데이트를 수행해야 합니다.

>[!NOTE]
>
>이벤트에 사용된 사용자 지정 리소스의 필드를 수정하거나 삭제하면 해당 이벤트의 게시를 자동으로 취소됩니다. See [Configuring Transactional messaging](../../administration/using/configuring-transactional-messaging.md).

1. 고급 메뉴에서 Adobe Campaign 로고를 통해 **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**&#x200B;을 선택한 다음 **[!UICONTROL Publishing]**&#x200B;선택합니다.
1. 기본적으로 이 옵션이 선택되어 **[!UICONTROL Determine modifications since the last publication]** 있으므로 마지막 업데이트 이후 수행된 변경 사항만 적용됩니다.

   >[!NOTE]
   >
   >게시가 완료되기 전에 실패한 경우 올바른 구성을 **[!UICONTROL Repair database structure]** 재설정합니다. 사용자 지정 리소스를 사용하지 않고 데이터베이스에서 직접 수행한 수정 사항은 모두 삭제됩니다.

   ![](assets/schema_extension_12.png)

1. 분석을 시작하려면 **[!UICONTROL Prepare publication]** 단추를 클릭합니다. 워크플로우에서 인스턴스가 집중적으로 사용되지 않을 경우 큰 테이블 업데이트를 수행해야 합니다.

   프로필 및 서비스 API에서 수행하는 작업에 대한 자세한 내용은 API [확장명을](#publishing-a-resource-with-api-extension)사용하여 리소스 게시를 참조하십시오.

   ![](assets/schema_extension_13.png)

1. 발행물이 실행되면 단추를 클릭하여 새 구성을 적용합니다. **[!UICONTROL Publish]**
1. 게시되면 각 리소스의 **[!UICONTROL Summary]** 창이 현재 상태를 나타내고 마지막 게시 날짜를 **[!UICONTROL Published]** 지정합니다.

   >[!NOTE]
   >
   >리소스를 새로 변경하는 경우 적용할 변경 사항에 대해 이 작업을 반복해야 합니다.

   게시하기 전에 리소스의 **[!UICONTROL Pending re-draft]** 상태가 있으면 게시하면 확정적인 변경 사항(열, 표 삭제...)이 발생하므로 작업을 확인하라는 추가 메시지가 표시됩니다. 이 마지막 변경 사항을 수행하는 데 도움이 되도록 탭을 사용할 수 **[!UICONTROL SQL Script]** 있습니다. 게시 중에 실행될 SQL 명령을 제공합니다.

   ![](assets/schema_extension_scriptsql.png)

   >[!NOTE]
   >
   >단추를 클릭하여 다시 초안 작성 프로세스를 중지할 수 **[!UICONTROL Cancel re-draft]** 있습니다. 이 작업은 리소스의 상태를 원래 상태로 되돌립니다.

1. 발행물이 실패하면 언제든지 을 클릭하여 이전 발행물로 돌아갈 수 **[!UICONTROL Back to latest successful publication]**&#x200B;있습니다.

   게시 실패 상태로 두면 인스턴스에 로그인하는 즉시 팝업 창이 열려 이 발행물을 수정하도록 알립니다. 발행물이 수정될 때까지 인스턴스가 새 제품 버전으로 업그레이드되지 않습니다.

   ![](assets/schema_extension_31.png)

## API 확장을 사용하여 리소스 게시 {#publishing-a-resource-with-api-extension}

다음 경우에 프로필 및 서비스 API를 만들 수 있습니다.

* 사용자 지정 리소스를 확장하거나 **[!UICONTROL Profiles]** 사용자 지정 리소스 **[!UICONTROL Services]**&#x200B;확장에서 선언된 필드를 통합하기 위해 프로필 및 서비스 API의 업데이트를 수행할 수 있습니다.
* 사용자 지정 리소스를 정의하고 리소스 **[!UICONTROL Profiles]** 또는 사용자 지정 리소스와 **[!UICONTROL Services]** 사용자 지정 리소스 간의 링크를 만들 때 API에 새 리소스를 포함하도록 업데이트를 수행할 수 있습니다.

발행물 화면에서 이 옵션을 선택할 수 있습니다.

* API가 아직 게시되지 않은 경우(리소스를 확장한 적이 없거나 이 리소스 또는 다른 리소스에 대해 이 옵션을 아직 확인하지 않은 경우) API를 만들지 여부를 선택할 수 있습니다.

   ![](assets/create-profile-and-services-api.png)

* API가 이미 게시되어 있는 경우(리소스를 이미 연장하고 이 옵션을 한 번 선택한 경우) API 업데이트가 강제 수행됩니다.

   실제로 API가 만들어지면 다시 게시할 때마다 API가 자동으로 업데이트됩니다. 이 API의 프로필 또는 서비스 리소스를 끊지 않고 인스턴스를 손상시키지 않기 위한 것입니다.

기본적으로 사용자 지정 리소스는 통합되지만, 특정 동작의 경우 이 리소스를 게시하지 않으려는 경우 에서 **[!UICONTROL Hide this resource from APIs]** 사용할 수 있는 옵션을 선택할 수 있습니다 **[!UICONTROL Resource Properties]**.

![](assets/removefromextoption.png)

단계 **[!UICONTROL Prepare Publication]** 후 Adobe Campaign은 탭의 게시 후 현재 버전의 API와 향후 버전 간의 삼각주를 표시합니다 **[!UICONTROL Profiles & Services API Preview]**. API를 처음 확장하는 경우 델타는 기본 사용자 지정 리소스 정의를 확장자와 비교합니다.

탭에 표시되는 정보는 다음 세 섹션으로 나누어집니다.추가, 삭제 및 수정된 요소

![](assets/extendpandsapi_diff.png)

델타의 분석은 게시 단계에서 API 동작을 수정할 수 있으므로 필수 단계이며 이러한 추이 변화에 영향을 줄 수 있습니다.

>[!NOTE]
>
>이 게시는 API를 **[!UICONTROL profilesAndServicesExt]** 업데이트합니다. API는 **[!UICONTROL profilesAndServices]** 업데이트되지 않습니다.

Adobe Campaign API에 대한 자세한 내용은 Adobe IO에 대한 전용 Adobe Campaign 설명서를 [참조하십시오](https://docs.campaign.adobe.com/doc/standard/en/adobeio.html).
