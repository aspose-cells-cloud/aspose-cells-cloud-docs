---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "TransposeData"
type: docs
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, облачный API, электронная таблица, транспонирование"
description: "Поменять местами строки и столбцы в электронной таблице."
weight: 1000
---

## TransposeData в веб-сервисах Aspose.Cells Cloud

Поменять местами строки и столбцы в электронной таблице.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра   | Тип   | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                            |
|------------------|--------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Загрузить файл электронной таблицы.                                                                                                               |
| worksheet        | String | Query                       | Имя листа.                                                                                                                    |
| cellArea         | String | Query                       | Указанный диапазон данных.                                                                                                                |
| outPath          | String | Query                       | (Необязательно) Путь к папке, где сохраняется рабочая книга. По умолчанию — null.                                                          |
| outStorageName   | String | Query                       | Имя хранилища выходного файла.                                                                                                              |
| region           | String | Query                       | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияют на форматирование чисел, разбор дат и поведение, зависящее от языка и региона. |
| password         | String | Query                       | Пароль для открытия файла электронной таблицы.                                                                                             |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **Ответ**

```json
{
  "file": "двоичный поток транспонированной электронной таблицы"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Файл транспонированной электронной таблицы возвращён. |
| 400 | Bad Request | Недопустимые входные параметры или некорректно сформированный запрос. |
| 401 | Unauthorized | Ошибка аутентификации или отсутствующий/недействительный JWT-токен. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error | Непредвиденная ошибка сервера. |

## Как использовать TransposeData с SDK

### Спецификация TransposeData

[Спецификация API TransposeData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. Пример ниже показывает, как сделать вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "двоичный поток транспонированной электронной таблицы"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

В приведённых ниже примерах кода показано, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:
`[TBD]`
---