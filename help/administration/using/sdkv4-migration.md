---
title: Adobe Experience Platform SDK로 SDK v4 모바일 애플리케이션 마이그레이션
description: 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법에 대해 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: eb7a209e-069e-4068-966d-05344bd838c7
source-git-commit: 620ae1adc6f804e90c10daeb5fa4df42ce106885
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 1%

---

# 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법 {#sdkv4-migration}


Adobe Experience Platform Mobile 버전 4 SDK에 대한 지원이 2021년 8월 31일부로 종료되었습니다. 이 레거시 버전의 SDK를 사용 중인 경우 2024년 6월 말 **전에 Adobe Experience Platform SDK를 사용하여 구현을**&#x200B;업데이트해야 합니다. 이 문서에서 Adobe Experience Platform SDK로 마이그레이션하는 방법을 알아봅니다.

>[!IMPORTANT]
>
> SDK V4 모바일 애플리케이션을 Adobe Experience Platform SDK로 마이그레이션하기 전에 문서를 주의 깊게 읽어 보십시오.

## SDK V4 마이그레이션 기본 정보

Adobe Campaign Standard은 SDK V4를 사용하여 모바일 애플리케이션을 Adobe Experience Platform SDK를 사용하는 애플리케이션과 별도의 애플리케이션으로 처리합니다.

Adobe SDK 버전을 v4에서 Adobe Experience Platform으로 업그레이드한 후 모바일 애플리케이션은 기존 애플리케이션 구독자 데이터와 캠페인을 계속 사용해야 합니다. 따라서 마이그레이션이 필요합니다.

>[!NOTE]
>
> 이 페이지에서는 SDK v4 모바일 애플리케이션을 새로 생성된 Adobe Experience Platform SDK 애플리케이션으로의 마이그레이션에 대해 설명합니다. SDK v4 모바일 애플리케이션은 **[!UICONTROL Configured]** **[!UICONTROL Property status]**&#x200B;을(를) 사용하는 Adobe Experience Platform SDK 모바일 애플리케이션과 병합되지 않습니다.

| 마이그레이션 후 변경되지 않는 사항 |
|:-:|
| 마이그레이션된 SDK V4 애플리케이션을 사용하는 기존 게재 및 캠페인에는 영향을 주지 않습니다. |
| 모바일 애플리케이션 이름은 그대로 유지됩니다. |
| iOS 및 Android에 대한 플랫폼 자격 증명은 유지됩니다. |
| 애플리케이션의 모든 구독자와 데이터는 유지됩니다. |
| 기존 SDK v4 모바일 애플리케이션은 데이터(PII 데이터, 구독자 및 토큰 정보)를 Adobe Campaign Standard에 계속 전송합니다. |
| 모바일 응용 프로그램의 **[!UICONTROL Organizational unit]**&#x200B;은(는) 동일하게 유지됩니다. |

| 마이그레이션 후 변경 사항 |
|:-:|
| 모바일 애플리케이션은 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**&#x200B;에서 사용할 수 있습니다. 마이그레이션 전에 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**&#x200B;에서 사용할 수 있습니다. |
| 응용 프로그램의 **[!UICONTROL Collect PII Endpoint]**&#x200B;이(가) 변경됩니다. 이전 **[!UICONTROL Collect PII Endpoint]**&#x200B;은(는) 계속 작동하므로 보낸 데이터는 손실되지 않습니다. |
| 응용 프로그램이 태그 **[!UICONTROL Mobile Property]**&#x200B;에 연결됩니다. 새롭게 생성된 모바일 애플리케이션으로 처리됩니다. |
| 마이그레이션에 사용된 원래 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다. |

## 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션 {#how-to-migrate}

마이그레이션하기 전에 다음 권장 사항을 고려해야 합니다.

