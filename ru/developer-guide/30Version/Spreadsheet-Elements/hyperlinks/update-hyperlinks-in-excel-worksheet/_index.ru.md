---
title: "Обновление гиперссылки в листе Excel — руководство по API Aspose.Cells Cloud"
description: "Узнайте, как обновить гиперссылку в листе Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает:endpoint, параметры, схему тела запроса, пример cURL, фрагменты кода SDK, обработку ошибок, ограничение частоты запросов и предварительные требования."
keywords:
  - "Aspose.Cells"
  - "обновление гиперссылки"
  - "Excel API"
  - "REST API"
  - "облачная таблица"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Обновление гиперссылки в листе Excel  

**Версия API:** v3.0  

Операция **PostWorksheetHyperlink** обновляет существующую гиперссылку в листе, идентифицируемом по её нулевому индексу.

---

## Содержание
1. [Предварительные требования](#prerequisites)  
2. [Ограничение частоты запросов](#rate-limiting)  
3. [Конечная точка](#endpoint)  
4. [Параметры](#parameters)  
   - [Параметры пути](#path-parameters)  
   - [Параметры строки запроса](#query-parameters)  
   - [Схема тела запроса](#request-body-schema)  
5. [Ответы](#responses)  
   - [Успешный ответ](#success-response)  
   - [Ответы об ошибках](#error-responses)  
6. [Пример cURL](#curl-example)  
7. [Фрагменты кода SDK](#sdk-code-samples)  
8. [См. также](#see-also)  

---

## Предварительные требования <a name="prerequisites"></a>

| Требование | Описание |
|-------------|-------------|
| **Аутентификация** | Аутентификация на основе JWT-токенов. Получите токен, как описано в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Хранилище** | Рабочая книга должна быть сохранена в поддерживаемом облачном хранилище Aspose Cloud (по умолчанию — **Default**). |
| **Права доступа** | JWT-токен должен иметь права на чтение и запись целевой рабочей книги. |
| **Заголовки** | Для всех запросов обязательны заголовки `Content-Type: application/json` и `Accept: application/json`. |

---

## Ограничение частоты запросов <a name="rate-limiting"></a>

Aspose.Cells Cloud ограничивает количество запросов: **максимум 60 запросов в минуту на один токен доступа**. Превышение этого лимита приводит к возврату HTTP-кода **429 Too Many Requests**. При возникновении ограничения используйте экспоненциальную задержку или следуйте заголовку `Retry-After`.

---

## Конечная точка <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Обновляет гиперссылку, идентифицируемую по `hyperlinkIndex`, в листе `sheetName` файла `name`.*

---

## Параметры <a name="parameters"></a>

### Параметры пути <a name="path-parameters"></a>

| Имя             | Тип    | Обязательный | Описание |
|-----------------|--------|------------|-------------|
| `name`          | строка | ✅ | Имя файла Excel (включая расширение). |
| `sheetName`     | строка | ✅ | Имя листа, содержащего гиперссылку. |
| `hyperlinkIndex`| целое число| ✅ | Нулевой индекс обновляемой гиперссылки. |

### Параметры строки запроса <a name="query-parameters"></a>

| Имя           | Тип    | Обязательный | Описание |
|---------------|--------|------------|-------------|
| `folder`      | строка | ❌ | Путь к папке в хранилище, где находится рабочая книга. |
| `storageName` | строка | ❌ | Имя облачного хранилища (например, `Default`). |

### Схема тела запроса <a name="request-body-schema"></a>

Тело запроса должно содержать объект **`hyperlink`**. Необходимо указать только те поля, которые требуется изменить; пропущенные необязательные поля сохранят текущие значения.

| Поле            | Тип    | Обязательный | Описание |
|-----------------|--------|------------|-------------|
| `Address`       | строка | ✅ | Целевой URL-адрес гиперссылки. |
| `Area`          | объект | ✅ | Диапазон ячеек, в котором размещена гиперссылка. Должен содержать `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (все — целые числа, с нулевым индексом). |
| `ScreenTip`     | строка | ❌ | Всплывающая подсказка при наведении курсора. |
| `TextToDisplay` | строка | ❌ | Текст, отображаемый внутри ячейки. |
| `link`          | объект | ❌ | Гиперссылки (Href, Rel, Title, Type). Обычно не указываются в теле запроса. |

**Определение объекта `Area`**

| Подполе         | Тип    | Обязательный | Описание |
|-----------------|--------|------------|-------------|
| `StartRow`      | целое число | ✅ | Индекс начальной строки (с нулевым индексом). |
| `StartColumn`   | целое число | ✅ | Индекс начального столбца (с нулевым индексом). |
| `EndRow`        | целое число | ✅ | Индекс конечной строки (с нулевым индексом). |
| `EndColumn`     | целое число | ✅ | Индекс конечного столбца (с нулевым индексом). |

---

## Ответы <a name="responses"></a>

### Успешный ответ <a name="success-response"></a>

| Поле       | Тип    | Описание |
|------------|--------|-------------|
| `Code`     | целое число | HTTP-код статуса (200 — успех). |
| `Status`   | строка | Текстовое описание статуса (`OK`). |
| `Hyperlink`| объект (необязательно) | Обновлённый объект гиперссылки, возвращаемый при запросе вложенного объекта `link`. |

**Пример JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Ответы об ошибках <a name="error-responses"></a>

| HTTP-код | Причина | Пример тела ответа |
|-----------|--------|-------------------|
| **400** | Неверный запрос — отсутствуют или неверны параметры. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Неавторизован — отсутствует или недействителен JWT-токен. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Не найдено — рабочая книга, лист или гиперссылка не существуют. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | Слишком много запросов — лимит частоты превышен. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Внутренняя ошибка сервера — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Пример cURL <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Ответ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Совет:* Сохраните JSON-полезную нагрузку в файл (например, `payload.json`) и используйте `--data @payload.json` для более удобного копирования и вставки.

---

## Фрагменты кода SDK <a name="sdk-code-samples"></a>

В приведённых ниже фрагментах показано, как вызывать **PostWorksheetHyperlink** с использованием официальных SDK Aspose.Cells Cloud. Замените заглушки (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` и др.) реальными данными.

| Язык | Пример |
|------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Все SDK являются открытыми и доступны в [репозитории Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud).*

---

## См. также <a name="see-also"></a>

- **Аутентификация** – [Начало работы с JWT-токенами](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Операции с хранилищем** – [Загрузка файла](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Другие операции с гиперссылками** – [Добавление гиперссылки](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Удаление гиперссылки](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **Спецификация OpenAPI** – полное описание конечной точки: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Дата последнего обновления документа: 2026‑07‑30*