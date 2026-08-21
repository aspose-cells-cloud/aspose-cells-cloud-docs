---
title: "Импорт данных JSON в электронную таблицу"
ArticleTitle: "Импорт данных JSON в электронную таблицу – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /cells/import/data/json
aliases: []
keywords: "Импорт JSON, Aspose.Cells, Электронная таблица, API"
description: "Импорт файла данных JSON в локальную электронную таблицу."
weight: 1
---

## Импорт данных JSON в электронную таблицу с помощью облачных веб-сервисов Aspose.Cells

Импортируйте файл данных JSON в локальную электронную таблицу. Метод анализирует JSON, сопоставляет данные со структурой ячеек электронной таблицы и сохраняет файл локально. Поддерживаемые форматы электронных таблиц: .xlsx и .ods.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/HTTP-тело | Описание |
|---------------|--------|-------------------------------|----------|
| datafile      | File   | FormData                      | Загрузка файла данных. |
| Spreadsheet   | File   | FormData                      | Загрузка файла электронной таблицы. |
| worksheet     | string | Query                         | Электронная таблица, в которую необходимо импортировать данные JSON. |
| startcell     | string | Query                         | Начальная позиция для импорта данных |
| insert        | boolean| Query                         | Управляет поведением вставки. true: вставляет данные; false: перезаписывает существующие данные. (По умолчанию: true) |
| outPath       | string | Query                         | (Необязательно) Путь к папке, где хранится рабочая книга. По умолчанию — null. |
| outStorageName| string | Query                         | Имя хранилища для выходного файла. |
| fontsLocation | string | Query                         | Использование пользовательских шрифтов. |
| region        | string | Query                         | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от языкового стандарта. |
| password      | string | Query                         | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| ------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Ответ**

```json
{
  "file": "двоичный поток"
}
```

**Коды состояния ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Файл успешно сгенерирован и возвращён. |
| 400 | Bad Request | Неверный URL. |
| 401 | Unauthorized | Аутентификация не удалась или учетные данные не предоставлены. |
| 404 | Not Found | Исходный файл недоступен. |
| 413 | Payload Too Large | [TBD] |
| 500 | Internal Server Error | В электронной таблице возникла ошибка при получении данных. |

## Как использовать импорт данных JSON в электронную таблицу с помощью SDK

### Спецификация импорта данных JSON в электронную таблицу

[Спецификация API импорта данных JSON в электронную таблицу](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для легкого доступа к облачным веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}
{< tab tabNum="1" >}
```bash
# Используйте HTTPS для защищенного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "двоичный поток"
}
```
{< /tab >}
{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать облачные веб-сервисы Aspose.Cells с использованием различных SDK:  
`[TBD]`