* 마이그레이션 프로세스를 취소할 수 없습니다.
* 여러 애플리케이션의 마이그레이션을 동시에 실행하면 안 됩니다. 또한 동일한 애플리케이션의 마이그레이션이 여러 창에서 동시에 트리거되지 않도록 해야 합니다.
* 마이그레이션하기 전에 마이그레이션하려는 모바일 응용 프로그램과 마이그레이션에 사용 중인 Adobe Experience Platform 응용 프로그램의 **[!UICONTROL Organizational unit]**&#x200B;이(가) 할당되었는지 확인하십시오.
* 마이그레이션 후 애플리케이션은 Adobe Experience Platform SDK 애플리케이션이 됩니다. 변경 내용이 해당 태그 **[!UICONTROL Mobile Property]**&#x200B;에 연결됩니다.

1. 데이터 수집 UI에 새 **[!UICONTROL Mobile property]**&#x200B;을(를) 만듭니다. 자세한 내용은 [설명서](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/)를 참조하세요.

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]**&#x200B;을(를) 선택하고 **[!UICONTROL syncWithLaunch]** 워크플로우를 엽니다. 워크플로우가 오류 없이 종료되었는지 확인합니다.

1. 워크플로우 완료 후 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]** 메뉴에서 모바일 애플리케이션을 Adobe Campaign Standard에서 사용할 수 있고 상태가 **[!UICONTROL Ready to Configure]**&#x200B;인지 확인하십시오.

   ![](assets/aep_v4_2.png)

1. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**&#x200B;에서 마이그레이션할 SDK V4 응용 프로그램을 선택하십시오.

1. **[!UICONTROL Mobile application migration to AEP SDK]** 탭을 선택합니다. 

   ![](assets/aep_v4_3.png)

1. **[!UICONTROL Select AEP SDK mobile application to merge current application with]** 드롭다운에서 이전에 만든 Adobe Experience Platform SDK 모바일 애플리케이션을 선택합니다.

1. **[!UICONTROL Migrate]**&#x200B;를 클릭합니다.

   ![](assets/aep_v4_4.png)

1. **[!UICONTROL Migration application]** 창에서 **[!UICONTROL Ok]**&#x200B;을(를) 클릭합니다.

   ![](assets/aep_v4_5.png)

1. 완료 완료 창이 나타나면 **[!UICONTROL Go to Adobe Experience Platform SDK Channel list]**&#x200B;을(를) 클릭합니다.

1. Adobe Experience Platform SDK 채널 목록 페이지에서 이전 V4 모바일 애플리케이션이 **[!UICONTROL Ready To Configure]**(으)로 설정되어 있는지 확인하십시오.

1. 모바일 애플리케이션을 선택하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭하여 마이그레이션을 완료합니다.

이 마이그레이션 후 모바일 애플리케이션의 V4 버전에서 수집한 구독자와 모바일 애플리케이션의 AEP 버전에서 수집한 새 구독자를 마이그레이션된 애플리케이션에서 사용할 수 있습니다.

구독자의 두 가지 다른 형식을 구별하기 위해 사용자 지정 리소스 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**&#x200B;을(를) `sdkversion` 또는 `appVersion`(으)로 확장할 때 **[!UICONTROL Text]** 형식의 새 사용자 지정 필드를 추가할 수 있습니다. 사용자 지정 리소스를 확장하는 방법에 대한 자세한 내용은 이 [페이지](../../developing/using/creating-or-extending-the-resource.md)를 참조하십시오.
그런 다음 Collect PII 호출에서 이 사용자 지정 필드 값을 보내도록 연결된 태그 **[!UICONTROL Mobile property]**&#x200B;을(를) 구성하고 그에 따라 모바일 애플리케이션 구성을 변경해야 합니다.

## FAQ {#faq}

### Q: SDK v4 모바일 애플리케이션에서 Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션을 볼 수 없습니다. {#tab-not-visible}

A: 고급 메뉴 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**&#x200B;에서 **[!UICONTROL Enable migration of mobile app from SDK v4 to Adobe Experience Platform SDK option]** 옵션의 값을 확인하십시오. 1로 설정하고 기본적으로 활성화되어 있어야 합니다. 관리자가 수동으로 비활성화했을 수 있습니다.

![](assets/aep_v4_1.png)

### Q: Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션 탭에서 데이터 없음 메시지가 표시됩니다. {#no-data}

