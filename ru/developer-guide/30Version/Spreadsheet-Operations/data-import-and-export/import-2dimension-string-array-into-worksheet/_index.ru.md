---
title: "Импорт двумерного строкового массива в рабочую тетрадь Excel"
second_title: "Документ"
linktitle: "Импорт двумерного строкового массива"
type: docs
url: /import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud, импорт двумерного строкового массива, Excel, REST API, SDK"
description: "Узнайте, как использовать Aspose.Cells Cloud REST API для импорта двумерного строкового массива в рабочую тетрадь Excel. Включает формат запроса, подробную информацию о параметрах и примеры кода SDK для C#, PHP и Ruby."
weight: 20
---

Этот REST API **импортирует двумерный строковый массив** в рабочую тетрадь Excel.

Запрос представляет собой HTTP-запрос с многочастным содержимым (см. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть многочастного содержимого содержит данные `Import2DimensionStringArrayOption`, а вторая — файл с данными.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

Основные параметры описаны в следующей таблице:

### **Import2DimensionStringArrayOption**

| Имя параметра         | Тип                 | Описание                                                                   |
| --------------------- | ------------------- | -------------------------------------------------------------------------- |
| FirstRow              | int                 | Индекс строки (начиная с нуля), с которой начинается импорт.               |
| FirstColumn           | int                 | Индекс столбца (начиная с нуля), с которого начинается импорт.             |
| Data                  | String[,]           | Двумерный массив, содержащий строки, подлежащие импорту.                   |
| DestinationWorksheet  | string              | Имя рабочего листа, на который будут импортированы данные.                |
| IsInsert              | string (true/false) | Если **true**, данные вставляются, а существующие ячейки сдвигаются.      |
| ImportDataType        | string              | Указывает тип данных; для этой операции используйте `TwoDimensionStringArray`. |
| Source                | FileSource          | Указывает расположение файла с данными, когда параметр `BatchData` равен null. |

### Пример тела запроса

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| Код  | Значение                   | Описание                                                |
|------|----------------------------|---------------------------------------------------------|
| 200  | OK (ОК)                    | Фильтр успешно применён; в ответе содержатся подробности операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недопустимый или отсутствующий токен JWT.               |
| 413  | Payload Too Large (Слишком большой объём полезной нагрузки) | Загружаемый файл превышает предельный размер.           |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                          |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) определяет публично доступное программное интерфейсное описание, позволяющее выполнять взаимодействие с REST напрямую из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ интеграции этого функционала. SDK скрывает детали низкоуровневого взаимодействия, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}