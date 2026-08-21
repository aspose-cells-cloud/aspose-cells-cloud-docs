---
title: "Принять все изменения"
ArticleTitle: "Принять все изменения – Aspose.Cells Cloud"
second_title: "Документ"
linktype: "Принять все изменения"
type: docs
url: /ru/cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, электронная таблица, изменения"
description: "Принять все изменения в файле электронной таблицы с использованием API Aspose.Cells Cloud."
weight: 100
---

## Принять все изменения в веб-сервисах Aspose.Cells Cloud

Принимает все изменения в загруженном файле электронной таблицы и возвращает обработанный рабочий файл.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе маркера JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|---------------|-------|----------------------------------------|----------|
| Spreadsheet   | File  | FormData (Тело HTTP-запроса)           | Загрузка файла электронной таблицы. |
| outPath       | string | Query                                 | (Необязательно) Путь к папке, где хранится рабочий файл. По умолчанию — null. |
| outStorageName| string | Query                                 | Имя хранилища для выходного файла. |
| fontsLocation | string | Query                                 | Использование пользовательских шрифтов. |
| region        | string | Query                                 | Параметры региона/языка электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password      | string | Query                                 | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
|---------------|-----|----------|
| Spreadsheet   | File | Загрузка файла электронной таблицы. |

### **Ответ**

```json
{
  "File": "Бинарный поток обработанной электронной таблицы"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Изменения успешно приняты, обработанный файл возвращён. |
| 400 | Bad Request | Неверный запрос (например, отсутствует обязательный файл или указаны некорректные параметры). |
| 401 | Unauthorized | Ошибка аутентификации или отсутствует/недействителен маркер JWT. |
| 413 | Payload Too Large | Размер загруженного файла превышает допустимый лимит. |
| 500 | Internal Server Error | На сервере произошла непредвиденная ошибка. |

## Как использовать AcceptAllRevisions с SDK

### Спецификация AcceptAllRevisions

[Спецификация API AcceptAllRevisions](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "Бинарный поток обработанной электронной таблицы"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь с <a href="[TBD]" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:
 `[TBD]`
---