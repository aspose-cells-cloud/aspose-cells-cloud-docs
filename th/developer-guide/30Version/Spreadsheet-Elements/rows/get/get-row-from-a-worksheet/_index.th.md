---
title: "รับคำอธิบายแถวจากแผ่นงาน Excel"
second_title: "Document"
linktitle: "แถว"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel row API, Get Worksheet Row, REST API, .NET SDK, Java SDK, Python SDK"
description: "ดึงข้อมูลโดยละเอียด (ความสูง รูปแบบ สถานะการซ่อน เป็นต้น) สำหรับแถวที่ระบุในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมตัวอย่าง curl ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 10
ArticleTitle: "รับคำอธิบายแถวจากแผ่นงาน Excel – Aspose.Cells Cloud API"
---

**ข้อกำหนดเบื้องต้น:**  
- รับโทเค็น JWT ที่ใช้งานได้และใส่ไว้ในส่วนหัว `Authorization: Bearer <jwt token>`  
- ตรวจสอบให้แน่ใจว่าสมุดงานถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud หรือระบุเส้นทางโฟลเดอร์ที่อยู่ของสมุดงาน  
- ใช้เวอร์ชัน API **v3.0** ดังที่แสดงใน URL ของปลายทาง

API REST นี้ดึงข้อมูลแถวโดยใช้ดัชนีของแถวในแผ่นงาน Excel

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบใช้โทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                              |
| -------------- | ------- | -------- | ----------------------------------------------------- |
| name           | string  | path     | ชื่อไฟล์สมุดงาน                                       |
| sheetName      | string  | path     | ชื่อของแผ่นงานภายในสมุดงาน                           |
| rowIndex       | integer | path     | ดัชนีแบบเริ่มต้นที่ 0 ของแถวที่ต้องการดึงข้อมูล        |
| folder         | string  | query    | โฟลเดอร์ที่เก็บสมุดงานไว้                            |
| storageName    | string  | query    | ชื่อของพื้นที่จัดเก็บที่สมุดงานนั้นอยู่               |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST interaction โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL แบบ command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL ใส่ส่วนหัว `Authorization: Bearer <jwt token>` เพื่อพิสูจน์ตัวตนคำขอ

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**โครงสร้างการตอบกลับ**

| คุณสมบัติ          | ประเภท    | คำอธิบาย                                                               |
|-------------------|----------|------------------------------------------------------------------------|
| `GroupLevel`      | integer  | ระดับโครงร่างของแถว (ใช้สำหรับการจัดกลุ่ม)                              |
| `Height`          | number   | ความสูงของแถวเป็นหน่วยพอยต์                                            |
| `Index`           | integer  | ดัชนีแบบเริ่มต้นที่ 0 ของแถวที่ส่งกลับมา                               |
| `IsBlank`         | boolean  | ระบุว่าแถวมีข้อมูลหรือไม่                                              |
| `IsHeightMatched` | boolean  | เป็น `true` หากความสูงของแถวตรงกับความสูงของแถวเริ่มต้น                |
| `IsHidden`        | boolean  | เป็น `true` หากแถวถูกซ่อน                                             |
| `Style`           | object   | วัตถุที่มีข้อมูลรูปแบบสำหรับแถว                                        |
| `link`            | object   | อ้างอิงลิงก์ไปยังทรัพยากรแถว                                           |
| `Code`            | integer  | โค้ดสถานะ HTTP ของการตอบกลับ                                          |
| `Status`          | string   | คำอธิบายแบบข้อความของสถานะ (เช่น “OK”)                               |

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุ / การจัดการข้อผิดพลาด:** API อาจส่งกลับโค้ดสถานะ HTTP ต่อไปนี้:

- **200** – ความสำเร็จ; ส่งกลับข้อมูลแถวแล้ว  
- **401** – ไม่ได้รับอนุญาต; โทเค็น JWT หายไปหรือไม่ถูกต้อง  
- **404** – ไม่พบ; สมุดงาน แผ่นงาน หรือแถวที่ระบุไม่มีอยู่  
- **500** – ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน; เกิดสภาวะที่ไม่คาดคิด  

| โค้ด | คำอธิบาย                                   | วิธีแก้ไข                              |
|------|---------------------------------------------|----------------------------------------|
| 200  | ความสำเร็จ – ข้อมูลแถวถูกส่งกลับมา         | –                                      |
| 401  | ไม่ได้รับอนุญาต – โทเค็น JWT หายไปหรือไม่ถูกต้อง | ระบุโทเค็น JWT ที่ถูกต้อง               |
| 404  | ไม่พบ – สมุดงาน แผ่นงาน หรือแถวหายไป     | ตรวจสอบชื่อและดัชนีแถว                 |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – สภาวะที่ไม่คาดคิด | ติดต่อฝ่ายสนับสนุนของ Aspose          |

สำหรับรายการโค้ดข้อผิดพลาดทั้งหมด โปรดดูเอกสาร [Error Codes](https://docs.aspose.cloud/cells/) ของ Aspose.Cells Cloud

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}