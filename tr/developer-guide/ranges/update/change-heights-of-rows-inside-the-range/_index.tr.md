---
title: Aralık içindeki satırların yüksekliğini ayarlayın
second_title: Aspose.Cells Cloud Documen
linktitle: sıra yüksekliği
type: docs
url: /tr/ranges/update/row-height/
aliases: [/change-heights-of-rows-inside-the-range/]
keywords: Set row height for range on an Excel workshee
description: Aspose.Cells Cloud REST API, bir Excel çalışma sayfasında aralık için satır yüksekliğini ayarlamayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 76
---
Bu REST API, bir Excel çalışma sayfasında aralığın satır yüksekliğini ayarlamayı gösterir.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| sayfaAdı| sicim| yol||
| değer| sayı| sorgu||
| menzil|| vücut||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"ColumnCount\": 7, \"ColumnWidth\": 19, \"FirstColumn\": 0, \"FirstRow\": 9, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 1, \"RowHeight\": 15, \"Worksheet\": \"Sheet1\"}"
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
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "18574f2f44071ac9d80be95568c193ff" >}}

{{< /tab >}}

{{< /tabs >}}
