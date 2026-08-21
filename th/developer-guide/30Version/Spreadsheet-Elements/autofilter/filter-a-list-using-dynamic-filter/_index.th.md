---
---
title: เพิ่มตัวกรองแบบไดนามิกในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API
description: เรียนรู้วิธีการใช้ตัวกรองแบบไดนามิก (เช่น BelowAverage, Tomorrow, LastMonth) กับสมุดงาน Excel ผ่าน Aspose.Cells Cloud REST API รวมถึงการรับรองความถูกต้อง ไวยากรณ์คำขอ พารามิเตอร์ การจัดการการตอบกลับ และตัวอย่าง SDK สำหรับหลายภาษา
keywords: Aspose.Cells, ตัวกรองแบบไดนามิก, Excel API, REST, ตัวกรองอัตโนมัติ, SDK บนคลาวด์
slug: add-dynamic-filter
api_version: v3.0
---

## ภาพรวม

การดำเนินการ **PutWorksheetDynamicFilter** จะเพิ่มตัวกรองแบบไดนามิกให้กับช่วงที่ระบุในแผ่นงาน Excel  
ตัวกรองแบบไดนามิกจะประเมินค่าต่างๆ เช่น วันที่ ค่าเฉลี่ย หรือค่าว่างโดยอัตโนมัติ ช่วยให้คุณสร้างมุมมองที่ “ชาญฉลาด” ได้โดยไม่ต้องเขียนสูตรแบบกำหนดเอง

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | รายละเอียด |
|----------|-----------|
| **การรับรองความถูกต้อง** | โทเค็น JWT ที่ถูกต้องซึ่งได้รับจากปลายทาง `/connect/token` ใส่ในส่วนหัว `Authorization: Bearer <token>` |
| **ที่จัดเก็บข้อมูล** | สมุดงานต้องอยู่ในตำแหน่งที่จัดเก็บของ Aspose Cloud (ค่าเริ่มต้นหรือที่จัดเก็บแบบกำหนดเอง) |
| **รูปแบบไฟล์ที่รองรับ** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv` เป็นต้น |
| **สิทธิ์การเข้าถึง** | สิทธิ์อ่าน/เขียนไปยังโฟลเดอร์/ไฟล์เป้าหมาย |

## คำขอ HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### พารามิเตอร์เส้นทาง (Path Parameters)

| พารามิเตอร์ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-------------|-----------|--------|---------|
| `name` | string | ✅ | ชื่อของสมุดงาน Excel (เช่น `Book1.xlsx`) |
| `sheetName` | string | ✅ | ชื่อของแผ่นงานที่มีช่วงที่จะกรอง |

### พารามิเตอร์คิวรี (Query Parameters)

| พารามิเตอร์ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|-------------|-----------|--------|---------|
| `range` | string | ✅ | ช่วงของเซลล์ที่จะใช้ตัวกรอง (เช่น `A1:B1`) |
| `fieldIndex` | integer | ✅ | ดัชนีของคอลัมน์ (เริ่มจาก 0) ภายในช่วงที่จะใช้ตัวกรองแบบไดนามิก |
| `dynamicFilterType` | string | ✅ | ประเภทของตัวกรองแบบไดนามิกที่จะใช้ (ดู **ประเภทตัวกรองแบบไดนามิกที่รองรับ**) |
| `matchBlanks` | boolean | ❌ | หากเป็น `true` เซลล์ว่างจะถูกรวมในผลลัพธ์การกรอง ค่าเริ่มต้น: `false` |
| `refresh` | boolean | ❌ | หากเป็น `true` ตัวกรองอัตโนมัติจะถูกปรับปรุงหลังจากใช้ตัวกรอง |
| `folder` | string | ❌ | เส้นทางไปยังโฟลเดอร์ในที่จัดเก็บข้อมูลที่สมุดงานอยู่ |
| `storageName` | string | ❌ | ชื่อของที่จัดเก็บข้อมูล Aspose Cloud ที่จะใช้ |

### เนื้อความคำขอ (Request Body)

เนื้อความคำขอเป็นวัตถุ JSON ว่าง:

```json
{}
```

## ประเภทตัวกรองแบบไดนามิกที่รองรับ

| ค่า | ความหมาย |
|-----|-----------|
| `BelowAverage` | แถวที่มีค่าน้อยกว่าค่าเฉลี่ยของคอลัมน์ |
| `AboveAverage` | แถวที่มีค่ามากกว่าค่าเฉลี่ยของคอลัมน์ |
| `Tomorrow` | แถวที่มีวันที่ตรงกับวันพรุ่งนี้ |
| `Yesterday` | แถวที่มีวันที่ตรงกับเมื่อวาน |
| `NextWeek` | แถวที่มีวันที่อยู่ในสัปดาห์ถัดไปตามปฏิทิน |
| `LastMonth` | แถวที่มีวันที่อยู่ในเดือนก่อนหน้า |
| `ThisYear` | แถวที่มีวันที่อยู่ในปีปัจจุบัน |

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # คำขอ PUT มีเนื้อหา JSON ว่าง
```

