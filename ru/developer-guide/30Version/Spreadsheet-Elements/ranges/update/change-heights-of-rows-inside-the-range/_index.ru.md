---
title: "Установка высоты строк для диапазона в Excel — Aspose.Cells Cloud API (v3.0)"
description: "Измените высоту строк в заданном диапазоне рабочего листа Excel с помощью REST API Aspose.Cells Cloud. Включает URL-адрес, параметры, пример cURL, образцы ответов и фрагменты кода SDK для нескольких языков."
keywords: "Aspose.Cells, высота строк, диапазон, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Установка высоты строк для диапазона в Excel

Эта операция обновляет высоту строк в указанном диапазоне рабочего листа, хранящегося в облачном хранилище Aspose Cloud.

## Предварительные требования / Аутентификация

Вы должны получить JWT-токен доступа из службы OAuth Aspose Cloud с областью **Cells.ReadWrite**.

Включите токен в заголовок `Authorization` каждого запроса:

```http
Authorization: Bearer <jwt token>
```

Если у вас нет токена, следуйте руководству **Аутентификация в Aspose Cloud**, чтобы запросить его.

## HTTP-запрос

| Метод | URI |
|-------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Параметры пути

| Имя | Тип | Описание |
|-----|-----|----------|
| `name` | `string` | **Обязательный.** Имя файла Excel, хранящегося в облаке. |
| `sheetName` | `string` | **Обязательный.** Рабочий лист, содержащий целевой диапазон. |

### Параметры запроса

| Имя | Тип | Обязательный | Описание |
|-----|-----|-------------|----------|
| `value` | `number` | **Да** | Желаемая высота строк (в пунктах) для применения к диапазону. |
| `folder` | `string` | Нет | Путь к папке в хранилище, где находится файл. |
| `storageName` | `string` | Нет | Имя сервиса хранилища (если настроено несколько хранилищ). |

### Тело запроса (JSON)

Тело должно содержать объект **Range**, определяющий, какие строки будут затронуты.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Схема JSON объекта Range

| Свойство | Тип | Обязательный | Описание |
|----------|-----|-------------|----------|
| `FirstRow` | integer | **Да** | Индекс первой строки в диапазоне (начинается с 0). |
| `RowCount` | integer | **Да** | Количество строк, к которым будет применена высота. |
| `FirstColumn` | integer | Нет | Индекс первого столбца (начинается с 0) — необязательный параметр для операции установки высоты строк. |
| `ColumnCount` | integer | Нет | Количество столбцов, охватываемых диапазоном (необязательно). |

Для операции установки высоты строк используются только указанные выше свойства; любые дополнительные поля игнорируются.

## Пример запроса

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Пример ответа (успех)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|-----|------------------------------|-----------------------------------------------|
| 200 | OK (ОК)                      | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

Все ответы содержат числовое поле `Code` и понятное человеку поле `Status` (или `Message` при ошибках). При возникновении ошибки могут быть предоставлены дополнительные сведения в `ErrorDetails`.

## Примеры SDK

Следующие фрагменты демонстрируют вызов операции **Установка высоты строк для диапазона** с использованием официальных SDK Aspose.Cells Cloud.

| Язык | Пример |
|------|--------|
| **C#** | <details><summary>Показать код</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Показать код</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Показать код</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Показать код</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Показать код</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Показать код</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Показать код</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Показать код</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Примечание:** Все SDK автоматически добавляют обязательный заголовок `Authorization: Bearer`, если токен доступа настроен.

## См. также

- **Спецификация OpenAPI** – подробный контракт для этой операции: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Репозиторий SDK Aspose.Cells Cloud** – исходный код и дополнительные привязки для других языков: <https://github.com/aspose-cells-cloud>
- **Руководство по аутентификации** – как получить JWT-токен: <https://docs.aspose.cloud/cells/authentication/>

---