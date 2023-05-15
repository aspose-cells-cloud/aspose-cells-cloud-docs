---
title: CSV Verilerini Excel Çalışma Sayfasına Aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: csv verilerini içe aktar
type: docs
url: /tr/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API, csv verilerini Excel dosyalarına aktarmayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 19
---
Bu REST API `import csv data`, Excel çalışma sayfasına.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk bölümü ImportCSVDataOption verilerini içerir ve ikincisi bir veri dosyası içerir.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:


**ImportCSVDataOption**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| AyırıcıDize| sicim||
| Sayısal Verileri Dönüştür| sicim|doğru yanlış.|
| İlk sıra| int||
| İlk sütun| int||
| Kaynak dosyası| sicim||
| Özel Ayrıştırıcılar|Liste<CustomParserConfig> ||


**ÖzelAyrıştırıcıYapılandırması**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Sütun Dizini| int||
| Ayrıştırma Yöntemi| sicim||
| Özel Stil| sicim||

**Örnek**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
