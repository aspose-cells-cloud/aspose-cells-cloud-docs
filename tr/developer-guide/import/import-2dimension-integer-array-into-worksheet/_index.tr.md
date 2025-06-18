---
title: 2 Boyutlu Tamsayı Dizisini Excel Çalışma Sayfasına Aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: 2 boyutlu tamsayı dizisini içe aktar
type: docs
url: /tr/import/2dimension-integer-array/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/]
keywords: Import 2 dimension integer array data into Excel files
description: Aspose.Cells Cloud REST API, 2 boyutlu tam sayı dizisi verilerinin Excel dosyalarına aktarılmasını destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 20
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, 2 Boyutlu Tamsayı Dizisini Excel Çalışma Sayfasına Aktar
---
Bu REST API `import 2 dimension integer array data`'i Excel çalışma sayfasına dönüştürün.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı Import2DimensionIntegerArrayOption verilerini, ikincisi ise bir veri dosyasını içerir.

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

**Import2DimensionIntegerArrayOption**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| İlk sıra| int||
| İlk sütun| int||
| Veri|Tamsayı[,]||
| HedefÇalışma Sayfası| sicim| hedef çalışma sayfası adı.|
| Ekle| sicim| doğru yanlış.|
| Veri Türü İçe Aktarma| sicim|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Kaynak| Dosya Kaynağı| BatchData parametresi null olduğunda veri dosyası konumunu gösterir.|



**Örnek**

```json
{
    "Data": [
        [1, 2],
        [3, 4]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionIntArray"
}

```
## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




