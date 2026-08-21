---
title: "อัปเดตวัตถุ OLE ในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "อัปเดต"
type: docs
url: /th/oleobjects/update/
aliases: [  /th/update-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "อัปเดตวัตถุ OLE, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "เรียนรู้วิธีอัปเดตวัตถุ OLE (รูปภาพ แผนภูมิ เป็นต้น) ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงตัวอย่าง cURL, SDK, ขั้นตอนการตรวจสอบสิทธิ์ และการจัดการข้อผิดพลาด"
weight: 30
author: "ทีมเอกสาร Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "อัปเดตวัตถุ OLE ในสมุดงาน Excel – คู่มือ API Aspose.Cells Cloud"
---

REST API นี้ใช้อัปเดต **วัตถุ OLE** ในสมุดงาน Excel

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเคน JWT</a>

## API PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

พารามิเตอร์ของคำขอ มีดังนี้:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่งพารามิเตอร์ | คำอธิบาย                                         |
| ---------------- | --------- | ------------------ | ------------------------------------------------ |
| name             | string    | path               | ชื่อสมุดงาน                                     |
| sheetName        | string    | path               | ชื่อแผ่นงาน                                     |
| oleObjectIndex   | integer   | path               | ดัชนีของวัตถุ OLE ภายในแผ่นงาน                  |
| ole              | object    | body               | การแสดง JSON ของวัตถุ OLE ที่ต้องการอัปเดต       |
| folder           | string    | query              | โฟลเดอร์ที่เก็บสมุดงานไว้                       |
| storageName      | string    | query              | ชื่อของบริการจัดเก็บข้อมูล                       |

### ฟิลด์ในเนื้อหาคำขอ (Request Body)

| ฟิลด์               | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                                      |
| -------------------- | ---------- | ------ | ------------------------------------------------------------- |
| ImageSourceFullName  | string     | ไม่บังคับ | ตำแหน่งไฟล์รูปภาพที่ใช้สำหรับวัตถุ OLE                         |
| IsAutoSize           | boolean    | ไม่บังคับ | กำหนดว่าควรปรับขนาดวัตถุ OLE อัตโนมัติหรือไม่                 |
| SourceFullName       | string     | จำเป็น | ไฟล์ต้นทาง (เช่น รูปภาพหรือแผนภูมิ) ที่ใช้ในวัตถุ OLE          |
| UpperLeftRow         | integer    | จำเป็น | ดัชนีแถว (เริ่มจาก 0) ของมุมซ้ายบน                             |
| UpperLeftColumn      | integer    | จำเป็น | ดัชนีคอลัมน์ (เริ่มจาก 0) ของมุมซ้ายบน                         |
| Left                 | integer    | ไม่บังคับ | ค่าออฟเซตแนวนอน (หน่วยเป็นจุด) จากมุมซ้ายบน                  |
| Top                  | integer    | ไม่บังคับ | ค่าออฟเซตแนวตั้ง (หน่วยเป็นจุด) จากมุมซ้ายบน                  |
| Width                | integer    | จำเป็น | ความกว้างของวัตถุ OLE (หน่วยเป็นจุด)                           |
| Height               | integer    | จำเป็น | ความสูงของวัตถุ OLE (หน่วยเป็นจุด)                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## การตอบกลับข้อผิดพลาด (Error Responses)

| สถานะ HTTP | โค้ด | ข้อความ                                                        |
| ----------- | ---- | -------------------------------------------------------------- |
| 400         | 4000 | คำขอไม่ถูกต้อง – ขาดพารามิเตอร์หรือพารามิเตอร์ไม่ถูกต้อง      |
| 401         | 4010 | ไม่ได้รับอนุญาต – โทเคน JWT ไม่ถูกต้องหรือไม่มี                |
| 404         | 4040 | ไม่พบ – สมุดงาน แผ่นงาน หรือวัตถุ OLE ไม่มีอยู่จริง           |
| 500         | 5000 | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เกิดความล้มเหลวที่ไม่คาดคิดบนฝั่งเซิร์ฟเวอร์ |

API ยังส่งกลับฟิลด์ **Code** แบบกำหนดเองในเนื้อหาการตอบกลับ ซึ่งสอดคล้องกับสถานะ HTTP (เช่น 200 → 2000, 400 → 4000 เป็นต้น)

## เมื่อใดควรใช้ API นี้?

ใช้ปลายทางนี้เมื่อคุณต้องการแก้ไขวัตถุ OLE ที่มีอยู่แล้ว—เช่น รูปภาพ แผนภูมิ หรือเอกสารที่ฝังอยู่—โดยไม่ต้องอัปโหลดสมุดงานทั้งชุดใหม่ ตัวอย่างสถานการณ์ทั่วไป ได้แก่ การอัปเดตแหล่งที่มาของรูปภาพ การปรับขนาดวัตถุใหม่ หรือการเปลี่ยนตำแหน่งของวัตถุหลังจากที่สร้างสมุดงานแล้ว สำหรับการดำเนินการที่เกี่ยวข้อง โปรดดู [เพิ่มวัตถุ OLE](/th/oleobjects/add/) และ [ลบวัตถุ OLE](/th/oleobjects/delete/)

## ครอบครัว SDK ของ Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ทำหน้าที่ซ่อนรายละเอียดระดับต่ำ เพื่อให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ด้านล่างนี้คือตัวอย่างภาษา C# สั้นๆ ที่ใช้ SDK อัปเดตวัตถุ OLE โดย Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}