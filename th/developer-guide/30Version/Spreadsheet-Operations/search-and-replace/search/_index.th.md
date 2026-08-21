---
---
title: "ค้นหาข้อความในไฟล์ Excel – Aspose.Cells Cloud API"
description: "ค้นหาข้อความเฉพาะในไฟล์ Excel (XLS, XLSX, XLSM, XLSB) และไฟล์ ODS โดยใช้ Aspose.Cells Cloud API ซึ่งรวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และ SDK รวมถึงการจัดการข้อผิดพลาด"
keywords: "Aspose.Cells, Excel, ค้นหา, API, REST"
type: docs
url: /cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# ค้นหาข้อความในไฟล์ Excel – Aspose.Cells Cloud API

## ภาพรวม
Aspose.Cells Cloud มี **POST** endpoint ที่ใช้ค้นหาสตริงข้อความที่ระบุภายในสมุดงาน Excel (XLS, XLSX, XLSM, XLSB) และไฟล์ OpenDocument Spreadsheet (ODS) โดย API จะส่งค่าเซลล์ทุกเซลล์ที่มีข้อความที่ต้องการค้นหาพร้อมลิงก์ไปยังชีตที่พบข้อความนั้น

> **กรณีการใช้งาน**  
> - ตรวจสอบว่าค่าที่ต้องการมีอยู่ในรายงานก่อนดำเนินการต่อ  
> - สร้างเครื่องมือ “ค้นหาและแทนที่” แบบเร็วโดยแสดงรายการการพบกันทั้งหมดก่อน  
> - สร้างดัชนีของคำสำคัญทั่วชุดของไฟล์สเปรดชีต  

---

## ข้อกำหนดเบื้องต้น
| ข้อกำหนด | รายละเอียด |
|----------|------------|
| **การยืนยันตัวตน** | JWT token ที่ได้รับจากขั้นตอน OAuth ของ Aspose Cloud โดย token ต้องมี scope **Cells** |
| **รูปแบบไฟล์ที่รองรับ** | XLS, XLSX, XLSM, XLSB, ODS |
| **ขนาดไฟล์สูงสุด** | 150 MB (เมื่อบีบอัดแล้ว) ไฟล์ที่มีขนาดใหญ่กว่านี้จะส่งค่า **413 Payload Too Large** |
| **หัวข้อที่จำเป็น** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **สิทธิ์การเข้าถึง** | Token ต้องมีสิทธิ์ *อ่าน* บน storage ที่ใช้งาน (หากใช้ storage ระยะไกล) – ไม่จำเป็นเมื่ออัปโหลดไฟล์เป็น `multipart/form-data` |

