---
title: "Çalışma Kitabında Grafik Açıklamasını Göster"
type: docs
url: /tr/charts/legend/show/
aliases: [  /tr/show-chart-legend-in-a-worksheet/ ]
weight: 100
keywords: "Aspose.Cells Cloud, grafik açıklama API'si, Excel grafik açıklaması, REST PUT grafik açıklaması, Aspose API v3.0"
description: "Aspose.Cells Cloud REST API'si (v3.0) kullanarak bir Excel çalışma kitabında bir çalışma sayfasındaki bir grafikte açıklama kutusunu nasıl göstereceğinizi öğrenin. Uç nokta detayları, parametreler, bir cURL örneği ve SDK kod parçacıkları içerir."
---

Bu REST API, bir Excel çalışma kitabındaki bir çalışma sayfasında bulunan bir grafikte veri serilerini tanımlayan açıklama kutusunu (**legend**) göstermenizi sağlar.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### İstek parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                      |
| ------------- | ------ | ----- | --------------------------------------------- |
| name          | string | path  | Çalışma kitabının dosya adı.                   |
| sheetName     | string | path  | Grafik içeren çalışma sayfasının adı.          |
| chartIndex    | integer| path  | Grafikin sıfır tabanlı indeksi.               |
| folder        | string | query | Çalışma kitabının bulunduğu klasör.            |
| storageName   | string | query | Depolama hizmetinin adı.                       |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Kimlik doğrulama, **Authorization** başlığına sağlanan Bearer JWT jetonu ile gerçekleştirilir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

API aşağıdaki HTTP durum kodlarından birini döndürebilir:

- **200 OK** – Açıklama başarıyla gösterildi.
- **400 Bad Request** – Geçersiz parametreler.
- **401 Unauthorized** – Kimlik doğrulama başarısız oldu.
- **404 Not Found** – Belirtilen çalışma kitabı, çalışma sayfası veya grafik bulunamadı.
- **500 Internal Server Error** – Beklenmeyen bir sunucu hatası oluştu.

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Kullanımı

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}