A: **[!UICONTROL Organizational unit]**&#x200B;의 적격한 응용 프로그램만 목록에 표시됩니다. 마이그레이션을 위한 올바른 Adobe Experience Platform 애플리케이션이 있는지 확인하십시오. Adobe Experience Platform 응용 프로그램의 **[!UICONTROL Property Status]**&#x200B;을(를) **[!UICONTROL Ready to Configure]**(으)로 설정하고 **[!UICONTROL Mobile app migration status]**&#x200B;을(를) **[!UICONTROL Not Migrated]**(으)로 설정해야 합니다.

![](assets/aep_v4_6.png)

### Q: 구성된 속성 상태의 Adobe Experience Platform SDK 애플리케이션을 마이그레이션에 사용할 수 없는 이유는 무엇입니까? {#property-status}

A: 마이그레이션 프로세스는 SDK v4 구독자 및 속성을 유지합니다. Adobe Experience Platform SDK 애플리케이션의 태그 관련 정보만 유지됩니다. Adobe Experience Platform SDK 애플리케이션의 구독자 및 기타 데이터가 손실됩니다. 데이터 손실을 방지하려면 **[!UICONTROL Ready to Configure]** **[!UICONTROL Property Status]**&#x200B;이(가) 있는 Adobe Experience Platform SDK 응용 프로그램만 마이그레이션할 수 있습니다.

### Q: 마이그레이션 후 이전 SDK v4 모바일 애플리케이션은 어디에서 찾을 수 있습니까? {#v4-app-not-visible}

A: 마이그레이션 후 모바일 애플리케이션이 고급 메뉴 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**&#x200B;에 표시됩니다.

### Q: 마이그레이션 후 새로 만든 Adobe Experience Platform SDK 애플리케이션은 어디에서 찾을 수 있습니까? {#aep-not-visible}

A: 마이그레이션에 사용되는 새로 만든 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A(조직 단위 ALL의 하위)로 설정되어 있고 Adobe Experience Platform SDK가 ALL로 설정된 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#v4-org-unit}

A: **[!UICONTROL Organizational unit]** ALL의 관리자는 두 모바일 애플리케이션을 모두 관리할 수 있는 권한을 가지며 마이그레이션을 담당하게 됩니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A로 설정되고 Adobe Experience Platform SDK 애플리케이션이 B(조직 단위 A의 형제)로 설정된 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#aep-org-unit}

A: Adobe Experience Platform SDK 응용 프로그램은 형제 **[!UICONTROL Organizational unit]**&#x200B;의 자산이며 **[!UICONTROL Organizational unit]** A의 사용자에게 모바일 응용 프로그램이 표시되지 않습니다. 모바일 응용 프로그램은 **[!UICONTROL Organizational unit]** ALL의 관리자가 사용할 수 있지만 이 관리자에게 모바일 응용 프로그램을 마이그레이션하지 않는 것이 좋습니다.
이 경우 모바일 응용 프로그램을 동일한 **[!UICONTROL Organizational unit]** 또는 상위 링크가 있는 **[!UICONTROL Organizational unit]**&#x200B;에서 이동해야 합니다.
**[!UICONTROL Organizational unit]**&#x200B;에 대한 자세한 내용은 이 [섹션](../../administration/using/organizational-units.md)을 참조하세요.

### Q: Adobe Experience Platform SDK 모바일 애플리케이션(v4 모바일 애플리케이션에서 마이그레이션됨) 페이지의 푸시 채널 설정 드롭다운 아래에 업로드된 날짜/이름과 같은 정보가 Android 키 또는 iOS 인증서에 대해 표시되지 않습니다 {#no-information-v5}

A: SDK V4 모바일 애플리케이션을 만들 때 시스템이 이 정보를 저장하지 않습니다. SDK V4 모바일 애플리케이션을 Adobe Experience Platform SDK 모바일 애플리케이션으로 마이그레이션할 때 마이그레이션된 모바일 애플리케이션에는 이러한 종류의 정보도 표시되지 않습니다. 사용자가 새 iOS 인증서 또는 Android 키를 업로드하는 즉시 키 또는 인증서의 다른 세부 정보가 저장되고 **[!UICONTROL Push channel settings]** 드롭다운 아래에 올바르게 표시됩니다.
