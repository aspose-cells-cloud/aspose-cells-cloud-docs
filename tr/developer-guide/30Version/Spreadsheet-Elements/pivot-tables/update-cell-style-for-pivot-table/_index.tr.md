---
title: "Pivot Tablosu İçin Hücre Stilini Güncelle"
second_title: "Belge"
linktype: Biçimlendirme
type: docs
url: /tr/pivot-tables/format/
aliases: [  /tr/update-cell-style-for-pivot-table/ ]
keywords: "Aspose.Cells Cloud, pivot tablo stili, hücre stili güncelleme API'si, REST API, Excel API'si, elektronik tablo biçimlendirme, bulut SDK'sı, hücre stili, pivot tablo"
description: "Aspose.Cells Cloud pivot tablosunda bir hücrenin stilini REST API aracılığıyla nasıl güncelleyeceğinizi öğrenin. Uç nokta, parametreler, kimlik doğrulama, cURL örneği, Go SDK kod parçacığı ve SEO optimizeilmiş rehberlik içerir."
weight: 90
ArticleTitle: "Pivot Tablosu İçin Hücre Stilini Güncelle - Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir pivot tablodaki bir hücrenin **stilini** günceller.

**Önkoşullar / Kimlik Doğrulama**  
Bu uç noktayı çağırmak için geçerli bir Aspose Cloud JWT erişim belirteciniz olmalıdır. Belirteci [Kimlik Doğrulama Kılavuzu](/authentication/)’nda açıklanan OAuth 2.0 akışı aracılığıyla edinin. Belirteci istek başlığında şu şekilde ekleyin:

```http
Authorization: Bearer <jwt token>
```

JWT belirteci, tüm Aspose.Cells Cloud API çağrıları için gereklidir.

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum | Açıklama                                                                                                |
| --------------- | -------- | ----- | --------------------------------------------------------------------------------------------------------- |
| name            | string   | path  | Belge adı (zorunludur).                                                                                   |
| sheetName       | string   | path  | Çalışma sayfası adı (zorunludur).                                                                         |
| pivotTableIndex | integer  | path  | Pivot tablo dizini (zorunludur).                                                                          |
| column          | integer  | query | Biçimlendirilecek hücrenin sıfır tabanlı sütun dizini (zorunludur).                                        |
| row             | integer  | query | Biçimlendirilecek hücrenin sıfır tabanlı satır dizini (zorunludur).                                       |
| style           | object   | body  | Yeni hücre stilini tanımlayan Style DTO (veri aktarım nesnesi).                                           |
| needReCalculate | boolean  | query | Stil uygulandıktan sonra pivot tablonun yeniden hesaplanıp hesaplanmayacağını belirtir. Varsayılan değer **false**’dır. |
| folder          | string   | query | Belgenin saklandığı klasör (isteğe bağlı).                                                               |
| storageName     | string   | query | Depo adı (isteğe bağlı).                                                                                 |
| Method          | string   | N/A   | İstek için kullanılan HTTP yöntemi (**POST**).                                                           |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt**  
Başarılı durumda hizmet, stilin uygulandığını göstermek için boş gövdeli HTTP 200 döndürür. Hata durumunda ise bir JSON yükü, hata kodu ve mesajı ile birlikte döndürülür.

| HTTP Durum Kodu | Açıklama                                             |
|-----------------|------------------------------------------------------|
| 200             | Stil başarıyla uygulandı.                            |
| 400             | Geçersiz istek – örneğin, geçersiz sütun/satır dizini. |
| 401             | Yetkisiz erişim – eksik veya geçersiz JWT belirteci. |
| 404             | Bulunamadı – belirtilen belge, çalışma sayfası veya pivot tablo mevcut değil. |
| 500             | Sunucu iç hatası – beklenmeyen durum.                |

Yanıt gövdesi başarı durumunda boş olur.

Daha fazla bilgi için **Get Pivot Table** API dokümantasyonuna bakın.

## Bulut SDK Geliştirme Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örneği, **Go** SDK kullanarak Aspose.Cells web servislerini nasıl çağırdığınızı göstermektedir:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Pivot Tablosu İçin Hücre Stilini Güncelle",
  "description": "Aspose.Cells Cloud pivot tablosunda belirli bir hücrenin stilini REST API kullanarak güncelleme rehberi.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, pivot tablo, hücre stili, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>