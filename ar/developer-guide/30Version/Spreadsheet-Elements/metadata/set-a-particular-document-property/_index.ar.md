---
title: "واجهة برمجة تطبيقات Aspose.Cells السحابية – تحديث (ضبط) خاصية المستند"
description: "ضبط أو إنشاء خاصية مستند في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, واجهة برمجة تطبيقات سحابية, تحديث خاصية المستند, بيانات التعريف الخاصة بملف Excel, واجهة برمجة تطبيقات REST, أمثلة لواجهات برمجة التطبيقات (SDKs)"
api_version: "v3.0"
---

# نظرة عامة
تتيح لك عملية **تحديث (ضبط) خاصية المستند** إنشاء خاصية مستند جديدة أو تعديل خاصية موجودة مسبقًا في ملف Excel مخزن في وحدة تخزين Aspose Cloud.

*نقطة النهاية (Endpoint)*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

يقبل الطلب حمولة JSON تصف الخاصية المراد ضبطها.

---

## المتطلبات الأساسية
- رمز وصول **JWT** صالح (انظر قسم **المصادقة**).  
- يجب أن يكون ملف المصنف المستهدف (`{name}`) موجودًا بالفعل في وحدة تخزين Aspose Cloud (أو في مجلد تحدده).  
- اسم وحدة التخزين (`storageName`) اختياري؛ وفي حال حذفه، سيُستخدم وحدة التخزين الافتراضية.

---

## المصادقة
تستخدم Aspose.Cells Cloud **المصادقة القائمة على رموز JWT**. يجب تضمين الرمز في رأس `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

لمزيد من التفاصيل حول كيفية الحصول على رمز JWT، راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## طلب HTTP

| العنصر          | القيمة |
|------------------|-------|
| **طريقة الطلب**       | `PUT` |
| **عنوان URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **نوع المحتوى (Content-Type)**| `application/json` |
| **النوع المقبول (Accept)**       | `application/json` |

### معلمات المسار (Path Parameters)

| الاسم          | النوع   | الإجبارية | الوصف |
|---------------|--------|----------|-------------|
| `name`        | نص (string) | ✅ | اسم ملف Excel (مع امتداد الملف). |
| `propertyName`| نص (string) | ✅ | اسم خاصية المستند التي سيتم ضبطها أو إنشاؤها. |

### معلمات الاستعلام (Query Parameters)

| الاسم          | النوع   | الإجبارية | الوصف |
|---------------|--------|----------|-------------|
| `folder`      | نص (string) | ❌ | مسار المجلد داخل وحدة التخزين حيث يوجد ملف المصنف. |
| `storageName` | نص (string) | ❌ | اسم خدمة التخزين. وفي حال حذفه، سيُستخدم وحدة التخزين الافتراضية. |

### جسم الطلب – كائن خاصية المستند

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // اختياري، مثلًا: "true" أو "false"
  "Link": {                     // اختياري
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| الحقل   | النوع   | الإجبارية | الوصف |
|---------|--------|----------|-------------|
| **Name**   | نص (string) | ✅ | اسم الخاصية (مثلًا: `author`). |
| **Value**  | نص (string) | ✅ | قيمة الخاصية. |
| **BuiltIn**| نص (string) | ❌ | يشير إلى ما إذا كانت الخاصية مدمجة. |
| **Link**   | كائن (object) | ❌ | معلومات الارتباط التشعبي (`Href`, `Rel`, `Title`, `Type`). |

---

## مثال على الطلب (cURL)

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

### مثال على استجابة ناجحة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق الفلتر بنجاح؛ وتتضمن الاستجابة تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معلمات مفقودة أو غير صالحة (مثلًا: نوع ملف غير مدعوم). |
| 401  | غير مصادق عليه (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |
---

## أمثلة لواجهات برمجة التطبيقات (SDKs)
توضح مقاطع الكود التالية كيفية استدعاء هذه العملية باستخدام واجهات برمجة تطبيقات Aspose.Cells Cloud الرسمية.

| اللغة | المثال |
|----------|--------|
| **C#** | <details><summary>عرض مثال C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>عرض مثال Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>عرض مثال Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>عرض مثال Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>عرض مثال Go</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>عرض مثال Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>عرض مثال PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>عرض مثال Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## روابط ذات صلة
- **مواصفات OpenAPI**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (يفتح في علامة تبويب جديدة، `rel="noopener noreferrer"`).  
- **دليل المصادقة**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (يفتح في علامة تبويب جديدة، `rel="noopener noreferrer"`).  
- **واجهات برمجة تطبيقات Aspose.Cells Cloud (SDKs)**: <https://github.com/aspose-cells-cloud> (يفتح في علامة تبويب جديدة، `rel="noopener noreferrer"`).

---
---