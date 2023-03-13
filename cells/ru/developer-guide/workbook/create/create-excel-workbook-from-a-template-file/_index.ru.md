---
title: Как создать книгу Excel с файлом шаблона
second_title: Aspose.Cells Cloud Documen
linktitle: Шаблон
type: docs
url: /ru/workbook/create/template-file/
aliases: [/create-excel-workbook-from-a-template-file/,/workbook/new-from-a-template-file/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API как создать рабочую книгу Excel из шаблона смарт-маркера. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 30
---
Этот REST API указывает на создание `workbook` из `template file`.

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

|**API**|**Тип**|**Описание**|**Свэггер Ссылка**|
|:- |:- |:- |:- |
|/ячейки/{имя}|ПОМЕЩАТЬ|Создайте новую рабочую книгу Excel из файла шаблона.|[ПоместитьКнигуСоздать](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)|

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** инструмент командной строки для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&dataFile=Sample_Data.xml&isWriteOver=true" -H "accept: application/json" -H "x-aspose-client: Containerize.Swagger"


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


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "1ba81e1c8c3b8ffe85019434a1cbb5e8" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "3e47ddd0f0cb006c4311790d67c21a74" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PutWorkbookCreate-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-create_new_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "CreateExcelWorkbookFromTempateFile.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-CreateWorkbookFromTemplate-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-CreateWorkbookFromTemplate-create-empty-workbook-from-template.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateWorkbookFromTemplate-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "0828352a30b729404dd415c5ceed5615" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "046b2a6af4e89e88b75a417ca3862e41" >}}

{{< /tab >}}

{{< /tabs >}}
