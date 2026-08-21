---
title: "Aspose.Cells Cloud API – อัปเดต (ตั้งค่า) คุณสมบัติของเอกสาร"
description: "ตั้งค่าหรือสร้างคุณสมบัติของเอกสารในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API"
keywords: "Aspose.Cells, Cloud API, อัปเดตคุณสมบัติของเอกสาร, เมตาดาต้า Excel, REST API, ตัวอย่าง SDK"
api_version: "v3.0"
---

# ภาพรวม
การดำเนินการ **อัปเดต (ตั้งค่า) คุณสมบัติของเอกสาร** ช่วยให้คุณสามารถสร้างคุณสมบัติของเอกสารใหม่หรือแก้ไขคุณสมบัติที่มีอยู่ในสมุดงาน Excel ที่จัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud

*จุดปลายทาง (Endpoint)*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

คำร้องขอจะรับข้อมูล JSON ที่อธิบายคุณสมบัติที่จะถูกตั้งค่า

---

## ข้อกำหนดเบื้องต้น
- โทเคน JWT ที่ถูกต้อง (ดูหัวข้อ **การยืนยันตัวตน**)  
- สมุดงานเป้าหมาย (`{name}`) ต้องมีอยู่แล้วในพื้นที่จัดเก็บของ Aspose Cloud (หรือโฟลเดอร์ที่คุณระบุ)  
- ชื่อพื้นที่จัดเก็บ (`storageName`) เป็นตัวเลือก; หากไม่ระบุ จะใช้พื้นที่จัดเก็บเริ่มต้น

---

## การยืนยันตัวตน
Aspose.Cells Cloud ใช้ **การยืนยันตัวตนแบบโทเคน JWT** โดยคุณต้องใส่โทเคนในส่วนหัว `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

สำหรับรายละเอียดเกี่ยวกับการรับโทเคน JWT โปรดดูที่ [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

---

## คำร้องขอ HTTP

| ส่วนประกอบ           | ค่า |
|----------------------|-----|
| **เมธอด (Method)**   | `PUT` |
| **URI**              | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**     | `application/json` |
| **Accept**           | `application/json` |

### พารามิเตอร์ในเส้นทาง (Path Parameters)

| ชื่อ          | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|---------------|------------|--------|----------|
| `name`        | สตริง | ✅ | ชื่อไฟล์ Excel (รวมนามสกุลด้วย) |
| `propertyName`| สตริง | ✅ | ชื่อของคุณสมบัติของเอกสารที่ต้องการตั้งค่าหรือสร้างใหม่ |

### พารามิเตอร์ใน query string

| ชื่อ          | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|---------------|------------|--------|----------|
| `folder`      | สตริง | ❌ | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานอยู่ |
| `storageName` | สตริง | ❌ | ชื่อของบริการพื้นที่จัดเก็บ หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น |

### เนื้อหาคำร้องขอ – ออบเจกต์คุณสมบัติของเอกสาร

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // ไม่บังคับ เช่น "true" หรือ "false"
  "Link": {                     // ไม่บังคับ
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| ฟิลด์   | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|---------|------------|--------|----------|
| **Name**   | สตริง | ✅ | ชื่อคุณสมบัติ (เช่น `author`) |
| **Value**  | สตริง | ✅ | ค่าของคุณสมบัติ |
| **BuiltIn**| สตริง | ❌ | ระบุว่าคุณสมบัตินี้เป็นคุณสมบัติปรับแต่งมาหรือไม่ |
| **Link**   | ออบเจกต์ | ❌ | ข้อมูลลิงก์ (Href, Rel, Title, Type) |

---

## ตัวอย่างคำร้องขอ (cURL)

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

### ตัวอย่างการตอบกลับที่สำเร็จ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย |
|------|-------------------------------|----------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | เนื้อหาคำร้องขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |

---

## ตัวอย่าง SDK
โค้ดตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้งานการดำเนินการนี้ผ่าน SDK อย่างเป็นทางการของ Aspose.Cells Cloud

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>แสดงตัวอย่าง C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: \"test.xlsx\",\n    propertyName: \"author\",\n    property: new CellsDocumentProperty {\n        Name = \"author\",\n        Value = \"aspose\",\n        BuiltIn = \"false\",\n        Link = new Link {\n            Href = \"https://example.com\",\n            Rel = \"self\",\n            Title = \"Author link\",\n            Type = \"text/html\"\n        }\n    },\n    folder: \"Docs\",\n    storageName: \"MyStorage\"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>แสดงตัวอย่าง Java</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName(\"author\");\nprop.setValue(\"aspose\");\nprop.setBuiltIn(\"false\");\nLink link = new Link();\nlink.setHref(\"https://example.com\");\nlink.setRel(\"self\");\nlink.setTitle(\"Author link\");\nlink.setType(\"text/html\");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest(\"test.xlsx\", \"author\", prop, \"Docs\", \"MyStorage\");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>แสดงตัวอย่าง Python</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name=\"author\", value=\"aspose\", built_in=\"false\")\nprop.link = Link(href=\"https://example.com\", rel=\"self\", title=\"Author link\", type=\"text/html\")\nresponse = api.put_document_property(name=\"test.xlsx\", property_name=\"author\", property=prop, folder=\"Docs\", storage_name=\"MyStorage\")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>แสดงตัวอย่าง Node.js</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>แสดงตัวอย่าง Go</summary>```go\nimport (\n    \"context\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: \"author\", Value: \"aspose\", BuiltIn: \"false\"}\nprop.Link = &cells.Link{Href: \"https://example.com\", Rel: \"self\", Title: \"Author link\", Type: \"text/html\"}\nreq := cells.PutDocumentPropertyRequest{Name: \"test.xlsx\", PropertyName: \"author\", Property: &prop, Folder: \"Docs\", StorageName: \"MyStorage\"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>แสดงตัวอย่าง Ruby</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>แสดงตัวอย่าง PHP</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>แสดงตัวอย่าง Perl</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## ลิงก์ที่เกี่ยวข้อง
- **OpenAPI Specification**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty> (เปิดในแท็บใหม่, `rel="noopener noreferrer"`)  
- **คู่มือการยืนยันตัวตน**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/> (เปิดในแท็บใหม่, `rel="noopener noreferrer"`)  
- **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud> (เปิดในแท็บใหม่, `rel="noopener noreferrer"`)  

---
---