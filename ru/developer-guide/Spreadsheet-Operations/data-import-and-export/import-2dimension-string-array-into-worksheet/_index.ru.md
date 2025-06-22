---
title: Импорт 2-мерного строкового массива в рабочий лист Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Импорт 2-мерной строки arra
type: docs
url: /ru/import-a-2D-string-array-into-excel-worksheet/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/,/import/2dimension-string-array/ ]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт данных массива строк 2-мерного размера в файлы Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 20
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт 2-мерного строкового массива в рабочий лист Excel
---
Этот REST API `import 2 dimension string array data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[Запрос на изменение 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные Import2DimensionStringArrayOption, а вторая — файл данных.

## РЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Важные параметры описаны в следующей таблице:

**Import2DimensionStringArrayOption**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| FirstRow| инт||
| ПерваяКолонка| инт||
| Данные|Нить[,]||
| Рабочий лист назначения| нить| наименование целевого рабочего листа.|
| IsInsert| нить| правда/ложь.|
| ИмпортТипДанные| нить|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Источник| Источник файла| Указывает позицию файла данных, если параметр BatchData равен нулю.|

**Пример**

```json

{
    "Data": [
        ["1.0", "2.9"],
        ["2.0", "2.1"]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 1,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionStringArray"
}

```

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
