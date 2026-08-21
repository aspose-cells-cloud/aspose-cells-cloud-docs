---
title: "Aspose.Cells Cloud Web API - รับสถานะของ Aspose Cells Cloud"
second_title: "เอกสาร"
ArticleTitle: "รับสถานะของ Aspose.Cells Cloud"
linktitle: "รับสถานะของ Aspose.Cells Cloud"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, การตรวจสอบสุขภาพ, Excel, REST"
description: "ตรวจสอบสถานะสุขภาพของบริการ Aspose.Cells Cloud แบบเรียลไทม์"
weight: 100
---

รับสถานะสุขภาพของบริการ Aspose.Cells Cloud แบบเรียลไทม์

**ข้อกำหนดเบื้องต้น:** เพื่อเรียก API นี้ คุณต้องได้รับโทเคนการเข้าถึงแบบ Bearer โดยใช้ข้อมูลประจำตัวของลูกค้า Aspose Cloud ของคุณ แล้วใส่โทเคนนี้ในส่วนหัว `Authorization` ในรูปแบบ `Bearer {access_token}`

## **รับสถานะของ Aspose.Cells Cloud**

### **Web API**

จุดปลายทางใช้เมธอด HTTP **GET** และไม่จำเป็นต้องมีเนื้อหาคำขอ

```
GET https://api.aspose.cloud/v4.0/cells
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                               |
| ---------------- | ---------- | --------------------------- | --------------------------------------- |
| Authorization    | String     | Header                      | โทเคน Bearer สำหรับการพิสูจน์ตัวตน (จำเป็น) |
| format           | String     | Query                       | รูปแบบการตอบกลับที่ต้องการ เช่น `json` |

### **การตอบกลับ**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**โครงสร้างข้อมูลของการตอบกลับ**

| ฟิลด์     | ชนิดข้อมูล        | คำอธิบาย                                   |
| --------- | ----------------- | ------------------------------------------- |
| status    | string            | สถานะสุขภาพของบริการ (`OK`, `Degraded`, เป็นต้น) |
| service   | string            | ชื่อของบริการ                              |
| timestamp | string (ISO‑8601) | เวลาที่ตรวจสอบสถานะ                        |

API จะส่งข้อมูล JSON มาตรฐานที่รวมถึง **สถานะสุขภาพ** ปัจจุบันของบริการ Aspose.Cells Cloud

**โค้ดสถานะ HTTP**

- **200 OK** – บริการมีสุขภาพดี และการตอบกลับประกอบด้วยข้อมูลสถานะ
- **401 Unauthorized** – โทเคนการพิสูจน์ตัวตนหายไปหรือไม่ถูกต้อง
- **503 Service Unavailable** – บริการไม่สามารถให้บริการได้ในขณะนี้ เนื่องจากกำลังปรับปรุงหรือเกิดปัญหา

## วิธีใช้ API รับสถานะของ Aspose.Cells Cloud ด้วย SDK

### ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDK

การใช้ SDK จะช่วยให้การบูรณาการง่ายขึ้นและลดโค้ดที่ซ้ำซ้อน ซึ่ง SDK จะจัดการรายละเอียดเบื้องต้นทั้งหมด ทำให้คุณสามารถดึงสถานะการรันของ Aspose.Cells Cloud ได้อย่างง่ายดาย กรุณาดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อรับรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน