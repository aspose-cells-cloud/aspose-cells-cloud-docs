---
title: "ป้องกันสมุดงาน Excel ด้วย Aspose.Cells Cloud API"
secondtitle: "เอกสาร"
linktitle: "ป้องกันไฟล์ Excel"
type: docs
url: /th/protect-excel-file/
aliases: [  /th/protect-excel-workbooks/ , /th/workbook/protect/ ]
keywords: "Aspose.Cells, การป้องกัน Excel, API, REST, SDK"
description: "เรียนรู้วิธีการป้องกันสมุดงาน Excel ผ่าน Aspose.Cells Cloud REST API ซึ่งรวมถึงขั้นตอนการตรวจสอบสิทธิ์ พารามิเตอร์ในส่วนของ query และ body, คำขอ cURL และตัวอย่างโค้ด SDK สำหรับ C#, Java, PHP, Ruby, Node.js, Python, Perl และ Go"
weight: 30
ArticleTitle: "ป้องกันสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้ **ป้องกัน** สมุดงาน Excel ทำให้คุณสามารถป้องกันสมุดงาน Excel อย่างปลอดภัยด้วยรหัสผ่านและตัวเลือกการป้องกันโดยใช้ Aspose.Cells Cloud

## API PostProtectDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเคน JWT</a>

### พารามิเตอร์ Query

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                                         |
| ---------------- | ------ | ----------------------------------------------------------------- |
| folder           | string | โฟลเดอร์ที่มีสมุดงานต้นฉบับอยู่ (_ไม่บังคับ_)                    |
| storageName      | string | ชื่อของตำแหน่งพื้นที่จัดเก็บ (_ไม่บังคับ; ค่าเริ่มต้น = "Default")_ |

### พารามิเตอร์ Request Body

| ชื่อพารามิเตอร์ | ประเภท                    | คำอธิบาย                                                      |
| ---------------- | ------------------------- | ------------------------------------------------------------- |
| protection       | WorkbookProtectionRequest | ออบเจกต์ที่กำหนดการตั้งค่าการป้องกันสำหรับสมุดงาน           |

#### WorkbookProtectionRequest

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                                                                                                                              |
| ---------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType   | string | ประเภทของการป้องกันที่จะใช้ ค่าที่อนุญาต (ไม่区分ตัวพิมพ์เล็ก-ใหญ่): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS** |
| Password         | string | รหัสผ่านที่ตั้งเพื่อการป้องกัน (ไม่บังคับ)                                                                                                             |

### การตอบกลับ

```json
{
  "Status": "OK",
  "Code": 200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                                 |
|-----|-------------------------------|--------------------------------------------------------------------------|
| 200 | OK                            | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation        |
| 400 | Bad Request                   | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                 |
| 401 | Unauthorized                  | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413 | Payload Too Large             | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500 | Internal Server Error         | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                |

## วิธีใช้ API PostProtectDocument ด้วย SDK

### สิ่งที่ต้องมีก่อนใช้งาน

ก่อนเรียก API โปรดตรวจสอบให้แน่ใจว่าคุณได้ดำเนินการขั้นตอนต่อไปนี้แล้ว:

- **รับ JWT access token** โดยใช้กระบวนการตรวจสอบสิทธิ์ตามที่อธิบายไว้ในส่วนความปลอดภัย  
- **อัปโหลดสมุดงาน** ไปยังพื้นที่จัดเก็บใน Aspose Cloud ของคุณ หรือยืนยันว่าสมุดงานนั้นมีอยู่แล้วในโฟลเดอร์เป้าหมาย  
- **รู้ชื่อพื้นที่จัดเก็บ** (ค่าเริ่มต้นคือ `"Default"` หากไม่ระบุ) และ **ชื่อไฟล์ที่แน่นอน** ที่คุณต้องการป้องกัน

### ข้อมูลกำกับ API PostProtectDocument

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่าง: ป้องกันสมุดงานด้วย cURL

1. รับ access token ตามที่อธิบายไว้ใน **สิ่งที่ต้องมีก่อนใช้งาน / การตรวจสอบสิทธิ์**  
2. รันคำสั่งคำขอ:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   การตอบกลับจะประกอบด้วยออบเจกต์สถานะยืนยันว่าการป้องกันสำเร็จ

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาแอปพลิเคชันกับ Aspose.Cells Cloud SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ ดู <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### ตัวอย่างการตอบกลับแบบเต็ม

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```