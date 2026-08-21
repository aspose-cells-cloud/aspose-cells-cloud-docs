---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Получение объединённых ячеек в удалённом листе – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /ru/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, получение объединённых ячеек, удалённый лист, API"
description: "Получает все области объединённых ячеек из удалённого листа электронной таблицы."
weight: 10
---

## Метод GetMergedCellsInRemotedWorksheet веб-сервисов Aspose.Cells Cloud

Получает все области объединённых ячеек из удалённого листа электронной таблицы.

### Конечная точка веб-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип | Путь/Строка запроса/HTTP-тело | Описание |
|---------------|------|-------------------------------|----------|
| name | string | Путь | Имя электронной таблицы |
| worksheet | string | Путь | Имя листа |
| folder | string | Запрос | Путь к облачному хранилищу электронной таблицы |
| storageName | string | Запрос | (Необязательно) Имя хранилища при использовании пользовательского облачного хранилища. По умолчанию используется хранилище по умолчанию. |
| region | string | Запрос | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали |
| password | string | Запрос | Пароль для открытия файла электронной таблицы |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| ------------- | --- | -------- |
| — | — | *Нет* |

### **Ответ**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Коды статусов ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Запрос выполнен успешно, возвращён список областей объединённых ячеек |
| 400 | Bad Request | Неверный URL или некорректно сформированные параметры запроса |
| 401 | Unauthorized | Аутентификация не удалась или не предоставлены учётные данные |
| 413 | Payload Too Large | Размер полезной нагрузки запроса превышает допустимый предел |
| 500 | Internal Server Error | Произошла ошибка при получении данных из электронной таблицы |

## Как использовать GetMergedCellsInRemotedWorksheet с SDK

### Спецификация GetMergedCellsInRemotedWorksheet

[Спецификация API GetMergedCellsInRemotedWorksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со списком всех SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:
`[TBD]`
---