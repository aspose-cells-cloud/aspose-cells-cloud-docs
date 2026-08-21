---
title: "Excel Çalışma Sayfasına Renk Filtresi Ekleme"
second_title: "Belge"
linktitle: "Renk filtresi ekle"
type: docs
url: /tr/autofilter/add-color-filter/
aliases: [  /tr/filter-a-list-using-a-color-filter/ , /tr/autofilter/add-a-color-filter/ ]
keywords: "Excel, renk filtresi, Aspose.Cells Cloud, REST API, otomatik filtre, JWT kimlik doğrulama"
description: "Aspose.Cells Cloud API ile bir Excel çalışma sayfasına renk filtresi nasıl uygulanacağını öğrenin. Uç nokta, parametreler, cURL örneği, hata yönetimi ve SDK örneklerini içerir."
weight: 65
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasına Renk Filtresi Ekleme"
---

Aspose.Cells Cloud API kullanarak bir Excel çalışma sayfasına renk filtresi nasıl ekleyeceğinizi öğrenin. Bu kılavuz, gerekli uç noktayı, parametreleri, kimlik doğrulama ön koşullarını, örnek cURL isteğini, SDK örneklerini ve yanıt yönetimini kapsar.

Bu REST API, bir Excel çalışma sayfasına bir **renk filtresi** ekler.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri:


| Parametre Adı | Tür      | Konum  | Açıklama                                                                 |
|---------------|----------|--------|-----------------------------------------------------------------------------|
| name          | string   | path   | Excel dosyasının adı.                                                 |
| sheetName     | string   | path   | Filtrelenecek verileri içeren çalışma sayfasının adı.           |
| range         | string   | query  | Filtrenin uygulanacağı hücre aralığı (örneğin, `A1:B10`).            |
| fieldIndex    | integer  | query  | Renk filtresinin uygulanacağı sütunun sıfır tabanlı indeksi.       |
| colorFilter   | object   | body   | Filtrelenecek ön plan ve arka plan renklerini tanımlayan JSON nesnesi.   |
| matchBlanks   | boolean  | query  | Boş hücreler içeren satırların filtre sonuçlarına dahil edilip edilmeyeceği.   |
| refresh       | boolean  | query  | `true` ise, filtre uygulandıktan sonra çalışma sayfası yenilenir.           |
| folder        | string   | query  | Excel dosyasının bulunduğu depolama klasörü.                      |
| storageName   | string   | query  | Depolama hizmetinin adı (örneğin, Aspose Cloud Storage).              |

**`colorFilter` JSON şeması**

| Özellik           | Tür    | Açıklama                                                                    | Zorunlu |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | Filtre deseni (örneğin, `"Solid"`).                                             | Evet      |
| ForegroundColor   | object | Ön plan rengini tanımlar. `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` ve `Type` gibi alt özellikler içerir. | Hayır |
| BackgroundColor   | object | Arka plan rengini tanımlar. `ForegroundColor` ile aynı alt özelliklere sahiptir.      | Hayır |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşar. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |
## PutWorksheetColorFilter API’sini SDK’larla Nasıl Kullanılır

### PutWorksheetColorFilter API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye ayrıntıları soyutlayarak proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'nu kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:** [Özel filtre ekleme](https://docs.aspose.cloud/cells/tr/autofilter/add-custom-filter/), [Tarih filtresi ekleme](https://docs.aspose.cloud/cells/tr/autofilter/add-date-filter/), [Otomatik filtre kaldırma](https://docs.aspose.cloud/cells/tr/autofilter/remove-auto-filter/).