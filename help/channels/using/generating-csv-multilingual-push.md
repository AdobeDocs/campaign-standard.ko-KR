---
title: Campaign Standard을 사용하여 다국어 푸시 알림용 CSV 파일 생성
description: CSV 파일을 업로드하여 배달할 컨텐츠를 생성하는 것은 다국어 푸시 알림을 지원하는 데 사용되는 기능입니다.
page-status-flag: never-activated
uuid: e90f4ec8-14e3-4304-b5fc-bce0ba08a4ef
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 79231445-1d51-499a-adcf-0c0f6db1cfa3
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---


# 다국어 푸시 알림용 CSV 파일 생성{#generating-csv-multilingual-push}

CSV 파일을 업로드하여 배달할 컨텐츠를 생성하는 것은 다국어 푸시 알림을 지원하는 데 사용되는 기능입니다. CSV 파일의 형식은 파일 업로드가 성공하고 결과적으로 배달을 만들 수 있도록 하기 위한 특정 지침을 준수해야 합니다. 다음 섹션에서는 파일 형식 및 해당 고려 사항에 대해 설명합니다.

## 파일 포맷 {#file-format}

CSV 파일에 다국어 푸시가 필요한 열:

1. title
1. messageBody
1. 사운드
1. adge
1. deplinkURI
1. category
1. iosMediaAttachmentURL
1. androidMediaAttachmentURL
1. isContentAvailable
1. isMutableContent
1. customFields
1. 로케일
1. language
1. silentPush

창에서 을 클릭하여 CSV 샘플 **[!UICONTROL Download a sample file]** 을 **[!UICONTROL Manage Content Variants]** 확인합니다. For more on this, refer to the this [section](../../channels/using/creating-a-multilingual-push-notification.md).

