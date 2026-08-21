---
title: "Aspose.Cells Cloud API – Excel Çalışma Sayfasında Grafik Başlığı Ayarlama"
type: docs
url: /tr/chart/title/add/
aliases: [  /tr/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, grafik başlığı API'si, Excel grafik başlığı, REST API, SDK örnekleri"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında grafik başlığı nasıl eklenir veya güncellenir öğrenin. cURL, SDK örnekleri, gerekli parametreler, kimlik doğrulama adımları ve hata işleme içerir."
---

Mevcut bir başlığı görünür yapar veya yeni bir grafik başlığı ekler.

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum  | Açıklama                             |
| -------------- | ------- | ------ | ------------------------------------ |
| name           | string  | path   | Çalışma kitabının adı.               |
| sheetName      | string  | path   | Çalışma sayfasının adı.              |
| chartIndex     | integer | path   | Grafikin indeksi.                    |
| title          | string  | body   | Grafik başlığının metni.             |
| folder         | string  | query  | Çalışma kitabını içeren klasör.      |
| storageName    | string  | query  | Depo adı.                            |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Satış Grafiği"}' \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Hata Yanıtları**

| HTTP Kodu | Örnek Yük (Payload)                                                                   | Açıklama                                             |
| --------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| 400       | `{ "Code": "400", "Message": "Geçersiz istek yükü." }`                               | İstek gövdesi bozuk veya gerekli alanlar eksik.     |
| 401       | `{ "Code": "401", "Message": "Kimlik doğrulama başarısız. Geçersiz veya süresi dolmuş JWT belirteci." }` | Taşıyıcı (bearer) belirteç eksik, geçersiz veya süresi dolmuş. |
| 404       | `{ "Code": "404", "Message": "Çalışma kitabı, çalışma sayfası veya grafik bulunamadı." }` | Belirtilen kaynak mevcut değil.                     |
| 500       | `{ "Code": "500", "Message": "Sunucu iç hatası." }`                                   | Sunucuda beklenmeyen bir hata oluştu.               |

## Bulut SDK Ailesi

SDK kullanmak, geliştirmenin en hızlı yoludur. SDK, düşük seviye ayrıntıları soyutlayarak proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerinin çeşitli SDK’lar kullanılarak nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}