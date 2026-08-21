---
---
title: "เริ่มต้นใช้งาน Aspose.Cells Cloud API – ประมวลผลไฟล์ Excel ใน 3 ขั้นตอนง่ายๆ"
second_title: "เอกสาร"
ArticleTitle: "เริ่มต้นใช้งาน Aspose.Cells Cloud"
linktitle: "เริ่มต้นใช้งาน"
type: docs
url: /th/getting-started/
description: "เรียนรู้วิธีอัปโหลด แปลง และดาวน์โหลดไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API ในสามขั้นตอนง่ายๆ พร้อมตัวอย่างโค้ด cURL"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, การแปลงสเปรดชีต, Excel เป็น PDF, สเปรดชีตบนคลาวด์, Aspose.Cells Cloud API"
---

- [ภาพรวม](/th/cells/overview/)
- [คู่มือด่วน](/th/cells/quickstart/)
- [SDK ที่มีให้ใช้งาน](/th/cells/available-sdks/)
- [แพลตฟอร์มที่รองรับ](/th/cells/supported-platforms/)
- [รูปแบบไฟล์ที่รองรับ](/th/cells/supported-file-formats/)
- [ทดลองใช้ Aspose.Cells Cloud](/th/cells/evaluate-aspose-cells/)
- [แผนค่าบริการ](/th/cells/pricing-plan/)
- [การสนับสนุนทางเทคนิค](/th/cells/technical-support/)
- [วิธีรัน Docker Container](/th/cells/how-to-run-docker-container/)

**คู่มือเริ่มต้นใช้งาน**

ก่อนเริ่มต้น คุณต้องมี **คีย์ API ของ Aspose Cloud** และ **ชื่อพื้นที่จัดเก็บข้อมูล (storage name)** ที่ถูกต้อง เอกสารรับรองเหล่านี้จำเป็นสำหรับการเรียกใช้งาน API ทั้งหมดในขั้นตอนต่อไป

**ขั้นตอนที่ 1: อัปโหลดไฟล์ Excel**  
อัปโหลดสมุดงานต้นทางของคุณไปยังพื้นที่จัดเก็บข้อมูลของ Aspose Cloud

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*เนื้อหาคำขอ*: ไฟล์จะถูกส่งเป็นสตรีมไบนารี (`application/octet‑stream`)  
*พารามิเตอร์ที่จำเป็น*:

- `path` – ตำแหน่งในพื้นที่จัดเก็บข้อมูลที่จะบันทึกไฟล์ (เช่น `folder/sample.xlsx`)

**ขั้นตอนที่ 2: แปลงสมุดงานเป็น PDF**  
ส่งคำขอแปลงหลังจากไฟล์ถูกจัดเก็บแล้ว

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*พารามิเตอร์ที่จำเป็น*:

- `name` – ชื่อสมุดงานที่อัปโหลดแล้ว (เช่น `sample.xlsx`)  
- `format` – รูปแบบปลายทาง (`pdf`)  
- `outputPath` – ตำแหน่งในพื้นที่จัดเก็บข้อมูลที่จะบันทึกไฟล์ที่แปลงแล้ว (เช่น `folder/result.pdf`)

*ตัวอย่างเนื้อหาการตอบกลับ* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**ขั้นตอนที่ 3: ดาวน์โหลดไฟล์ PDF ที่แปลงแล้ว**  
ดึงไฟล์ PDF ที่ได้รับจากพื้นที่จัดเก็บข้อมูล

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*พารามิเตอร์ที่จำเป็น*:

- `outputPath` – ตำแหน่งไฟล์ PDF ที่สร้างขึ้นในขั้นตอนก่อนหน้า

**สรุปตัวอย่างคำขอ / การตอบกลับ**

| การดำเนินการ | HTTP Method | Endpoint (ตัวอย่าง) | พารามิเตอร์ | สถานะที่ประสบความสำเร็จ |
|-------------|-------------|--------------------|------------|------------------------|
| อัปโหลด     | PUT         | /cells/storage/file/{path} | `path` (ตำแหน่งพื้นที่จัดเก็บ) | 200 OK |
| แปลง       | POST        | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| ดาวน์โหลด   | GET         | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**รหัสข้อผิดพลาดที่พบบ่อย**

- **400 Bad Request** – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง  
- **401 Unauthorized** – โทเคนการเข้าถึงไม่ถูกต้องหรือขาดหาย  
- **404 Not Found** – ไฟล์หรือตำแหน่งที่ระบุไม่มีอยู่จริง  
- **500 Internal Server Error** – ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์; ลองใหม่หรือติดต่อฝ่ายสนับสนุน