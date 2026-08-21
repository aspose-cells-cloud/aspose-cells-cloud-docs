---
title: "แปลงข้อความในสเปรดชีตระยะไกล"
ArticleTitle: "แปลงข้อความในสเปรดชีตระยะไกล – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktype: "docs"
url: /th/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, การแปลงข้อความ, API"
description: "แปลงข้อความในช่วงที่ระบุของแผ่นงาน รวมถึงการแปลงตัวเลข การแทนที่อักขระ การจัดการการขึ้นบรรทัดใหม่ และการปรับให้ตัวอักษรที่มีเครื่องหมายเน้นเป็นรูปแบบไม่มีเครื่องหมายเน้น"
weight: 1000
---

## การแปลงข้อความในสเปรดชีตระยะไกลของ Aspose.Cells Cloud Web Services

หมายถึงการแปลงตัวเลขที่ถูกจัดเก็บในรูปแบบข้อความให้อยู่ในรูปแบบตัวเลขที่ถูกต้อง การแทนที่อักขระและการขึ้นบรรทัดใหม่ที่ไม่ต้องการด้วยอักขระที่ต้องการ และการแปลงอักขระที่มีเครื่องหมายเน้นให้เป็นอักขระที่เทียบเท่าโดยไม่มีเครื่องหมายเน้น

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|-------------|
| name             | string | Path | (จำเป็น) ชื่อไฟล์สมุดบันทึกที่ต้องการดึงข้อมูล |
| worksheet        | string | Path | ระบุแผ่นงานของสเปรดชีต |
| range            | string | Path | ระบุช่วงของแผ่นงานในสเปรดชีต |
| convertTextType  | string | Query | ระบุประเภทของการแปลงข้อความ (จำเป็น) |
| sourceCharacters | string | Query | ระบุอักขระต้นทาง (ไม่บังคับ) |
| targetCharacters | string | Query | ระบุอักขระเป้าหมาย (ไม่บังคับ) |
| folder           | string | Query | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดบันทึก ค่าเริ่มต้นคือ null |
| storageName      | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บหากใช้พื้นที่จัดเก็บแบบคลาวด์ที่กำหนดเอง หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น |
| region           | string | Query | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะภูมิภาค (ไม่บังคับ) |
| password         | string | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต (ไม่บังคับ) |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| - | - | - |

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "การแปลงข้อความเสร็จสิ้นเรียบร้อยแล้ว",
  "Data": {
    // รายละเอียดของผลลัพธ์การแปลง เช่น จำนวนเซลล์ที่อัปเดต สามารถเพิ่มได้ที่นี่
  }
}
```

**รหัสสถานะการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | OK | การดำเนินการแปลงข้อความเสร็จสิ้นเรียบร้อยแล้ว |
| 400 | Bad Request | คำขอมีรูปแบบไม่ถูกต้องหรือขาดพารามิเตอร์ที่จำเป็น |
| 401 | Unauthorized | การยืนยันตัวตนล้มเหลวหรือ JWT token หายไป/ไม่ถูกต้อง |
| 413 | Payload Too Large | เนื้อหาคำขอเกินขนาดที่กำหนด |
| 500 | Internal Server Error | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้การแปลงข้อความในสเปรดชีตระยะไกลด้วย SDK

### ข้อมูลจำเพาะการแปลงข้อความในสเปรดชีตระยะไกล

[ข้อมูลจำเพาะ API การแปลงข้อความในสเปรดชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่ใช้งานผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "การแปลงข้อความเสร็จสิ้นเรียบร้อยแล้ว",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "แปลงตัวเลขแล้ว, แทนที่อักขระแล้ว, ปรับการขึ้นบรรทัดใหม่ให้เป็นมาตรฐาน"
  }
}
```

{< /tab >}

{< /tabs >}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> kho ithub ของ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose Cells Cloud ผ่าน SDK ต่างๆ:
 `[TBD]`
---