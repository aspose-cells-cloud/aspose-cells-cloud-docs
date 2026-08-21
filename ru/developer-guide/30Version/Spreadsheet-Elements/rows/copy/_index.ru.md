---
title: "Копирование строк в листе Excel"
description: "Копирование данных и форматов из конкретных строк в листе Excel с использованием REST API Aspose.Cells Cloud (v3.0). Включает аутентификацию, детали запроса и ответа, обработку ошибок и примеры SDK."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Копирование строк в листе Excel <span style="float:right;">v3.0</span>

Копирование данных и форматов из указанных целых строк листа.

---

## Необходимые условия

| № | Требование |
|---|-------------|
| 1 | Действующий токен **JWT**. Подробности см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | Рабочая книга (`{name}`) уже должна существовать в выбранной **папке** / **хранилище**. |
| 3 | Целевой лист (`{sheetName}`) должен присутствовать в рабочей книге. |
| 4 | (Опционально) Укажите **папку** и **storageName**, если файл находится не в папке по умолчанию. |

---

## Конечная точка

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Все параметры пути чувствительны к регистру.*

### Параметры пути

| Параметр | Тип   | Обязательный | Описание |
|----------|--------|--------------|----------|
| `name`    | строка | ✅ | Имя файла рабочей книги (например, `test.xlsx`). |
| `sheetName` | строка | ✅ | Имя листа (например, `Sheet1`). |

### Параметры запроса

| Параметр            | Тип    | Обязательный | Описание |
|---------------------|--------|--------------|----------|
| `sourceRowIndex`     | целое число | ✅ | Индекс исходной строки (начиная с 0). |
| `destinationRowIndex`| целое число | ✅ | Индекс строки, на которую будут скопированы данные (начиная с 0). |
| `rowNumber`          | целое число | ✅ | Количество копируемых строк. |
| `worksheet`          | строка  | ❌ | Идентификатор листа; обычно совпадает с **sheetName**. |
| `folder`             | строка  | ❌ | Путь к папке, содержащей рабочую книгу. |
| `storageName`        | строка  | ❌ | Имя сервиса хранилища. |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Примечание**  
> Замените `<jwt token>` на действующий JWT-токен, полученный от сервиса аутентификации.

---

## Успешный ответ

| Код | Описание |
|-----|----------|
| **200** | Строки успешно скопированы. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Тело ответа представляет собой экземпляр `CellsCloudResponse`.

---

## Обработка ошибок

| HTTP-код | Значение                              | Пример тела ответа |
|----------|---------------------------------------|--------------------|
| **400**   | Неверный запрос — отсутствующие/неверные параметры. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | Неавторизованный доступ — неверный или отсутствующий JWT-токен. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Не найдено — рабочая книга или лист не существуют. | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | Внутренняя ошибка сервера — непредвиденное состояние сервера. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Рекомендации по устранению**

* **400** — Убедитесь, что все обязательные параметры запроса присутствуют и корректно сформатированы.  
* **401** — Повторно сгенерируйте или обновите JWT-токен.  
* **404** — Проверьте имена рабочей книги и листа, а также убедитесь, что файл существует в указанной папке/хранилище.  
* **500** — Повторите запрос через короткую задержку; при повторении ошибки обратитесь в службу поддержки Aspose.

---

## Примеры SDK

Ниже приведены фрагменты кода, демонстрирующие вызов операции **Copy Rows** с использованием официальных SDK Aspose.Cells Cloud.

| Язык | Пример |
|------|--------|
| **C#**   | <details><summary>Показать код</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Показать код</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Показать код</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Показать код</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Показать код</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient("clientId", "clientSecret")\n_, err := api.PostCopyWorksheetRows(context.Background(), "test.xlsx", "Sheet1", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Показать код</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Показать код</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Показать код</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Полные исходные файлы доступны в репозитории [Aspose‑Cells‑Cloud на GitHub](https://github.com/aspose-cells-cloud).*

---

## См. также

- [Добавление строки в листе Excel](/rows/add/)  
- [Удаление строки в листе Excel](/rows/delete/)  
- [Обновление строки в листе Excel](/rows/update/)  

---

*Страница сгенерирована **{{DATE}}**. Последнюю версию этого API см. в [спецификации OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*