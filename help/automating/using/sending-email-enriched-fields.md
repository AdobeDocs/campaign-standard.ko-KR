---
title: 풍부한 필드가 포함된 이메일 보내기
description: 아래 예제는 파일 로드 작업을 통해 외부 파일에서 검색된 추가 데이터를 사용하여 이메일을 전송하는 방법을 보여줍니다.
page-status-flag: never-activated
uuid: 69af12cc-6f82-4977-9f53-aa7bc26f5d7e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 584ff893-9b1b-46c9-9628-714ab349ab88
context-tags: fileImport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---


# 풍부한 필드가 포함된 이메일 보내기 {#sending-email-enriched-fields}

<!--A new example showing how to send an email containing additional data retrieved from a load file activity has been added. [Read more](example-2-email-with-enriched-fields)-->

또한 파일 로드 작업을 사용하면 동일한 워크플로우에서 외부 파일의 추가 데이터가 포함된 이메일을 보낼 수 있습니다.

아래 예제는 파일 로드 작업을 통해 외부 파일에서 검색된 추가 데이터를 사용하여 이메일을 전송하는 방법을 보여줍니다. 이 예에서 외부 파일에는 관련 계정 번호와 함께 프로파일 목록이 들어 있습니다. 이 데이터를 가져와서 계정 번호와 함께 각 프로필에 이메일을 보내려는 경우

![](assets/load_file_workflow_ex2.png)

워크플로우를 빌드하려면 다음 단계를 따르십시오.

1. 워크플로우 [에 쿼리](../../automating/using/query.md) 활동을 끌어다 놓고 열어서 기본 대상을 정의합니다.

   <!--The Query activity is presented in the [Query](../../automating/using/query.md) section.-->

1. 파일 [로드](../../automating/using/load-file.md) 활동을 드래그하여 놓아 프로필에 일부 데이터를 할당합니다. 이 예에서는 데이터베이스의 일부 프로필에 해당하는 계정 번호가 포함된 파일을 로드합니다.

   ![](assets/load_file_activity.png)

1. 데이터 [농축활동](../../automating/using/enrichment.md) (Enrichment Activity)을 워크플로우에 드래그 앤 드롭하여 로드 파일과 쿼리 활동을 여기에 연결합니다.

1. 농축활동 **[!UICONTROL Advanced relations]** 탭에서 조정을 위해 사용할 필드를 **[!UICONTROL 0 or 1 cardinality simple link]** 선택하고 정의합니다. 여기에서 마지막으로 이름을 사용하여 데이터를 데이터베이스 프로필과 조정합니다.

   ![](assets/load_file_enrichment_relation.png)

1. 탭에서 **[!UICONTROL Additional data]** 이메일에 사용할 요소를 선택합니다. 여기에서 계정 번호(로드 파일 활동을 통해 검색한 파일의 열)를 선택합니다.

   ![](assets/load_file_enrichment_select_element.png)

   <!--![](assets/load_file_enrichment_additional_data.png)-->

   자세한 내용은 [데이터 연계](../../automating/using/enrichment.md) 섹션을 참조하십시오.

1. 워크플로우에 [세그멘테이션](../../automating/using/segmentation.md) 활동을 드래그 앤 드롭한 다음 열어 기본 타겟을 세분화합니다.

   ![](assets/load_file_segmentation.png)

   자세한 내용은 세그멘테이션 [섹션을](../../automating/using/segmentation.md) 참조하십시오.

1. 워크플로우에 [이메일 배달](../../automating/using/email-delivery.md) 활동을 드래그하여 놓고 엽니다.

   <!--The Email delivery activity is presented in the [Email delivery](../../automating/using/email-delivery.md) section.-->

1. 개인화 필드를 추가하고 노드에서 농축활동(계정 번호)에 정의된 추가 데이터를 **[!UICONTROL Additional data (targetData)]** 선택합니다. 이를 통해 이메일 컨텐츠에 있는 각 프로필의 계정 번호를 동적으로 검색할 수 있습니다.

   ![](assets/load_file_perso_field.png)

1. 이메일을 저장하고 워크플로우를 시작합니다.

이메일이 타겟으로 전송됩니다. 각 프로필은 해당 계정 번호와 함께 이메일을 수신합니다.

![](assets/load_file_email.png)
