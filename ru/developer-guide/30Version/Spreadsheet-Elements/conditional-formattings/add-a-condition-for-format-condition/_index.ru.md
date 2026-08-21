---
---
title: Добавление условия к условному форматированию
description: Узнайте, как добавить условие к условному форматированию рабочего листа с помощью REST API Aspose.Cells Cloud (v3.0). Включает URL-адрес конечной точки, параметры, аутентификацию, пример cURL, фрагменты SDK и обработку ошибок.
keywords: "Aspose.Cells Cloud, условное форматирование, добавление условия, REST API, Excel, рабочий лист"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Добавление условия к условному форматированию

Добавьте условие к существующему правилу условного форматирования на рабочем листе с помощью REST API Aspose.Cells Cloud (v3.0).

---

## Предварительные требования

| Требование | Подробности |
|-------------|-------------|
| **Аутентификация** | Действующий JWT-токен доступа (Bearer), полученный через OAuth 2.0. |
| **Версия API** | v3.0 — URL-адрес конечной точки содержит `/v3.0/`. |
| **Хранилище** | Рабочая книга должна находиться в хранилище, доступном для Aspose.Cells Cloud (по умолчанию — `Default`). |
| **Разрешения** | Разрешения на чтение и запись целевой рабочей книги. |
| **Поддерживаемые форматы** | Любой формат рабочей книги, поддерживаемый Aspose.Cells (например, `.xlsx`, `.xls`, `.xlsm`). |

---

## Конечная точка

**HTTP-метод:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Параметр | Место размещения | Тип | Обязательный | Описание |
|----------|------------------|-----|-------------|----------|
| `name` | Путь | string | **Да** | Имя файла рабочей книги (включая расширение). |
| `sheetName` | Путь | string | **Да** | Имя рабочего листа, содержащего условное форматирование. |
| `index` | Путь | integer | **Да** | Индекс (от 0) коллекции условного форматирования, которую требуется изменить. |
| `type` | Параметр запроса | string | **Да** | Тип условия. Допустимые значения: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Параметр запроса | string | **Да** | Оператор для условия. Допустимые значения: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Параметр запроса | string | **Да** | Первая формула/значение, связанное с условием. |
| `formula2` | Параметр запроса | string | Нет | Вторая формула/значение (обязательна только для операторов, требующих двух значений, например, `Between`). |
| `folder` | Параметр запроса | string | Нет | Папка в хранилище, где находится рабочая книга. |
| `storageName` | Параметр запроса | string | Нет | Имя сервиса хранилища. |

> **Примечание:** Все параметры пути (`name`, `sheetName`, `index`) и параметры запроса `type`, `operatorType`, `formula1` являются обязательными. Параметры `formula2`, `folder` и `storageName` являются необязательными.

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Замените `<jwt_token>` на действующий токен доступа и при необходимости скорректируйте значения `name`, `sheetName`, `index` и параметров запроса.*

---

## Успешный ответ

```json
{
  "Code": "200",
  "Status": "OK"
}
```

Ответ указывает на успешное добавление условия. Операция возвращает обобщенный объект `CellsCloudResponse`, содержащий HTTP-код состояния и краткое сообщение о статусе.

---

## Ответы об ошибках

| HTTP-код | Причина | Пример тела ответа |
|----------|---------|--------------------|
| **400** | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Неавторизованный доступ — отсутствует или некорректен JWT-токен. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Не найдено — рабочая книга, рабочий лист или индекс условного форматирования не существует. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Внутренняя ошибка сервера — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Примечания и типичные ошибки

* **Кодирование параметров** — кодируйте специальные символы в `formula1`/`formula2` (например, пробелы → `%20`).  
* **Совместимость операторов** — некоторые операторы (например, `Between`) требуют наличие и `formula1`, и `formula2`. Пропустите `formula2` для операторов, требующих только одного значения.  
* **Индекс условного форматирования** — индекс отсчитывается от нуля. Если вы не уверены, используйте конечную точку **Get Conditional Formattings** для получения правильного индекса.  
* **Папка хранилища** — если рабочая книга находится не в папке по умолчанию, укажите параметр запроса `folder`; иначе API предположит корневую папку.  
* **Ограничение частоты запросов** — Aspose.Cells Cloud ограничивает количество запросов на аккаунт. При получении ответа 429 подождите и повторите запрос позже.

---

## Примеры SDK

Ниже приведены готовые к запуску фрагменты кода для наиболее популярных SDK. Замените заглушки (`YOUR_FILE`, `YOUR_SHEET` и т. д.) на ваши данные.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // необязательно
        string storageName = null;     // необязательно

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
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
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **Отсутствующие SDK** — Если необходимого вам языка нет в списке, обратитесь к общему **API Reference** и сформируйте HTTP-запрос вручную.

---

## См. также

- **[Получение условного форматирования](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** — получить список правил условного форматирования для рабочего листа.  
- **[Удаление условного форматирования](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** — удалить существующее правило условного форматирования.  
- **[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** — полное машинно-читаемое описание этой операции.  

---
---