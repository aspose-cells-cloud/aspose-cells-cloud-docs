---
title: Excel çalışma sayfasının bir sayfasını dışa aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: Sayfa
type: docs
url: /tr/worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: Get page to different format content from an Excel worksheet
description: Aspose.Cells Cloud REST API, bir Excel Çalışma Sayfasından farklı biçim içeriğine sayfa almayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 240
---
[/cells/{name}/worksheets/{sheetName} GET](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API, çalışma sayfasının sivri uçlu sayfasını format dosyası türlerine dönüştürmenizi sağlar. Desteklenen formatlar:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV'ler](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [ÖTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/),[GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/),[TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [SAYILAR](https://docs.fileformat.com/spreadsheet/numbers/), [YEMEKLER](https://docs.fileformat.com/spreadsheet/fods/).


## DİNLENME API

 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorkshee) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Converted Image 

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="7" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Ruby" tabName6="PHP" tabName7="Node.js" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "c26975dacdc050fccd6d003b487b39d9" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a555abf44e31590c6ae3260c1bcd3066" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "3c7008ae0d54a40cd0c92a1273bfd7d5" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "bd5c03f09104b9d59941d6583117dce2" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "64a33901d4f45c9edf31ab83e816981e" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "daa94750c751cb595de0b8a357c051ed" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "a4bb7786b0d6bc98d8b51da49a687cf5" >}}

{{< /tab >}}

{{< /tabs >}}
