---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, электронная таблица, структура"
description: "Получение структурных метаданных удалённой книги Excel, включая рабочие листы, таблицы, сводные таблицы, диаграммы, фигуры и другую основную информацию."
weight: 100
---

## Получение структуры удалённой электронной таблицы с помощью веб-сервисов Aspose.Cells Cloud

Структурное преобразование основных метаданных, рабочих листов, таблиц, сводных таблиц, диаграмм, фигур и другой информации книги Excel в объект JSON типа JObject для таких сценариев, как экспорт данных, ответы API и запись журналов.

### Конечная точка веб-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|----------------|------|----------------------------------------|----------|
| name | string | Path | Имя файла электронной таблицы. |
| folder | string | Query | Папка, в которой находится файл. (Необязательно) |
| storageName | string | Query | (Необязательно) Имя хранилища при использовании пользовательского облачного хранилища. Если не указано, используется хранилище по умолчанию. |
| region | string | Query | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password | string | Query | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Структура книги успешно получена. |
| 400 | Bad Request | Некорректные параметры запроса. |
| 401 | Unauthorized | Ошибка аутентификации или отсутствие токена. |
| 413 | Payload Too Large | Размер полезной нагрузки запроса превышает допустимый предел. |
| 500 | Internal Server Error | Непредвиденная ошибка сервера. |

## Как использовать получение структуры удалённой электронной таблицы с помощью SDK

### Спецификация получения структуры удалённой электронной таблицы

[Спецификация API получения структуры удалённой электронной таблицы](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) определяет публично доступный программный интерфейс и позволяет выполнять взаимодействие REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен на <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose Cells Cloud с использованием различных SDK:
`[TBD]`
---