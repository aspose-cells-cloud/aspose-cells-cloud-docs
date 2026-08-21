---
title: "Импорт данных JSON в Excel"
second_title: "Документ"
linktitle: "Импорт JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, импорт JSON, Excel API, REST-импорт JSON, примеры SDK"
description: "Узнайте, как импортировать данные JSON в лист Excel с помощью REST API Aspose.Cells Cloud. Включает подробную информацию об endpoint’ах, примеры запросов и ответов, а также код SDK для .NET, Java и Python."
weight: 40
---

Этот REST API **импортирует данные JSON** в лист Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметры запроса**

| Имя параметра         | Местоположение | Тип    | Описание                                                                                      |
| --------------------- | -------------- | ------ | ---------------------------------------------------------------------------------------------- |
| name                  | Path           | string | Имя файла рабочей книги.                                                                       |
| importJsonRequest     | Тело HTTP      | class  | Полезная нагрузка запроса, содержащая сведения об импорте JSON.                               |
| password              | Строка запроса | string | Пароль для открытия рабочей книги (если она защищена).                                        |
| folder                | Строка запроса | string | Папка, содержащая исходную рабочую книгу.                                                     |
| storageName           | Строка запроса | string | Имя хранилища, в котором находится рабочая книга.                                             |
| outPath               | Строка запроса | string | Путь к выходному файлу после импорта. Если не указан, обновлённая рабочая книга возвращается в ответе. |
| outStorageName        | Строка запроса | string | Имя хранилища для выходного файла.                                                             |
| checkExcelRestriction | Строка запроса | string | Флаг, указывающий, следует ли применять ограничения, специфичные для Excel (true/false).      |

### **Пример тела запроса**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Ответ

Успешный запрос возвращает **HTTP 200** с JSON-полезной нагрузкой, подобной следующей:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Возможные коды состояния:

| Код | Значение                                        |
| ---- | ----------------------------------------------- |
| 200  | Импорт выполнен успешно                         |
| 400  | Неверный запрос — отсутствующие или некорректные данные |
| 401  | Ошибка авторизации — неверный или отсутствующий токен |
| 500  | Внутренняя ошибка сервера                       |


## Как использовать API PostWorkbookImportJson с SDK

### Спецификация API PostWorkbookImportJson

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — наиболее эффективный способ ускорить разработку. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен на [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK: