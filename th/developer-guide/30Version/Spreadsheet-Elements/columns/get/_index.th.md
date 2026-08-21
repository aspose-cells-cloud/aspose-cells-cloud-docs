---
title: รับรายละเอียดคอลัมน์ – อ้างอิง API ของ Aspose.Cells Cloud (เวอร์ชัน 4.0)
description: ดึงข้อมูลรายละเอียดเกี่ยวกับคอลัมน์ของเวิร์กชีต (ดัชนี ความกว้าง รูปแบบ และสถานะการซ่อน) โดยใช้ REST API ของ Aspose.Cells Cloud
keywords: Aspose.Cells, Cloud API, คอลัมน์ Excel, รับคอลัมน์, REST API, JWT, เวิร์กชีต
date: 2026-07-30
---

# รับรายละเอียดคอลัมน์  

ดึงข้อมูลรายละเอียดเกี่ยวกับคอลัมน์ของเวิร์กชีตที่ระบุ (ดัชนี ความกว้าง รูปแบบ และสถานะการซ่อน) จากสมุดค่าที่จัดเก็บไว้ใน Aspose Cloud

## สารบัญ
1. [ข้อกำหนดเบื้องต้น](#prerequisites)  
2. [การยืนยันตัวตน](#authentication)  
3. [จุดปลายทาง](#endpoint)  
4. [พารามิเตอร์คำขอ](#request-parameters)  
5. [ตัวอย่าง cURL](#curl-example)  
6. [ตัวอย่างการตอบกลับ](#response-example)  
7. [โครงสร้างการตอบกลับ](#response-schema)  
8. [ข้อผิดพลาดที่เป็นไปได้](#possible-errors)  
9. [ตัวอย่าง SDK](#sdk-examples)  
10. [แหล่งข้อมูลเพิ่มเติม](#additional-resources)  

---

## ข้อกำหนดเบื้องต้น
- **โทเคนการเข้าถึง JWT** ที่ถูกต้อง ซึ่งได้รับจากการยืนยันตัวตนกับ Aspose Cloud  
- ไฟล์สมุดค่าต้องถูกจัดเก็บไว้ใน Aspose Cloud Storage (หรือการจัดเก็บอื่นที่รองรับ) และต้องทราบเส้นทางโฟลเดอร์ (หากมี)  

---

## การยืนยันตัวตน
API ทั้งหมดของ Aspose.Cells Cloud ใช้การยืนยันตัวตนแบบ **โทเคน JWT** ใส่โทเคนในหัวข้อ `Authorization`:

```http
Authorization: Bearer <access_token>
```

สำหรับรายละเอียดเกี่ยวกับวิธีรับโทเคน ดูได้ที่ [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

---

## จุดปลายทาง
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – ชื่อไฟล์สมุดค่า (เช่น `test.xlsx`)  
- **{sheetName}** – ชื่อเวิร์กชีต (เช่น `Sheet1`)  
- **{columnIndex}** – ดัชนีของคอลัมน์ที่ต้องการรับข้อมูล (เริ่มต้นที่ 0)

---

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">โทเคน JWT</a>

## พารามิเตอร์คำขอ

| ชื่อ          | ตำแหน่ง | ประเภท    | จำเป็น | คำอธิบาย |
|---------------|----------|-----------|--------|----------|
| **name**      | path     | string    | ใช่    | ชื่อไฟล์สมุดค่า |
| **sheetName** | path     | string    | ใช่    | เวิร์กชีตที่มีคอลัมน์ที่ต้องการ |
| **columnIndex** | path  | integer   | ใช่    | ดัชนีของคอลัมน์ที่ต้องการรับข้อมูล (เริ่มต้นที่ 0) |
| **folder**    | query    | string    | ไม่บังคับ | โฟลเดอร์ที่สมุดค่าอยู่ในระบบจัดเก็บ |
| **storageName** | query  | string    | ไม่บังคับ | ชื่อของบริการจัดเก็บ (เช่น Aspose Cloud Storage) |

---

## ตัวอย่าง cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## ตัวอย่างการตอบกลับ
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## โครงสร้างการตอบกลับ
| ฟิลด์               | ประเภท  | คำอธิบาย |
|---------------------|---------|----------|
| `Column.GroupLevel` | integer | ระดับโครงสร้างแบบกลุ่ม (outline level) ของคอลัมน์ (ใช้สำหรับการจัดกลุ่ม) |
| `Column.Index`      | integer | ดัชนีของคอลัมน์ (เริ่มต้นที่ 0) |
| `Column.IsHidden`   | boolean | `true` หากคอลัมน์ถูกซ่อนไว้ มิฉะนั้นเป็น `false` |
| `Column.Width`      | number  | ความกว้างของคอลัมน์ในหน่วยตัวอักษร |
| `Column.Style`      | object  | ประกอบด้วย `link` ที่ชี้ไปยังทรัพยากรรูปแบบของคอลัมน์ |
| `Column.link`       | object  | ลิงก์ชี้กลับไปยังทรัพยากรคอลัมน์นี้เอง |
| `Code`              | integer | โค้ดสถานะ HTTP ของการตอบกลับ |
| `Status`            | string  | คำอธิบายข้อความของสถานะ (เช่น **OK**) |

---

## ข้อผิดพลาดที่เป็นไปได้
| สถานะ HTTP | โค้ด | ข้อความ               | เกิดขึ้นเมื่อ |
|------------|------|-----------------------|--------------|
| 400        | 400  | Bad Request           | พารามิเตอร์ที่จำเป็นไม่ครบหรือมีรูปแบบผิด |
| 401        | 401  | Unauthorized          | ไม่มีหรือใช้หัวข้อ `Authorization` ที่ไม่ถูกต้อง |
| 404        | 404  | Not Found             | ไม่พบสมุดค่า เวิร์กชีต หรือคอลัมน์ |
| 500        | 500  | Internal Server Error | ข้อผิดพลาดที่ไม่คาดคิดที่เกิดขึ้นในเซิร์ฟเวอร์ |

### ตัวอย่าง – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### ตัวอย่าง – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## ตัวอย่าง SDK
ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้การดำเนินการ **Get Worksheet Columns** โดยใช้ SDK ทางการของ Aspose.Cells Cloud หาก Gist ไม่สามารถใช้งานได้ โค้ดตัวอย่างจะแสดงไว้ในเนื้อหาด้วย

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// กำหนดค่าไคลเอนต์ API
var apiInstance = new CellsApi("client_id", "client_secret");

// ตั้งค่าพารามิเตอร์ที่จำเป็น
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // ไม่บังคับ
string storageName = "MyStorage";    // ไม่บังคับ

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // ไม่บังคับ
        String storageName = "MyStorage";    // ไม่บังคับ

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # ไม่บังคับ
storage_name = "MyStorage"  # ไม่บังคับ

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // ไม่บังคับ
const storageName = "MyStorage"; // ไม่บังคับ

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **หมายเหตุ:** SDK ทั้งหมดจะจัดการหัวข้อ `Authorization` โดยอัตโนมัติหลังจากที่คุณระบุ `client_id` และ `client_secret`

---

## แหล่งข้อมูลเพิ่มเติม
- **สเปค OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **คู่มือการยืนยันตัวตน:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **ที่เก็บ GitHub (SDK และตัวอย่าง):** <https://github.com/aspose-cells-cloud>  

--- 

*เอกสารอัปเดตล่าสุดเมื่อ 2026-07-30*