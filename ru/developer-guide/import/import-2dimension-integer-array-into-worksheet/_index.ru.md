﻿---
title: Импортируйте двухмерный целочисленный массив в таблицу Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Импортировать 2-мерное целое число arra
type: docs
url: /ru/import/2dimension-integer-array/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/]
keywords: Import 2 dimension integer array data into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт данных двумерного целочисленного массива в файлы Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 20
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, импорт двухмерного целочисленного массива в рабочий лист Excel
---
Этот REST API `import 2 dimension integer array data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[РФК 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные Import2DimensionIntegerArrayOption, а вторая — файл данных.

Важные параметры описаны в следующей таблице:

## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

**Import2DimensionIntegerArrayOption**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Первая строка| интервал||
| Первая колонка| интервал||
| Данные|Целое число[,]||
| Рабочий лист назначения| нить| имя рабочего листа назначения.|
| IsInsert| нить| правда/ложь.|
| Импортдататипе| нить|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Источник| источник файла| Указывает позицию файла данных, когда параметр BatchData имеет значение null.|



**Пример**

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
## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

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




