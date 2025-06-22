---
title: Импортировать изображение в рабочий лист Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Импортировать картинку
type: docs
url: /ru/import-picture-into-excel-worksheet/
aliases: [/import-picture-into-worksheet/,/import-data/picture/, /import/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт изображений в файлы Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 19
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт изображения в Excel Рабочий лист
---
Этот REST API `import picture data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[Запрос на изменение 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные ImportPictureOption, а вторая — файл данных.

## РЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Важные параметры описаны в следующей таблице:

**ImportPictureOption**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Верхний левый ряд| инт||
| Верхний левый столбец| инт||
| НижнийПравыйСтрока| инт||
| Нижний правый столбец| инт||
| Имя файла| нить||
| Данные| Нить||
| Рабочий лист назначения| нить| наименование целевого рабочего листа.|
| IsInsert| нить| правда/ложь.|
| ИмпортТипДанные| нить|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Источник| Источник файла| Указывает позицию файла данных, если параметр BatchData равен нулю.|

**Пример**

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
