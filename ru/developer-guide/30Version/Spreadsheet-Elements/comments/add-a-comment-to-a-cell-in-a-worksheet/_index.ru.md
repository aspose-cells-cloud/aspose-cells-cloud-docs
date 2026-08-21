---
---
title: "Добавить комментарий к листу"
description: "Добавить комментарий к определённой ячейке на листе Excel-книги с использованием REST API Aspose.Cells Cloud (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, облачный API, добавление комментария к листу, Excel, электронная таблица, комментарий к ячейке"
weight: 20
api_version: "v3.0"
---

# Добавить комментарий к листу

Добавьте комментарий к определённой ячейке на листе Excel-книги с использованием REST API Aspose.Cells Cloud.

---

## Предварительные требования / Аутентификация

* Для каждого запроса требуется **Bearer JWT-токен**.  
  *Получить токен* можно через endpoint **/connect/token** (см. [Руководство по аутентификации](/cells/authentication/)).  
* Включите токен в заголовок `Authorization`:

```http
Authorization: Bearer <jwt token>
```

* Все вызовы должны выполняться по протоколу **HTTPS** для защиты токена и данных.

---

## HTTP-запрос

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Параметры пути

| Имя        | Тип    | Обязательный | Описание |
|-----------|--------|-------------|----------|
| `name`    | string | ✔️ | Имя файла книги (например, `test.xlsx`). |
| `sheetName` | string | ✔️ | Имя листа (например, `Sheet1`). |
| `cellName` | string | ✔️ | Адрес целевой ячейки (например, `A1`). |

### Параметры запроса

| Имя           | Тип    | Обязательный | Описание |
|---------------|--------|-------------|----------|
| `folder`      | string | опционально | Папка, содержащая книгу. |
| `storageName` | string | опционально | Имя сервиса хранилища, где расположен файл. |

### Тело запроса

Тело должно содержать объект **Comment** в формате JSON.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Поля объекта Comment**

| Поле                      | Тип     | Обязательное | Описание |
|---------------------------|---------|--------------|----------|
| `CellName`                | string  | ✔️ | Адрес ячейки (должен совпадать со значением `{cellName}` в пути). |
| `Author`                  | string  | опционально | Имя автора комментария. |
| `HtmlNote`                | string  | опционально | Текст комментария в формате HTML. |
| `Note`                    | string  | опционально | Текст комментария в обычном формате. |
| `AutoSize`                | boolean | опционально | Автоматическая подстройка размера поля комментария. |
| `IsVisible`               | boolean | опционально | Показывать комментарий по умолчанию. |
| `Width` / `Height`        | number  | опционально | Размер поля комментария (в пунктах). |
| `TextHorizontalAlignment`| string  | опционально | Горизонтальное выравнивание (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | string  | опционально | Ориентация текста (`NoRotation`, `Rotate90`, …). |
| `TextVerticalAlignment`  | string  | опционально | Вертикальное выравнивание (`Top`, `Center`, `Bottom`). |

---

## Пример cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Схема ответа

| Поле    | Тип    | Описание |
|---------|--------|----------|
| `Comment` | object | Созданный объект комментария (см. **Поля объекта Comment** выше, плюс метаданные ссылки). |
| `Code`   | integer | Код HTTP-статуса, возвращаемый API (например, `200`). |
| `Status` | string  | Текстовое сообщение о статусе (например, `"OK"`). |

Объект `Comment` также содержит подобъект **link**:

| Подполе    | Тип    | Описание |
|------------|--------|----------|
| `Href`     | string | URL-адрес для обращения к самому ресурсу комментария. |
| `Rel`      | string | Тип связи (`self`). |
| `Title`    | string | Необязательный заголовок (может быть `null`). |
| `Type`     | string | Необязательный MIME-тип (может быть `null`). |

---

## Пример успешного ответа

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Ответы об ошибках

| HTTP-код | Описание | Пример |
|----------|----------|--------|
| **400**  | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**  | Неавторизованный доступ — токен отсутствует или недействителен. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**  | Не найдено — книга, лист или ячейка не существует. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**  | Внутренняя ошибка сервера — неожиданное условие на сервере. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## Примеры SDK

Ниже приведены готовые обёртки для данной операции в различных SDK. Замените значения-заглушки (`<YOUR_TOKEN>`, `<FILE_NAME>` и т.д.) на реальные данные.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Настройка клиента API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Подготовка объекта комментария
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## См. также

* **Получить комментарий к листу** — `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Обновить комментарий к листу** — `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Удалить комментарий к листу** — `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Очистить все комментарии** — `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Дополнительные примечания

* Путь endpoint содержит **v3.0**. Доступна более новая версия (**v3.1**); обновите базовый URL, если вам нужны последние функции.  
* Полное определение OpenAPI доступно по ссылке: [Aspose.Cells Cloud API reference](/cells/#/Worksheets/PutWorksheetComment).  
* Не забывайте обрабатывать ограничение частоты запросов (HTTP 429) и повторять запросы в соответствии с рекомендациями API.  

---
---