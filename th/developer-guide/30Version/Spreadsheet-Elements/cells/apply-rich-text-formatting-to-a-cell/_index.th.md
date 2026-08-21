---
title: "ใช้รูปแบบข้อความแบบมีคุณภาพสูงกับเซลล์"
type: docs
url: /th/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, rich text, cell formatting, REST API, Aspose.Cells Cloud"
description: "เรียนรู้วิธีใช้ REST API ของ Aspose.Cells Cloud ในการใช้รูปแบบข้อความแบบมีคุณภาพสูงกับเซลล์ Excel ที่ระบุ ประกอบด้วยไวยากรณ์คำขอ รายละเอียดพารามิเตอร์ ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
ArticleTitle: "ใช้ Aspose.Cells Cloud API ในการใช้รูปแบบข้อความแบบมีคุณภาพสูงกับเซลล์"
---

REST API นี้ใช้ **รูปแบบข้อความแบบมีคุณภาพสูง (rich text formatting)** กับเซลล์ในไฟล์ Excel

**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเคน JWT ที่ถูกต้อง และไฟล์ Excel เป้าหมายต้องมีอยู่แล้วในโฟลเดอร์ที่ระบุของพื้นที่จัดเก็บก่อนที่จะเรียกใช้การดำเนินการนี้

**พื้นหลัง:** การใช้รูปแบบข้อความแบบมีคุณภาพสูงช่วยให้คุณสามารถใช้รูปแบบฟอนต์หลายแบบภายในเซลล์เดียว ทำให้สามารถนำเสนอข้อมูลได้อย่างมีชีวิตชีวามากขึ้นในแผ่นงาน Excel

## API PostCellCharacters

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| name           | string | path                         | ชื่อไฟล์ Excel (เช่น `Book1.xlsx`) |
| sheetName      | string | path                         | ชีตที่มีเซลล์เป้าหมาย |
| cellName       | string | path                         | ที่อยู่ของเซลล์ที่ต้องการจัดรูปแบบ (เช่น `A1`) |
| options        | object | body                         | ออบเจกต์ JSON ที่กำหนดการตั้งค่ารูปแบบข้อความแบบมีคุณภาพสูงสำหรับเซลล์ |
| folder         | string | query                        | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ Excel อยู่ |
| storageName    | string | query                        | ชื่อของบริการพื้นที่จัดเก็บ (หากใช้พื้นที่จัดเก็บแบบกำหนดเอง) |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error       | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ API PostCellCharacters กับ SDK

### ข้อมูลจำเพาะ API PostCellCharacters

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*ตัวอย่าง SDK C#*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*ตัวอย่าง SDK Java*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*ตัวอย่าง SDK PHP*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*ตัวอย่าง SDK Ruby*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*ตัวอย่าง SDK Node.js*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*ตัวอย่าง SDK Python*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*ตัวอย่าง SDK Perl*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*ตัวอย่าง SDK Go*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}