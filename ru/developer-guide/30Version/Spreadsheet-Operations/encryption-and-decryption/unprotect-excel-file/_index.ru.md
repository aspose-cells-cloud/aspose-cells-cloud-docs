---
title: Снять защиту с рабочей книги Excel
second_title: Documen
linktitle: Снять защиту Excel fil
type: docs
url: /ru/excel-file-unprotect/
aliases: [/unprotect-excel-workbooks/, /workbook/unprotect/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Cloud API для работы Excel: защита рабочей книги Excel"
weight: 60
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Снятие защиты с книги Excel
---
Этот REST API снимает защиту с Excel `workbook`.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|папка|нить|Оригинальная папка рабочей тетради.|
|имя_хранилища|нить|Имя хранилища.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|защита|WorkbookProtectionRequest||

**WorkbookProtectionRequest**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|Тип защиты|нить|ВСЕ/СОДЕРЖИМОЕ/НИ ОДНОГО/ОБЪЕКТЫ/СЦЕНАРИИ/СТРУКТУРА/ОКНА|
|Пароль|нить||

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Swagger Link**|
|:- |:- |:- |:- |
|/клетки/{имя}/защита|УДАЛИТЬ|Снять защиту документа|[DeleteUnProtectWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

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

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
