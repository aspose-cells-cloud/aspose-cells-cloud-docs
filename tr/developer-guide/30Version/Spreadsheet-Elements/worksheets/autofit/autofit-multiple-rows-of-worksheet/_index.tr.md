---
title: "Bir Excel Çalışma Sayfasında Birden Fazla Satırı Otomatik Uygun Hale Getirme"
second_title: "Belge"
linktitle: "Satırlar"
type: docs
url: /tr/worksheets/autofit/rows/
aliases: [  /tr/autofit-multiple-rows-of-worksheet/ ]
keywords: "satırları otomatik uygun hale getirme, Excel, Aspose.Cells Cloud, REST API, çalışma sayfası, elektronik tablo"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel çalışma sayfasında birden fazla satırı otomatik uygun hale getirmeyi öğrenin. İstek sözdizimi, parametreler, cURL örneği, SDK kod parçacıkları ve hata işleme içerir."
weight: 40
ArticleTitle: "Bir Excel Çalışma Sayfasında Birden Fazla Satırı Otomatik Uygun Hale Getirme – Aspose.Cells Cloud API Belgelendirmesi"
---

Bu REST API, bir Excel çalışma sayfasındaki satırların yüksekliğini otomatik olarak ayarlar.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **İstek parametreleri**

| Parametre Adı         | Tür      | Konum | Açıklama                                                                                                                              | Gerekli |
| --------------------- | -------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| **name**              | string   | path  | Excel dosyasının adı.                                                                                                                 | ✔       |
| **sheetName**         | string   | path  | Çalışma sayfasının adı.                                                                                                               | ✔       |
| **autoFitterOptions** | object   | body  | Satırların nasıl otomatik uygun hale getirileceğini denetleyen seçenekler (örneğin, gizli satırların yoksayılması). Aşağıdaki kısa alan açıklamasına bakın. | ✖       |
| **startRow**          | integer  | query | Otomatik uygun hale getirilecek ilk satır (1 tabanlı indeks).                                                                        | ✔       |
| **endRow**            | integer  | query | Otomatik uygun hale getirilecek son satır (dahil).                                                                                   | ✔       |
| **onlyAuto**          | boolean  | query | `true` ise, API yalnızca yüksekliği Excel tarafından otomatik olarak hesaplanan satırları ayarlar. `false` ise tam bir otomatik uygun hale getirme yapılır. | ✖       |
| **folder**            | string   | query | Belgeyi içeren klasör.                                                                                                                | ✖       |
| **storageName**       | string   | query | Depolama hizmetinin adı.                                                                                                              | ✖       |

**autoFitterOptions** alanları (tümü isteğe bağlıdır):

- `AutoFitMergedCells` _(boolean)_ – `true` ise, satır yüksekliği hesaplanırken birleştirilmiş hücreler dikkate alınır.
- `IgnoreHidden` _(boolean)_ – `true` ise, otomatik uygun hale getirme işlemi sırasında gizli satırlar yoksayılır.
- `OnlyAuto` _(boolean)_ – Sorgu parametresi `onlyAuto` ile aynı işlevi görür; ayarlandığında, sorgu değerini geçersiz kılar.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows), herkese açık bir erişilebilir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Typical error responses include:

- **400 Bad Request** – Geçersiz parametre değerleri veya bozuk JSON gövdesi.
- **401 Unauthorized** – Eksik veya geçersiz JWT belirteci.
- **404 Not Found** – Belirtilen dosya veya çalışma sayfası mevcut değil.
- **500 Internal Server Error** – Beklenmeyen bir sunucu hatası oluştu.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Sü 필터 başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ortaklığı

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları işler böylece projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}