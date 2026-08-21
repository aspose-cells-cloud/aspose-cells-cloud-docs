---
title: "Импорт двумерного массива типа double в рабочий лист Excel"
second_title: "Документ"
linktitle: "Импорт двумерного массива типа double"
type: docs
url: /ru/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, импорт двумерного массива типа double, API Excel, облачный SDK"
description: "Узнайте, как импортировать двумерный массив типа double в рабочий лист Excel с помощью облачного REST API Aspose.Cells. Включает информацию об аутентификации, формате запроса, параметрах, примерах XML/JSON и деталях ответа."
weight: 20
ArticleTitle: "Импорт двумерного массива типа double в рабочий лист Excel — Руководство Aspose.Cells Cloud"
---

Этот REST API **импортирует данные в виде двумерного массива типа double** в рабочий лист Excel.

> **Необходимые условия:** Перед вызовом этого API вы должны иметь действительный JWT-токен. Подробности см. в руководстве по аутентификации.

Вы отправляете HTTP-запрос с содержимым типа **multipart** (см. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Первая часть тела multipart содержит данные **ImportDoubleArrayOption**, а вторая часть — файл с данными.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Безопасность и аутентификация**

API облачной платформы Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

#### **ImportDoubleArrayOption**

| Имя параметра       | Тип       | Описание                                                                                                   |
| ------------------- | --------- | ---------------------------------------------------------------------------------------------------------- |
| FirstRow            | int       | Начиная с нуля индекс первой строки, в которую будут помещены данные.                                      |
| FirstColumn         | int       | Начиная с нуля индекс первого столбца, в который будут помещены данные.                                    |
| IsVertical          | boolean   | `true` / `false` — определяет, вставляется ли массив вертикально (`true`) или горизонтально (`false`).    |
| Data                | Double[]  | Массив значений типа double для импорта.                                                                   |
| DestinationWorksheet | string    | Имя целевого рабочего листа.                                                                               |
| IsInsert            | boolean   | `true` / `false` — если `true`, данные вставляются; если `false`, существующие ячейки перезаписываются.   |
| ImportDataType      | string    | Тип импортируемых данных (например, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`).    |
| Source              | FileSource | Указывает местоположение файла с данными, когда параметр `BatchData` равен null.                          |

#### Пример (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Пример (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
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

| Код | Значение                                            |
| --- | --------------------------------------------------- |
| 200 | Импорт успешно завершён                             |
| 400 | Неверный запрос — отсутствуют или некорректны данные |
| 401 | Неавторизованный доступ — недействительный или отсутствующий токен |
| 500 | Внутренняя ошибка сервера                           |

### Обработка ошибок

При возникновении ошибки API возвращает JSON-объект, содержащий код ошибки и описательное сообщение. Пример для неавторизованного запроса:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

Дополнительную информацию о связанных операциях импорта см. на страницах документации «Импорт двумерного массива типа int» и «Импорт массива целых чисел».

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK облачной платформы Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK облачной платформы Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}