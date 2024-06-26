﻿---
title: Импортируйте изображение в рабочий лист Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Импортировать изображение
type: docs
url: /ru/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт изображений в файлы Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 19
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Импорт изображения в рабочий лист Excel
---
Этот REST API `import picture data` в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[РФК 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит данные ImportPictureOption, а вторая — файл данных.

## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


Важные параметры описаны в следующей таблице:


**Импорткартуревариант**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Верхний левый ряд| интервал||
| Верхний левый столбец| интервал||
| Нижний правый ряд| интервал||
| Нижний правый столбец| интервал||
| Имя файла| нить||
| Данные| Нить||
| Рабочий лист назначения| нить| имя рабочего листа назначения.|
| IsInsert| нить| правда/ложь.|
| Импортдататипе| нить|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Источник| источник файла| Указывает позицию файла данных, когда параметр BatchData имеет значение null.|


**Пример**


## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

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

