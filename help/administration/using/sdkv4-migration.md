---
title: Adobe Experience Platform SDK로 SDK v4 모바일 애플리케이션 마이그레이션
description: 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법을 알아봅니다
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: eb7a209e-069e-4068-966d-05344bd838c7
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 1%

---

# 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션하는 방법 {#sdkv4-migration}

>[!IMPORTANT]
>
> 마이그레이션 프로세스는 되돌릴 수 없습니다.
>
> SDK V4 모바일 애플리케이션에서 Adobe Experience Platform SDK로 마이그레이션을 시작하기 전에 해당 문서를 자세히 읽어보십시오.

## SDK V4 마이그레이션 기본 정보

Adobe Campaign Standard은 SDK V4를 Adobe Experience Platform SDK를 사용하는 애플리케이션과 별도의 애플리케이션으로 사용하여 모바일 애플리케이션을 처리합니다.
Adobe SDK 버전을 v4에서 Adobe Experience Platform으로 업그레이드한 후 모바일 애플리케이션은 기존 애플리케이션 가입자 데이터 및 캠페인을 계속 사용해야 합니다. 따라서 마이그레이션이 필요합니다.

>[!NOTE]
>
> 이 페이지에서는 SDK v4 모바일 애플리케이션을 새로 만든 Adobe Experience Platform SDK 애플리케이션으로의 마이그레이션에 대해 설명합니다. SDK v4 모바일 애플리케이션은 **[!UICONTROL Configured]** **[!UICONTROL Property status]**.

| 마이그레이션 후 변경되지 않는 사항 |
|:-:|
| 마이그레이션된 SDK V4 애플리케이션을 사용하는 기존 게재 및 캠페인에는 영향을 주지 않습니다. |
| 모바일 애플리케이션 이름은 동일하게 유지됩니다. |
| iOS 및 Android의 플랫폼 자격 증명은 유지됩니다. |
| 애플리케이션의 모든 구독자와 해당 데이터가 유지됩니다. |
| 기존 SDK v4 모바일 애플리케이션에서는 데이터(PII 데이터, 가입자 및 토큰 정보)를 Adobe Campaign Standard에 계속 전송합니다. |
| 다음 **[!UICONTROL Organizational unit]** 모바일 애플리케이션의 이름은 동일하게 유지됩니다. |

| 마이그레이션 후 변경 사항 |
|:-:|
| 모바일 애플리케이션은에서 사용할 수 있습니다. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**. 마이그레이션 전에에서 사용할 수 있었습니다. **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**. |
| 다음 **[!UICONTROL Collect PII Endpoint]** 응용 프로그램의 내용이 변경됩니다. 나이 든 **[!UICONTROL Collect PII Endpoint]** 은(는) 계속 작동하며, 전송된 데이터는 손실되지 않습니다. |
| 애플리케이션이 태그에 연결되어 있습니다 **[!UICONTROL Mobile Property]**. 새로 만든 모바일 애플리케이션으로 처리됩니다. |
| 마이그레이션에 사용된 원본 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다. |

## 모바일 애플리케이션을 SDK v4에서 Adobe Experience Platform SDK로 마이그레이션 {#how-to-migrate}

마이그레이션하기 전에 다음 권장 사항을 고려해야 합니다.

* 마이그레이션 프로세스는 되돌릴 수 없습니다.
* 여러 응용 프로그램의 마이그레이션을 동시에 실행해서는 안 됩니다. 또한 동일한 응용 프로그램의 마이그레이션이 동시에 여러 창에 의해 트리거되지 않도록 해야 합니다.
* 마이그레이션 전에 에 대한 **[!UICONTROL Organizational unit]** 마이그레이션할 모바일 애플리케이션 및 마이그레이션에 사용하는 Adobe Experience Platform 애플리케이션의 .
* 마이그레이션 후 애플리케이션이 Adobe Experience Platform SDK 애플리케이션이 됩니다. 변경 사항이 해당 태그에 연결됩니다 **[!UICONTROL Mobile Property]**.

