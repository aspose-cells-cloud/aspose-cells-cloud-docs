---
title: "Импорт пакетных данных в лист Excel"
second_title: "Документ"
linktitle: "Импорт пакетных данных"
type: docs
url: /ru/import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, облачный API, импорт пакетных данных, Excel, CSV, JSON, XML, массивы"
description: "Узнайте, как импортировать пакетные данные (CSV, JSON, XML, массивы) в лист Excel с помощью облачного REST API Aspose.Cells. Приведены примеры аутентификации, запросов и ответов, фрагменты кода SDK, а также обработка ошибок."
weight: 19
ArticleTitle: "Импорт пакетных данных в лист Excel — документация Aspose.Cells Cloud"
---

Этот REST API **импортирует пакетные данные** в лист Excel. Он принимает многокомпонентный запрос, в котором первая часть содержит объект **ImportBatchDataOption**, а вторая — фактический файл с данными (CSV, JSON, XML и т.д.).

Операция использует HTTP-запрос с многокомпонентным содержимым (см. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Безопасность и аутентификация**

API облачной платформы Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### ImportBatchDataOption

| Имя параметра          | Тип               | Описание                                                                                                                                                         |
| ---------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**          | `List<CellValue>` | Коллекция значений ячеек, которые будут записаны напрямую.                                                                                                       |
| **DestinationWorksheet** | `string`          | Имя листа, в который будут импортированы данные.                                                                                                                 |
| **IsInsert**           | `bool`            | Если `true`, данные вставляются, а существующие ячейки сдвигаются; если `false`, данные перезаписывают существующие ячейки.                                     |
| **ImportDataType**     | `string`          | Формат импортируемых данных. Допустимые значения: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**             | `FileSource`      | Указывает местоположение файла с данными, если **BatchData** равен `null`.                                                                                      |

### CellValue

| Имя параметра  | Тип      | Описание                                                |
| -------------- | -------- | ------------------------------------------------------- |
| **rowIndex**   | `int`    | Индекс строки целевой ячейки (начиная с 0).            |
| **columnIndex**| `int`    | Индекс столбца целевой ячейки (начиная с 0).           |
| **type**       | `string` | Тип данных значения (например, `int`, `double`, `string`). |
| **value**      | `string` | Фактическое значение, которое будет записано в ячейку. |
| **style**      | `Style`  | Необязательная информация о стиле ячейки.              |

### FileSource

| Имя параметра      | Тип      | Описание                                                          |
| ------------------ | -------- | ----------------------------------------------------------------- |
| **FileSourceType** | `string` | Источник файла: `InMemoryFiles`, `CloudFileSystem` или `RequestFiles`. |
| **FilePath**       | `string` | Путь или идентификатор файла в выбранном источнике.              |

### Пример (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                                      |
|------|-----------------------------|-------------------------------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит информацию о выполнении операции.    |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Неверный или отсутствующий токен JWT.                                         |
| 413  | Payload Too Large           | Загруженный файл превышает допустимый размер.                                 |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                                                |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) определяет публичный программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK облачной платформы Aspose.Cells

Использование SDK — самый быстрый способ интеграции этой функциональности. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK облачной платформы Aspose.Cells приведён в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}