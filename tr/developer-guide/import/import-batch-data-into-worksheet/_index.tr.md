﻿---
title: Toplu Verileri Excel Çalışma Sayfasına Aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: Toplu veriyi içe aktar
type: docs
url: /tr/import/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/,/import-data/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API, toplu verilerin Excel dosyalarına aktarılmasını destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 19
---
Bu REST API `import batch data`, Excel çalışma sayfasına.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk bölümü ImportBatchDataOption verilerini içerir ve ikincisi bir veri dosyası içerir.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:


**ImportBatchDataOption**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Toplu Veri|Liste<CellValue> | toplu veri|
| HedefÇalışma Sayfası| sicim| hedef çalışma sayfası adı.|
| Eklemek| sicim| doğru yanlış.|
| ImportDataType| sicim|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Kaynak| Dosya Kaynağı| BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.|



**Hücre Değeri**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| satır dizini| int||
| sütun dizini| int||
| tip| sicim| veri tipi|
| değer| sicim||
| stil| Stil(nesne)||



**Dosya Kaynağı**
|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Dosya Kaynağı Türü| sicim| InMemoryFiles/CloudFileSystem/RequestFiles|
| Dosya yolu| sicim| dosya konumu|


**Örnek**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
