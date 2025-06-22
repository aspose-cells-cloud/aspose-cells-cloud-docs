---
title: Tabloyu pivot tabloya dönüştür
second_title: Aspose.Cells Cloud Documen
linktitle: Dönüştürmek
type: docs
url: /tr/pivot-tables/convert-table-to-pivottable/
aliases: [/create-a-pivottable-with-table/,/create-new-pivot-table-with-list-object-as-source-data/]
keywords: Create a pivot table with list object. Convert list object to pivot table
description: Aspose.Cells Cloud REST API liste nesnesiyle pivot tablo oluşturmayı destekler. SDK çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 60
kwords: Excel, Office Bulut, REST API, E-tablo, PDF, CSV, Json, Markdown, Tabloyu pivot tabloya dönüştür
---
Bu REST API, liste nesnesi ile `pivottable` oluşturulmasını belirtir.
 
## RSETAPI
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
 
```
 İstek parametreleri şunlardır:
 
| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| sayfaAdı| sicim| yol||
| listeNesneİndeksi| tam sayı| yol||
| destsheetName| sicim| sorgu||
| rica etmek|| vücut||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını göstermektedir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api-qa.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \ \
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
 
 
