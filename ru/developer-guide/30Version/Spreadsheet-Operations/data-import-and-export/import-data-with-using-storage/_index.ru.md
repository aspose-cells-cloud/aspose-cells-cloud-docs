---
title: "Импорт данных с использованием хранилища"
second_title: "Документ"
linktype: docs
url: /ru/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Импорт данных с использованием хранилища: импорт данных в рабочую книгу Excel с помощью API Aspose.Cells Cloud из различных источников хранилища. Поддерживает форматы JSON, CSV и другие через HTTPS."
keywords: "Aspose.Cells Cloud, Excel, импорт данных, REST API, облачное хранилище, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Импорт данных с использованием хранилища — документация API Aspose.Cells Cloud"
---

Этот REST API импортирует данные в файл Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                            |
|---------------|-------|-------------|-----------------------------------------------------|
| name          | string | path        | Имя файла Excel.                                    |
| folder        | string | query       | Путь к папке в хранилище, где расположен файл.     |
| storageName   | string | query       | Имя службы хранилища.                               |
| importData    | object | body        | JSON-объект, содержащий данные для импорта.         |

**Параметры опций импорта данных** описаны в [справочной ссылке](/cells/import/#import-data-option-parameter).

**Необходимые условия:** вы должны предоставить действительный JWT-токен в заголовке `Authorization`, а также убедиться, что целевая рабочая книга уже существует в указанном расположении хранилища.

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK (OK)                    | Фильтр успешно применён; ответ содержит данные о выполнении операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.      |
| 413 | Payload Too Large (Слишком большой объём данных) | Загруженный файл превышает лимит размера.          |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                     |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступный программный интерфейс, позволяющий выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующий пример кода демонстрирует вызов веб-сервиса Aspose.Cells с использованием PHP SDK:
---