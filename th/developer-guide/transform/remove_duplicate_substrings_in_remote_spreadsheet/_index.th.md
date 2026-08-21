---
title: "ลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกล"
ArticleTitle: "ลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกล – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "ลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกล"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, ลบสตริงที่ซ้ำกัน, API"
description: "API สำหรับค้นหาและลบสตริงที่ซ้ำกันภายในเซลล์ของช่วงที่ระบุในสมุดงาน"
weight: 1
---

## การลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกลของ Aspose.Cells Cloud Web Services

ค้นหาและลบสตริงที่ซ้ำกันภายในแต่ละเซลล์ของช่วงที่เลือก โดยใช้ตัวคั่นที่ผู้ใช้กำหนดหรือตัวคั่นที่กำหนดไว้ล่วงหน้า ทั้งนี้ยังคงรักษาสูตร การจัดรูปแบบ และการตรวจสอบข้อมูลไว้

**วิธีการตรวจจับสตริงที่ซ้ำกัน**  
1. ค่าในแต่ละเซลล์จะถูกแบ่งออกเป็นสตริงย่อยตามตัวคั่นที่เลือก  
2. เครื่องมือนี้จะเปรียบเทียบสตริงย่อย **ภายในเซลล์เดียวกัน** และเก็บเฉพาะ **ครั้งแรก** ของสตริงย่อยที่ซ้ำกันไว้  
3. สตริงย่อยที่ทำความสะอาดแล้วจะถูกเชื่อมกลับเข้าด้วยกันโดยใช้ตัวคั่นเดียวกัน และเขียนกลับลงในเซลล์  

**ตัวเลือกตัวคั่น**  
- รายการที่กำหนดไว้ล่วงหน้า: จุลภาค อัฒภาค ช่องว่าง แท็บ ขึ้นบรรทัดใหม่  
- `Custom` – ป้อนตัวอักษรใดก็ได้ (หนึ่งตัวหรือหลายตัว); ตัวอักษรหลายตัวจะถือเป็นตัวคั่นเดียวที่ประกอบด้วยหลายตัว  
- `TreatConsecutiveDelimitersAsOne` – รวมตัวคั่นที่อยู่ติดกันให้เป็นตัวคั่นตัวเดียว  

เฉพาะเซลล์ที่เป็นข้อมูลชนิดสตริงเท่านั้นที่จะถูกประมวลผล; ตัวเลข ค่าบูลีน และสูตรจะถูกแปลงเป็นสตริงก่อนการแบ่ง (สูตรจะถูกลบออก) ส่งคืนจำนวนเซลล์ที่ทำความสะอาดแล้วและสตรีมสมุดงานที่อัปเดตแล้ว

### จุดสิ้นสุดของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์ของ Request

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|---------|-----------------------------|-------------|
| name | string | Path | (จำเป็น) ชื่อของไฟล์สมุดงานที่ต้องการดึงข้อมูล |
| worksheet | string | Path | ระบุชีตของสเปรดชีต |
| range | string | Path | ระบุช่วงของชีตในสเปรดชีต |
| delimiters | string | Query | ตัวคั่นที่ใช้ในการแบ่งค่าในเซลล์ (เช่น จุลภาค อัฒภาค ช่องว่าง แท็บ ขึ้นบรรทัดใหม่) จำเป็นต้องระบุ |
| treatConsecutiveDelimitersAsOne | boolean | Query | รวมตัวคั่นที่อยู่ติดกันให้เป็นตัวคั่นตัวเดียว ค่าเริ่มต้น: true ไม่บังคับ |
| caseSensitive | boolean | Query | ใช้การเปรียบเทียบที่คำนึงถึงตัวพิมพ์ใหญ่-เล็กเมื่อตรวจจับสตริงที่ซ้ำกัน ไม่บังคับ |
| folder | string | Query | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้น: null |
| storageName | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บหากใช้คลาวด์สตอเรจแบบกำหนดเอง |
| region | string | Query | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ไม่บังคับ |
| password | string | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต ไม่บังคับ |

### พารามิเตอร์ของ Request Body

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| - | - | ไม่จำเป็นต้องส่ง request body สำหรับการทำงานนี้ |

### **Response**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```

**รหัสสถานะของ Response**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | OK | การดำเนินการสำเร็จ; ส่งคืนจำนวนเซลล์ที่ทำความสะอาดแล้วและสตรีมสมุดงานที่อัปเดตแล้ว |
| 400 | Bad Request | พารามิเตอร์ของ request หนึ่งพารามิเตอร์ขึ้นไปขาดหายหรือไม่ถูกต้อง |
| 401 | Unauthorized | การยืนยันตัวตนล้มเหลว หรือ JWT token ขาดหายหรือไม่ถูกต้อง |
| 413 | Payload Too Large | Request มีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | Internal Server Error | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้การลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกลด้วย SDK

### ข้อมูลระบุการลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกล

[ข้อมูลระบุ API การลบสตริงที่ซ้ำกันในสเปรดชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) กำหนดอินเทอร์เฟซการโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณใช้งาน REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# ใช้ HTTPS เพื่อเชื่อมต่อแบบปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```
{< /tab >}
{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดู <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose Cells Cloud ด้วย SDK ต่างๆ:
`[TBD]`