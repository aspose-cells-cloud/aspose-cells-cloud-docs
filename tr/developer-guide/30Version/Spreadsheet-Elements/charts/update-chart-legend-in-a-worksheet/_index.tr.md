---
title: "Çalışma Sayfasında Grafik Efsanesini Güncelleme"
type: docs
url: /tr/charts/legend/update/
aliases: [  /tr/update-chart-legend-in-a-worksheet/ ]
weight: 160
keywords: "Aspose.Cells, Bulut, Excel, Grafik, Efsane, REST API, Güncelleme, Çalışma Sayfası, cURL, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında grafik efsanesini nasıl güncelleyeceğiniz, cURL istek örnekleri ve birden fazla programlama dili için SDK kod parçacıklarıyla ilgili bilgi."
ArticleTitle: "Çalışma Sayfasında Grafik Efsanesini Güncelleme – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir grafik efsanesini günceller.

**Ön Koşullar:** Bu uç noktayı kullanmak için geçerli bir Aspose Cloud JWT belirteciniz olmalı ve hedef çalışma kitabının desteklenen bir depolama konumunda (varsayılan olarak Aspose Cloud deposu) bulunmalıdır. Çalışma kitabının adı, çalışma sayfasının adı ve grafik dizini doğru olduğundan emin olun.

Bir grafik efsanesi, grafikteki veri serilerinin adlarını ve sembollerini görüntüler. Efsaneyi güncellemek, yazı tipi stili, renk ve gölge gibi görünümünü özelleştirmenizi sağlar.

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                     |
| ------------- | ------ | ----- | -------------------------------------------- |
| name          | string | path  | Çalışma kitabının adı.                       |
| sheetName     | string | path  | Çalışma sayfasının adı.                      |
| chartIndex    | integer| path  | Değiştirilecek grafiğin dizini.             |
| legend        | object | body  | Efsane ayarlarını tanımlayan JSON nesnesi.   |
| folder        | string | query | Çalışma kitabını içeren klasör.              |
| storageName   | string | query | Depolama adı.                                |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL kullanarak Cloud API'yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
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

## Bulut SDK Ailesi

Bir SDK kullanmak geliştirme sürecini hızlandırır. SDK, düşük seviye detayları yöneterek projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}
---