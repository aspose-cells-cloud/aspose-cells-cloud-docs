---
---
title: "การลบภาพทั้งหมดในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "ล้าง"
type: docs
url: /th/pictures/clear/
aliases: [/delete-all-pictures-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, ลบภาพทั้งหมด, แผ่นงาน, REST API, ล้างภาพ"
description: "เรียนรู้วิธีการลบภาพทั้งหมดออกจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และ SDK"
weight: 60
ArticleTitle: "วิธีลบภาพทั้งหมดในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud"
---

REST API นี้จะลบ **ภาพทั้งหมด** ออกจากแผ่นงาน

**ข้อกำหนดเบื้องต้น**  
- บัญชี Aspose.Cells Cloud ที่ยังไม่หมดอายุ และมีโทเคนการยืนยันตัวตน OAuth 2.0 ที่ถูกต้อง  
- ต้องใช้เวอร์ชัน API 3.0 ขึ้นไป (เวอร์ชันก่อนหน้าถูกเลิกใช้งานแล้ว)  
- ไฟล์ Excel เป้าหมายต้องถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ (ค่าเริ่มต้นหรือแบบกำหนดเอง)

**ความเข้ากันได้ของเวอร์ชัน**  
จุดสิ้นสุดนี้อ้างอิงตามข้อกำหนด API ของ Cells Cloud เวอร์ชัน 3.0 ตรวจสอบให้แน่ใจว่าไลบรารีไคลเอนต์และ URL คำขอของคุณชี้ไปที่ `api.aspose.cloud/v3.0`

## API DeleteWorksheetPictures

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | -------- | -------- | -------------------------------------------- |
| name             | string   | Path     | ชื่อไฟล์ Excel                               |
| sheetName        | string   | Path     | ชื่อแผ่นงานที่มีภาพอยู่                     |
| folder           | string   | Query    | โฟลเดอร์ที่ไฟล์ถูกจัดเก็บ                   |
| storageName      | string   | Query    | ชื่อของบริการที่จัดเก็บข้อมูล                |

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย                                                                            |
| ---------- | ----------------------------------------------------------------------------------- |
| 401        | ไม่ได้รับอนุญาต – ไม่มีโทเคนหรือโทเคนไม่ถูกต้อง                                  |
| 404        | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนีตัดหน้าที่ระบุไม่มีอยู่                             |
| 400        | คำขอไม่ถูกต้อง – ไวยากรณ์คำขอผิดรูปแบบหรือพารามิเตอร์ไม่ถูกต้อง                 |
| 500        | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสถานการณ์ที่ไม่คาดคิดขึ้น                       |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้โดยสาธารณะ และอนุญาตให้คุณดำเนินการ REST ผ่านเว็บเบราว์เซอร์โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียก API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
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

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะเชิงธุรกิจของคุณได้ ดู[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุ:** การดำเนินการ DELETE ไม่รองรับการแบ่งหน้า และอยู่ภายใต้ข้อจำกัดอัตราการใช้งานมาตรฐานของ Aspose.Cells Cloud API (ค่าเริ่มต้นคือ 100 คำขอต่อนาที) ปรับตรรกะไคลเอนต์ของคุณให้สอดคล้องกัน

**ดูเพิ่มเติม**:  
- [/pictures/delete/](../delete/) – ลบภาพหนึ่งภาพที่ระบุออกจากแผ่นงาน  
- [/pictures/add/](../add/) – เพิ่มภาพลงในแผ่นงาน  
---