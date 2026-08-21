---
title: "Удаление гиперссылки на листе"
type: docs
url: /ru/hyperlinks/delete/
description: "Удалите гиперссылку на листе по индексу с помощью API Aspose.Cells Cloud. Узнайте необходимые параметры, аутентификацию и посмотрите примеры кода для C#, Java, Python и других языков."
keywords: "Aspose.Cells, облако, удаление гиперссылки, Excel API, REST, гиперссылка на листе"
ArticleTitle: "Удаление гиперссылки на листе – документация API Aspose.Cells Cloud"
weight: 40
---

Этот REST API удаляет гиперссылку на листе Excel по её индексу.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации по токену JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Параметры запроса

| Имя параметра    | Тип     | Расположение | Обязательный | Описание                                                     |
| ---------------- | ------- | ------------ | ------------ | ------------------------------------------------------------ |
| **name**         | string  | путь         | ✅           | Имя документа Excel.                                         |
| **sheetName**    | string  | путь         | ✅           | Имя листа.                                                   |
| **hyperlinkIndex** | integer | путь         | ✅           | Индекс удаляемой гиперссылки (начинается с нуля).            |
| **folder**       | string  | параметр запроса | ❌        | Папка, содержащая документ (по умолчанию: корневая).         |
| **storageName**  | string  | параметр запроса | ❌        | Имя сервиса хранения (если не указано, используется хранилище по умолчанию). |

#### Ответы

| Код состояния                | Описание                                               | Пример тела ответа                                |
| ---------------------------- | ------------------------------------------------------ | ------------------------------------------------- |
| **200 OK**                   | Гиперссылка успешно удалена.                           | `{"Code":200,"Status":"OK"}`                      |
| **400 Bad Request**          | Отсутствуют или некорректны параметры запроса.        | `{"Code":400,"Message":"Invalid hyperlinkIndex."}` |
| **401 Unauthorized**         | Отсутствует или недействителен токен аутентификации.  | `{"Code":401,"Message":"Invalid access token."}`  |
| **404 Not Found**            | Файл, лист или индекс гиперссылки не найдены.         | `{"Code":404,"Message":"Resource not found."}`    |
| **500 Internal Server Error**| Непредвиденная ошибка сервера.                        | `{"Code":500,"Message":"Internal server error."}` |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на проекте. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK. Для надёжности встроены фрагменты кода; ссылка на исходный Gist сохраняется для справки.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Источник: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Источник: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Источник: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
// Example_DeleteWorksheetHyperlink.rb
// Источник: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Источник: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlink deleted"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
// Example_DeleteWorksheetHyperlink.py
// Источник: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
// Example_DeleteWorksheetHyperlink.pl
// Источник: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Источник: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}