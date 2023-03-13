---
title: Импорт данных с использованием хранилища
second_title: Aspose.Cells Cloud Documen
linktitle: Импорт данных с помощью хранилища
type: docs
url: /ru/import/with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/]
description: "Cells.Cloud API для работы Excel: Импорт данных в рабочий лист Excel"
weight: 10
---
Этот REST API указывает `import data` в файле Excel.
 
## РСЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
| импорт данных|| тело||

**Параметры параметров импорта данных**описаны в[справочная ссылка](/cells/ru/import/#import-data-option-parameter).

 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
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
 
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

