---
title: Adobe Experience Platform SDK로 SDK v4 모바일 애플리케이션 마이그레이션
description: 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법에 대해 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: eb7a209e-069e-4068-966d-05344bd838c7
source-git-commit: 3b2f8d9b2b7a4ec9532917af3a0880400d98e636
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 1%

---

# 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법 {#sdkv4-migration}


Adobe Experience Platform Mobile 버전 4 SDK에 대한 지원은 종료되었습니다 **2021년 8월 31일**. 이 문서에서 Adobe Experience Platform SDK로 마이그레이션하는 방법을 알아봅니다.

>[!IMPORTANT]
>
> 마이그레이션 프로세스를 취소할 수 없습니다.
>
> SDK V4 모바일 애플리케이션을 Adobe Experience Platform SDK로 마이그레이션하기 전에 문서를 주의 깊게 읽어 보십시오.

## SDK V4 마이그레이션 기본 정보

Adobe Campaign Standard은 SDK V4를 사용하여 모바일 애플리케이션을 Adobe Experience Platform SDK를 사용하는 애플리케이션과 별도의 애플리케이션으로 처리합니다.
Adobe SDK 버전을 v4에서 Adobe Experience Platform으로 업그레이드한 후 모바일 애플리케이션은 기존 애플리케이션 구독자 데이터와 캠페인을 계속 사용해야 합니다. 따라서 마이그레이션이 필요합니다.

>[!NOTE]
>
> 이 페이지에서는 SDK v4 모바일 애플리케이션을 새로 생성된 Adobe Experience Platform SDK 애플리케이션으로의 마이그레이션에 대해 설명합니다. SDK v4 모바일 애플리케이션은 를 사용하여 Adobe Experience Platform SDK 모바일 애플리케이션과 병합되지 않습니다. **[!UICONTROL Configured]** **[!UICONTROL Property status]**.

| 마이그레이션 후 변경되지 않는 사항 |
|:-:|
| 마이그레이션된 SDK V4 애플리케이션을 사용하는 기존 게재 및 캠페인에는 영향을 주지 않습니다. |
| 모바일 애플리케이션 이름은 그대로 유지됩니다. |
| iOS 및 Android에 대한 플랫폼 자격 증명이 유지됩니다. |
| 애플리케이션의 모든 구독자와 데이터는 유지됩니다. |
| 기존 SDK v4 모바일 애플리케이션은 데이터(PII 데이터, 구독자 및 토큰 정보)를 Adobe Campaign Standard에 계속 전송합니다. |
| 다음 **[!UICONTROL Organizational unit]** 의 모바일 애플리케이션은 그대로 유지됩니다. |

| 마이그레이션 후 변경 사항 |
|:-:|
| 모바일 애플리케이션은에서 사용할 수 있습니다. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**. 마이그레이션 전에는에서 사용할 수 있었습니다. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**. |
| 다음 **[!UICONTROL Collect PII Endpoint]** 의 애플리케이션이 변경됩니다. 더 이전 **[!UICONTROL Collect PII Endpoint]** 은(는) 계속 작동하며 전송된 데이터는 손실되지 않습니다. |
| 애플리케이션이 태그에 연결됩니다. **[!UICONTROL Mobile Property]**. 새롭게 생성된 모바일 애플리케이션으로 처리됩니다. |
| 마이그레이션에 사용된 원래 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다. |

## 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션 {#how-to-migrate}

마이그레이션하기 전에 다음 권장 사항을 고려해야 합니다.

* 마이그레이션 프로세스를 취소할 수 없습니다.
* 여러 애플리케이션의 마이그레이션을 동시에 실행하면 안 됩니다. 또한 동일한 애플리케이션의 마이그레이션이 여러 창에서 동시에 트리거되지 않도록 해야 합니다.
* 마이그레이션 전에 사용자에게 이(가) 할당되었는지 확인 **[!UICONTROL Organizational unit]** / 마이그레이션하려는 모바일 애플리케이션과 마이그레이션에 사용하는 Adobe Experience Platform 애플리케이션.
* 마이그레이션 후 애플리케이션은 Adobe Experience Platform SDK 애플리케이션이 됩니다. 해당 변경 사항이 해당 태그에 연결됩니다. **[!UICONTROL Mobile Property]**.

