---
title: Pivot tablo için stil güncellemesi
second_title: Documen
linktitle: Tümünü biçimlendir
type: docs
url: /tr/pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: Update all cell style for a pivot table
description: Aspose.Cells Cloud REST API, pivot tablolar için tüm hücre stillerinin güncellenmesini destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Pivot tablo için stil güncellemesi
---
Bu REST API, pivot tablo için `update` stilini gösterir
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
 
```
 İstek parametreleri şunlardır:
 
| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfasının adı.|
| pivotTableIndex| tam sayı| yol| Pivot tablo dizini|
| stil|| vücut| İstek gövdesinde stil dto.|
| Yeniden Hesaplamayaihtiyacın Var| Boolean| sorgu|YANLIŞ|
| dosya| sicim| sorgu| Belgenin klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile API Cloud'a nasıl çağrı yapılacağını göstermektedir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'
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
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
