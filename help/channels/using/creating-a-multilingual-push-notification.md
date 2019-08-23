---
title: 다국어 푸시 알림 만들기
seo-title: 다국어 푸시 알림 만들기
description: 다국어 푸시 알림 만들기
seo-description: 다국어 푸시 알림을 만들어 사용자를 원하는 언어로 타겟팅할 수 있습니다.
page-status-flag: 정품 인증 안 함
uuid: D 4 AFF 741-E 969-47 C 6-BAE 8-787 C 6 C 673191
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 채널
content-type: 참조
topic-tags: 푸시 알림
discoiquuid: F 9 BB 2235-D 388-4025-9 ACE -734 BEB 0 C 1961
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 782a5f89b0361f1cbe59c9b353ca90dec90c3906

---


# 다국어 푸시 알림 만들기{#creating-a-multilingual-push-notification}

## 다국어 푸시 알림 정보 {#about-multilingual-push-notification}

사용자의 선호 언어 및 지역을 기반으로 메시지를 전송하여 푸시 알림 콘텐츠를 개인화할 수 있습니다. 컨텐츠 편집기에서 다국어 푸시 알림 컨텐츠 변형을 바로 가져와 한 번의 클릭으로 다국어 푸시 알림을 전송할 수 있습니다.

이 기능은 푸시 알림에 사용되는 배달 템플릿에 따라 모바일 앱 가입자에 대해 수신자의 프로필이나 시스템 언어 기본 설정에 지정된 기본 언어를 활용합니다. 특정 사용자에 대해 언어 기본 설정이 채워지지 않으면 시스템은 다국어 푸시 알림을 만드는 동안 정의된 기본 변형을 사용합니다. 프로필 및 가입자를 관리하는 방법에 대한 자세한 내용은 [이 안내서를](../../audiences/using/about-profiles-and-audiences.md)참조하십시오.

![](assets/multivariant_push_1.png)

푸시 알림 전달을 위해 다국어 컨텐츠 변형을 사용하려면 다음 단계를 수행하십시오.

