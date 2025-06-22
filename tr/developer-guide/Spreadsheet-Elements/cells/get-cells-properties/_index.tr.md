---
title: Cells Mülkiyetini Alın
type: docs
url: /tr/get-cells-properties/
weight: 130
kwords: Excel, Office Bulut, REST API, E-Tablo, PDF, CSV, Json, Markdown, Cells Özelliklerini Alın
---
Bu REST API, Excel dosyasında `get a specific cell`'in nasıl yapılacağını gösterir.

## RSETAPI

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma kağıdı adı.|
| hücreVeyaYöntemAdı| sicim| yol|Hücrenin veya metodun adı. (Metot adı değeri : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn ve cellName.)|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### **Bulut SDK Ailesi**

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **Belirli hücre nasıl alınır**

- [Bir Çalışma Sayfasından Hücre Verilerini Alın](/cells/tr/get-cell-data-from-a-worksheet/)
- [Excel'den İlk Cep Telefonu Çalışma Sayfasını Alın](/cells/tr/get-first-cell-from-excel-worksheet/)
- [Excel Çalışma Sayfasının Son Hücresini Alın](/cells/tr/get-last-cell-of-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxRow'u Alın](/cells/tr/get-maxrow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxDataRow'u Alın](/cells/tr/get-maxdatarow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxColumn'u Alın](/cells/tr/get-maxcolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxDataColumn'u Alın](/cells/tr/get-maxdatacolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinRow'u Alın](/cells/tr/get-minrow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinDataRow'u Alın](/cells/tr/get-mindatarow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinColumn'u Alın](/cells/tr/get-mincolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinDataColumn'u Alın](/cells/tr/get-mindatacolumn-from-excel-worksheet/)
