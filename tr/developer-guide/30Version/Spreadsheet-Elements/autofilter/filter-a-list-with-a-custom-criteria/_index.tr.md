---
title: "Excel çalışma sayfasına özel bir kriter ekleme"
second_title: "Belge"
linktitle: "Özel filtre ekle"
type: docs
url: /tr/autofilter/add-custom-filter/
aliases: [  /tr/filter-a-list-with-a-custom-criteria/ , /tr/autofilter/add-a-custom-filter/ ]
keywords: "Excel, özel filtre, Aspose.Cells Cloud, REST API, otomatik filtre, çalışma sayfası, özel kriter"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına özel bir filtre nasıl ekleyeceğinizi öğrenin. İstek detaylarını, cURL örneğini ve birden fazla programlama dilinde SDK kodu snippet’lerini içerir."
weight: 65
ArticleTitle: "Excel çalışma sayfasına özel bir kriter ekleme – Aspose.Cells Cloud API"
---

Bu REST API, bir listeyi **özel kriter** kullanarak filtreler.

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/tr/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri:

| Parametre Adı   | Tür      | Konum           | Açıklama                                                                     |
|-----------------|----------|-----------------|------------------------------------------------------------------------------|
| name            | string   | path            | Excel dosyasının adı.                                                       |
| sheetName       | string   | path            | Filtrelenecek verileri içeren çalışma sayfasının adı.                       |
| range           | string   | query           | Filtrenin uygulanacağı hücre aralığı (örn. `A1:B1`).                        |
| fieldIndex      | integer  | query           | Filtrenin uygulanacağı sütunun sıfır tabanlı indeksi.                       |
| operatorType1   | string   | query           | İlk karşılaştırma operatörü (örn. `LessOrEqual`, `Equal`).                  |
| criteria1       | string   | query           | İlk filtre değeri veya ifadesi.                                             |
| isAnd           | boolean  | query           | `true` ise, iki kriter **VE** ile birleştirilir; aksi halde **VEYA**.      |
| operatorType2   | string   | query           | İkinci karşılaştırma operatörü (isteğe bağlı).                              |
| criteria2       | string   | query           | İkinci filtre değeri veya ifadesi (isteğe bağlı).                           |
| matchBlanks     | boolean  | query           | `true` ise, boş hücreler filtre sonuçlarına dahil edilir.                   |
| refresh         | boolean  | query           | `true` ise, filtreyi uyguladıktan sonra çalışma sayfasını yenilemeyi zorlar.|
| folder          | string   | query           | Dosyanın bulunduğu depolama dizin yolu.                                     |
| storageName     | string   | query           | Depolama hizmetinin adı.                                                    |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                           |

## PutWorksheetCustomFilter API’yi SDK’larla Nasıl Kullanılır?

### PutWorksheetCustomFilter API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek atacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları yöneterek size proje mantığına odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Standart filtre veya tarih filtresi ekleme gibi diğer AutoFilter işlemleri için, ilgili belgeler sayfalarına bakın.