---
title: "Excel Çalışma Sayfasında Satırı Otomatik Uydur"
second_title: "Belge"
linktitle: "Satır"
type: docs
url: /tr/worksheets/autofit/row/
aliases: [  /tr/autofit-single-row-of-worksheet/ ]
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasında satırı otomatik uydurmanın nasıl kullanılacağını öğrenin. Uç nokta, parametreler, kimlik doğrulama, hata yönetimi, cURL isteği ve SDK örneklerini içerir."
keywords: "satırı otomatik uydur, Aspose.Cells Cloud, Excel API, REST, çalışma sayfası, SDK, elektronik tablo, bulut API"
weight: 30
ArticleTitle: "Aspose.Cells Cloud API Kullanılarak Excel Çalışma Sayfasında Satırı Otomatik Uydurma"
---

Bu REST API, bir Excel çalışma sayfasında **satırı otomatik uydurur**.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **İstek Parametreleri**

| Parametre Adı     | Tür      | Konum  | Açıklama                                                                                                                                                                                      |
| ----------------- | -------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name              | string   | path   | Excel dosyasının adı.                                                                                                                                                                         |
| sheetName         | string   | path   | Çalışma sayfasının adı.                                                                                                                                                                       |
| rowIndex          | integer  | query  | Otomatik uydurulacak satırın sıfır tabanlı indeksi.                                                                                                                                          |
| firstColumn       | integer  | query  | İşleme dahil edilen ilk sütunun indeksi.                                                                                                                                                      |
| lastColumn        | integer  | query  | İşleme dahil edilen son sütunun indeksi.                                                                                                                                                      |
| autoFitterOptions | object   | body   | Otomatik uydurma davranışını kontrol eden nesne (örneğin, birleştirilmiş hücrelerin, metin kaydırmalarının vb. göz önünde bulundurulup oluşturulmayacağını belirler). bkz. [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Otomatik uydurma davranışını kontrol eder"}. |
| folder            | string   | query  | Dosyanın depolandığı klasör.                                                                                                                                                                  |
| storageName       | string   | query  | Depo adı.                                                                                                                                                                                     |

**Örnek `autoFitterOptions` JSON gövdesi**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Varlık Tanımları

| Varlık                | Açıklama                                                                              |
| --------------------- | ------------------------------------------------------------------------------------- |
| `rowIndex`            | Hedef satırın sıfır tabanlı indeksi.                                                  |
| `firstColumn`         | Otomatik uydurma işleminin başlayacağı sütun.                                         |
| `lastColumn`          | Otomatik uydurma işleminin biteceği sütun.                                            |
| `autoFitterOptions`   | Satırın nasıl otomatik uyduğunun etkilenmesini sağlayan isteğe bağlı ayarlar (birleştirilmiş hücreler, metin kaydırma vb.). |

[OpenAPI Spesifikasyonu](/cells/#/Worksheets/PostAutofitWorksheetRow), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API'yi cURL ile nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Alan   | Açıklama                                 |
| ------ | ---------------------------------------- |
| Code   | `200` – istek başarıyla tamamlandı.      |
| Status | `"OK"` – satır başarıyla otomatik uydu.  |

{{< /tab >}}

{{< /tabs >}}

## Hata Yönetimi

API, standart HTTP durum kodlarını döndürür. Bu uç nokta için yaygın hata yanıtları aşağıdaki gibidir:

| HTTP Kodu | Örnek Yük                                                  | Anlam                                                                                 |
| --------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Satır indeksi aralık dışı." }` | Sağlanan `rowIndex` çalışma sayfasında mevcut değildir.                               |
| 401       | `{ "Code": 401, "Message": "Geçersiz veya süresi dolmuş belirteç." }` | Kimlik doğrulama başarısız oldu – JWT belirtecini kontrol edin ve isteğin HTTPS üzerinden yapıldığından emin olun. |
| 404       | `{ "Code": 404, "Message": "Dosya bulunamadı." }`          | Belirtilen Excel dosyası veya çalışma sayfası bulunamıyor.                           |
| 500       | `{ "Code": 500, "Message": "İç sunucu hatası." }`          | Beklenmeyen bir sunucu tarafı sorunu oluştu.                                         |

## Bulut SDK Ailesi

SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakın:** [Sütunu otomatik uydur](/worksheets/autofit/column/), [Satırları otomatik uydur](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).