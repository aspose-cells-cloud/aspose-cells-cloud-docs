﻿---
title: Расшифровать файл Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Расшифровать файл Excel
type: docs
url: /ru/excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/,/workbook/decrypt/]
keywords: REST API, spreadsheets, excel, decryp
description: "Cells.Облако API для работы Excel: расшифровка рабочей книги Excel"
weight: 50
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Расшифровка рабочей книги Excel
---
Этот REST API расшифровывает Excel `workbook`.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|папка|нить|Оригинальная папка рабочей тетради.|
|имя_хранилища|нить|Имя хранилища.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|шифрование|WorkbookEncryptionRequest||

**WorkbookEncryptionRequest**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|ТипШифрования|нить|XOR/Совместимый/Улучшенный криптографический провайдерV1/Сильный криптографический провайдер|
|ДлинаКлюча|целое число||
|Пароль|нить||

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка Swagger**|
|:- |:- |:- |:- |
|/cells/{имя}/шифрование|УДАЛИТЬ|Расшифровать документ|[DeleteDecryptWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 1280, \"Password\": \"aspose\"}"

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

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