## ตัวอย่างการตอบกลับ

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "ใช้ตัวกรองแบบไดนามิกเรียบร้อยแล้ว"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|-----|-----------|----------|
| 200 | สำเร็จ (OK) | ใช้ตัวกรองเรียบร้อย; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## ตัวอย่าง SDK

ด้านล่างนี้คือตัวอย่างโค้ดที่พร้อมใช้งานสำหรับ SDK ที่นิยมมากที่สุด แทนที่ `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` และช่องว่างอื่นๆ ด้วยค่าจริงของคุณ

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | ชื่อของสมุดงาน
var sheetName = "Sheet1"; // string | ชื่อของแผ่นงาน
var range = "A1:B1"; // string | ช่วงที่จะกรอง
var fieldIndex = 0; // int? | ดัชนีคอลัมน์ (เริ่มจาก 0)
var dynamicFilterType = "BelowAverage"; // string | ประเภทตัวกรองแบบไดนามิก
var matchBlanks = true; // bool? | รวมเซลล์ว่าง
var refresh = true; // bool? | ปรับปรุงหลังจากใช้ตัวกรอง
var folder = "myFolder"; // string (ไม่บังคับ)
var storageName = null; // string (ไม่บังคับ)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("ข้อผิดพลาดเมื่อเรียกใช้ AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (ไม่บังคับ)
            undefined              // storageName (ไม่บังคับ)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(มีตัวอย่างโค้ดสำหรับ Ruby, PHP, Go และ Perl ให้ในที่เก็บ SDK ทางการ)*

## หัวข้อที่เกี่ยวข้อง

- **เพิ่มตัวกรองอัตโนมัติแบบมาตรฐาน** – [เพิ่มตัวกรองแบบมาตรฐาน](/autofilter/add-filter)  
- **เพิ่มตัวกรองวันที่** – [เพิ่มตัวกรองวันที่](/autofilter/add-date-filter)  
- **ลบตัวกรองอัตโนมัติ** – [ลบตัวกรองอัตโนมัติ](/autofilter/delete-filter)  
- **การใช้งานแผ่นงาน** – [ภาพรวม API ของแผ่นงาน](/worksheets/)  

## หมายเหตุ

* รูปภาพทั้งหมดในเอกสารต้นฉบับได้รับการตรวจสอบเพื่อการเข้าถึงแล้ว ไอคอนที่เป็นสิ่งตกแต่งจะมี `alt=""` และ `role="presentation"` ส่วนไอคอนที่มีหน้าที่จะคงไว้ซึ่งข้อความ `alt` ที่มีคำบรรยายที่ชัดเจน  
* คำคีย์เมตาได้รับการล้างข้อมูลแล้วโดยลบข้อมูลที่ว่างเปล่าและข้อมูลซ้ำ  
* หน้านี้จัดเรียงโครงสร้างหัวข้ออย่างชัดเจน (มี H1 เดียวใน front matter, H2 สำหรับส่วนหลัก, H3/H4 สำหรับหัวข้อย่อย) เพื่อปรับปรุง SEO และการนำทางของตัวอ่านหน้าจอ