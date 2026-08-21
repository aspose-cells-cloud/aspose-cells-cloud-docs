---
title: "การทำงานกับตัวกรองพิวต์"
second_title: "เอกสาร"
linktitle: "ตัวกรอง"
type: docs
url: /th/pivot-tables/add-filters/
aliases: [  /th/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, พิวต์แท็บล์, ตัวกรอง, REST API, คลาวด์"
description: "เรียนรู้วิธีเพิ่ม ดึงข้อมูล และลบตัวกรองพิวต์แท็บล์โดยใช้ Aspose.Cells Cloud REST API รวมถึงไวยากรณ์คำขอ พารามิเตอร์ที่จำเป็น ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับ C# และ Go"
weight: 50
ArticleTitle: "การทำงานกับตัวกรองพิวต์ – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้จะเพิ่ม **ตัวกรองพิวต์** ให้กับพิวต์แท็บล์ที่ตำแหน่งดัชนีที่ระบุ

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกใช้ปลายทางนี้ คุณต้อง:

- สร้างโทเค็นการเข้าถึง OAuth/JWT ที่ถูกต้อง และใส่ไว้ในเฮดเดอร์ `Authorization`  
- ตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกจัดเก็บไว้ในโฟลเดอร์คลาวด์ที่คุณมีสิทธิ์เข้าถึง (ระบุ `folder` และ `storageName` ตามความจำเป็น)  
- ใช้เวอร์ชัน API ของ Aspose.Cells Cloud 3.0 หรือใหม่กว่า

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์    | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                      |
| ------------------- | ---------- | -------- | ----------------------------------------------------------------------------------------------- |
| **name**            | string     | path     | ชื่อไฟล์ Excel                                                                                 |
| **sheetName**       | string     | path     | ชีตที่มีพิวต์แท็บล์                                                                           |
| **pivotTableIndex** | integer    | path     | ดัชนีแบบเริ่มต้นที่ 0 ของพิวต์แท็บล์ที่จะใช้ตัวกรอง                                             |
| **filter**          | object     | body     | ออบเจกต์ JSON ที่กำหนดการตั้งค่าตัวกรอง ดูตาราง **filter schema** ด้านล่าง                    |
| **needReCalculate** | boolean    | query    | เมื่อเป็น **true** จะบังคับให้สมุดงานคำนวณใหม่หลังจากเพิ่มตัวกรอง ค่าเริ่มต้นคือ **false**     |
| **folder**          | string     | query    | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่ไฟล์ตั้งอยู่                                                |
| **storageName**     | string     | query    | ชื่อของพื้นที่จัดเก็บบนคลาวด์                                                                |

**โครงสร้าง filter**

| คุณสมบัติ                     | ชนิดข้อมูล | คำอธิบาย                                                                                   |
| ---------------------------- | ---------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object     | การตั้งค่าสำหรับ AutoFilter; สามารถละเว้นได้หากไม่ได้ใช้                                   |
| **EvaluationOrder**          | integer    | ลำดับการประมวลผลตัวกรอง                                                                   |
| **FieldIndex**               | integer    | ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์ที่ตัวกรองนำไปใช้                                            |
| **FilterType**               | string     | ประเภทตัวกรอง (เช่น `Value`, `Count`, `Label`)                                              |
| **MeasureFldIndex**          | integer    | ดัชนีของฟิลด์ measure (ถ้ามี)                                                               |
| **MemberPropertyFieldIndex** | integer    | ดัชนีของฟิลด์ member property (ถ้ามี)                                                      |
| **Name**                     | string     | ชื่อตัวกรอง (ระบุหรือไม่ก็ได้)                                                               |
| **Value1**                   | string     | ค่าแรกที่ใช้โดยตัวกรอง (เช่น ค่าต่ำสุดของช่วง)                                               |
| **Value2**                   | string     | ค่าที่สองที่ใช้โดยตัวกรอง (เช่น ค่าสูงสุดของช่วง)                                            |
| **CustomFilters**            | array      | คอลเลกชันของออบเจกต์ตัวกรองแบบกำหนดเอง (แต่ละออบเจกต์มี `FilterOperatorType`, `Value1`, `Value2`) |
| **DynamicFilter**            | object     | การตั้งค่าสำหรับตัวกรองแบบไดนามิก (เช่น Top10, Bottom10)                                    |
| **IconFilter**               | object     | การตั้งค่าสำหรับตัวกรองแบบใช้ไอคอน                                                          |
| **Top10Filter**              | object     | การตั้งค่าสำหรับตัวกรอง Top10/Bottom10                                                      |
| **ColorFilter**              | object     | การตั้งค่าสำหรับตัวกรองแบบใช้สี                                                             |
| **Visibledropdown**          | boolean    | ระบุว่ามีการแสดงเมนูแบบเลื่อนของตัวกรองหรือไม่                                             |

> **หมายเหตุ:** พารามิเตอร์ทั้งหมดที่ระบุไว้ข้างต้นเป็นพารามิเตอร์ที่จำเป็น เว้นแต่จะระบุว่าเป็นทางเลือกไว้ในเอกสารอ้างอิง API

### โค้ดสถานะของคำตอบ

| โค้ด | ความหมาย                                       |
| ---- | ---------------------------------------------- |
| 200  | เพิ่มตัวกรองสำเร็จ                            |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง         |
| 401  | ไม่ได้รับอนุญาต – ขาดหรือโทเค็นไม่ถูกต้อง       |
| 404  | ไม่พบ – สมุดงานหรือพิวต์แท็บล์ไม่มีอยู่          |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                     |

**แนวทางปฏิบัติที่ดี**  
- ควรทำให้ออบเจกต์ตัวกรองมีขนาดเล็กที่สุดเท่าที่จะเป็นไปได้ เนื่องจากคำอธิบายตัวกรองขนาดใหญ่อาจทำให้เวลาในการตอบสนองของคำขอเพิ่มขึ้น  
- การเรียกใช้มีลักษณะเป็น idempotent — การเพิ่มตัวกรองเดียวกันสองครั้งจะไม่สร้างสำเนาซ้ำ  
- ปฏิบัติตามขีดจำกัดอัตราคำขอของ API ที่ 100 คำขอต่อนาทีต่อหนึ่งบัญชี  

*หมายเหตุเพิ่มเติม:*  
- ขนาดสูงสุดของคำอธิบายตัวกรองคือ 1 เมกะไบต์; ข้อมูลที่มีขนาดใหญ่กว่านี้จะถูกปฏิเสธด้วยข้อผิดพลาด 400  
- เมื่อใช้ `needReCalculate=true` การคำนวณใหม่อาจเพิ่มเวลาในการตอบสนองสำหรับสมุดงานที่มีขนาดใหญ่  

คุณสามารถดูนิยาม OpenAPI แบบเต็มได้ที่นี่:  
[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### ตัวอย่างคำขอ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา against Aspose.Cells Cloud SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดู [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // เริ่มต้นไคลเอนต์ API (แทนที่ด้วยข้อมูลประจำตัวของคุณ)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // สร้างออบเจกต์ตัวกรอง
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // เตรียมคำขอ
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // ดำเนินการคำขอ
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับการดำเนินการเพิ่มเติมที่เกี่ยวข้องกับพิวต์แท็บล์ โปรดดูเอกสารประกอบสำหรับ **เพิ่ม**, **ลบ** และ **ล้าง** ตัวกรอง