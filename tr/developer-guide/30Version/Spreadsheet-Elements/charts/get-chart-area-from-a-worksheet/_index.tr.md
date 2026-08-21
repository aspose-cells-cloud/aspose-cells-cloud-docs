---
title: "Çalışma Kitabından Grafik Alanını Alın"
type: docs
url: /tr/charts/area/get/
aliases: [  /tr/get-chart-area-from-a-worksheet/ ]
weight: 60
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "ChartArea"
  - "Worksheet"
  - "cURL"
  - "SDK"
  - "GetChartArea"
description: "Aspose.Cells Cloud REST API ile bir çalışma sayfasından grafik alanı bilgilerini nasıl alacağınızı, cURL ve birden fazla SDK için örneklerle öğrenin."
ArticleTitle: "Çalışma Kitabından Grafik Alanını Alın - Aspose.Cells Cloud API"
---

Bu REST API, grafik alanı bilgilerini döndürür.

**Önkoşullar:** Bu uç noktayı çağırmak için geçerli bir JWT erişim belirteciniz, hedef çalışma kitabının Aspose Cloud depolama alanına yüklenmiş olması ve dosya formatının Aspose.Cells tarafından desteklenmesi gerekir.

**Arka plan:** Bir grafik alanı, başlıkları, efsaneleri (legend) ve çizim alanını da içeren Excel grafiğinin en dıştaki sınırlayıcı kutusunu tanımlar. Özelliklerini almak, düzeni ve stilini programatik olarak ayarlamanıza olanak tanır.

## GetChartArea API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek parametreleri

| Parametre Adı  | Tür     | Konum   | Açıklama                                       |
| -------------- | ------- | ------- | ---------------------------------------------- |
| name           | string  | path    | Çalışma kitabının dosya adı.                   |
| sheetName      | string  | path    | Grafiği içeren çalışma sayfasının adı.         |
| chartIndex     | integer | path    | Grafiğin sıfır tabanlı indeksi.                |
| folder         | string  | query   | Çalışma kitabının bulunduğu klasör.            |
| storageName    | string  | query   | Depolama hizmetinin adı.                       |

### **Yanıt**

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                 |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.              |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                         |

## SDK’lar ile GetChartArea API Nasıl Kullanılır

### GetChartArea API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/ChartArea/GetChartArea" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartArea-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartArea-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_info-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartArea-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartArea-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "e00e3bbfdf94f400244f1974c3488036" >}}
{{< /tab >}}

{{< /tabs >}}

**Genel HTTP isteği (örneğin, fetch kullanarak):**

```javascript
fetch('https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'Authorization': 'Bearer <jwt token>'
  }
})
  .then(response => response.json())
  .then(data => console.log(data));
```