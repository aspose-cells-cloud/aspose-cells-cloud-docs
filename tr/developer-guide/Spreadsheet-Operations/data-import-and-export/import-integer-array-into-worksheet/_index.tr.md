﻿---
title: Tamsayı Dizisini Excel Çalışma Sayfasına Aktar
linktitle: Tam sayı dizisini içe aktar
type: docs
url: /tr/import-integer-array-into-excel-worksheet/
aliases: [/import-integer-array-into-excel-worksheet/,/import-integer-array-into-worksheet/,/import-data/integer-array/, /import/integer-array/]
keywords: Import integer array data into Excel files
description: Aspose.Cells Cloud REST API, tamsayı dizisi verilerini Excel dosyalarına aktarmayı destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir.
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Tamsayı Dizisini Excel Çalışma Sayfasına Aktar
---
Bu REST API `import int array data`'i Excel çalışma sayfasına aktarın.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı ImportIntegerArrayOption verilerini, ikinci kısmı ise bir veri dosyasını içerir.

## RSETAPI

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

**TamsayıArraySeçeneğini İçe Aktar**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| İlk Sıra| int||
| İlkSütun| int||
| Dikey mi| sicim| doğru/yanlış.|
| Veri|Tamsayı[]||
| HedefÇalışma Sayfası| sicim| hedef çalışma sayfası adı.|
| Eklemek| sicim| doğru/yanlış.|
| Veri Türünü İçe Aktar| sicim|IntArray/DoubleArray/StringArray/İki BoyutluIntArray/İki BoyutluÇift Dizi/İki BoyutluDize Dizi/Toplu Veri/CSVVeri.|
| Kaynak| Dosya Kaynağı| BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.|

**Örnek**

```JSON

{
    "Data": [1, 2, 4],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 1,
    "FirstColumn": 2,
    "IsVertical": true,
    "IsInsert": true,
    "importDataType": "IntArray"
}

```

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
