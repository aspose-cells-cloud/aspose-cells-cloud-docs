---
---
title: "ลบอักขระตามตำแหน่ง"
ArticleTitle: "ลบอักขระตามตำแหน่ง – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ลบอักขระตามตำแหน่ง"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, ลบอักขระ, API"
description: "ลบอักขระออกจากเซลล์ตามตำแหน่งในไฟล์ตารางคำนวณ"
weight: 100
---

## การลบอักขระตามตำแหน่งด้วยบริการเว็บ Aspose.Cells Cloud

ลบอักขระออกจากทุกเซลล์ในช่วงที่กำหนดตามตำแหน่ง (N อักขระแรก/สุดท้าย, ก่อน/หลังสตริงย่อย หรือระหว่างตัวคั่วสองตัว) โดยคงรูปแบบสูตร การจัดรูปแบบ และการตรวจสอบข้อมูลไว้

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์          | ประเภท    | เส้นทาง/สตริงคำสั่ง/เนื้อหา HTTP Body | คำอธิบาย                                                                                                          |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | ไฟล์    | FormData                    | อัปโหลดไฟล์ตารางคำนวณ                                                                                              |
| theFirstNCharacters       | จำนวนเต็ม | Query                       | ระบุการลบอักขระ n ตัวแรกออกจากเซลล์ที่เลือก เลือกได้                                                               |
| theLastNCharacters        | จำนวนเต็ม | Query                       | ระบุการลบอักขระ n ตัวสุดท้ายออกจากเซลล์ที่เลือก เลือกได้                                                            |
| allCharactersBeforeText   | สตริง  | Query                       | ลบข้อความที่อยู่ก่อนสตริงย่อยที่ระบุ เลือกได้                                                                          |
| allCharactersAfterText    | สตริง  | Query                       | ลบข้อความที่อยู่หลังสตริงย่อยที่ระบุ เลือกได้                                                                          |
| caseSensitive             | ค่าบูลีน | Query                       | มีผลต่อโหมด `Substring` และ `CustomChars` เมื่อเปิดใช้งาน เลือกได้                                                   |
| worksheet                 | สตริง  | Query                       | ระบุชีตงานของไฟล์ตารางคำนวณ เลือกได้                                                                                  |
| range                     | สตริง  | Query                       | ระบุช่วงของชีตงานในไฟล์ตารางคำนวณ (เช่น `A1:B10`) เลือกได้                                                            |
| outPath                   | สตริง  | Query                       | (เลือกได้) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null เลือกได้                                                 |
| outStorageName            | สตริง  | Query                       | ชื่อพื้นที่จัดเก็บไฟล์ผลลัพธ์ เลือกได้                                                                                 |
| region                    | สตริง  | Query                       | การตั้งค่าภูมิภาค/ภาษาของไฟล์ตารางคำนวณ (เช่น `en-US`, `fr-FR`) เลือกได้                                              |
| password                  | สตริง  | Query                       | รหัสผ่านสำหรับเปิดไฟล์ตารางคำนวณ เลือกได้                                                                             |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์ตารางคำนวณ |

### **การตอบกลับ**

```json
{
  "status": "OK",
  "message": "ลบอักขระเรียบร้อยแล้ว",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**รหัสสถานะการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | การดำเนินการเสร็จสมบูรณ์ และส่งคืนไฟล์ที่ประมวลผลแล้ว |
| 400 | คำขอไม่ถูกต้อง | คำขอผิดรูปแบบหรือมีพารามิเตอร์ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต | การรับรองความถูกต้องล้มเหลว หรือไม่มี/โทเค็น JWT ไม่ถูกต้อง |
| 413 | ข้อมูลส่งไปขนาดใหญ่เกินไป | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดที่ไม่คาดคิดบนฝั่งเซิร์ฟเวอร์ |

## วิธีใช้การลบอักขระตามตำแหน่งด้วย SDK

### ข้อมูลจำเพาะของการลบอักขระตามตำแหน่ง

[ข้อมูลจำเพาะ API การลบอักขระตามตำแหน่ง](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "ลบอักขระเรียบร้อยแล้ว",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`
---