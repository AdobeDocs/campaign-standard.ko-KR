---
title: 암호화된 데이터 관리
description: 암호화된 데이터를 관리하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows, Encryption
role: Data Architect
level: Experienced
exl-id: 1df1552a-6578-47eb-ba14-fb91cd2a3999
source-git-commit: 69c47c8f3cbb405acbef634aa1ebaef8e767f159
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 4%

---

# 암호화된 데이터 관리 {#managing-encrypted-data}

## 사전 처리 단계 정보 {#about-preprocessing-stages}

경우에 따라 Campaign 서버를 가져올 데이터를 암호화해야 할 수 있습니다(예: PII 데이터가 포함된 경우).

나가는 데이터를 암호화하거나 들어오는 데이터를 해독하려면 다음을 사용하여 GPG 키를 관리해야 합니다 [Campaign 컨트롤 패널](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html?lang=ko).

>[!NOTE]
>
>Campaign 컨트롤 패널은 AWS에서 호스팅되는 모든 고객이 사용할 수 있습니다(온프레미스에서 마케팅 인스턴스를 호스팅하는 고객은 제외).

Campaign 컨트롤 패널을 사용할 자격이 없는 경우 Adobe 고객 지원 센터에 연락하여 필요한 암호화/암호 해독 명령을 인스턴스에 제공하도록 해야 합니다. 이렇게 하려면 다음을 나타내는 요청을 제출합니다.

* 다음 **레이블** 명령을 사용하기 위해 Campaign 인터페이스에 표시됩니다. 예: &quot;파일 암호화&quot;.
* 다음 **명령** 을 클릭하여 인스턴스에 설치합니다.

요청이 처리되면 다음 위치에서 암호화/암호 해독 명령을 사용할 수 있습니다. **[!UICONTROL Pre-processing stage]** 의 필드 **[!UICONTROL Load file]** 및 **[!UICONTROL Extract file]** 활동. 이 파일을 사용하여 가져오거나 내보낼 파일을 해독하거나 암호화할 수 있습니다.

![](assets/preprocessing-encryption.png)

**관련 항목:**

* [파일 로드](../../automating/using/load-file.md)
* [파일 추출](../../automating/using/extract-file.md)

## 사용 사례: Campaign 컨트롤 패널에서 생성한 키를 사용하여 암호화된 데이터 가져오기 {#use-case-gpg-decrypt}

이 사용 사례에서는 Campaign 컨트롤 패널에서 생성된 키를 사용하여 외부 시스템에서 암호화된 데이터를 가져오기 위한 워크플로우를 빌드합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

이 사용 사례를 수행하는 단계는 다음과 같습니다.

