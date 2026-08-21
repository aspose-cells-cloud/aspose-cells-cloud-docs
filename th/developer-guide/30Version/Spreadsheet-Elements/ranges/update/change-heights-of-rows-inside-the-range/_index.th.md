---
---
title: "ตั้งค่าความสูงของแถวสำหรับช่วงใน Excel – Aspose.Cells Cloud API (v3.0)"
description: "เปลี่ยนความสูงของแถวภายในช่วงที่ระบุของสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL, ตัวอย่างการตอบกลับ และโค้ดตัวอย่าง SDK สำหรับหลายภาษา"
keywords: "Aspose.Cells, ความสูงของแถว, ช่วง, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# ตั้งค่าความสูงของแถวสำหรับช่วงใน Excel

การดำเนินการนี้จะอัปเดตความสูงของแถวของช่วงที่ระบุบนชีตที่จัดเก็บไว้ในที่จัดเก็บของ Aspose Cloud

## ข้อกำหนดเบื้องต้น / การตรวจสอบสิทธิ์

คุณต้องได้รับโทเคน JWT เข้าถึงจากบริการ OAuth ของ Aspose Cloud ด้วยขอบเขต **Cells.ReadWrite**

ใส่โทเคนนี้ในส่วนหัว `Authorization` ของทุกคำขอ:

```http
Authorization: Bearer <jwt token>
```

หากคุณยังไม่มีโทเคน ให้ทำตาม **คู่มือการตรวจสอบสิทธิ์ของ Aspose Cloud** เพื่อขอรับโทเคน

## คำขอ HTTP

| เมธอด | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### พารามิเตอร์เส้นทาง (Path Parameters)

| ชื่อ | ประเภท | คำอธิบาย |
|------|--------|-----------|
| `name` | `string` | **จำเป็น** ชื่อของไฟล์ Excel ที่จัดเก็บไว้ในคลาวด์ |
| `sheetName` | `string` | **จำเป็น** ชีตที่มีช่วงเป้าหมาย |

### พารามิเตอร์คิวรี (Query Parameters)

| ชื่อ | ประเภท | จำเป็น | คำอธิบาย |
|------|--------|--------|-----------|
| `value` | `number` | **ใช่** | ความสูงของแถวที่ต้องการ (เป็นหน่วยจุด) ที่จะนำไปใช้กับช่วง |
| `folder` | `string` | ไม่จำเป็น | เส้นทางโฟลเดอร์ในที่จัดเก็บที่ไฟล์นั้นตั้งอยู่ |
| `storageName` | `string` | ไม่จำเป็น | ชื่อของบริการที่จัดเก็บ (หากมีการกำหนดค่าหลายที่จัดเก็บ) |

### เนื้อหาคำขอ (JSON)

เนื้อหาต้องมีวัตถุ **Range** ที่กำหนดว่าแถวใดบ้างที่ได้รับผลกระทบ

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### โครงร่าง JSON ของ Range

| คุณสมบัติ | ประเภท | จำเป็น | คำอธิบาย |
|-----------|--------|--------|-----------|
| `FirstRow` | integer | **ใช่** | ดัชนีของแถวแรกในช่วง (เริ่มต้นที่ 0) |
| `RowCount` | integer | **ใช่** | จำนวนแถวที่จะนำไปใช้ความสูง |
| `FirstColumn` | integer | ไม่จำเป็น | ดัชนีของคอลัมน์แรก (ไม่บังคับสำหรับการตั้งค่าความสูงแถวเท่านั้น) |
| `ColumnCount` | integer | ไม่จำเป็น | จำนวนคอลัมน์ที่ช่วงครอบคลุม (ไม่บังคับ) |

เฉพาะคุณสมบัติที่ระบุไว้ข้างต้นเท่านั้นที่ถูกใช้ในการดำเนินการตั้งค่าความสูงของแถว; ฟิลด์เพิ่มเติมใดๆ จะถูกละเลย

## ตัวอย่างคำขอ

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### ตัวอย่างการตอบกลับ (ความสำเร็จ)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-------------------------------|-----------------------------------------------|
| 200  | OK (สำเร็จ)                  | กรองถูกนำไปใช้เรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request (คำขอไม่ถูกต้อง) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized (ไม่ได้รับอนุญาต) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large (ข้อมูลหนักเกินไป) | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error (ข้อผิดพลาดภายในเซิร์ฟเวอร์) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

การตอบกลับทุกครั้งจะมี `Code` เป็นตัวเลข และ `Status` (หรือ `Message` สำหรับข้อผิดพลาด) ที่อ่านเข้าใจได้ อาจมี `ErrorDetails` เพิ่มเติมเมื่อเกิดข้อผิดพลาด

## ตัวอย่าง SDK

โค้ด snippets ต่อไปนี้แสดงวิธีเรียก **Set Row Height for a Range** โดยใช้ SDK อย่างเป็นทางการของ Aspose.Cells Cloud

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>Show code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Show code</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Show code</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Show code</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Show code</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Show code</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Show code</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Show code</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **หมายเหตุ:** SDK ทั้งหมดจะเพิ่มส่วนหัว `Authorization: Bearer` ที่จำเป็นโดยอัตโนมัติเมื่อกำหนดค่าโทเคนการเข้าถึงแล้ว

## ดูเพิ่มเติม

- **OpenAPI Specification** – ข้อตกลงเชิงรายละเอียดสำหรับการดำเนินการนี้: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK Repository** – โค้ดแหล่งที่มาและ binding ภาษาเพิ่มเติม: <https://github.com/aspose-cells-cloud>
- **Authentication Guide** – วิธีรับโทเคน JWT: <https://docs.aspose.cloud/cells/authentication/>

---
---