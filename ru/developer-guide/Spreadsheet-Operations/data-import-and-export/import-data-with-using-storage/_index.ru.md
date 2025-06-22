---
title: Импорт данных с использованием хранилища
second_title: Aspose.Cells Cloud Documen
linktitle: Импорт данных с помощью хранилища
type: docs
url: /ru/import-data-with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/,/import/with-using-storage/]
description: "Cells.Cloud API для работы Excel: Импорт данных в рабочий лист Excel"
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт данных с использованием хранилища
---
Этот REST API указывает `import data` в файле Excel.

## РЕТ API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
| импортДанные|| тело||

**Параметры импорта данных** описаны в[ссылка для справки](/cells/ru/import/#import-data-option-parameter).

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
