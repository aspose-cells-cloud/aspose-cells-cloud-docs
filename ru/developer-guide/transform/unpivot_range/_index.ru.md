---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "UnpivotRange"
type: docs
url: /ru/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Меняет местами строки и столбцы в электронной таблице."
weight: 10
---

## UnpivotRange в веб-сервисах Aspose.Cells Cloud

Меняет местами строки и столбцы в электронной таблице.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра   | Тип   | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Файл   | FormData                    | Загружаемый файл электронной таблицы.                                                                                                                         |
| worksheet        | string | Query                       | Имя рабочего листа.                                                                                                                                           |
| cellArea         | string | Query                       | Указанный диапазон данных.                                                                                                                                     |
| skipEmptyValue   | boolean| Query                       | Если значение true, пустые значения пропускаются. По умолчанию: true.                                                                                         |
| outPath          | string | Query                       | (Необязательно) Путь к папке, где сохраняется рабочая книга. По умолчанию — null.                                                                            |
| outStorageName   | string | Query                       | Имя хранилища для выходного файла.                                                                                                                            |
| region           | string | Query                       | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияют на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password         | string | Query                       | Пароль для открытия файла электронной таблицы.                                                                                                               |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
|----------------|------|-------------|
| — | — | — |

### **Ответ**

```json
{
  "File": "binary stream"
}
```

**Коды статусов ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Возвращается файл электронной таблицы без сводной таблицы. |
| 400 | Bad Request | Недопустимые параметры запроса. |
| 401 | Unauthorized | Ошибка аутентификации. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error | На сервере возникло непредвиденное состояние. |

## Как использовать UnpivotRange с SDK

### Спецификация UnpivotRange

[Спецификация API UnpivotRange](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. Пример ниже демонстрирует, как выполнить вызов облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищенного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK скрывает детали низкоуровневой реализации, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose Cells Cloud с использованием различных SDK:
 `[TBD]`
---