1. 새 만들기 **[!UICONTROL Mobile property]** ( 데이터 수집 UI) 자세한 내용은 [설명서](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/).

1. Adobe Campaign Standard의 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Workflows]** 그리고 **[!UICONTROL syncWithLaunch]** 워크플로우. 워크플로우가 오류 없이 종료되었는지 확인합니다.

1. 워크플로우 완료 후 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]** 메뉴에서 모바일 애플리케이션을 Adobe Campaign Standard에서 사용할 수 있고 이 사이트에 있는지 확인합니다 **[!UICONTROL Ready to Configure]** state.

   ![](assets/aep_v4_2.png)

1. in **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (SDK V4)]**&#x200B;를 클릭하고 마이그레이션할 SDK V4 애플리케이션을 선택합니다.

1. **[!UICONTROL Mobile application migration to AEP SDK]** 탭을 선택합니다. 

   ![](assets/aep_v4_3.png)

1. 에서 **[!UICONTROL Select AEP SDK mobile application to merge current application with]** 드롭다운에서 이전에 만든 Adobe Experience Platform SDK 모바일 애플리케이션을 선택합니다.

1. **[!UICONTROL Migrate]**&#x200B;를 클릭합니다.

   ![](assets/aep_v4_4.png)

1. 에서 **[!UICONTROL Migration application]** 창 **[!UICONTROL Ok]**.

   ![](assets/aep_v4_5.png)

1. 완료 창이 나타나면 **[!UICONTROL Go to Adobe Experience Platform SDK Channel list]**.

1. Adobe Experience Platform SDK 채널 목록 페이지에서 이전 V4 모바일 애플리케이션이 **[!UICONTROL Ready To Configure]**.

1. 모바일 애플리케이션을 선택하고 을(를) 클릭합니다 **[!UICONTROL Save]** 마이그레이션을 완료합니다.

이 마이그레이션 후 모바일 애플리케이션의 V4 버전에서 수집된 구독자와 모바일 애플리케이션의 AEP 버전에서 수집한 새 구독자를 마이그레이션된 애플리케이션에서 사용할 수 있습니다.

서로 다른 두 유형의 구독자를 구분하기 위해 **[!UICONTROL Text]** 사용자 지정 리소스를 확장할 때 유형 **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** 로서의 `sdkversion` 또는 `appVersion` 예. 사용자 지정 리소스 확장 방법에 대한 자세한 내용은 다음을 참조하십시오 [페이지](../../developing/using/creating-or-extending-the-resource.md).
그런 다음 연결된 태그를 구성해야 합니다 **[!UICONTROL Mobile property]** collect PII 호출에서 이 사용자 지정 필드 값을 보내고 그에 따라 모바일 애플리케이션 구성을 변경합니다.

## FAQ {#faq}

### Q: SDK v4 모바일 애플리케이션에서 Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션 탭이 표시되지 않습니다. {#tab-not-visible}

A: 고급 메뉴에서 **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**&#x200B;를 채울 때 **[!UICONTROL Enable migration of mobile app from SDK v4 to Adobe Experience Platform SDK option]** 선택 사항입니다. 기본적으로 1로 설정하고 활성화해야 합니다. 관리자가 수동으로 비활성화했을 수 있습니다.

![](assets/aep_v4_1.png)

### Q: Adobe Experience Platform SDK로 모바일 애플리케이션 마이그레이션 탭에서 데이터 없음 메시지가 표시됩니다. {#no-data}

A: 해당 응용 프로그램만 **[!UICONTROL Organizational unit]** 가 목록에 표시됩니다. 마이그레이션에 올바른 Adobe Experience Platform 애플리케이션이 있는지 확인하십시오. 다음 **[!UICONTROL Property Status]** Adobe Experience Platform 애플리케이션의 **[!UICONTROL Ready to Configure]**  그리고 **[!UICONTROL Mobile app migration status]** 설정 **[!UICONTROL Not Migrated]**.

![](assets/aep_v4_6.png)

### Q: 구성된 속성 상태가 있는 Adobe Experience Platform SDK 애플리케이션을 마이그레이션에 사용할 수 없는 이유는 무엇입니까? {#property-status}

A: 마이그레이션 프로세스는 SDK v4 구독자와 속성을 유지합니다. Adobe Experience Platform SDK 애플리케이션의 태그 관련 정보만 유지합니다. 구독자와 Adobe Experience Platform SDK 애플리케이션의 기타 데이터가 손실됩니다. 데이터 손실을 방지하기 위해 **[!UICONTROL Ready to Configure]** **[!UICONTROL Property Status]** 은 마이그레이션에 대상이 됩니다.

### Q: 마이그레이션 후 이전 SDK v4 모바일 애플리케이션은 어디에서 찾을 수 있습니까? {#v4-app-not-visible}

A: 마이그레이션 후 모바일 애플리케이션이 고급 메뉴에서 표시됩니다 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile app (Adobe Experience Platform SDK)]**.

### Q: 마이그레이션 후 새로 만든 Adobe Experience Platform SDK 애플리케이션은 어디에서 찾을 수 있습니까? {#aep-not-visible}

A: 마이그레이션에 사용된 새로 만든 Adobe Experience Platform SDK 애플리케이션은 별도의 애플리케이션으로 존재하지 않습니다. 마이그레이션된 SDK v4 애플리케이션만 사용할 수 있습니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A(조직 단위 ALL의 하위)로 설정되어 있고 Adobe Experience Platform SDK가 모두 로 설정되어 있는 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#v4-org-unit}

A: 의 관리자 **[!UICONTROL Organizational unit]** 모든 관리자는 모바일 애플리케이션을 모두 관리할 수 있는 권한이 있으며 마이그레이션을 담당합니다.

### Q: SDK v4 모바일 애플리케이션 조직 단위가 A로 설정되어 있고 Adobe Experience Platform SDK 애플리케이션이 B(조직 단위 A의 동위)로 설정된 경우. 모바일 애플리케이션을 마이그레이션하려면 어떻게 해야 합니까? {#aep-org-unit}

A: Adobe Experience Platform SDK 애플리케이션이 동위 멤버의 자산임 **[!UICONTROL Organizational unit]**&#x200B;를 설정하는 경우 모바일 애플리케이션이 **[!UICONTROL Organizational unit]** A. 모바일 애플리케이션은 **[!UICONTROL Organizational unit]** 모두 그렇지만 이러한 관리자는 모바일 애플리케이션을 마이그레이션하지 않는 것이 좋습니다.
이 경우 모바일 애플리케이션을 동일한 위치로 이동해야 합니다 **[!UICONTROL Organizational unit]** 또는 **[!UICONTROL Organizational unit]** 상위 링크 사용.
자세한 내용은 **[!UICONTROL Organizational unit]**, 다음 문서를 참조하십시오. [섹션](../../administration/using/organizational-units.md).

### Q: Adobe Experience Platform SDK 모바일 애플리케이션(v4 모바일 애플리케이션에서 마이그레이션됨) 페이지의 푸시 채널 설정 드롭다운 아래에 Android 키 또는 iOS 인증서에 대해 업로드한 날짜/이름 등의 정보가 표시되지 않습니다 {#no-information-v5}

A: SDK V4 모바일 애플리케이션을 만들 때 시스템은 이 정보를 저장하지 않습니다. SDK V4 모바일 애플리케이션을 Adobe Experience Platform SDK 모바일 애플리케이션으로 마이그레이션할 때 마이그레이션된 모바일 애플리케이션에도 이러한 유형의 정보가 포함되어 있지 않습니다. 사용자가 새 iOS 인증서 또는 Android 키를 업로드하는 즉시 키 또는 인증서의 다른 세부 정보가 저장되고 아래에 올바르게 표시됩니다 **[!UICONTROL Push channel settings]** 드롭다운.
