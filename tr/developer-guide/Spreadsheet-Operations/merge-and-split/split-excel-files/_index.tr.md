---
title: Excel çalışma kitabını çoklu dosyaya böl
second_title: Aspose.Cells Cloud Documen
linktitle: Excel numaralı telefonu bölün
type: docs
url: /tr/split-multi-excel-files/
aliases: [ /split/multi-files/]
keywords: Split an Excel workbook to multi-files
description: Aspose.Cells Cloud REST API, bir çalışma kitabını birden fazla dosyaya bölmeyi destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift dahildir.
weight: 130
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Bir Excel çalışma kitabını birden fazla dosyaya bölme
---
Bu REST API, Excel `workbook`'i farklı formatta birden fazla dosyaya bölmeyi gösterir.

**Sorgu Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|biçim|sicim|Bölünmüş format.|
|itibaren|tam sayı|Çalışma sayfası dizinini başlat.|
|ile|tam sayı|Çalışma sayfası dizininin sonu.|
|yatayÇözünürlük|tam sayı|Görüntü yatay çözünürlüğü.|
|dikeyÇözünürlük|tam sayı|Görüntünün dikey çözünürlüğü.|
|outFolder|sicim|çıkış bölünmüş dosya konumu.|
|splitNameRule|sicim||
|dosya|sicim|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim|Depolama adı.|

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/{isim}/böl|POSTALAMAK|Excel Çalışma Kitabını Böl|[PostWorkbookSplit](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web servislerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Result": {

    "Documents": [

      {

        "Id": 1,

        "link": {

          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",

          "Rel": null,

          "Title": null,

          "Type": null

        }

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
