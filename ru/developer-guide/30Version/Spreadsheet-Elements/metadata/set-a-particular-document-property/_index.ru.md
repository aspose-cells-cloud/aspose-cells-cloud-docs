---
---
title: "Aspose.Cells Cloud API — обновление (установка) свойства документа"
description: "Установка или создание свойства документа в книге Excel с использованием Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, облачный API, обновление свойства документа, метаданные Excel, REST API, примеры SDK"
api_version: "v3.0"
---

# Обзор
Операция **Обновление (установка) свойства документа** позволяет создать новое свойство документа или изменить существующее в книге Excel, хранящейся в облачном хранилище Aspose.

*Конечная точка*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

В запросе передаётся JSON-полезная нагрузка, описывающая устанавливаемое свойство.

---

## Требования
- Действующий **JWT-токен доступа** (см. раздел **Аутентификация**).  
- Целевая книга (`{name}`) должна уже существовать в облачном хранилище Aspose (или в указанной папке).  
- Имя хранилища (`storageName`) является необязательным; при его отсутствии используется хранилище по умолчанию.

---

## Аутентификация
Aspose.Cells Cloud использует **аутентификацию на основе JWT-токенов**. Токен следует указать в заголовке `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Дополнительные сведения о получении JWT-токена см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-запрос

| Элемент           | Значение |
|-------------------|----------|
| **Метод**         | `PUT` |
| **URI**           | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**  | `application/json` |
| **Accept**        | `application/json` |

### Параметры пути

| Имя               | Тип    | Обязательный | Описание |
|-------------------|--------|--------------|----------|
| `name`            | string | ✅ | Имя файла Excel (включая расширение). |
| `propertyName`    | string | ✅ | Имя свойства документа, которое требуется установить или создать. |

### Параметры запроса

| Имя               | Тип    | Обязательный | Описание |
|-------------------|--------|--------------|----------|
| `folder`          | string | ❌ | Путь к папке в хранилище, где расположена книга. |
| `storageName`     | string | ❌ | Имя сервиса хранилища. При отсутствии используется хранилище по умолчанию. |

### Тело запроса — объект свойства документа

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // необязательно, например, "true" или "false"
  "Link": {                     // необязательно
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Поле       | Тип    | Обязательный | Описание |
|------------|--------|--------------|----------|
| **Name**   | string | ✅ | Имя свойства (например, `author`). |
| **Value**  | string | ✅ | Значение свойства. |
| **BuiltIn**| string | ❌ | Указывает, является ли свойство встроенным. |
| **Link**   | object | ❌ | Информация о гиперссылке (`Href`, `Rel`, `Title`, `Type`). |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://example.com",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### Пример успешного ответа

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**Коды HTTP-статусов**

| Код | Значение                    | Описание |
|-----|-----------------------------|----------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

---

## Примеры SDK
Следующие фрагменты кода демонстрируют вызов операции с использованием официальных SDK Aspose.Cells Cloud.

| Язык | Пример |
|------|--------|
| **C#** | <details><summary>Показать пример на C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Показать пример на Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Показать пример на Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Показать пример на Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Показать пример на Go</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Показать пример на Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>Показать пример на PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Показать пример на Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## См. также
- **Спецификация OpenAPI**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (открывается в новой вкладке, `rel="noopener noreferrer"`).  
- **Руководство по аутентификации**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (открывается в новой вкладке, `rel="noopener noreferrer"`).  
- **SDK Aspose.Cells Cloud**: <https://github.com/aspose-cells-cloud> (открывается в новой вкладке, `rel="noopener noreferrer"`).

---
---