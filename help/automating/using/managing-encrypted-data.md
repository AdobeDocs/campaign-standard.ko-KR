---
solution: Campaign Standard
product: campaign
title: 암호화된 데이터 관리
description: 암호화된 데이터를 관리하는 방법을 알아봅니다.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: 워크플로우
role: Data Architect
level: Experienced
exl-id: 1df1552a-6578-47eb-ba14-fb91cd2a3999
source-git-commit: 05e7de6d59420f532e0095ddb1fd7f158519518b
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 5%

---

# 암호화된 데이터 관리 {#managing-encrypted-data}

## 사전 처리 단계 정보 {#about-preprocessing-stages}

경우에 따라 Campaign Server를 가져오려는 데이터를 암호화해야 할 수 있습니다(예: PII 데이터가 포함되어 있는 경우).

발신 데이터를 암호화하거나 들어오는 데이터를 해독하려면 [Campaign 컨트롤 패널](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html?lang=ko)을(를) 사용하여 GPG 키를 관리해야 합니다.

>[!NOTE]
>
>Campaign 컨트롤 패널은 AWS를 통해 호스팅되는 모든 고객에게 제공됩니다(온 프레미스에서 마케팅 인스턴스를 호스팅하는 고객은 제외).

Campaign 컨트롤 패널을 사용할 수 없는 경우 인스턴스에 필요한 암호화/암호 해독 명령을 제공하도록 Adobe 고객 지원 센터에 문의해야 합니다. 이렇게 하려면 다음을 나타내는 요청을 제출합니다.

* 명령을 사용하기 위해 Campaign 인터페이스에 표시되는 **label**&#x200B;입니다. 예: &quot;파일 암호화&quot;
* 인스턴스에 설치할 **명령**&#x200B;입니다.

요청이 처리되면 **[!UICONTROL Load file]** 및 **[!UICONTROL Extract file]** 활동의 **[!UICONTROL Pre-processing stage]** 필드에서 암호화 / 암호 해독 명령을 사용할 수 있습니다. 이 파일을 사용하여 가져오거나 내보낼 파일을 해독하거나 암호화할 수 있습니다.

![](assets/preprocessing-encryption.png)

**관련 항목:**

* [파일 로드](../../automating/using/load-file.md)
* [파일 추출](../../automating/using/extract-file.md)

## 사용 사례:Campaign 컨트롤 패널 {#use-case-gpg-decrypt}에서 생성한 키를 사용하여 암호화된 데이터 가져오기

이 사용 사례에서는 Campaign 컨트롤 패널에서 생성된 키를 사용하여 외부 시스템에서 암호화된 데이터를 가져오기 위한 워크플로우를 빌드합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

이 사용 사례를 수행하는 단계는 다음과 같습니다.

