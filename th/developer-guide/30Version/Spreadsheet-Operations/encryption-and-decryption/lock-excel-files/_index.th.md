---
title: "ล็อกไฟล์ Excel"
second_title: "เอกสาร"
linktype: "ล็อกไฟล์ Excel"
type: docs
url: /lock-excel-files/
aliases: [/lock/without-storage/, /lock/, /lock/without-using-storage/]
keywords: "ล็อก, Excel, API, Aspose.Cells, Cloud, REST, Workbook, Spreadsheet, SDK"
description: "เรียนรู้วิธีการล็อกสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งประกอบด้วย HTTPS endpoint, การยืนยันตัวตน, คำสั่ง cURL, โครงร่างการตอบกลับ และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ อีกมากมาย"
ArticleTitle: "ล็อกไฟล์ Excel – เอกสารประกอบ API ของ Aspose.Cells Cloud"
weight: 70
---

**เวอร์ชัน API:** v3.0 (เวอร์ชันปัจจุบัน)

API REST นี้ **ล็อก** สมุดงาน Excel

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**ข้อกำหนดเบื้องต้น** – คำขอต้องส่งผ่าน **HTTPS** และต้องมีโทเค็น OAuth 2.0 Bearer ที่ถูกต้องในส่วนหัว `Authorization`

### พารามิเตอร์ของคำขอมีดังนี้

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง                   | คำอธิบาย                                     |
| ---------------- | ---------- | -------------------------- | --------------------------------------------- |
| file             | ไฟล์       | form‑data (multipart body) | สมุดงาน Excel ที่จะอัปโหลดและล็อก           |
| password         | สตริง       | query string               | รหัสผ่านสำหรับสมุดงาน (ไม่บังคับ)            |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธี **เรียก** API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*คุณสามารถดาวน์โหลดสมุดงานตัวอย่าง — [Sample.xlsx](https://example.com/Sample.xlsx) — เพื่อทดสอบคำขอ*

**หมายเหตุ:** API รองรับไฟล์ขนาดไม่เกิน 100 MB; ไฟล์ที่มีขนาดใหญ่กว่านี้อาจได้รับการตอบกลับด้วยสถานะ 413 (Payload Too Large)

### **รายละเอียดการตอบกลับ**

| ฟิลด์       | ชนิดข้อมูล       | คำอธิบาย                                            |
| ----------- | ---------------- | ---------------------------------------------------- |
| Filename    | สตริง             | ชื่อสมุดงานที่ล็อกแล้วซึ่งบริการส่งคืนกลับมา       |
| FileSize    | จำนวนเต็ม         | ขนาดไฟล์ที่ล็อกแล้วเป็นไบต์                         |
| FileContent | สตริง (Base64)    | สมุดงานที่ล็อกแล้วซึ่งถูกเข้ารหัสเป็นสตริง Base64   |

เพื่อดึงสมุดงานที่ล็อกแล้ว ให้ถอดรหัสค่า `FileContent` จาก Base64 และบันทึกไฟล์โดยใช้ `Filename` ที่ระบุไว้ในการตอบกลับ

### **การจัดการข้อผิดพลาด**

– API จะส่งรหัสสถานะ HTTP มาตรฐาน (เช่น `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) ร่วมกับออบเจกต์ข้อผิดพลาด JSON ที่มีฟิลด์ `Code` และ `Message`

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}