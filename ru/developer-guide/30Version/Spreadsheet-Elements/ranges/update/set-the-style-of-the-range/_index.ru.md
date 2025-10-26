---
title: Установите стиль ранга
second_title: Documen
linktitle: Установить стиль
type: docs
url: /ru/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API поддерживает настройку стиля диапазона на листе Excel. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 70
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Установка стиля диапазона
---
## **Введение**
Этот пример позволяет задать стиль диапазона, используя Aspose.Cells Cloud API в своих приложениях. Вы можете использовать наш REST API с любым языком: .NET, Java, PHP, Ruby, Rails, Python, jQuery и многими другими.
## **API Информация**

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/cells/{name}/worksheets/{sheetName}/ranges/style|ПОЧТА|Установить стиль ячейки именованного диапазона|[PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Пример**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **Источник SDK**
Пакеты Cloud SDK Aspose.Cells можно загрузить со следующей страницы:[Доступные SDK](/cells/ru/available-sdks/)
### **Примеры SDK**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