1. 새로 만들기 **[!UICONTROL Mobile property]** (데이터 수집 UI) 자세한 내용은 [설명서](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/).

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]** 및 열기 **[!UICONTROL syncWithLaunch]** 워크플로입니다. 워크플로우가 오류 없이 종료되었는지 확인합니다.

1. 워크플로우 완료 후 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]** 메뉴에서 모바일 애플리케이션을 Adobe Campaign Standard에서 사용할 수 있고에 있는지 확인합니다. **[!UICONTROL Ready to Configure]** 주.

   ![](assets/aep_v4_2.png)

1. 위치 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**&#x200B;마이그레이션하려는 SDK V4 애플리케이션을 선택합니다.

1. **[!UICONTROL Mobile application migration to AEP SDK]** 탭을 선택합니다. 

   ![](assets/aep_v4_3.png)

1. 다음에서 **[!UICONTROL Select AEP SDK mobile application to merge current application with]** 드롭다운에서 이전에 만든 Adobe Experience Platform SDK 모바일 애플리케이션을 선택합니다.

1. **[!UICONTROL Migrate]**&#x200B;를 클릭합니다.

   ![](assets/aep_v4_4.png)

1. 다음에서 **[!UICONTROL Migration application]** 창에서 다음을 클릭: **[!UICONTROL Ok]**.

   ![](assets/aep_v4_5.png)

1. 완료 성공 창이 나타나면 **[!UICONTROL Go to Adobe Experience Platform SDK Channel list]**.

1. Adobe Experience Platform SDK 채널 목록 페이지에서 이전 V4 모바일 애플리케이션이 로 설정되어 있는지 확인합니다. **[!UICONTROL Ready To Configure]**.

1. 모바일 애플리케이션을 선택하고 **[!UICONTROL Save]** 마이그레이션을 완료합니다.

이 마이그레이션 후 모바일 애플리케이션의 V4 버전에서 수집한 구독자와 모바일 애플리케이션의 AEP 버전에서 수집한 새 구독자를 마이그레이션된 애플리케이션에서 사용할 수 있습니다.

두 가지 다른 유형의 구독자를 구분하기 위해 의 새 사용자 지정 필드를 추가할 수 있습니다. **[!UICONTROL Text]** 사용자 지정 리소스를 확장할 때 입력 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 다음으로: `sdkversion` 또는 `appVersion` 예. 사용자 지정 리소스를 확장하는 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../developing/using/creating-or-extending-the-resource.md).
그런 다음 연결된 태그를 구성해야 합니다 **[!UICONTROL Mobile property]** 를 사용하여 Collect PII 호출에서 이 사용자 지정 필드 값을 보내고 모바일 애플리케이션 구성을 적절하게 변경합니다.

## FAQ {#faq}

### Q: SDK v4 모바일 애플리케이션에서 Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션을 볼 수 없습니다. {#tab-not-visible}

A: 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**&#x200B;의 값을 확인합니다. **[!UICONTROL Enable migration of mobile app from SDK v4 to Adobe Experience Platform SDK option]** 옵션을 선택합니다. 1로 설정하고 기본적으로 활성화되어 있어야 합니다. 관리자가 수동으로 비활성화했을 수 있습니다.

![](assets/aep_v4_1.png)

### Q: Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션 탭에서 데이터 없음 메시지가 표시됩니다. {#no-data}

