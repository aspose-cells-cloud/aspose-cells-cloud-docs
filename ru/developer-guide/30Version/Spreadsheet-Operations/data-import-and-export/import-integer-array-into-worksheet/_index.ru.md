---
title: "Импорт целочисленного массива в рабочую тетрадь Excel"
linktype: "import-integer-array"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, импорт целочисленного массива, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Узнайте, как импортировать целочисленный массив в рабочую тетрадь Excel с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, параметры, примеры кода для различных SDK и детали ответа."
weight: 30
ArticleTitle: "Импорт целочисленного массива в рабочую тетрадь Excel – API Aspose.Cells Cloud"
---

Этот REST API импортирует целочисленный массив в рабочую тетрадь Excel.

Запрос должен быть HTTP **POST** с многочастным содержимым (см. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть многочастного тела содержит JSON-полезную нагрузку **ImportIntegerArrayOption**, а вторая часть — исходный файл данных (например, CSV-файл или двоичный файл Excel).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Оба конечных пункта принимают одну и ту же многочастную полезную нагрузку. Первый конечный пункт выполняет общую операцию импорта, а второй нацелен на конкретную рабочую книгу, идентифицируемую по `{name}`.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе маркера JWT</a>.

### **Параметры запроса**

### ImportIntegerArrayOption

| Имя параметра          | Тип       | Описание                                                                                                                                                                                        |
| ---------------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**           | int       | Индекс первой строки (начиная с нуля), в которую будут помещены данные.                                                                                                                         |
| **FirstColumn**        | int       | Индекс первого столбца (начиная с нуля), в который будут помещены данные.                                                                                                                       |
| **IsVertical**         | boolean   | `true`, чтобы вставить массив вертикально (вниз по столбцу); `false`, чтобы вставить его горизонтально (вдоль строки).                                                                        |
| **Data**               | Integer[] | Целочисленный массив для импорта.                                                                                                                                                               |
| **DestinationWorksheet** | string    | Имя рабочего листа, который получит данные.                                                                                                                                                    |
| **IsInsert**           | boolean   | `true`, чтобы вставить строки/столбцы перед записью данных; `false`, чтобы перезаписать существующие ячейки.                                                                                  |
| **ImportDataType**     | string    | Тип импортируемых данных. Допустимые значения: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**             | FileSource | Указывает расположение файла данных, когда параметр **BatchData** имеет значение `null`.                                                                                                      |

#### Пример тела запроса

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Ответ

Успешный запрос возвращает **HTTP 200** с JSON-полезной нагрузкой, подобной следующей:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Возможные коды состояния:

| Код | Значение                                     |
| --- | -------------------------------------------- |
| 200 | Импорт успешно завершён                      |
| 400 | Неверный запрос — отсутствующие или недопустимые данные |
| 401 | Неавторизован — недопустимый или отсутствующий токен |
| 500 | Внутренняя ошибка сервера                   |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ интеграции этого функционала. SDK абстрагируют низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}