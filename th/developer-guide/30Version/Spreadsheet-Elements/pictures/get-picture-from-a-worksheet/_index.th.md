---
title: "รับรูปภาพทั้งหมดจากแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "รับทั้งหมด"
type: docs
url: /th/pictures/get-all/
aliases: [/th/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, แผ่นงาน Excel, API รูปภาพ, รับรูปภาพทั้งหมด, REST API, SDK"
description: "ดึงข้อมูลวัตถุรูปภาพทั้งหมดจากแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API"
ArticleTitle: "รับรูปภาพทั้งหมดจากแผ่นงาน Excel - Aspose.Cells Cloud API"
weight: 10
---

REST API นี้จะดึงข้อมูลรูปภาพทั้งหมดจากแผ่นงาน Excel

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกใช้จุดปลายทางนี้ โปรดตรวจสอบให้แน่ใจว่าคุณมี:

- โทเคน JWT สำหรับการเข้าถึง Aspose Cloud ที่ใช้งานได้  
- ไฟล์ Excel ปลายทางถูกอัปโหลดไปยังพื้นที่จัดเก็บที่เลือกแล้ว  
- ชื่อพื้นที่จัดเก็บที่ถูกต้อง (หากใช้พื้นที่จัดเก็บแบบกำหนดเอง)  
- ชื่อแผ่นงานที่มีรูปภาพ

## API GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**หมายเหตุ:** ใช้ HTTPS (TLS 1.2 หรือสูงกว่า) เมื่อเรียกใช้ API และแนบโทเคน JWT ที่ใช้งานได้ในส่วนหัว `Authorization`

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                    |
| ---------------- | ------ | -------- | ------------------------------------------- |
| name             | string | path     | ชื่อของไฟล์ Excel                           |
| sheetName        | string | path     | ชื่อของแผ่นงานที่มีรูปภาพ                  |
| folder           | string | query    | เส้นทางโฟลเดอร์ที่ไฟล์ถูกจัดเก็บอยู่       |
| storageName      | string | query    | ชื่อของบริการพื้นที่จัดเก็บ                 |

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | คำอธิบาย                                                                      |
| --------- | ----------------------------------------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต – โทเคนหายไปหรือไม่ถูกต้อง                                 |
| 404       | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนีการแบ่งหน้าที่ระบุไม่มีอยู่                    |
| 400       | คำขอไม่ถูกต้อง – ไวยากรณ์คำขอผิดรูปแบบหรือพารามิเตอร์ไม่ถูกต้อง            |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสภาวะที่ไม่คาดคิดขึ้น                      |

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**การตอบกลับที่สำเร็จ** – การเรียกที่สำเร็จจะส่งกลับ HTTP 200 พร้อมข้อมูล JSON ที่มีวัตถุ `Pictures` ซึ่งระบุลิงก์ทรัพยากรของแต่ละรูปภาพ

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

คุณสามารถดาวน์โหลด SDK จากตัวจัดการแพ็กเกจของแต่ละภาษาโดยตรง (เช่น NuGet สำหรับ .NET, Maven Central สำหรับ Java, Composer สำหรับ PHP, npm สำหรับ Node.js, PyPI สำหรับ Python, CPAN สำหรับ Perl และ Go modules สำหรับ Go)

*ดูเพิ่มเติม:* เพิ่มรูปภาพ, ลบรูปภาพ, อัปเดตคุณสมบัติของรูปภาพ