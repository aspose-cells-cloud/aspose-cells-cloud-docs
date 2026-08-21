---
title: "Преобразование OLE-объекта в изображение – Aspose.Cells Cloud REST API"
description: "Получите встроенный OLE-объект из листа Excel и преобразуйте его в формат PNG, JPEG, TIFF, GIF, EMF или BMP с помощью Aspose.Cells Cloud REST API."
keywords:
  - "преобразование OLE-объекта в изображение"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "преобразование изображения"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Преобразование OLE-объекта в изображение

Получите встроенный OLE-объект из листа и верните его в запрошенном формате изображения.

---

## Предварительные требования

Перед вызовом этого конечного узла убедитесь, что у вас есть:

1. **Учётная запись Aspose.Cells Cloud** – зарегистрируйтесь на [портале Aspose Cloud](https://dashboard.aspose.cloud/).  
2. **Таблица Excel загружена в облачное хранилище** – используйте API **Upload File** или интерфейс Aspose Cloud.  
3. **JWT-токен доступа** – получите токен, следуя [руководству по аутентификации](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Безопасность и аутентификация

Все API Aspose.Cells Cloud требуют **аутентификации по токену JWT**. Укажите токен в заголовке `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Поддерживаются только HTTPS-конечные узлы; использование `http://` недопустимо.

---

## Запрос

### HTTP-метод
`GET`

### Конечный узел
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Параметры пути

| Имя           | Тип    | Обязательный | Описание                                 |
|---------------|--------|-------------|------------------------------------------|
| `name`        | строка | ✅          | Имя файла таблицы (например, `Book1.xlsx`). |
| `sheetName`   | строка | ✅          | Имя листа, содержащего OLE-объект.       |
| `objectNumber`| целое число | ✅    | Индекс OLE-объекта (начиная с 0).        |

### Параметры запроса

| Имя         | Тип    | Обязательный | Описание |
|-------------|--------|-------------|----------|
| `format`    | строка | ❌          | Требуемый формат изображения (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). По умолчанию — `png`, если параметр не указан. |
| `folder`    | строка | ❌          | Путь к папке, где находится таблица.     |
| `storageName`| строка| ❌          | Имя службы хранилища (например, `MyCloud`). |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Замените `<jwt-token>` на действительный JWT-токен.*

---

## Ответ

| Статус | Content-Type           | Описание |
|--------|------------------------|----------|
| `200`  | `image/png` (или запрошенный формат) | Двоичные данные изображения, представляющие OLE-объект. |
| `400`  | `application/json`     | Некорректные параметры запроса. |
| `401`  | `application/json`     | Ошибка аутентификации (отсутствует/некорректный JWT). |
| `404`  | `application/json`     | Указанная таблица, лист или OLE-объект не найден. |
| `500`  | `application/json`     | Ошибка на стороне сервера. |

### Обработка двоичного содержимого

API возвращает необработанные байты изображения. Вы можете:

* **Сохранить непосредственно в файл** (пример для Linux/macOS):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Закодировать в Base64** для отладки или встраивания в JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Пример (сокращённый) вывод Base64:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Ошибки ответа

| HTTP-статус | Код ошибки             | Сообщение |
|-------------|------------------------|-----------|
| `400`       | `InvalidParameter`     | Один или несколько параметров запроса недопустимы. |
| `401`       | `AuthenticationFailed` | Отсутствует или некорректен JWT-токен. |
| `404`       | `PropertyNotFound`     | Указанная таблица, лист или OLE-объект не существует. |
| `500`       | `InternalError`        | На сервере произошла непредвиденная ошибка. |

---

## Примеры SDK

Следующие фрагменты демонстрируют вызов операции с использованием официальных SDK. Замените `YOUR_JWT_TOKEN` и другие заполнители на реальные значения.

| Язык | Пример |
|------|--------|
| **C#** | <details><summary>Показать код</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png\"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Показать код</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Показать код</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Показать код</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Показать код</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Показать код</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Показать код</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Показать код</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(Полный список SDK доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).)*

---

## Связанные операции

- **Добавление OLE-объекта** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Обновление OLE-объекта** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Удаление OLE-объекта** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Получение списка OLE-объектов** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Дополнительные сведения см. на соответствующих страницах справочника API.

---

## Дополнительные ресурсы

- **Спецификация OpenAPI** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Руководство по аутентификации** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Репозитории SDK** – <https://github.com/aspose-cells-cloud>
- **Производительность и доступность** – запустите аудиты Lighthouse и axe-core, чтобы обеспечить оптимальное время загрузки и соответствие стандарту WCAG 2.1 AA.