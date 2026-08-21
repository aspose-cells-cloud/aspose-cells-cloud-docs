---
title: "API คลาวด์ Aspose.Cells Excel สำหรับการยกเลิกการป้องกันเว็บ – ลบรหัสผ่านเปิดและแก้ไขโดยการเขียนโปรแกรม"
second_title: "เอกสาร"
ArticleTitle: "ยกเลิกการป้องกันรหัสผ่าน Excel – ปลดล็อกรหัสผ่านเปิดและแก้ไขได้ทันที"
linktype: "unprotect-spreadsheet"
type: docs
url: /unprotect-spreadsheet/
keywords: "ยกเลิกการป้องกัน, สเปรดชีต, Aspose.Cells, API, Excel, การลบรหัสผ่าน"
description: "ลบรหัสผ่านเปิดและรหัสผ่านการแก้ไขจากไฟล์ Excel โดยการเขียนโปรแกรมด้วย API การยกเลิกการป้องกันสเปรดชีตของ Aspose.Cells Cloud รองรับไฟล์ .xlsx/.xls, การตรวจสอบสิทธิ์แบบ OAuth2 และการประมวลผลแบบเป็นกลุ่ม"
weight: 100
---

API การยกเลิกการป้องกันสเปรดชีตช่วยลบการป้องกันด้วยรหัสผ่านสำหรับการเปิดและการแก้ไขจากไฟล์ Excel ได้ในคำสั่งเดียว เหมาะสำหรับระบบสายงานข้อมูล ระบบจัดการเอกสาร และกระบวนการย้ายข้อมูล

## **API การยกเลิกการป้องกันสเปรดชีต**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                     |
| ---------------- | ---------- | -------- | -------------------------------------------------------------------------------------------- |
| Spreadsheet      | ไฟล์       | FormData | ไฟล์ Excel ที่ต้องการยกเลิกการป้องกัน                                                         |
| password         | ข้อความ    | Query    | รหัสผ่านที่ใช้ป้องกันไฟล์จากการเปิด                                                           |
| modifyPassword   | ข้อความ    | Query    | รหัสผ่านที่ต้องการเพื่อแก้ไขไฟล์ (ไม่บังคับหากตั้งเฉพาะรหัสผ่านเปิดเท่านั้น)                     |
| outPath          | ข้อความ    | Query    | (ไม่บังคับ) ที่อยู่โฟลเดอร์ที่จะบันทึกสมุดงานที่ยกเลิกการป้องกันแล้ว                            |
| outStorageName   | ข้อความ    | Query    | (ไม่บังคับ) ชื่อพื้นที่จัดเก็บที่จะบันทึกไฟล์ผลลัพธ์                                            |
| region           | ข้อความ    | Query    | (ไม่บังคับ) การตั้งค่าภูมิภาคของสเปรดชีต                                                       |

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

การตอบกลับที่สำเร็จจะส่งคืนไฟล์ที่ยกเลิกการป้องกันแล้วในรูปแบบสตรีม ไฟล์สามารถบันทึกไปยังตำแหน่งที่ระบุโดย `outPath`/`outStorageName` หรือเรียกใช้งานได้โดยตรงจากข้อมูลโหลดของการตอบกลับ

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                  | คำอธิบาย                                                           |
| ---- | ------------------------- | ------------------------------------------------------------------ |
| 200  | สำเร็จ (OK)               | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                           |
| 413  | ข้อมูลโหลดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                              |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                   |

## เมื่อใดควรใช้ API การยกเลิกการป้องกันสเปรดชีต?

- **กู้คืนการเข้าถึงสมุดงานที่ล็อกไว้** – ลบรหัสผ่านเปิดหรือรหัสผ่านการแก้ไขที่ลืมได้อย่างรวดเร็วโดยไม่ต้องดำเนินการด้วยตนเอง
- **ดำเนินการปลดล็อกจำนวนมากโดยอัตโนมัติ** – ประมวลผลไฟล์จำนวนมากในโครงการย้ายข้อมูลหรือการจัดเก็บข้อมูลระยะยาว
- **บูรณาการกับกระบวนการที่มีอยู่แล้ว** – ผสานรวมกับ API สำหรับการจัดเก็บหรือการแปลง เพื่อสร้างสายงานแบบครบวงจร (เช่น อัปโหลด → ยกเลิกการป้องกัน → แปลงเป็น PDF)
- **รักษาความปลอดภัยข้อมูล** – การดำเนินการเกิดขึ้นที่ฝั่งเซิร์ฟเวอร์ ช่วยให้ไฟล์ต้นฉบับยังคงปลอดภัยในขณะที่เวอร์ชันที่ยกเลิกการป้องกันแล้วถูกจัดเก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ของคุณ

## วิธีใช้ API การยกเลิกการป้องกันสเปรดชีตด้วย SDK

### ข้อกำหนด OpenAPI

[ข้อกำหนด API การยกเลิกการป้องกันสเปรดชีต](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) จัดเตรียมอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ เพื่อช่วยให้สามารถโต้ตอบกับ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (เข้ารหัส Base64)",
  "contentType": "MIME type",
  "fileDownloadName": "ชื่อไฟล์ (ไม่บังคับ)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK ช่วยทำให้การเรียกใช้งานง่ายขึ้นโดยจัดการการตรวจสอบสิทธิ์ การสร้างคำขอ และการประมวลผลการตอบกลับ SDK มีให้ใช้งานในหลายภาษาและรวมเมธอดสำเร็จรูปสำหรับการยกเลิกการป้องกันสเปรดชีตไว้ด้วย

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ API การยกเลิกการป้องกันสเปรดชีตโดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}