1. Campaign 컨트롤 패널을 사용하여 키 쌍(공개/비공개)을 생성합니다. 자세한 단계는에서 확인할 수 있습니다. [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html#decrypting-data).

   * 공개 키는 외부 시스템과 공유되며, 외부 시스템은 이 키를 사용하여 Campaign으로 전송할 데이터를 암호화합니다.
   * 개인 키는 Campaign에서 들어오는 암호화된 데이터를 해독하는 데 사용됩니다.

   ![](assets/gpg_generate.png)

1. 외부 시스템에서는 Campaign 컨트롤 패널에서 다운로드한 공개 키를 사용하여 데이터를 암호화하여 Campaign Standard으로 가져옵니다.

1. Campaign Standard에서 암호화된 데이터를 가져오고 Campaign 컨트롤 패널을 통해 설치된 개인 키를 사용하여 해독하는 워크플로우를 빌드합니다. 이렇게 하려면 다음과 같이 워크플로우를 빌드합니다.

   ![](assets/gpg_workflow.png)

   * **[!UICONTROL Transfer file]** 활동: 파일을 외부 소스에서 Campaign으로 전송합니다. 이 예에서는 SFTP 서버에서 파일을 전송하려고 합니다.
   * **[!UICONTROL Load file]** 활동: 파일에서 데이터베이스로 데이터를 로드하고 Campaign 컨트롤 패널에서 생성된 개인 키를 사용하여 해독합니다.

1. 를 엽니다. **[!UICONTROL Transfer file]** 그런 다음 필요에 따라 활동을 구성합니다. 활동을 구성하는 방법에 대한 전체적인 개념은에서 사용할 수 있습니다. [이 섹션](../../automating/using/load-file.md).

   다음에서 **[!UICONTROL Protocol]** 탭에서 전송할 sftp 서버 및 암호화된 .gpg 파일에 대한 세부 정보를 지정합니다.

   ![](assets/gpg_transfer.png)

1. 를 엽니다. **[!UICONTROL Load file]** 활동을 구성한 다음 필요에 따라 구성합니다. 활동을 구성하는 방법에 대한 전체적인 개념은에서 사용할 수 있습니다. [이 섹션](../../automating/using/load-file.md).

   들어오는 데이터를 해독하기 위해 활동에 전처리 단계를 추가합니다. 이렇게 하려면 **[!UICONTROL Decryption GPG]** 목록에서 옵션을 선택합니다.

   >[!NOTE]
   >
   >데이터 암호를 해독하는 데 사용할 개인 키를 지정할 필요는 없습니다. 개인 키는 Campaign 컨트롤 패널에 저장되며, 이를 통해 파일 암호를 해독하는 데 사용할 키를 자동으로 검색합니다.

   ![](assets/gpg_load.png)

1. 클릭 **[!UICONTROL OK]** 활동 구성을 확인합니다.

1. 이제 워크플로우를 실행할 수 있습니다.

## 사용 사례: Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기 {#use-case-gpg-encrypt}

이 사용 사례에서는 Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터를 암호화하고 내보내는 워크플로우를 빌드합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

이 사용 사례를 수행하는 단계는 다음과 같습니다.

1. GPG 유틸리티를 사용하여 GPG 키 쌍(공개/비공개)을 생성한 다음 공개 키를 Campaign 컨트롤 패널에 설치합니다. 자세한 단계는에서 확인할 수 있습니다. [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html#encrypting-data).

   ![](assets/gpg_install.png)

1. Campaign Standard에서 데이터를 내보내는 워크플로우를 빌드하고 Campaign 컨트롤 패널을 통해 설치된 개인 키를 사용하여 암호화합니다. 이렇게 하려면 다음과 같이 워크플로우를 빌드합니다.

   ![](assets/gpg-workflow-export.png)

   * **[!UICONTROL Query]** 활동: 이 예제에서는 내보내려는 데이터베이스의 데이터를 타겟팅하는 쿼리를 실행하려고 합니다.
   * **[!UICONTROL Extract file]** 활동: 데이터를 암호화하여 파일로 추출합니다.
   * **[!UICONTROL Transfer file]** 활동: 암호화된 데이터가 포함된 파일을 SFTP 서버로 전송합니다.

1. 구성 **[!UICONTROL Query]** 활동으로 데이터베이스에서 원하는 데이터를 타겟팅할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../automating/using/query.md)을 참조하십시오.

1. 를 엽니다. **[!UICONTROL Extract file]** 그런 다음 필요에 따라 활동을 구성합니다(출력 파일, 열, 형식 등). 활동을 구성하는 방법에 대한 전체적인 개념은에서 사용할 수 있습니다. [이 섹션](../../automating/using/extract-file.md).

   추출할 데이터를 암호화하기 위해 활동에 전처리 단계를 추가합니다. 이렇게 하려면 데이터를 암호화하는 데 사용할 암호화 GPG 키를 선택합니다.

   ![](assets/gpg-extract-stage.png)

   >[!NOTE]
   >
   >괄호로 묶인 값은 **댓글** gpg 암호화 도구를 사용하여 키 쌍을 생성할 때 정의한 것입니다. 올바른 일치 키를 선택해야 합니다. 그렇지 않으면 수신자는 파일의 암호를 해독할 수 없습니다.

1. 를 엽니다. **[!UICONTROL Transfer file]** 그런 다음 파일을 전송할 SFTP 서버를 지정합니다. 활동을 구성하는 방법에 대한 전체적인 개념은에서 사용할 수 있습니다. [이 섹션](../../automating/using/transfer-file.md).

   ![](assets/gpg-transfer-encrypt.png)

1. 이제 워크플로우를 실행할 수 있습니다. 실행되면 쿼리의 데이터 대상이 SFTP 서버로 암호화된 .gpg 파일로 내보내집니다.

## 튜토리얼 비디오 {#video}

이 비디오는 GPG 키를 사용하여 데이터를 해독하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/35753?quality=12)

이 비디오는 GPG 키를 사용하여 데이터를 암호화하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/36380?quality=12)

추가 Campaign Standard 방법 비디오를 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko).
