---
title: Импортируйте данные Json в Exce.
second_title: Aspose.Cells Cloud Documen
linktitle: Импортировать JSO
type: docs
url: /ru/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API поддерживает импорт данных строкового массива в файлы Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 40
---
Этот REST API `import json data` в рабочий лист Excel.


## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Важные параметры описаны в следующей таблице:


**Импортстрингаррайопцион**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| имя| нить| Имя книги|
| импортJsonRequest| сорт| Импортируйте json-запрос.|
| пароль| нить| Пароль рабочей книги.|
| папка| нить|Оригинальная папка с рабочей тетрадью.|
| имя_хранилища| нить| Имя хранилища.|
| outPath| нить| Путь к выходному файлу.|
| outStorageName| нить| Имя хранилища для выходного файла.|
| проверкаExcelRestriction| нить| Проверьте ограничение Excel.|


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

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:





