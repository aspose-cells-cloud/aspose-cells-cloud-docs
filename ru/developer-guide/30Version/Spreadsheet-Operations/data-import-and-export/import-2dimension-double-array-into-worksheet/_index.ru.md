---
title: "Импорт двумерного массива типа double в рабочий лист Excel"
second_title: "Документ"
linktitle: "Импорт двумерного массива типа double"
type: docs
url: /ru/import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "импорт двумерного массива типа double, Excel, Aspose Cells Cloud, REST API, электронная таблица, импорт данных"
description: "Узнайте, как импортировать двумерный массив типа double в рабочий лист Excel с использованием REST API Aspose.Cells Cloud. Включает формат запроса, параметры и примеры кода SDK."
weight: 20
---

Этот REST API **импортирует двумерный массив типа double** в рабочий лист Excel.

Запрос представляет собой HTTP-запрос `POST` с многочастным содержимым (см. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть тела многочастного запроса содержит данные **Import2DimensionDoubleArrayOption**, а вторая часть — исходный файл данных.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Важные параметры описаны в следующей таблице:

### Import2DimensionDoubleArrayOption

| Имя параметра          | Тип         | Описание                                                                                                            |
| ---------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**           | `int`       | Индекс строки (с 1), с которой начинается импорт.                                                                  |
| **FirstColumn**        | `int`       | Индекс столбца (с 1), с которого начинается импорт.                                                                 |
| **Data**               | `Double[,]` | Двумерный массив значений типа double, подлежащий импорту.                                                          |
| **DestinationWorksheet** | `string`  | Имя рабочего листа, в который будут импортированы данные.                                                          |
| **IsInsert**           | `string`    | `"true"` — вставить строки, `"false"` — перезаписать существующие ячейки.                                          |
| **ImportDataType**     | `string`    | Тип импортируемых данных (например, `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData` и т.д.). |
| **Source**             | `FileSource`| Указывает расположение файла данных, если параметр `BatchData` имеет значение null.                               |

**Пример**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит данные о выполненной операции.   |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large           | Загруженный файл превышает допустимый размер.                           |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                          |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) определяет общедоступное программное интерфейсное описание, позволяющее выполнять взаимодействие по REST непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ интеграции этой функциональности. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}