---
title: "แยกตาราง"
ArticleTitle: "Split Table – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "Split Table"
type: docs
url: /th/cells/split/table
aliases: []
keywords: "Aspose.Cells, แยกตาราง, API"
description: "API สำหรับแยกตารางในไฟล์สเปรดชีตตามค่าในคอลัมน์"
weight: 1
---

## SplitTable ของ Aspose.Cells Cloud Web Services

เมธอดนี้ดำเนินการแยกข้อมูลจากตารางต้นฉบับ โดยจัดกลุ่มแถวตามค่าที่ไม่ซ้ำกันในคอลัมน์ที่ระบุ จากนั้นประมวลผลแต่ละกลุ่มข้อมูล (สำหรับค่าที่แยกแต่ละค่า) เป็นหน่วยข้อมูลแยกต่างหาก ปลายทางการส่งออกจะถูกควบคุมด้วยพารามิเตอร์บูลีนหลัก 2 ตัว:

- กำหนดโครงสร้างสมุดงาน: ถ้าเป็น `true` แต่ละหน่วยที่แยกจะถูกบันทึกในไฟล์สมุดงานแยกต่างหาก หากเป็น `false` แต่ละหน่วยจะกลายเป็นแผ่นงานใหม่ภายในสมุดงานปัจจุบัน
- กำหนดการแพ็กเกจผลลัพธ์: เมื่อตั้งค่าเป็น `true` และใช้ร่วมกับ `toNewWorkbook` = `true` เมธอดจะสร้างไฟล์หลายไฟล์และส่งคืนเป็นไฟล์ ZIP อาร์คีฟ หากเป็น `false` ข้อมูลทั้งหมดจะถูกรวมเข้าไว้ในไฟล์เดียว (สมุดงานหลายแผ่นหรือไฟล์เดียวตามการตั้งค่าอื่นๆ)

### ปลายทางของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบ JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|---------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | String  | Query                       | แผ่นงานที่มีตาราง |
| tableName        | String  | Query                       | ตารางข้อมูลที่ต้องการแยก |
| splitColumnName  | String  | Query                       | ชื่อคอลัมน์ที่ใช้ในการแยก |
| saveSplitColumn  | Boolean | Query                       | กำหนดว่าจะเก็บข้อมูลในคอลัมน์ที่ใช้แยกหรือไม่ |
| splitRowNumber   | Integer | Query                       | [TBD] |
| toNewWorkbook    | Boolean | Query                       | การควบคุมปลายทางการส่งออก: true — สร้างไฟล์สมุดงานใหม่ที่มีข้อมูลที่แยกแล้ว; false — เพิ่มแผ่นงานใหม่ลงในสมุดงานปัจจุบัน |
| toMultipleFiles  | Boolean | Query                       | true — ส่งออกข้อมูลตารางเป็น **หลายไฟล์แยกต่างหาก** (ส่งคืนเป็นไฟล์ ZIP); false — เก็บข้อมูลทั้งหมดใน **ไฟล์เดียว** ที่มีหลายแผ่นงาน ค่าเริ่มต้น: false |
| outPath          | String  | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่สมุดงานจะถูกบันทึก ค่าเริ่มต้นคือ null |
| outStorageName   | String  | Query                       | ชื่อพื้นที่จัดเก็บไฟล์ผลลัพธ์ |
| fontsLocation    | String  | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| region           | String  | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภาษาท้องถิ่น |
| password         | String  | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ**

```json
{
  "file": "stream ไบนารี (ไฟล์ ZIP หรือสมุดงาน ขึ้นอยู่กับพารามิเตอร์)"
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200  | สำเร็จ (OK) | การแยกข้อมูลเสร็จสมบูรณ์ ผลตอบกลับประกอบด้วยไฟล์ที่สร้างขึ้น (ไฟล์ ZIP หรือสมุดงาน) |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | URL หรือพารามิเตอร์ของคำขอไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | การตรวจสอบสิทธิ์ล้มเหลวหรือไม่มีการให้ข้อมูลยืนยันตัวตน |
| 404  | ไม่พบ (Not Found) | ไฟล์ต้นฉบับไม่สามารถเข้าถึงได้ |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ขนาดของข้อมูลในคำขอเกินขีดจำกัดที่อนุญาต |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | สเปรดชีตเกิดข้อผิดพลาดระหว่างการดึงข้อมูล |

## วิธีใช้ SplitTable ด้วย SDK

### ข้อมูลเฉพาะของ SplitTable

[Splittable API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึง Aspose.Cells Cloud web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "stream ไบนารี (ไฟล์ ZIP หรือสมุดงาน ขึ้นอยู่กับพารามิเตอร์)"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ให้คุณโฟกัสไปที่งานในโครงการของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้ Aspose Cells Cloud web services ผ่าน SDK ต่างๆ:
`[TBD]`
---