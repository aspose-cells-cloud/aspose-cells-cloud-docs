---
title: ยกเลิกการจัดกลุ่มคอลัมน์ใน Excel – Aspose.Cells Cloud API  
description: ลบการจัดกลุ่มคอลัมน์ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ประกอบด้วย endpoint, พารามิเตอร์, วิธีการยืนยันตัวตน, ตัวอย่าง cURL, รูปแบบการตอบกลับ และตัวอย่าง SDK  
keywords: Aspose.Cells, ยกเลิกการจัดกลุ่ม, คอลัมน์, Excel, API, REST, คลาวด์, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---

# ยกเลิกการจัดกลุ่มคอลัมน์ใน Excel  

Aspose.Cells Cloud มี operation **POST** ที่ใช้ในการยกเลิกการจัดกลุ่มคอลัมน์จากแผ่นงานที่ระบุ หน้านี้อธิบายรูปแบบคำขอ พารามิเตอร์ที่จำเป็น วิธีการยืนยันตัวตน ตัวอย่างคำเรียก API และการใช้งาน SDK  

---

## สิ่งที่จำเป็นก่อนเริ่มใช้งาน  

| สิ่งที่จำเป็น | เหตุผลที่ต้องใช้ |
|------------|-----------------|
| **บัญชี Aspose Cloud** | เพื่อเข้าถึงบริการของ Aspose.Cells Cloud |
| **โทเค็น JWT** | การเรียก API ทุกครั้งต้องได้รับการยืนยันตัวตนด้วย bearer token ดูเพิ่มเติมได้ที่ [คู่มือการยืนยันตัวตน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) |
| **สมุดงานที่จัดเก็บไว้ใน Aspose Cloud Storage** | API ทำงานกับไฟล์ที่อยู่ในพื้นที่จัดเก็บบนคลาวด์ (หรือพื้นที่จัดเก็บภายนอกที่เชื่อมต่อไว้) |
| **ชื่อแผ่นงาน** | แผ่นงานเป้าหมายต้องมีอยู่ในสมุดงาน |

---

## การยืนยันตัวตน  

คำขอทุกคำขอต้องมี header **Authorization** ที่มีโทเค็น JWT ที่ถูกต้อง:

```http
Authorization: Bearer <access_token>
```

โทเค็นนี้ได้มาจากการใช้ OAuth flow ของ Aspose Cloud ซึ่งโทเค็นมีอายุการใช้งานจำกัด ควรรีเฟรชเมื่อจำเป็น

---

## Endpoint  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Path** – ชื่อไฟล์สมุดงาน (เช่น `test.xlsx`)  
* `{sheetName}` – **Path** – ชื่อแผ่นงาน (เช่น `Sheet1`)  

---

## พารามิเตอร์  

### พารามิเตอร์ Path  

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|------------------|-----------|--------|----------|
| `name` | string | ใช้งานได้ | ชื่อไฟล์สมุดงาน |
| `sheetName` | string | ใช้งานได้ | ชื่อแผ่นงาน |

### พารามิเตอร์ Query  

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|------------------|-----------|--------|----------|
| `firstIndex` | integer | ใช้งานได้ | ดัชนีของคอลัมน์แรกที่ต้องการยกเลิกการจัดกลุ่ม (เริ่มต้นที่ 0) |
| `lastIndex` | integer | ใช้งานได้ | ดัชนีของคอลัมน์สุดท้ายที่ต้องการยกเลิกการจัดกลุ่ม (เริ่มต้นที่ 0) |
| `folder` | string | ไม่จำเป็น | เส้นทางของโฟลเดอร์ที่เก็บสมุดงานไว้ |
| `storageName` | string | ไม่จำเป็น | ชื่อของบริการจัดเก็บข้อมูลที่ไฟล์นั้นอยู่ |

---

## ตัวอย่างคำขอ (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*แทนที่ `<access_token>` ด้วย JWT token ที่ถูกต้อง*

---

## การตอบกลับเมื่อสำเร็จ  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

ออบเจกต์การตอบกลับ (`CellsCloudResponse`) จะมีช่วงของคอลัมน์ที่ถูกยกเลิกการจัดกลุ่มเรียบร้อยแล้ว

### การตอบกลับเมื่อเกิดข้อผิดผลาด  

เมื่อคำขอไม่สำเร็จ บริการจะส่ง JSON payload ที่มีฟิลด์ดังนี้:

| ฟิลด์ | ความหมาย |
|-------|---------|
| `Code` | โค้ดข้อผิดพลาดแบบ HTTP (เช่น 400, 401) |
| `Status` | คำอธิบายสั้นเกี่ยวกับข้อผิดพลาด |
| `ErrorMessage` | คำอธิบายรายละเอียดของข้อผิดพลาด |

---

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|-----|----------|----------|
| 200 | OK | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับจะมีรายละเอียดของ operation |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ประเภทที่ไม่รองรับ) |
| 401 | Unauthorized | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | Internal Server Error | ข้อผิดพลาดที่ไม่คาดคิดจากเซิร์ฟเวอร์ |
---

## ตัวอย่างโค้ด SDK  

ด้านล่างนี้คือตัวอย่างโค้ดพร้อมใช้งานสำหรับ SDK ที่นิยมมากที่สุด แทนที่ค่า placeholder (`<YourAccessToken>`, `<YourFileName>` เป็นต้น) ด้วยข้อมูลของคุณเอง

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **หมายเหตุ:** SDK สำหรับ PHP, Ruby, Perl และภาษาอื่น ๆ มีลำดับพารามิเตอร์เดียวกัน สำหรับตัวอย่างแบบสมบูรณ์ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)

---

## อ้างอิง  

* **สเปค OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **คู่มือการยืนยันตัวตน:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **ที่เก็บ SDK:** <https://github.com/aspose-cells-cloud>

---

## ประวัติการแก้ไข  

| วันที่ | ผู้เขียน | การเปลี่ยนแปลง |
|------|--------|--------|
| 2026‑07‑30 | AI Optimizer | แก้ไขการเข้ารหัส UTF‑8, เพิ่มหัวข้อสิ่งที่จำเป็นก่อนเริ่มใช้งาน, ปรับปรุงคำค้นหาเมตา, ปรับปรุงโครงสร้างหัวข้อ และเพิ่มตัวอย่างโค้ด SDK |
| 2026‑07‑29 | ผู้เขียนเดิม | ร่างเอกสารฉบับแรก |  
---