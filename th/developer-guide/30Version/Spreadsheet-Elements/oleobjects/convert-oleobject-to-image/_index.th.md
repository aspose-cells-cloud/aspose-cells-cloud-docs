---
title: "การแปลงวัตถุ OLE เป็นรูปภาพ – Aspose.Cells Cloud REST API"
description: "ดึงข้อมูลวัตถุ OLE ที่ฝังอยู่ในแผ่นงาน Excel และแปลงเป็นรูปแบบ PNG, JPEG, TIFF, GIF, EMF หรือ BMP โดยใช้ Aspose.Cells Cloud REST API"
keywords:
  - "แปลงวัตถุ OLE เป็นรูปภาพ"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "การแปลงรูปภาพ"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# แปลงวัตถุ OLE เป็นรูปภาพ

ดึงข้อมูลวัตถุ OLE ที่ฝังอยู่ในแผ่นงานแล้วส่งกลับในรูปแบบภาพที่ร้องขอ

---

## ข้อกำหนดเบื้องต้น

ก่อนเรียกใช้จุด endpoints นี้ โปรดตรวจสอบให้แน่ใจว่าคุณมี:

1. **บัญชี Aspose.Cells Cloud** – สมัครสมาชิกได้ที่ [พอร์ทัล Aspose Cloud](https://dashboard.aspose.cloud/)  
2. **สมุดงานที่อัปโหลดไว้ในที่จัดเก็บบนคลาวด์** – ใช้ API **Upload File** หรืออินเทอร์เฟซผู้ใช้ของ Aspose Cloud  
3. **โทเคน JWT** – รับโทเคนโดยทำตามคู่มือการ [ยืนยันตัวตน](/total/getting-started/rest-api-overview/authenticating-api-requests/)  

---

## ความปลอดภัยและการยืนยันตัวตน

API ทั้งหมดของ Aspose.Cells Cloud ต้องใช้การยืนยันตัวตนแบบใช้โทเคน JWT  
ให้แนบโทเคนในส่วนหัว `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

รองรับเฉพาะ endpoints ที่ใช้ HTTPS เท่านั้น ห้ามใช้ `http://`

---

## คำขอ

### เมธอด HTTP
`GET`

### จุด endpoints
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### พารามิเตอร์เส้นทาง (Path Parameters)

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|------------------|--------|--------|---------|
| `name`           | สตริง | ✅     | ชื่อไฟล์สมุดงาน (เช่น `Book1.xlsx`) |
| `sheetName`      | สตริง | ✅     | ชื่อแผ่นงานที่มีวัตถุ OLE |
| `objectNumber`   | จำนวนเต็ม | ✅  | ดัชนีเริ่มต้นที่ 0 ของวัตถุ OLE |

### พารามิเตอร์คิวรี (Query Parameters)

| ชื่อพารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|------------------|--------|--------|---------|
| `format`         | สตริง | ❌     | รูปแบบภาพที่ต้องการ (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`) หากไม่ระบุจะใช้ค่าเริ่มต้นเป็น `png` |
| `folder`         | สตริง | ❌     | ตำแหน่งโฟลเดอร์ที่เก็บสมุดงานไว้ |
| `storageName`    | สตริง | ❌     | ชื่อของบริการจัดเก็บข้อมูล (เช่น `MyCloud`) |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*แทนที่ `<jwt-token>` ด้วยโทเคน JWT ที่ถูกต้อง*

---

## การตอบกลับ

| สถานะ (Status) | Content-Type              | คำอธิบาย |
|----------------|---------------------------|----------|
| `200`          | `image/png` (หรือรูปแบบที่ร้องขอ) | ข้อมูลไบนารีของภาพที่แสดงวัตถุ OLE |
| `400`          | `application/json`        | พารามิเตอร์คำขอไม่ถูกต้อง |
| `401`          | `application/json`        | การยืนยันตัวตนล้มเหลว (โทเคน JWT หายไปหรือไม่ถูกต้อง) |
| `404`          | `application/json`        | ไม่พบสมุดงาน แผ่นงาน หรือวัตถุ OLE ที่ร้องขอ |
| `500`          | `application/json`        | ข้อผิดพลาดที่เกิดจากฝั่งเซิร์ฟเวอร์ |

### การจัดการข้อมูลไบนารี (Binary Payload)

API จะส่งกลับข้อมูลภาพแบบไบนารีโดยตรง คุณสามารถ:

* **บันทึกเป็นไฟล์โดยตรง** (ตัวอย่าง Linux/macOS):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **เข้ารหัสเป็น Base64** เพื่อการดีบักกิ้งหรือฝังใน JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *ตัวอย่าง (ย่อ) ผลลัพธ์ Base64:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## การตอบกลับข้อผิดพลาด

| สถานะ HTTP | โค้ด (Code)          | ข้อความ |
|------------|----------------------|--------|
| `400`      | `InvalidParameter`   | พารามิเตอร์คำขอหนึ่งหรือหลายตัวไม่ถูกต้อง |
| `401`      | `AuthenticationFailed` | โทเคน JWT หายไปหรือไม่ถูกต้อง |
| `404`      | `PropertyNotFound`   | สมุดงาน แผ่นงาน หรือวัตถุ OLE ที่ร้องขอไม่มีอยู่จริง |
| `500`      | `InternalError`      | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

---

## ตัวอย่าง SDK

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้งานด้วย SDK อย่างเป็นทางการ  
แทนที่ `YOUR_JWT_TOKEN` และค่าว่างอื่นๆ ด้วยค่าจริงของคุณ

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>แสดงโค้ด</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>แสดงโค้ด</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>แสดงโค้ด</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>แสดงโค้ด</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>แสดงโค้ด</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>แสดงโค้ด</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>แสดงโค้ด</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>แสดงโค้ด</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(รายชื่อ SDK ทั้งหมดมีอยู่ใน [repository บน GitHub](https://github.com/aspose-cells-cloud))*

---

## การดำเนินการที่เกี่ยวข้อง

- **เพิ่มวัตถุ OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **อัปเดตวัตถุ OLE** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **ลบวัตถุ OLE** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **ดึงรายการวัตถุ OLE** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

สำหรับรายละเอียดเพิ่มเติม โปรดดูที่หน้าเอกสารอ้างอิง API ที่เกี่ยวข้อง

---

## ทรัพยากรเพิ่มเติม

- **OpenAPI Specification** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **คู่มือการยืนยันตัวตน** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Repository SDK** – <https://github.com/aspose-cells-cloud>
- **ประสิทธิภาพและเข้าถึงได้ (Accessibility)** – รันการตรวจสอบด้วย Lighthouse และ axe-core เพื่อให้มั่นใจว่ามีเวลาโหลดที่เหมาะสมและเป็นไปตามมาตรฐาน WCAG 2.1 AA