* [1 단계: 다국어 컨텐츠 변형 업로드](../../channels/using/creating-a-multilingual-push-notification.md#step-1--upload-multilingual-content-variant)
* [2 단계: 다국어 컨텐츠 변형을 사용하여 푸시 알림 미리 보기 및 완성](../../channels/using/creating-a-multilingual-push-notification.md#step-2--preview-and-finalize-a-push-notification-using-multilingual-content-variants)
* [3 단계: 다국어 푸시 알림 전달 전송 및 분석](../../channels/using/creating-a-multilingual-push-notification.md#step-3--send-and-analyze-multilingual-push-notification-delivery)

## 1 단계: 다국어 컨텐츠 변형 업로드 {#step-1--upload-multilingual-content-variant}

다국어 푸시 알림을 개인화하기 전에 먼저 다국어 전달 템플릿에서 컨텐츠 변형을 업로드하고 전달을 만들어야 합니다.

>[!NOTE]
>
>각 언어 변형에 대해 수동으로 변형을 만들려면 이 단계를 건너뛸 수도 있습니다.

1. 에서 **[!UICONTROL Marketing activities]****[!UICONTROL Create]** 단추를 클릭한 **[!UICONTROL Push notification]**&#x200B;다음을 선택합니다.
1. 모바일 응용 프로그램 **[!UICONTROL Send multilingual push to Campaign profiles]** 또는 템플릿을 **[!UICONTROL Send multilingual push to app subscriber]** 구독한 Adobe Campaign 프로필을 타깃팅하여 모바일 응용 프로그램에서 알림을 받도록 선택한 모든 사용자에게 푸시 알림을 보내도록 하려면 템플릿을 선택합니다.

   ![](assets/multivariant_push_2.png)

1. 푸시 알림 속성을 입력하고 **[!UICONTROL Associate a Mobile App to a delivery]** 필드에서 모바일 앱을 선택합니다.

   드롭다운에는 SDK v 4와 Adobe Experience Platform SDK 애플리케이션이 모두 표시됩니다.

1. **[!UICONTROL Audiences]** Windows 에서는 쿼리를 드래그하여 놓는 방식으로 고객을 세밀하게 조정할 수 있습니다.

   추가된 쿼리는 선택한 템플릿에 따라 다릅니다. **[!UICONTROL Send multilingual push to Campaign profiles]** 템플릿을 선택한 경우 모바일 애플리케이션의 알려진 수신자를 쿼리할 수 있습니다. **[!UICONTROL Send multilingual push to app subscriber]** 반면에 템플릿을 선택한 경우 선택한 특정 앱의 모든 가입자를 쿼리할 수 있습니다.

   ![](assets/push_notif_audience.png)

1. **[!UICONTROL Manage Content Variants]** 창에서 파일을 드래그하여 놓거나 컴퓨터에서 파일을 선택합니다.

   파일은 UTF 8로 인코딩되어야 하며 **[!UICONTROL Download the sample file]** 이 옵션을 클릭하여 찾을 수 있는 특정 레이아웃을 가져야 합니다. 로케일 값에 적절한 구문을 사용해야 합니다. 파일 형식 및 지원되는 로케일에 대한 자세한 내용은 [이 기술 문서를](http://helpx.adobe.com/campaign/kb/acs-generate-csv-multilingual-push.html)참조하십시오.

   ![](assets/multivariant_push_4.png)

1. 파일을 업로드한 후 언어 변형이 **[!UICONTROL Variants]** 탭에 자동으로 채워집니다. 타깃팅된 사용자에 대해 기본 언어가 지정되지 않은 경우 기본 컨텐츠 변형이 될 파일에 A를 **[!UICONTROL Default variant]** 제공할 수 있습니다.

   ![](assets/multivariant_push_5.png)

1. **[!UICONTROL Variant selection]** 탭에서는 배달 템플릿에 따라 고려할 언어 기본 설정을 결정하는 스크립트를 제공합니다. 이 스크립트는 변경하지 않아도 됩니다.
1. 가져온 파일에 없는 변형을 더 추가하려면 **[!UICONTROL Add an element]** 단추를 클릭하고 필요에 따라 새 언어 변형을 추가할 수 있습니다.

   파일에서 업로드된 것 이외의 변형을 추가하여 이 언어와 연결할 수 없습니다. 배달 대시보드에서 직접 컨텐츠를 편집해야 합니다.

   ![](assets/multivariant_push_6.png)

1. 구성이 **[!UICONTROL Create]** 완료되면 클릭합니다. **[!UICONTROL Content variant]** 언제든지 창으로 돌아가 배달 대시보드에서 일부 항목을 변경할 수 있습니다.

   ![](assets/multivariant_push_8.png)

이제 다국어 푸시 알림을 개인화할 수 있습니다.

## 2 단계: 다국어 컨텐츠 변형을 사용하여 푸시 알림 미리 보기 및 완성 {#step-2--preview-and-finalize-a-push-notification-using-multilingual-content-variants}

컨텐츠 변형이 포함된 파일을 업로드한 후 푸시 알림 전달에서 다른 변형을 미리 볼 수 있습니다.

또한 파일에서 업로드된 것 외에도 더 많은 변형을 만들고 편집할 수 있습니다.

1. 배달 대시보드의 **[!UICONTROL Content]** 창에서 드롭다운을 사용하여 선택한 언어에 따라 푸시 알림 컨텐츠를 미리 볼 수 있습니다.

   ![](assets/multivariant_push_7.png)

1. 특정 언어에 대해 컨텐츠 변형이 지정되지 않은 경우 미리 보기 아래의 벨 아이콘을 클릭하여 이 언어 변형에 컨텐츠 추가를 시작합니다.

   **[!UICONTROL Content]** 창을 클릭하면 푸시 알림은 드롭다운에서 선택한 언어로 된 컨텐츠를 나타냅니다. 이 창에서 변경한 내용은 하나의 언어에만 적용됩니다.

1. 컨텐츠 변형을 클릭하여 개인화 필드로 예를 들어, 사용자 지정 필드를 추가할 수도 있습니다.

   푸시 알림을 사용자 정의하는 방법에 대한 자세한 내용은 [이 섹션을](../../channels/using/customizing-a-push-notification.md)참조하십시오.

   ![](assets/multivariant_push_9.png)

1. 언어 변형을 추가하거나 삭제하려면 **[!UICONTROL Content variant]** 창을 클릭합니다.

   새 언어를 추가하면 추가된 언어에 연결된 푸시 알림에 컨텐츠를 수동으로 추가해야 합니다.

   ![](assets/multivariant_push_10.png)

이제 다국어 푸시 알림 전달을 전송할 수 있습니다.

## 3 단계: 다국어 푸시 알림 전달 전송 및 분석 {#step-3--send-and-analyze-multilingual-push-notification-delivery}

이제 다국어 컨텐츠 변형 푸시 알림을 사용자에게 전송할 수 있습니다.

1. 전송을 시작하려면 **[!UICONTROL Prepare]** 단추를 클릭합니다.
1. 경고 없이 완료되면 **[!UICONTROL Confirm]** 단추를 클릭하여 다국어 푸시 전송을 시작할 수 있습니다.

   ![](assets/multivariant_push_12.png)

1. 푸시 알림을 성공적으로 전송한 다음 **[!UICONTROL Reports]** 아이콘을 클릭하여 **[!UICONTROL Dynamic reports]** 전달 성공률을 분석합니다.

   ![](assets/multivariant_push_13.png)

1. **[!UICONTROL Push notification report]** Select.
1. **[!UICONTROL Variant]** 데이터를 패널에 드래그하여 놓아 데이터 필터링을 시작합니다.

   ![](assets/multivariant_push_11.png)

이제 다국어 푸시 알림 전달 효과를 받는 사람에게 측정할 수 있습니다.

**관련 항목:**

* [푸시 알림 보고서](../../reporting/using/push-notification-report.md)
* [워크플로우 내에서 푸시 알림 전송](../../automating/using/push-notification-delivery.md)
* [하나의 워크플로우로 다국어 고객 확보](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Engageyourcustomersateverystep)
