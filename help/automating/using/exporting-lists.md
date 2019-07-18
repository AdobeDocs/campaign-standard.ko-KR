---
title: 목록 내보내기
seo-title: 목록 내보내기
description: 목록 내보내기
seo-description: 'Adobe Campaign 에서는 나중에 사용할 수 있도록 개요 화면의 목록으로 표시된 데이터를 파일로 직접 내보낼 수 있습니다. '
page-status-flag: 정품 인증 안 함
uuid: C 64 FE 706-BD 6 E -4746-958 E-F 94226 F 4 E 2 CB
contentOwner: Sauviat
products: sg_ campaign/standard
audience: 자동화
content-type: 참조
topic-tags: 가져오기 및 내보내기 데이터
discoiquuid: 12 c 874 DA -435 F -44 B 6-A 3 C 8-873301 E 177 CC
internal: n
snippet: Y
translation-type: tm+mt
source-git-commit: 36727e82d3aa73add6116fa2916752ff0e407d9d

---


# Exporting lists{#exporting-lists}

Adobe Campaign를 사용하면 나중에 사용할 수 있도록 파일로 직접 목록을 내보낼 수 있습니다. Exporting a list in a file generates a log entry in the **[!UICONTROL Export audits]** menu. For more information on export audits, refer to the [Auditing exports](../../administration/using/auditing-export-logs.md) section.

The export list option allows you to export a maximum of 100,000 lines by default and defined by the **Nms_ExportListLimit** option. This option can be managed by the functional administrator, under the **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]** menu.

Export list is available in all the screens that have a **List** mode view, for users with the **[!UICONTROL EXPORT (export)]** role.

1. Go to your chosen **List** screen. For example, the test profile overview screen ( **[!UICONTROL Profiles & audiences]** &gt; **[!UICONTROL Test profiles]** ).
1. Check that the screen is in **List** mode.

   ![](assets/export_list_mode_switch.png)

1. Organize the columns in the list in the order that you want to export them using the **[!UICONTROL Configure list]** button, in the top right corner. 구성된 열 외에도 리소스의 기본 키를 내보냅니다.
1. 원하는 경우 필터를 적용할 수 있습니다. 이렇게 하려면 왼쪽 상단의 단추를 클릭하여 검색 창을 표시합니다.

   다른 리소스가 포함된 목록에서 내보내기를 수행하는 경우 목록에 한 가지 유형의 리소스만 표시되도록 필터를 적용해야 합니다.

1. 원하는 경우 선택한 열을 정렬합니다.
1. Select the export button ![](assets/exportlistbutton.png).

   팝업을 확인하는 팝업이 나타납니다. 내보내기를 확인하면 파일이 자동으로 컴퓨터에 다운로드됩니다.

내보내기가 iOS에서 수행되지 않는 한 파일이 txt 형식인 경우 파일이 CSV 형식으로 생성됩니다. 내보낸 리소스와 내보내기 날짜에 따라 이름이 지정됩니다. 예를 들면 다음과 같습니다. Profilebase_ 20150426_ 120253. csv 라는 이름은 2015 년 4 월 26 일 12:02:53에 수행한 프로필 내보내기에 적용됩니다. UTF -8 형식으로 인코딩됩니다.

숫자 값과 날짜는 내보내기를 수행하는 사용자의 현지 시간 (로케일) 를 고려합니다. 예를 들면 다음과 같습니다. dd-mm-yyyy 또는 mm-dd-yyyy.

이 값보다 큰 내보내기를 수행하려면 전용 워크플로우를 만들어야 합니다. Refer to the [Extract file](../../automating/using/extract-file.md) section.

**example**

다음 예는 아래 정의된 프로필 목록에서 수행한 내보내기입니다.

* 표시된 열 (순서대로): 성, 이름, 생년월일, 이메일 주소.
* 이름은 알파벳순으로 정렬됩니다.

![](assets/export_list_example1.png)

생성된 파일은 다음과 같이 표시됩니다 (처음 10 개 레코드에 대해).

```
Last name;First name;Birth date;Email;Zip code
Abalo;Patrick;11/11/1941 02:00:00;patrick.a@testmail.com;29200
Abasq;Joel;21/08/1977 02:00:00;abasq.joel@testmail.com;92160
Abernot;John;12/07/1963 01:00:00;john.abernot@testmail.com;78510
Abiven;Christian;16/03/1975 01:00:00;chris.a@mailtest.com;35000
Abouvier;Peter;02/07/1975 01:00:00;pabouvier@mailtest.com;94560
Accardi;Mike;22/06/1948 01:00:00;mike.accardi@mail.com;76400
Accremont;Frank;27/04/1947 01:00:00;accr.frank@mailtest.com;13500
Adam;Daniel;17/09/1953 01:00:00;danieladam@mail.com;17000
Adama;Pascal;22/01/1990 01:00:00;adapascal@mailtest.com;75012
Adama;Henry;22/09/1992 02:00:00;henry.adama@mail.com;64120
```

**관련 항목:**

* [역할](../../administration/using/list-of-roles.md)
* [목록 사용자 지정](../../start/using/customizing-lists.md)
* [목록 비디오 구성](https://helpx.adobe.com/campaign/kt/acs/using/acs-configuring-a-list-feature-video-setup.html)