A: 귀하의 적격한 애플리케이션만 **[!UICONTROL Organizational unit]** 목록에 이 표시됩니다. 마이그레이션을 위한 올바른 Adobe Experience Platform 애플리케이션이 있는지 확인하십시오. 다음 **[!UICONTROL Property Status]** Adobe Experience Platform 애플리케이션의 를 **[!UICONTROL Ready to Configure]**  및 **[!UICONTROL Mobile app migration status]** 을 로 설정 **[!UICONTROL Not Migrated]**.

![](assets/aep_v4_6.png)

### Q: 구성된 속성 상태의 Adobe Experience Platform SDK 애플리케이션을 마이그레이션에 사용할 수 없는 이유는 무엇입니까? {#property-status}

A: 마이그레이션 프로세스는 SDK v4 구독자 및 속성을 유지합니다. Adobe Experience Platform SDK 애플리케이션의 태그 관련 정보만 유지됩니다. Adobe Experience Platform SDK 애플리케이션의 구독자 및 기타 데이터가 손실됩니다. 데이터 손실을 방지하려면 가 있는 Adobe Experience Platform SDK 애플리케이션만 **[!UICONTROL Ready to Configure]** **[!UICONTROL Property Status]** 은(는) 마이그레이션할 수 있습니다.

### Q: 마이그레이션 후 이전 SDK v4 모바일 애플리케이션은 어디에서 찾을 수 있습니까? {#v4-app-not-visible}

A: 마이그레이션 후 모바일 애플리케이션이 고급 메뉴에 표시됩니다 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**.

### Q: 마이그레이션 후 새로 만든 Adobe Experience Platform SDK 애플리케이션은 어디에서 찾을 수 있습니까? {#aep-not-visible}

A: 마이그레이션에 사용되는 새로 만든 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A(조직 단위 ALL의 하위)로 설정되어 있고 Adobe Experience Platform SDK가 ALL로 설정된 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#v4-org-unit}

A: 의 관리자 **[!UICONTROL Organizational unit]** 모두 모바일 애플리케이션을 모두 관리할 수 있는 권한을 가지며 마이그레이션을 담당합니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A로 설정되고 Adobe Experience Platform SDK 애플리케이션이 B(조직 단위 A의 형제)로 설정된 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#aep-org-unit}

A: 형제자매의 자산인 Adobe Experience Platform SDK 애플리케이션 **[!UICONTROL Organizational unit]**, 모바일 애플리케이션은 의 사용자에게 표시되지 않습니다. **[!UICONTROL Organizational unit]** A. 모바일 애플리케이션은 의 관리자가 사용할 수 있습니다. **[!UICONTROL Organizational unit]** 모두. 그러나 이러한 관리자에게 모바일 애플리케이션을 마이그레이션하지 않는 것이 좋습니다.
이 경우 모바일 애플리케이션을 동일한 위치로 이동해야 합니다 **[!UICONTROL Organizational unit]** 또는 **[!UICONTROL Organizational unit]** (상위 링크 포함)
에 대한 자세한 내용 **[!UICONTROL Organizational unit]**, 이를 참조하십시오. [섹션](../../administration/using/organizational-units.md).

### Q: Adobe Experience Platform SDK 모바일 애플리케이션(v4 모바일 애플리케이션에서 마이그레이션됨) 페이지의 푸시 채널 설정 드롭다운 아래에 업로드된 날짜/이름과 같은 정보가 Android 키 또는 iOS 인증서에 대해 표시되지 않습니다 {#no-information-v5}

A: SDK V4 모바일 애플리케이션을 만들 때 시스템이 이 정보를 저장하지 않습니다. SDK V4 모바일 애플리케이션을 Adobe Experience Platform SDK 모바일 애플리케이션으로 마이그레이션할 때 마이그레이션된 모바일 애플리케이션에는 이러한 종류의 정보도 표시되지 않습니다. 사용자가 새 iOS 인증서 또는 Android 키를 업로드하는 즉시, 키 또는 인증서의 다른 세부 정보가 아래에 저장되고 올바르게 표시됩니다. **[!UICONTROL Push channel settings]** 드롭다운.
