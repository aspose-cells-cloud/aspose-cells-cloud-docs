---
title: "อัปเดตรูปภาพในไฟล์ Excel"
second_title: "เอกสาร"
linktype: "อัปเดต"
type: docs
url: /th/pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, อัปเดตรูปภาพ, REST API, SDK"
description: "เรียนรู้วิธีการอัปเดตรูปภาพในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรายละเอียดคำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับหลายภาษา"
ArticleTitle: "อัปเดตรูปภาพในไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API"
weight: 70
---

REST API นี้จะอัปเดตรูปภาพที่ระบุด้วยดัชนีในแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเคน JWT ที่ถูกต้องของ Aspose Cloud ไฟล์ Excel เป้าหมายที่จัดเก็บไว้ในที่จัดเก็บข้อมูล Aspose Cloud ของคุณ และใช้เวอร์ชัน API 3.0 หรือใหม่กว่า

## API PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                     |
| ---------------- | -------- | -------- | ------------------------------------------------------------ |
| name             | string   | path     | ชื่อของเอกสาร Excel                                          |
| sheetName        | string   | path     | ชื่อของแผ่นงานที่มีรูปภาพ                                   |
| pictureIndex     | integer  | path     | ดัชนีของรูปภาพที่จะอัปเดต (เริ่มต้นที่ 0)                    |
| picture          | object   | body     | ออบเจกต์ JSON ที่อธิบายคุณสมบัติของรูปภาพที่จะอัปเดต         |
| folder           | string   | query    | โฟลเดอร์ที่เก็บเอกสารไว้                                     |
| storageName      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล                                   |

**หมายเหตุ:** ดัชนีของรูปภาพเริ่มต้นที่ 0 รูปแบบภาพที่รองรับ ได้แก่ JPEG, PNG, BMP และ GIF ขนาดรูปภาพสูงสุดคือ 10 เมกะไบต์

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย                                                         |
| --------- | ---------------------------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต – ไม่มีโทเคนหรือโทเคนไม่ถูกต้อง               |
| 404       | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนีรูปภาพที่ระบุไม่มีอยู่จริง       |
| 400       | คำขอไม่ถูกต้อง – ไวยากรณ์คำขอผิดพลาดหรือพารามิเตอร์ไม่ถูกต้อง |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสภาวะที่ไม่คาดคิดขึ้น         |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

## ครอบครัว SDK ของ Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*ดูเพิ่มเติม:* เพิ่มรูปภาพ, ลบรูปภาพ, รับข้อมูลรูปภาพ, ล้างรูปภาพ – การดำเนินการที่เกี่ยวข้องกับรูปภาพอื่นๆ ใน API ของ Aspose.Cells Cloud