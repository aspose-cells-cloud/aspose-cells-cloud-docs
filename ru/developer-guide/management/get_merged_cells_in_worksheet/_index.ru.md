---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Получение объединённых ячеек в листе — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, объединённые ячейки, лист, API"
description: "Получить все объединённые области ячеек из локального файла электронной таблицы."
weight: 1000
---

## Получение объединённых ячеек в листе с помощью веб-сервисов Aspose.Cells Cloud

Получить все объединённые области ячеек из локального файла электронной таблицы.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|----------------|------|---------------------------------------|----------|
| Spreadsheet | File | FormData | Загрузка файла электронной таблицы. |
| worksheet | String | Query | Имя листа. |
| region | String | Query | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password | String | Query | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| N/A | N/A | Эта операция не принимает JSON-тело; файл электронной таблицы отправляется через `multipart/form-data`. |

### **Ответ**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Коды статуса ответа**

| Код | Значение | Описание |
|------|---------|----------|
| 200 | OK | Объединённые области ячеек успешно получены. |
| 400 | Bad Request | Один или несколько параметров запроса недопустимы или отсутствуют. |
| 401 | Unauthorized | Ошибка аутентификации — недопустимый или отсутствующий токен JWT. |
| 413 | Payload Too Large | Загруженный файл электронной таблицы превышает допустимый размер. |
| 500 | Internal Server Error | На сервере произошла непредвиденная ошибка. |

## Как использовать получение объединённых ячеек в листе с помощью SDK

### Спецификация API получения объединённых ячеек в листе

[Спецификация API получения объединённых ячеек в листе](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:
 `[TBD]`
---