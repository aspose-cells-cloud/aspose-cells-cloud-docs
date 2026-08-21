---
title: "Удаление символов по позиции"
ArticleTitle: "Удаление символов по позиции – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Удаление символов по позиции"
type: docs
url: /ru/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, удаление символов, API"
description: "Удаляет символы из ячеек по позиции в электронной таблице."
weight: 100
---

## Удаление символов по позиции в веб-сервисах Aspose.Cells Cloud

Удаляет символы из каждой ячейки в целевом диапазоне по позиции (первые/последние N символов, до/после подстроки или между двумя разделителями), сохраняя формулы, форматирование и проверку данных.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра            | Тип    | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                                                                          |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | File    | FormData                    | Загрузить файл электронной таблицы.                                                                            |
| theFirstNCharacters       | Integer | Query                       | Указать удаление первых N символов из выбранных ячеек. Необязательно.                                               |
| theLastNCharacters        | Integer | Query                       | Указать удаление последних N символов из выбранных ячеек. Необязательно.                                              |
| allCharactersBeforeText   | String  | Query                       | Удалить текст, расположенный до указанной подстроки. Необязательно.                                                  |
| allCharactersAfterText    | String  | Query                       | Удалить текст, расположенный после указанной подстроки. Необязательно.                                                |
| caseSensitive             | Boolean | Query                       | Влияет на режим `Substring` и `CustomChars`, если включено. Необязательно.                                           |
| worksheet                 | String  | Query                       | Указать лист электронной таблицы. Необязательно.                                                                      |
| range                     | String  | Query                       | Указать диапазон листа электронной таблицы (например, `A1:B10`). Необязательно.                                      |
| outPath                   | String  | Query                       | (Необязательно) Путь к папке, где сохранена рабочая книга. По умолчанию — null. Необязательно.                         |
| outStorageName            | String  | Query                       | Имя хранилища выходного файла. Необязательно.                                                                        |
| region                    | String  | Query                       | Настройки региона/языка электронной таблицы (например, `en-US`, `fr-FR`). Необязательно.                              |
| password                  | String  | Query                       | Пароль для открытия файла электронной таблицы. Необязательно.                                                        |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Загрузить файл электронной таблицы. |

### **Ответ**

```json
{
  "status": "OK",
  "message": "Символы успешно удалены.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Операция завершена успешно, возвращается обработанный файл. |
| 400 | Bad Request | Запрос имеет неверный формат или содержит недопустимые параметры. |
| 401 | Unauthorized | Аутентификация не удалась или JWT-токен отсутствует/недействителен. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error | На стороне сервера произошла непредвиденная ошибка. |

## Как использовать удаление символов по позиции с SDK

### Спецификация удаления символов по позиции

[Спецификация API удаления символов по позиции](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells Cloud можно легко использовать утилиту командной строки cURL. Приведённый ниже пример демонстрирует, как выполнять вызовы в облачный API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Символы успешно удалены.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь со списком всех SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:
`[TBD]`
---