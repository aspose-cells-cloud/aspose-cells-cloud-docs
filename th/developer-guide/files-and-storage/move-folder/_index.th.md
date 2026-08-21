---
---
title: "API ย้ายโฟลเดอร์ของ Aspose.Cells Cloud – ย้ายโฟลเดอร์ได้อย่างรวดเร็วในคลาวด์"
second_title: "เอกสาร"
ArticleTitle: "การจัดการไฟล์ Excel บนคลาวด์ – ย้ายโฟลเดอร์ได้อย่างรวดเร็วในคลาวด์"
linktype: "ย้ายโฟลเดอร์"
type: docs
url: /move-folder/
keywords: "Aspose.Cells, ย้ายโฟลเดอร์, พื้นที่จัดเก็บข้อมูลบนคลาวด์, API สำหรับ Excel"
description: "เรียนรู้วิธีย้ายโฟลเดอร์ภายในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud ผ่าน API ย้ายโฟลเดอร์แบบ RESTful ซึ่งประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL, รหัสข้อผิดพลาด และตัวอย่าง SDK สำหรับ C#, Java, Python เป็นต้น"
weight: 100
---

API นี้ใช้ย้ายโฟลเดอร์จากตำแหน่งหนึ่งไปยังอีกตำแหน่งหนึ่งภายในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud ช่วยให้คุณจัดระเบียบไฟล์และจัดการพื้นที่จัดเก็บข้อมูลบนคลาวด์ได้อย่างมีประสิทธิภาพ

## **API สำหรับ Excel: ย้ายโฟลเดอร์**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**ตัวอย่างคำสั่ง cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของ API **moveFolder** มีดังนี้

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------ |
| srcPath          | string    | Path     | เส้นทางเต็มของโฟลเดอร์ที่ต้องการย้าย เช่น `FolderA/`                     |
| destPath         | string    | Query    | เส้นทางปลายทางที่ต้องการย้ายโฟลเดอร์ไป เช่น `FolderB/`                  |
| srcStorageName   | string    | Query    | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บต้นทาง                                   |
| destStorageName  | string    | Query    | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บปลายทาง                                 |

**รายละเอียดพารามิเตอร์**

- **srcPath** – จำเป็นต้องระบุ เส้นทางของโฟลเดอร์ต้นทาง  
- **destPath** – จำเป็นต้องระบุ เส้นทางของโฟลเดอร์ปลายทาง  
- **srcStorageName** – ไม่บังคับ ตัวระบุของพื้นที่จัดเก็บต้นทาง  
- **destStorageName** – ไม่บังคับ ตัวระบุของพื้นที่จัดเก็บปลายทาง  

### **การตอบกลับ**

เมื่อการเรียก API สำเร็จ จะส่งกลับเนื้อหาการตอบกลับว่างเปล่าพร้อมสถานะ HTTP **200 OK** สำหรับข้อผิดพลาด จะส่งกลับในรูปแบบ JSON object ที่มีฟิลด์ `error`

**รหัสสถานะ HTTP**

| รหัส HTTP | สถานะ HTTP            | คำอธิบาย                                                           |
| --------- | --------------------- | ------------------------------------------------------------------ |
| 200       | OK                    | เรียกใช้ Web API สำเร็จ การตอบกลับจะมีรายละเอียดของ operation    |
| 400       | Bad Request           | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)    |
| 401       | Unauthorized          | JWT token ไม่ถูกต้องหรือไม่ได้ระบุ                                 |
| 413       | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500       | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด                        |

## OpenAPI Specification

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) กำหนด programming interface ที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

---