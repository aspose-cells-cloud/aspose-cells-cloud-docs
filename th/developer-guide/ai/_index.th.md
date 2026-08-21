---
---
title: "Aspose.Cells Cloud AI – การย่อยภารกิจ, การแปลงสเปรดชีต และข้อความ"
second title: "เอกสาร"
ArticleTitle: "พัฒนาทักษะ AI ของคุณ: เรียนรู้การแปลง Excel, การย่อยภารกิจ และอื่นๆ"
linktype: "AI"
type: docs
url: /ai/
keywords: "Aspose.Cells, Cloud AI, การแปลง Excel, การย่อยภารกิจ, REST API"
description: "สำรวจ Aspose.Cells Cloud AI เพื่อย่อยภารกิจ แปลงสมุดงาน Excel และไฟล์ข้อความ พร้อมรวมถึงจุดสิ้นสุด REST ตัวอย่างโค้ด และแนวทางปฏิบัติที่ดีที่สุด"
weight: 20
---

Aspose.Cells Cloud AI มีบริการขับเคลื่อนด้วย AI สามบริการที่ช่วยให้การทำงานกับข้อมูล Excel และข้อความง่ายขึ้น ได้แก่ **ย่อยภารกิจของผู้ใช้**, **แปลงสเปรดชีต**, และ **แปลงไฟล์ข้อความ** แอปพลิเคชันเหล่านี้ช่วยให้นักพัฒนาสามารถย่อยเป้าหมายผู้ใช้ที่ซับซ้อนเป็นขั้นตอนที่สามารถดำเนินการได้อย่างเป็นระบบ แปลงสมุดงานทั้งหมดหรือไฟล์ข้อความแบบธรรมดา และรวมผลลัพธ์เหล่านี้เข้ากับแอปพลิเคชันที่พัฒนาขึ้นเองได้อย่างมีประสิทธิภาพ ใช้จุดสิ้นสุดด้านล่างเพื่อเริ่มต้นได้อย่างรวดเร็ว และอ้างอิงข้อมูลเฉพาะรายละเอียดของคำขอ/การตอบกลับที่ให้ไว้สำหรับแต่ละบริการ

- **[ย่อยภารกิจของผู้ใช้](https://docs.aspose.cloud/cells/decompose-user-task/)** – แปลงเป้าหมายของผู้ใช้เป็นแผนการดำเนินการตามลำดับด้วย Aspose.Cells Cloud AI  
  - **วิธีการร้องขอ:** `POST`  
  - **URL ของจุดสิ้นสุด:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **ส่วนหัว:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **เนื้อหาคำขอ (JSON):**  
    ```json
    {
      "task": "สร้างรายงานยอดขายรายไตรมาสพร้อมกราฟและพิวต์แท็บล์"
    }
    ```  
  - **การตอบกลับ:** ส่งคืนไฟล์สเปรดชีตที่มีรายการภารกิจเป็นไฟล์ที่สามารถดาวน์โหลดได้  
  - **รหัสสถานะ:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **ข้อกำหนดเบื้องต้น:** โทเคนการเข้าถึงที่ถูกต้องพร้อมขอบเขต **CellsAI**  
  - **ตัวอย่างการตอบกลับ (ส่วน JSON):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **หมายเหตุ:** สมุดงานที่สร้างขึ้นจะมีชีตชื่อ **TaskList** ที่มีขั้นตอนที่เรียงลำดับแล้ว ขีดจำกัดอัตรา: 100 คำขอต่อนาที

- **[แปลงสเปรดชีต](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – แปลงสเปรดชีตทั้งหมดด้วย Aspose.Cells Cloud AI  
  - **วิธีการร้องขอ:** `POST`  
  - **URL ของจุดสิ้นสุด:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **ส่วนหัว:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **พารามิเตอร์คำขอ:**  
    - `file` – ไฟล์ Excel ที่ต้องการแปลง (ไบนารี)  
    - `targetLanguage` – รหัสภาษา ISO (เช่น `fr`, `de`)  
  - **การตอบกลับ:** ส่งคืนสมุดงานที่แปลแล้วเป็นไฟล์ที่สามารถดาวน์โหลดได้  
  - **รหัสสถานะ:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **ข้อกำหนดเบื้องต้น:** โทเคนการเข้าถึงพร้อมขอบเขต **CellsAI** และมีโควต้าพื้นที่จัดเก็บเพียงพอ  
  - **ตัวอย่างการตอบกลับ (ส่วน JSON):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **หมายเหตุ:** ค่าในเซลล์ทั้งหมด คำอธิบาย และชื่อชีตจะถูกแปลงทั้งหมด ขีดจำกัดอัตรา: 100 คำขอต่อนาที

- **[แปลงไฟล์ข้อความ](https://docs.aspose.cloud/cells/translate-text-file/)** – แปลงไฟล์ข้อความทั้งหมดด้วย Aspose.Cells Cloud AI  
  - **วิธีการร้องขอ:** `POST`  
  - **URL ของจุดสิ้นสุด:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **ส่วนหัว:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **พารามิเตอร์คำขอ:**  
    - `file` – ไฟล์ข้อความที่ต้องการแปลง (ไบนารี)  
    - `targetLanguage` – รหัสภาษา ISO (เช่น `es`, `ja`)  
  - **การตอบกลับ:** ส่งคืนไฟล์ข้อความที่แปลแล้ว  
  - **รหัสสถานะ:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **ข้อกำหนดเบื้องต้น:** โทเคนการเข้าถึงที่ถูกต้องพร้อมขอบเขต **CellsAI**  
  - **ตัวอย่างการตอบกลับ (ส่วน JSON):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **หมายเหตุ:** รองรับไฟล์ข้อความธรรมดาที่เข้ารหัส UTF-8 สูงสุด 5 เมกะไบต์ ขีดจำกัดอัตรา: 100 คำขอต่อนาที
---