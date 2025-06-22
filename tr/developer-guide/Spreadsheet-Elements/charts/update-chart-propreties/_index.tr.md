---
title: Grafik Özelliklerini Güncelle
type: docs
url: /tr/charts/propreties/update/
aliases: [/update-chart-propreties/]
weight: 160
kwords: Excel, Office Bulut, REST API, E-Tablo, PDF, CSV, Json, Markdown, Grafik Özelliklerini Güncelle
---
Bu REST API, grafik özelliklerinin güncellendiğini gösterir
 
## RSETAPI
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
 
```
 İstek parametreleri şunlardır:
 
| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| sayfaAdı| sicim| yol||
| grafikIndeksi| tam sayı| yol||
| çizelge|| vücut||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|

<br/>
 
 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" 
-d '{"Type": "line"}'
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Code":200,
    
    "Status":"OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}
