---
---
title: "การลบคอลัมน์จากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
description: "เรียนรู้วิธีการลบคอลัมน์เดียวหรือหลายคอลัมน์จากแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API รวมถึงข้อมูลเกี่ยวกับการยืนยันตัวตน ไคลต์สูตรคำสั่งพารามิเตอร์ การตอบกลับ การจัดการข้อผิดพลาด และตัวอย่าง SDK"
keywords: ["Aspose.Cells", "ลบคอลัมน์", "Excel API", "REST", "คลาวด์", "แผ่นงาน", "คอลัมน์"]
date: 2026-07-30
api_version: "v3.0"
---

# ลบคอลัมน์จากแผ่นงาน Excel

**จุดปลายทาง (Endpoint)**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

การดำเนินการนี้จะลบคอลัมน์เดียวหรือช่วงของคอลัมน์ออกจากแผ่นงาน โดยสามารถอัปเดตการอ้างอิงของเซลล์ (รวมถึงสูตร) ได้อัตโนมัติหลังการลบ

---

## สารบัญ
1. [ข้อกำหนดเบื้องต้น](#prerequisites)  
2. [การยืนยันตัวตน](#authentication)  
3. [URL คำขอและเมธอด HTTP](#request-url--http-method)  
4. [พารามิเตอร์](#parameters)  
   - [พารามิเตอร์เส้นทาง (Path parameters)](#path-parameters)  
   - [พารามิเตอร์คำสั่ง (Query parameters)](#query-parameters)  
5. [ตัวอย่าง cURL](#curl-example)  
6. [การตอบกลับ](#responses)  
7. [รหัสข้อผิดพลาด](#error-codes)  
8. [ตัวอย่าง SDK](#sdk-samples)  
9. [หมายเหตุเพิ่มเติม](#additional-notes)  

---

## ข้อกำหนดเบื้องต้น
- โทเคน JWT ที่ถูกต้องซึ่งได้รับจากขั้นตอนการยืนยันตัวตนของ Aspose Cloud  
- สมุดงาน (`{name}`) ต้องถูกอัปโหลดไว้ในที่เก็บข้อมูลของ Aspose Cloud หรือสามารถเข้าถึงได้ผ่านพารามิเตอร์คำสั่ง `folder`/`storageName`  

---

## การยืนยันตัวตน
คำขอทั้งหมดไปยัง Aspose.Cells Cloud จำเป็นต้องใช้การยืนยันตัวตนแบบ **Bearer token**

```http
Authorization: Bearer <access_token>
```

ดูรายละเอียดการรับโทเคน JWT ได้ที่ [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

---

## URL คำขอและเมธอด HTTP
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – ชื่อไฟล์สมุดงาน (เช่น `test.xlsx`)  
- **`{sheetName}`** – ชื่อแผ่นงาน (เช่น `Sheet1`)  
- **`{columnIndex}`** – ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่ต้องการลบ  

---

## พารามิเตอร์

| ชื่อพารามิเตอร์ | ตำแหน่ง | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-----------------|----------|-----------|--------|-----------|
| **name**        | path     | string    | ✅ ใช่   | ชื่อไฟล์สมุดงาน |
| **sheetName**   | path     | string    | ✅ ใช่   | ชื่อแผ่นงาน |
| **columnIndex** | path     | integer   | ✅ ใช่   | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่ต้องการลบ |
| **startColumn** | query    | integer   | ❌ ไม่จำเป็น | ดัชนีแบบเริ่มต้นที่ 0 ที่การลบเริ่มต้น ค่าเริ่มต้นคือ `columnIndex` หากไม่ระบุ |
| **totalColumns**| query    | integer   | ❌ ไม่จำเป็น | จำนวนคอลัมน์ที่ต้องการลบ หากไม่ระบุ จะลบเฉพาะคอลัมน์ที่ระบุด้วย `columnIndex` เท่านั้น |
| **updateReference** | query | boolean | ❌ ไม่จำเป็น | เมื่อตั้งค่าเป็น `true` จะอัปเดตการอ้างอิงของเซลล์ (รวมถึงสูตร) ในสมุดงานทั้งหมดหลังการลบ |
| **folder**      | query    | string    | ❌ ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงาน |
| **storageName** | query    | string    | ❌ ไม่จำเป็น | ชื่อของบริการที่เก็บข้อมูลของ Aspose Cloud |

> **หมายเหตุ** – พารามิเตอร์ `columns` ที่แสดงในสเปค API ระดับต่ำถูกแทนที่ด้วยพารามิเตอร์คำสั่ง `startColumn` และ `totalColumns` ที่มีความยืดหยุ่นมากขึ้น ทั้งสองวิธียังคงรองรับเพื่อความเข้ากันได้ย้อนหลัง

---

## ตัวอย่าง cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### คำอธิบาย
- ลบคอลัมน์ **B** (`columnIndex = 1`) จาก `Sheet1` ของ `test.xlsx`  
- `startColumn=1` และ `totalColumns=1` ระบุการลบคอลัมน์เพียงคอลัมน์เดียว  
- `updateReference=true` ทำให้สูตรและการอ้างอิงอื่นๆ ถูกปรับโดยอัตโนมัติ  

---

## การตอบกลับ

| โค้ด HTTP | คำอธิบาย | ตัวอย่าง |
|-----------|----------|---------|
| **200** | สำเร็จ – คอลัมน์ถูกลบแล้ว | `{ "Code": 200, "Status": "OK" }` |
| **400** | คำขอไม่ถูกต้อง – ขาดหรือพารามิเตอร์ไม่ถูกต้อง | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | ไม่ได้รับอนุญาต – โทเคน JWT ขาดหรือไม่ถูกต้อง | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่จริง | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์ | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

เนื้อหาในส่วนตอบกลับใช้รูปแบบโมเดลทั่วไป **`CellsCloudResponse`**

---

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ตัวกรองถูกใช้งานเรียบร้อย; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |
---

## ตัวอย่าง SDK

ด้านล่างนี้คือตัวอย่างโค้ดที่พร้อมใช้งานสำหรับ SDK ที่นิยมมากที่สุด แทนที่ค่าตัวแปรจำเพาะ (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` เป็นต้น) ด้วยข้อมูลของคุณเอง

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>แสดงโค้ด</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>แสดงโค้ด</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>แสดงโค้ด</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>แสดงโค้ด</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>แสดงโค้ด</summary> <br>```go\npackage main\n\nimport (\n    "context"\n    "fmt"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_ACCESS_TOKEN>"\n    cfg.BasePath = "https://api.aspose.cloud"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), "test.xlsx", "Sheet1", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println("Error:", err)\n        return\n    }\n    fmt.Println("Status:", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>แสดงโค้ด</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts "Status: #{resp.status}"\nrescue AsposeCellsCloud::ApiError => e\n  puts "Exception: #{e}"\nend\n```</details> |
| **PHP** | <details><summary>แสดงโค้ด</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo "Status: " . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>แสดงโค้ด</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint "Status: ", $response->{Status}, "\n";\n```</details> |

*SDK ทั้งหมดจะเพิ่ม header `Authorization` ที่จำเป็นโดยอัตโนมัติเมื่อกำหนดค่า `access_token` แล้ว*

---

## หมายเหตุเพิ่มเติม

### ส่วนหัวด้านความปลอดภัย (แนะนำสำหรับการใช้งานจริง)
เมื่อให้บริการหน้าเอกสารนี้ ให้รวมส่วนหัว HTTP ต่อไปนี้เพื่อปรับปรุงความปลอดภัย:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### เคล็ดลับด้านประสิทธิภาพ
- โหลดสคริปต์วิเคราะห์ของบุคคลที่สาม (`gtag.js`, `containerize.js`) ด้วยแอตทริบิวต์ `async` หรือเลื่อนการโหลดจนกว่าหน้าจะโหลดเสร็จแล้ว  
- ย่อ (minify) ชุด JavaScript/CSS ที่ปรับแต่งเอง  
- โหลดไอคอน SVG ขนาดเล็กล่วงหน้าหากมีผลต่อการเรนเดอร์:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### การปรับปรุง SEO (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Learn how to delete one or more columns from an Excel worksheet via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Delete Column", "Excel", "REST API"]
}
```

วางโค้ดดังกล่าวไว้ในบล็อก `<script type="application/ld+json">` ภายในส่วน `<head>` ของ HTML

### การเข้าถึงได้ (Accessibility)
- รูปภาพที่เป็นส่วนตกแต่งทั้งหมดใช้ `alt=""` หรือซ่อนด้วย `aria-hidden="true"`  
- รูปภาพ Open Graph มีแอตทริบิวต์ `alt` ในแท็กเมตาเพื่อความสมบูรณ์  

---

## ดูเพิ่มเติม
- [สเปค OpenAPI สำหรับ DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [ภาพรวมการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDK ของ Aspose.Cells Cloud บน GitHub](https://github.com/aspose-cells-cloud)  

---
---