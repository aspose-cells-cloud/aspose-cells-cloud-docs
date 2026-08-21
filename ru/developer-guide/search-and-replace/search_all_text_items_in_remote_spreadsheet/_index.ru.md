---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /ru/cells/{name}/search/content/all-textitems
aliases: []
keywords: "поиск, текстовые элементы, Aspose.Cells"
description: "Поиск всех текстовых элементов в удалённой электронной таблице с использованием Aspose.Cells Cloud."
weight: 100
---

## Метод SearchAllTextItemsInRemoteSpreadsheet веб-сервисов Aspose.Cells Cloud

Этот метод выполняет поиск всех текстовых элементов в удалённом файле электронной таблицы. Он поддерживает поиск по всем листам и ячейкам книги, выявляя вхождения искомого термина. Операция выполняется в облаке, не требуя локального хранилища. Убедитесь, что у вас есть необходимые права на чтение исходного файла. Если исходный файл недоступен или во время поиска возникает ошибка (например, неподдерживаемый формат файла), будет сгенерировано соответствующее исключение. Возвращаемые данные могут включать местоположения совпадений (например, имя листа, координаты ячейки) в зависимости от деталей реализации.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|---------------|-------|----------------------------------------|----------|
| name          | string | Path                                  | Имя файла книги. |
| folder        | string | Query                                 | Путь к папке, в которой хранится книга. |
| storageName   | string | Query                                 | (Необязательно) Имя хранилища при использовании пользовательского облачного хранилища. Если параметр не указан, используется хранилище по умолчанию. |
| region        | string | Query                                 | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от языкового стандарта. |
| password      | string | Query                                 | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| [TBD]          |      | [TBD] |

### **Ответ**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Коды статусов ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Запрос выполнен успешно, в ответе содержатся все найденные текстовые элементы в электронной таблице. |
| 400 | Bad Request | Неверный URL-адрес или параметры запроса. |
| 401 | Unauthorized | Аутентификация не удалась или не предоставлены учётные данные. |
| 404 | Not Found | Исходный файл недоступен. |
| 413 | Payload Too Large | Размер полезной нагрузки запроса превышает допустимый предел. |
| 500 | Internal Server Error | В ходе получения данных из электронной таблицы возникла ошибка. |

## Как использовать SearchAllTextItemsInRemoteSpreadsheet с SDK

### Спецификация SearchAllTextItemsInRemoteSpreadsheet

[Спецификация API SearchAllTextItemsInRemoteSpreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Лист1",
      "CellAddress": "A1",
      "Text": "Образцовый текст"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со списком всех SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose Cells Cloud с использованием различных SDK:
`[TBD]`
---