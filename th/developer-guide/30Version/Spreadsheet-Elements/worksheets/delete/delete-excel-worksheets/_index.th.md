---
title: "การลบแผ่นงาน Excel หลายแผ่น"
second_title: "เอกสาร"
linktitle: "หลายแผ่นงาน"
type: docs
url: /th/worksheets/delete-multiple/
aliases: [  /th/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, ลบแผ่นงานหลายแผ่น, Excel API, REST API, v3.0, ลบแผ่นงาน"
description: "เรียนรู้วิธีการลบแผ่นงานหลายแผ่นจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) ซึ่งประกอบด้วย endpoint ที่ปลอดภัยผ่าน HTTPS, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL ที่ถูกต้อง และตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 20
ArticleTitle: "ลบแผ่นงาน Excel หลายแผ่นโดยใช้ Aspose.Cells Cloud REST API"
---

REST API นี้จะลบแผ่นงานหลายแผ่นออกจากสมุดงาน

## ความปลอดภัยและการตรวจสอบสิทธิ์
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การตรวจสอบสิทธิ์แบบใช้โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | ---------- | -------- | -------------------------------------------------------------------------- |
| name             | string     | path     | ชื่อไฟล์ Excel                                                              |
| matchCondition   | object     | body     | ออบเจกต์ `MatchConditionRequest` ที่ระบุแผ่นงานที่จะถูกลบ                     |
| folder           | string     | query    | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์นั้นตั้งอยู่                                |
| storageName      | string     | query    | ชื่อของบริการพื้นที่จัดเก็บ                                                   |

**คุณสมบัติของ MatchConditionRequest**

| ชื่อ                | ชนิดข้อมูล | คำอธิบาย                                     | หมายเหตุ   |
| ------------------- | ---------- | -------------------------------------------- | ---------- |
| RegexPattern        | string     | นิพจน์ทั่วไปสำหรับจับคู่ชื่อแผ่นงาน               | ไม่บังคับ |
| FullMatchConditions | string[]   | ชื่อแผ่นงานที่ต้องการลบแบบตรงกันทุกประการ         | ไม่บังคับ |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในคอมมานด์ไลน์เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL **จำเป็นต้องมีโทเคน JWT ที่ถูกต้องในส่วนหัว `Authorization`**

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

คำขอก็อาจส่งการตอบกลับข้อผิดพลาดทั่วไปกลับมาด้วย เช่น:

| HTTP Status | ความหมาย                                     | ตัวอย่าง Payload                                        |
| ----------- | -------------------------------------------- | ------------------------------------------------------- |
| 400         | คำขอไม่ถูกต้อง – JSON หรือพารามิเตอร์ไม่ถูกต้อง | `{"Code":400,"Message":"Invalid request payload."}`     |
| 401         | ไม่ได้รับอนุญาต – ขาดหรือโทเคน JWT ไม่ถูกต้อง  | `{"Code":401,"Message":"Authentication failed."}`       |
| 403         | ถูกปฏิเสธการเข้าถึง – สิทธิ์ไม่เพียงพอ          | `{"Code":403,"Message":"Access denied."}`               |
| 404         | ไม่พบ – ไฟล์หรือแผ่นงานไม่มีอยู่จริง           | `{"Code":404,"Message":"Resource not found."}`          |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์                     | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:**  
- [ลบแผ่นงานเดียว](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [คัดลอกแผ่นงาน](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [ย้ายแผ่นงาน](https://docs.aspose.cloud/cells/worksheets/move/)  
---