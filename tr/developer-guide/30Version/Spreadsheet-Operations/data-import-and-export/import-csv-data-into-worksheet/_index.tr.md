---
title: CSV Verilerini Excel Çalışma Sayfasına Aktar
second_title: Documen
linktitle: csv verilerini içe aktar
type: docs
url: /tr/import-csv-data-into-excel/
aliases: [/import-csv-data-into-worksheet/,/import-data/csv-data/,/import/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API, CSV verilerinin Excel dosyalarına aktarılmasını destekler. SDK, Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift gibi çeşitli geliştirme dillerini destekler.
weight: 19
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, CSV Verilerini Excel Çalışma Sayfasına Aktar
---
Bu REST API `import csv data`'i Excel çalışma sayfasına dönüştürün.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı ImportCSVDataOption verilerini, ikinci kısmı ise bir veri dosyasını içerir.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

**CSVDataSeçeneğini İçe Aktar**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| AyırıcıDize| sicim||
| Sayısal Verileri Dönüştür| sicim|doğru/yanlış.|
| İlk Sıra| int||
| İlkSütun| int||
| Kaynak Dosyası| sicim||
| ÖzelAyrıştırıcılar|Liste<CustomParserConfig> ||

**CustomParserConfig**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Sütun İndeksi| int||
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

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
