---
---
title: "Удаление столбца из рабочего листа Excel с помощью Aspose.Cells Cloud API"
description: "Узнайте, как удалить один или несколько столбцов из рабочего листа Excel с помощью REST API Aspose.Cells Cloud. Включает аутентификацию, синтаксис запроса, параметры, ответы, обработку ошибок и примеры SDK."
keywords: ["Aspose.Cells", "Удаление столбца", "Excel API", "REST", "Облако", "Рабочий лист", "Столбцы"]
date: 2026-07-30
api_version: "v3.0"
---

# Удаление столбца из рабочего листа Excel

**Конечная точка**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

Операция удаляет один столбец или диапазон столбцов из рабочего листа. Ссылки на ячейки (включая формулы) могут быть автоматически обновлены после удаления.

---

## Содержание
1. [Необходимые условия](#prerequisites)  
2. [Аутентификация](#authentication)  
3. [URL-адрес запроса и HTTP-метод](#request-url--http-method)  
4. [Параметры](#parameters)  
   - [Параметры пути](#path-parameters)  
   - [Параметры запроса](#query-parameters)  
5. [Пример cURL](#curl-example)  
6. [Ответы](#responses)  
7. [Коды ошибок](#error-codes)  
8. [Примеры SDK](#sdk-samples)  
9. [Дополнительные примечания](#additional-notes)  

---

## Необходимые условия
- Действующий **JWT-токен доступа**, полученный в рамках процесса аутентификации Aspose Cloud.  
- Книга (`{name}`) должна быть уже загружена в облачное хранилище Aspose Cloud (или доступна через параметры запроса `folder`/`storageName`).  

---

## Аутентификация
Все запросы к Aspose.Cells Cloud требуют аутентификации по токену **Bearer**.

```http
Authorization: Bearer <access_token>
```

Дополнительные сведения о получении JWT-токена см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## URL-адрес запроса и HTTP-метод
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – имя файла книги (например, `test.xlsx`).  
- **`{sheetName}`** – имя рабочего листа (например, `Sheet1`).  
- **`{columnIndex}`** – индекс первого удаляемого столбца (начиная с нуля).

---

## Параметры

| Имя             | Местоположение | Тип    | Обязательный | Описание |
|-----------------|----------------|--------|-------------|----------|
| **name**        | path           | string | ✅ Да       | Имя файла книги. |
| **sheetName**   | path           | string | ✅ Да       | Имя рабочего листа. |
| **columnIndex** | path           | integer| ✅ Да       | Индекс первого удаляемого столбца (начиная с нуля). |
| **startColumn** | query          | integer| ❌ Нет      | Индекс столбца, с которого начинается удаление (начиная с нуля). Если не указан, по умолчанию используется `columnIndex`. |
| **totalColumns**| query          | integer| ❌ Нет      | Количество удаляемых столбцов. Если не указано, удаляется только столбец, указанный в `columnIndex`. |
| **updateReference** | query     | boolean| ❌ Нет      | Если `true`, обновляет ссылки на ячейки (включая формулы) по всей книге после удаления. |
| **folder**      | query          | string | ❌ Нет      | Путь к папке, содержащей книгу. |
| **storageName** | query          | string | ❌ Нет      | Имя облачного сервиса хранилища Aspose Cloud. |

> **Примечание** – Параметр `columns`, указанный в спецификации низкоуровневого API, устарел и заменён более выразительными параметрами запроса `startColumn` и `totalColumns`. Оба подхода поддерживаются для обратной совместимости.

---

## Пример cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Пояснение
- Удаляет столбец **B** (`columnIndex = 1`) из `Sheet1` файла `test.xlsx`.  
- Параметры `startColumn=1` и `totalColumns=1` задают удаление одного столбца.  
- Параметр `updateReference=true` обеспечивает автоматическую корректировку формул и других ссылок.

---

## Ответы

| HTTP-код | Описание | Пример |
|----------|----------|--------|
| **200** | Успех — столбцы удалены. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | Неавторизовано — отсутствует или недействителен JWT-токен. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | Не найдено — книга или рабочий лист не существуют. | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | Внутренняя ошибка сервера — непредвиденное состояние на стороне сервера. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

Тело ответа соответствует общей модели **`CellsCloudResponse`**.

---

**HTTP-коды состояния**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загружаемый файл превышает допустимый размер. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |
---

## Примеры SDK

Ниже приведены готовые к запуску фрагменты кода для наиболее популярных SDK. Замените шаблонные значения (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` и т.д.) на свои данные.

| Язык | Пример |
|------|--------|
| **C#** | <details><summary>Показать код</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Показать код</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Показать код</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Показать код</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Показать код</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Показать код</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Показать код</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Показать код</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*Все SDK автоматически добавляют необходимый заголовок `Authorization`, если указан `access_token`.*

---

## Дополнительные примечания

### Заголовки безопасности (рекомендуется для production-среды)
При обслуживании страницы документации добавьте следующие HTTP-заголовки ответа для повышения безопасности:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Советы по производительности
- Загружайте сторонние скрипты аналитики (`gtag.js`, `containerize.js`) с атрибутом `async` или откладывайте их выполнение до после отрисовки страницы.  
- Минифицируйте собственные пакеты JavaScript/CSS.  
- Предварительно загружайте небольшие SVG-иконки, если они блокируют рендеринг:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### Улучшения SEO (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Узнайте, как удалить один или несколько столбцов из рабочего листа Excel с помощью REST API Aspose.Cells Cloud.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Удаление столбца", "Excel", "REST API"]
}
```

Вставьте фрагмент внутрь блока `<script type="application/ld+json">` в `<head>` HTML-страницы.

### Доступность
- Все декоративные изображения имеют `alt=""` или скрыты с помощью `aria-hidden="true"`.  
- Изображение Open Graph теперь включает атрибут `alt` в мета-теге для полноты.

---

## См. также
- [OpenAPI-спецификация для DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Обзор аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDK Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud)  

---
---