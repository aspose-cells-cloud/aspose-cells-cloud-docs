﻿---
title: Akıllı işaretleyici şablonuyla Excel raporu nasıl oluşturulur
second_title: Aspose.Cells Cloud Documen
linktitle: AkıllıMarke
type: docs
url: /tr/build-report-with-smart-marker/
aliases: [/create-excel-workbook-from-a-smartmarker-template/,/workbook/smartmarker/,/workbook/create/smartmarker/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API akıllı işaretleyici şablonuyla Excel çalışma kitabı nasıl oluşturulur. SDK çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 40
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Akıllı işaretleyici şablonuyla Excel çalışma kitabı nasıl oluşturulur
---
Bu REST API, `smart marker` ile `workbook`'in oluşturulmasını belirtir.

**Sorgu Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|xmlDosyası|sicim||
|çıkış yolu|sicim||
|dosya|sicim|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim|Depolama adı.|

**İstek Gövde Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|xmlDosyası|dosya||

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/{isim}/akıllıişaretleyici|POSTALAMAK|SmartMarker şablon dosyasından yeni bir Excel Çalışma Kitabı oluşturun|[PostWorkbookGetSmartMarkerResult](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web servislerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?xmlFile=Sample_SmartMarker_Data.xml" -H "accept: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the processing result in content.

}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}
