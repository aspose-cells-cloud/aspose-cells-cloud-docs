---
title: "Excel Çalışma Sayfasında Grafik Efsanesini Gizle – Aspose.Cells Cloud API"
type: docs
url: /tr/charts/legend/hide/
aliases: [  /tr/hide-chart-legend-in-a-worksheet/ ]
weight: 110
keywords: "Aspose.Cells, Excel, grafik efsanesini gizle, REST API, Bulut SDK'sı, grafik efsanesi"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında grafik efsanesini nasıl gizleyeceğinizi öğrenin. HTTPS uç noktası, gerekli kimlik doğrulama, istek sözdizimi, yanıt ayrıntıları, hata işleme ve SDK örnekleri içerir."
---

Bu REST API, bir grafikteki efsaneyi gizler. Bir **grafik efsanesi**, grafikte çizilen veri serilerini tanımlayan kutudur.

API, geçerli bir Aspose Cloud JWT jetonu gerektirir; çalışma kitabının Aspose Cloud deposuna yüklenmiş olması gerekir ve kullanılan API sürümü **v3.0**'dır.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT jeton tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### İstek parametreleri

| Parametre Adı   | Tür     | Konum | Açıklama                          |
| ---------------- | ------- | ------ | --------------------------------- |
| **name**         | string  | path   | Çalışma kitabı adı.               |
| **sheetName**    | string  | path   | Çalışma sayfası adı.              |
| **chartIndex**   | integer | path   | Grafik indeksi.                   |
| **folder**       | string  | query  | Çalışma kitabı klasörü (isteğe bağlı). |
| **storageName**  | string  | query  | Depo adı (isteğe bağlı).          |

[OpenAPI Specifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend), bu genel olarak erişilebilir programlama arayüzünü tanımlar.

API'yi kolayca çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, _Sample_Test_Book.xls_ dosyasındaki 0 numaralı grafik için efsaneyi gizleyen bir isteği göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

## Yanıtlar

| HTTP Durumu                   | Açıklama                                             | Örnek JSON                                                     |
| ----------------------------- | ---------------------------------------------------- | -------------------------------------------------------------- |
| **200 OK**                    | Efsane başarıyla gizlendi.                           | `{ "Code": 200, "Status": "OK" }`                              |
| **401 Unauthorized**          | Eksik veya geçersiz JWT jetonu.                      | `{ "Code": 401, "Message": "Invalid access token." }`          |
| **404 Not Found**             | Çalışma kitabı, çalışma sayfası veya grafik yoktur.  | `{ "Code": 404, "Message": "Chart not found." }`               |
| **500 Internal Server Error** | Beklenmeyen sunucu hatası.                           | `{ "Code": 500, "Message": "An unexpected error occurred." }`  |

## SSS

**S:** _Aspose.Cells Cloud kullanarak bir grafik efsanesini nasıl gizlerim?_  
**C:** Geçerli bir JWT jetonunu `Authorization` başlığında taşıyıp `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` adresine bir `DELETE` isteği gönderin. `200 OK` yanıtı başarı anlamına gelir.

**S:** _Grafik Efsanesini Gizle API'si için hangi kimlik doğrulama gerekir?_  
**C:** `Authorization: Bearer <jwt token>` başlığını ekleyin. Jetonu Aspose Cloud OAuth akışı aracılığıyla edinin.

**S:** _Grafik indeksi geçersizse hangi hata yanıtı alırım?_  
**C:** Servis, `Code: 404` içeren ve eksik grafikle ilgili bir mesaj barındıran JSON gövdesiyle `404 Not Found` döndürür.

**S:** _HTTPS yerine HTTP kullanabilir miyim?_  
**C:** Hayır. Tüm Aspose Cloud uç noktaları güvenlik nedeniyle HTTPS gerektirir.

## Bulut SDK Ailesi
SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub Deposu'na](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web servislerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Yakında gelecek** – Swift SDK örneği kısa sürede eklenecektir.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Excel Çalışma Sayfasında Grafik Efsanesini Gizle – Aspose.Cells Cloud API",
  "description": "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında grafik efsanesini gizlemenin adım adım rehberi. HTTPS uç noktası, kimlik doğrulama, istek sözdizimi, yanıt ayrıntıları, hata işleme ve SDK örnekleri içerir.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Ana Sayfa", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Grafik Efsanesini Gizle", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Aspose.Cells Cloud API kullanarak grafik efsanesini gizleme"
}
</script>