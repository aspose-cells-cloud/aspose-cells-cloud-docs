---
title: "Преобразование рабочего листа в HTML-таблицу"
ArticleTitle: "Преобразование рабочего листа в HTML-таблицу – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "ConvertWorksheetToHtmlTable"
type: docs
url: /ru/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML-таблица, API"
description: "Преобразует рабочий лист электронной таблицы, расположенной на локальном диске, в файл HTML-таблицы с помощью Aspose.Cells Cloud."
weight: 100
---

## Преобразование рабочего листа в HTML-таблицу в веб-сервисах Aspose.Cells Cloud

Эта операция считывает файл электронной таблицы из локальной файловой системы, преобразует указанный рабочий лист в HTML-таблицу и возвращает результат преобразования в виде потока данных файла. Преобразование выполняется полностью на облачном сервере, поэтому промежуточная загрузка в облачное хранилище не требуется. Поддерживаются дополнительные настройки локали и защищенные паролем рабочие книги.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/HTTP-тело | Описание |
|---------------|-------|-------------------------------|----------|
| Spreadsheet   | File  | FormData                      | Загрузка файла электронной таблицы. |
| worksheet     | String| Query                         | Имя рабочего листа электронной таблицы. (обязательно) |
| region        | String| Query                         | Регион/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password      | String| Query                         | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| ------------- | --- | -------- |
| *None*        | *None* | *Тело в формате JSON не требуется; файл передаётся как multipart/form-data.* |

### **Ответ**

```json
{
  "File": "двоичный поток сгенерированной HTML-таблицы"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Рабочий лист успешно преобразован в HTML-таблицу и возвращён как поток данных файла. |
| 400 | Bad Request | Неверный URL-адрес запроса или отсутствуют обязательные параметры. |
| 401 | Unauthorized | Аутентификация не удалась или учётные данные не были предоставлены. |
| 404 | Not Found | Исходный файл недоступен. |
| 500 | Internal Server Error | При получении данных для преобразования в электронной таблице возникла ошибка. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый размер. |

## Как использовать преобразование рабочего листа в HTML-таблицу с помощью SDK

### Спецификация преобразования рабочего листа в HTML-таблицу

[Спецификация API преобразования рабочего листа в HTML-таблицу](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "двоичный поток сгенерированной HTML-таблицы"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:
`[TBD]`
---