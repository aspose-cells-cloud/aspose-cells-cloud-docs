---
---
title: "ลบอักขระในสเปรดชีตระยะไกล"
ArticleTitle: "ลบอักขระในสเปรดชีตระยะไกล – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ลบอักขระในสเปรดชีตระยะไกล"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, ลบอักขระ, การประมวลผลข้อความ"
description: "ลบอักขระที่ผู้ใช้กำหนด ชุดสัญลักษณ์ที่กำหนดไว้ล่วงหน้า หรือสตริงย่อยใดๆ ออกจากทุกเซลล์ในช่วงที่เลือก โดยรักษาสูตร รูปแบบ และการตรวจสอบข้อมูลไว้สำหรับสเปรดชีตที่อยู่ในระบบคลาวด์"
weight: 100
---

## การลบอักขระในสเปรดชีตระยะไกลด้วยเว็บเซอร์วิสของ Aspose.Cells Cloud

ลบอักขระที่ผู้ใช้กำหนด ชุดสัญลักษณ์ที่กำหนดไว้ล่วงหน้า หรือสตริงย่อยใดๆ ออกจากทุกเซลล์ในช่วงที่เลือก โดยรักษาสูตร รูปแบบ และการตรวจสอบข้อมูลไว้สำหรับสเปรดชีตที่อยู่ในระบบคลาวด์

### จุดปลายทางของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์    | ชนิดข้อมูล | เส้นทาง/สตริงคำถาม/เนื้อหา HTTP | คำอธิบาย                                                                                                                                                                       |
|---------------------|-----------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string    | เส้นทาง                         | (จำเป็น) ชื่อไฟล์สมุดทำงานที่ต้องการดึงข้อมูล                                                                                                                                    |
| worksheet           | string    | เส้นทาง                         | ระบุชีตงานของสเปรดชีต                                                                                                                                           |
| range               | string    | เส้นทาง                         | ระบุช่วงของชีตงานในสเปรดชีต                                                                                                                                     |
| removeTextMethod    | string    | คิวรี                           | ระบุประเภทวิธีการลบข้อความ                                                                                                                                      |
| characterSets       | string    | คิวรี                           | ระบุชุดอักขระ                                                                                                                                                       |
| removeCustomValue   | string    | คิวรี                           | ระบุค่าที่ต้องการลบแบบกำหนดเอง                                                                                                                                                  |
| caseSensitive       | boolean   | คิวรี                           | ส่งผลต่อโหมด `Substring` และโหมด `CustomChars` เมื่อเปิดใช้งาน                                                                                                                          |
| folder              | string    | คิวรี                           | (ไม่บังคับ) เส้นทางของโฟลเดอร์ที่เก็บสมุดทำงานไว้ ค่าเริ่มต้นคือ null                                                                                                    |
| storageName         | string    | คิวรี                           | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บ หากใช้พื้นที่จัดเก็บคลาวด์แบบกำหนดเอง หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น                                                                               |
| region              | string    | คิวรี                           | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ส่งผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค                                         |
| password            | string    | คิวรี                           | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                                                                                                                         |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| *ไม่มี* | *ไม่มี* | การดำเนินการนี้ไม่ต้องใช้เนื้อหาคำขอ |

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "ลบอักขระเรียบร้อยแล้ว",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | ลบอักขระเรียบร้อยแล้ว และอัปเดตสมุดทำงานแล้ว |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หนึ่งหรือหลายตัวขาดหายไปหรือไม่ถูกต้อง |
| 401 | ไม่มีสิทธิ์ (Unauthorized) | การตรวจสอบสิทธิ์ล้มเหลว – ขาดหายไปหรือโทเค็น JWT ไม่ถูกต้อง |
| 413 | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ขนาดคำขอเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดที่ฝั่งเซิร์ฟเวอร์ |

## วิธีใช้การลบอักขระในสเปรดชีตระยะไกลด้วย SDK

### ข้อมูลเฉพาะของ API การลบอักขระในสเปรดชีตระยะไกล

[ข้อมูลเฉพาะของ API การลบอักขระในสเปรดชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "ลบอักขระเรียบร้อยแล้ว",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> khoงเก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---