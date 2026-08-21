---
title: "API удаления комментария листа — Aspose.Cells Cloud"
description: "Удаление конкретного комментария ячейки в листе Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает адрес конечной точки, параметры, примеры запросов и ответов, фрагменты кода SDK и обработку ошибок."
keywords: "Aspose.Cells, удаление комментария, Excel API, REST, комментарий листа"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API удаления комментария листа — Aspose.Cells Cloud

> **Страница обновлена:** 30 июля 2026 г.

## Обзор
**Комментарий** — это текстовая заметка, прикреплённая к конкретной ячейке в листе Excel.  
Операция **Удаление комментария листа** удаляет комментарий из указанной ячейки.

![Aspose.Cells Cloud – Иллюстрация удаления комментария листа](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud — API удаления комментария листа")

## Аутентификация
Все конечные точки Aspose.Cells Cloud требуют **аутентификации на основе JWT-токена**.  
Добавьте токен в заголовок `Authorization`:

```
Authorization: Bearer <jwt token>
```

Сведения о получении JWT-токена см. в [Руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Необходимые условия
- Действующий JWT-токен доступа.  
- Целевая рабочая книга (`{name}`) должна существовать в указанном хранилище.  
- Опционально: одно из SDK Aspose.Cells Cloud, установленное для выбранного языка программирования.

## HTTP-запрос

### Конечная точка
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Параметры пути
| Параметр    | Тип    | Обязательный | Описание |
|-------------|--------|--------------|----------|
| `name`      | string | ✅           | Имя рабочей книги Excel (например, `test.xlsx`). |
| `sheetName` | string | ✅           | Имя листа, содержащего комментарий. |
| `cellName`  | string | ✅           | Адрес ячейки, комментарий которой будет удалён (например, `A1`). |

### Параметры запроса
| Параметр      | Тип    | Обязательный | Описание |
|---------------|--------|--------------|----------|
| `folder`      | string | ❌           | Путь к папке, где хранится рабочая книга. Если не указан, используется корневая папка. |
| `storageName` | string | ❌           | Имя сервиса хранилища (например, `MyCloud`). Если не указан, используется хранилище по умолчанию. |

## Пример запроса

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Ответ

### Успех (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание |
|------|-----------------------------|----------|
| 200  | OK (ОК)                    | Фильтр применён успешно; ответ содержит сведения о выполнении операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает допустимый размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

### Ошибочные ответы

| HTTP-код | Описание | Пример |
|----------|----------|--------|
| 400 | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | Неавторизовано — недействительный или отсутствующий токен. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | Не найдено — файл, лист или комментарий не существуют. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | Внутренняя ошибка сервера — непредвиденное состояние на сервере. | `{ "Code": 500, "Message": "Server error." }` |

## Примеры SDK
Ниже приведены готовые к запуску фрагменты кода для наиболее популярных языков. Замените `<jwt token>`, `test.xlsx`, `Sheet1` и `A1` на свои значения.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Настройка клиента API
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## См. также
- [Добавление комментария листа](/comments/add/)  
- [Обновление комментария листа](/comments/update/)  

## Ограничение частоты запросов
Aspose.Cells Cloud устанавливает **ограничение частоты запросов по умолчанию — 100 запросов в минуту на аккаунт**. Превышение лимита возвращает HTTP 429 Too Many Requests. Чтобы избежать ограничений, используйте экспоненциальную задержку или следуйте заголовку `Retry-After`.

## См. также
- **Спецификация OpenAPI:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Руководство по аутентификации:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Репозиторий SDK:** <https://github.com/aspose-cells-cloud>  

---