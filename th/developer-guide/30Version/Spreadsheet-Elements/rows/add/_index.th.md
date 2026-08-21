---
title: "วิธีการเพิ่มแถวลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่ม"
type: docs
url: /th/rows/add/
keywords: "Aspose.Cells, เพิ่มแถว, Excel API, REST, C#, Java, Python, Node.js"
description: "คู่มือทีละขั้นตอนในการเพิ่มแถวเดียวหรือหลายแถวลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ดสำหรับ C#, Java, Python และ Node.js"
weight: 20
ArticleTitle: "เพิ่มแถวลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API – คู่มือทีละขั้นตอน"
---

## วิธีการเพิ่มแถวลงในแผ่นงาน Excel

บทความนี้อธิบายวิธีการแทรกแถวว่างเพียงแถวเดียวหรือหลายแถวลงในแผ่นงานที่มีอยู่โดยใช้ Aspose.Cells Cloud REST API ตรวจสอบให้แน่ใจว่าคุณมีคีย์ API ที่ถูกต้องและ SDK ที่รองรับติดตั้งและตั้งค่าเรียบร้อยแล้วก่อนดำเนินการต่อ

**ข้อกำหนดเบื้องต้น**  
- [ ] บัญชี Aspose.Cells Cloud ที่มีการสมัครสมาชิกที่ยังมีผล  
- [ ] API key/Access token ที่สร้างขึ้นจากแดชบอร์ด Aspose Cloud  
- [ ] SDK หนึ่งในตัวที่รองรับ (C#, Java, Python, Node.js) ที่ติดตั้งและตั้งค่าเรียบร้อยแล้ว  

**การอ้างอิง API**  
- **วิธี HTTP:** `POST`  
- **ปลายทาง (Endpoint):** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **พารามิเตอร์ในเส้นทางที่จำเป็น:**  
  - `fileName` – ชื่อไฟล์ Excel ที่เก็บไว้ในคลาวด์  
  - `sheetName` – ชื่อแผ่นงานที่จะเพิ่มแถว  
- **พารามิเตอร์แบบคิวรี (Query Parameters):**  
  - `startrow` – ดัชนีแบบเริ่มต้นที่ 0 ของแถวที่เริ่มการแทรก  
  - `totalRows` – จำนวนแถวที่จะแทรก  
  - `folder` – (ไม่บังคับ) เส้นทางโฟลเดอร์ในคลาวด์ของไฟล์  
  - `storage` – (ไม่บังคับ) ชื่อที่จัดเก็บข้อมูลหากใช้ที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้น  
- **เนื้อหาคำขอ (ตัวอย่าง JSON):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **ตัวอย่าง cURL**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **การตอบกลับที่สำเร็จ (HTTP 200):** ส่งคืนข้อมูลแผ่นงานที่อัปเดตแล้ว รวมถึงจำนวนแถวใหม่  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **ตัวอย่างการตอบกลับข้อผิดพลาด (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "พารามิเตอร์ startrow ไม่ถูกต้อง ต้องเป็นจำนวนเต็มที่ไม่ติดลบ"
  }
  ```

- **รหัสสถานะ (Status Codes):**  

  | รหัส | ความหมาย                             |
  |------|---------------------------------------|
  | 200  | เพิ่มแถวเรียบร้อยแล้ว                 |
  | 400  | พารามิเตอร์ไม่ถูกต้องหรือ JSON ผิดรูปแบบ |
  | 401  | การตรวจสอบสิทธิ์ล้มเหลว               |
  | 404  | ไม่พบไฟล์หรือแผ่นงาน                 |
  | 500  | ข้อผิดพลาดของเซิร์ฟเวอร์               |

ด้านล่างนี้คือลิงก์ด่วนไปยังตัวอย่างโดยละเอียดสำหรับการเพิ่มแถว:

- [วิธีการเพิ่มแถวว่างลงในแผ่นงาน Excel](/cells/rows/add/row/)
- [วิธีการเพิ่มหลายแถวลงในแผ่นงาน Excel](/cells/rows/add/rows/)
---