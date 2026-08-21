---
---
title: "นำเข้าข้อมูล JSON ลงใน Excel"
second_title: "เอกสาร"
linktype: "นำเข้า JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, การนำเข้า JSON, Excel API, การนำเข้า JSON ผ่าน REST, ตัวอย่าง SDK"
description: "เรียนรู้วิธีการนำเข้าข้อมูล JSON ลงในเวิร์กชีต Excel ด้วย Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรายละเอียดจุดปลาย (endpoint), ตัวอย่างคำขอ/การตอบกลับ และโค้ด SDK สำหรับ .NET, Java และ Python"
weight: 40
---

REST API นี้ **นำเข้าข้อมูล JSON** ลงในเวิร์กชีต Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์       | ตำแหน่ง     | ชนิดข้อมูล | คำอธิบาย                                                                                          |
| --------------------- | ------------ | ---------- | ------------------------------------------------------------------------------------------------- |
| name                  | Path         | string     | ชื่อไฟล์สมุดงาน                                                                                  |
| importJsonRequest     | HTTP body    | class      | ข้อมูลคำขอที่มีรายละเอียดการนำเข้า JSON                                                         |
| password              | Query string | string     | รหัสผ่านสำหรับเปิดสมุดงาน (ถ้ามีการป้องกันไว้)                                                   |
| folder                | Query string | string     | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ                                                                    |
| storageName           | Query string | string     | ชื่อของพื้นที่จัดเก็บที่เก็บสมุดงานไว้                                                           |
| outPath               | Query string | string     | ตำแหน่งไฟล์ผลลัพธ์หลังการนำเข้า หากไม่ระบุ สมุดงานที่อัปเดตจะถูกส่งกลับมาในส่วนของคำตอบ         |
| outStorageName        | Query string | string     | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์                                                               |
| checkExcelRestriction | Query string | string     | ค่าบูลีนระบุว่าจะบังคับข้อจำกัดเฉพาะของ Excel (true/false)                                       |

### **ตัวอย่างเนื้อหาคำขอ**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### การตอบกลับ

คำขอที่ประสบความสำเร็จจะส่งกลับ **HTTP 200** พร้อมกับ JSON payload ที่มีลักษณะดังนี้:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

รหัสสถานะที่เป็นไปได้:

| รหัส | ความหมาย                                      |
| ---- | --------------------------------------------- |
| 200  | การนำเข้าสำเร็จ                               |
| 400  | คำขอไม่ถูกต้อง – ข้อมูลขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – token ไม่ถูกต้องหรือขาดหาย |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                    |


## วิธีใช้ API PostWorkbookImportJson ด้วย SDK

### ข้อกำหนด PostWorkbookImportJson API

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ สำหรับรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด กรุณาเยี่ยมชม [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

---