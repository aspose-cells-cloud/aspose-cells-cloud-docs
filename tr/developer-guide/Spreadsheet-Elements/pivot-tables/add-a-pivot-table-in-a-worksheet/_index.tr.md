---
title: Excel çalışma sayfasına pivot tablo ekleyin
second_title: Aspose.Cells Cloud Documen
linktitle: Eklemek
type: docs
url: /tr/pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: Add a pivot table in an Excel worksheet
description: Aspose.Cells Cloud REST API, Excel çalışma sayfasına pivot tablo eklemeyi destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Excel çalışma sayfasına pivot tablo ekleme
---
Bu REST API, `add`'e bir pivot tablonun çalışma sayfasına dönüştürüldüğünü gösterir.
 
## RSETAPI
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
 
```
 İstek parametreleri şunlardır:
 
| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfasının adı.|
| rica etmek|| vücut| İstek gövdesinde CreatePivotTableRequest dto.|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
| kaynakVeri| sicim| sorgu| Yeni PivotTable önbelleğine ait veriler.|
|hedefHücreAdı| sicim| sorgu| PivotTable raporunun hedef aralığının sol üst köşesindeki hücre.|
| tabloAdı| sicim| sorgu| Yeni PivotTable raporunun adı.|
| AynıKaynağıkullan| Boolean| sorgu| Başka bir mevcut pivot tablonun bu veri kaynağını kullandığında aynı veri kaynağının kullanılıp kullanılmadığını belirtir. Özellik doğruysa, bellek tasarrufu sağlar.|
 
 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını göstermektedir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v  "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables"
-X PUT \
-d '{"Name":"MyPivot", "SourceData":"A5:E10", "DestCellName":"H20", "UseSameSource":true, "PivotFieldRows":[1], "PivotFieldColumns":[1], "PivotFieldData ":[1]}'\
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}
