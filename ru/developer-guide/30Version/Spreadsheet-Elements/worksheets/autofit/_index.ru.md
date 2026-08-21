---
title: "Работа с автоподбором размера в рабочей таблице Excel"
second_title: "Документ"
linktitle: "Автоподбор"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "автоподбор, столбец, строка, Aspose.Cells, облако, Excel, API, изменение размера"
description: "Узнайте, как автоматически изменять размер строк и столбцов в рабочей таблице Excel с помощью REST API Aspose.Cells Cloud. Включает примеры на cURL, .NET, Java и Python."
weight: 20
ArticleTitle: "Работа с автоподбором размера в рабочей таблице Excel – Aspose.Cells Cloud API"
---

## Работа с автоподбором размера в рабочей таблице Excel

- [Как выполнить автоподбор для одного столбца в рабочей таблице Excel.](/cells/worksheets/autofit/column/)
- [Как выполнить автоподбор для нескольких столбцов в рабочей таблице Excel.](/cells/worksheets/autofit/columns/)
- [Как выполнить автоподбор для одной строки в рабочей таблице Excel.](/cells/worksheets/autofit/row/)
- [Как выполнить автоподбор для нескольких строк в рабочей таблице Excel.](/cells/worksheets/autofit/rows/)

**Необходимые условия**  
Перед использованием операций автоподбора необходимо:

1. Иметь учётную запись Aspose.Cells Cloud с корректными значениями **Client Id** и **Client Secret**.  
2. Загрузить рабочую книгу в облачное хранилище Aspose (или получить к ней доступ по общедоступному URL-адресу).  
3. Знать имя рабочего листа, который вы собираетесь изменить.

**Справочник по API**

| Операция | HTTP-метод | Конечная точка | Обязательные параметры | Тело запроса | Пример ответа | Коды состояния |
|----------|-------------|----------------|----------------------|--------------|----------------|----------------|
| Автоподбор **столбца** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (путь) <br> `columnIndex` (запрос) | *отсутствует* | `{ "code": 200, "status": "OK", "message": "Столбец подобран по содержимому." }` | 200, 400, 401, 404, 500 |
| Автоподбор **столбцов** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (путь) <br> `startColumn`, `endColumn` (запрос) | *отсутствует* | `{ "code": 200, "status": "OK", "message": "Столбцы подобраны по содержимому." }` | 200, 400, 401, 404, 500 |
| Автоподбор **строки** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (путь) <br> `rowIndex` (запрос) | *отсутствует* | `{ "code": 200, "status": "OK", "message": "Строка подобрана по содержимому." }` | 200, 400, 401, 404, 500 |
| Автоподбор **строк** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (путь) <br> `startRow`, `endRow` (запрос) | *отсутствует* | `{ "code": 200, "status": "OK", "message": "Строки подобраны по содержимому." }` | 200, 400, 401, 404, 500 |

**Примеры кода**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Аутентификация
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Вызов автоподбора столбцов
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Автоподбор строк
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Автоподбор одного столбца
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Эти фрагменты кода демонстрируют:

1. Аутентификацию в Aspose.Cells Cloud с использованием ваших **Client Id** и **Client Secret**.  
2. Вызов соответствующей конечной точки автоподбора для столбцов или строк.  
3. Обработку ответа, подтверждающего успешное выполнение операции.

**Следующие шаги**

После завершения вызова автоподбора вы можете загрузить обновлённую рабочую книгу:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Не стесняйтесь изменять параметры `startColumn`, `endColumn`, `startRow` и `endRow`, чтобы обработать нужные диапазоны.
---