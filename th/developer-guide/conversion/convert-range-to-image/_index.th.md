---
title: "แปลงช่วงข้อมูลใน Excel เป็นรูปภาพ – API Aspose.Cells Cloud"
description: "แปลงช่วงข้อมูลที่ระบุจากไฟล์ Excel บนเครื่องเป็น PNG, JPEG, SVG, TIFF หรือ BMP ผ่าน REST API ของ Aspose.Cells Cloud – ไม่จำเป็นต้องอัปโหลดไฟล์สมุดงานทั้งหมด"
keywords: "Aspose.Cells Cloud, แปลงช่วงข้อมูลเป็นรูปภาพ, Excel API, รูปแบบภาพ, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

คำสั่งนี้จะอ่านไฟล์สเปรดชีตบนเครื่อง แปลงช่วงข้อมูลที่ระบุ และส่งคืนรูปภาพในรูปแบบสตรีมไบนารี

## วิธีการแปลงช่วงข้อมูลเป็นรูปภาพ

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเคน JWT</a>

## พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์   | ตำแหน่ง                          | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                                                 |
| ------------------ | --------------------------------- | ---------- | ------ | -------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data (`multipart/form-data`) | ไฟล์       | **ใช่**  | ไฟล์ Excel ที่ต้องการประมวลผล                                             |
| **worksheet**      | Query                             | สตริง       | **ใช่**  | ชื่อแผ่นงานที่มีช่วงข้อมูล (เช่น `Sheet1`)                                |
| **range**          | Query                             | สตริง       | **ใช่**  | พื้นที่เซลล์ที่ต้องการแปลง เช่น `A1:C10`                                 |
| **format**         | Query                             | สตริง       | **ใช่**  | รูปแบบของไฟล์รูปภาพที่ส่งออก (`png`, `jpeg`, `svg`, `tiff`, `bmp`)       |
| **printHeadings**  | Query                             | บูลีน       | ไม่จำเป็น | `true` เพื่อแสดงหัวตารางแถว/คอลัมน์ในรูปภาพ                               |
| **outPath**        | Query                             | สตริง       | ไม่จำเป็น | เส้นทางโฟลเดอร์สำหรับไฟล์ที่สร้างขึ้น หากต้องการจัดเก็บไว้ในพื้นที่เก็บข้อมูลบนคลาวด์ |
| **outStorageName** | Query                             | สตริง       | ไม่จำเป็น | ชื่อของบริการพื้นที่เก็บข้อมูล (เช่น `MyStorage`)                          |
| **fontsLocation**  | Query                             | สตริง       | ไม่จำเป็น | URL หรือเส้นทางไปยังฟอนต์ที่กำหนดเองซึ่งใช้ระหว่างการแปลง               |
| **region**         | Query                             | สตริง       | ไม่จำเป็น | ตัวระบุภาษาและภูมิภาค (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลขและวันที่ |
| **password**       | Query                             | สตริง       | ไม่จำเป็น | รหัสผ่านสำหรับสมุดงานที่เข้ารหัส                                            |
| **AutoRowsFit**    | Query                             | บูลีน       | ไม่จำเป็น | ปรับขนาดแถวอัตโนมัติก่อนการเรนเดอร์                                       |
| **AutoColumnsFit** | Query                             | บูลีน       | ไม่จำเป็น | ปรับขนาดคอลัมน์อัตโนมัติก่อนการเรนเดอร์                                  |

## การตอบกลับ

API จะส่งคืนไฟล์ HTML ที่แปลงแล้วเป็น **สตรีมไบนารี** (`application/octet-stream`)

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### ตัวอย่างการตอบกลับที่สำเร็จ (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

บันทึกเนื้อหาของส่วนตอบกลับเป็นไฟล์ (เช่น `report.png`) เพื่อดูรูปภาพที่เรนเดอร์แล้วในเบราว์เซอร์

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย                                                          |
| ---- | ----------------------- | ------------------------------------------------------------------ |
| 200  | สำเร็จ (OK)            | ใช้ตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)     |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                      |
| 413  | ข้อมูลส่งข้อมูลมากเกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                  |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                           |

## วิธีใช้ API แปลงช่วงข้อมูลเป็นรูปภาพพร้อม SDK?

### ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) ระบุ API ที่สามารถเข้าถึงได้สาธารณะ ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้เบื้องหลัง ทำให้คุณสามารถแปลงช่วงข้อมูลเป็นไฟล์รูปภาพได้โดยใช้โค้ดเพียงไม่กี่บรรทัด  
สำรวจรายการ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [คลัง GitHub ของเรา](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ หากไม่สามารถโหลดจาก Gist ได้ คุณสามารถดาวน์โหลดตัวอย่างโดยตรงจากคลังได้

---