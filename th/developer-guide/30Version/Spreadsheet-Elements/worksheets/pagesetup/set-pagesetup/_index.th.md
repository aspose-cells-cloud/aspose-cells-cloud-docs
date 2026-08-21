---
title: "ตั้งค่าการตั้งค่าหน้าสำหรับเวิร์กชีต"
second_title: "เอกสาร"
linktype: "ตั้งค่าการตั้งค่าหน้า"
type: docs
url: /set-page-setup/
keywords: "Aspose.Cells, Excel, การตั้งค่าหน้า, REST API, เวิร์กชีต, SDK บนคลาวด์"
description: "เรียนรู้วิธีตั้งค่าการตั้งค่าหน้าสำหรับเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงรายละเอียดคำขอ ตัวอย่าง cURL แบบ HTTPS ที่ปลอดภัย โค้ดสถานะการตอบกลับ และโค้ดตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 20
ArticleTitle: "ตั้งค่าการตั้งค่าหน้าสำหรับเวิร์กชีต – คู่มือ API Aspose.Cells Cloud"
---

เงื่อนไขเบื้องต้น: หากต้องการเรียกใช้ API นี้ คุณต้องมี JWT (OAuth) token ที่ถูกต้อง และสมุดงานต้องอยู่ในตำแหน่งที่จัดเก็บบนคลาวด์ของ Aspose Cloud ซึ่งคุณมีสิทธิ์ในการอ่าน/เขียน ตรวจสอบให้แน่ใจว่ามีการระบุ token ในส่วนหัว **Authorization** และบัญชีของคุณมีโควต้า API ที่จำเป็น

API นี้ตั้งค่าการตั้งค่าหน้าสำหรับเวิร์กชีต Excel

## API บนเว็บ (REST API)

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                 |
| ---------------- | -------- | -------- | ------------------------- |
| name             | string   | path     | ชื่อเอกสาร               |
| sheetName        | string   | path     | ชื่อเวิร์กชีต            |
| pageSetup        | object   | body     | คำอธิบายการตั้งค่าหน้า   |
| folder           | string   | query    | โฟลเดอร์ของเอกสาร        |
| storageName      | string   | query    | ชื่อพื้นที่จัดเก็บข้อมูล |

**ตัวอย่าง JSON payload สำหรับออบเจกต์ `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL บน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API จะส่งกลับออบเจกต์ JSON ที่แสดงผลลัพธ์ของการดำเนินการ:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**โค้ดสถานะการตอบกลับที่เป็นไปได้**

| โค้ด | ความหมาย                   | เวลาที่เกิด                                     |
|-----|----------------------------|-----------------------------------------------|
| 200 | OK                         | อัปเดตการตั้งค่าหน้าสำเร็จ                   |
| 400 | Bad Request                | JSON payload ไม่ถูกต้องหรือขาดฟิลด์ที่จำเป็น |
| 401 | Unauthorized               | ขาด JWT token หรือ token ไม่ถูกต้อง           |
| 404 | Not Found                  | ไม่มีชื่อสมุดงานหรือเวิร์กชีต                |
| 500 | Internal Server Error      | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์      |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}