---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Документ"
linktype: "docs"
url: /ru/cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, структура электронной таблицы, API"
description: "Структурное преобразование основных метаданных, рабочих листов, таблиц, сводных таблиц, диаграмм, фигур и другой информации из книги Excel в объект JSON типа JObject."
weight: 1000
---

## GetSpreadsheetStructure веб-сервисов Aspose.Cells Cloud

Структурное преобразование основных метаданных, рабочих листов, таблиц, сводных таблиц, диаграмм, фигур и другой информации из книги Excel в объект JSON типа JObject, для сценариев, таких как экспорт данных, ответы API и запись журналов.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищёнными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|---------------|-------|----------------------------------------|----------|
| Spreadsheet   | File  | FormData (тело)                        | Загрузка файла электронной таблицы. |
| region        | String| Query                                  | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password      | String| Query                                  | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| ------------- | --- | -------- |
| Spreadsheet   | File | Загрузка файла электронной таблицы. |

### **Ответ**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Структура электронной таблицы успешно получена. |
| 400 | Bad Request | Некорректные параметры запроса или формат файла. |
| 401 | Unauthorized | Ошибка аутентификации или отсутствует токен JWT. |
| 413 | Payload Too Large | Размер загруженного файла превышает допустимый лимит. |
| 500 | Internal Server Error | На сервере произошла непредвиденная ошибка. |

## Как использовать GetSpreadsheetStructure с SDK

### Спецификация GetSpreadsheetStructure

[Спецификация API GetSpreadsheetStructure](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose Cells Cloud. Следующий пример демонстрирует, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:
`[TBD]`
---