*คำแนะนำ:* ใช้ endpoint **/connect/token** เพื่อสร้าง JWT token ดูรายละเอียดได้ที่[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

---

## Endpoint

| รายการ | ค่า |
|--------|-----|
| **HTTP Method** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **วัตถุประสงค์** | ค้นหาข้อความที่ระบุภายในสมุดงาน Excel ที่อัปโหลด |
| **ความปลอดภัย** | JWT token (Bearer) – ดูรายละเอียดใน *ข้อกำหนดเบื้องต้น* ด้านบน |

---

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>

## พารามิเตอร์ของคำขอ

| ชื่อ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย |
|------|-----------|---------|--------|-----------|
| `file` | **file** | `formData` (multipart) | **ใช่** | ไฟล์สเปรดชีตที่จะอัปโหลด |
| `text` | **string** | Query string | **ใช่** | ข้อความที่ต้องการค้นหา |
| `password` | **string** | Query string | ไม่บังคับ | รหัสผ่านสำหรับเปิดสมุดงานที่มีการป้องกัน (ถ้ามี) |
| `sheetname` | **string** | Query string | ไม่บังคับ | ชื่อชีตที่จะจำกัดการค้นหา หากไม่ระบุ จะค้นหาในทุกชีต |
| `checkExcelRestriction` | **boolean** | Query string | ไม่บังคับ (ค่าเริ่มต้น: `true`) | เมื่อตั้งค่าเป็น `true` API จะตรวจสอบข้อจำกัดเฉพาะของ Excel (เช่น เซลล์แบบ read-only) ก่อนการค้นหา |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*แทนที่ `<jwt-token>` ด้วย token ที่ถูกต้องและปรับแต่งพารามิเตอร์ query ตามความเหมาะสม*

---

## การตอบกลับที่สำเร็จ

**HTTP 200 – ค้นหาสำเร็จ; การตอบกลับมีรายการข้อความที่พบ**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### ฟิลด์ในการตอบกลับ

| ฟิลด์ | ชนิดข้อมูล | คำอธิบาย |
|-------|------------|-----------|
| `Status` | string | สถานะคำขอโดยรวม (`OK` สำหรับความสำเร็จ) |
| `Code` | integer | HTTP status code (200) |
| `TextItems.link` | object | ลิงก์Hypermedia ไปยังทรัพยากร collection |
| `TextItems.TextItemList` | array | รายการผลลัพธ์ที่ตรงกัน แต่ละรายการประกอบด้วย: |
| `Text` | string | ค่าในเซลล์ที่ตรงกับข้อความที่ค้นหา |
| `link` | object | ลิงก์ไปยังชีตที่พบข้อความ (`Href` ชี้ไปที่ `Workbook/worksheets/SheetName`) |

---

## การตอบกลับข้อผิดพลาด

| HTTP Code | ความหมาย | สาเหตุทั่วไป | ตัวอย่างเนื้อหา |
|-----------|----------|---------------|----------------|
| **400** | Bad Request | พารามิเตอร์ที่จำเป็นขาดหาย รูปแบบไฟล์ไม่รองรับ หรือค่า query ไม่ถูกต้อง | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | Unauthorized | JWT token ขาดหายหรือไม่ถูกต้อง | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | Payload Too Large | ขนาดไฟล์ที่อัปโหลดเกินขีดจำกัด 150 MB | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | Internal Server Error | ปัญหาที่เกิดขึ้นภายในเซิร์ฟเวอร์โดยไม่คาดคิด | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## ตัวอย่าง SDK

ด้านล่างนี้คือตัวอย่างโค้ดขั้นพื้นฐานสำหรับการดำเนินการ **PostSearch** โดยใช้ SDK อย่างเป็นทางการของ Aspose.Cells Cloud SDK แทนที่ `YOUR_JWT_TOKEN` และเส้นทางไฟล์ด้วยค่าของคุณเอง

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(มี SDK สำหรับ PHP, Ruby, Go และ Perl อยู่ใน [GitHub repository ของ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud))*

---

## หมายเหตุเพิ่มเติม

- **`checkExcelRestriction`** มีค่าเริ่มต้นเป็น `true` เปลี่ยนเป็น `false` ก็ต่อเมื่อคุณแน่ใจว่าสมุดงานไม่มีเซลล์ที่ป้องกันซึ่งอาจรบกวนการค้นหา
- API จะส่งค่า **hypermedia links** (`Href`) ที่สามารถนำไปใช้กับ endpoint อื่นๆ ของ Aspose.Cells (เช่น เพื่อดาวน์โหลดชีตหรือดึงข้อมูลรูปแบบเซลล์)
- เมื่อค้นหาในสมุดงานขนาดใหญ่ ควรจำกัดขอบเขตด้วยพารามิเตอร์ `sheetname` เพื่อเพิ่มความเร็วในการตอบกลับ

---

## ลิงก์ที่เกี่ยวข้อง

- **คู่มือการยืนยันตัวตน** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **สเปค OpenAPI สำหรับ PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>
- **ขีดจำกัดอัตราและโควต้า** – <https://docs.aspose.cloud/total/getting-started/limits/>

---
---