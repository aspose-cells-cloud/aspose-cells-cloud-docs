---
---
title: "Aspose.Cells Cloud API – รับคีย์สาธารณะ (v4.0) | เอกสารประกอบ REST"
second_title: "เอกสาร"
ArticleTitle: "รับคีย์สาธารณะ"
linktitle: "รับคีย์สาธารณะ"
type: docs
url: /th/get-public-key/
keywords: "Aspose.Cells, คีย์สาธารณะ, RSA, API, Cloud"
description: "ดึงคีย์สาธารณะ RSA ที่ใช้สำหรับการเข้ารหัสข้อมูลด้วย Aspose.Cells Cloud รวมถึง endpoint, พารามิเตอร์, ตัวอย่างคำขอ/คำตอบ, โค้ดสถานะ HTTP และตัวอย่างการใช้งาน SDK"
weight: 100
---

API นี้ใช้สำหรับดึงคีย์สาธารณะจากอัลกอริทึมการเข้ารหัสแบบไม่สมมาตร

**สรุปโดยย่อ:** ใช้ Aspose.Cells Get Public Key API เพื่อรับคีย์สาธารณะ RSA (ขนาด 2048 บิต) ที่จำเป็นสำหรับการเข้ารหัสข้อมูลเมื่อทำงานกับไฟล์ Excel บนคลาวด์ endpoint จะคืนค่าคีย์ในรูปแบบ JSON และได้รับความปลอดภัยด้วย OAuth 2.0

## **API รับคีย์สาธารณะ**

**ข้อกำหนดเบื้องต้น:**  
ต้องได้รับ access token ของ OAuth 2.0 ที่ถูกต้องซึ่งมี scope `Cells.Read` ก่อนที่จะเรียก endpoint นี้

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**ตัวอย่างคำขอ (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์ของคำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                      |
| ---------------- | ---------- | -------- | ----------------------------------------------------------------------------- |
| Authorization    | string     | Header   | Bearer token สำหรับการยืนยันตัวตน OAuth2 (จำเป็น)                             |
| Accept           | string     | Header   | รูปแบบคำตอบที่ต้องการ เช่น `application/json` (ไม่บังคับ ค่าเริ่มต้นคือ JSON) |

### **คำตอบ**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                           |
| ---- | ---------------------- | ------------------------------------------------------------------ |
| 200  | สำเร็จ (OK)            | กรองข้อมูลสำเร็จ คำตอบมีรายละเอียดของ оперation อยู่               |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)            |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                      |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                  |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์                         |

## วิธีใช้ Get public key API ผ่าน SDK

### **OpenAPI Specification**

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) นิยาม programming interface ที่สามารถเข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์ของคุณ

### **ใช้ Aspose.Cells Cloud SDK**

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดที่อยู่เบื้องหลัง ทำให้คุณสามารถใช้งานฟังก์ชัน get public key สำหรับ cells ได้อย่างง่ายดายด้วยโค้ดเพียงไม่กี่บรรทัด  
โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ต่อไปนี้คือตัวอย่างที่เป็นรูปธรรมสำหรับภาษาที่นิยมใช้มากที่สุด:

---