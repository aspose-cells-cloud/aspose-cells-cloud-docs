---
title: "Çalışma Sayfasına Bir Grafik Ekleyin"
type: docs
url: /tr/charts/add/
aliases: [  /tr/add-a-chart-in-a-worksheet/ ]
weight: 20
description: "Aspose.Cells Cloud API v3.0 kullanarak bir Excel çalışma sayfasına grafik nasıl ekleneğini öğrenin. Endpoint, parametreler, cURL örneği ve SDK kod parçacıklarını içerir."
keywords:
  - "Aspose.Cells ile grafik ekle"
  - "Aspose.Cells grafik ekleme API'si"
  - "REST grafik API'si"
  - "Aspose.Cells SDK örnekleri"
ArticleTitle: "Çalışma Sayfasına Bir Grafik Ekleyin – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir çalışma sayfasına yeni bir grafik ekler.

**Ön Gereksinimler**  
Bu işlemi çağırmadan önce geçerli bir JWT erişim belirteci edinin ve hedef çalışma kitabının belirtilen klasörde veya depolama konumunda saklandığından emin olun.

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı         | Tür      | Konum  | Açıklama                                                                                                                                                                                   |
| --------------------- | -------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**              | string   | path   | Çalışma kitabı adı.                                                                                                                                                                        |
| **sheetName**         | string   | path   | Çalışma sayfası adı.                                                                                                                                                                       |
| **chartType**         | string   | query  | Grafik türü (grafik kaynağındaki **Type** özelliğine bakın). Desteklenen grafik türleri: **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar** vb.     |
| **upperLeftRow**      | integer  | query  | Grafik alanının sol üst köşe satır indeksi (0‑tabanlı).                                                                                                                                   |
| **upperLeftColumn**   | integer  | query  | Grafik alanının sol üst köşe sütun indeksi (0‑tabanlı).                                                                                                                                   |
| **lowerRightRow**     | integer  | query  | Grafik alanının sağ alt köşe satır indeksi (0‑tabanlı).                                                                                                                                   |
| **lowerRightColumn**  | integer  | query  | Grafik alanının sağ alt köşe sütun indeksi (0‑tabanlı).                                                                                                                                   |
| **area**              | string   | query  | Grafikte kullanılacak verilerin aralığı (örn. `A1:B5`).                                                                                                                                   |
| **isVertical**        | boolean  | query  | Grafik yönlendirmesinin dikey olup olmadığını belirtir.                                                                                                                                    |
| **categoryData**      | string   | query  | Kategori eksenindeki verilerin aralığı (örn. `D1:E10`).                                                                                                                                    |
| **isAutoGetSerialName** | boolean | query | **true** ise serilerin adları otomatik oluşturulur.                                                                                                                                        |
| **title**             | string   | query  | Grafik başlığı.                                                                                                                                                                            |
| **folder**            | string   | query  | Çalışma kitabının bulunduğu klasör.                                                                                                                                                        |
| **storageName**       | string   | query  | Depolama adı.                                                                                                                                                                              |
| **dataLabels**        | boolean  | query  | **true** olduğunda veri etiketlerini gösterir.                                                                                                                                            |
| **dataLabelsPosition** | string  | query  | Veri etiketlerinin konumu (örn. `Above`).                                                                                                                                                  |
| **pivotTableSheet**   | string   | query  | Pivot tablonun bulunduğu sayfanın adı.                                                                                                                                                     |
| **pivotTableName**    | string   | query  | Pivot tablonun adı.                                                                                                                                                                        |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                         |
|-----|-----------------------------|------------------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                              |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                           |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                                      |

## PutWorksheetAddChart API’yi SDK’larla Nasıl Kullanılır?

### PutWorksheetAddChart API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Bu işlem için istek gövdesine gerek yoktur
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)’na bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl atılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}