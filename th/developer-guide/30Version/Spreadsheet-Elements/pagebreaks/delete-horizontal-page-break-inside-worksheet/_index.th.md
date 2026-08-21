---
title: "ลบตัวแบ่งหน้าแนวนอน"
ArticleTitle: "Aspose.Cells Cloud – ลบตัวแบ่งหน้าแนวนอน (REST API)"
second_title: "เอกสาร"
linktitle: "ลบตัวแบ่งหน้าแนวนอน"
type: docs
url: /th/page-breaks/delete-horizontal-page-break/
aliases: [  /th/delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, ลบตัวแบ่งหน้าแนวนอน, สมุดงาน Excel, REST API, SDK"
description: "ลบตัวแบ่งหน้าแนวนอนออกจากสมุดงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud มี SDK ให้ใช้งานสำหรับ C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
weight: 50
---

API นี้จะลบ **ตัวแบ่งหน้าแนวนอน** ออก

**ข้อกำหนดเบื้องต้น**: เพื่อเรียกใช้ปลายทางนี้ คุณต้องมีโทเคน JWT สำหรับการเข้าถึง Aspose Cloud ที่ถูกต้อง สามารถรับโทเคนได้โดยทำตาม [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/cells/authentication/)

## API DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*ทุกคำขอ API จะต้องส่งผ่าน **HTTPS** เท่านั้น*

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                    |
| ---------------- | -------- | -------- | ------------------------------------------------------------ |
| `name`           | string   | path     | ชื่อไฟล์ Excel (สมุดงาน)                                     |
| `sheetName`      | string   | path     | ชื่อของแผ่นงานที่มีตัวแบ่งหน้า                                |
| `index`          | integer  | path     | ดัชนีของตัวแบ่งหน้าแนวนอนที่จะลบ (เริ่มจาก 0)               |
| `folder`         | string   | query    | ไดรฟ์ที่อยู่ของไฟล์ในพื้นที่จัดเก็บ (ไม่บังคับ)               |
| `storageName`    | string   | query    | ชื่อของบริการพื้นที่จัดเก็บ (ไม่บังคับ)                        |

### การตอบกลับข้อผิดพลาด

| HTTP Code | คำอธิบาย                                                            |
| --------- | -------------------------------------------------------------------- |
| 401       | ไม่ได้รับอนุญาต – ไม่มีโทเคนหรือโทเคนไม่ถูกต้อง                   |
| 404       | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนีของตัวแบ่งหน้าที่ระบุไม่มีอยู่จริง   |
| 400       | คำขอไม่ถูกต้อง – รูปแบบคำขอหรือพารามิเตอร์ไม่ถูกต้อง               |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสภาวะที่ไม่คาดคิดขึ้น              |

**ดูเพิ่มเติม:**  
- [เพิ่มตัวแบ่งหน้าแนวนอน](/page-breaks/add-horizontal-page-break/)  
- [รับข้อมูลตัวแบ่งหน้าแนวนอน](/page-breaks/get-horizontal-page-breaks/)  
- [ลบตัวแบ่งหน้าแนวตั้ง](/page-breaks/delete-vertical-page-break/)

[สเปซิฟิเคชัน OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ **cURL** ที่รันผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**โครงสร้างการตอบกลับ**

| ฟิลด์   | ประเภท   | คำอธิบาย                                        |
|---------|----------|--------------------------------------------------|
| Code    | integer  | รหัสสถานะ HTTP (เช่น 200)                        |
| Status  | string   | ข้อความแสดงสถานะในรูปแบบข้อความ (เช่น "OK")     |
| Message | string   | ข้อมูลเพิ่มเติมสำหรับกรณีที่เกิดข้อผิดพลาด (ไม่บังคับ) |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d)*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f)*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152)*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca)*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0)*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1)*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca)*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*หากตัวอย่างไม่สามารถโหลดได้ สามารถดูได้ที่ [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185)*

{{< /tab >}}

{{< /tabs >}}
---