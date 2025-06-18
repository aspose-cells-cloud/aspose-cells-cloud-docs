---
title: Импортируйте данные CSV в таблицу Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Импортировать данные CSV
type: docs
url: /ru/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт данных CSV в файлы Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 19
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, импорт данных CSV в рабочий лист Excel
---
Этот REST API `import csv data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[РФК 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные ImportCSVDataOption, а вторая — файл данных.

## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Важные параметры описаны в следующей таблице:


**Импорт CSVDataOption**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| РазделительСтрока| нить||
| Конвертироватьчисловые данные| нить|правда/ложь.|
| Первая строка| интервал||
| Первая колонка| интервал||
| Исходный файл| нить||
| ПользовательскиеПарсеры|Список<CustomParserConfig> ||


**CustomParserConfig**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Индекс Столбца| интервал||
| Метод разбора| нить||
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

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
