---
title: "แยกไฟล์ Excel เป็นหลายไฟล์"
second_title: "เอกสาร"
linktype: "แยกไฟล์ Excel หลายไฟล์"
type: docs
url: /split-an-excel-file-to-multi-files/
aliases: [/split-excel-workbooks/,/workbook/split/]
keywords: "Aspose.Cells, คลาวด์, Excel, แยก, API, PDF, CSV, JSON"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อแยกสมุดงาน Excel หลายแผ่นงานเป็นไฟล์แยกต่างหาก โดยรองรับรูปแบบเอาต์พุต เช่น PDF, CSV และ JSON พร้อมให้บริการผ่าน SDK สำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 32
ArticleTitle: "แยกไฟล์ Excel เป็นหลายไฟล์ - เอกสาร Aspose.Cells Cloud"
---

Aspose.Cells Cloud REST API สามารถแยกสมุดงาน Excel หลายแผ่นงานเป็นไฟล์แยกต่างหาก

**ข้อกำหนดเบื้องต้น**  
ก่อนเรียกใช้ API คุณต้องได้รับโทเค็น JWT ที่ถูกต้องและแนบไว้ในส่วนหัว `Authorization` ของการร้องขอแต่ละรายการ โปรดดู [คู่มือการตรวจสอบสิทธิ์](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) เพื่อรายละเอียดเพิ่มเติม

## API PostSplit

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำร้องขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|----------------|--------|-----------|---|
| file           | ไฟล์   | formData  | สมุดงาน Excel ที่จะอัปโหลด |
| format         | สตริง | query     | รูปแบบเอาต์พุตที่ต้องการ (เช่น `pdf`, `csv`, `json`) |
| password       | สตริง | query     | รหัสผ่านสำหรับสมุดงานที่เข้ารหัส (ไม่บังคับ) |
| from           | จำนวนเต็ม | query     | ดัชนีของแผ่นงานแรกที่จะรวม (เริ่มที่ 1) |
| to             | จำนวนเต็ม | query     | ดัชนีของแผ่นงานสุดท้ายที่จะรวม (รวมด้วย) |

### **การตอบกลับ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[ชื่อไฟล์1]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[ชื่อไฟล์2]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[ชื่อไฟล์3]",
            "Filesize" : [ขนาดไฟล์],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย |
|------|-----------------------------|---|
| 200  | OK                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ API PostSplit ด้วย SDK

### ข้อมูลจำเพาะ API PostSplit

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                         | คำอธิบาย |
|------|---------------------------------|
| 200  | OK                              | แยกสมุดงานสำเร็จ และการตอบกลับมีรายชื่อไฟล์ |
| 400  | Bad Request                     | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น รูปแบบที่ไม่รองรับ) |
| 401  | Unauthorized                    | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 500  | Internal Server Error           | เกิดข้อผิดพลาดที่ไม่คาดคิดฝั่งเซิร์ฟเวอร์ |

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API คลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำร้องขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# แทนที่ xxxxx1.xlsx และ xxxxx2.xlsx ด้วยเส้นทางไปยังไฟล์ Excel ของคุณ
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและปล่อยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}