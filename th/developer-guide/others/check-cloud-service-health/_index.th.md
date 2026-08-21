---
title: "Aspose.Cells Cloud – ตรวจสอบสุขภาพของบริการ (API)"
second_title: "เอกสาร"
ArticleTitle: "การตรวจสอบสุขภาพของ Aspose.Cells Cloud"
linktitle: "ตรวจสอบสุขภาพของบริการคลาวด์"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud, การตรวจสอบสุขภาพ API, สถานะ REST, การตรวจสอบบริการคลาวด์"
description: "ตรวจสอบสุขภาพของ Aspose.Cells Cloudแบบเรียลไทม์ เรียนรู้เกี่ยวกับจุดปลายทาง GET /v4.0/cells/status/check พารามิเตอร์ รูปแบบการตอบกลับ และตัวอย่าง SDK"
weight: 100
---

ตรวจสอบสถานะสุขภาพของบริการ Aspose.Cells Cloud

**ข้อกำหนดเบื้องต้น**  
ในการเรียกใช้จุดปลายทางนี้ คุณต้องมีโทเค็นการเข้าถึง Aspose Cloud ที่ถูกต้อง รับโทเค็นโดยการลงทะเบียนแอปพลิเคชันในแดชบอร์ด Aspose Cloud แล้วใช้ client-id และ client-secret เพื่อขอโทเค็น Bearer ผ่านจุดปลายทาง OAuth2 token ใส่โทเค็นนี้ใน header `Authorization` ดังตัวอย่างด้านล่าง

## **ตรวจสอบสุขภาพของบริการคลาวด์**

### **เว็บ API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยสูงและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์คำขอ**

| พารามิเตอร์   | ประเภท   | จำเป็น | คำอธิบาย                                                          |
| ------------- | -------- | ------ | ------------------------------------------------------------------ |
| Authorization | header   | ใช่     | Bearer token สำหรับการยืนยันตัวตน (`Authorization: Bearer <token>`) |
| detail        | query    | ไม่บังคับ | ตั้งค่าเป็น `true` เพื่อรวมข้อมูลรายละเอียดของคอมโพเนนต์         |
| Accept        | header   | ไม่บังคับ | รูปแบบการตอบกลับที่ต้องการ ค่าเริ่มต้นคือ `application/json`      |

### **การตอบกลับ**

เมื่อคำขอยังผลสำเร็จ บริการจะส่ง JSON payload กลับมา

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Operational",
    "storage": "Operational",
    "database": "Operational"
  }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย             | คำอธิบาย                                              |
| ---- | ------------------- | -------------------------------------------------------- |
| 200  | สำเร็จ (OK)         | บริการอยู่ในสภาวะปกติ ดูตัวอย่าง JSON ได้จากด้านบน     |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็นการยืนยันตัวตนไม่ถูกต้องหรือขาดหายไป             |
| 503  | บริการไม่พร้อมใช้งาน (Service Unavailable) | บริการปัจจุบันไม่อยู่ในสภาวะปกติหรืออยู่ระหว่างการบำรุงรักษา |
| 4xx  | ข้อผิดพลาดของไคลเอนต์ (Client error) | พารามิเตอร์คำขอไม่ถูกต้องหรือคำขอผิดรูปแบบ             |
| 5xx  | ข้อผิดพลาดของเซิร์ฟเวอร์ (Server error) | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด; ลองใหม่อีกครั้งในภายหลัง |

## วิธีใช้ Aspose.Cells Cloud Status API ด้วย SDK

### **OpenAPI Specification**

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> กำหนด programming interface ที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

### **ใช้ Aspose.Cells Cloud SDK**

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งพัฒนา SDK จะจัดการรายละเอียดพื้นหลังให้คุณสามารถใช้การตรวจสอบสุขภาพของบริการคลาวด์สำหรับ Cells ด้วยโค้ดน้อยที่สุด  
โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud อย่างครบถ้วน

ด้านล่างนี้คือตัวอย่างโค้ดที่แสดงวิธีการเรียกใช้จุดปลายทางการตรวจสอบสุขภาพด้วย SDK ที่นิยมใช้กันมากที่สุด

---