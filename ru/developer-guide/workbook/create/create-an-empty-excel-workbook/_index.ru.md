﻿---
title: Создайте пустую рабочую книгу Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Пустая рабочая книга
type: docs
url: /ru/workbook/create/empty-workbook/
aliases: [/create-an-empty-excel-workbook/,/workbook/new/]
keywords: How to create an Excel workbook
description: Aspose.Cells Cloud REST API как создать пустую книгу Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 20
---
Этот REST API указывает на создание файла `empty workbook`.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|файл шаблона|нить||
|файл данных|нить||
|isWriteOver|нить| правда/ложь|
|папка|нить|Оригинальная папка с рабочей тетрадью.|
|имя_хранилища|нить|Имя хранилища.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|данные|файл||


## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/ячейки/{имя}|ПОМЕЩАТЬ|Создать пустую рабочую книгу|[ПоместитьКнигуСоздать](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)|


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** инструмент командной строки для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" -H "accept: application/json" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Status": "string",
  "Workbook": {
    "FileName": "string",
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Names": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Settings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "IsWriteProtected": "string",
    "IsProtected": "string",
    "IsEncryption": "string",
    "Password": "string"
  }
}

```

{{< /tab >}}

{{< /tabs >}}



## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.


{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateEmptyWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "ad2ef2b72254d01920fc05d3ae506375" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "9e868bc0e2c275d9552372e65ca554b3" >}}

{{< /tab >}}

{{< /tabs >}}
