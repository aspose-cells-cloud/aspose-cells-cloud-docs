---
title: "ผสานไฟล์ Excel หลายไฟล์ลงในสมุดงานเดียว"
second_title: "เอกสาร"
linktype: "ผสานไฟล์ Excel หลายไฟล์"
type: docs
url: /th/merge-multi-files-into-excel/
aliases: [  /th/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud, ผสานไฟล์ Excel หลายไฟล์, REST API, การผสานสเปรดชีต, SDK บนคลาวด์"
description: "เรียนรู้วิธีการผสานสมุดงาน Excel หลายไฟล์ลงในไฟล์เดียวโดยใช้ REST API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0) ประกอบด้วย HTTPS endpoint, คำสั่ง cURL, ตัวอย่าง SDK, พารามิเตอร์ที่จำเป็น และรายละเอียดการจัดการข้อผิดพลาด"
weight: 32
---

## REST API

REST API นี้ใช้ผสานไฟล์ Excel หลายไฟล์ลงในสมุดงาน Excel เดียว

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและบังคับใช้การยืนยันตัวตนด้วย <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">โทเคน JWT</a>


### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                                   | จำเป็น |
| ---------------- | ------- | -------- | ------------------------------------------------------------------------------------------ | ------ |
| files[]          | file    | formData | สมุดงาน Excel หนึ่งไฟล์ขึ้นไปที่จะผสาน ใช้ `file1`, `file2`, … ในคำขอ                       | ใช่    |
| format           | string  | query    | รูปแบบไฟล์ส่งออกที่ต้องการ (เช่น `xlsx`)                                                   | ใช่    |
| mergeToOneSheet  | boolean | query    | ตั้งค่าเป็น `true` เพื่อรวมแผ่นงานทั้งหมดลงในแผ่นงานเดียว ค่าเริ่มต้นคือ `false`              | ไม่จำเป็น |

### **การตอบกลับ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[ชื่อไฟล์ที่ผสานแล้ว]",
    "Filesize" : [ขนาดไฟล์],
    "FileContent" : "[Base64String]"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                                     |
|-----|------------------------------|-------------------------------------------------------------|
| 200 | สำเร็จ (OK)                  | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของOPERATION |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                              |
| 413 | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                           |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                       |
## วิธีใช้ PostMerge API ผ่าน SDK

### ข้อกำหนด PostMerge API

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ คุณจึงสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) สำหรับรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}