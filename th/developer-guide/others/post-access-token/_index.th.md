---
---
title: "Aspose.Cells Cloud Web API - การขอโทเคนการเข้าถึง"
second_title: "เอกสาร"
ArticleTitle: "รับโทเคนการเข้าถึงโดยใช้ Client ID และ Secret"
linktitle: "การขอโทเคนการเข้าถึง"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, คลาวด์, โทเคนการเข้าถึง, OAuth2, API, การพิสูจน์ตัวตน, REST, Excel, Office Cloud"
description: "รับโทเคนการเข้าถึง OAuth2 สำหรับ Aspose.Cells Cloud โดยการเรียก endpoint POST /cells/connect/token ด้วย Client ID และ Secret ของคุณ"
weight: 100
---

รับโทเคนการเข้าถึงโดยใช้ Cells Cloud Get Token API ด้วย Client ID และ Secret

## API การขอโทเคนการเข้าถึง

ก่อนที่จะเรียก endpoint ดังกล่าว คุณจำเป็นต้องมี:

* บัญชี Aspose Cloud ที่ลงทะเบียนไว้แล้ว  
* **Client ID** และ **Client Secret** ที่สร้างขึ้นในพอร์ทัล Aspose Cloud  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องการ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง                     | คำอธิบาย                                          |
| ---------------- | ---------- | ---------------------------- | ------------------------------------------------- |
| grant_type       | string     | body (form‑url‑encoded)      | ค่าคงที่ `client_credentials` ซึ่งจำเป็นสำหรับ OAuth |
| client_id        | string     | body (form‑url‑encoded)      | ตัวระบุไคลเอนต์ที่จัดให้แก่คุณ                   |
| client_secret    | string     | body (form‑url‑encoded)      | ความลับที่เกี่ยวข้องกับ Client ID                |

**ตัวอย่างคำขอ (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### คำตอบ

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|------------------------------|-----------------------------------------------|
| 200  | สำเร็จ (OK)                  | ค้นหาข้อมูลสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์   |

**ตัวอย่างการจัดการข้อผิดพลาด**

```json
{
  "error": "invalid_client",
  "error_description": "การพิสูจน์ตัวตนของไคลเอนต์ล้มเหลว"
}
```

## วิธีใช้ Get public key API ด้วย SDK

### ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเริ่มต้นใช้งาน SDK จะซ่อนรายละเอียด HTTP ไว้เบื้องหลัง ช่วยให้คุณรับโทเคนการเข้าถึงสำหรับ Cells ได้ด้วยโค้ดเพียงเล็กน้อย

โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud SDK จัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:  
---