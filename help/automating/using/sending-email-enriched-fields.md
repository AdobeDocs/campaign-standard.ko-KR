---
title: 보강된 필드가 포함된 이메일 보내기
description: 아래 예제는 파일 로드 활동을 통해 외부 파일에서 검색한 추가 데이터를 사용하여 이메일을 보내는 방법을 보여 줍니다.
page-status-flag: never-activated
uuid: 69af12cc-6f82-4977-9f53-aa7bc26f5d7e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 584ff893-9b1b-46c9-9628-714ab349ab88
context-tags: fileImport,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 75%

---


# 보강된 필드가 포함된 이메일 보내기 {#sending-email-enriched-fields}

<!--A new example showing how to send an email containing additional data retrieved from a load file activity has been added. [Read more](example-2-email-with-enriched-fields)-->

파일 로드 활동을 사용하면 같은 워크플로우를 통해 외부 파일의 추가 데이터로 보강한 이메일을 보낼 수 있습니다.

아래 예제는 파일 로드 활동을 통해 외부 파일에서 검색한 추가 데이터를 사용하여 이메일을 보내는 방법을 보여 줍니다. 이 예제에서 외부 파일에는 프로필 목록과 해당 프로필의 계좌 번호가 들어 있습니다. 이 데이터를 가져와서 각 프로필에 계좌 번호가 포함된 이메일을 보내려고 합니다.

![](assets/load_file_workflow_ex2.png)

워크플로우를 빌드하려면 다음 단계를 따르십시오.

1. Drag and drop a [Query](../../automating/using/query.md) activity into your workflow and open it to define the main target.

   <!--The Query activity is presented in the [Query](../../automating/using/query.md) section.-->

1. Drag and drop a [Load file](../../automating/using/load-file.md) activity to assign some data to a profile. 이 예제에서는 데이터베이스의 프로필 일부에 해당하는 계좌 번호가 들어 있는 파일을 로드합니다.

   ![](assets/load_file_activity.png)

1. Drag and drop an [Enrichment](../../automating/using/enrichment.md) activity into your workflow and link the load file and query activities to it.

1. 데이터 보강 활동의 **[!UICONTROL Advanced relations]** 탭에서 **[!UICONTROL 0 or 1 cardinality simple link]**&#x200B;을(를) 선택하고 조정에 사용할 필드를 정의합니다. 여기에서는 성을 사용하여 데이터와 데이터베이스 프로필을 조정합니다.

   ![](assets/load_file_enrichment_relation.png)

1. **[!UICONTROL Additional data]** 탭에서 이메일에 사용할 요소를 선택합니다. 여기에서는 계좌 번호(파일 로드 활동을 통해 검색한 파일의 열)를 선택합니다.

   ![](assets/load_file_enrichment_select_element.png)

   <!--![](assets/load_file_enrichment_additional_data.png)-->

   자세한 내용은 [데이터 보강](../../automating/using/enrichment.md) 섹션을 참조하십시오.

1. Drag and drop a [Segmentation](../../automating/using/segmentation.md) activity into your workflow and open it to refine the main target.

   ![](assets/load_file_segmentation.png)

   자세한 내용은 [세분화](../../automating/using/segmentation.md) 섹션을 참조하십시오.

1. Drag and drop an [Email delivery](../../automating/using/email-delivery.md) activity into your workflow and open it.

   <!--The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.-->

1. 개인화 필드를 추가하고 **[!UICONTROL Additional data (targetData)]** 노드에서 데이터 보강 활동에 정의된 추가 데이터(이 경우 계좌 번호)를 선택합니다. 이를 통해 이메일 콘텐츠에서 각 프로필의 계좌 번호를 다이내믹하게 가져올 수 있습니다.

   ![](assets/load_file_perso_field.png)

1. 이메일을 저장하고 워크플로우를 시작합니다.

이메일이 타겟에게 보내집니다. 각 프로필은 해당 계좌 번호가 담긴 이메일을 수신합니다.

![](assets/load_file_email.png)
