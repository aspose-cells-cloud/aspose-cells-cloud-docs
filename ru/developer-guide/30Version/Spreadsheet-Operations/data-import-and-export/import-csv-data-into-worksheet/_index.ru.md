---
title: "Импорт данных CSV в рабочий лист Excel"
second_title: "Документ"
linktitle: "Импорт данных CSV"
type: docs
url: /ru/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "импорт данных CSV, Excel, Aspose.Cells Cloud, REST API, электронная таблица, импорт CSV"
description: "REST API Aspose.Cells Cloud позволяет импортировать данные CSV в рабочие листы Excel. Поддерживаемые SDK: Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 19
---

Этот REST API **импортирует данные CSV** в рабочий лист Excel.

Запрос представляет собой HTTP-запрос с многочастным содержимым (см. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть многочастного содержимого содержит данные `ImportCSVDataOption`, а вторая часть — файл CSV.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

Важные параметры описаны в таблицах ниже.

### ImportCSVDataOption

| Имя параметра      | Тип                        | Описание                                                                 |
| ------------------ | -------------------------- | ------------------------------------------------------------------------ |
| SeparatorString    | string                     | Символ, используемый для разделения полей в файле CSV (например, `,` или `;`). |
| ConvertNumericData | string (`true`/`false`)    | Указывает, следует ли преобразовывать строковые представления чисел в числовые значения. |
| FirstRow           | int                        | 1‑индексированный номер первой строки, куда будут помещены данные.       |
| FirstColumn        | int                        | 1‑индексированный номер первого столбца, куда будут помещены данные.     |
| SourceFile         | string                     | Имя исходного CSV-файла для импорта.                                      |
| CustomParsers      | List\<CustomParserConfig\> | Коллекция настроек пользовательских парсеров для конкретных столбцов.     |

### CustomParserConfig

| Имя параметра | Тип    | Описание                                                             |
| ------------- | ------ | -------------------------------------------------------------------- |
| ColumnIndex   | int    | 0‑индексированный номер столбца, к которому применяется пользовательский парсер. |
| ParseMethod   | string | Метод парсинга для столбца (например, `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle   | string | Пользовательский стиль (например, формат числа), применяемый к распарсенным ячейкам. |

**Пример**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий токен JWT.     |
| 413 | Payload Too Large           | Загружаемый файл превышает предельный размер.     |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                    |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) определяет публично доступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — оптимальный способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующий пример кода демонстрирует вызов веб-сервиса Aspose.Cells с использованием SDK для PHP:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}

---