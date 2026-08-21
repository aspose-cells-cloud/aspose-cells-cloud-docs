---
---
title: "Aspose.Cells Cloud API – Belge Özelliğini Güncelleme (Ayarlama)"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabında bir belge özelliği oluşturun veya ayarlayın."
keywords: "Aspose.Cells, Bulut API, Belge Özelliğini Güncelle, Excel meta verisi, REST API, SDK örnekleri"
api_version: "v3.0"
---

# Genel Bakış
**Belge Özelliğini Güncelleme (Ayarlama)** işlemi, Aspose Cloud Depolama’da depolanan bir Excel çalışma kitabında yeni bir belge özelliği oluşturmanıza veya mevcut birini değiştirmenize olanak tanır.

*Uç Nokta*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

İstek, ayarlanacak özelliği açıklayan bir JSON yükü alır.

---

## Ön Koşullar
- Geçerli bir **JWT erişim belirteci** (bkz. **Kimlik Doğrulama** bölümü).  
- Hedef çalışma kitabının (`{name}`) zaten Aspose Cloud Depolama’da (veya belirttiğiniz bir klasörde) bulunuyor olması gerekir.  
- `storageName` (depolama adı) isteğe bağlıdır; atlanırsa varsayılan depolama kullanılır.

---

## Kimlik Doğrulama
Aspose.Cells Cloud, **JWT belirteci tabanlı kimlik doğrulama** kullanır. Belirteci `Authorization` başlığına ekleyin:

```http
Authorization: Bearer <jwt-token>
```

JWT belirteci almayle ilgili ayrıntılar için [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) sayfasını ziyaret edin.

---

## HTTP İsteği

| Öğe              | Değer |
|------------------|-------|
| **Yöntem**       | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### Yol Parametreleri

| Ad            | Tür    | Gerekli | Açıklama |
|---------------|--------|---------|----------|
| `name`        | string | ✅ | Excel dosyasının adı (uzantısı dahil). |
| `propertyName`| string | ✅ | Ayarlanacak veya oluşturulacak belge özelliği adı. |

### Sorgu Parametreleri

| Ad            | Tür    | Gerekli | Açıklama |
|---------------|--------|---------|----------|
| `folder`      | string | ❌ | Çalışma kitabının bulunduğu depolamadaki klasör yolu. |
| `storageName` | string | ❌ | Depolama hizmetinin adı. Atlanırsa varsayılan depolama kullanılır. |

### İstek Gövdesi – Belge Özelliği Nesnesi

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // isteğe bağlı, örneğin "true" veya "false"
  "Link": {                     // isteğe bağlı
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| Alan    | Tür    | Gerekli | Açıklama |
|---------|--------|---------|----------|
| **Name**   | string | ✅ | Özellik adı (örneğin `author`). |
| **Value**  | string | ✅ | Özellik değeri. |
| **BuiltIn**| string | ❌ | Özelliğin yerleşik olup olmadığını belirtir. |
| **Link**   | object | ❌ | Hiperbağlantı bilgisi (`Href`, `Rel`, `Title`, `Type`). |

---

## Örnek İstek (cURL)

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

### Örnek Başarılı Yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |
---

## SDK Örnekleri
Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’larıyla bu işlemi çağırmayı göstermektedir.

| Dil | Örnek |
|-----|-------|
| **C#** | <details><summary>C# örneğini göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Java örneğini göster</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Python örneğini göster</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Node.js örneğini göster</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Go örneğini göster</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Ruby örneğini göster</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>PHP örneğini göster</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Perl örneğini göster</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## İlgili Bağlantılar
- **OpenAPI Spesifikasyonu**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (yeni sekmede açılır, `rel="noopener noreferrer"`).  
- **Kimlik Doğrulama Kılavuzu**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (yeni sekmede açılır, `rel="noopener noreferrer"`).  
- **Aspose.Cells Cloud SDK’ları**: <https://github.com/aspose-cells-cloud> (yeni sekmede açılır, `rel="noopener noreferrer"`).

---
---