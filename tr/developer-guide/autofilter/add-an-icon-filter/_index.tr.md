﻿---
title: Excel çalışma sayfasına simge filtresi ekleme
second_title: Aspose.Cells Cloud Documen
linktitle: Simge filtresi ekle
type: docs
url: /tr/autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: Adds an icon filter on an Excel worksheet
description: Aspose.Cells Bulut API, Excel çalışma sayfasına simge filtresi eklemeyi destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 65
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Excel çalışma sayfasına simge filtresi ekleme
---
Bu REST API, Excel Çalışma Sayfasına `icon filter` ekleneceğini belirtir.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter

```

İstek parametreleri şunlardır:

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| Yol| Çalışma kitabı adı.|
| sayfaAdı| sicim| Yol| Çalışma sayfası adı.|
|menzil|sicim| Sorgu||
|alanIndex|tamsayı| Sorgu||
|iconSetType|sicim| Sorgu|Arrows3/ArrowsGray3/Flags3/Signs3/Symbols3/Symbols32/TrafficLights31/TrafficLights32/Arrows4/ArrowsGray4/Rating4/RedToBlack4/TrafficLights4/Arrows5/ArrowsGray5/Quarters5/Rating5/Stars3/Boxes5/Triangles3/Hiçbiri/ CustomSet/Smilies3/ColorSmilies3|
|simge kimliği|tamsayı| Sorgu||
|maçBoşluklar|sicim| Sorgu|doğru yanlış|
|yenileme|sicim| Sorgu|doğru yanlış|
|dosya|sicim| Sorgu|Orijinal çalışma kitabı klasörü.|
|depolamaAdı| Sorgu|sicim|Depolama adı.|

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldIndex=0&iconSetType=ArrowsGray3&iconId=1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}


## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddIconFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetIconFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_icon_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddIconFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddIconFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "a05cbd25e102b8369a2ad33d46252a07" >}}

{{< /tab >}}

{{< /tabs >}}
