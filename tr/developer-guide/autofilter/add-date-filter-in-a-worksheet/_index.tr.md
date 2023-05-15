---
title: Excel çalışma sayfasına tarih filtresi ekleme
second_title: Aspose.Cells Cloud Documen
linktitle: Tarih filtresi ekle
type: docs
url: /tr/autofilter/add-date-filter/
aliases: [/add-date-filter-in-a-worksheet/,/autofilter/add-a-date-filter/]
keywords: Adds a date filter on an Excel worksheet
description: Aspose.Cells Bulut API, Excel çalışma sayfasına tarih filtresi eklemeyi destekler. SDK, geliştirme dillerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 65
---
Bu REST API, bir Excel Çalışma Sayfasına `date filter` eklenmesini belirtir.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter

```
İstek parametreleri şunlardır:

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| Yol|Çalışma kitabı adı.|
| sayfaAdı| sicim| Yol| Çalışma sayfası adı.|
|menzil|sicim| Sorgu||
|alan dizini|tamsayı| Sorgu||
|tarihSaatGruplamaTürü|sicim| Sorgu| Gün/Saat/Dakika/Ay/Saniye/Yıl|
|yıl|tamsayı| Sorgu||
|ay|tamsayı| Sorgu||
|gün|tamsayı| Sorgu||
|saat|tamsayı| Sorgu||
|dakika|tamsayı| Sorgu||
|ikinci|tamsayı| Sorgu||
|Maç Boşlukları|sicim| Sorgu|doğru yanlış|
|yenile|sicim| Sorgu|doğru yanlış|
|dosya|sicim| Sorgu|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim| Sorgu|Depolama adı.|


 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
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

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddDataFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddDateWorksheetExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetDateFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_date_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddDateFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddDateWorksheetExample-1.java" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddDateFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "54cd61aee4496583dfacaf7dadef6463" >}}

{{< /tab >}}

{{< /tabs >}}
