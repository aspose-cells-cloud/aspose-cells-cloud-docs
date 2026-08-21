---
title: "รับสมุดงานทั้งหมด"
second_title: "เอกสาร"
linktype: "ทั้งหมด"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, Cloud API, รับสมุดงาน, Excel, REST, SDK"
description: "ดึงรายการสมุดงานในไฟล์สมุดงาน Excel ผ่าน Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมตัวอย่าง cURL, โค้ดตัวอย่าง SDK และรูปแบบการตอบกลับ"
weight: 10
---

API นี้ของ REST จะส่งคืนข้อมูลเกี่ยวกับสมุดงานที่อยู่ในไฟล์สมุดงาน

## API ของ REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                |
| ---------------- | -------- | ------- | --------------------------------------- |
| name             | string   | path    | ชื่อของเอกสาร Excel                     |
| folder           | string   | query   | โฟลเดอร์ที่เก็บเอกสารไว้               |
| storageName      | string   | query   | ชื่อของพื้นที่จัดเก็บที่ต้องการใช้งาน  |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการ Aspose.Cells Cloud ตัวอย่างด้านล่างแสดงคำขอ GET เพื่อดึงข้อมูลสมุดงาน

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## การจัดการข้อผิดพลาด

รหัสสถานะ HTTP ทั่วไปที่ถูกส่งคืนโดยปลายทางนี้:

| รหัส | ความหมาย                  | คำอธิบาย                                     |
| ---- | ------------------------- | -------------------------------------------- |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | ขาดพารามิเตอร์ที่จำเป็น (เช่น `name`)        |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหายไป           |
| 404  | ไม่พบ (Not Found)         | ไม่มีสมุดงานที่ระบุไว้                       |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เงื่อนไขเซิร์ฟเวอร์ที่ไม่คาดคิด             |

การตอบกลับข้อผิดพลาดจะถูกส่งคืนในรูปแบบ JSON เช่น:

```json
{
  "Code": "401",
  "Message": "Access token ไม่ถูกต้อง"
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ คุณจึงสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}