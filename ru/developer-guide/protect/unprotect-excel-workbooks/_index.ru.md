---
title: Снимите защиту с рабочей книги Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Снять защиту
type: docs
url: /ru/workbook/unprotect/
aliases: [/unprotect-excel-workbooks/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Облако API для Excel работает: защита книги Excel"
weight: 60
kwords: Excel, Office Cloud, REST API, электронная таблица, PDF, CSV, Json, Markdwon, снять защиту с книги Excel.
---
Этот REST API снимает защиту с Excel `workbook`.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|папка|нить|Оригинальная папка с рабочей тетрадью.|
|имя_хранилища|нить|Имя хранилища.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|защита|Запрос на защиту книги||

**Запрос на защиту книги**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|Тип защиты|нить|ВСЕ/СОДЕРЖИМОЕ/НЕТ/ОБЪЕКТЫ/СЦЕНАРИИ/СТРУКТУРА/ОКНА|
|Пароль|нить||


## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Сваггер Ссылка**|
|:- |:- |:- |:- |
|/cells/{имя}/защита|УДАЛИТЬ|Снять защиту с документа|[УдалитьУнЗащититьДокумент](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument)|

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectDocument) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

 Вы можете использовать**cURL**инструмент командной строки для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json"  -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Java" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteUnProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteUnProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-unprotect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-UnprotectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-UnprotectWorkbook-unprotect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-UnprotectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e70e326db37cfb9a80aadf9d795687c5" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "a856eb7506ccc320def87e055b177ca5" >}}

{{< /tab >}}

{{< /tabs >}}
