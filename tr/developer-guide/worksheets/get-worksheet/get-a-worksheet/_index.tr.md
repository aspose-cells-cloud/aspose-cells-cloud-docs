﻿---
title: Excel çalışma sayfasından çalışma sayfasını alın
second_title: Aspose.Cells Cloud Documen
linktitle: Çalışma Sayfası
type: docs
url: /tr/worksheets/get-worksheet/
keywords: Get worksheet to different format from an Excel worksheet
description: Aspose.Cells Cloud REST API, çalışma sayfasının Excel Çalışma Sayfasından farklı bir formata alınmasını destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 10
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Excel çalışma sayfasından çalışma sayfası alın
---
Bu REST API, `get worksheet description` veya `export worksheet to kinds of format file`'i gösterir.
 

 Formatları dışa aktarabilirsiniz:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DMF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/),[GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/),[TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMARALAR](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).


## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| biçim| sicim| sorgu|Dışa aktarılan dosya formatı.|
| dikeyÇözünürlük| tamsayı| sorgu| Oluşturulan görüntüler için dikey çözünürlüğü inç başına nokta cinsinden ayarlar.|
| yatayÇözünürlük| tamsayı| sorgu| Oluşturulan görüntüler için yatay çözünürlüğü inç başına nokta cinsinden ayarlar.|
| alan| sicim| sorgu| İhraç edilen alan.|
| sayfaIndex| tamsayı| sorgu| Dışa aktarılan sayfa dizini.|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash

{
stream
} 

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-ConvertWorksheetToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-ConvertWorksheetToImage-convert-worksheet-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-GetWorkSheetWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-read_worksheet_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertWorkSheetToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-ConvertWorksheetToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-ConvertWorksheetToImage-convert-worksheet-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-ConvertWorksheetToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b830e952db97940189ac7867f8ee37dc" >}}

{{< /tab >}}

{{< /tabs >}}
