---
title: "Импорт массива строк в рабочий лист Excel – Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Импорт массива строк"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, импорт массива строк, REST API Excel, многокомпонентная загрузка, импорт данных в рабочий лист, облачный SDK"
description: "Узнайте, как импортировать массив строк в рабочий лист Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает формат запроса, параметры и примеры SDK."
weight: 40
ArticleTitle: "Импорт массива строк в рабочий лист Excel – Aspose.Cells Cloud"
---

Импорт массива строк в рабочий лист Excel — распространённая задача при заполнении электронных таблиц данными в виде списков. Эта операция полезна, например, при загрузке значений конфигурации, передаче данных из внешних источников или инициализации рабочих листов заранее заданными наборами строк.

**Необходимые условия:**  
- Действующий JWT-токен, полученный в рамках процедуры аутентификации Aspose.Cells Cloud.  
- Существующая рабочая книга (или возможность её создания) в хранилище Aspose Cloud.  
- Соответствующая версия SDK, поддерживающая модель `ImportStringArrayOption`.

Этот REST API позволяет импортировать данные в виде массива строк в рабочий лист Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

Запрос использует многокомпонентное HTTP-содержимое (см. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Первая часть многокомпонентного тела содержит полезную нагрузку **ImportStringArrayOption**, а вторая — исходный файл с данными.

Важные параметры описаны в следующей таблице:

<caption>Параметры ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| Имя параметра        | Тип        | Описание                                                                                                                                                             |
| --------------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Индекс начальной строки (с 1), куда будут помещены данные.                                                                                                            |
| FirstColumn          | int        | Индекс начального столбца (с 1), куда будут помещены данные.                                                                                                         |
| IsVertical           | boolean    | `true`, чтобы вставить данные вертикально; `false`, чтобы вставить горизонтально.                                                                                   |
| Data                 | String[]   | Массив строк для импорта.                                                                                                                                             |
| DestinationWorksheet | string     | Имя рабочего листа, в который будут импортированы данные.                                                                                                            |
| IsInsert             | boolean    | `true`, чтобы вставить строки/столбцы (со смещением существующих ячеек); `false`, чтобы перезаписать существующие ячейки.                                            |
| ImportDataType       | string     | Тип импортируемых данных (например, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Указывает местоположение файла с данными, когда **BatchData** равен null (например, `CloudFileSystem`, `LocalFile`). Обязателен, если `BatchData` не указан.          |

### Пример

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Ответ

Успешный запрос возвращает **HTTP 200** с JSON-полезной нагрузкой следующего вида:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Возможные коды состояния:

| Код | Значение                                 |
|-----|------------------------------------------|
| 200 | Импорт успешно завершён                   |
| 400 | Неверный запрос — отсутствуют или недопустимы данные |
| 401 | Неавторизованный доступ — недействительный или отсутствующий токен |
| 500 | Внутренняя ошибка сервера                 |


## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}