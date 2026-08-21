---
title: "ประเมิน Aspose.Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "ประเมิน Aspose.Cells Cloud"
LinkTitle: "ประเมิน"
type: docs
url: /th/evaluate-aspose-cells/
description: "สำรวจ Aspose.Cells Cloud ซึ่งเป็น REST API สำหรับการสร้าง แปลง ผสาน แยก ป้องกัน และจัดการไฟล์ Excel และรูปแบบสเปรดชีตอื่นๆ"
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - การจัดการสเปรดชีต
  - ใช้งานทดลองฟรี
  - ประเมิน
---

คุณสามารถประเมิน REST API ของ **Aspose.Cells Cloud** โดยการสร้างบัญชีใช้งานทดลองฟรีผ่านแดชบอร์ด Aspose Cloud หลังจากลงทะเบียนแล้ว คุณจะได้รับ **Client Id** และ **Client Secret** ซึ่งอนุญาตให้เรียกใช้ API ได้สูงสุด 150 ครั้งต่อเดือน

**ข้อกำหนดเบื้องต้น**  
ก่อนเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าคุณมีการเชื่อมต่ออินเทอร์เน็ตที่ใช้งานได้และสภาพแวดล้อมการพัฒนาที่รองรับ API สามารถเรียกใช้งานผ่าน HTTP โดยตรง หรือคุณสามารถใช้หนึ่งใน SDK ของ Aspose.Cells (เช่น .NET, Java, Python, PHP) เพื่อให้การบูรณาการง่ายขึ้น

**ขั้นตอนเริ่มต้นอย่างรวดเร็ว**

1. **สร้างบัญชีใช้งานทดลองฟรี** – ไปที่ [แดชบอร์ด Aspose Cloud](https://dashboard.aspose.cloud) ลงทะเบียนและยืนยันที่อยู่อีเมลของคุณ  
2. **รับข้อมูลรับรอง** – ค้นหา *Client Id* และ *Client Secret* ในส่วน **Authentication** ของแดชบอร์ด  
3. **สร้างโทเคนการเข้าถึง** – ส่งคำขอ `POST` ไปยัง `https://api.aspose.cloud/connect/token` พร้อมข้อมูลรับรองของคุณ (ดูเอกสารอ้างอิง API เพื่อดูข้อมูลที่ส่งไปอย่างละเอียด)  
4. **เรียกใช้ API ครั้งแรกของคุณ** – ใส่โทเคนในส่วนหัว `Authorization: Bearer <token>` และเรียกใช้จุดสิ้นสุดที่ง่าย เช่น `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`  

การใช้งานทดลองฟรีนี้จะให้คุณได้รับประสบการณ์เชิงปฏิบัติเกี่ยวกับความสามารถของบริการ ช่วยให้คุณสามารถเริ่มต้นพัฒนาและทดสอบได้โดยไม่ต้องจ่ายค่าใช้จ่ายใดๆ

**สรุปเอกสารอ้างอิง API**

| การดำเนินการ | เมธอด | URL | พารามิเตอร์ที่จำเป็น | ตัวอย่างการตอบกลับ |
|---------------|--------|-----|------------------------|---------------------|
| รับโทเคนการเข้าถึง | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (form-urlencoded) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| แสดงรายการเวิร์กชีต | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | เส้นทาง: `{file}` – ชื่อของสมุดงานที่อัปโหลด; ส่วนหัว: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

สำหรับรายละเอียดเกี่ยวกับราคา ขีดจำกัดการใช้งาน และตัวเลือกแผนบริการเพิ่มเติม โปรดดูที่หน้า [แผนใช้งานทดลอง](https://purchase.aspose.cloud/trial)