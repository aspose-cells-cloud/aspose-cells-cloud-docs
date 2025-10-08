---
title: Объединить рабочие книги Excel с другими книгами Excel
second_title: Documen
linktitle: Объединить файл Excel с файлом Excel
type: docs
url: /ru/merge-an-excel-file-into-the-excel-file/
aliases: [/merge-excel-workbooks/, /workbook/merge/]
keywords: Merge an Excel Workbooks into other Excel file
description: Aspose.Cells Cloud REST API поддерживает объединение файлов Excel с другими файлами Excel. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 50
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Объединение рабочих книг Excel с другими файлами Excel
---
Этот REST API указывает на объединение книги Excel `workbook` с другой книгой Excel.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|папка|нить|Оригинальная папка рабочей тетради.|
|имя_хранилища|нить|Имя хранилища.|

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Swagger Link**|
|:- |:- |:- |:- |
|/cells/{name}/merge|ПОЧТА|Объединение рабочих книг Excel|[PostWorkbooksMerge](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Workbook": {

    "FileName": "test.xlsx",

    "Links": [

      {

        "Href": "/test.xlsx",

        "Rel": "self",

        "Title": null,

        "Type": null

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As CSV",

        "Type": "text/csv"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As HTML",

        "Type": "text/html"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As ODS",

        "Type": "application/vnd.oasis.opendocument.spreadsheet"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As PDF",

        "Type": "application/pdf"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Table Delimited Text Format",

        "Type": "text/plain"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As TIFF",

        "Type": "image/tiff"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Microsoft Excel 2003",

        "Type": "application/vnd.ms-excel"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As Microsoft Excel 2007",

        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"

      },

      {

        "Href": "/test.xlsx",

        "Rel": "alternate",

        "Title": "Download As XPS",

        "Type": "application/vnd.ms-xpsdocument"

      }

    ],

    "Worksheets": {

      "link": {

        "Href": "/worksheets",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "DefaultStyle": {

      "link": {

        "Href": "/defaultstyle",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "DocumentProperties": {

      "link": {

        "Href": "/documentproperties",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "Names": {

      "link": {

        "Href": "/names",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "Settings": {

      "link": {

        "Href": "/settings",

        "Rel": "self",

        "Title": null,

        "Type": null

      }

    },

    "IsWriteProtected": "False",

    "IsProtected": "False",

    "IsEncryption": "false",

    "Password": null

  },

  "Code": 200,

  "Status": "OK"

}


Response headers


```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
