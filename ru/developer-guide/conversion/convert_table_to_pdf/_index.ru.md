---
title: "Преобразование таблицы в PDF"
ArticleTitle: "Преобразование таблицы в PDF – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /ru/cells/convert/table/pdf
aliases: []
keywords: "Преобразование таблицы в PDF, Aspose.Cells, API"
description: "Преобразует таблицу электронной таблицы, хранящейся на локальном диске, в PDF-файл с использованием Aspose.Cells Cloud."
weight: 1000
---

## Преобразование таблицы в PDF с помощью веб-сервисов Aspose.Cells Cloud

Эта операция считывает файл электронной таблицы из локальной файловой системы, преобразует указанную таблицу в PDF-документ и возвращает результат преобразования. Вся обработка происходит на облачном сервере, поэтому промежуточная загрузка в облачное хранилище не требуется. API поддерживает дополнительные параметры: местоположение выходного файла, пользовательские шрифты, автоматическое подогнавание строк/столбцов, региональные настройки и защищённые паролем рабочие книги.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра   | Тип   | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Файл   | FormData                    | Загрузка файла электронной таблицы.                                                                                                                                         |
| worksheet        | Строка | Запрос                      | Имя рабочего листа электронной таблицы.                                                                                                                                  |
| tableName        | Строка | Запрос                      | Имя таблицы.                                                                                                                                                      |
| outPath          | Строка | Запрос                      | (Необязательно) Путь к папке, где хранится рабочая книга. По умолчанию — null.                                                                                  |
| outStorageName   | Строка | Запрос                      | Имя хранилища для выходного файла.                                                                                                                                       |
| fontsLocation    | Строка | Запрос                      | Использование пользовательских шрифтов.                                                                                                                                               |
| AutoRowsFit      | Boolean| Запрос                      | (Необязательно) Автоматическая подгонка всех строк на рабочих листах.                                                                                                                    |
| AutoColumnsFit   | Boolean| Запрос                      | (Необязательно) Автоматическая подгонка всех столбцов на рабочих листах.                                                                                                                 |
| region           | Строка | Запрос                      | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали.                         |
| password         | Строка | Запрос                      | Пароль для открытия файла электронной таблицы.                                                                                                                      |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
|----------------|------|-------------|
| *Нет* | *Нет* | *Тело в формате JSON не требуется; файл отправляется через multipart/form-data.* |

### **Ответ**

```json
{
  "file": "<двоичное содержимое PDF>"
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Таблица успешно преобразована в PDF; тело ответа содержит поток PDF-файла. |
| 400 | Bad Request | Некорректные параметры запроса или неверный URL. |
| 401 | Unauthorized | Аутентификация не удалась или учетные данные не предоставлены. |
| 404 | Not Found | Исходный файл недоступен или рабочий лист/таблица не найдены. |
| 413 | Payload Too Large | Загруженная электронная таблица превышает допустимый размер. |
| 500 | Internal Server Error | Произошла ошибка при преобразовании электронной таблицы в PDF. |

## Как использовать преобразование таблицы в PDF с помощью SDK

### Спецификация преобразования таблицы в PDF

[Спецификация API преобразования таблицы в PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) определяет публично доступный программный интерфейс и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<двоичное содержимое PDF>"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

```csharp
// Пример кода SDK для C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Пример кода SDK для Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Пример кода SDK для Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`