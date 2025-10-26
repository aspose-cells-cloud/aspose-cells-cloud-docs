---
title: Импорт данных CSV в рабочий лист Excel
second_title: Documen
linktitle: Импорт csv-данных
type: docs
url: /ru/import-csv-data-into-excel/
aliases: [/import-csv-data-into-worksheet/,/import-data/csv-data/,/import/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт CSV-данных в файлы Excel. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 19
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт данных CSV в рабочий лист Excel
---
Этот REST API `import csv data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные ImportCSVDataOption, а вторая — файл данных.

## РСЕT API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Важные параметры описаны в следующей таблице:

**ImportCSVDataOption**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| РазделительСтрок| нить||
| ConvertNumericData| нить|верно/ложно.|
| FirstRow| инт||
| FirstColumn| инт||
| Исходный файл| нить||
| CustomParsers|Список<CustomParserConfig> ||

**CustomParserConfig**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| ColumnIndex| инт||
| ParseMethod| нить||
| CustomStyle| нить||

**Пример**

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

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
