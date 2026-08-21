---
title: Удалить вертикальный разрыв страницы – Aspose.Cells Cloud REST API
description: Удалить вертикальный разрыв страницы из рабочего листа Excel с помощью Aspose.Cells Cloud REST API (v3.0). Включает синтаксис запроса, параметры, примеры, коды ответов и фрагменты кода SDK.
keywords: удалить вертикальный разрыв страницы, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# Удалить вертикальный разрыв страницы

Удалить вертикальный разрыв страницы из рабочего листа в книге Excel с помощью Aspose.Cells Cloud REST API.

---

## Необходимые условия

* В заголовке `Authorization` должен быть предоставлен **JWT-токен аутентификации**.  
* Книга (`{name}`) должна находиться в указанной **папке** или **хранилище** и быть доступна клиенту API.

---

## HTTP-запрос

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Параметр | Тип | Местоположение | Обязательный | Описание |
|-----------|--------|----------|----------|-------------|
| **name**      | string | path   | Да | Имя файла Excel. |
| **sheetName** | string | path   | Да | Имя рабочего листа, содержащего разрыв страницы. |
| **index**     | integer| path   | Да | Индекс удаляемого вертикального разрыва страницы (начинается с 0). |
| **folder**    | string | query  | Нет | Путь к папке, в которой хранится файл. |
| **storageName**| string| query  | Нет | Имя службы хранилища. |

---

## Пример запроса

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Успешный ответ

| Код | Описание |
|------|-------------|
| **200** | Вертикальный разрыв страницы успешно удалён. |

**Пример тела ответа**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Ответы об ошибках

| HTTP-код | Описание |
|-----------|-------------|
| **401** | Неавторизовано — отсутствует или недействителен токен. |
| **404** | Не найдено — указанный файл, рабочий лист или индекс разрыва страницы не существует. |
| **400** | Неверный запрос — некорректный синтаксис запроса или недопустимые параметры. |
| **500** | Внутренняя ошибка сервера — возникло непредвиденное условие. |

**Примеры тел ошибок**

*401 – Неавторизовано*

```json
{
  "Code": 401,
  "Message": "Недействительный токен аутентификации."
}
```

*404 – Не найдено*

```json
{
  "Code": 404,
  "Message": "Указанный файл, рабочий лист или индекс разрыва страницы не найден."
}
```

*400 – Неверный запрос*

```json
{
  "Code": 400,
  "Message": "Параметры запроса недопустимы или имеют некорректный формат."
}
```

*500 – Внутренняя ошибка сервера*

```json
{
  "Code": 500,
  "Message": "Произошла непредвиденная ошибка сервера."
}
```

---

## Примеры кода SDK

Следующие примеры демонстрируют вызов операции **DeleteVerticalPageBreak** с использованием различных SDK Aspose.Cells Cloud.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(Фрагменты кода SDK для PHP, Ruby, Perl и других языков следуют той же схеме и доступны в официальном репозитории GitHub.)*

---

## Связанные ресурсы

* **Спецификация OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **SDK Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>  
* **Руководство по аутентификации** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Документ обновлён: 2026‑07‑30*