---
title: "เข้ารหัส, ถอดรหัส และลงลายมือชื่อดิจิทัลให้กับไฟล์ Excel"
second_title: "เอกสาร"
linktype: "ป้องกัน Excel"
type: docs
url: /protect/
aliases: [/workbook/password/]
keywords: "Excel, ป้องกัน, เข้ารหัส, ถอดรหัส, ลายมือชื่อดิจิทัล, Aspose.Cells Cloud, REST API, รหัสผ่าน, ความปลอดภัย"
description: "เรียนรู้วิธีการป้องกัน เข้ารหัส ถอดรหัส และลงลายมือชื่อดิจิทัลให้กับสมุดงาน Excel ด้วย Aspose.Cells Cloud REST API – ตัวอย่างโค้ดสำหรับ Android, C#, Java, Python และอื่นๆ"
ArticleTitle: "เข้ารหัส ถอดรหัส ลงลายมือชื่อดิจิทัล และป้องกันไฟล์ Excel โดยใช้ Aspose.Cells Cloud API"
weight: 36
---

## **การป้องกันและยกเลิกการป้องกันไฟล์ Excel**

**"การป้องกัน" ใน Aspose.Cells Cloud คืออะไร?**  
การดำเนินการ **Protect** ช่วยรักษาความปลอดภัยให้กับสมุดงาน Excel โดยการใช้รหัสผ่านเพื่อจำกัดการเปิด อ่าน แก้ไข หรือเปลี่ยนแปลงโครงสร้างของไฟล์ API ยังรองรับการเข้ารหัสสมุดงาน การถอดรหัส และการเพิ่มลายมือชื่อดิจิทัลเพื่อการตรวจสอบความสมบูรณ์ของข้อมูล

**การอ้างอิง API**

| วิธี HTTP | จุดปลายทาง | พารามิเตอร์ที่ต้องระบุใน query/body | ตัวอย่างเนื้อหาคำขอ | คำตอบที่พบบ่อย |
|-----------|------------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (path), `password` (query) | `{ "password": "MySecret123" }` | `200 OK` – ใช้การป้องกันแล้ว, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (path), `password` (query) | ไม่มี | `200 OK` – ยกเลิกการป้องกันแล้ว, รหัสข้อผิดพลาดดังกล่าวข้างต้น |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (path), `password` (query) | ไม่มี | `200 OK` – ไฟล์ถูกเข้ารหัสแล้ว |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (path), `password` (query) | ไม่มี | `200 OK` – ไฟล์ถูกถอดรหัสแล้ว |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (path) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – เพิ่มลายมือชื่อดิจิทัลแล้ว |

**ตัวอย่างโค้ด (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// เริ่มต้นไคลเอนต์ API
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// ป้องกันสมุดงาน
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**ข้อกำหนดเบื้องต้น**  
- สมาชิกภาพ Aspose.Cells Cloud ที่ยังไม่หมดอายุ  
- `AppSid` และ `AppKey` สำหรับการตรวจสอบสิทธิ์  

**การตรวจสอบสิทธิ์**  
คำขอทั้งหมดต้องแนบ header `Authorization` พร้อมโทเคน JWT ที่ถูกต้องซึ่งได้มาจากการตรวจสอบสิทธิ์ของ Aspose Cloud

**การจัดการข้อผิดพลาด**  
ตรวจสอบรหัสสถานะ HTTP และออบเจกต์ `Error` ที่ส่งกลับมาในเนื้อหาของคำตอบ ข้อผิดพลาดที่พบบ่อย ได้แก่ รหัสผ่านไม่ถูกต้อง (`400`) ไฟล์หายไป (`404`) และความล้มเหลวในการตรวจสอบสิทธิ์ (`401`)

**หมายเหตุ**  
- สามารถใช้จุดปลายทางเดียวกันในการ **เข้ารหัส** หรือ **ถอดรหัส** ได้โดยเปลี่ยนส่วนการดำเนินการ (`/encrypt`, `/decrypt`)  
- ลายมือชื่อดิจิทัลต้องใช้ไฟล์ใบรับรองที่ถูกต้องและสามารถเข้าถึงได้โดย API  

- [เข้ารหัสไฟล์ Excel ด้วย Aspose.Cells Cloud API](/cells/excel-file-encrypt/)
- [ป้องกันไฟล์ Excel ด้วย Aspose.Cells Cloud API](/cells/protect-excel-file/)
- [เพิ่มลายมือชื่อดิจิทัลให้กับไฟล์ Excel](/cells/excel-digital-signature/)
- [ป้องกันไฟล์ Excel – คู่มือแบบละเอียด](/cells/protect-excel-files/)
- [ตั้งรหัสผ่านให้กับไฟล์ Excel](/cells/workbook/password/modify/)
- [ถอดรหัสไฟล์ Excel](/cells/excel-file-decrypt/)
- [ยกเลิกการป้องกันไฟล์ Excel](/cells/excel-file-unprotect/)
- [ปลดล็อกไฟล์ Excel](/cells/unlock-excel-files/)
- [ล้างรหัสผ่านของไฟล์ Excel](/cells/clear-excel-files-password/)
---