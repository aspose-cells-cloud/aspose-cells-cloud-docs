---
---
title: "API ย้ายไฟล์ของ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการย้ายไฟล์อย่างรวดเร็วในคลาวด์"
second_title: "เอกสาร"
ArticleTitle: "โซลูชันจัดการไฟล์ Excel แบบคลาวด์ที่มีประสิทธิภาพ – อินเทอร์เฟซสำหรับการย้ายไฟล์อย่างรวดเร็วในคลาวด์"
linktitle: "ย้ายไฟล์"
type: docs
url: /move-file/
keywords: "Aspose.Cells, Move File API, Cloud Storage, Excel API, File Management"
description: "วิธีการย้ายไฟล์ระหว่างโฟลเดอร์ต่างๆ ในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud โดยใช้ API ย้ายไฟล์รุ่น v4.0 – endpoint, พารามิเตอร์, ตัวอย่าง และลิงก์ SDK"
weight: 100
---

API **moveFile** ใช้สำหรับย้ายไฟล์จากตำแหน่งหนึ่งไปยังอีกตำแหน่งหนึ่งภายในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud ซึ่งช่วยให้คุณจัดระเบียบไฟล์และบริหารจัดการพื้นที่จัดเก็บข้อมูลได้อย่างมีประสิทธิภาพ

## **API สำหรับ Excel: ย้ายไฟล์**

### Web API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์ของคำขอสำหรับ API **moveFile** มีดังนี้

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                   |
| ---------------- | --------- | --------------------------- | ---------------------------------------------------------- |
| srcPath          | String    | Path                        | เส้นทางต้นทางของไฟล์ที่ต้องการย้าย                         |
| destPath         | String    | Query                       | เส้นทางปลายทางที่ไฟล์จะถูกย้ายไป                         |
| srcStorageName   | String    | Query                       | ชื่อพื้นที่จัดเก็บข้อมูลต้นทาง (ถ้ามี)                     |
| destStorageName  | String    | Query                       | ชื่อพื้นที่จัดเก็บข้อมูลปลายทาง (ถ้ามี)                    |
| versionId        | String    | Query                       | รหัสเวอร์ชันของไฟล์ (ถ้ามี)                                 |

### **การตอบกลับ**

หากคำขอมีความถูกต้อง จะได้รับการตอบกลับด้วย **HTTP 200 OK** โดยมีเนื้อหา JSON ว่างเปล่า

```json
{}
```

**โค้ดสถานะ HTTP**

| โค้ด HTTP | สถานะ HTTP            | คำอธิบาย                                                                 |
| --------- | --------------------- | ------------------------------------------------------------------------ |
| 200       | OK                    | เรียกใช้ Web API สำเร็จ โดยการตอบกลับจะประกอบด้วยรายละเอียดของคำสั่ง |
| 400       | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)          |
| 401       | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                           |
| 413       | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                               |
| 500       | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์โดยไม่คาดคิด                             |

## ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานของโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

---