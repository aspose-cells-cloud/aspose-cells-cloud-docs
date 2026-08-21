---
title: "Çalışma Sayfasında Grafik Başlığını Sil"
type: docs
url: /tr/charts/delete-chart-title/
aliases: [  /tr/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells, Bulut API, grafik başlığını sil, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API (v4.0) kullanarak bir Excel çalışma sayfasından grafik başlığını nasıl kaldıracağınızı öğrenin. cURL, SDK örnekleri ve hata işleme içerir."
---

Bu REST API, bir grafiğin başlığını siler.

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerek duyar.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                              |
|---------------|----------|--------|---------------------------------------|
| name          | string   | path   | Çalışma kitapası dosyasının adı.      |
| sheetName     | string   | path   | Çalışma sayfasının adı.               |
| chartIndex    | integer  | path   | Grafiğin sıfır tabanlı dizini.        |
| folder        | string   | query  | Çalışma kitabını içeren klasör.       |
| storageName   | string   | query  | Depo adı.                             |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                      | Açıklama                                              |
|-----|----------------------------|-------------------------------------------------------|
| 200 | Tamam                      | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek             | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                   | Geçersiz veya eksik JWT belirteci.                    |
| 413 | Yük Çok Büyük              | Yüklenen dosya boyut sınırını aşıyor.                 |
| 500 | İç Sunucu Hatası           | Beklenmeyen sunucu hatası.                            |

## SDK’lar ile DeleteWorksheetChartTitle API’yi Nasıl Kullanılır

### DeleteWorksheetChartTitle API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, kimlik doğrulama için gereken **Bearer JWT** belirtecini de içeren istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -X DELETE \
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

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}