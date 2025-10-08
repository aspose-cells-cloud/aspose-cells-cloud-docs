---
title: Импорт данных Json в Exce
second_title: Documen
linktitle: Импорт Jso
type: docs
url: /ru/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API поддерживает импорт строковых массивов данных в файлы Excel. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 40
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Импорт данных Json в Excel
---
Этот REST API `import json data` в рабочий лист Excel.

## РСЕT API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Важные параметры описаны в следующей таблице:

**ImportStringArrayOption**

|Имя параметра| Путь/Строка запроса/HTTPBody|Тип|Описание|
|:- |:- |:- |:- |
| имя| Путь| нить| Название рабочей книги|
| importJsonRequest| HTTPBody| сорт| Импорт json-запроса.|
| пароль| Строка запроса| нить| Пароль рабочей книги.|
| папка| Строка запроса| нить| Оригинальная папка рабочей тетради.|
| имя_хранилища| Строка запроса| нить| Имя хранилища.|
| outPath| Строка запроса| нить| Путь к выходному файлу.|
|outStorageName| Строка запроса| нить| Имя хранилища выходного файла.|
| checkExcelRestriction| Строка запроса| нить| Проверьте ограничение Excel.|

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

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:
