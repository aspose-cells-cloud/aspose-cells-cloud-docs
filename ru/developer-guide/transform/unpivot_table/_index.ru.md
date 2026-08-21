---
title: "Развернуть таблицу"
ArticleTitle: "Развернуть таблицу – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Развернуть таблицу"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, развернуть, трансформировать"
description: "Поменять местами строки и столбцы в электронной таблице."
weight: 1
---

## Развертывание таблицы с помощью облачных веб-сервисов Aspose.Cells

Поменять местами строки и столбцы в электронной таблице.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра   | Тип    | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                                                                            |
|------------------|---------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                               | Загрузка файла электронной таблицы.                                                                                  |
| worksheet        | String  | Query                                  | Имя рабочего листа.                                                                                                   |
| index            | Integer | Query                                  | Указанный диапазон данных.                                                                                            |
| skipEmptyValue   | Boolean | Query                                  | Пропустить пустые значения (по умолчанию: true).                                                                     |
| outPath          | String  | Query                                  | (Необязательно) Путь к папке, где сохраняется рабочая книга. По умолчанию — null.                                   |
| outStorageName   | String  | Query                                  | Имя хранилища для выходного файла.                                                                                    |
| region           | String  | Query                                  | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияют на форматирование чисел, разбор дат и поведение, зависящее от региона. |
| password         | String  | Query                                  | Пароль для открытия файла электронной таблицы.                                                                       |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| N/A            | N/A  | Параметры тела запроса отсутствуют. |

### **Ответ**

```json
{
  "File": "двоичный поток развернутой электронной таблицы"
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Возвращается файл развернутой электронной таблицы. |
| 400 | Bad Request | Неверные параметры запроса. |
| 401 | Unauthorized | Ошибка аутентификации или отсутствует/недействителен JWT-токен. |
| 413 | Payload Too Large | Размер загруженного файла превышает допустимый предел. |
| 500 | Internal Server Error | Непредвиденная ошибка сервера. |

## Как использовать развертывание таблицы с помощью SDK

### Спецификация API развертывания таблицы

[Спецификация API развертывания таблицы](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищенного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "двоичный поток развернутой электронной таблицы"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK скрывает детали низкоуровневой реализации, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:
 `[TBD]`
---