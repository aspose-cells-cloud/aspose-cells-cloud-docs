---
title: "Удаление всех сводных таблиц в листе Excel"
description: "Удаляет все сводные таблицы из указанного листа с использованием REST API Aspose.Cells Cloud."
keywords: "Aspose.Cells, сводная таблица, удаление, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Удаление всех сводных таблиц в листе Excel

## Обзор
Эта операция удаляет **все** сводные таблицы из заданного листа в файле Excel. Это полезно, когда необходимо сбросить анализ на листе или очистить неиспользуемые сводные таблицы в одном вызове.

## Предварительные требования
Перед вызовом API убедитесь, что вы выполнили следующие шаги:

1. **Аккаунт Aspose Cloud** – зарегистрируйтесь в Aspose Cloud, если у вас ещё нет аккаунта.  
2. **JWT-токен** – сгенерируйте JSON Web Token (JWT) для аутентификации. Подробности см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
3. **Настройка хранилища** – загрузите целевой файл Excel в облачное хранилище Aspose Cloud или во внешнее хранилище, подключённое к аккаунту. Обратите внимание на **папку** и **имя хранилища** (если применимо), где расположен файл.

## Аутентификация
API Aspose.Cells Cloud требуют **аутентификации по JWT-токену**. Укажите токен в заголовке `Authorization` каждого запроса:

```
Authorization: Bearer <jwt token>
```

## HTTP-запрос

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Параметры пути
| Имя | Тип | Обязательный | Описание |
|------|--------|----------|-------------|
| `name` | строка | Да | Имя файла Excel (например, `Sample.xlsx`). |
| `sheetName` | строка | Да | Имя листа, из которого будут удалены все сводные таблицы (например, `Sheet1`). |

### Параметры запроса
| Имя | Тип | Обязательный | Описание |
|------|--------|----------|-------------|
| `folder` | строка | Нет | Папка, содержащая файл. |
| `storageName` | строка | Нет | Имя хранилища (если файл находится не в хранилище по умолчанию). |

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Успешный ответ
Сервис возвращает стандартный объект `CellsCloudResponse`, отражающий статус операции.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Обработка ошибок

| HTTP-статус | Значение | Пример полезной нагрузки |
|-------------|---------|-----------------|
| **400** | Неверный запрос — отсутствуют или некорректны параметры | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | Неавторизованный доступ — недействительный или просроченный JWT | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | Не найдено — файл или лист не существует | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | Внутренняя ошибка сервера — непредвиденная ошибка | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Примеры SDK

Следующие фрагменты кода демонстрируют вызов операции с использованием различных SDK Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Инициализация клиента API
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Настройка параметров запроса
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Настройка клиента API
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*Дополнительные SDK (Go, PHP, Ruby, Swift, Perl, Android) доступны в [репозитории SDK Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

## См. также
- [Удаление конкретной сводной таблицы](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Получение всех сводных таблиц в листе](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Обзор аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI-спецификация для DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Документ обновлён 2026-07-30. Весь контент закодирован в UTF-8.*