---
title: "Импорт двумерного целочисленного массива в рабочий лист Excel"
second_title: "Документ"
linktitle: "Импорт двумерного целочисленного массива"
type: docs
url: /ru/import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, импорт двумерного целочисленного массива, рабочий лист Excel, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API позволяет импортировать двумерные целочисленные массивы в рабочие листы Excel. SDK доступны для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 20
---

Этот REST API **импортирует двумерный целочисленный массив** в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с многочастным содержимым (см. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть многочастного содержимого содержит данные `Import2DimensionIntegerArrayOption`, а вторая — файл с данными.

Важные параметры описаны в следующей таблице:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Import2DimensionIntegerArrayOption**

| Имя параметра        | Тип        | Описание                                                                                                                                                                                                 |
| -------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | 1-индексированная позиция первой строки, в которую будут помещены данные.                                                                                                                                |
| FirstColumn          | int        | 1-индексированная позиция первого столбца, в который будут помещены данные.                                                                                                                             |
| Data                 | Integer[,] | Двумерный целочисленный массив, содержащий значения для импорта.                                                                                                                                        |
| DestinationWorksheet | string     | Имя целевого рабочего листа.                                                                                                                                                                            |
| IsInsert             | string     | `"true"` — вставить данные (сдвигая существующие ячейки), `"false"` — перезаписать существующие ячейки.                                                                                                |
| ImportDataType       | string     | Указывает формат данных. Поддерживаемые значения: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`.      |
| Source               | FileSource | Указывает местоположение файла с данными, когда параметр `BatchData` равен `null`.                                                                                                                      |

### **Пример**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
}
```

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (OK)                     | Фильтр применён успешно; в ответе содержатся детали операции.            |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.                           |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                             |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                         |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[OpenAPI-спецификация](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) определяет публично доступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}