1. 키 쌍(공개/개인)을 생성하려면 Campaign 컨트롤 패널을 사용합니다. 자세한 단계는 [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html#decrypting-data)에서 확인할 수 있습니다.

   * 공개 키는 외부 시스템과 공유되며, 이 키를 사용하여 Campaign으로 전송할 데이터를 암호화합니다.
   * 개인 키는 Campaign이 들어오는 암호화된 데이터를 해독하는 데 사용됩니다.

   ![](assets/gpg_generate.png)

1. 외부 시스템에서 Campaign 컨트롤 패널에서 다운로드한 공개 키를 사용하여 Campaign Standard으로 가져올 데이터를 암호화합니다.

1. Campaign Standard에서 Campaign 컨트롤 패널을 통해 설치된 개인 키를 사용하여 암호화된 데이터를 가져오는 워크플로우를 빌드하고 암호를 해독합니다. 이를 위해 다음과 같이 워크플로우를 빌드합니다.

   ![](assets/gpg_workflow.png)

   * **[!UICONTROL Transfer file]** 활동:외부 소스에서 Campaign으로 파일을 전송합니다. 이 예제에서는 SFTP 서버에서 파일을 전송하려고 합니다.
   * **[!UICONTROL Load file]** 활동:파일의 데이터를 데이터베이스에 로드하고 Campaign 컨트롤 패널에서 생성된 개인 키를 사용하여 암호를 해독합니다.

1. **[!UICONTROL Transfer file]** 활동을 열고 필요에 따라 구성합니다. 활동 구성 방법에 대한 글로벌 개념은 [이 섹션](../../automating/using/load-file.md)에서 확인할 수 있습니다.

   **[!UICONTROL Protocol]** 탭에서 전송할 sftp 서버 및 암호화된 .gpg 파일에 대한 세부 정보를 지정합니다.

   ![](assets/gpg_transfer.png)

1. **[!UICONTROL Load file]** 활동을 연 다음 필요에 따라 구성합니다. 활동 구성 방법에 대한 글로벌 개념은 [이 섹션](../../automating/using/load-file.md)에서 확인할 수 있습니다.

   들어오는 데이터를 해독하기 위해 활동에 사전 처리 단계를 추가합니다. 이렇게 하려면 목록에서 **[!UICONTROL Decryption GPG]** 옵션을 선택합니다.

   >[!NOTE]
   >
   >데이터 암호를 해독하는 데 사용할 개인 키를 지정할 필요는 없습니다. 개인 키는 Campaign 컨트롤 패널에 저장되며 이 키는 파일의 암호를 해독하는 데 사용할 키를 자동으로 감지합니다.

   ![](assets/gpg_load.png)

1. **[!UICONTROL OK]** 을 클릭하여 활동 구성을 확인합니다.

1. 이제 워크플로우를 실행할 수 있습니다.

## 사용 사례:{#use-case-gpg-encrypt} Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터 암호화 및 내보내기

이 사용 사례에서는 Campaign 컨트롤 패널에 설치된 키를 사용하여 데이터를 암호화하고 내보내기 위해 워크플로우를 빌드합니다.

![](assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

이 사용 사례를 수행하는 단계는 다음과 같습니다.

1. GPG 유틸리티를 사용하여 GPG 키 쌍(공개/개인)을 생성한 다음 공개 키를 Campaign 컨트롤 패널에 설치합니다. 자세한 단계는 [Campaign 컨트롤 패널 설명서](https://experienceleague.adobe.com/docs/control-panel/using/instances-settings/gpg-keys-management.html#encrypting-data)에서 확인할 수 있습니다.

   ![](assets/gpg_install.png)

1. Campaign Standard에서 Campaign 컨트롤 패널을 통해 설치된 개인 키를 사용하여 데이터를 내보내고 암호화하는 워크플로우를 빌드합니다. 이를 위해 다음과 같이 워크플로우를 빌드합니다.

   ![](assets/gpg-workflow-export.png)

   * **[!UICONTROL Query]** 활동:이 예제에서는 내보낼 데이터베이스의 데이터를 타겟팅하는 쿼리를 실행하려고 합니다.
   * **[!UICONTROL Extract file]** 활동:데이터를 암호화하고 파일에 추출합니다.
   * **[!UICONTROL Transfer file]** 활동:암호화된 데이터가 포함된 파일을 SFTP 서버로 전송합니다.

1. 데이터베이스에서 원하는 데이터를 타겟팅하도록 **[!UICONTROL Query]** 활동을 구성합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../../automating/using/query.md)을 참조하십시오.

1. **[!UICONTROL Extract file]** 활동을 열고 필요에 따라 구성합니다(출력 파일, 열, 형식 등). 활동 구성 방법에 대한 글로벌 개념은 [이 섹션](../../automating/using/extract-file.md)에서 확인할 수 있습니다.

   추출할 데이터를 암호화하기 위해 활동에 사전 처리 단계를 추가합니다. 이렇게 하려면 데이터를 암호화하는 데 사용할 암호화 GPG 키를 선택합니다.

   ![](assets/gpg-extract-stage.png)

   >[!NOTE]
   >
   >괄호로 묶인 값은 GPG 암호화 도구를 사용하여 키 쌍을 생성할 때 정의한 **주석**&#x200B;입니다. 올바른 일치 키를 선택해야 수신자가 파일의 암호를 해독할 수 없습니다.

1. **[!UICONTROL Transfer file]** 활동을 열고 파일을 전송할 SFTP 서버를 지정합니다. 활동 구성 방법에 대한 글로벌 개념은 [이 섹션](../../automating/using/transfer-file.md)에서 확인할 수 있습니다.

   ![](assets/gpg-transfer-encrypt.png)

1. 이제 워크플로우를 실행할 수 있습니다. 실행되면 쿼리에 의한 데이터 타겟이 SFTP 서버로 암호화된 .gpg 파일로 내보내집니다.

## 튜토리얼 비디오 {#video}

이 비디오에서는 GPG 키를 사용하여 데이터를 해독하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/35753?quality=12)

이 비디오에서는 GPG 키를 사용하여 데이터를 암호화하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/36380?quality=12)

추가 Campaign Standard 방법 동영상은 [여기](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=ko)에 있습니다.