* **title, messageBody, sound, badge, deplinkURI, category, iosMediaAttachmentURL, androidMediaAttachmentURL**:정기적인 푸시 페이로드 내용 이 정보는 푸시 배달을 만들 때와 유사한 방법으로 제공해야 합니다.
* **사용자 정의 필드**: 사용자 정의 필드(예: `{"key1":"value1","key2":"value2"}`. 사용자 정의 필드의 예는 위의 샘플 파일을 참조하십시오.
* **isContentAvailable**:컨텐츠 사용 가능 확인 플래그, 값 1은 true를 의미하며 값 0은 false를 의미합니다. 기본값은 0입니다. 이 열을 비워 두면 값이 0으로 간주됩니다.
* **isMutableContent**:가변 컨텐트에 대한 플래그, 값 1은 true를, 값 0은 false를 의미합니다. 기본값은 0입니다. 이 열을 비워 두면 값이 0으로 간주됩니다.
* **로케일**:locale은 언어 변형의 필드입니다(예:).&quot;en_us&quot; for US-English, &quot;fr_fr&quot; for France-French.
* **언어**:로케일과 연관된 언어의 이름입니다. 예를 들어 로케일이 &quot;en_us&quot;인 경우 언어 이름은 &quot;영어-미국&quot;이어야 합니다.
* **silentPush**:푸시 알림 유형에 대한 플래그. 일반 푸시 알림일 경우 값은 0이어야 합니다. 자동 푸시인 경우 값은 1이어야 합니다. 기본값은 0입니다. 이 열을 비워 두면 값이 0으로 간주됩니다.

## csv 파일 작성을 위한 제한 및 지침 {#constraints-guideline-csv}

**각 열의 이름이 수정되었습니다**.
컨텐츠에 열을 사용하지 않는 경우 CSV 파일에 각 열의 이름을 포함해야 합니다.

**&quot;locale&quot; 및 &quot;language&quot; 열은 필수이며 값은 각 행에 대해 고유합니다.**
이 열에 대해 빈 값을 사용하면 파일 업로드가 실패합니다.

**열의 순서가 중요합니다**. 업로드된 파일의 열 순서는 샘플 파일과 동일한 형식을 따라야 합니다.

**견적 열 컨텐츠**. CSV(쉼표로 구분된 값) 파일이므로 쉼표(,)를 포함하는 열 내용을 따옴표로 묶어야 합니다. 예: &quot;Hello, Tom!&quot;

**국제 문자에 UTF-8 인코딩이 필요합니다.**

**일반 텍스트로 파일을 생성하는 경우 각 열을 &quot;,&quot;로 구분합니다.**

**변형 불일치.** 컨텐츠 블록을 사용하고 특정 언어로 대상 고객을 타깃팅하는 경우 CSV 파일에 대상 언어를 모두 나열해야 합니다. 그렇지 않으면 배달을 보낼 때 오류가 발생합니다.

## csv 파일에 개인화 필드 삽입 {#personalization-field-csv}

개인화 필드를 사용하려면 파일에 <span> 태그를 포함해야 합니다.

messageBody에 &quot;firstName&quot; 개인화 필드를 삽입하려면 메시지가 다음과 같아야 합니다.

```
 "Hello <span class="nl-dce-field nl-dce-done"  data-nl-expr="/context/profile/firstName">First name</span>, this is message".
```

&quot;firstName&quot; 필드는 다음으로 표시됩니다.

```
 <span class="nl-dce-field nl-dce-done" data-nl-expr="/context/profile/firstName">First name</span>
```

이 범위에는 두 가지 필수 속성이 있습니다.

* 하나는 정적인 수업이다. 어떤 개인화 필드를 사용할지 관계없이 항상 class=&quot;nl-dce-field nl-dce-dce-done&quot;이 됩니다.

* 다른 하나는 개인화 필드의 경로인 data-nl-exr입니다. 예를 들어 UI에서 &quot;firstName&quot; 개인화 필드를 삽입하면 탐색 경로가 **[!UICONTROL Context (context)]** > **[!UICONTROL Profile (profile)]** > **[!UICONTROL First name (firstName)]** (아래 이미지에 표시된 대로)됩니다. 이 경우 경로는

   ```
   /context/profile/firstName. data-nl-expr="/context/profile/firstName".
   ```

![](assets/multilingual_push_2.png)

## 로케일 및 언어 이름 {#locale-language-names}

지원되는 언어는 다음과 같습니다.

| 로케일 | language |
|:-:|:-:|
| af_za | 아프리칸스어 - 남아프리카 |
| sq_al | 알바니아 - 알바니아 |
| ar_dz | 아랍어 - 알제리 |
| ar_bh | 아랍어 - 바레인 |
| ar_iq | 아랍어 - 이라크 |
| ar_il | 아랍어 - 이스라엘 |
| ar_jo | 아랍어 - 요르단 |
| ar_kw | 아랍어 - 쿠웨이트 |
| ar_lb | 아랍어 - 레바논 |
| ar_ma | 아랍어 - 모로코 |
| ar_om | 아랍어 - 오만 |
| ar_qa | 아랍어 - 카타르 |
| ar_sa | 아랍어 - 사우디아라비아 |
| ar_sy | 아랍어 - 시리아 |
| ar_tn | 아랍어 - 튀니지 |
| ar_ae | 아랍어 - 아랍에미리트 |
| ar_ye | 아랍어 - 예멘 |
| hy_am | 아르메니아 - 아르메니아 |
| az_az | 아제리 - 아제르바이잔 |
| be_by | 벨로루시 - 벨라루스 |
| bs_ba | 보스니아 - 보스니아 |
| bg_bg | 불가리아어 - 불가리아 |
| ca_es | 카탈로니아어 - 스페인 |
| zh_cn | 중국어(간체) - 중국 |
| zh_sg | 중국어(간체) - 싱가포르 |
| zh_hk | 중국어(번체) - 중국 홍콩 특별 행정구 |
| zh_tw | 중국어 번체 - 대만 지역 |
| hr | 크로아티아어 - 크로아티아 |
| cs_cz | 체코어 - 체체치아 |
| da_dk | 덴마크어 - 덴마크 |
| nl_be | 네덜란드어 - 벨기에 |
| nl_nl | 네덜란드어 - 네덜란드 |
| en_au | 영어 - 오스트레일리아 |
| en_bz | 영어 - 벨리즈 |
| en_ca | 영어 - 캐나다 |
| en_in | 영어 - 인도 |
| en_ie | 영어 - 아일랜드 |
| en_jm | 영어 - 자메이카 |
| en_nz | 영어 - 뉴질랜드 |
| en_ph | 영어 - 필리핀 |
| en_za | 영어 - 남아프리카 |
| en_tt | 영어 - 트리니다드 토바고 |
| en_gb | 영어 - 영국 |
| en_us | 영어 - 미국 |
| en_zw | 영어 - 짐바브웨 |
| et_ee | 에스토니아어 - 에스토니아 |
| fi_fi | 핀란드어 - 핀란드 |
| fr_be | 프랑스어 - 벨기에 |
| fr_ca | 프랑스어 - 캐나다 |
| fr_fr | 프랑스어 - 프랑스 |
| fr_lu | 프랑스어 - 룩셈부르크 |
| fr_ch | 프랑스어 - 스위스 |
| de_at | 독일어 - 오스트리아 |
| de_de | 독일어 - 독일 |
| de_lu | 독일어 - 룩셈부르크 |
| de_ch | 독일어 - 스위스 |
| el_cy | 그리스어 - 키프로스 |
| el_gr | 그리스어 - 그리스 |
| gu_in | 구자라티 - 인도 |
| he_il | 히브리어 - 이스라엘 |
| hi_in | 힌디어 - 인도 |
| hu_hu | 헝가리어 - 헝가리 |
| is_is | 아이슬란드어 - 아이슬란드 |
| id_id | 인도네시아 - 인도네시아 |
| it_it | 이탈리아어 - 이탈리아 |
| it_ch | 이탈리아어 - 스위스 |
| ja_jp | 일본어 - 일본 |
| kn_in | 칸나다 - 인도 |
| kz | 카자흐어 - 카자흐스탄 |
| ko_kr | 한국어 - 대한민국 |
| lv_lv | 라트비아어 - 라트비아 |
| lt_lt | 리투아니아어 - 리투아니아 |
| mk_mk | 마케도니아 - 마케도니아 |
| ms_my | 말레이어 - 말레이시아 |
| mr_in | 마라티어 - 인도 |
| no_no | 노르웨이어 - 노르웨이 |
| pl_pl | 폴란드어 - 폴란드 |
| pt_br | 포르투갈어 - 브라질 |
| pt_pt | 포르투갈어 - 포르투갈 |
| pa_in | 펀자비 - 인도 |
| ro_md | 루마니아어 - 몰도바 |
| ro_ro | 루마니아어 - 루마니아 |
| ru_kz | 러시아어 - 카자흐스탄 |
| ru_ru | 러시아어 - 러시아 |
| ru_ua | 러시아어 - 우크라이나 |
| a_in | 산스크리트어 - 인도 |
| sr_ba | 세르비아어 - 보스니아 |
| sr_rs | 세르비아어 - 세르비아 |
| sk_sk | 슬로바키아어 - 슬로바키아 |
| sl_si | 슬로베니아어 - 슬로베니아 |
| es_ar | 스페인어 - 아르헨티나 |
| es_bo | 스페인어 - 볼리비아 |
| es_cl | 스페인어 - 칠레 |
| es_co | 스페인어 - 콜롬비아 |
| es_cr | 스페인어 - 코스타리카 |
| es_do | 스페인어 - 도미니카 공화국 |
| es_ec | 스페인어 - 에콰도르 |
| es_sv | 스페인어 - 엘살바도르 |
| es_gt | 스페인어 - 과테말라 |
| es_hn | 스페인어 - 온두라스 |
| es_mx | 스페인어 - 멕시코 |
| es_ni | 스페인어 - 니카라과 |
| es_pa | 스페인어 - 파나마 |
| es_py | 스페인어 - 파라과이 |
| es_pe | 스페인어 - 페루 |
| es_pr | 스페인어 - 푸에르토리코 |
| es_es | 스페인어 - 스페인 |
| es_uy | 스페인어 - 우루과이 |
| es_ve | 스페인어 - 베네수엘라 |
| sw_ke | 스와힐리 - 케냐 |
| sv_fi | 스웨덴어 - 핀란드 |
| sv_se | 스웨덴어 - 스웨덴 |
| ta_in | 타밀어 - 인도 |
| tt_ru | 타타르 - 러시아어 |
| te_in | 텔레구 - 인도 |
| th_th | 태국 - 태국 |
| tr_cy | 터키어 - 키프로스 |
| tr_tr | 터키 - 터키 |
| uk_ua | 우크라이나어 - 우크레인 |
| ur_in | 우르두 - 인도 |
| ur_pk | 우르두 - 파키스탄 |
| vi_vn | 베트남 - 베트남 |
