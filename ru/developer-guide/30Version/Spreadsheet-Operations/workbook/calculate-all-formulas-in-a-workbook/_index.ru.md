---
title: "Вычислить все формулы в рабочей книге Excel"
second_title: "Документ"
linktitle: "Вычислить"
type: docs
url: /ru/calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, вычисление формул, Excel API, облачный SDK"
description: "Вычислить каждую формулу в рабочей книге Excel через облачное REST API Aspose.Cells. Включает пример cURL, параметры запроса, схему ответа, предварительные требования и фрагменты кода SDK для множества языков."
weight: 140
ArticleTitle: "Вычислить все формулы в рабочей книге Excel"
---

Это REST API вычисляет **все формулы** в рабочей книге Excel.

**Предварительные требования:** Перед вызовом этой конечной точки убедитесь, что у вас есть:
- Действительный токен аутентификации JWT. (См. [Руководство по аутентификации](/authentication/).)  
- Ваш идентификатор клиента и секрет Aspose.Cells Cloud.  
- Целевая рабочая книга загружена в указанное местоположение хранилища. (См. [Настройка хранилища](/storage/).)

## API PostWorkbookCalculateFormula

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

Ниже приведены параметры запроса:

| Имя параметра  | Тип                | Местоположение | Описание                                                                                  |
| --------------- | ------------------ | ------------- | ----------------------------------------------------------------------------------------- |
| **name**        | string             | path          | Имя файла рабочей книги.                                                                   |
| **options**     | CalculationOptions | body          | JSON-объект, определяющий параметры вычислений (например, `CalcStackSize`, `IgnoreError`). |
| **ignoreError** | boolean            | query         | Если `true`, ошибки, возникающие в процессе вычисления, игнорируются.                      |
| **folder**      | string             | query         | Путь к папке, содержащей рабочую книгу.                                                    |
| **storageName** | string             | query         | Имя сервиса хранилища, в котором сохранена рабочая книга.                                  |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) определяет общедоступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells вы можете легко использовать утилиту командной строки cURL. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Подробности ответа

| Поле             | Тип    | Описание                                                             |
| ---------------- | ------ | -------------------------------------------------------------------- |
| **Code**         | int    | HTTP-подобный код состояния (200 означает успешное выполнение).       |
| **Status**       | string | Краткое текстовое описание результата (например, `OK`).              |
| **WorkbookUrl**  | string | Прямая ссылка для загрузки обновлённой рабочей книги.                |
| **ErrorMessage** | string | Подробная информация об ошибке при неудачном запросе; `null` при успехе. |

#### Следующие шаги / Типичные ошибки

- **Обработка ошибок вычисления** — установите `ignoreError=false`, чтобы получить ответ об ошибке при невозможности вычисления формулы.
- **Учёт ограничений скорости** — проверьте заголовок `X-RateLimit-Remaining`; если он достигает `0`, подождите перед повторной попыткой.
- **Рекомендации по HTTP-статусам**:
  - `400` — Неверные параметры запроса.
  - `401` — Аутентификация не удалась (недействительный или просроченный JWT).
  - `404` — Рабочая книга не найдена.
  - `500` — Ошибка на стороне сервера; обратитесь в службу поддержки Aspose, если она сохраняется.

| Код | Значение              | Когда возвращается                                        |
|-----|-----------------------|----------------------------------------------------------|
| 400 | Неверный запрос       | Неверные параметры запроса или некорректный JSON.        |
| 401 | Неавторизован         | Отсутствующий, недействительный или просроченный JWT.   |
| 404 | Не найдено            | Указанная рабочая книга отсутствует в хранилище.         |
| 500 | Внутренняя ошибка сервера | Непредвиденная ошибка на стороне сервера; обратитесь в службу поддержки Aspose. |

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Ниже приведены примеры кода, демонстрирующие вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}