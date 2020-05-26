---
title: 암호화된 데이터 관리
description: 암호화된 데이터를 관리하는 방법을 알아봅니다.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# 암호화된 데이터 관리 {#managing-encrypted-data}

경우에 따라, 캠페인 서버를 가져오려는 데이터를 암호화해야 할 수 있습니다(예: PII 데이터가 포함되어 있는 경우).

암호화된 파일을 가져오거나 내보내려면 먼저 Adobe 고객 지원 센터에 연락하여 필요한 암호화/암호 해독 명령을 인스턴스에 제공해야 합니다.

이렇게 하려면 다음을 나타내는 요청을 제출합니다.

* 명령을 사용하기 위해 캠페인 인터페이스에 표시되는 **레이블입니다** . 예: &quot;파일 암호화&quot;
* 인스턴스에 설치하는 **명령입니다** .
예를 들어 PGP를 사용하여 파일의 암호를 해독하려면 다음 명령을 사용합니다.

   ```
   <path-to_pgp_if-not_global_or_server/>pgp.exe --decrypt --input nl6/var/vp/import/filename.pgp --passphrase "your password" --recipient recipient @email.com --verbose --output nl6/var/vp/import/filename
   ```

요청이 처리되면, 암호화/암호 해독 명령은 **[!UICONTROL Pre-processing stage]** 및 **[!UICONTROL Load file]** 활동의 필드 **[!UICONTROL Extract file]** 에서 사용할 수 있습니다. 이 암호를 사용하여 가져오거나 내보낼 파일의 암호를 해독하거나 암호화할 수 있습니다.

![](assets/preprocessing-encryption.png)

**관련 항목:**

* [파일 로드](../../automating/using/load-file.md)
* [파일 추출](../../automating/using/extract-file.md)
