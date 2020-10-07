---
title: 데이터베이스로 파일 대상자 조정
description: 이 예에서는 대상 읽기 활동을 사용하여 파일 가져오기에서 직접 만든 대상을 조정하는 방법을 보여 줍니다.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 87%

---


# 데이터베이스로 파일 대상자 조정 {#example--reconcile-a-file-audience-with-the-database}

이 예제에서는 **[!UICONTROL Read audience]** 활동을 사용하여 파일 가져오기로 직접 만든 대상자를 조정하는 방법을 보여줍니다. 

파일 가져오기를 수행할 때 콘텐츠를 대상자에 직접 저장할 수 있습니다. 이 대상자는 파일 대상자이며, 데이터는 데이터베이스 리소스에 연결되어 있지 않습니다.

가져오기 워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example3.png)

* [파일 로드](../../automating/using/load-file.md) 활동으로 외부 도구에서 추출한 프로필 데이터가 포함된 파일을 업로드합니다.

   예제:

   ```
   lastname;firstname;birthdate;email;crmID
   Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
   Mars;Daniel;17/11/1987;dannymars@example.com;123545
   Smith;Clara;08/02/1989;hayden.smith@example.com;124567
   Durance;Allison;15/12/1978;allison.durance@example.com;120987
   Lucassen;Jody;28/03/1988;jody.lucassen@example.com;127634
   Binder;Tom;19/01/1982;tombinder@example.com;128653
   Binder;Tommy;19/01/1915;tombinder@example.com;134576
   Connor;Jade;10/10/1979;connor.jade@example.com;132452
   Mack;Clarke;02/03/1985;clarke.mack@example.com;149876
   Ross;Timothy;04/07/1986;timross@example.com;157643
   ```

* [대상자 저장](../../automating/using/save-audience.md) 활동으로 들어오는 데이터를 대상자로 저장합니다. 데이터가 아직 조정되지 않았기 때문에 이 대상자는 파일 대상자이며, 데이터가 아직 프로필 데이터로 인식되지 않습니다.

조정 워크플로우는 다음과 같이 디자인됩니다.

![](assets/readaudience_activity_example2.png)

* A [Read audience](../../automating/using/read-audience.md) activity uploads the File audience created in the import workflow. 아직 대상자 데이터가 Adobe Campaign 데이터베이스로 조정되지 않았습니다.
* [조정](../../automating/using/reconciliation.md) 활동은 **[!UICONTROL Identification]** 탭을 통해 들어오는 데이터를 프로필로 식별합니다. 예를 들어 조정 기준으로 **이메일** 필드를 사용하는 등의 방법이 있습니다.
* [데이터 업데이트](../../automating/using/update-data.md) 활동은 들어오는 데이터로 데이터베이스의 프로필 리소스를 삽입 및 업데이트합니다. 데이터가 이미 프로필로 식별되었으므로 **[!UICONTROL Directly using the targeting dimension]** 옵션을 선택하고 활동의 **[!UICONTROL Identification]** 탭에서 **[!UICONTROL Profiles]**&#x200B;을(를) 선택할 수 있습니다. 그런 다음 해당하는 탭에서 업데이트해야 하는 필드 목록을 추가하면 됩니다.
