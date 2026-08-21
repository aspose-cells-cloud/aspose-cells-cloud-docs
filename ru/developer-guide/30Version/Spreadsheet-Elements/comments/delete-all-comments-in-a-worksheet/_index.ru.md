---
title: "Удаление всех комментариев в листе"
description: "Удалите все комментарии из листа в файле Excel с помощью API Aspose.Cells Cloud. Изучите конечную точку DELETE, необходимые параметры, аутентификацию, пример запроса cURL, формат ответа, коды ошибок и примеры SDK."
keywords: "Aspose, Cells, удаление комментариев, лист, API, REST, Excel, облачные технологии"
url: /ru/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Удаление всех комментариев в листе

**Версия API:** `v3.0`  
**Ресурс:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud предоставляет надёжную REST-конечную точку для удаления **всех** комментариев из указанного листа. Данная операция является необратимой: после её выполнения комментарии не подлежат восстановлению.

---

## Предварительные требования

| Требование | Подробности |
|-----------|-----------|
| **Аутентификация** | Требуется действующий JWT-токен в заголовке `Authorization` (`Bearer <jwt token>`). Получите токен через [процесс аутентификации OAuth2](https://docs.aspose.cloud/cells/authentication/). |
| **Хранилище** | Файл должен находиться в хранилище, доступном для Aspose.Cells Cloud (по умолчанию используется стандартное хранилище, если параметр `storageName` опущен). |
| **Права доступа** | Токен должен иметь права на чтение и запись целевого файла. |
| **SDK (опционально)** | SDK доступны для .NET, Java, PHP, Ruby, Node.js, Python, Perl и Go (см. раздел **Примеры SDK**). |

---

## HTTP-запрос

### Конечная точка

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Параметры пути

| Имя       | Тип    | Описание |
|-----------|--------|----------|
| `name`    | string | Имя файла Excel (например, `test.xlsx`). |
| `sheetName` | string | Имя листа (например, `Sheet1`). |

### Параметры запроса

| Имя          | Тип    | Обязательный | Описание |
|--------------|--------|-------------|----------|
| `folder`     | string | нет         | Путь к папке, содержащей файл. |
| `storageName` | string | нет         | Имя хранилища, в котором расположен файл. |

### Заголовки запроса

| Заголовок             | Значение                           |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Замените `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` и `<jwt token>` на ваши фактические значения.*

---

## Ответ

### Успех (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Тело ответа соответствует модели `CellsCloudResponse`.

### Ошибочные ответы

| HTTP-код | Значение                                | Пример тела ответа |
|----------|-----------------------------------------|--------------------|
| **400**  | Неверный запрос – некорректные параметры. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**  | Неавторизованный доступ – отсутствует/некорректный JWT-токен. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | Не найдено – файл или лист не существует. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**  | Внутренняя ошибка сервера.              | `{ "Code": 500, "Message": "Server error." }` |

---

## Примеры SDK

Следующие фрагменты демонстрируют вызов конечной точки с использованием официальных SDK Aspose.Cells Cloud (версия 3.13.0). Замените заглушки (`<fileName>`, `<sheet>`, `<jwt token>` и т.д.) на ваши собственные данные.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Имя файла.
var sheetName = "Sheet1"; // string | Имя листа.
var folder = "Documents"; // string | Путь к папке (опционально)
var storageName = "MyStorage"; // string | Имя хранилища (опционально)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Ошибка при вызове WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Ошибка при вызове WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # optional
storage_name = 'MyStorage'    # optional

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Ошибка при вызове WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Ошибка:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # optional
storage_name = "MyStorage"    # optional

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Ошибка при вызове WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Ошибка при вызове WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Ошибка: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Примечания и ограничения

* Данная операция **удаляет все комментарии** в указанном листе. Используйте её с осторожностью — отмена невозможна.
* Запрос **не принимает тело запроса**; вся необходимая информация передаётся через URL и заголовки.
* Если целевой файл **защищён** или лист находится в режиме **только для чтения**, API вернёт ошибку `400` или `401` в зависимости от причины.
* Конечная точка работает как с файлами, хранящимися в **Aspose Cloud Storage**, так и в **Amazon S3**, **Azure Blob** или **Google Cloud Storage**, если они корректно указаны через `storageName`.

---

## См. также

* **Спецификация OpenAPI** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)  
* **Руководство по аутентификации** – [OAuth2 для Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)  
* **Репозиторий SDK** – <https://github.com/aspose-cells-cloud>  
* **Общие сведения об API для листов** – <https://docs.aspose.cloud/cells/worksheets/>  

---

*Последнее обновление: 2026‑07‑30*  
---