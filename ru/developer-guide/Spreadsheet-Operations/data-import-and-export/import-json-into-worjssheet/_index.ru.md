---
title: Импорт данных Json в Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Импорт Jso
type: docs
url: /ru/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API поддерживает импорт данных массива строк в файлы Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 40
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт данных Json в Excel
---
Этот REST API `import json data` в рабочий лист Excel.

## РЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Важные параметры описаны в следующей таблице:

**ImportStringArrayOption**

|Имя параметра| Путь/Строка запроса/HTTPBody|Тип|Описание|
|:- |:- |:- |:- |
| имя| Путь| нить| Название рабочей книги|
| importJsonRequest| HTTP-тело| сорт| Импорт json-запроса.|
| пароль| Строка запроса| нить| Пароль рабочей книги.|
| папка| Строка запроса| нить| Оригинальная папка рабочей тетради.|
| имя_хранилища| Строка запроса| нить| Имя хранилища.|
| outPath| Строка запроса| нить| Путь к выходному файлу.|
| outStorageName| Строка запроса| нить| Имя хранилища для выходного файла.|
| checkExcelОграничение| Строка запроса| нить| Проверьте ограничение Excel.|

**Пример**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
